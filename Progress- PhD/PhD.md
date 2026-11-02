Path Nov 2026 - Dec 2027

# PhD Projects & Tasks — T9.1 Reliable & Resilient C2 for UAV BVLOS

Built 2026-11-02 from `PhD_Research_Matrix.xlsx` (Matrix, Publications, Chapters, Sprint_Feb27, Timeline) plus your own task list.
Each RQ is a project; each sub-question (SQ) is a task block with sub-tasks and two kinds of outcome:

- <span style="color:#2E7D32">**Internal**</span> = flight tests, data collection, simulation/emulation runs, models, code (what you have in hand)
- <span style="color:#1565C0">**External**</span> = publications / submissions (what the outside world sees)

Status tags: `[Done]` `[Submitted]` `[In progress]` `[Planned]` `[Not started]` · `(you)` = item from your own list

**Time frame:** contract ends 04/2028 · final thesis draft by 12/2027 · submit before the contract ends.

## Next deadlines

| Date                     | What                                                 | Project      |
| ------------------------ | ---------------------------------------------------- | ------------ |
| **2026-11-12, 20:00 ET** | AIAA AVIATION Forum 2027 — abstract (CNS paper)      | 4 / SQ4.4    |
| 2026-11                  | AESS call deadline + extended-paper policy confirmed | 3 / SQ3.3    |
| **2026-12-31**           | IEEE Access J1 submitted (also counts as PhD report) | 2 / SQ2.1, 6 |
| 2027-02                  | AESS Resilient-C2 J2 submitted                       | 3            |
| 2027-02-08               | AIAA notification                                    | 4            |
| 2027-04                  | Internship exam                                      | 6            |
| ~2027-03/04 (TBA)        | DroNet @ MobiSys 2027 — CFP not out yet              | 2 / SQ2.5    |
| 2027-05-04               | AIAA final manuscript                                | 4            |
| 2027-12                  | Final thesis draft                                   | 5            |

---

# Project 1 — RQ1: Aviation safety → network KPIs (safety-of-link)

> How can aviation safety requirements (ICAO RCP/PBCS) be translated into measurable network KPIs and link-quality indicators for UAV C2 over heterogeneous links?

1. **SQ1.1 RCP → 3GPP KPI mapping per SAIL** `[Done]`
	1. RCP-from-mission-risk methodology (FNWF)
	2. State in thesis scope: integrity excluded
	- <span style="color:#2E7D32">**Internal:** RCP → KPI mapping table (input to Ch 3)</span>
	- <span style="color:#1565C0">**External:** FNWF 2026 — accepted</span>
2. **SQ1.2 Technology diversity TN + NTN vs TN alone** `[Done]`
	1. TN + NTN continuity/availability simulation (99.99 % continuity; gaps at handover)
	- <span style="color:#2E7D32">**Internal:** OMNeT++ TN–NTN runs</span>
	- <span style="color:#1565C0">**External:** FNWF 2026 — accepted</span>
3. **SQ1.3 Physical LQI ↔ logical LQI, and RCP-violation prediction** `[In progress 30 %, due 2027-06]`
	1. Export per-link SINR/delay traces from the simulator (TN, NTN, CHO)
	2. Get Iridium LQI access (open risk)
	3. Collect flight LQI logs — 5G modem AT logs, Iridium, mesh → depends on Project 2 / SQ2.5
	4. Fit physical → logical LQI per link and flight phase; measure prediction lead time
	5. LAWN — RIS for 5G UAV corridors (with T2) (you): your part = C2 / RCP evaluation of RIS-assisted links
		1. Draft review (pending)
		2. Decide venue: conference or journal
	6. Risk quantification from signal quality (with T2, T10) — scope after IEEE Access is submitted
	- <span style="color:#2E7D32">**Internal:** LQI dataset (sim + flight), LQI → RCP-violation predictor</span>
	- <span style="color:#1565C0">**External:** IEEE Access J1 (part), flight-dataset journal J4, LAWN (conf or journal), risk paper C6</span>
