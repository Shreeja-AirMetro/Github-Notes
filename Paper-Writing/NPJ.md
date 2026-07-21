
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


Good instinct — RCP alone (even with Integrity added, which I hadn't fully covered) doesn't capture the whole regulatory picture your paper needs to gesture at. Here's the fuller landscape.

## The missing RCP parameter: Integrity

I gave you Availability, Continuity, and Transaction Time — the fourth JARUS C2 link RCP parameter is **Integrity**, defined around _undetected_ loss or corruption of service, distinct from Continuity's _detected_ loss. This matters for your data pipeline: it requires you to be able to tell the difference between "packet was lost and MAVLink/your transport knows it" versus "packet was corrupted/delayed and nothing flagged it" — the latter needs sequence-number or checksum-level scrutiny of your MAVLink stream, not just throughput/loss counters. Worth at least scoping explicitly whether your paper addresses Integrity or defers it, since it's the hardest of the four to instrument.

## RSP — the sibling standard, likely relevant to your setup

RCP doesn't exist alone in ICAO's framework — it's paired with **Required Surveillance Performance (RSP)** under the Performance-Based Communication and Surveillance (PBCS) concept, where RCP governs the communication element and RSP the surveillance element, with RSP itself decomposed into surveillance data delivery time, continuity, availability, and integrity. This is directly relevant to you: **MAVLink carries both command traffic and telemetry/position reporting simultaneously**, meaning your link is arguably serving both an RCP function (commands) and an RSP-like function (position/state reporting back to the ground station) at once. If a reviewer familiar with PBCS reads your paper, they'll expect you to acknowledge this — either scope explicitly to C2/RCP and treat telemetry as a different traffic class you're not certifying against RSP, or explicitly extend your mapping methodology to both. Either is defensible, but leaving it unaddressed reads as a gap.

## RNP/PBN — not your metric, but shapes your test conditions

**Required Navigation Performance (RNP)**, under the Performance-Based Navigation (PBN) framework, is paired conceptually with RCP/RSP as the third leg of the performance-based CNS model — RPAS ConOps explicitly states that C2 link performance requirements must be adequate to support both RCP and PBN specifications together, since airspace access ultimately depends on both being satisfied jointly. You won't measure RNP directly, but it's worth using PBN corridor/route concepts to justify your test matrix's operating conditions (range, altitude, maneuver profile) — grounds your "handover event," "varying range" test conditions in something regulators actually use to define airspace segments, rather than ad hoc scenario choice.

## SORA/SAIL/OSO — this is the actual mechanism your work would need to plug into

This is probably the most valuable addition for your paper's framing. ICAO-adjacent regulators (via JARUS, adopted by EASA, UK CAA, and others) don't approve BVLOS operations by checking RCP numbers directly — they use the **Specific Operations Risk Assessment (SORA)** process, which derives a **Specific Assurance and Integrity Level (SAIL)** from the operation's ground and air risk, and then requires evidence of **robustness** (a combined integrity + assurance rating: optional/low/medium/high) against 24 **Operational Safety Objectives (OSOs)** — several of which are specifically about C2 link performance and loss-of-link procedures. Robustness requirements scale with SAIL — semi-rural BVLOS operations already require documented C2 link reliability evidence at SAIL II, and this evidence burden increases sharply at SAIL III/IV. There's also recent work (MDPI, 2026) explicitly identifying SAIL III/IV C2-link evidence generation as _the_ current bottleneck in BVLOS regulatory approval, arguing existing work addresses either individual technical solutions or high-level risk analysis but not a systematic bridge between the two.

That's a genuinely strong hook for your paper's motivation: your RCP-mapping methodology is, in effect, a candidate mechanism for generating the traceable, quantitative C2-link robustness evidence that SORA's OSOs demand but that (per that 2026 paper) doesn't currently have a systematic technical pathway. Citing this connects your contribution to a live regulatory pain point, not just an abstract standards gap — reviewers in an applied journal respond well to that.

## Detect-and-Avoid (DAA) — a scope boundary worth stating explicitly

BVLOS operations under SORA also carry **Tactical Mitigation Performance Requirements (TMPR)** for Detect-and-Avoid, with their own robustness levels tied to residual air risk. DAA has its own timing-critical data needs (potentially sharing bandwidth/links with C2). You don't need to measure this, but explicitly stating "DAA traffic and its performance requirements are out of scope; this work addresses C2 only" preempts a reviewer question about whether your link characterization accounts for contention from safety-critical DAA traffic on the same physical links.

## The anchor above all of these: Target Level of Safety (TLS)

Every one of RCP/RSP/RNP and SORA's SAIL/OSO robustness levels ultimately trace back to a **Target Level of Safety** — the quantitative safety objective (e.g., an acceptable fatal-accident rate per flight hour) that the whole performance-based framework exists to satisfy. You don't need to derive numbers against TLS, but one sentence in your introduction or discussion connecting "RCP parameters exist to demonstrably support a TLS" shows you understand _why_ the four RCP parameters are the ones that matter, rather than treating them as an arbitrary checklist — which materially strengthens the paper's framing for reviewers from the aviation side.

**For your paper**, I'd suggest a short subsection (half a page) situating your RCP-mapping methodology within this wider PBCS/SORA landscape — explicitly stating what you address (RCP, C2 only) and what you deliberately scope out (RSP/telemetry, DAA/TMPR, RNP) — rather than trying to cover all of it. That scoping statement is what turns "here's a metric mapping" into "here's a methodology positioned correctly within the actual regulatory pathway BVLOS operators need to satisfy."

That's the shape your scoping subsection can follow: TLS anchors the whole framework, SORA determines what evidence is actually required (SAIL/OSO), and that requirement fans out across four performance domains — RCP, RSP, RNP, DAA/TMPR — of which your methodology addresses only RCP for the C2 link.

In the half-page write-up, I'd keep this same order: one sentence on TLS/SORA as the reason RCP matters at all, one sentence naming the sibling domains (RSP, RNP, DAA/TMPR) and why each is out of scope, then transition straight into your RCP-mapping contribution. That's the paragraph a reviewer needs to see you've thought about the full picture without trying to solve all of it.
![[rcp_scope_within_pbcs_sora.png]]

A few concrete reasons, any of which you can use directly in the scoping paragraph:

**RSP and RCP are formally separate specifications, even on the same link.** Under ICAO's PBCS framework, RCP governs the _communication_ function (commands to the aircraft) while RSP governs the _surveillance_ function (position/state data back to the ground) — each with its own delivery-time, continuity, availability, and integrity parameters, evaluated and certified separately even when carried over the same physical channel. Your MAVLink stream happens to carry both command traffic and telemetry, but that's an implementation detail of MAVLink, not a reason to treat them as one regulatory object.

**The compliance thresholds don't transfer.** RSP designators (like RSP180) are defined against ATC surveillance-data-delivery expectations in a specific oceanic/procedural airspace context — they're not directly reusable for UAS telemetry without a separate derivation exercise. Folding RSP in would mean justifying a second set of thresholds from scratch, which is real additional work, not just relabeling your existing RCP thresholds.

**It keeps your contribution legible.** Your mapping methodology's whole value is a clean chain: heterogeneous physical/logical metrics → one well-defined target (RCP). Adding RSP mid-paper turns one mapping problem into two, and a reviewer has to hold both threshold systems in mind to evaluate either — that dilutes rather than strengthens the standards-contribution framing.

**It matches your realistic scope.** You have a bounded September campaign and a C2-transaction-centered methodology (MAVLink command→ack). Extending the empirical case study to also validate RSP-style delivery-time claims for telemetry would need its own test conditions and thresholds you haven't built yet.

**It's a natural, low-cost future-work line, not a dead end.** Because your pipeline (FSMC + EVT + bias-correction per RAT) is target-framework-agnostic, you can close the scoping paragraph by noting the same methodology extends to RSP by substituting its parameter definitions — signaling foresight without having to deliver it now.

A ready-to-adapt sentence: _"While the same physical links also carry telemetry data relevant to RSP, this work addresses only the C2/RCP function; extending the proposed mapping to RSP's delivery-time and continuity parameters is a natural but separate direction, left to future work."_

## Formal setup

Let $r \in {5G, LEO, Mesh}$ index the RATs, and $t$ index discrete sample times at interval $\Delta t$.

**Physical layer:** $X_r(t) = (SINR_r(t), RSSI_r(t))$. Discretize into a physical state via quantization: $s_r(t) = \phi(X_r(t)) \in {1,\dots,K}$.

**Logical layer (MAVLink):** packet-error indicator $e_r(t)\in{0,1}$, latency $L_r(t)$ (command→ack), throughput $Th_r(t)$.

**Active probes:** $L_r^{iperf}(t)$, $Th_r^{iperf}(t)$ (controlled-rate reference), $L_r^{RTT}(t)$ (ICMP/RTT baseline).

**Compliance indicator**, thresholds set by the target RCP type: $$C_r(t) = \mathbb{1}{e_r(t)=0 ;\wedge; L_r(t)\le L_{max};\wedge;Th_r(t)\ge Th_{min}}$$

## Stage 1 — vertical fusion (the bias-correction term)

Model logical compliance conditional on physical state, per RAT, with an explicit RAT-interaction term: $$\text{logit},P(C_r(t)=1 \mid s_r(t)) = \alpha + \beta, s_r(t) + \gamma_r + \delta_r, s_r(t)$$

$\gamma_r,\delta_r$ are your formal, reportable "technology-specific bias" coefficients — the same SINR bin producing different compliance probability on 5G vs. Iridium is captured exactly by $\delta_r$.

## Stage 2 — per-RAT Markov model → Availability

Estimate transition probabilities empirically from the joint (physical-state × compliance) sequence: $$p^r_{ij} = \frac{N^r_{i\to j}}{N^r_i}$$

Steady-state $\pi_r$ solves $\pi_r P_r = \pi_r,; \sum_i \pi_r(i)=1$. Then: $$Availability_r = \sum_{j\in G} \pi_r(j)$$ where $G$ is the set of compliant states.

## Continuity — first-passage over the transaction window

Let $T$ = transaction duration (from your MAVLink command→ack cycle, or the RCP type's transaction expiration time), $n = T/\Delta t$ steps. Restrict $P_r$ to the compliant-state sub-matrix $Q_r$ (transitions among $G$ only): $$Continuity_r(n) = \sum_{i\in G}\frac{\pi_r(i)}{Availability_r}\sum_{j\in G}(Q_r^{,n})_{ij}$$

This is the probability of remaining compliant for the whole transaction, given compliant at the start — directly checkable against your logged real command-ack success/failure sequence.

## Transaction Time — empirical + tail extrapolation

Empirical distribution from measured command-ack and iperf/RTT latencies: $F_r(x) = P(TT_r \le x)$, reported as $TT_r^{(p)} = F_r^{-1}(p)$ (95th/99th percentile, bootstrapped CI). For extrapolated worst-case beyond observed range, fit a Generalized Pareto Distribution to exceedances over threshold $u$: $$\bar F(x) \approx (1-F(u))\Big[1+\xi\frac{x-u}{\sigma}\Big]^{-1/\xi}, \quad x>u$$

## Integrity — the honest caveat

True undetected errors aren't directly observable in a short campaign (that's what "undetected" means). Treat it as a _bounded estimate_, not a measured quantity: $$Integrity_r \approx P(s_r(t) < s_{crit}) \times \big(1 - P_{detect}\big)$$ where $P(s_r<s_{crit})$ comes from the same EVT tail model on physical state, and $P_{detect}$ is the MAVLink/transport-level detection rate (sequence-number/CRC check success). State this explicitly as an estimated upper bound derived from physical-layer tail behavior, not a directly measured RCP-grade Integrity figure — reviewers will respect the honesty more than an overclaimed number.

## Fusion across RATs (end-to-end)

$$Availability_{fused} = 1 - C\big(1-Availability_1,, 1-Availability_2\big)$$ where $C$ is a fitted copula capturing dependence between RAT outage events (test independence first; if it holds, this reduces to the simple product rule). Continuity_fused and TT_fused are best obtained via Monte Carlo simulation of the joint process under your chosen redundancy policy, since the closed-form absorbing-state calculation gets unwieldy once dependence is included.

## Data-to-RCP matrix

|Data source|Availability|Continuity|Transaction Time|Integrity|
|---|---|---|---|---|
|SINR / RSSI (physical, per RAT)|Primary — drives Markov states $\to \pi_r$|Primary — defines $G$, feeds $Q_r$|Supporting — explains latency variance|Primary — EVT tail feeds estimate|
|MAVLink packet error/loss|Primary — defines $C_r(t)$|Primary — detected-loss component|—|Supporting — flags detected vs. undetected split|
|MAVLink latency (cmd→ack)|Supporting — contributes to $C_r(t)$|Supporting — transaction-window definition|Primary — direct measurement|—|
|MAVLink throughput|Supporting|—|Supporting|—|
|iperf throughput/loss (controlled load)|Supporting — RAT-comparable baseline|Supporting — cross-checks MAVLink-based continuity|Supporting — clean reference RTT|—|
|ICMP/RTT probes|—|—|Primary — baseline TT, tail input|—|

## Does RCP "ensure" reliability, and where does Integrity fit?

RCP isn't one number that _implies_ reliability — it **is** how reliability is operationally defined for a C2 link in this framework. A link can satisfy Availability, Continuity, and Transaction Time simultaneously and still be unreliable in the safety-relevant sense if it fails Integrity: it stays up, stays stable, and responds fast, but occasionally delivers a corrupted command without anyone knowing. That's precisely why Integrity is framed around _undetected_ failure — the other three parameters describe a link that's up and timely, Integrity is the one guaranteeing that what arrives is actually correct. An RCP type is only credited when all four thresholds are met jointly, not any one in isolation — so your paper's honest framing should be: reliability = joint compliance across Availability, Continuity, Transaction Time, _and_ Integrity, with the last being the hardest to establish from a short campaign and the one you should flag most explicitly as a bounded estimate rather than a directly validated figure.

1. build the algorithm 
2. test with simulation data 


 I pulled the actual npj Wireless Technology "Article" format requirements directly, so this isn't guesswork.

## Official structure (Article type — what you want, not Perspective/Review)

The journal **doesn't impose a strict word count** — it's online-only, fully open access — but the section rules are specific and matter more than length:

|Section|Rule|
|---|---|
|Title|≤15 words, no punctuation/idioms/puns|
|Abstract|≤150 words, **no subheadings**|
|Introduction|**no subheadings**|
|Results|**subheadings required**|
|Discussion|**no subheadings, no separate Limitations or Conclusions section** — integrate both into the discussion prose|
|Methods|subheadings required, comes **after** Discussion, full detail in main text (not Supplementary)|
|References|≤60 (soft limit)|
|Figure legends|≤350 words each|

Note the ordering: **Introduction → Results → Discussion → Methods**, Nature-style — Methods goes last, not first. This matters for how you draft: readers hit your findings before your pipeline details.

For length, this journal's page doesn't state a number, but a sibling npj journal's stated norm is a useful anchor: **~5,000 words of main text as a guide, with Methods excluded from that count**. That's roughly consistent with your original 6–10 page target — treat 5,000 words (excluding Methods, references, figure legends) as your working ceiling, not a hard rule.

## Suggested section-by-section plan

- **Abstract (≤150 words):** the gap (RCP defined top-down, 3GPP KPIs bottom-up, no formal bridge), your contribution (bias-corrected mapping + FSMC/EVT pipeline), and headline validation result (simulation ground-truth + field pilot).
- **Introduction (no subheadings, ~600–800 words):** BVLOS/AAM motivation → PBCS/SORA regulatory context → the specific gap → your contribution stated plainly in the last paragraph. This is where your Annex 10 Vol VI / SORA-SAIL framing earns its keep.
- **Results (subheadings, ~1,800–2,200 words):** structure by claim, not by method — e.g. "Simulation validates estimator accuracy under limited sampling," "RAT-specific bias is measurable and significant," "Fused multi-RAT reliability exceeds single-RAT baselines." Each subsection: what you found, one figure, minimal method explanation (that's what Methods is for).
- **Discussion (no subheadings, ~800–1,000 words):** what the results mean for BVLOS C2 link certification evidence, how this connects to QoSD/SORA-OSO evidence generation, honest limitations (short campaign, Integrity as bounded estimate, deferred RSP/RNP/DAA) woven into the prose — not as a separate section, since the journal disallows one.
- **Methods (subheadings, no length limit, likely your longest section):** testbed hardware, OMNeT++ TN/NTN simulation setup, FSMC fitting, EVT/POT tail estimation, RAT-bias regression, copula fusion, RCP parameter derivation — all the mathematical model from earlier in our conversation belongs here in full.

## Research contributions (for your cover letter / significance framing)

Distilled from what we've built across this conversation, in decreasing order of novelty:

1. **A formal, testable mapping methodology** from heterogeneous physical/logical network metrics (3GPP-style KPIs) to ICAO C2 link RCP parameters, with an explicit, estimable RAT-specific bias-correction term — addressing a gap both GSMA and the RCP/RSP literature acknowledge but don't formally close.
2. **A statistical pipeline suited to short measurement campaigns** — FSMC state modeling plus EVT/POT tail estimation, chosen specifically because they extrapolate rare-event (RCP-relevant) statistics from limited data rather than requiring long observation windows.
3. **A simulation-validated estimator** — using OMNeT++ TN+NTN to establish ground truth and confirm the pipeline recovers accurate reliability estimates from realistically short sampling windows, before applying it to real hardware.
4. **Real multi-RAT hardware validation** (5G, LEO SATCOM, mesh WiFi) — genuinely rare in this literature, directly responsive to the collection's explicit call for hardware/real-world experimentation.
5. **Explicit regulatory positioning** — situating the methodology as an instrumentation approach for QoSD (Annex 10 Vol VI) and as a candidate mechanism for the C2-link evidence SORA's OSO/SAIL process currently lacks a systematic technical pathway for.

That fifth point is your strongest single differentiator for the significance statement — it's the one thing almost nothing else in the literature does, and it directly answers "why should anyone outside wireless engineering care about this paper."



---
[elabftw] review person -  