
# Wishful and ambitious try 

Collection 

# Sustainable and Intelligent Connectivity for Low-Altitude Wireless Networks

Submission status

Open

Submission deadline

13 October 2026 - try for this collection 


1. RCP methods 
2. Physical and logical link analysis 
3. Protocol level C2 link 

**Aviation reliability analysis** leans heavily on a small set of tools, mostly borrowed from systems safety engineering rather than communications theory:

- **Continuous-time Markov chains (CTMC)** are the workhorse — used for avionics system reliability (e.g. modular avionics reconfiguration analysis) and more broadly for modeling failure/recovery transitions, computing probability of failure per hour and related integrity metrics that map directly onto IEC 61508-style safety parameters.
- **Reliability Block Diagrams (RBD)** combined with survival/hazard functions — one cross-layer framework models a wireless link's reliability from packet generation through PHY/MAC/network/application layers using non-repairable-system survival analysis, treating "availability" as the probability a reliable transmission link is present.
- **Generalized Stochastic Petri Nets** for dispatch reliability, and Markov techniques generally, for backup/redundancy compensation modeling.
- On the navigation-integrity side (closest cousin to your "integrity" RCP parameter), **ARAIM for GNSS** builds explicit stochastic error models — Gaussian bounds on orbit/clock error, elevation-dependent variance models — validated against both simulation and real data, specifically to support continuity/availability/integrity guarantees for safety-of-life applications. This is a genuinely useful template because it's solving almost exactly your problem: turning noisy technical measurements into formal integrity/continuity/availability numbers under a certification-grade definition.

**The gap in this list:** none of these methods were built to reconcile heterogeneous RAT statistics. CTMC/RBD approaches assume you already have a well-characterized failure process; they don't tell you how to derive that process consistently from raw 3GPP-style KPIs across structurally different technologies.

### Telecom-side statistical machinery you can borrow

- **Finite-State Markov Channel (FSMC) models** — the standard way to capture burst/correlated fading behavior (rather than treating samples as i.i.d.), used extensively in wireless networked control to derive stability guarantees from channel state transitions.
- These models have also been _learned_ from data via regression trees rather than assumed a priori, which matters for you: with a short campaign you won't want to hand-pick a channel model, you'll want to fit one from what you actually observe.

RCP's continuity and integrity parameters are fundamentally about the _probability of rare, severe events_ — not average behavior. Extreme Value Theory (specifically Peak-Over-Threshold with the Generalized Pareto Distribution) was developed precisely to estimate tail/rare-event probabilities **from limited data**, rather than requiring massive datasets to observe enough rare events directly — recent work explicitly frames EVT as solving the case where "gathering large datasets and fitting them to standard statistical distributions often fails to represent the tail behavior, due to scarcity of such events." There's also a documented method for building confidence intervals into EVT-based rate/reliability estimates specifically to cope with limited training data.

This is a strong fit for your 20–30 minute, 2–3 repetition sessions: you're not trying to empirically observe a 10⁻⁵ outage event, you're using EVT to extrapolate the tail from the moderate exceedances you _can_ observe. That's the standard justification in the URLLC literature, and it transfers cleanly to your RCP-integrity claim.

Multivariate EVT extensions go further and model the **joint tail across multiple channels/links simultaneously**, using a Poisson point process approach to capture how rare events on different links are correlated — this is directly applicable to your multi-RAT fusion problem, since RCP-relevant failure should really be assessed on the _fused_ link, not independently per RAT.

### The satellite/space-specific piece (for your Iridium/LEO link)

Terrestrial fading statistics don't transfer to LEO propagation, which is why this domain has its own modeling tradition: **Land Mobile Satellite (LMS) channel models**, almost always Markov-based (two-state, three-state, up to six-state formulations), capturing elevation-angle-dependent shadowing and signal envelope fluctuation as the satellite moves across the sky. This is essentially the same FSMC idea as above, but with domain-specific state definitions tuned to satellite geometry rather than terrestrial multipath — which is exactly the kind of "technology-specific bias" you're trying to formalize and correct for in your mapping.

### How this fits together as your methodology

A defensible pipeline, and arguably your paper's real novelty (nobody currently combines these three literatures):

1. **Per-RAT state-space modeling** — fit an FSMC (or LMS-style Markov model for the satellite link) to each RAT's measured KPI time series, capturing burst/correlation structure rather than treating samples as independent.
2. **Tail estimation via EVT/POT** — from the same short sessions, fit a Generalized Pareto Distribution to threshold exceedances per RAT to get defensible rare-event/outage probabilities despite limited samples, with bootstrapped confidence intervals to be honest about uncertainty given your sample size.
3. **RCP parameter derivation** — map: Markov steady-state probabilities → Availability; sojourn-time-in-degraded-state distributions → Continuity/transaction expiration time; EVT tail exceedance probabilities → Integrity (undetected severe degradation).
4. **Bias correction / normalization** — because each RAT's state-space and tail parameters are fit independently with technology-appropriate structure (terrestrial FSMC vs. LMS-style satellite model), the "bias correction" is explicit and inspectable: you're not forcing one channel model onto structurally different physics, you're deriving a common RCP-scale output from technology-native models.
5. **Multivariate/joint tail step (optional but strong)** — if you have time, applying multivariate EVT across your two RATs to characterize joint outage probability would directly demonstrate the "fusion improves RCP" claim quantitatively, which is a compelling result even from a short campaign.

This gives reviewers something methodologically rigorous to evaluate even with a modest dataset, because the statistical tools you'd be using (EVT, FSMC) are specifically designed for exactly your data regime, and the combination — aviation Markov/RBD tradition + URLLC-style EVT tail modeling + satellite-specific LMS models, unified through an RCP-mapping layer — doesn't currently exist as a single framework in the literature I found.

