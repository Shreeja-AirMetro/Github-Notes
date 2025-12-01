
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

### # Pathloss Analysis and Modelling for 5G Communication in U-SPACE


//Misc Papers

### URLLC Multi-link/connectivity 

Reliability and Delay Analysis of 3-Dimensional Networks With Multi-Connectivity: Satellite, HAPs, and Cellular Communications  https://ieeexplore.ieee.org/abstract/document/10227357 
Aerial vehicles (AVs) such as electric vertical take-off and landing (eVTOL) aircraft make aerial passenger transportation a reality in urban environments. However, their communication connectivity is still under research to realize their safe and full-scale operation. This paper envisages a multi-connectivity (MC) enabled aerial network to provide ubiquitous and reliable service to AVs. Vertical heterogeneous networks with direct air-to-ground (DA2G) and air-to-air (A2A) communication, high altitude platforms (HAPs), and low Earth orbit (LEO) satellites are considered. We evaluate the end-to-end (E2E) multi-hop reliability and network availability of the downlink of AVs for remote piloting scenarios, and control/telemetry traffic. Command and control (C2) connectivity service requires ultra-reliable and low-latency communication (URLLC), therefore we analyze E2E reliability and latency under the finite blocklength (FBL) regime. We explore how different MC options satisfy the demanding E2E connectivity requirements taking into account antenna radiation patterns and unreliable backhaul links. Since providing seamless connectivity to AVs is very challenging due to the line-of-sight (LoS) interference and reduced gains of downtilt ground base station (BS) antennas, we use coordinated multi-point (CoMP) among ground BSs to alleviate the inter-cell interference. Furthermore, we solve an optimization problem to select the best MC path under the quality of service (QoS) constraints. We maximize spectral efficiency (SE) to specify the optimum MC path with the minimum number of required links. Based on the simulation results, we find out that even with very efficient interference mitigation, MC is the key enabler for safe remote piloting operations.