4. **SQ1.4 Composite safety-of-link indicator** `[Planned, due 2027-09]`
	1. Define the indicator as the *input* to the operational margin (avoid overlap with SQ3.2)
	2. Compute it online from LQI; check it ranks configurations the same way as RCP pass/fail
	- <span style="color:#2E7D32">**Internal:** indicator definition + evaluation on sim and flight data</span>
	- <span style="color:#1565C0">**External:** section of AESS J2; thesis synthesis (Ch 3 / Ch 9)</span>

---

# Project 2 — RQ2: Reliable C2 mechanisms over 5G + Iridium + Wi-Fi mesh

> Which L2+/application-layer mechanisms (multipath, RLNC, sliding-window coding, LQI-adaptive redundancy) best improve C2 reliability over a heterogeneous multi-link system, and at what cost?

1. **SQ2.1 TN ↔ NTN (conditional) handover, UL/DL asymmetry** `[In progress 60 %, submit by 2026-12-31]` → IEEE Access J1 (you)
	1. Freeze scope + contribution list with J. Zhang — due 2026-11
	2. Simulator comparison table (Simu5G-NTN, 5G-LENA NTN, SNS3, OpenSAND) — due 2026-11
	3. Calibrate against 3GPP TR 38.811 / 38.821 reference results — due 2026-12
	4. ≥ 30 seeds per configuration, confidence intervals on all KPIs — due 2026-12
	5. Public code repo + module-ownership statement — due 2026-12
	6. Submit — by 2026-12-31
	- <span style="color:#2E7D32">**Internal:** completed simulation campaign with CIs; released simulator code</span>
	- <span style="color:#1565C0">**External:** IEEE Access J1 (first author) — also your second PhD report (Project 6)</span>
2. **SQ2.2 Multipath: duplication vs scheduling** `[Planned, due 2027-03]`
	1. Define C2 traffic profile + MAVLink message classes; Iridium plan and cost per hour — due 2026-11
	2. MAVLink protocol — open todos (you)
	3. Multipath — Hansini collab (you), part of your first-author J3: set up the multipath testbed
	4. MAVLink multipath layer (per-link sequence numbers, duplication) on 5G + Iridium + mesh — ground test due 2027-01
	5. Compare vs single link and vs homogeneous dual-5G (PDR, latency, overhead, Iridium airtime)
	- <span style="color:#2E7D32">**Internal:** multipath testbed + layer working in sim and hardware; ground-test PDR/latency per link</span>
	- <span style="color:#1565C0">**External:** methods journal J3 (first author, venue TBD, ~2027-07)</span>
3. **SQ2.3 Block RLNC vs sliding-window RLNC vs duplication** `[Not started, due 2027-03]`
	1. Choose and integrate an RLNC library (check licence) — OMNeT++ app layer + testbed
	2. Compare PDR, in-order delay, redundancy overhead, decoding delay
	- <span style="color:#2E7D32">**Internal:** RLNC / sliding-window implementation, simulation results</span>
	- <span style="color:#1565C0">**External:** methods journal J3</span>
4. **SQ2.4 LQI-adaptive path selection and coding rate** `[Not started, due 2027-06]`
	1. Controller design (depends on the SQ1.3 predictor)
	2. Evaluate RCP compliance vs overhead against static redundancy
	- <span style="color:#2E7D32">**Internal:** adaptive controller in sim + testbed</span>
	- <span style="color:#1565C0">**External:** methods journal J3</span>