Good — you now have exactly the three metric families the fusion problem needs: physical-layer state (SINR/RSSI), logical/application-layer outcome (MAVLink packet error/latency/throughput), and a controlled synthetic load (iperf/RTT) to decouple "what the network does" from "what MAVLink's variable telemetry rate happens to produce." Here's a concrete pipeline.

## Why you need two fusion stages, not one

You're actually fusing along two different axes, and conflating them is where these mapping attempts usually go wrong:

1. **Vertical fusion** (within one RAT): physical state → logical outcome. This is where "technology-specific bias" literally lives — the same SINR value means a different packet-error probability on terrestrial 5G than on a LEO link with elevation-dependent shadowing.
2. **Horizontal fusion** (across RATs): combining the compliance states of multiple links into one end-to-end RCP figure, assuming some redundancy/switching policy.

Treat these as two separate, chained models rather than one big regression — it's both more defensible statistically and it's the part reviewers can actually audit.

## Stage 1 — Vertical fusion: physical state → logical compliance (the bias-correction step)

- **Discretize the physical metric into states per RAT.** Bin SINR/RSSI into 3–5 states (e.g., good / marginal / poor), using RAT-appropriate thresholds rather than one universal cutoff — 3GPP coverage thresholds for 5G, C/N0-style thresholds for Iridium. This gives you a physical state sequence per RAT, which is also your input to the FSMC modeling discussed earlier.
- **Define "compliant" on the logical side** using your RCP-derived thresholds — e.g., latency < X ms, packet error rate < Y over a MAVLink transaction window — so each logical sample becomes a binary compliant/non-compliant label.
- **Fit a conditional model of compliance given physical state, per RAT** — logistic regression is the honest choice for a small dataset (interpretable, doesn't overfit): `P(compliant | physical_state, RAT)`. Including a RAT × physical_state interaction term is exactly how you formally estimate "the bias" — it's a specific, reportable coefficient, not a hand-wave.
- This step is also how you make the most of a short campaign: physical-layer samples are cheap and fast (you can log SINR at high rate), while logical-layer "failure" events are comparatively rare. Cross-layer analysis has been used elsewhere specifically to propagate physical-layer statistics into higher-layer reliability estimates rather than requiring dense observation at every layer independently — same idea here.

## Stage 2 — Horizontal fusion: combining RATs into an end-to-end figure

- **Don't assume independence between RATs by default — test it.** If two RATs' degradation events are correlated (shared environment, weather, geometry), naively multiplying single-RAT reliabilities overstates your fused availability. A copula-based dependency model is the standard tool for capturing this without forcing a full joint parametric distribution, and it's been used elsewhere specifically to reconstruct cross-mode dependence for system-level reliability under correlated failure modes — directly transferable to "is my 5G outage independent of my mesh WiFi outage."
- Practically, with only two RATs and a short campaign, you don't need a sophisticated copula — even checking empirical correlation of compliance-indicator time series per condition, and reporting whether the fused-reliability gain closely matches the independence assumption or falls short of it, is a legitimate and reportable result.
- **Simulate the fused process** by combining the fitted per-RAT Markov/FSMC models under your chosen redundancy policy (e.g., "use best available," or "primary-with-failover") via Monte Carlo, rather than trying to derive it in closed form — this is standard practice when RATs have different state-space definitions and makes the pipeline extensible to a third RAT later without re-deriving equations.

## From the fused model to your three RCP parameters

- **Availability** — the steady-state probability, from the fused Markov model, that at least one RAT is in a compliant state. This is a direct output of Stage 2's Monte Carlo/Markov fusion.
- **Continuity** — reframe as a first-passage/sojourn-time question: given compliance at the start of a transaction of duration T (your MAVLink command→ack window is a natural, literal definition of "transaction" here — COMMAND_LONG to COMMAND_ACK), what's the probability of remaining compliant throughout T? This is computable analytically from the Markov chain via phase-type/absorbing-state methods, and — importantly — you can also validate it empirically against your actual logged MAVLink command-ack success/failure sequence, which gives you a real accuracy check on the model rather than pure simulation.
- **Transaction time** — this one you measure most directly: MAVLink command-ack round-trip time and iperf/ICMP RTT give you the empirical distribution. Report it as a percentile with a confidence interval (e.g., 95th/99th percentile via bootstrap) rather than a mean, and use EVT/POT on the upper tail if you want a defensible extrapolated worst-case bound beyond what you directly observed — this is where the earlier EVT discussion plugs in concretely.

## Practical note on the two logical-metric sources

Use iperf/RTT and MAVLink traffic for different jobs rather than treating them as redundant: iperf gives you a controlled, RAT-comparable load so throughput/loss differences reflect the network, not MAVLink's own variable telemetry rate; MAVLink traffic gives you the actual application-relevant transaction semantics (command-ack pairs) that Continuity and Transaction Time should be defined against. Reporting both — "here's the clean network-level characterization" and "here's what it means for a real C2 transaction" — is a stronger, more legible result than either alone, and gives reviewers an easy sanity check that your RCP numbers aren't an artifact of one measurement method.

This whole pipeline — RAT-specific FSMC + explicit bias term via interaction regression + copula/joint fusion + EVT tail estimation, chained through to RCP-native outputs — is the paper's real contribution. It's worth stating that combination explicitly in your framing, since none of the individual pieces are new but the chain from raw heterogeneous KPIs to certification-relevant RCP parameters, with the bias term made explicit and testable, is.