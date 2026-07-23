
# Paper Structure — Extended Version for IEEE FNWF 2026

**Working title (candidates):**
- *"Adaptive Data-Mesh-Driven MEC Placement for Real-Time Tactical Deconfliction in Multi-Zone U-space"*
- *"From Static to Adaptive: Data-Mesh-Governed Edge Placement for Scalable U-space Deconfliction"*

**Target track:** Track 7 (Future RAN Design — Edge/Fog Computing), secondary fit Track 2 (NTN/UAV) or Track 5 (Autonomics) if the adaptive-policy framing is emphasized in the abstract.

**Positioning relative to the original paper:** the original paper established *that* far-edge vs. metro-edge is a real trade-off (static A/B comparison, single zone, single scenario). This extension answers the natural reviewer question the original leaves open: *"So which one should the system actually use, and does the answer change as conditions change?"* That's the one-sentence pitch for the whole paper — keep it in your back pocket for the abstract and the intro's last paragraph.

---

## Abstract (reframed)

Condense to ~200 words, four moves:
1. Same problem framing as before (U-space, VLL, MEC, data mesh) — 1-2 sentences, can reuse almost verbatim.
2. **What's new**: state plainly that this paper extends the static A/B comparison with (a) a systematic sensitivity analysis across traffic density, USSP fragmentation, and zone topology, and (b) an adaptive, data-mesh-governed placement policy that selects far-edge vs. metro-edge per conflict event.
3. **How**: mention the SimPy-based discrete-event re-implementation (credibility signal — reviewers read this as "not a toy script").
4. **Headline result** (fill in once you have numbers): e.g., "the adaptive policy achieves X% latency reduction over the best static baseline across Y% of the tested operating range."

---

## I. Introduction

Reuse ~70% of the original introduction (UAS growth, VLL/U-space background, MEC motivation, data mesh motivation). Add two new paragraphs before the contributions list:

- **Gap paragraph**: explicitly name the limitation of the original static-comparison approach — a single operating point, single zone, no mechanism for the system itself to choose. This is your gap statement and justifies the whole paper.
- **Why adaptive + data mesh naturally fit together**: the data mesh already publishes per-domain metadata (load, trust, freshness) as discoverable products — so an adaptive policy that consumes these products isn't a bolt-on ML system, it's the natural extension of the governance model you already proposed. This is a good sentence for tying the new contribution back to the original paper's core idea (nice for reviewers who might read both).

**Updated contributions list** (condense to 4, each one sentence + one clause on why it matters):
1. **Sensitivity-driven characterization** of far-edge vs. metro-edge trade-offs across traffic density, USSP fragmentation, and zone topology — replacing the single-point comparison with a design-space view.
2. **Adaptive, data-mesh-governed placement policy** that dynamically selects far-edge or metro-edge resolution per conflict event, using domain-published load/trust/freshness signals rather than a static architectural choice.
3. **Multi-zone deconfliction and handover model** extending the single-zone scenario to heterogeneous, adjacent U-space zones, exercising inter-zone handover under realistic (not single-drone) transit load.
4. **A reproducible, discrete-event simulation methodology** (SimPy-based, seeded/replicated with confidence intervals), replacing the original scripted model — stated explicitly as a methodological contribution, not just an implementation detail.

---

## II. Background

Mostly reuse as-is. Trim the "Technology enablers" and "5G-integrated UTM" subsections by ~20% to make room for new material elsewhere (page budget matters for FNWF). Keep the "Data governance in UTM" subsection close to verbatim — it's the bridge into the adaptive policy section later.