5. **SQ2.5 Validation in real flights** `[In progress 20 %, due 2027-09]` — hardware integration (you)
	1. Satcom terminal
		1. Power and data
		2. Satcom terminal test 5G
		3. Test Iridium
	2. Mesh terminal
		1. Vendors contacted (Abraham | Doodle Labs) — setup done on your own
		2. Power setup
		3. Data test — mesh devices
	3. Drone tests
		1. Flight — Pikachu and Nemo
		2. Mr. Shrek weight tuning
		3. Mr. Shrek Satcom
	4. Testbed readiness (Sprint Feb-27)
		1. Time sync (GNSS-PPS / chrony) on companion computer + GCS, offset < 1 ms — due 2026-12
		2. Logging schema + data-management plan (per-link LQI, per-packet seq/timestamps, GNSS, flight phase) — due 2026-12
		3. Test matrix: phases, links on/off, link-kill events, sample sizes — due 2027-01
		4. Flight authorisation (SORA) with the flight team — due 2026-12
	5. Staged flight tests: ground → VLOS → BVLOS-like (Q1–Q3 2027)
	6. DroNet @ MobiSys 2027 (you) — watch for the CFP (not announced yet; past CFPs came out in March, MobiSys is 21–25 June 2027)
	- <span style="color:#2E7D32">**Internal:** integrated drone (Mr. Shrek) with 5G + Satcom + mesh; flight logs; sim-vs-flight comparison</span>
	- <span style="color:#1565C0">**External:** DroNet 2027 workshop paper (testbed / first flights); flight-test & dataset journal J4 (~2027-10)</span>

---

# Project 3 — RQ3: Resilience — behavioural model & operational margin

> Can a dynamic, RCP-anchored operational margin quantitatively assess how a heterogeneous C2 system absorbs, adapts to and recovers from disruption?

1. **SQ3.1 Behavioural resilience model (proactive / reactive / post-corrective, semi-Markov)** `[Submitted]`
	1. Aeroconf paper submission `[Done]`
	2. Aeroconf reviews → camera-ready → talk (Q1 2027)
	- <span style="color:#2E7D32">**Internal:** model with 4 layers × 3 phases</span>
	- <span style="color:#1565C0">**External:** IEEE Aerospace Conf. 2027 (first author)</span>
2. **SQ3.2 Margin separates mechanisms that look equal under static RCP** `[Submitted]`
	1. Fit semi-Markov sojourn times from simulator traces + sensitivity analysis — due 2027-01
	- <span style="color:#2E7D32">**Internal:** fitted distributions, sensitivity plot</span>
	- <span style="color:#1565C0">**External:** Aeroconf 2027 → extended in AESS J2</span>
3. **SQ3.3 Adverse interaction of independently triggered mechanisms; coordinator** `[In progress 50 %, due 2027-02]`
	1. Confirm AESS Resilient-C2 call deadline + policy on extended conference papers — due 2026-11
	2. "New vs Aeroconf" content plan (≥ 3 of: 4-layer evaluation, coordinator, multipath as mechanism, fitted semi-Markov, multi-SAIL) — due 2026-11
	3. Positioning: margin vs performability / survival time; SQ1.4 indicator as margin input — due 2026-12
	4. Coordinator design and evaluation
	5. Submit J2 — due 2027-02
	- <span style="color:#2E7D32">**Internal:** coordinator implemented in OMNeT++</span>
	- <span style="color:#1565C0">**External:** IEEE Trans. AESS J2 (first author)</span>
4. **SQ3.4 Margin validated on flight data with RQ2 mechanisms** `[Planned, due 2027-10]`
	1. Controlled link-kill experiments during flights (enough disruption events) → uses SQ2.5 flights
	2. Compute margin from flight LQI; compare ranking with simulation
	- <span style="color:#2E7D32">**Internal:** flight-derived margin traces</span>
	- <span style="color:#1565C0">**External:** flight-dataset journal J4; Ch 7 validation</span>

---

# Project 4 — RQ4 (extension): From one UAV to the airspace — UTM & CNS

> How do network enablers (MEC, data mesh) and C2 link quality jointly determine the timeliness and resilience of UTM services in multi-UAV VLL airspace?

1. **SQ4.1 MEC placement for tactical deconfliction (cloud / far-edge / metro-edge)** `[Done]`
	- <span style="color:#2E7D32">**Internal:** MEC emulator runs (5 USSPs, 100 UAS, 5 h)</span>
	- <span style="color:#1565C0">**External:** European Wireless 2026 — accepted</span>
