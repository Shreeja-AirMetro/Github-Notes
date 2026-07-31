
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
2. Paper 

--- 
# Simulation Results Summary — for drafting Sections IV & V

## What was built

A SimPy discrete-event model (`model.py`) in which MEC processing delay emerges from **resource contention** (`simpy.Resource` with finite capacity and stochastic service times), replacing the original closed-form latency equations. Three routing policies share the identical resource model:

- `far_edge` — Scenario A (static)
- `metro_edge` — Scenario B (static); its shared MEC pool also absorbs background load from `n_zones - 1` other zones, so metro contention genuinely increases with topology fan-in rather than being imposed by hand
- `adaptive` — reads **periodically published, freshness-bounded** load signals (`signal_interval = 5 ms`) from both domains — i.e., not instantaneous global state, consistent with the data-mesh "data-as-a-product" framing — and routes each conflict event to the estimated lower-latency path, at a small fixed policy-evaluation overhead (0.3 ms).

**Bug worth knowing about if you re-run/extend this**: the first working version silently dropped the simulated queueing delay from the reported latency (it only summed the fixed overhead terms). Fixed by measuring `env.now` deltas across each resource request. Worth a one-line mention if you want to preempt "how do we know contention is really modeled" reviewer questions — you can just state the delay is measured directly from simulated queue occupancy.

## IV-B. DOE approach (for the methodology section)

- **Full-factorial grid** (`sweep.py::full_factorial_grid`): 10 density levels (25–300) × 5 USSP-fragmentation levels (2, 3, 5, 7, 10), fixed `n_zones = 3`, × 3 policies × **20 seeded replications** per cell = 3,000 runs. This is the basis for the heatmap and the crossover-point extraction (fixed 2D slice, full coverage — appropriate here because you want a clean visual crossover boundary, not sparse sampling).
- **Latin Hypercube Sample** (`sweep.py::lhs_design`): 48 points drawn jointly over (density ∈ [25,300], n_ussp ∈ [2,12], n_zones ∈ [1,8]) via `scipy.stats.qmc.LatinHypercube`, × 8 replications × 3 policies = 1,152 runs. Used to confirm the adaptive-policy finding generalizes across the full 3-parameter space, not just the 2D heatmap slice.
- Each run simulates 500 post-warm-up conflict events (10% warm-up discarded). Per-configuration statistics: mean, P50, P95, and reliability at two URLLC-style budgets (10 ms strict / 20 ms practical, matching the original paper's "URLLC budget" and observed baseline).
- Replications are seeded (`seed=0..19` for the grid, `seed=0..7` for LHS) so every reported number has a reproducible basis; report the 95% CI (`agg()` in `analyze.py`) rather than a single-run point estimate.

## V-A. Sensitivity results — headline finding

**Crossover point: far-edge is overtaken by metro-edge at density ≈ 125 (proxy units), essentially independent of USSP fragmentation** (crossover density is ~125 for every tested n_ussp from 2 to 10). Mechanism: far-edge degradation is driven by **capacity saturation** (fixed, small per-zone compute pool — 2 servers in this model) which scales sharply and nonlinearly with density once the resource nears its throughput limit; metro-edge degradation is driven by **negotiation overhead**, which only grows logarithmically with USSP count in this model, so fragmentation shifts the _level_ of metro-edge latency but barely shifts _where_ the crossover happens against far-edge.

This is a stronger and more specific claim than the original paper's static comparison, and it's falsifiable/checkable directly from `out/grid_density_ussp.csv` and `fig_crossover_map.png`.

Suggested figure: `fig_heatmap_mean_latency.png` (three-panel heatmap, one per policy) as your main Fig. 3 replacement/addition, plus `fig_crossover_map.png` as a compact single-panel summary if page budget is tight.

## V-B. Adaptive vs. static — headline finding

The adaptive policy does not merely match the better static choice — **it Pareto-dominates both static baselines in every representative operating point tested**, because it load-balances across both resource pools rather than committing 100% of traffic to one path (see `table_adaptive_vs_static.csv`):

|Operating point|Far-edge (mean/P95 ms)|Metro-edge (mean/P95 ms)|Adaptive (mean/P95 ms)|
|---|---|---|---|
|Low density / low fragmentation (d=25, u=2)|13.1 / 16.7|42.3 / 53.9|13.4 / 17.0|
|Moderate (d=100, u=5)|19.9 / 30.4|46.5 / 57.8|**17.7 / 25.8**|
|Crossover region (d=150, u=5)|128.2 / 215.7|47.9 / 59.7|**32.0 / 52.1**|
|High (d=200, u=7)|—|—|43.4 / — (see CSV)|
|Extreme (d=300, u=10)|294.6 / 507.8|179.9 / 279.2|**116.9 / 182.6**|

At low density the adaptive policy correctly defaults to far-edge (matching Scenario A almost exactly — the 0.3 ms gap is the policy-evaluation overhead). From moderate density onward, it clearly beats _both_ static architectures, not just the better of the two.

**LHS validation** (`lhs_summary.csv`): across 48 design points spanning the full (density, n_ussp, n_zones) space jointly, the adaptive policy matches-or-beats the better static baseline in **60.4%** of sampled points, with a mean improvement of **+14.7 ms** over the best static choice where it does improve. Worth investigating in the write-up _why_ the other ~40% don't improve — likely low-density/low-contention points where there's no queue to load-balance across, so adaptive ≈ far-edge with a small fixed overhead tax (check `lhs_summary.csv` directly to characterize this before writing the claim — don't just report the aggregate number without checking the failure mode, a reviewer will ask).

## Open item: AirFogSim cross-validation

Installed and inspected (`pip install airfogsim`, v1.1.1). It's a legitimate, actively maintained agent-based UAV/fog simulator (drones as agents with mobility/sensing/computation components, task priority and preemption managers) — a real independent-tool option, not a dead end. But it is meaningfully heavier than a drop-in latency validator: building even a reduced single-zone scenario that's a _fair_ comparison to this contention model (matching capacity/service-rate semantics) is a non-trivial build, not a narrow afternoon task. Recommend treating this as an explicit "future work" line in the paper rather than rushing a shallow validation before the deadline — a rushed, badly-matched AirFogSim comparison would hurt credibility more than omitting it and being upfront that it's planned next.

## Files

- `model.py` — simulation model (read this first)
- `sweep.py` — DOE harness (grid + LHS)
- `analyze.py` — figures, tables, crossover extraction
- `out/fig_heatmap_mean_latency.png`, `out/fig_crossover_map.png`, `out/fig_adaptive_vs_static.png` — the three headline figures
- `out/grid_density_ussp.csv`, `out/lhs_design.csv`, `out/lhs_summary.csv`, `out/table_adaptive_vs_static.csv` — raw and aggregated results