**Optional new short paragraph** at the end of this section: briefly survey adaptive/AI-driven MEC placement literature (1-2 sentences, 2-3 citations) to justify why an adaptive policy is a credible next step and to differentiate from pure RL-based placement papers (yours is explicitly governance-driven, not just performance-driven — that's your novelty angle).

---

## III. System Architecture and Adaptive Data Mesh Policy

This is where the paper diverges most from the original. Restructure the original Section III into two subsections, then add two new ones.

### III-A. Network-Aware MEC for U-space (reused)
Keep Figure 1 and the architecture description close to the original — this is your foundation and doesn't need to change.

### III-B. Federated Data Mesh Governance (reused, lightly extended)
Keep Figure 2 and the four principles as-is. Add one paragraph explicitly framing each data product (geo-awareness, telemetry, load state) as an **input signal** for the adaptive policy in III-C — this is the connective tissue that makes the adaptive policy feel like a natural extension rather than a bolt-on.

### III-C. Adaptive Placement Policy *(new)*
This is your core novel mechanism. Structure it like a proper algorithm description:
- **Decision inputs** (published as data-mesh products): local conflict density, far-edge MEC compute headroom, USSP negotiation backlog, AoI of the geo-awareness feed.
- **Decision rule**: define the threshold/rule-based logic precisely (pseudocode or a small flowchart figure — this is a good candidate for a compact diagram). State clearly it's rule-based (not RL) and why that's a defensible choice for a safety-critical tactical function — explainability and auditability matter for URLLC-grade deconfliction, and this ties back nicely to your "verifiable audit trail" language from the original paper's governance section.
- **Where it executes**: clarify it's evaluated at the MNO orchestrator (already defined in your architecture) subscribing to the shared API bus — no new architectural entity needed, just new logic at an existing one. Reviewers like when new contributions don't require inventing new infrastructure.

### III-D. Multi-Zone Scenario Extension *(new)*
Describe the expanded topology: N adjacent zones (e.g., WHC/CEN/STD, now actually simulated as concurrent entities, not just illustrated), heterogeneous per-zone traffic profiles (steady vs. bursty), and how inter-zone handover (Eq. 4a/4b from the original) is now exercised under realistic multi-drone transit rather than the original single-drone case.

---

## IV. Simulation Methodology *(expanded — give this its own section, not folded into Results)*

Elevating this to a standalone section (rather than a paragraph inside "Results and Analysis" like the original) signals methodological seriousness — worth the page cost.

- **IV-A. Discrete-event model**: describe the SimPy re-implementation — drones, USSPs, MEC nodes, and the orchestrator as SimPy processes; event-driven conflict generation; explicit queuing/contention model for MEC compute (this is the concrete new capability over the original script — name it explicitly: "unlike the original latency-equation-driven model, MEC processing delay `TMEC_proc` now emerges from queuing contention rather than being sampled from a fixed distribution").
- **IV-B. Sensitivity sweep design**: state your DOE approach (parameter ranges, replications per point, seeding, confidence interval reporting). If you use Latin Hypercube Sampling for multi-parameter coverage, name it here.
- **IV-C. Baselines**: define your three comparison arms clearly — Scenario A (static far-edge), Scenario B (static metro-edge), and the new Adaptive policy — so Section V results can reference them by name consistently.
- **(Optional, only if time allows) IV-D. AirFogSim cross-validation**: if you get to the mid-tier upgrade, use it narrowly — e.g., validate your SimPy latency numbers against AirFogSim on a reduced single-zone case, rather than re-running the full sweep in AirFogSim. Frame it explicitly as a validation/calibration step ("to corroborate the SimPy-derived latency figures against a purpose-built UAV-fog simulator") — this gets you the credibility benefit of a second, independent tool without the cost of redoing everything in it.

---

## V. Results and Analysis

Restructure around your three contributions rather than by figure, so each subsection has a clear takeaway:

- **V-A. Sensitivity results**: present the sweep as a small multiple of plots or a heatmap (e.g., latency as a function of drone density × USSP count) rather than the original single-run time series. State the crossover point(s) explicitly in text — this is your headline empirical finding.
- **V-B. Adaptive policy vs. static baselines**: the direct comparison table/plot — this is where you prove the adaptive policy earns its place (Pareto improvement or reduced worst-case tail latency vs. either static choice).
- **V-C. Multi-zone handover results**: extend the original Figure 5 (single-drone migration) to the multi-zone, multi-drone case — report handover latency distribution, not a single trace.
- Keep one KPI comparison table like the original Table I, but add a fourth column for "Adaptive."

---

## VI. Conclusion

Reuse the structure of the original conclusion but update the takeaway: instead of "no single architecture dominates," the extended claim is "the operating point determines the winner, and a lightweight adaptive policy recovers most of the benefit of the better static choice without requiring a priori knowledge of traffic conditions." Keep the future-work paragraph but trim it — you've now executed on the adaptive-placement and multi-zone items that were future work in the original, so future work should point further out (e.g., learned/RL policy, real testbed validation, cross-USSP trust/security hardening).

---

## Page-budget notes

FNWF technical track papers are typically 6 pages (IEEE double-column) including references. Given the original paper is already near that limit, budget roughly:
- Trim Introduction/Background by ~0.5–0.75 page combined (tighten reused text)
- New Section III-C/III-D: ~0.75–1 page
- New Section IV (methodology): ~0.5–0.75 page
- Expanded Results: ~0.5 page net (some original figures can shrink/combine)

If it doesn't fit in 6 pages, the AirFogSim cross-validation (IV-D) is the first thing to cut to a single sentence or move to future work — it's the lowest-priority item relative to the sensitivity sweep and adaptive policy, which are your two headline contributions.

1. Simulator and Results 
2. 
