
Collaboration with T2 
https://vtsociety.org/post/announcement/call-papers-special-issue-low-altitude-wireless-networks-lawn#:~:text=Low%2DAltitude%20Wireless%20Networks%20(LAWN)%20represent%20a%20paradigm%20shift,across%20aerial%20and%20terrestrial%20nodes.

6/11
- Regular Paper 
- 100-3000m Low-altitude airspace 
- Low-Altitude Wireless Networks (LAWN) represent a paradigm shift from conventional aerial communications by introducing a multifunctional, service-aware, and dynamically reconfigurable 3D network fabric that integrates communication, sensing, control, and distributed computing across aerial and terrestrial nodes. LAWN enables intelligent, mission-driven aerial operations and supports future autonomous systems by combining cross-layer design principles with advanced technologies.
Potential Topic 
- Scalable Air Traffic Management for LAWN
- URLLC for Safety-Critical Applications in LAWN
- Air-to-Ground and Air-to-Air Channel Modeling and Measurement for LAWN


Roshan's direction 

RIS material simulator start with near-field 
Implementation Near-field simulator for FEM - EM scattering 
that can be moved to far-field parameters - by far-field transformers 

Far-field - Antenna gain , reflector 
Ray tracing get RSSI and RSRP 

3D environemnt 

Check 
Ray tracing simulator 
Circuit modeling - cannot  work for physics based flying 

MMwave and RSSI and how it used 
MMwave for drone 
Database of current antennas - geospatial map

HW 
SoA - RSSI and RSRP of ray tracing from Mm wave
mmwave for drone operatoin 

Ray tracing

- Latex - write about our goal and discussed
- Sienna at different heights coverage map 
mm wave and the 
- ideal RIS parameters
- multi-physics based 
https://nvlabs.github.io/sionna/rt/index.html 
https://ieee-aess.org/technical-committee/low-altitude-wireless-networks-technical-working-group

https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9424177

Germany government link 
https://gigabitgrundbuch.bund.de/GIGA/DE/Roadmap/start.html
https://gigabitgrundbuch.bund.de/GIGA/DE/_Home/start.html
https://gigabitgrundbuch.bund.de/GIGA/DE/Funklochkarte/start.html
https://gigabitgrundbuch.bund.de/GIGA/DE/Downloads_Suche/Formular.html#searchResult
https://www.geoportal.de/info/tk_03-netzabdeckung_mobilfunk

Openmap
https://opencellid.org/#zoom=14&lat=51.03984&lon=13.73236
https://www.reddit.com/r/cellmapper/comments/hnvqqh/noob_reading_cellmapper_map/

https://www.cellmapper.net/map?MCC=262&MNC=1&type=LTE&latitude=51.05278891249753&longitude=13.23739078683101&zoom=13.861113944109777&showTowers=true&showIcons=true&showTowerLabels=true&clusterEnabled=true&tilesEnabled=true&showOrphans=false&showNoFrequencyOnly=false&showFrequencyOnly=false&showBandwidthOnly=false&DateFilterType=Last&showHex=false&showVerifiedOnly=false&showUnverifiedOnly=false&showLTECAOnly=false&showENDCOnly=false&showBand=0&showSectorColours=true&mapType=roadmap&darkMode=false&imperialUnits=false

https://www.radartutorial.eu/06.antennas/Antenna%20Characteristics.en.html

# 1) How TVT special issues typically review & timing