2. **SQ4.2 Data-mesh governance between U-space stakeholders** `[Done]`
	- <span style="color:#1565C0">**External:** European Wireless 2026 — accepted</span>
3. **SQ4.3 Link quality → UTM timeliness; link-aware MEC placement and service migration** `[Planned, due 2027-06]`
	1. Deconfliction (you) — with J. Zhang, expanding the ComNets MEC emulator
	2. Mahdi collab (you) — UTM deconfliction and service migration
	3. Couple OMNeT++ link traces with the MEC emulator; measure AoI, drift, deconfliction failures, migration time
	4. Link-aware cooperative SLAM (with T9.2) — outlook only unless your C2 part is substantial
	- <span style="color:#2E7D32">**Internal:** coupled sim + emulator scenario incl. service migration</span>
	- <span style="color:#1565C0">**External:** UTM link-aware MEC conference paper C5</span>
4. **SQ4.4 C2 in the integrated CNS chain (strategic / pre-tactical / tactical)** `[In progress 20 %, due 2027-10]`
	1. CNS paper → AIAA AVIATION Forum 2027 (you)
		1. Pick the technical discipline track and read its call (e.g. Air Transportation Systems: extended abstract ≥ 3 pages)
		2. Extended abstract — **due 2026-11-12, 20:00 ET**
		3. Notification 2027-02-08 → final manuscript due 2027-05-04 → forum 7–11 June 2027, San Diego
	2. Write a 1-page "C2 interface spec" for the digital twin (coverage/RCP risk maps, in-flight margin)
	- <span style="color:#2E7D32">**Internal:** C2 layer of the CNS demonstrator</span>
	- <span style="color:#1565C0">**External:** AIAA AVIATION 2027 paper (CNS demonstrator, C4)</span>

---

# Project 5 — Monograph writing

Final draft by 12/2027; submit before the contract ends (04/2028).

1. Research statements → research questions (you) — fix RS1–RS4 / RQ1–RQ4 wording for Ch 1
2. Math background (you) — formal basis for Ch 3 / Ch 7 (RCP mapping, semi-Markov model, margin)
3. Literature (you) — Ch 2; expand the SoA tables from the TAC deck (slides 24–25)
4. Chapters
	1. Ch 2 Background & State of the Art `[In progress]` — draft 2027-02
	2. Ch 4 Evaluation methodology: simulator, emulator, testbed — draft 2027-03 (lift from IEEE Access)
	3. Ch 3 Aviation safety → network KPIs (RQ1) — draft 2027-04
	4. Ch 5 Heterogeneous multi-link characterisation (SQ1.3, SQ2.1) — draft 2027-06
	5. Ch 6 Reliable C2 mechanisms (RQ2) — draft 2027-08
	6. Ch 7 Reliability → resilience (RQ3) — draft 2027-09
	7. Ch 8 Scaling to airspace: UTM & CNS (RQ4) — draft 2027-10 (could shrink to a section of Ch 7)
	8. Ch 1 Introduction, Ch 9 V&V and mapping to ICAO/3GPP — draft 2027-11
	9. Ch 10 Conclusion & outlook — draft 2027-12
	10. **Full final draft — 2027-12**
	11. Supervisor revisions → submission (Q1 2028, before 04/2028)
- <span style="color:#2E7D32">**Internal:** chapter drafts reviewed by supervisors</span>
- <span style="color:#1565C0">**External:** thesis submission</span>

---

# Project 6 — PhD requirements (2 exams + 2 reports pending)

1. Exams
	1. ComNets 3 exam (you)
	2. Internship exam — 2027-04 (you)
2. Reports
	1. Internship report (you)
	2. IEEE Access paper — by 2026-12-31 (same work as Project 2 / SQ2.1)
- <span style="color:#2E7D32">**Internal:** credits completed (10 + 30 CP per TAC 2026)</span>
- <span style="color:#1565C0">**External:** admission to thesis submission</span>

---

# Side tasks (minor)

1. Ming — DT side project for a patent (minor)