- TVT’s editorial goal is to complete the **first review cycle within ~3 months**; community-reported stats show **first review ≈ 2.9 months** and **total handling for accepted manuscripts ≈ 7.8 months**, with an **average ~2.7 rounds** of review. That matches expectations for a high-rank IEEE Transactions. [vtsociety.org+1](https://vtsociety.org/publication/ieee-transactions-vehicular-technology/information-editors/first-review-cycle?utm_source=chatgpt.com)
    
- **Acceptance rates** for TVT (and most IEEE Transactions) are not published publicly for every issue. Expect a _low_ acceptance probability for a special issue in a hot topic because high-quality groups target these calls. Community anecdotes indicate high selectivity. [SciRev](https://scirev.org/journal/ieee-transactions-on-vehicular-technology/?utm_source=chatgpt.com)
    

# 2) Is “RIS + RSSI/RSRP conversion for low-altitude drone operation” novel enough?

Short verdict: **Possibly — but only if you add something substantively new.** Here’s why:

What’s already out there

- RIS + UAV (RIS-assisted UAV or RIS-UAV) is a well-established and rapidly growing subfield: surveys, arXiv papers, MDPI and conference/IEEE papers discuss RIS placement, energy/trajectory co-design, channel modeling, and performance gains for UAVs. So _basic_ RIS-UAV proposals are not novel by default. [arXiv+1](https://arxiv.org/abs/2504.02162?utm_source=chatgpt.com)
    
- RSSI ↔ RSRP conversions and their formulas are standard in cellular engineering (RSRP = reference-signal based metric; RSSI measures total received power including noise/interference). Tools and calculators for converting exist because these metrics are widely used in LTE/5G measurements. [Digi International+1](https://www.digi.com/support/knowledge-base/understanding-lte-signal-strength-values?utm_source=chatgpt.com)
    

When your idea _would_ be novel for this TVT LAWN special issue

- You develop a **new measurement model or conversion algorithm tailored to low-altitude aerial channels with RIS in the propagation path** (e.g., account for altitude-dependent multipath, drone body blockage, high Doppler, controllable RIS phase patterns, and dynamic geometry).
    
- **You validate on real hardware or a realistic testbed** (in-flight measurements with RIS assisted links, or a carefully instrumented field experiment). The LAWN call explicitly welcomes real-world prototypes/testbeds — that strongly improves novelty/acceptance chances. [vtsociety.org](https://vtsociety.org/publication/transactions-vehicular-technology/call-papers?utm_source=chatgpt.com)
    
- You demonstrate **practical benefit** (e.g., better link adaptation, more accurate ranging/positioning, improved handover decisions, or improved spectral efficiency) and compare to baseline industry/academic methods (standard RSSI→RSRP heuristics).
    
- You provide **cross-layer insights** (how the conversion affects MAC/handovers, or how RIS control + conversion improves network-level KPIs), since TVT likes system-level/vehicular implications.
    

# 3) Concrete checklist to make the submission competitive for the TVT special issue

1. **Clear novelty statement**: exactly what is new (theory, algorithm, model, dataset, testbed).
    
2. **Channel/modeling contribution**: derive an analytical or data-driven conversion model that captures low-altitude specifics and RIS effects (not just apply LTE formulas blindly). Cite and contrast with standard RSSI/RSRP relations. [Digi International+1](https://www.digi.com/support/knowledge-base/understanding-lte-signal-strength-values?utm_source=chatgpt.com)
    
3. **Validation**: at least high-fidelity simulations with 3D mobility + RIS modeling _and_ (strongly preferred) measured data from a hardware test or proof-of-concept. The special-issue call highlights prototypes/testbeds. [vtsociety.org](https://vtsociety.org/publication/transactions-vehicular-technology/call-papers?utm_source=chatgpt.com)
    
4. **System impact**: show how the conversion matters — e.g., improves handover accuracy, power control, situational awareness in LAWN scenarios.
    
5. **Compare baselines**: standard RSSI→RSRP conversions, RIS-free scenarios, existing RIS-UAV works. [arXiv+1](https://arxiv.org/abs/2012.04775?utm_source=chatgpt.com)
    
6. **Paper preparation**: follow TVT formatting; consider a longer regular paper if you have thorough experiments (TVT allows up to 14 pages for full papers). [vtsociety.org](https://vtsociety.org/publication/transactions-vehicular-technology/call-papers?utm_source=chatgpt.com)
    

# 4) Recommended framing for reviewers (short paragraph you can adapt)

“We propose a _low-altitude channel-aware RSSI→RSRP conversion and calibration method_ that explicitly models RIS-altered propagation and UAV dynamics. We validate via (i) a 3D ray-tracing + mobility simulation study, and (ii) in-flight measurements with a prototype RIS-assisted link. Results show X dB improvement in RSRP estimation accuracy and Y% improvement in handover/throughput compared to standard LTE conversions — demonstrating practical benefit for LAWN deployments.”  
If you can truthfully write something like that, you’ll be in a competitive position.

# 5) Final recommendations / next steps

- If you want, I can:
    
    1. Draft a **short outline** and novelty paragraph (tailored to the TVT LAWN call) you can paste into your submission.
        
    2. Help design an **experiment plan** (simulator + measurement checklist) focusing on RIS effects on RSSI/RSRP at low altitudes.
        
    3. Search for **recent RIS-UAV experimental papers** to cite and to show the gaps your work fills. (I already found surveys and experimental-ish papers; I can fetch more targeted examples.) [arXiv+1](https://arxiv.org/abs/2504.02162?utm_source=chatgpt.com)
        

Would you like me to draft a submission abstract and the “what’s new” paragraph now, or to build a suggested experiment plan (simulator parameters, UAV altitudes, metrics to collect)?

---
Let’s focus on **how to make your paper novel enough for a Q1 journal like IEEE TVT**, especially since your topic — **RIS-assisted communication for low-altitude drones (LAWN)** and **RSSI↔RSRP conversion** — already has active competition.

---

## 🧭 Step-by-Step Strategy to Make Your Paper Novel

### **1️⃣ Define the exact novelty gap**

You need to **pinpoint what hasn’t been done**, not just what’s been _rarely done_.  
To do this:

- **Map existing work**:
    
    - Collect 15–20 most recent (2023–2025) IEEE/Elsevier papers on _RIS + UAV_, _LAWN_, _channel modeling_, and _signal strength estimation_.
        
    - Classify them into themes (e.g., trajectory optimization, beamforming, positioning, channel estimation, measurement).
        
- **Identify a missing link**, for example:
    
    - “Most studies assume perfect RSRP estimation for UAVs, but none model the error due to altitude-dependent RSSI distortion under RIS reflection.”
        
    - “Existing RIS-UAV works optimize beamforming, but not for the accuracy of signal-quality indicators used for link adaptation.”
        

This gives you a **precise ‘research gap’** statement reviewers value.

---

### **2️⃣ Add one strong differentiator**

In top-tier journals, novelty usually comes from **one of four angles** — pick at least one and make it _quantitative_.

|Novelty Type|What to Do|Example for Your Case|
|---|---|---|
|**New Model**|Derive a new analytical or statistical model capturing an overlooked factor.|Model the RSSI→RSRP conversion error as a function of altitude, drone attitude, and RIS phase control.|
|**New Algorithm**|Propose a control, optimization, or estimation algorithm.|Develop a learning-based converter that self-calibrates using limited flight data to improve RSRP accuracy.|
|**New Experimental Insight**|Provide first measurement/testbed data for a scenario.|Build a small UAV–RIS testbed and record real RSSI/RSRP pairs to validate your model.|
|**New System Perspective**|Combine two layers or domains not yet linked.|Show how inaccurate RSRP estimation impacts MAC-layer handover or path planning in LAWN.|

---

### **3️⃣ Quantify novelty**

Make your paper’s contribution _measurable_.  
Use phrases like:

> “Unlike previous RIS-UAV studies that assume ideal signal metrics, our method reduces the RSRP estimation error by **38%** compared to the 3GPP baseline.”

Concrete performance numbers help reviewers instantly see the innovation.

---

### **4️⃣ Integrate a realistic validation**

In IEEE TVT, reviewers love when **models are grounded in real data**:

- Use **flight-test data**, **drone-mounted SDRs**, or **ray-tracing simulation** with 3D urban topologies.
    
- Include **realistic impairments** (e.g., Doppler, body shadowing, RIS misalignment).
    
- Compare your new model/algorithm with **standard conversions** used in LTE/5G documentation.
    

Even small-scale experiments can drastically improve the perception of novelty.

---

### **5️⃣ Strengthen the framing**

Even if your method is modestly new, _how you position it_ makes a difference.  
Structure your Introduction so that:

1. **Gap:** “Current RIS-UAV works ignore inaccurate link-quality metrics at low altitude.”
    
2. **Problem:** “This causes suboptimal power control and handover in LAWN.”
    
3. **Contribution:** “We propose a low-altitude-aware RIS-aided RSRP estimation framework validated via simulation and prototype tests.”
    

This narrative convinces reviewers of relevance and originality.

---

### **6️⃣ Optional “novelty boosters”**

If you can, add one of these:

- **Dataset release:** Share your RSSI↔RSRP measurements — makes your paper more citable.
- **Explainable model:** Combine physics-based modeling + AI (hybrid approach).
- **Cross-disciplinary insight:** e.g., use reinforcement learning or 6G sensing integration for LAWN signal calibration.
---

## 🔬 Example Framing of a Novel Contribution

> _“We propose the first integrated modeling and calibration framework for signal-strength metrics in low-altitude UAV networks assisted by reconfigurable intelligent surfaces (RIS). The framework analytically models the altitude- and angle-dependent bias between RSSI and RSRP in reflected channels, and introduces a lightweight adaptive conversion algorithm. Simulation and experimental validation show up to 35% reduction in RSRP estimation error and 18% improvement in link throughput compared to existing models, highlighting the framework’s potential for 6G LAWN optimization.”_

That’s the type of “novelty paragraph” reviewers expect.

---

Would you like me to help you **draft a specific novelty paragraph** (tailored to your planned method and data) — or would you prefer I first help you **identify what kind of novelty is most realistic for your team**

---
Great — below are **concrete, actionable idea directions** you can use to make a novel TVT submission comparing **RIS-on-facades** vs **RIS-on-drones**. For each idea I give: the _novel gap_, _why it matters_, a short _simulation / experiment plan_ (parameters & baselines), and the _expected signal_ (what result would convince reviewers). I finish with a ready-to-copy **novelty paragraph** and a suggested **evaluation checklist**. I cite recent surveys and experimental work that show the gaps. ([arXiv](https://arxiv.org/html/2506.19526v1?utm_source=chatgpt.com "Reconfigurable Intelligent Surfaces for 6G and Beyond - arXiv"))

---

## 1) Altitude- and angle-aware RSSI → RSRP conversion under RIS reflection

**Gap:** Most RSSI↔RSRP conversion rules are terrestrial (LTE/5G) and ignore altitude/angle, RIS reflection geometry, and UAV body blockage. ([MDPI](https://www.mdpi.com/1424-8220/24/20/6615?utm_source=chatgpt.com "Experimental Study on LTE Mobile Network Performance ... - MDPI"))  
**Why it matters:** Wrong conversion leads to bad link adaptation, handover and resource allocation in LAWN.  
**Sim plan:** Build a 3D channel model with direct link + RIS-reflected path; vary altitude (10–200 m), elevation angles, RIS type (facade planar vs drone-mounted array), RIS phase patterns. Produce synthetic RSSI and RSRP (per 3GPP definitions) and fit a parametric conversion model (e.g., altitude, elevation, RIS-gain terms). Baselines: standard LTE conversion formula, simple linear regression.  
**Metrics / success:** Reduction in RSRP estimation error (RMSE) vs baseline; show how improved conversion improves throughput or handover accuracy. Expected convincing numbers: ≥25–35% RMSE reduction and measurable throughput/handover gains. ([MDPI](https://www.mdpi.com/1424-8220/24/20/6615?utm_source=chatgpt.com "Experimental Study on LTE Mobile Network Performance ... - MDPI"))

---

## 2) Mobility & Doppler impact on RIS control and signal indicators

**Gap:** Existing RIS-UAV works often ignore high Doppler and fast geometry changes caused by moving UAVs and moving RIS (if on drone). ([arXiv](https://arxiv.org/html/2506.19526v1?utm_source=chatgpt.com "Reconfigurable Intelligent Surfaces for 6G and Beyond - arXiv"))  
**Why it matters:** Controller latency and imperfect phase updates change the reflected channel and distort RSSI/RSRP.  
**Sim plan:** Simulate UAV trajectories (speeds 0–20 m/s) and RIS-on-drone with control update intervals (10–500 ms). Model Doppler on direct and reflected paths, include phase update errors. Baseline: ideal instantaneous RIS control.  
**Metrics / success:** Show the tradeoff between control latency and RSRP estimation / throughput; demonstrate a robust control policy (e.g., predictive phase updates or Kalman-filtered conversion) that recovers performance when update latency exists. ([arXiv](https://arxiv.org/pdf/2401.17180?utm_source=chatgpt.com "[PDF] Channel Characterization of UAV-RIS-aided Systems with Adaptive ..."))

---

## 3) SWaP and power-constrained RIS on UAV vs wired facades: system-level cost-benefit

**Gap:** Little quantified comparison of SWaP (size/weight/power) constraints vs communication gain between tethered/facade RIS and airborne RIS. ([Iowa State University Digital Repository](https://dr.lib.iastate.edu/bitstreams/5ff059de-880e-4dc1-a646-b6b07b0eba0f/download?utm_source=chatgpt.com "[PDF] Mounting RIS on Tethered and Untethered UAVs"))  
**Why it matters:** Drone RIS will be smaller/less powerful — need to show when airborne RIS is worth the cost.  
**Sim plan:** Model RIS element count and power budgets for drone RIS and for large facade RIS. Run coverage & throughput simulations across urban canyon scenarios, include deployment cost (mobility advantage), handover improvements, and maintenance complexity. Baselines: facade RIS only, drone RIS only, hybrid.  
**Metrics / success:** Provide Pareto curves (coverage gain vs SWaP cost) showing operating regimes where drone RIS is superior (e.g., temporary event coverage, disaster zones).

---

## 4) Multi-RIS coordination: distributed RIS scheduling & interference management

**Gap:** Coordination algorithms for multiple moving RIS (drones) + fixed facade RIS in the same airspace are underexplored. ([arXiv](https://arxiv.org/html/2506.19526v1?utm_source=chatgpt.com "Reconfigurable Intelligent Surfaces for 6G and Beyond - arXiv"))  
**Why it matters:** Without coordination, RIS reflections can interfere and mislead RSSI/RSRP measurements.  
**Sim plan:** Multi-RIS network with Nfacade + Mdrone; optimize phase schedules under constrained backhaul/command channels. Evaluate with and without a conversion-aware metric.  
**Metrics / success:** Network-level KPIs (sum-rate, fairness, latency). Novelty: distributed scheduling algorithm that uses corrected RSRP estimates to reduce harmful interference. Show improvements vs naïve coordination.

---

## 5) Hybrid physics-plus-ML conversion calibrated by small flight dataset (transfer learning)

**Gap:** Pure physics models miss hardware imperfections; pure ML needs lots of data. Hybrid models are promising but few apply to RIS+UAV. ([arXiv](https://arxiv.org/html/2506.19526v1?utm_source=chatgpt.com "Reconfigurable Intelligent Surfaces for 6G and Beyond - arXiv"))  
**Why it matters:** A hybrid model can generalize across altitudes and RIS types with small calibration dataset.  
**Sim plan:** Train a physics-informed ML model on simulated data; fine-tune with 1–3 short flights (RSRP/RSSI pairs) for a new environment. Baselines: physics-only, ML-only.  
**Metrics / success:** Show fast adaptation (few-shot) and lower RSRP RMSE than baselines.

---

## 6) First-of-its-kind in-flight measurements for facade vs drone RIS (small testbed)

**Gap:** Few public in-flight datasets that contain RSSI/RSRP with RIS presence; datasets for LAWN with RIS are scarce. ([arXiv](https://arxiv.org/html/2510.08752v1?utm_source=chatgpt.com "Wireless Datasets for Aerial Networks - arXiv"))  
**Why it matters:** Real data strongly convinces reviewers and is explicitly welcomed by TVT.  
**Experiment plan:** Mount a small RIS prototype or controllable reflector on a rooftop/facade and on a drone (or mount a retroreflector pattern on a payload). Fly predefined trajectories at altitudes 20–120 m, collect timestamps, GPS, RSSI, RSRP, SNR, AoA estimates, RIS phase settings. Release dataset.  
**Metrics / success:** Publish dataset + show model calibration & algorithm validation. Even a small dataset from 5–10 flights is valuable.

---

## 7) Impact on MAC/handover decisions: closed-loop evaluation

**Gap:** Many works stop at PHY metrics; TVT values system and vehicular-level impacts. ([ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0140366423001743?utm_source=chatgpt.com "A survey on UAV-assisted wireless communications"))  
**Why it matters:** Demonstrate that better conversion leads to better handover triggers, link selection, and mission success for drones.  
**Sim plan:** Integrate your conversion into an LTE/5G MAC/handover policy in a network simulator (ns-3 or custom). Compare mission-level KPIs: packet loss during handover, control-loop latency, mission completion.  
**Metrics / success:** Show reductions in handover failures or control-plane downtime that matter for UAV missions.

---

## 8) RIS-induced positioning bias and correction for UAV navigation

**Gap:** RIS reflections can bias RSSI/AoA-based positioning; few works quantify or correct this for UAV navigation. ([MDPI](https://www.mdpi.com/1424-8220/24/9/2789?utm_source=chatgpt.com "Experimental Evaluation of an SDR-Based UAV Localization System"))  
**Why it matters:** For LAWN, navigation and comms intersect — errors affect safety.  
**Sim plan:** Simulate positioning algorithms under facade vs drone RIS, quantify bias, propose a correction that leverages RIS state information.  
**Metrics / success:** Position RMSE improvements and demonstration of safe navigation margins.

---

## 9) Security/privacy & spoofing risks introduced by drone-mounted RIS

**Gap:** Drone RIS can be used maliciously to spoof RSSI/RSRP or create false coverage; few mitigation strategies exist. ([MDPI](https://www.mdpi.com/2504-446X/9/6/431?utm_source=chatgpt.com "Cooperative Jamming for RIS-Assisted UAV-WSN Against Aerial ..."))  
**Why it matters:** Safety and trust in LAWN deployments.  
**Sim plan:** Attack-defense study: simulate a malicious drone RIS altering perceived RSRP; propose detection (consistency checks across multiple sensors) or resilient converters.  
**Metrics / success:** Detection rate / false alarm tradeoffs.

---

## 10) Practical deployment optimization: when to use facade RIS, drone RIS, or hybrid

**Gap:** No concrete decision framework comparing deployment tradeoffs under real urban constraints. ([Iowa State University Digital Repository](https://dr.lib.iastate.edu/bitstreams/5ff059de-880e-4dc1-a646-b6b07b0eba0f/download?utm_source=chatgpt.com "[PDF] Mounting RIS on Tethered and Untethered UAVs"))  
**Why it matters:** Operators need guidance: temporary events, emergency response, persistent deployments.  
**Sim plan:** Build cost + performance model and run scenario analysis (stadium event, urban canyon, disaster). Produce policy maps telling when hybrid makes sense.  
**Metrics / success:** Decision boundaries (e.g., when drone RIS outperforms facade RIS given user density, requiring X dB improvement at Y locations).

---

## Short experimental parameter suggestions (use these in sims / testbed)

- Frequencies: sub-6 GHz (2.6 GHz) and a mmWave band (28–39 GHz) if possible.
    
- Altitudes: 10 m, 30 m, 60 m, 120 m.
    
- UAV speeds: 0, 5, 10, 20 m/s.
    
- RIS element sizes: small (8×8), medium (32×32), large (64×64) — scaled gains.
    
- Control latency: 10 ms, 50 ms, 100 ms, 500 ms.
    
- Metrics to collect: RSSI, RSRP, RSRQ/SINR, throughput, packet loss, handover delay/failure, position RMSE.
    
- Baselines: no-RIS, facade-only RIS, drone-only RIS, ideal-RIS (perfect CSI & zero latency).
    

---

## Ready-to-use novelty paragraph (paste into intro/submission cover letter)

> “This paper is the first to systematically compare façade-mounted and drone-mounted reconfigurable intelligent surfaces (RIS) for low-altitude wireless networks, focusing specifically on the _bias between RSSI and RSRP under RIS-influenced propagation_. We introduce an altitude- and motion-aware RSSI→RSRP conversion model that accounts for RIS geometry, UAV attitude and controller latency, and a hybrid physics-ML calibration method that adapts from limited in-flight measurements. Through 3D ray-tracing simulations and a small in-flight testbed, we show our method reduces RSRP estimation RMSE by **X%** and reduces handover failures by **Y%** compared to standard conversions — demonstrating practical benefits for LAWN deployments.”  
> (Replace X/Y with your measured numbers.)

---

## What reviewers will look for — evaluation checklist

1. Clear gap and “what’s new” statement.
    
2. Solid channel model (explain assumptions; cite RIS/UAV surveys). ([arXiv](https://arxiv.org/html/2506.19526v1?utm_source=chatgpt.com "Reconfigurable Intelligent Surfaces for 6G and Beyond - arXiv"))
    
3. Realistic impairments (Doppler, controller latency, body blockage). ([arXiv](https://arxiv.org/pdf/2401.17180?utm_source=chatgpt.com "[PDF] Channel Characterization of UAV-RIS-aided Systems with Adaptive ..."))
    
4. Baselines and ablation studies (physics-only, ML-only, no-RIS).
    
5. Reproducible simulation parameters and, if possible, a small real dataset or testbed results. ([arXiv](https://arxiv.org/html/2510.08752v1?utm_source=chatgpt.com "Wireless Datasets for Aerial Networks - arXiv"))
    
6. System-level implications (MAC/handover/mission metrics).
    

---


LAWN paper - Structure - Flow - Clarity and Speed

To dos:
- [ ] What is the research gap , SoA, novelty 
- [x] Structure of the paper with My contribution and Roshan's contribution 
- [ ] My hws: SoA - RSSI and RSRP of ray tracing from Mm wave
mmwave for drone operation 
- [ ] ray tracing for regular ghz frequency possible? 
- [x] Points to discuss for next meeting 



---

The paper targets UAV based application in UAM 
UAM with 5G posses significant challenges , Plan UAM network , Multi-technology / multi-link 
**URLLC - Meta modeling - Air-to-ground and ground to air channel modelling  (find the connection)**


RIS 

To read
- [ ] Air-to-ground and ground to air channel modelling 
- [ ] URLLC for LAWN
- [ ] RSSI and RSRP of ray tracing from Mm wave - mmwave for drone operation
 - [ ] ray tracing for regular ghz frequency possible
 - [ ] Novelty of the paper (my side and roshan side)
 - [ ] To do for simulation part
---
Air-to-ground and ground to air channel modelling 

Air-to-ground (A2G) and ground-to-air (G2A) channel modeling involves ==creating mathematical representations of radio wave propagation from an aircraft to the ground and vice versa to predict signal quality and optimize communication systems==. These models must account for factors like multipath fading, the altitude of the aircraft, the propagation environment (e.g., urban, rural), and the receiver's location. They are used to test and optimize communication, navigation, and surveillance (CNS) systems, often through computer simulations to avoid the high cost and complexity of real-world flight trials.

Types of channel models

- **[Path loss models](https://www.google.com/search?q=Path+loss+models&rlz=1C1GCEU_deDE1112DE1112&oq=Air-to-ground+and+ground+to+air+channel+modelling&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRifBdIBCTEwNDcwajBqN6gCALACAA&sourceid=chrome&ie=UTF-8&mstk=AUtExfCG2_3KrXeDJdGSD1osiptihd7Rr_nHCWUwTYU5zyg28j8-2pYTtUkrg4dAfAEk73jhTCCV7UJ4l_PpoKdAoEk1Y48brOFmxE8jUecqX8Kbx1gUimn_lnE0_NapDJTU_wOOKDD0lSP6DwzIanzhppJ4S_AC1cHvhLAVDLXReV3128g&csui=3&ved=2ahUKEwjAt7fXo5yRAxUwRPEDHXF7DIoQgK4QegQIBRAB)**: These models predict the reduction in signal power over distance, without considering other effects like fading. The [Friis free space propagation model](https://www.google.com/search?q=Friis+free+space+propagation+model&rlz=1C1GCEU_deDE1112DE1112&oq=Air-to-ground+and+ground+to+air+channel+modelling&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRifBdIBCTEwNDcwajBqN6gCALACAA&sourceid=chrome&ie=UTF-8&mstk=AUtExfCG2_3KrXeDJdGSD1osiptihd7Rr_nHCWUwTYU5zyg28j8-2pYTtUkrg4dAfAEk73jhTCCV7UJ4l_PpoKdAoEk1Y48brOFmxE8jUecqX8Kbx1gUimn_lnE0_NapDJTU_wOOKDD0lSP6DwzIanzhppJ4S_AC1cHvhLAVDLXReV3128g&csui=3&ved=2ahUKEwjAt7fXo5yRAxUwRPEDHXF7DIoQgK4QegQIBRAC) is a basic example used for unobstructed paths.
- **[Stochastic models](https://www.google.com/search?q=Stochastic+models&rlz=1C1GCEU_deDE1112DE1112&oq=Air-to-ground+and+ground+to+air+channel+modelling&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRifBdIBCTEwNDcwajBqN6gCALACAA&sourceid=chrome&ie=UTF-8&mstk=AUtExfCG2_3KrXeDJdGSD1osiptihd7Rr_nHCWUwTYU5zyg28j8-2pYTtUkrg4dAfAEk73jhTCCV7UJ4l_PpoKdAoEk1Y48brOFmxE8jUecqX8Kbx1gUimn_lnE0_NapDJTU_wOOKDD0lSP6DwzIanzhppJ4S_AC1cHvhLAVDLXReV3128g&csui=3&ved=2ahUKEwjAt7fXo5yRAxUwRPEDHXF7DIoQgK4QegQIBRAE)**: These are purely statistical models that capture the random nature of noise and multipath fading but may lack geometric details.
- **[Spatial models](https://www.google.com/search?q=Spatial+models&rlz=1C1GCEU_deDE1112DE1112&oq=Air-to-ground+and+ground+to+air+channel+modelling&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRifBdIBCTEwNDcwajBqN6gCALACAA&sourceid=chrome&ie=UTF-8&mstk=AUtExfCG2_3KrXeDJdGSD1osiptihd7Rr_nHCWUwTYU5zyg28j8-2pYTtUkrg4dAfAEk73jhTCCV7UJ4l_PpoKdAoEk1Y48brOFmxE8jUecqX8Kbx1gUimn_lnE0_NapDJTU_wOOKDD0lSP6DwzIanzhppJ4S_AC1cHvhLAVDLXReV3128g&csui=3&ved=2ahUKEwjAt7fXo5yRAxUwRPEDHXF7DIoQgK4QegQIBRAG)**: Developed for systems using multiple antennas ([MIMO](https://www.google.com/search?q=MIMO&rlz=1C1GCEU_deDE1112DE1112&oq=Air-to-ground+and+ground+to+air+channel+modelling&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRifBdIBCTEwNDcwajBqN6gCALACAA&sourceid=chrome&ie=UTF-8&mstk=AUtExfCG2_3KrXeDJdGSD1osiptihd7Rr_nHCWUwTYU5zyg28j8-2pYTtUkrg4dAfAEk73jhTCCV7UJ4l_PpoKdAoEk1Y48brOFmxE8jUecqX8Kbx1gUimn_lnE0_NapDJTU_wOOKDD0lSP6DwzIanzhppJ4S_AC1cHvhLAVDLXReV3128g&csui=3&ved=2ahUKEwjAt7fXo5yRAxUwRPEDHXF7DIoQgK4QegQIBRAH)), these models account for the spatial characteristics of the channel, including how the signal interacts with the antenna array.
- **[Ray tracing](https://www.google.com/search?q=Ray+tracing&rlz=1C1GCEU_deDE1112DE1112&oq=Air-to-ground+and+ground+to+air+channel+modelling&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIHCAEQIRifBdIBCTEwNDcwajBqN6gCALACAA&sourceid=chrome&ie=UTF-8&mstk=AUtExfCG2_3KrXeDJdGSD1osiptihd7Rr_nHCWUwTYU5zyg28j8-2pYTtUkrg4dAfAEk73jhTCCV7UJ4l_PpoKdAoEk1Y48brOFmxE8jUecqX8Kbx1gUimn_lnE0_NapDJTU_wOOKDD0lSP6DwzIanzhppJ4S_AC1cHvhLAVDLXReV3128g&csui=3&ved=2ahUKEwjAt7fXo5yRAxUwRPEDHXF7DIoQgK4QegQIBRAJ): A more complex and accurate method that simulates the paths of radio waves as they bounce off objects in the environment to predict signal propagation and multipath effects.** 

Why modeling is important

- **Performance evaluation**: Channel models allow engineers to simulate and evaluate the performance of A2G and G2A communication systems under various conditions without expensive and time-consuming flight tests.
- **System optimization**: They provide a basis for optimizing communication systems for reliability, efficiency, and performance.
- **Realistic testing**: Models enable the simulation of a wide range of scenarios and configurations that may be impractical to test in real-world flight trials.

**Definition (short):** An A2G/G2A channel model describes how radio signals propagate between an airborne node (UAV, balloon, HAP, airplane) and a ground node (base station, user equipment, sensor). It captures large-scale effects (path loss, elevation-dependent LOS probability, shadowing), small-scale fading (Rice/K-factor, multipath delay/angle spreads), Doppler/non-stationarity, and spatial/temporal correlation. [PMC+1](https://pmc.ncbi.nlm.nih.gov/articles/PMC10222034/?utm_source=chatgpt.com)
- **Key physical differences vs terrestrial channels:**
    - **Much higher LOS probability** (but depends on altitude and environment), so Ricean fading with large K is common. [ITU+1](https://www.itu.int/pub/S-JNL-VOL2.ISSUE2-2021-A11?utm_source=chatgpt.com)
    - **Height/elevation dependence**: path loss, shadowing, and the relative importance of reflections change strongly with UAV height. [MDPI](https://www.mdpi.com/2227-7390/13/21/3377?utm_source=chatgpt.com)
    - **Stronger, unusual interference patterns** in cellular-connected UAV scenarios because ground BS antennas are downtilted (interfere differently with airborne nodes). [ITU](https://www.itu.int/pub/S-JNL-VOL2.ISSUE2-2021-A11?utm_source=chatgpt.com)
    - **Rapid non-stationarity & Doppler** for moving UAVs (especially fast or rotary wing), requiring time-varying / spatially-consistent models.
- **It covers both.** “A2G/G2A” is the physical link description — it’s agnostic to the _role_ of the UAV. The same propagation phenomena matter whether the UAV is:

    - a **flying base station** (UAV-BS) providing coverage to ground users, or
    - a **cellular user equipment** (cell-connected UAV) served by ground BSs, or
    - a **relay/mesh node** between other UAVs and ground, or
    - **air-to-air (A2A)** links (related but modelled separately because geometry/relative motion differs). [ScienceDirect+1](https://www.sciencedirect.com/science/article/pii/S2405959522000157?utm_source=chatgpt.com)
- Practically, **model parameters and emphasis change** with the use case:
    
    - For UAV-BS design you often need **coverage maps, elevation-dependent PL, spatial consistency** (how coverage evolves during small movements). [arXiv](https://arxiv.org/html/2511.15412v1?utm_source=chatgpt.com)
    - For cellular-connected UAVs you need **interference models, base-station antenna patterns and handover behavior** because ground infrastructure was designed for terrestrial UEs.

To read 
- [ ] Book
- [ ] tab of papers sort
- [ ] Thesis 
- [ ] ITU Doc
- [ ] Read old nokia paper 
- [ ] Paper listed below


---

### Reasons 

### Paper 1
Ubiquitous accessibility worldwide and superior performance of cellular networks of communication like 4G and 5G make them a perfect candidate for air to ground (A2G) communications for low to medium altitude aircraft systems such as unmanned aerial vehicles (UAVs) and urban air mobility (UAM). However, cellular networks are designed and optimized for terrestrial users, and employing them communication of cellular connected aerial vehicles such as electric vertical take-off and landing (eVTOL) aircraft flying at higher altitudes and faster speeds is accompanied with some issues which should be resolved prior to application. Too many handovers and following consequences such as radio link failures, longer delays, and degraded throughput are major issues in wider employment of cellular networks for A2G communications. In this paper we have considered two main issues of handover in LTE networks when used for A2G communications of cellular-connected aircraft and have proposed novel handover algorithms addressing these issues which will decrease the number of unnecessary and ping pong handovers, as well as radio link failure rate for cellular connected aircraft. The improved performance of the proposed algorithms has been verified by extensive simulations in a bespoke designed simulation model for cellular connected aircraft served by LTE networks.  https://ieeexplore.ieee.org/abstract/document/9925868 

### Paper 2 - URLLC 
In this paper, we propose a model for beyond visual line of sight (BVLOS) operation for remote piloting of unmanned aerial vehicles (UAVs), which utilizes different technologies such as mobile edge computing and augmented reality. Ultra reliable low latency communication (URLLC) is a key service of 5G that enables safe BVLOS operation. Since message size of piloting signal is finite and communication channel is altitude dependent, we study reliability and latency under finite blocklength regime for different altitudes. In our numerical study, we find that for message sizes 30 and 50 bits, coded packet size, i.e., blocklength, should be in the range of 200 and 300 bits to enable BVLOS operation. We also found that minimum distance between UAVs to avoid any crash should be around 0.2 m for 15 m/s UAV speed and different altitudes ranging from 1.5 m to 120 m. According to our study, BVLOS operation of UAVs can be realized by URLLC by providing error probability in the vicinity of 10-3, and latency on the order of milliseconds for downlink communication with blocklength of tens to hundred bits. https://ieeexplore.ieee.org/abstract/document/8647652

==**G2A is Radio link**== 

Reliable Aerial Mobile Communications with RSRP & RSRQ Prediction Models for the Internet of Drones: A Machine Learning Approach https://www.mdpi.com/1424-8220/22/15/5522

To investigate the reliability of provided aerial coverage by the terrestrial cellular base stations (BSs), this article proposes six machine learning-based models to predict reference signal received power (RSRP) and reference signal received quality (RSRQ) based on the multiple linear regression, polynomial, and logarithmic methods. In this regard, first, a UAV-to-BS measurement campaign was conducted in a 4G LTE network within a suburban environment. Then, the aerial coverage was statistically analyzed and the prediction methods were developed as a function of distance and elevation angle. The results reveal the capability of terrestrial BSs in providing aerial coverage under some circumstances, which mainly depends on the distance between the UAV and BS and flight height. The performance evaluation shows that the proposed RSRP and RSRQ models achieved RMSE of 4.37 dBm and 2.71 dB for testing samples, respectively.

###  Paper 3 
Pathloss Analysis and Modelling for 5G Communication in U-SPACE https://ieeexplore.ieee.org/abstract/document/10253853 
This was done by field measurements with TSMA6B - an industrial-grade mobile frequency scanner, attached to a rotary-wing UAV. Using the network configurations obtained by the MNO (Mobile Network Operator), measurement campaigns were carried out at altitudes (22 - 35 meters) within the elevation angle of the transmitting antenna. Collected results were used to fit a path loss regression line for each altitude using the measured power of the reference signal and the instantaneous distance of the UAV from the base station. Findings from the analysis show that the path loss model is height dependent with altitude-specific cell edge requirements. In conclusion, the findings indicate that a 3.5GHz radio channel, deployed in a rural scenario, approximates a free space channel with an increase in altitude. This is because the channel conditions are similar to a line-of-sight scenario with increased altitude.


//Misc Papers

### URLLC Multi-link/connectivity 

Reliability and Delay Analysis of 3-Dimensional Networks With Multi-Connectivity: Satellite, HAPs, and Cellular Communications  https://ieeexplore.ieee.org/abstract/document/10227357 
Aerial vehicles (AVs) such as electric vertical take-off and landing (eVTOL) aircraft make aerial passenger transportation a reality in urban environments. However, their communication connectivity is still under research to realize their safe and full-scale operation. This paper envisages a multi-connectivity (MC) enabled aerial network to provide ubiquitous and reliable service to AVs. Vertical heterogeneous networks with direct air-to-ground (DA2G) and air-to-air (A2A) communication, high altitude platforms (HAPs), and low Earth orbit (LEO) satellites are considered. We evaluate the end-to-end (E2E) multi-hop reliability and network availability of the downlink of AVs for remote piloting scenarios, and control/telemetry traffic. Command and control (C2) connectivity service requires ultra-reliable and low-latency communication (URLLC), therefore we analyze E2E reliability and latency under the finite blocklength (FBL) regime. We explore how different MC options satisfy the demanding E2E connectivity requirements taking into account antenna radiation patterns and unreliable backhaul links. Since providing seamless connectivity to AVs is very challenging due to the line-of-sight (LoS) interference and reduced gains of downtilt ground base station (BS) antennas, we use coordinated multi-point (CoMP) among ground BSs to alleviate the inter-cell interference. Furthermore, we solve an optimization problem to select the best MC path under the quality of service (QoS) constraints. We maximize spectral efficiency (SE) to specify the optimum MC path with the minimum number of required links. Based on the simulation results, we find out that even with very efficient interference mitigation, MC is the key enabler for safe remote piloting operations.

### URLLC

URLLC (Ultra-Reliable Low-Latency Communication) is a specific service category in 5G and future 6G networks designed for mission-critical applications where failure or delay is unacceptable, such as remote robotic surgery, autonomous driving, and industrial automation.

Unlike standard mobile broadband (eMBB), which prioritizes speed (throughput), URLLC prioritizes **certainty**.

 **Executive Summary**

- **The Goal:** Deliver data with **<1 ms latency** and **>99.999% reliability**.
- **The Challenge:** Wireless channels are inherently unstable due to noise, interference, and reflection. URLLC must mathematically guarantee delivery despite these physical distortions.
- **Signal Strength:** Is not just about "bars" on a phone; in URLLC, it is about maintaining a massive "Fade Margin" so that even when the signal dips, it never drops below the decoding threshold.
- **Physical Distortion:** Includes **Multipath Fading** (echoes confusing the receiver) and **Doppler Shift** (movement distorting frequency).
- **Key Parameters:** The link is tuned using **Low-Order Modulation (QPSK)**, **High Subcarrier spacing (SCS)**, and **Diversity (MIMO)** to combat these distortions.

**1. The "Link" in URLLC: A Technical Overview**

In URLLC, the "link" refers to the air interface between the User Equipment (UE) and the Base Station (gNodeB). This link is fragile because it relies on radio waves that bounce, scatter, and fade.

To achieve URLLC standards, the link is engineered differently than a standard 4G/5G link:

- **Standard Link:** Optimizes for "Average" performance (it's okay if 1% of packets fail and need retransmission).
- **URLLC Link:** Optimizes for "Worst-Case" performance (the system is designed so that the _worst_ possible signal dip still allows successful decoding).

**2. Impact of Signal Strength**

Signal strength in URLLC is analyzed via the **Signal-to-Interference-plus-Noise Ratio (SINR)**.

- **The "Waterfall" Threshold:** Every modulation scheme (like QPSK or 16QAM) requires a minimum SINR to decode data successfully. If signal strength drops below this threshold, the **Block Error Rate (BLER)** spikes to 100%, causing packet loss.
- **The "Fade Margin":** To ensure 99.999% reliability, URLLC links do not target the _minimum_ necessary signal strength. Instead, they target a much higher strength (e.g., +20 dB above the minimum). This "buffer" ensures that even if a physical obstruction momentarily drops the signal strength by 15 dB, the link remains unbroken.
- **Impact on Latency:** Low signal strength forces the network to use "Repetitions" (sending the same packet 2-4 times blindly). While this improves reliability, it **increases latency** significantly. Therefore, high signal strength is a prerequisite for _low-latency_ reliability.

## **3. Impact of Physical Distortion**

Physical distortion refers to how the environment mangles the radio wave before it reaches the receiver.

**A. Multipath Fading (The "Echo" Problem)**

- **Phenomenon:** Radio waves bounce off walls and buildings, arriving at the receiver at slightly different times. Sometimes these waves arrive "out of phase" (one wave is a peak, the other is a trough), cancelling each other out.
- **Impact:** This causes **Deep Fades**, where signal strength can drop by 30-40 dB in milliseconds. In a standard video call, this causes a glitch. In URLLC (e.g., a moving robot), this could cause a safety stop.
- **URLLC Solution:** **Frequency Diversity**. URLLC spreads the data across a wider chunk of the spectrum so that if one specific frequency fades, the others survive.

**B. Doppler Shift (The "Movement" Problem)**

- **Phenomenon:** If the device is moving fast (e.g., a drone or car), the frequency of the radio wave shifts (stretches or compresses).
- **Impact:** This destroys the orthogonality of OFDM subcarriers, causing **Inter-Carrier Interference (ICI)**. The "lanes" of data start bleeding into each other, corrupting the packet.
- **URLLC Solution:** **High Subcarrier Spacing (SCS)**. By spacing the "lanes" further apart (e.g., 60 kHz instead of 15 kHz), the system becomes more tolerant to frequency shifts caused by speed.
    

 **C. Delay Spread**

- **Phenomenon:** Reflected signals arrive late. If the delay is too long, the "echo" of the previous symbol bleeds into the current symbol.
- **Impact:** **Inter-Symbol Interference (ISI)**. The receiver cannot distinguish the current 1 or 0 from the "ghost" of the previous one.
    

---

## **4. Parameters that Impact the Link**

Engineers tune specific parameters to balance the Reliability-Latency trade-off.

 **A. Configurable Parameters (Network Controlled)**

|Parameter|Description|Impact on URLLC|
|---|---|---|
|**MCS (Modulation & Coding Scheme)**|Determines how much data is packed into the wave.|**Low MCS (QPSK)** is used. It is slow but extremely robust against distortion. High MCS (64QAM) is avoided because it is fragile.|
|**SCS (Subcarrier Spacing)**|The width of frequency channels.|**Higher SCS (30/60 kHz)** shortens the symbol duration (Mini-slots), reducing latency to <0.5ms, but makes the signal slightly more prone to noise.|
|**Diversity Order**|Using multiple antennas to send the same data.|**Transmit Diversity** is prioritized over Spatial Multiplexing. Instead of sending 2 different streams for speed, we send 2 copies of the _same_ stream for reliability.|
|**Grant-Free Access**|Allowing devices to transmit without asking permission.|Removes the "Handshake" delay (Scheduling Request -> Grant), saving ~5-10ms of latency.|

**B. Environmental Parameters (Physics Controlled)**

|Parameter|Description|Impact on URLLC|
|---|---|---|
|**Coherence Time**|How long the channel stays stable.|If the device moves fast, coherence time drops. URLLC packets must be shorter than the coherence time to avoid corruption.|
|**Coherence Bandwidth**|The range of frequencies that fade together.|If the channel is "Frequency Selective," the link must use wider bandwidth to ensure some parts of the signal get through.|

**Summary Table: The URLLC Equation**

|Feature|Standard 5G (eMBB)|URLLC|Why?|
|---|---|---|---|
|**Modulation**|High (256 QAM)|**Low (QPSK/16QAM)**|Reliability > Speed. Easier to decode in noise.|
|**Coding Rate**|High (0.9)|**Very Low (0.1)**|90% of the transmission is "redundancy" to fix errors.|
|**Packet Size**|Large|**Small / Mini-slot**|Smaller packets transmit faster (lower latency).|
|**Retransmission**|Standard HARQ|**One-Shot / Fast HARQ**|No time to wait for multiple retransmissions.|

1. [https://www.a1.digital/knowledge-hub/urllc-the-5g-component-simply-explained/](https://www.a1.digital/knowledge-hub/urllc-the-5g-component-simply-explained/)
2. [https://opendl.ifip-tc6.org/db/conf/cnsm/cnsm2017/1570374956.pdf](https://opendl.ifip-tc6.org/db/conf/cnsm/cnsm2017/1570374956.pdf)
3. [https://pmc.ncbi.nlm.nih.gov/articles/PMC8871328/](https://pmc.ncbi.nlm.nih.gov/articles/PMC8871328/)
4. [https://pmc.ncbi.nlm.nih.gov/articles/PMC6427249/](https://pmc.ncbi.nlm.nih.gov/articles/PMC6427249/)
5. [https://www.quobis.com/2022/09/13/latency-and-reliability-in-5g-networks/](https://www.quobis.com/2022/09/13/latency-and-reliability-in-5g-networks/)
6. [https://resources.pcb.cadence.com/blog/2022-ultra-reliable-low-latency-communication-design-challenges-and-applications](https://resources.pcb.cadence.com/blog/2022-ultra-reliable-low-latency-communication-design-challenges-and-applications)
7. [https://ieeexplore.ieee.org/iel8/8782711/8889399/10824882.pdf](https://ieeexplore.ieee.org/iel8/8782711/8889399/10824882.pdf)
8. [https://trepo.tuni.fi/bitstream/10024/131373/2/AbdullatifHussein.pdf](https://trepo.tuni.fi/bitstream/10024/131373/2/AbdullatifHussein.pdf)
9. [https://www.rakon.com/white-paper-synchronisation-requirements-in-urllc-networks](https://www.rakon.com/white-paper-synchronisation-requirements-in-urllc-networks)
10. [https://www.eurecom.fr/publication/6437/download/comsys-publi-6437.pdf](https://www.eurecom.fr/publication/6437/download/comsys-publi-6437.pdf)
11. [https://arxiv.org/pdf/2101.05215.pdf](https://arxiv.org/pdf/2101.05215.pdf)
12. [https://research.aalto.fi/files/26167794/URLLCdesign.pdf](https://research.aalto.fi/files/26167794/URLLCdesign.pdf)
13. [https://onlinelibrary.wiley.com/doi/10.1155/2021/6651326](https://onlinelibrary.wiley.com/doi/10.1155/2021/6651326)
14. [https://arxiv.org/pdf/0811.3887.pdf](https://arxiv.org/pdf/0811.3887.pdf)
15. [https://www.telecomhall.net/t/higher-subcarrier-spacing-impact-on-throughput/9828](https://www.telecomhall.net/t/higher-subcarrier-spacing-impact-on-throughput/9828)
16. [https://lup.lub.lu.se/student-papers/record/9118249/file/9121617.pdf](https://lup.lub.lu.se/student-papers/record/9118249/file/9121617.pdf)
17. [https://arxiv.org/pdf/1803.04139.pdf](https://arxiv.org/pdf/1803.04139.pdf)
18. [https://arxiv.org/html/2508.20205v1](https://arxiv.org/html/2508.20205v1)
19. [https://www.gaussianwaves.com/2014/08/diversity-techniques-and-spatial-multiplexing/](https://www.gaussianwaves.com/2014/08/diversity-techniques-and-spatial-multiplexing/)
20. [https://pmc.ncbi.nlm.nih.gov/articles/PMC8038383/](https://pmc.ncbi.nlm.nih.gov/articles/PMC8038383/)

The "LAWN" domain in this context refers to the **Low-Altitude Wireless Network** (typically 0–400 ft or 0–120m AGL), where Beyond Visual Line of Sight (BVLOS) drones operate.

Achieving URLLC (Ultra-Reliable Low-Latency Communication) in this domain is significantly harder than on the ground because terrestrial networks are optimized for users walking on streets, not flying above them.

**Executive Summary: State of the Art (SoTA)**

The current State of the Art for URLLC in BVLOS operations has moved beyond simple 4G/5G connectivity to **AI-native, Multi-Link, and Deterministic** architectures.

- **Current Standard:** 3GPP Release 17/18 (5G-Advanced).
- **Top Innovation:** **Integrated Sensing and Communication (ISAC)** and **Predictive QoS** using flight paths.
- **Key Shift:** Moving from "Reactive" (fixing errors after they happen) to "Proactive" (predicting signal drops before the drone reaches the dead zone).

---

**1. The Core Challenge: The "Sky Paradox"**

In the LAWN domain, drones suffer from a unique problem: **Too much connectivity, yet poor quality.**

- **Ground User:** Sees 1–3 base stations.
- **Drone (at 100m):** Has Line-of-Sight (LoS) to 20+ base stations.
- **The SoTA Problem:** This causes **severe uplink interference**. The drone's radio shouts to one tower, but 20 other towers hear it as noise. Conversely, the drone hears 20 towers shouting, raising the noise floor and degrading the Signal-to-Interference-plus-Noise Ratio (SINR).
    

**2. State-of-the-Art Technologies (2024–2025 Status)**

 **A. 3GPP Release 18 & 19: The "AI-Native" Air Interface**

The latest 3GPP standards have introduced features specifically for UAVs to solve the interference issue:

- **Height-Dependent Measurement Reports (Events H1/H2):** The drone now reports its altitude to the network. If it flies too high, the network automatically switches it to a dedicated "Aerial Slice" or changes the beam pattern to avoid jamming ground users.[3gpp](https://www.3gpp.org/images/newsletters/3GPP_Highlights_Issue_6_opt.pdf)​
- **Flight Path Reporting:** The drone uploads its waypoints to the 5G core. The network then "pre-allocates" resources at the future base stations along the route, reducing handover latency to near-zero.[3gpp](https://www.3gpp.org/images/newsletters/3GPP_Highlights_Issue_6_opt.pdf)​

 **B. Physical Layer Innovations**

- **RIS (Reconfigurable Intelligent Surfaces) / "Smart Mirrors":**
    
    - **Concept:** Terrestrial towers effectively point _down_. To get signals _up_ to a drone without tilting antennas (which ruins ground coverage), operators are deploying RIS on rooftops.
    - **SoTA Application:** These surfaces passively reflect and focus beams upwards toward the drone, creating a virtual Line-of-Sight where none existed, stabilizing the link against physical blockages.[pureadmin.qub+1](https://pureadmin.qub.ac.uk/ws/portalfiles/portal/256105029/Aerial_Reconfigurable_Intelligent_Surface_Enabled_URLLC_UAV_Systems.pdf)​
        
- **ISAC (Integrated Sensing and Communication):**
    
    - **Concept:** Using the 5G radio wave for both data (C2 link) and radar (sensing).
    - **SoTA Application:** The drone uses its comms link to "see" obstacles or non-cooperative aircraft (intruders). This increases reliability by merging safety (detect-and-avoid) with connectivity, ensuring the drone doesn't crash while maintaining the link.[papers.ssrn+1](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4989029)​
        

 **C. Network Architecture: "Bonding" & Redundancy**

For BVLOS, a single link is no longer considered "Ultra-Reliable." The industry standard has shifted to **Packet Duplication** (PDCP Duplication).

- **Multi-Link Bonding:** Systems like _Elsight Halo_ or _Honeywell_ now split the C2 (Command & Control) data packet into pieces (or duplicate it entirely) and send it simultaneously over **4G, 5G, and Satellite (LEO)**.[commercialuavnews](https://www.commercialuavnews.com/solving-the-redundancy-puzzle-for-bvlos-uavs)​
- ==**The Result:** If the 5G tower fades due to a physical dip, the packet arrives via 4G or Satellite. This creates a "virtual" reliability of 99.9999% even if individual links are only 90% reliable.==
    

**D. Predictive Quality of Service (pQoS)**

Instead of reacting to a lost link, SoTA systems use **Machine Learning (ML)** to predict channel quality.

- **Mechanism:** The drone knows its 3D trajectory. The ML model maps this trajectory against a "Radio Environment Map" (REM).
- **Outcome:** The system predicts, _"In 20 seconds, you will enter a shadow zone behind that building."_ The drone proactively pauses high-bandwidth video streaming and prioritizes C2 data _before_ the drop occurs, ensuring the safety link never breaks.[aaltodoc.aalto+1](https://aaltodoc.aalto.fi/items/50369b47-b377-4cdc-bc78-863978b62b19)​
    

 **3. Summary of URLLC Evolution for Drones**

|Feature|Legacy (Standard 4G/LTE)|**State of the Art (5G-Advanced / BVLOS)**|
|---|---|---|
|**Interference**|High (Omnidirectional antennas)|**3D Beamforming** (Narrow beams track the drone)|
|**Handover**|Reactive (Break-before-make)|**Conditional Handover (CHO)** (Prepare target cell before leaving source)|
|**Reliability**|Single Link|**PDCP Duplication** (Send data on 2 frequencies simultaneously)|
|**Latency**|30–50 ms|**< 10 ms** (via Mini-slots and Edge Computing)|
|**Coverage**|Best Effort|**Sidelobe Suppression & Aerial Slicing**|

 **4. Conclusion**

The state of the art for LAWN URLLC is **Deterministic Multi-Connectivity**. We no longer rely on "hoping" the signal is strong enough. We guarantee it by **mathematically modeling the flight path**, using **AI to predict fades**, and **bonding multiple networks** (Cellular + Satellite) to ensure that even if physics distorts one signal, the data still gets through.

Check sources

1. [https://www.3gpp.org/images/newsletters/3GPP_Highlights_Issue_6_opt.pdf](https://www.3gpp.org/images/newsletters/3GPP_Highlights_Issue_6_opt.pdf)
2. [https://pureadmin.qub.ac.uk/ws/portalfiles/portal/256105029/Aerial_Reconfigurable_Intelligent_Surface_Enabled_URLLC_UAV_Systems.pdf](https://pureadmin.qub.ac.uk/ws/portalfiles/portal/256105029/Aerial_Reconfigurable_Intelligent_Surface_Enabled_URLLC_UAV_Systems.pdf)
3. [https://bcpublication.org/index.php/SJISR/article/view/8567](https://bcpublication.org/index.php/SJISR/article/view/8567)
4. [https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4989029](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4989029)
5. [https://hdiac.dtic.mil/articles/integrated-sensing-and-communications-for-small-uav-applications-in-cellular-networks/](https://hdiac.dtic.mil/articles/integrated-sensing-and-communications-for-small-uav-applications-in-cellular-networks/)
6. [https://www.commercialuavnews.com/solving-the-redundancy-puzzle-for-bvlos-uavs](https://www.commercialuavnews.com/solving-the-redundancy-puzzle-for-bvlos-uavs)
7. [https://aaltodoc.aalto.fi/items/50369b47-b377-4cdc-bc78-863978b62b19](https://aaltodoc.aalto.fi/items/50369b47-b377-4cdc-bc78-863978b62b19)
8. [https://cris.vtt.fi/en/publications/predictive-qos-for-cellular-connected-uav-communications/](https://cris.vtt.fi/en/publications/predictive-qos-for-cellular-connected-uav-communications/)
9. [https://arxiv.org/pdf/2205.06046.pdf](https://arxiv.org/pdf/2205.06046.pdf)
10. [https://www.updwg.org/wp-content/uploads/2020/11/DECENTRALIZING-DRONE-REGULATIONS-IN-low-altitude-airspace.pdf](https://www.updwg.org/wp-content/uploads/2020/11/DECENTRALIZING-DRONE-REGULATIONS-IN-low-altitude-airspace.pdf)
11. [https://www.3gpp.org/news-events/partner-news/3gpp-release-17-and-uav-applications](https://www.3gpp.org/news-events/partner-news/3gpp-release-17-and-uav-applications)
12. [https://pureadmin.qub.ac.uk/ws/portalfiles/portal/260708450/UAV_Enabled_Ultra_Reliable_Low_Latency_Communications_for_6G_A_Comprehensive_Survey.pdf](https://pureadmin.qub.ac.uk/ws/portalfiles/portal/260708450/UAV_Enabled_Ultra_Reliable_Low_Latency_Communications_for_6G_A_Comprehensive_Survey.pdf)
13. [https://ncgs.state.nc.us/docs/2023-07-25_FEMA-NC_Govt_Sector_UAS_meeting_support_doc_AUVSI_Blueprint_for_Autonomy_Building_Blocks_for_Our_Collective_Future.pdf](https://ncgs.state.nc.us/docs/2023-07-25_FEMA-NC_Govt_Sector_UAS_meeting_support_doc_AUVSI_Blueprint_for_Autonomy_Building_Blocks_for_Our_Collective_Future.pdf)
14. [https://blog.3g4g.co.uk/2022/12/3gpp-release-17-description-and-summary.html](https://blog.3g4g.co.uk/2022/12/3gpp-release-17-description-and-summary.html)
15. [https://ntrs.nasa.gov/api/citations/20190025711/downloads/20190025711.pdf](https://ntrs.nasa.gov/api/citations/20190025711/downloads/20190025711.pdf)
16. [https://flyingcar.sky.trade/p/drone-dominance-and-the-most-american](https://flyingcar.sky.trade/p/drone-dominance-and-the-most-american)
17. [https://uavcoach.com/inside-bvlos/](https://uavcoach.com/inside-bvlos/)
18. [https://arxiv.org/html/2510.08080v2](https://arxiv.org/html/2510.08080v2)
19. [https://www.ericsson.com/en/reports-and-papers/ericsson-technology-review/articles/5g-evolution-toward-5g-advanced](https://www.ericsson.com/en/reports-and-papers/ericsson-technology-review/articles/5g-evolution-toward-5g-advanced)


Based on my research, I can now provide you with a comprehensive analysis of your paper idea for the IEEE TVT Special Issue on LAWN.

## Assessment of Your Paper Idea for IEEE TVT LAWN Special Issue

## Is the Idea Relevant to the Journal?

**Yes, highly relevant.** Your proposed research aligns directly with **at least three topics of interest** listed in the Call for Papers:[vtsociety](https://vtsociety.org/files/ieeevts/2025-06/CFP%20SI_LAWN2026.pdf)​

1. **"URLLC for Safety-Critical Applications in LAWN"** — Your core objective of adapting transmissions based on latency and signal quality for BVLOS drones is precisely this.
    
2. **"Air-to-Ground and Air-to-Air Channel Modeling and Measurement for LAWN"** — The FEM-based propagation modeling by your colleague fits squarely here.
    
3. **"Cross-Layer Optimization for LAWN"** — Converting physical-layer RSSI/SINR into application-layer decisions (transmit rate, latency-aware scheduling) is textbook cross-layer design.
    

The CFP specifically calls for "highly reliable, low-latency communication" for "autonomous aerial logistics" and "public safety operations" in the 100–3000m altitude range. Your BVLOS drone scenario is a direct match.

---

## Gaps and Weaknesses in Your Current Idea Definition

Your current description lacks several elements that reviewers and guest editors will look for. Below is a structured critique:

## **Gap 1: Vagueness in the "Adaptive Transmission" Mechanism**

Your statement "use the latency and signal quality and transmit data accordingly" is too generic. You must define **what you are adapting**:

|What to Adapt?|Example Mechanism|Why It Matters for LAWN|
|---|---|---|
|**MCS (Modulation & Coding Scheme)**|Switch from 64QAM to QPSK when SINR drops|Standard link adaptation; needs novelty.|
|**Packet Size / Blocklength**|Use shorter packets in low-SINR zones for URLLC|Relevant for finite blocklength theory[sciencedirect](https://www.sciencedirect.com/science/article/pii/S2352864822001675)​.|
|**Transmission Scheduling**|Delay non-critical payload data; prioritize C2 (Command & Control)|Cross-layer; relates to Goal-Oriented Comms[arxiv+1](https://arxiv.org/abs/2408.04358)​.|
|**Path/Link Selection**|Switch from 5G to Satellite when entering shadow zone|Multi-link; highly relevant for BVLOS.|
|**Power Allocation**|Increase power in predicted weak zones|Energy-constrained; relevant for UAVs.|

**Action Required:** Define the specific "knob" you are turning based on the FEM-derived SINR distribution.

## **Gap 2: Missing "Prediction" Component**

Your colleague provides a **static** EM propagation distribution at various heights. The state-of-the-art has moved to **predictive** and **proactive** systems. A static map is useful, but reviewers will ask: _"How does the drone use this information in real-time?"_[aaltodoc.aalto+2](https://aaltodoc.aalto.fi/bitstreams/c57ea466-b785-4781-aa7c-76ae55ecb47d/download)​

The novelty gap here is between:

- **Reactive:** Drone measures current RSSI → Adapts transmission → (Latency added).
    
- **Proactive (SoTA):** Drone knows its future trajectory → Queries the FEM-derived 3D Radio Environment Map (REM) → Pre-adapts _before_ entering the weak zone.[aaltodoc.aalto+1](https://aaltodoc.aalto.fi/items/50369b47-b377-4cdc-bc78-863978b62b19)​
    

**Action Required:** Frame your contribution as a **proactive, trajectory-aware link adaptation** system. The FEM model becomes the **Digital Twin of the Radio Environment**.

## **Gap 3: Lack of Benchmarking and Novel Metric**

Current literature uses standard metrics: SINR, BLER, Throughput, Latency. For a LAWN/URLLC paper, you need to show:

- **Outage Probability at the 99.999% percentile** (not the average).[vbn.aau+1](https://vbn.aau.dk/ws/files/302583519/08361404.pdf)​
    
- **Age of Information (AoI)** for safety-critical C2 data.
    
- **Task Success Rate** if you adopt a Goal-Oriented Communication framework.[arxiv+1](https://arxiv.org/abs/2408.04358)​
    

**Action Required:** Define the URLLC constraint (e.g., 1ms latency, 10⁻⁵ BLER) and show how your system meets it under varying channel conditions.

## **Gap 4: FEM vs. Ray Tracing — What is the Novelty?**

The literature heavily uses **Ray Tracing (RT)** for UAV channel modeling. FEM is standard for indoor/material-specific propagation, but uncommon for large-scale outdoor Air-to-Ground (A2G) channels.[scirp+5](https://www.scirp.org/journal/paperinformation?paperid=128131)​

**Potential Novelty Angles for FEM:**

- **Near-Ground Effects:** FEM can model complex ground reflections and building material properties (concrete, glass) more accurately than statistical models for low-altitude (<100m) urban canyons.
    
- **Electromagnetic Material Interaction:** If your scenario involves flying near specific infrastructure (e.g., metal bridges, harbor cranes for your drone logistics corridor), FEM can capture scattering and diffraction effects that simplified RT misses.
    
- **Validation Against Measurements:** A strong paper would validate the FEM model against real drone flight measurements.
    

**Action Required:** Clearly articulate _why FEM is superior_ to (or necessary alongside) the standard 3GPP TR 36.777/TR 38.901 statistical models or RT for your specific LAWN scenario.

---

## How to Make This Novel and Publishable

Based on the CFP and the state-of-the-art, here is a **reframed paper concept** that would be competitive:

## **Proposed Title:**

_"FEM-Derived 3D Radio Environment Maps for Proactive, URLLC-Compliant Link Adaptation in Low-Altitude Drone Operations"_

## **Novel Contributions to Claim:**

1. **A Novel FEM-based 3D Radio Environment Map (REM) for LAWN:**
    
    - Generate height-dependent RSSI/SINR distributions using FEM that capture urban material properties (concrete, metal, glass) with higher fidelity than statistical models for the 0–300m altitude layer.[ncrl.seu+1](https://ncrl.seu.edu.cn/_upload/article/files/45/01/d175be50402a9292cbee84b68fb8/9ab94c52-b41a-4fe3-9848-926b5298aff6.pdf)​
        
    - Validate against real-world flight measurements in a representative scenario (e.g., harbor-to-urban corridor).
        
2. **Proactive, Trajectory-Aware Link Adaptation Framework:**
    
    - The drone uploads its planned 4D trajectory (x, y, z, t) to an edge server.
        
    - The server queries the FEM-derived REM and predicts the SINR profile along the path.[cris.vtt+1](https://cris.vtt.fi/en/publications/predictive-qos-for-cellular-connected-uav-communications/)​
        
    - **Novelty:** A proactive decision algorithm that pre-selects MCS, blocklength, and transmission timing _N_ seconds ahead to meet a target URLLC constraint (e.g., 99.999% reliability at 10ms latency).[pmc.ncbi.nlm.nih+1](https://pmc.ncbi.nlm.nih.gov/articles/PMC12158281/)​
        
3. **Cross-Layer Optimization (Tying to CFP Topic):**
    
    - Integrate the physical-layer FEM channel model with a MAC-layer scheduler.
        
    - Show how priority is given to C2 data under predicted signal degradation, while payload data (video) is gracefully degraded (rate adaptation).[arxiv+1](https://arxiv.org/html/2510.08080v1)​
        
4. **Performance Evaluation under URLLC Metrics:**
    
    - Benchmark against: (a) Reactive link adaptation (standard 5G NR outer-loop), (b) 3GPP TR 36.777 statistical model-based prediction.
        
    - Metrics: Latency Violation Probability, Outage Probability at 10⁻⁵, Age of Information for C2 packets.
        

---

## Summary: Your Strengths and Weaknesses

|Aspect|Current Status|Action Needed|
|---|---|---|
|**Topic Fit**|✅ Excellent fit for URLLC + Channel Modeling topics.|None.|
|**FEM Modeling**|⚠️ Novelty unclear vs. Ray Tracing.|Justify FEM for material-specific urban LAWN.|
|**RSSI → SINR Conversion**|✅ Standard, but needs interference model.|Define interference model (from other cells, UEs).|
|**"Transmit data accordingly"**|❌ Too vague.|Specify: MCS? Blocklength? Scheduling? Power?|
|**Latency/Reliability Constraint**|❌ Not defined.|Define URLLC target (e.g., 1ms, 10⁻⁵).|
|**Proactive vs. Reactive**|❌ Not mentioned.|Frame as Predictive QoS using trajectory.|
|**Validation**|❌ Not mentioned.|Plan for simulation (OMNeT++/INET?) or testbed.|

Your core idea is sound and relevant. The transformation from a "good idea" to an "accepted IEEE TVT paper" requires sharpening the **novelty claim** (FEM + Proactive + Cross-Layer), defining the **URLLC constraint mathematically**, and **benchmarking rigorously**. I recommend aligning closely with the "URLLC for Safety-Critical Applications in LAWN" and "Cross-Layer Optimization for LAWN" topics in your abstract and introduction.

1. [https://vtsociety.org/files/ieeevts/2025-06/CFP%20SI_LAWN2026.pdf](https://vtsociety.org/files/ieeevts/2025-06/CFP%20SI_LAWN2026.pdf)
2. [https://www.sciencedirect.com/science/article/pii/S2352864822001675](https://www.sciencedirect.com/science/article/pii/S2352864822001675)
3. [https://arxiv.org/abs/2408.04358](https://arxiv.org/abs/2408.04358)
4. [https://www.ijetcsit.org/index.php/ijetcsit/article/download/434/386](https://www.ijetcsit.org/index.php/ijetcsit/article/download/434/386)
5. [https://aaltodoc.aalto.fi/bitstreams/c57ea466-b785-4781-aa7c-76ae55ecb47d/download](https://aaltodoc.aalto.fi/bitstreams/c57ea466-b785-4781-aa7c-76ae55ecb47d/download)
6. [https://cris.vtt.fi/en/publications/predictive-qos-for-cellular-connected-uav-communications/](https://cris.vtt.fi/en/publications/predictive-qos-for-cellular-connected-uav-communications/)
7. [https://aaltodoc.aalto.fi/items/50369b47-b377-4cdc-bc78-863978b62b19](https://aaltodoc.aalto.fi/items/50369b47-b377-4cdc-bc78-863978b62b19)
8. [https://vbn.aau.dk/ws/files/302583519/08361404.pdf](https://vbn.aau.dk/ws/files/302583519/08361404.pdf)
9. [https://vbn.aau.dk/ws/files/310030894/08705373.pdf](https://vbn.aau.dk/ws/files/310030894/08705373.pdf)
10. [https://www.scirp.org/journal/paperinformation?paperid=128131](https://www.scirp.org/journal/paperinformation?paperid=128131)
11. [https://www.nature.com/articles/s41598-025-02803-4](https://www.nature.com/articles/s41598-025-02803-4)
12. [https://vbn.aau.dk/files/318346362/shadow_fading_RT_UAVs.pdf](https://vbn.aau.dk/files/318346362/shadow_fading_RT_UAVs.pdf)
13. [https://cris.vtt.fi/en/publications/generative-neural-network-channel-modeling-for-millimeter-wave-ua](https://cris.vtt.fi/en/publications/generative-neural-network-channel-modeling-for-millimeter-wave-ua)
14. [https://ceur-ws.org/Vol-3793/paper_23.pdf](https://ceur-ws.org/Vol-3793/paper_23.pdf)
15. [https://ncrl.seu.edu.cn/_upload/article/files/45/01/d175be50402a9292cbee84b68fb8/9ab94c52-b41a-4fe3-9848-926b5298aff6.pdf](https://ncrl.seu.edu.cn/_upload/article/files/45/01/d175be50402a9292cbee84b68fb8/9ab94c52-b41a-4fe3-9848-926b5298aff6.pdf)
16. [https://pmc.ncbi.nlm.nih.gov/articles/PMC12158281/](https://pmc.ncbi.nlm.nih.gov/articles/PMC12158281/)
17. [https://arxiv.org/html/2510.08080v1](https://arxiv.org/html/2510.08080v1)
18. [https://arxiv.org/pdf/1801.07359.pdf](https://arxiv.org/pdf/1801.07359.pdf)
19. [https://www.eurecom.fr/publication/6901/download/comsys-publi-6901.pdf](https://www.eurecom.fr/publication/6901/download/comsys-publi-6901.pdf)
20. [https://pmc.ncbi.nlm.nih.gov/articles/PMC9331756/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9331756/)
21. [https://applexiong.github.io/PDF/2023/IEEE_IoTJ_vol_11_no_6_pp_10054_10068_Mar_2024.pdf](https://applexiong.github.io/PDF/2023/IEEE_IoTJ_vol_11_no_6_pp_10054_10068_Mar_2024.pdf)
22. [https://pmc.ncbi.nlm.nih.gov/articles/PMC9781936/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9781936/)
23. [https://arxiv.org/html/2510.08752v1](https://arxiv.org/html/2510.08752v1)
24. [https://people.computing.clemson.edu/~jmarty/projects/lowLatencyNetworking/papers/LossandPropModels/ForUAVSystems/SurveyOfAirToGndChannelModelingForDrones.pdf](https://people.computing.clemson.edu/~jmarty/projects/lowLatencyNetworking/papers/LossandPropModels/ForUAVSystems/SurveyOfAirToGndChannelModelingForDrones.pdf)
25. [https://arxiv.org/html/2505.06944v3](https://arxiv.org/html/2505.06944v3)
26. [https://www.tlc.unipr.it/ferrari/Publications/Journals/Pa_et_al_ACC24.pdf](https://www.tlc.unipr.it/ferrari/Publications/Journals/Pa_et_al_ACC24.pdf)
27. [https://www.eurecom.fr/en/publication/5452/download/comsys-publi-5452.pdf](https://www.eurecom.fr/en/publication/5452/download/comsys-publi-5452.pdf)
28. [https://onlinelibrary.wiley.com/doi/10.1155/2024/9062023](https://onlinelibrary.wiley.com/doi/10.1155/2024/9062023)
29. [https://www.diva-portal.org/smash/get/diva2:1845283/FULLTEXT01.pdf](https://www.diva-portal.org/smash/get/diva2:1845283/FULLTEXT01.pdf)
30. [https://www.sciencedirect.com/science/article/abs/pii/S1434841119321685](https://www.sciencedirect.com/science/article/abs/pii/S1434841119321685)
31. [https://ieeexplore.ieee.org/document/9149190/](https://ieeexplore.ieee.org/document/9149190/)
32. [https://www.sciencedirect.com/science/article/am/pii/S1389128620311324](https://www.sciencedirect.com/science/article/am/pii/S1389128620311324)
33. [https://d197for5662m48.cloudfront.net/documents/publicationstatus/128827/preprint_pdf/058e6f51d94d4f04697c413867dbc8b2.pdf](https://d197for5662m48.cloudfront.net/documents/publicationstatus/128827/preprint_pdf/058e6f51d94d4f04697c413867dbc8b2.pdf)
34. [https://www.sciencedirect.com/science/article/pii/S1574119224001238](https://www.sciencedirect.com/science/article/pii/S1574119224001238)
35. [https://par.nsf.gov/servlets/purl/10278341](https://par.nsf.gov/servlets/purl/10278341)
36. [https://www.techrxiv.org/users/808339/articles/1208490/master/file/data/main/main.pdf?inline=true](https://www.techrxiv.org/users/808339/articles/1208490/master/file/data/main/main.pdf?inline=true)
37. [https://eprints.whiterose.ac.uk/id/eprint/191390/1/An%20Improved%20Q-Learning%20Based%20Handover%20Scheme.pdf](https://eprints.whiterose.ac.uk/id/eprint/191390/1/An%20Improved%20Q-Learning%20Based%20Handover%20Scheme.pdf)
38. [https://www.sciencedirect.com/science/article/abs/pii/S1874490724002313](https://www.sciencedirect.com/science/article/abs/pii/S1874490724002313)
39. [https://www.eurecom.edu/publication/7003/download/comsys-publi-7003.pdf](https://www.eurecom.edu/publication/7003/download/comsys-publi-7003.pdf)
40. [https://patents.google.com/patent/US20230007564A1/en](https://patents.google.com/patent/US20230007564A1/en)
41. [https://arxiv.org/pdf/2502.03850.pdf](https://arxiv.org/pdf/2502.03850.pdf)
42. [https://dl.acm.org/doi/10.1145/3360774.3368199](https://dl.acm.org/doi/10.1145/3360774.3368199)
43. [https://arxiv.org/pdf/2206.11565.pdf](https://arxiv.org/pdf/2206.11565.pdf)
44. [https://www.sciencedirect.com/science/article/abs/pii/S0140366422000561](https://www.sciencedirect.com/science/article/abs/pii/S0140366422000561)
45. [https://www.grin.com/document/283052](https://www.grin.com/document/283052)
46. [https://peerj.com/articles/cs-2557/](https://peerj.com/articles/cs-2557/)
47. [https://arxiv.org/html/2508.20205v1](https://arxiv.org/html/2508.20205v1)
48. [https://ieeexplore.ieee.org/document/1321503/](https://ieeexplore.ieee.org/document/1321503/)
49. [https://ieeexplore.ieee.org/iel7/6287639/8274985/08361404.pdf](https://ieeexplore.ieee.org/iel7/6287639/8274985/08361404.pdf)
50. [https://download.e-bookshelf.de/download/0002/3037/59/L-G-0002303759-0003166034.pdf](https://download.e-bookshelf.de/download/0002/3037/59/L-G-0002303759-0003166034.pdf)
51. [https://www.techrxiv.org/users/874078/articles/1254303/master/file/data/URLLC_Survey/URLLC_Survey.pdf](https://www.techrxiv.org/users/874078/articles/1254303/master/file/data/URLLC_Survey/URLLC_Survey.pdf)
52. [https://www.wiley-vch.de/de/fachgebiete/ingenieurwesen/propagation-channel-characterization-parameter-estimation-and-modeling-for-wireless-communications-978-1-118-18823-1](https://www.wiley-vch.de/de/fachgebiete/ingenieurwesen/propagation-channel-characterization-parameter-estimation-and-modeling-for-wireless-communications-978-1-118-18823-1)
53. [https://mediatum.ub.tum.de/doc/1738030/1738030.pdf](https://mediatum.ub.tum.de/doc/1738030/1738030.pdf)
54. [https://arxiv.org/pdf/2012.06707.pdf](https://arxiv.org/pdf/2012.06707.pdf)
55. [http://scis.scichina.com/en/2021/120301.pdf](http://scis.scichina.com/en/2021/120301.pdf)
56. [https://tsapps.nist.gov/publication/get_pdf.cfm?pub_id=51188](https://tsapps.nist.gov/publication/get_pdf.cfm?pub_id=51188)
57. [https://pureadmin.qub.ac.uk/ws/portalfiles/portal/260708450/UAV_Enabled_Ultra_Reliable_Low_Latency_Communications_for_6G_A_Comprehensive_Survey.pdf](https://pureadmin.qub.ac.uk/ws/portalfiles/portal/260708450/UAV_Enabled_Ultra_Reliable_Low_Latency_Communications_for_6G_A_Comprehensive_Survey.pdf)
58. [http://www.diva-portal.org/smash/get/diva2:1412178/FULLTEXT01.pdf](http://www.diva-portal.org/smash/get/diva2:1412178/FULLTEXT01.pdf)
59. [https://www.sciencedirect.com/science/article/pii/S2215098625002538](https://www.sciencedirect.com/science/article/pii/S2215098625002538)
60. [https://www.ant.uni-bremen.de/en/finished_student_theses/2006/4138/](https://www.ant.uni-bremen.de/en/finished_student_theses/2006/4138/)
61. [https://ncrl.seu.edu.cn/_upload/article/files/3a/d1/7bcbf1e347a880a8b59d7660cbdb/9499810b-82d7-420e-aeea-3e8d7dbcd7c0.pdf](https://ncrl.seu.edu.cn/_upload/article/files/3a/d1/7bcbf1e347a880a8b59d7660cbdb/9499810b-82d7-420e-aeea-3e8d7dbcd7c0.pdf)
62. [https://arxiv.org/html/2502.10324v1](https://arxiv.org/html/2502.10324v1)
63. [https://decentcybersecurity.eu/low-latency-communication-protocols-for-drone-iff-ensuring-swift-and-secure-identification/](https://decentcybersecurity.eu/low-latency-communication-protocols-for-drone-iff-ensuring-swift-and-secure-identification/)
64. [https://amns.sciendo.com/es/article/10.2478/amns-2024-1919?tab=references](https://amns.sciendo.com/es/article/10.2478/amns-2024-1919?tab=references)
65. [https://ieeexplore.ieee.org/iel8/9882533/10792972/10879292.pdf](https://ieeexplore.ieee.org/iel8/9882533/10792972/10879292.pdf)
66. [https://mdpi-res.com/bookfiles/topic/10017/Unmanned_Ground_and_Aerial_Vehicles_UGVsUAVs_for_Digital_Farming.pdf?v=1754529015](https://mdpi-res.com/bookfiles/topic/10017/Unmanned_Ground_and_Aerial_Vehicles_UGVsUAVs_for_Digital_Farming.pdf?v=1754529015)
67. [https://arxiv.org/abs/2502.03761](https://arxiv.org/abs/2502.03761)
68. [https://www.nature.com/articles/s41598-024-68459-8](https://www.nature.com/articles/s41598-024-68459-8)
69. [https://arxiv.org/pdf/2306.02917.pdf](https://arxiv.org/pdf/2306.02917.pdf)
70. [https://arxiv.org/html/2505.06944v1](https://arxiv.org/html/2505.06944v1)
71. [https://www.sciencedirect.com/science/article/pii/S1389128624001087](https://www.sciencedirect.com/science/article/pii/S1389128624001087)
72. [https://www.sciencedirect.com/science/article/abs/pii/S1874490723000666](https://www.sciencedirect.com/science/article/abs/pii/S1874490723000666)
73. [https://vtsociety.org/post/announcement/call-papers-special-issue-low-altitude-wireless-networks-lawn](https://vtsociety.org/post/announcement/call-papers-special-issue-low-altitude-wireless-networks-lawn)
74. [https://ieeexplore.ieee.org/iel8/4234/10713398/10634104.pdf](https://ieeexplore.ieee.org/iel8/4234/10713398/10634104.pdf)
75. [http://ieeexplore.ieee.org/iel8/6979/11220917/11220875.pdf](http://ieeexplore.ieee.org/iel8/6979/11220917/11220875.pdf)
76. [https://dl.acm.org/doi/10.1145/3703790.3703808](https://dl.acm.org/doi/10.1145/3703790.3703808)
77. [https://dl.acm.org/doi/abs/10.1109/TWC.2024.3424493](https://dl.acm.org/doi/abs/10.1109/TWC.2024.3424493)
78. [https://wcnc2025.ieee-wcnc.org/program-0](https://wcnc2025.ieee-wcnc.org/program-0)
79. [https://www.oaepublish.com/articles/ces.2025.55](https://www.oaepublish.com/articles/ces.2025.55)
80. [https://ui.adsabs.harvard.edu/abs/2025ITVT...74.1610Q/abstract](https://ui.adsabs.harvard.edu/abs/2025ITVT...74.1610Q/abstract)
81. [https://www.semanticscholar.org/paper/A-Secure-Communication-Protocol-for-Drones-and-Won-Seo/c764ae6ce21efc949033c0c29936aff41325c79b](https://www.semanticscholar.org/paper/A-Secure-Communication-Protocol-for-Drones-and-Won-Seo/c764ae6ce21efc949033c0c29936aff41325c79b)
82. [https://arxiv.org/pdf/2301.12678.pdf](https://arxiv.org/pdf/2301.12678.pdf)
83. [https://vtechworks.lib.vt.edu/bitstream/handle/10919/113548/Adaptive_Height_Optimization_for_Cellular-Connected_UAVs_A_Deep_Reinforcement_Learning_Approach.pdf](https://vtechworks.lib.vt.edu/bitstream/handle/10919/113548/Adaptive_Height_Optimization_for_Cellular-Connected_UAVs_A_Deep_Reinforcement_Learning_Approach.pdf)
84. [https://arxiv.org/abs/1801.01656](https://arxiv.org/abs/1801.01656)
85. [http://www.diva-portal.org/smash/get/diva2:1942282/FULLTEXT02.pdf](http://www.diva-portal.org/smash/get/diva2:1942282/FULLTEXT02.pdf)
86. [https://www.sciencedirect.com/science/article/abs/pii/S1874490724002714](https://www.sciencedirect.com/science/article/abs/pii/S1874490724002714)
87. [https://www.ijert.org/research/modeling-simulation-of-air-to-ground-propagation-channel-IJERTV4IS040488.pdf](https://www.ijert.org/research/modeling-simulation-of-air-to-ground-propagation-channel-IJERTV4IS040488.pdf)
88. [https://www.sciencedirect.com/science/article/pii/S1389128624006212](https://www.sciencedirect.com/science/article/pii/S1389128624006212)
89. [https://arxiv.org/pdf/2304.04163.pdf](https://arxiv.org/pdf/2304.04163.pdf)
90. [https://oa.upm.es/43353/1/LEI_ZHANG.pdf](https://oa.upm.es/43353/1/LEI_ZHANG.pdf)
91. [https://par.nsf.gov/servlets/purl/10451174](https://par.nsf.gov/servlets/purl/10451174)
92. [https://vbn.aau.dk/ws/files/549464605/PHD_Rafhael_Medeiros_de_Amorim_E_pdf.pdf](https://vbn.aau.dk/ws/files/549464605/PHD_Rafhael_Medeiros_de_Amorim_E_pdf.pdf)
93. [https://papers.ssrn.com/sol3/Delivery.cfm/310412d5-7986-48e6-8722-f5aadd781ff4-MECA.pdf?abstractid=5399273&mirid=1](https://papers.ssrn.com/sol3/Delivery.cfm/310412d5-7986-48e6-8722-f5aadd781ff4-MECA.pdf?abstractid=5399273&mirid=1)
94. [https://pmc.ncbi.nlm.nih.gov/articles/PMC6929112/](https://pmc.ncbi.nlm.nih.gov/articles/PMC6929112/)
95. [https://dl.acm.org/doi/10.1145/3657287](https://dl.acm.org/doi/10.1145/3657287)
96. [https://pdfs.semanticscholar.org/2d51/d1854041ceecdd89870e57f225e7cfe63c2a.pdf](https://pdfs.semanticscholar.org/2d51/d1854041ceecdd89870e57f225e7cfe63c2a.pdf)


## **1. Can FEM be "Evaluated" Against Ray Tracing? (The "Validation" Strategy)**

**Yes, absolutely.** In the absence of flight tests, benchmarking your high-fidelity FEM model against a widely accepted Ray Tracing (RT) model is a standard valid research methodology. This is often called **"Cross-Model Validation"** or **"Inter-Model Comparative Analysis."**

To make this acceptable for _IEEE TVT_, you must frame it correctly:

- **The Narrative:** "Ray Tracing (RT) is the industry standard for large-scale coverage, but it fails to capture complex diffraction and scattering near complex obstacles (e.g., metal cranes, bridge cables). Our FEM model provides 'Ground Truth' fidelity in these critical zones."
    
- **The Strategy:** Use Ray Tracing as the **"Baseline"** and FEM as the **"High-Precision Enhancement."**
    
    - **Show Agreement:** Demonstrate that in open space (Line-of-Sight), your FEM results match RT results (validates your physics).
        
    - **Show Divergence:** Demonstrate that in "shadow zones" (behind buildings/structures), FEM reveals _different_ signal behavior (e.g., deep fades or waveguide effects) that RT misses. **This divergence is your "Novelty."**
        

---

## **2. Proposed Simulation Setup: From FEM Physics to Logical VM**

You need to build a pipeline that converts "Physics" (E-Field) into "Logic" (Packet Loss/Throughput). Here is a specific 3-stage architecture for your paper:

## **Phase A: The "Offline" Physical Layer (FEM & SINR Map)**

- **Input:** Your colleague's FEM data.
    
- **Process:**
    
    1. **Raw Export:** Export FEM results as a 3D Grid CSV: `[x, y, z, E_field_magnitude]`.
        
    2. **RSSI Conversion:** Convert E-field to Received Power ($P_{rx}$) in dBm using the antenna aperture formula.
        
    3. **Interference Injection:** Since FEM only models _propagation_ (signal), you must model _noise_. Create a "Noise Floor" variable (e.g., -100 dBm) or add a probabilistic interference map from "neighboring cells."
        
    4. **SINR Generation:**  
        SINR(x,y,z)=Prx(x,y,z)−(Iinterference+Nnoise)\text{SINR}(x,y,z) = P_{rx}(x,y,z) - (I_{interference} + N_{noise})SINR(x,y,z)=Prx(x,y,z)−(Iinterference+Nnoise)
        
- **Output Artifact:** A **"3D Quality Trace File"** (e.g., HDF5 or JSON) that maps spatial coordinates to SINR.
    

## **Phase B: The "Online" Logical Layer (The VM Setup)**

This is where you simulate the drone's network behavior.

**Option 1: Pure Simulation (ns-3 or MATLAB)**

- **Setup:** Use **ns-3** (Network Simulator 3).
    
- **Implementation:**
    
    - Create a **custom PropagationLossModel** class in ns-3.
        
    - Instead of calculating path loss using a formula, this class **reads your Phase A Trace File**.
        
    - When the simulated drone moves to position $(x,y,z)$, the simulator looks up the exact SINR from your FEM data.
        
- **Why this is good:** Reviewers love ns-3 because it accurately models the full protocol stack (TCP/IP, MAC retransmissions).
    

**Option 2: Emulation (Mininet-WiFi + Real VM)**

- **Setup:** If you want to run _actual_ code (e.g., a video streaming app) inside a VM.
    
- **Tool:** **Mininet-WiFi** or a Linux **Traffic Control (tc)** script.
    
- **Workflow:**
    
    1. **Trajectory Script:** A Python script simulates the drone "flying" through your 3D coordinates.
        
    2. **Real-Time Lookup:** Every 100ms, the script queries the Phase A SINR map.
        
    3. **Bandwidth Throttling:** The script maps SINR -> Throughput (using an MCS Table) and applies a standard Linux traffic shaping command to the VM's network interface:
        
        bash
        
        `# Example: Degrade VM interface to 2Mbps because FEM says SINR is low tc qdisc change dev eth0 root tbf rate 2mbit burst 32kbit latency 400ms`
        
- **Why this is good:** You can say, "We tested real video streaming software over an FEM-emulated channel."
    

---

## **3. Key "Novelty" Gaps to Fill in the Paper**

To ensure acceptance, explicitly address these in your simulation section:

1. **The "Cliff Edge" Effect:** Show a graph where RT predicts a smooth signal drop, but FEM predicts a sharp "cliff" (sudden drop) due to destructive interference. Explain how your "Proactive Link Adaptation" saves the drone from this specific cliff.
    
2. **Link-to-System (L2S) Mapping:** Explicitly state how you map FEM SINR to Packet Error Rate (BLER). Don't just say "we converted it." Cite a standard **5G NR LDPC Block Error Rate curve** (e.g., from 3GPP TS 38.214).
    
3. **The "Processing Delay" Argument:** If using FEM is computationally heavy, clarify that the FEM map is **pre-computed** (offline) and stored as a "Digital Twin" map. The drone only does a simple _lookup_ (O(1) complexity) in real-time. This proves it is feasible for low-latency operations.
    

4. [https://web.ornl.gov/~1qn/papers/hsc2006.pdf](https://web.ornl.gov/~1qn/papers/hsc2006.pdf)
5. [https://arxiv.org/html/2503.01300v1](https://arxiv.org/html/2503.01300v1)
6. [http://publications.rwth-aachen.de/record/723884/files/723884.pdf](http://publications.rwth-aachen.de/record/723884/files/723884.pdf)
7. [https://ns3-code.com/how-to-begin-implement-data-link-layer-in-ns3/](https://ns3-code.com/how-to-begin-implement-data-link-layer-in-ns3/)
8. [https://www.mathworks.com/matlabcentral/fileexchange/165746-simulation-tool-for-modeling-path-loss-scenarios](https://www.mathworks.com/matlabcentral/fileexchange/165746-simulation-tool-for-modeling-path-loss-scenarios)
9. [https://research-information.bris.ac.uk/files/2992100/Athanasiadou_IEEE_JSAC_March2000.pdf](https://research-information.bris.ac.uk/files/2992100/Athanasiadou_IEEE_JSAC_March2000.pdf)
10. [https://www.vodafone-chair.org/pbls/legacy/m-grieger/Ray-Tracing_Wireless_Channel_Modeling_and_Verification_in_Coordinated_Multi-Point_Systems.pdf](https://www.vodafone-chair.org/pbls/legacy/m-grieger/Ray-Tracing_Wireless_Channel_Modeling_and_Verification_in_Coordinated_Multi-Point_Systems.pdf)
11. [https://papers.ssrn.com/sol3/Delivery.cfm/a08c7fb1-356f-4f98-bcf1-22936c14b194-MECA.pdf?abstractid=4366462&mirid=1](https://papers.ssrn.com/sol3/Delivery.cfm/a08c7fb1-356f-4f98-bcf1-22936c14b194-MECA.pdf?abstractid=4366462&mirid=1)
12. [https://www.dei.unipd.it/~rossi/papers/MSWiM_long_version.pdf](https://www.dei.unipd.it/~rossi/papers/MSWiM_long_version.pdf)
13. [https://www.mathworks.com/help/5g/ug/include-path-loss-in-nr-link-level-simulations.html](https://www.mathworks.com/help/5g/ug/include-path-loss-in-nr-link-level-simulations.html)
Scenario based fitting  - Especially when an   airspace is under planning to be closed due to helicopter   landing, Emergency on the ground infrastructure like fire etc.,   and all the drones are expected to land in an unplanned   location or divert, time is of the essence here. Such emergency  
landing and the ”impact of communication requirement”

**Yes, this scenario is an excellent fit** for your paper idea. In fact, it significantly strengthens your value proposition by moving from a generic "flight optimization" paper to a "mission-critical safety" paper.

This "Emergency Airspace Closure & Forced Diversion" scenario provides the perfect **stress test** for your FEM-based link adaptation system. It justifies _why_ you need a high-fidelity FEM model: simply knowing the "average" signal isn't enough when a drone is forced to fly into an unplanned, signal-shadowed "urban canyon" to land immediately.

## **How to Integrate This Scenario into Your Paper**

Here is how you can map this "Emergency Landing" narrative to your technical contribution:

## **1. The Problem Statement (The "Hook")**

- **Current Gap:** Most drone communication research assumes a pre-planned, optimal flight path at 100m altitude.
- **The Crisis:** Real-world operations (U-Space/UTM) will face "Dynamic Airspace Closures" (e.g., a helicopter needs to land, or a fire starts). This forces drones to divert _instantly_ to low-altitude, unplanned "contingency landing spots."
- **The Risk:** These unplanned spots are often in "dead zones" (between buildings, near ground clutter) where standard ray-tracing models fail to predict deep fades accurately. A loss of C2 (Command & Control) link here = a crash or a rogue drone.
    

## **2. The Solution (Your Contribution)**

- **Your Proposed System:** "Proactive Link Assurance for Contingency Operations."
    
- **Mechanism:**
    
    1. **Trigger:** The UTM system broadcasts an "Airspace Closed" event.
        
    2. **Path Generation:** The drone's computer calculates a diversion path to the nearest safe landing zone.
        
    3. **The Novel Step:** Before committing to this path, the drone queries your **FEM-based Radio Environment Map**.
        
    4. **Outcome:** The map predicts a "signal cliff" (deep fade) on the shortest path. The drone effectively "sees" the radio hole and modifies its landing trajectory or switches MCS/Modulation _before_ the dive to ensure the C2 link survives the descent.
        

## **3. Simulation Scenario Setup (Specific to this Use Case)**

To prove this works in your simulation, define the scenario as follows:

|Parameter|Value / Description|
|---|---|
|**Primary Event**|**"Geofence Injection"**: At T=50s, a virtual cylinder (radius=500m) appears, representing the helicopter/fire zone.|
|**Drone Action**|Must divert from Altitude 120m -> Landing Pad (Ground Level) in a dense urban canyon.|
|**The Challenge**|The direct path to the landing pad is blocked by a metal-glass building (high reflection/scattering).|
|**Baseline (Ray Tracing)**|Predicts "Weak but usable signal" (e.g., -95 dBm). Drone attempts landing -> **Link Fails** due to unmodeled multipath -> **Crash**.|
|**Your Method (FEM)**|Predicts "Destructive Interference Node" (e.g., -115 dBm). Drone detects this _proactively_, adds 2 seconds to flight time to approach from a different angle -> **Safe Landing**.|

## **Why Reviewers Will Love This**

1. **Relevance:** It addresses **"URLLC for Safety-Critical Applications"** (CFP Topic 8) and **"Scalable Air Traffic Management"** (CFP Topic 11).
    
2. **Urgency:** It solves a real operational problem (contingency management) identified by regulators (EASA/FAA) but often ignored by comms researchers.
    
3. **Justification for FEM:** You justify the heavy computational cost of FEM by arguing: _"We only need this extreme fidelity for the critical last 50 meters of an emergency landing, where failure is not an option."_
    

## **Refined Title Suggestion**

_"Reliable Contingency Management in Low-Altitude Airspace: A FEM-Based Predictive Link Adaptation Framework for Emergency UAV Landing"_

This title captures the **Scenario** (Emergency Landing), the **Method** (FEM-Based Prediction), and the **Goal** (Reliability/URLLC).

1. [https://ntrs.nasa.gov/api/citations/20190025711/downloads/20190025711.pdf](https://ntrs.nasa.gov/api/citations/20190025711/downloads/20190025711.pdf)
2. [https://arxiv.org/html/2506.12308v2](https://arxiv.org/html/2506.12308v2)
3. [https://clawar.org/wp-content/uploads/2021/02/Clawar2020_Paper_52.pdf](https://clawar.org/wp-content/uploads/2021/02/Clawar2020_Paper_52.pdf)
4. [http://www.caac.gov.cn/English/Research/Reports/Other/202305/P020230515402360797365.pdf](http://www.caac.gov.cn/English/Research/Reports/Other/202305/P020230515402360797365.pdf)
5. [https://ansperformance.eu/library/PRC_2024_02_Performance_dynamic_airspace_management.pdf](https://ansperformance.eu/library/PRC_2024_02_Performance_dynamic_airspace_management.pdf)
6. [https://www.sciencedirect.com/science/article/abs/pii/S0957417422008958](https://www.sciencedirect.com/science/article/abs/pii/S0957417422008958)
7. [https://www.euspa.europa.eu/sites/default/files/documents/Report%20on%20Aviation%20and%20Drones%20-%20User%20Needs%20and%20Requirements.pdf](https://www.euspa.europa.eu/sites/default/files/documents/Report%20on%20Aviation%20and%20Drones%20-%20User%20Needs%20and%20Requirements.pdf)
8. [https://scholarsmine.mst.edu/cgi/viewcontent.cgi?article=2221&context=comsci_facwork](https://scholarsmine.mst.edu/cgi/viewcontent.cgi?article=2221&context=comsci_facwork)
9. [https://arc.aiaa.org/doi/pdfplus/10.2514/6.2018-2142](https://arc.aiaa.org/doi/pdfplus/10.2514/6.2018-2142)
10. [https://www.autonomyglobal.co/international-drone-regulations-key-updates-on-bvlos-utm-and-use-cases-from-europe-canada-australia-and-africa/](https://www.autonomyglobal.co/international-drone-regulations-key-updates-on-bvlos-utm-and-use-cases-from-europe-canada-australia-and-africa/)


### IMPORTANT 
1. Because of that, the NR measurement framework will support height-dependent measurement report triggering (i.e. Events H1 and H2, to be specified in TS 38.331) which will help the network in identifying at what altitude the UAV currently https://www.3gpp.org/images/newsletters/3GPP_Highlights_Issue_6_opt.pdf

### Simulation Setup and Goals / what I do

General story of this paper
Motivation: In AAM, the UAVs in BVLOS operation need to handle constant change in the environment (urban, rural). This have significant impact on the signal quality. Which impact the throughput and latency of the channel to the ground station. Here particularly for the command and control link which carry critical ”telemetry messages” from the drone or
short control messages from the ground latency is hugely relevant. Thus, Ultra-Reliable Low-Latency Communication (URLLC) is the key. Example cases: Especially when an airspace is under planning to be closed due to helicopter landing, Emergency on the ground infrastructure like fire etc., and all the drones are expected to land in an unplanned location or divert, time is of the essence here. Such emergency landing and the ”impact of communication requirement” is often sidelined in envisioned autonomous operations. Some Specifications about URLLC: Unlike standard mobile broadband (eMBB), which prioritizes speed (throughput), URLLC prioritizes certainty. Deliver data with <1 ms latency and >99.999% reliability. The Challenge: Wireless channels are inherently unstable due to noise, interference, and reflection. URLLC must mathematically guarantee delivery despite these physical distortions.
2 Signal Strength: Is not just about ”bars” on a phone; in URLLC, it is about maintaining a massive ”Fade Margin” so that even when the signal dips, it never drops below the decoding threshold. Signal strength in URLLC is analyzed via the Signal-to-Interference-plus-Noise Ratio (SINR). SINR is
based on RSSI and RSRP
Physical Distortion: Includes Multipath Fading (echoes confusing the receiver), Delay Spread and Doppler Shift (movement distorting frequency). Current State of Art for URLLC in LAWN:
• Achieving URLLC (Ultra-Reliable Low-Latency Communication) in this domain is significantly harder than on the ground because terrestrial networks are optimized for users walking on streets, not flying above them.
• Sky Paradox: In the LAWN domain, drones suffer from a unique problem: Too much connectivity, yet poor quality. This causes severe uplink interference. The drone’s radio shouts to one tower, but 20 other towers hear it as noise. Conversely, the drone hears 20 towers shouting, raising
the noise floor and degrading the Signal-to-Interference- plus-Noise Ratio (SINR).
• 3GPP High dependent signal quality - Aerial Slice , a service application of URLLC [SS: I am currently reading into it]
• RIS
• path predictive multi-link connectivity - In a pre- determined path when a ”shadow or black spot are” is expected to approach , switch from 5G to satcom link.

Our Contribution: Implementation Near-field simulator for FEM - EM scattering that can be moved to far-field parameters  by far-field transformers with - Antenna gain , reflector provides details that can help ray tracing to get RSSI and RSRP. These values help to build SINR - provide general idea about the signal quality. this will help to estimate Throughput , Latency margin based on Coding scheme and we ensure reliability (low latency) with limiting retransmissions and large
packets. Therefore, we focus on the Physical and logical characteristics of the communication channel to ensure reliability.
[SS: Questions to Roshan: Do we include results of RIS modeling ?] 
This structure covers the topics of the special issue: URLLC for Safety-Critical Applications in LAWN, combining cross-layer design principles with advanced technologies. Storyline and results [SS: I think the radio map is not done real-time. The radio map can/will be used for trajectory planning ?]
The height-dependent RSSI/SINR distributions using FEM that capture urban material properties and meta-physics based approach (concrete, metal, glass) with higher fidelity than statistical models or circuit modeling like ray tracing. Thus,
the path planned based on the communication 5G based
availability can be more accurate radio environment map.
The ”proactive link adaptation” can happen before entering
weak/none zone.
Scenario 1: FEM is computationally heavy. Therefore, the
FEM based radio environment map is pre-computed (offline)
and stored as a ”Digital Twin” map. The drone only does a
simple lookup (O(1) complexity) in real-time. This proves it
is feasible for low-latency operations.
Scenario 2: Real-world operations (U-Space/UTM) will face
”Dynamic Airspace Closures” (e.g., a helicopter needs to
land, or a fire starts). This forces drones to divert instantly
to low-altitude, unplanned ”contingency landing spots.” These
unplanned spots are often in ”dead zones” (between buildings,
near ground clutter) where standard ray-tracing models fail to
predict deep fades accurately. A loss of C2 link here = a crash
or a rogue drone.
Novelty:
• The FEM model becomes the Digital Twin of the Radio
Environment.[SS: from perplexity AI-Does this make
sense]. FEM can model complex ground reflections and
building material properties (concrete, glass) more ac-
curately (high-precision) than statistical models for low-
altitude (<100m) urban canyons. Pictures the EM mate-
rial interaction (scattering, diffraction effects better than
statistical model.
• Pipeline for Physics based signal quality to logical based
packet metrics. Evaluate to meet the Benchmark (3GPP)
LAWN URLLC [SS: Need to look into this based on
results] - cross layer optimization with SINR,etc..
• Validate the result against ray tracing , statistical model
setup


- Tabs and papers to read 


---
12/1

FEEP output to sionna can improve radio map 
model with RIS - uses FEM 
Sionna with RIS - doesn't take depth of Physics

Focus: adding a novelty of RIS to network and what it affects URLLC


Sionna PHY
Sample simulation - ray tracing 
SNR and RSSI 

Urban environment 

Shreeja: Link level simulator - Sionna | Python| Vienna 5G

Show based on use-case 

https://www.5gtechnologyworld.com/bler-a-critical-parameter-in-cellular-receiver-performance/

KPIs 
parameters


https://vtsociety.org/post/announcement/special-issues-ieee-vt-magazine

---

- [ ] LAWN paper 
	- [ ] To do plan and idea
	- [ ] Read 3GPP 38811, 38901, UAV as UE 3GPP and Base station 
	- [ ] Background
	- [ ] Simulation and to dos 
	- [ ] Start writing 


---

### Big picture

