> [!summary] Summary
> Links, ideas, thoughts and meeting take-aways from the year-named task files: 2025 moved here, 2026/2027 copied verbatim with line numbers.
>
> **Target / goal:** One place to search for ideas and links without digging through monthly todos.

# Ideas, Links & Thoughts

> One place for the extra info (links, ideas, thoughts, meeting take-aways) that sat inside the year-named task files.
> - **2025**: moved here; the 2025 tasks themselves are in [[2025 Todos]].
> - **2026 / 2027**: copied here verbatim with line numbers; the original monthly files were not changed.

## 2025

> Moved here from the 2025 task files (now merged into [[2025 Todos]]).

### Learning and reading links (Nov 2025)

Weekends: Work on this https://www.cisco.com/c/en/us/tech/index.html and https://www.sharetechnote.com/Home.html 
on Networking protocol 
5G , LTE and WiFi 

Read: 
https://www.dlr.de/en/kn/about-us/departments/communications-systems/aeronautical-communications-group
https://www.ldacs.com/ 

**test at difference scenarios and results** 

### PhD thoughts and AAM low-altitude challenges (Nov 2025)

### PhD Thoughts 
The PhD research network coding and computation is mandatory for Aerial communication. How the communication and computing via coding part will exists ? 

Explain the communication requirements 
Go to the coding part - Network coding and the crucks and nooks in multi-link communication 

3 big pillars of writing dissertation 
- UAV side of communication 
- GCS and ground infrastructure 
- New network architecture like NTN and particular to this use-case 


Key challenges: In **Advanced Air Mobility (AAM)** — especially low-altitude operations (0–120 m AGL) — drones (UAVs/UAS) must rely on robust, low-latency, and safe communication links for:
- Command and Control (C2/C3)
- Detect and Avoid (DAA)
- Navigation and cooperative behavior
- Integration with U-space / UTM (Unmanned Traffic Management) system

Challenges emerge because this **low-altitude environment** is complex:

- High interference from buildings and ground clutter
- Variable LOS/NLOS conditions
- Limited cellular coverage at 120 m (not optimized for aerial users)
- Spectrum sharing and regulatory issues
- Multi-operator coordination in AAM corridors 

**Big mistake is to assume:  redundancy equals reliability**
  
Latency is going to be your biggest problem for real time flight adjustments.
DTU (Technical University of Denmark) executed extensive 3D measurement campaigns at HCA Airport.  - https://genius.aero/index.php/work-package-1/ 

- NetworkX python package 

### Literature review workflow (Nov 2025)

### Literature review workflow
	- Find literature , filter and read main
	- Reference manager - Mendeley - Litmaps - connected papers - concenses /scispace for filtering 
	- Notebook LM for research concept and gaps - also concenses
	- Get a structure - suggested structure - scispace
	- content 
**==read from back for review==**

### Backups (Nov 2025)

### Misc
- We have 3 backup online
	-  Obsidian notes - regular backup Github and Gitlab 
	- Official backups Monthly on Gitlab- comnets

### RTG review takeaways and contacts (Nov 2025)

---
Takeaway from RTG review 
- More women 
- Post-Doc 
-  elect care person /  diversity manager 
- 4 year contract for second cohort 
----

 Jacob - Prague university UTM , infrastructure AAM - small workshop 

### To learn (Nov 2025)

### To learn 
- Wireless communications theory (link budgets, fading, Doppler, MIMO, beamforming).
- Cellular stack familiarity (4G/5G NR concepts, 3GPP specs affecting UAVs; how to read TRs/TSs)
- RF & antenna basics (antenna patterns at altitude, ground interaction).
- basic ML for signal/telemetry analytics.
- Cloud & edge computing (k8s, edge orchestration, low-latency MEC patterns).
- Satellite comms basics (LEO constellations, link budgets, latency constraints). [MDPI](https://www.mdpi.com/2078-2489/15/1/38?utm_source=chatgpt.com)
- Security & authentication for UAV links (secure Remote ID, secure boot/firmware). [Drone as a Service](https://www.droneasaservice.com/blog/faa-remote-id-rule-for-drones/?utm_source=chatgpt.com)
- Certification & regulatory knowledge: SORA, EASA U-Space, FAA BVLOS/Remote ID ecosystems.

### Running notes: deterministic multi-connectivity (Dec 2025)

### Running notes 

Describe the presentation of the project as lego of problems for comm in AAM and how you perform/ solve few of them 
Highlight few you talk about (dissertation)

The state of the art for LAWN URLLC is **Deterministic Multi-Connectivity**. We no longer rely on "hoping" the signal is strong enough. We guarantee it by **mathematically modeling the flight path**, using **AI to predict fades**, and **bonding multiple networks** (Cellular + Satellite) to ensure that even if physics distorts one signal, the data still gets through.

Network Architecture: "Bonding" & Redundancy**

For BVLOS, a single link is no longer considered "Ultra-Reliable." The industry standard has shifted to **Packet Duplication** (PDCP Duplication).

- **Multi-Link Bonding:** Systems like _Elsight Halo_ or _Honeywell_ now split the C2 (Command & Control) data packet into pieces (or duplicate it entirely) and send it simultaneously over **4G, 5G, and Satellite (LEO)**.[commercialuavnews](https://www.commercialuavnews.com/solving-the-redundancy-puzzle-for-bvlos-uavs)​
- ==**The Result:** If the 5G tower fades due to a physical dip, the packet arrives via 4G or Satellite. This creates a "virtual" reliability of 99.9999% even if individual links are only 90% reliable.==

idea:
Network coding based on technology for C2 communication and compary their latency and performance characterisctisc
Energy requirements 

### Stray idea (Dec 2025)

multitency in cloud

### Challenges and novelty in multi-link network coding (Dec 2025)

## **Challenges and Novelty for a Researcher in Multi-Link Drone Networks**

As a PhD researcher at TU Delft, moving beyond the "textbook" definition of Network Coding (NC) is critical. You are dealing with a highly dynamic, resource-constrained system (the drone) communicating over heterogeneous links (Satellite, 5G, WiFi). Below is a breakdown of the open challenges and specific "novelty" angles you can exploit for your thesis or publications.

---

## **1. Key Research Challenges (The "Pain Points")**

These are the problems that are currently difficult to solve and prevent widespread adoption of NC in drones.

## **A. The "Estimation-Adaptation" Loop**

- **Challenge:** NC works best when you know exactly how many "repair packets" to send. If the erasure probability is 10%, sending 15% redundancy is optimal. If you send 50%, you waste expensive Satcom data. If you send 5%, the decoding fails.
    
- **The Problem:** In a drone, the link quality changes in milliseconds (due to banking, shadowing by buildings, or handover). Estimating the erasure rate $\epsilon$ accurately in real-time on a high-latency link (Satcom) is notoriously difficult. Old channel state information (CSI) leads to wrong coding rates.
    

## **B. Computational Overhead vs. Latency**

- **Challenge:** You want "Ultra-Reliable Low-Latency Communication" (URLLC).
    
- **The Conflict:** To lower the overhead of NC, you usually group many packets into a large "Generation Size" (e.g., 50 packets). But waiting to collect 50 packets adds massive latency (jitter). If you reduce the generation size to 5 packets for low latency, the coding efficiency drops, and the CPU overhead per byte skyrockets. Finding the "Sweet Spot" dynamically is an open control theory problem.
    

## **C. Protocol Ossification (Middleboxes)**

- **Challenge:** Network Coding packets often look like "garbage" UDP payload to standard deep-packet inspection (DPI) firewalls or 5G NATs. They might be dropped.
    
- **The Gap:** Designing a header format or encapsulation (e.g., inside QUIC or GRE) that is transparent to 5G/Satcom modems but readable by your decoder is a practical engineering hurdle.
    

## **D. The "Straggler" Problem in Multi-Link**

- **Challenge:** You send Coded Packet A via 5G (latency 20ms) and Coded Packet B via Satcom (latency 600ms). The decoder has to wait for B to decode A.
    
- **The Issue:** A naive NC scheduler might actually _increase_ latency by forcing the fast link to wait for the slow link. Designing a scheduler that uses the slow link _only_ for recovering otherwise-lost packets (without blocking the stream) is complex.
    

---

## **2. Novelty & Research Directions (Your "PhD Contribution")**

These are specific areas where you can claim "Novelty" in a paper.

## **Novelty 1: Age of Information (AoI) Aware Network Coding**

- **Concept:** Traditional NC optimizes for _Throughput_ (getting all data across). But for drone telemetry, old data is useless. You care about "Freshness" (AoI).
    
- **Research Idea:** Develop a coding scheme that **prioritizes newer generations**. If a new telemetry packet arrives, the NC engine should _drop_ the unfinished old generation and start coding the new one immediately.
    
- **Contribution:** "A Novel Preemptive Network Coding Scheme for Minimizing AoI in UAV C2 Links."
    

## **Novelty 2: "Forecasting-Based" coding with AI/ML**

- **Concept:** Instead of reacting to packet loss, _predict_ it.
    
- **Research Idea:** Use an onboard sequence model (like an LSTM or Transformer) that inputs the drone's flight plan and 3D map.
    
    - _Scenario:_ "The drone is about to fly behind a cathedral. 5G LOS will be lost in 2 seconds."
        
    - _Action:_ The NC engine preemptively ramps up redundancy on the Satcom link _before_ the packet loss occurs.
        
- **Contribution:** "Proactive Multi-Link Network Coding for UAVs using Geospatial Channel Prediction."
    

## **Novelty 3: Joint Source-Network Coding (JSNC)**

- **Concept:** Don't treat all data the same.
    
- **Research Idea:** Integrate the NC layer with the Video Encoder (H.265/AV1).
    
    - Protect "I-Frames" (critical) with high redundancy (Satcom + 5G).
        
    - Protect "P-Frames" (less critical) with low redundancy (5G only).
        
- **Contribution:** "Content-Aware Unequal Error Protection (UEP) using Network Coding for Drone Video Surveillance."
    

## **Novelty 4: Compute-Efficient "Sparse" Codes**

- **Concept:** RLNC involves dense matrix multiplication ($O(N^3)$), which burns battery on a Raspberry Pi.
    
- **Research Idea:** Use **Sparse** codes (like BATched Sparse codes or TNC) where the coding matrix is mostly zeros. This drastically reduces CPU usage while maintaining similar recoverability.
    
- **Contribution:** "Energy-Efficient Sparse Network Coding Implementation for Embedded UAV Controllers."
    

## **Novelty 5: Security against "Pollution Attacks" in Swarms**

- **Concept:** If one drone in a swarm is hijacked and injects a "fake" coded packet, it corrupts the decoding of _everyone_ in the swarm.
    
- **Research Idea:** Design a lightweight "Homomorphic Signature" scheme that allows drones to verify the validity of a coded packet without decoding it first.
    
- **Contribution:** "Lightweight Byzantine-Resistant Network Coding for Secure UAV Swarm Coordination."
    

## **Summary of Positioning**

- **Don't just do:** "I implemented NC on a drone." (This is engineering).
    
- **Do this:** "I proposed an **adaptive** NC algorithm that uses **flight trajectory prediction** to minimize **Age of Information** over heterogeneous links." (This is Research).
    

1. [https://www.cse.wustl.edu/~jain/papers/ftp/uav_comst.pdf](https://www.cse.wustl.edu/~jain/papers/ftp/uav_comst.pdf)
2. [https://pmc.ncbi.nlm.nih.gov/articles/PMC11765453/](https://pmc.ncbi.nlm.nih.gov/articles/PMC11765453/)
3. [https://arxiv.org/pdf/2301.05835.pdf](https://arxiv.org/pdf/2301.05835.pdf)
4. [https://pdfs.semanticscholar.org/cae8/5b04456d6fd9d669744a72004b0f64944cd9.pdf](https://pdfs.semanticscholar.org/cae8/5b04456d6fd9d669744a72004b0f64944cd9.pdf)
5. [https://pmc.ncbi.nlm.nih.gov/articles/PMC9862947/](https://pmc.ncbi.nlm.nih.gov/articles/PMC9862947/)
6. [https://tdmujournal.vn/uploads/paper/files/05-Luu-Thi-Hiep.pdf](https://tdmujournal.vn/uploads/paper/files/05-Luu-Thi-Hiep.pdf)
7. [https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.1293.pdf](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.1293.pdf)
8. [https://aaltodoc.aalto.fi/server/api/core/bitstreams/db31e346-9da0-4d6b-bd21-8af084e6beca/content](https://aaltodoc.aalto.fi/server/api/core/bitstreams/db31e346-9da0-4d6b-bd21-8af084e6beca/content)
9. [https://arxiv.org/abs/2312.15778](https://arxiv.org/abs/2312.15778)
10. [https://onlinelibrary.wiley.com/doi/10.1155/2022/7726338](https://onlinelibrary.wiley.com/doi/10.1155/2022/7726338)

### Proposal impact-section checklist (Aug 2025, Dronnect proposal)

---
Impact section 
1. What all should be in project pathway
	- Direct results 
	- benifit the target group by D, C actions 
	- Shrot long term are imapct and outcomes 
	- Proejet centered  around whom? 
	- Direct and indirect results 
	- 
2. EI
3. EO
4. Scale scignificance
5. potential barrier
Summary table 
what are specific needs that triggered this project 
expected results 
what are the dissmenication, Explotatin resulst apply to this resuzlts
Who will use or further up-take the results of the project? Who will benefit from the results of the project?
What change do you expect to see after successful dissemination and exploitation of project results to the target group(s)?
Expected wider scientific, economic and societal effects of the project contributing to the expected impacts in the destination?
_who_ benefits, _what_ changes, and _by when_.

## 2026 (copied, originals unchanged in `07 TODOS/2026/`)

### From [[Jan 2026]]

#### Why BVLOS communication is under-represented (thoughts + sources) (lines 2-97)

### General Thoughts 
Communication technology for BVLOS is absolutely central, but it is structurally under‑represented and often treated as an enabling “black box” rather than a first‑class research axis. You are not missing something; the ecosystem is genuinely skewed, and that bias is dangerous for scalable autonomy.[unmannedsystemstechnology+1](https://www.unmannedsystemstechnology.com/expo/bvlos-communications/)​

## Where the current focus really is

Most BVLOS work and messaging cluster into two visible buckets.[jouav+1](https://www.jouav.com/blog/bvlos-drone.html)​

- **Operations/UTM/Concept of Operations**: U-space/UTM architectures, ADSP/USSP ecosystems, strategic deconfliction, and regulatory rulemaking (FAA BVLOS NPRM, EASA U-space, etc.) are framed as digital services and procedures, not radio systems.[faa+1](https://www.faa.gov/air_traffic/publications/atpubs/aim_html/chap11_section_4.html)​
    
- Onboard autonomy stack: perception, SLAM, LiDAR, cooperative/non‑cooperative DAA, and local trajectory planning dominate academic venues and robotics conferences because they fit well with established AI/robotics evaluation cultures.[mosaic-lab+1](http://www.mosaic-lab.org/uploads/papers/f278553f-4770-4b6a-877a-d3dae8c9437e.pdf)​
    

Communication is mentioned as a requirement (C2 link, “secure & reliable connectivity”) but rarely decomposed into a research problem beyond link availability.[zenatech+1](https://www.zenatech.com/bvlos-drone/)​

## Why comms is structurally “invisible”

Several systemic reasons push communication to the background.[orbit.dtu+1](https://backend.orbit.dtu.dk/ws/files/293927450/Overview_of_Drone_Communication_Requirements_in_5G.pdf)​

- Regulatory framing: BVLOS rules specify high‑level “reliable C2 link” obligations (availability, continuity, integrity) but remain technology‑agnostic; interfaces and performance figures are left to standards/industry, which shifts detailed work out of mainstream drone research.[aam-cms.marqui+1](https://aam-cms.marqui.tech/uploads/aam-portal-cms/originals/b67a0dfb-e95e-48f6-83dd-5d483a9db463.pdf)​
    
- Standards siloing: 3GPP, ETSI, ITU, etc., treat UAS as verticals of 4G/5G/6G (e.g., “UAV UE profiles,” NTN support), so work is reported as “5G feature evolution,” not as “drone communication research,” making it less visible to UAM/UTM communities.[sciencedirect+1](https://www.sciencedirect.com/science/article/pii/S1570870524000519)​
    
- Infrastructure assumption: Many BVLOS guides simply assume “4G/5G or SATCOM for C2,” as if these links were commoditized and uniform, which hides issues like mobility, interference, cell‑selection anomalies, and cross‑border handover.[jouav+1](https://www.jouav.com/blog/bvlos-drone.html)​
    
- Industry black‑box products: vendors push turnkey multilink bonding boxes (LTE/5G + SATCOM + RF) and market reliability as solved (“one securely bonded pipe”), which discourages open, critical examination of architectures, algorithms, and failure modes.[elsight+2](https://www.elsight.com/blog/dods-5g-strategy-hybrid-networks-are-the-future-of-military-drone-connectivity/)​
    
- Publication venue mismatch: Network‑centric work on UAV‑assisted cellular, B5G/6G NTNs, and multi‑connectivity often treats UAVs as “aerial UEs” or “aerial base stations,” not as safety‑critical vehicles; it optimizes rate/coverage rather than aviation‑grade dependability, so it does not speak the same language as UTM research.[arxiv+2](https://arxiv.org/pdf/2212.13329.pdf)​
    

The result is a fragmentation where each community implicitly assumes “someone else” is making connectivity robust and certifiable.

## Critical gap: from “link works” to “system is safe”

Current communications work rarely hits the aviation‑safety bar.[unmannedsystemstechnology+1](https://www.unmannedsystemstechnology.com/expo/bvlos-communications/)​

- Reliability is often expressed as average throughput or outage probability, not as end‑to‑end risk over mission profiles with explicit safety targets and hazard analysis for C2 loss.[mecs-press+1](https://www.mecs-press.org/ijwmt/ijwmt-v12-n4/IJWMT-V12-N4-3.pdf)​
    
- Multi‑link connectivity (4G/5G + SATCOM + RF) is promoted, but the actual decision logic, failover timing, and synchronization with flight management and UTM services are proprietary and under‑specified.[groundcontrol+1](https://www.groundcontrol.com/blog/enabling-bvlos-drone-operations-anywhere-on-earth/)​
    
- UTM/ADSP concepts assume continuous data exchange for intent sharing, conformance monitoring, and contingency management, yet the communication model is often a perfect or near‑perfect network; graceful degradation strategies under partial loss are weakly defined.[unmannedairspace+2](https://www.unmannedairspace.info/uncategorized/us-announces-much-anticipated-new-rule-to-normalise-commercial-bvlos-operations/)​
    
- Integration with autonomy is shallow: trajectory planners rarely internalize connectivity constraints (coverage, latency, handover risk) as first‑class costs, although industrial projects like ADACORSA start to demonstrate multi‑link and secure comms as a capability.[nlr+1](https://www.nlr.org/newsroom/video/adacorsa-demonstration-capabilities-for-drones/)​
    

So the field ossifies around a “perception‑heavy, comms‑naïve” autonomy stack running over a “UTM‑heavy, network‑agnostic” architecture.

## Where your perspective is actually ahead

Several emerging lines confirm that your intuition (multi‑link, edge, safety‑critical comms) is where the serious gaps are.[nlr+1](https://www.nlr.org/newsroom/video/adacorsa-demonstration-capabilities-for-drones/)​

- Survey and requirement papers explicitly call out that satellite and 5G are “viable” for drone C2, but note open problems in mobility, coverage holes, interference, and QoS guarantees tailored to UAV flight envelopes.[orbit.dtu+1](https://backend.orbit.dtu.dk/ws/files/293927450/Overview_of_Drone_Communication_Requirements_in_5G.pdf)​
    
- 5G/6G‑UAV surveys increasingly discuss unified sensing‑communication‑computation for UAVs, but translation into certifiable architectures for BVLOS logistics is missing.[mosaic-lab+1](http://www.mosaic-lab.org/uploads/papers/f278553f-4770-4b6a-877a-d3dae8c9437e.pdf)​
    
- EU projects such as ADACORSA explicitly list “multi-links for robust communication in WiFi, LTE/5G and SATcom” and “technologies for secure and reliable drone communication” as key demonstrators, indicating that current connectivity is not yet adequate.[nlr](https://www.nlr.org/newsroom/video/adacorsa-demonstration-capabilities-for-drones/)​
    

In other words, communication technology is present but mostly as industrial R&D and standards evolution, not as a coherent academic subsystem of “autonomous BVLOS operations.”

## How to be (deliberately) critical in your own work

Given your profile, there is a strong opening to treat communication as a safety‑critical, co‑equal pillar of BVLOS autonomy rather than plumbing.[orbit.dtu+1](https://backend.orbit.dtu.dk/ws/files/293927450/Overview_of_Drone_Communication_Requirements_in_5G.pdf)​

- Explicitly frame comms as part of the safety case: map link properties, multi‑path strategies, and edge offloading decisions directly into hazard analyses and assurance arguments, instead of performance metrics alone.[easa.europa+1](https://www.easa.europa.eu/sites/default/files/dfu/Easy_Access_Rules_for_U-space_-_May_2024__Word_.pdf)​
    
- Challenge black‑box resilience claims: expose multilink/aggregation schemes to realistic failure scenarios (coverage gaps, regulatory power limits, cross‑border roaming, link sabotage) and show where current “hybrid connectivity” falls short for harbor‑to‑urban logistics corridors.[elsight+1](https://www.elsight.com/blog/dods-5g-strategy-hybrid-networks-are-the-future-of-military-drone-connectivity/)​
    
- Force autonomy and planning to internalize connectivity: design planners and UTM interaction protocols where connectivity state and risk are explicit variables, not afterthoughts, and quantify operational capacity loss under degraded networks.[acm+1](https://dl.acm.org/doi/10.1145/3617992)​
    

So the honest answer is: the communication domain is genuinely under‑articulated at the BVLOS/autonomy interface, and that is a systemic blind spot rather than a gap in your understanding.

1. [https://www.unmannedsystemstechnology.com/expo/bvlos-communications/](https://www.unmannedsystemstechnology.com/expo/bvlos-communications/)
2. [https://backend.orbit.dtu.dk/ws/files/293927450/Overview_of_Drone_Communication_Requirements_in_5G.pdf](https://backend.orbit.dtu.dk/ws/files/293927450/Overview_of_Drone_Communication_Requirements_in_5G.pdf)
3. [https://www.jouav.com/blog/bvlos-drone.html](https://www.jouav.com/blog/bvlos-drone.html)
4. [https://dl.acm.org/doi/10.1145/3617992](https://dl.acm.org/doi/10.1145/3617992)
5. [https://www.faa.gov/air_traffic/publications/atpubs/aim_html/chap11_section_4.html](https://www.faa.gov/air_traffic/publications/atpubs/aim_html/chap11_section_4.html)
6. [https://aam-cms.marqui.tech/uploads/aam-portal-cms/originals/b67a0dfb-e95e-48f6-83dd-5d483a9db463.pdf](https://aam-cms.marqui.tech/uploads/aam-portal-cms/originals/b67a0dfb-e95e-48f6-83dd-5d483a9db463.pdf)
7. [http://www.mosaic-lab.org/uploads/papers/f278553f-4770-4b6a-877a-d3dae8c9437e.pdf](http://www.mosaic-lab.org/uploads/papers/f278553f-4770-4b6a-877a-d3dae8c9437e.pdf)
8. [https://www.nlr.org/newsroom/video/adacorsa-demonstration-capabilities-for-drones/](https://www.nlr.org/newsroom/video/adacorsa-demonstration-capabilities-for-drones/)
9. [https://www.zenatech.com/bvlos-drone/](https://www.zenatech.com/bvlos-drone/)
10. [https://www.easa.europa.eu/sites/default/files/dfu/Easy_Access_Rules_for_U-space_-_May_2024__Word_.pdf](https://www.easa.europa.eu/sites/default/files/dfu/Easy_Access_Rules_for_U-space_-_May_2024__Word_.pdf)
11. [https://www.sciencedirect.com/science/article/pii/S1570870524000519](https://www.sciencedirect.com/science/article/pii/S1570870524000519)
12. [https://arxiv.org/pdf/2212.13329.pdf](https://arxiv.org/pdf/2212.13329.pdf)
13. [https://www.elsight.com/blog/dods-5g-strategy-hybrid-networks-are-the-future-of-military-drone-connectivity/](https://www.elsight.com/blog/dods-5g-strategy-hybrid-networks-are-the-future-of-military-drone-connectivity/)
14. [https://www.defenseadvancement.com/news/bvlos-communications-technology-for-mission-critical-drones-robotics/](https://www.defenseadvancement.com/news/bvlos-communications-technology-for-mission-critical-drones-robotics/)
15. [https://www.groundcontrol.com/blog/enabling-bvlos-drone-operations-anywhere-on-earth/](https://www.groundcontrol.com/blog/enabling-bvlos-drone-operations-anywhere-on-earth/)
16. [https://www.mecs-press.org/ijwmt/ijwmt-v12-n4/IJWMT-V12-N4-3.pdf](https://www.mecs-press.org/ijwmt/ijwmt-v12-n4/IJWMT-V12-N4-3.pdf)
17. [https://www.unmannedairspace.info/uncategorized/us-announces-much-anticipated-new-rule-to-normalise-commercial-bvlos-operations/](https://www.unmannedairspace.info/uncategorized/us-announces-much-anticipated-new-rule-to-normalise-commercial-bvlos-operations/)
18. [https://www.unmannedsystemstechnology.com/expo/beyond-visual-line-of-sight/](https://www.unmannedsystemstechnology.com/expo/beyond-visual-line-of-sight/)
19. [https://www.flytbase.com/blog/bvlos-drone-operations](https://www.flytbase.com/blog/bvlos-drone-operations)
20. [https://www.federalregister.gov/documents/2025/08/07/2025-14992/normalizing-unmanned-aircraft-systems-beyond-visual-line-of-sight-operations](https://www.federalregister.gov/documents/2025/08/07/2025-14992/normalizing-unmanned-aircraft-systems-beyond-visual-line-of-sight-operations)



https://www.strategicmarketresearch.com/market-report/drone-data-link-system-market?utm_source=chatgpt.com

#### Misc: metrics vs KPIs vs key results (lines 99-105)

GNU  (Linux) and keen to gain hands-on experience in Networks and systems

Metrics - standard or system of measurements 
Metrics used in KPIs and key results 

KPIs - defining key area  - metric, current value and target value 
key results - belong to objective - clarify and quantify and measure progress  - metric current value start value target value and title

#### Paper/journal writing tips (lines 108-118)

Paper Journals 

- Where is disconnect 
- avoid confusing writing 
- Start with single clear topic sentence
- evidence 
- explain 
- Repeat 
- write like a cook book - enable reconstruction 
- methods and results linear 
- simplify 

#### Topics to look into (lines 172-176)

topics to look into 
1. CCNA and Network basics
2. Independent component Analysis - ICA
3. Paths for  Network Traffic Engineering
4.  BGP is difficult to master. Every year, the most confusing topic is the interaction between the control-plane messages (BGP advertisements) and the data plane. Most students have a hard time to realize that they have to e.g., adapt the outgoing BGP messages in order to influence the incoming traffic. They often wrongly believe route-maps are applied on each IP packet traversing the router. In addition, some students are confused with the language used to configure the routers as it does not follow modern programming language principles. As a result, we improved lecture slides and documentation and put more effort into showing the students the impact of their configuration using e.g., the measurement platform. Overall, we hope these insights help the students in the future to eliminate shortcoming of existing solutions should they have to develop new protocols or ways to configure network devices. Configure BGP policies. This is often the most complicated part. We first ask the students to configure the local-preferences as well as the exportation rules to implement the customer/provider and peer-to-peer business relationships with their neighbors [7]. Then, we ask them to implement more advanced policies to influence the inbound or outbound traffic. During this process the students learn about the different BGP attributes (e.g., AS path, MED) and how to use them in order to influence the forwarding behavior. For instance, we often ask them to configure BGP such that the inbound traffic coming from the provider with whom they have two external BGP sessions (see Fig. 1b) arrives preferably via one of the routers.

#### Syed call: EU-African Union proposal idea (lines 283-308)

21/1 Syed call EU African union call 
call deadline :  1st week 
pre-proposal 
EV market not great 
Assests and grid maintainance 
utility partners - test sites - tranformer side 
Field data 
sensors  - low power 
Protocols 
UAV - swarm 
drone with smart grids - information of powerlines - EMF charge - Startup from Munich 
TRL 1-3 - proof of concept 

- Follow- up call with Syed on Proposal  - 26/1 

Eva boo - Social  innovation project  - Contact wioth African partner 
Annette Hubschle  - Cape Town and   Namibia 
university of western cape 
Partner  - Cape verde 
STOP and review with vision and mission statement 
breakdowns on the idea 
cannot install a lot of sensors - we are doing with sparcity of data 
Technical solutions to be linked 

Freeze things when write a proposal 

### From [[Feb 2026]]

#### Thoughts + BVLOS C2/C3 research landscape (lines 1-92)

- Conceptual clarity 
- . Defaults quietly become standards and then get retroactively treated as principled choices in papers.
- PhD pitch slides - https://www.youtube.com/watch?v=0NmZg_rclP8
-  SET MINI GOALS
- https://associationfordrones.com/ - LOOK INTO THIS
-  litte cause of optimisum - its optimisum but error corrected - sabine hossenfelder 
- hysterisis factor 
- Reticulum - Fine network or netlike structure - READ

---

- The research landscape for drone communication (C2 and C3) has exploded in the last decade, transitioning from basic hobbyist links to safety-critical aerospace standards.

---

### 1. Literature Scale & Volume

The research volume is massive. On **IEEE Xplore**, a search for "UAV Communication" yields over **15,000 results**, with roughly **3,000+ specifically focused on BVLOS (Beyond Visual Line of Sight)**.

- **Annual Growth:** The field sees approximately **1,500–2,000 new papers per year**, driven by the integration of drones into the 3GPP (cellular) standards and the rise of Urban Air Mobility (UAM).
    
- **Focus Shift:** Pre-2015 research was mostly on point-to-point RF links. Post-2018 research has shifted almost entirely to **Cellular-Connected UAVs** and **Satellite integration**.
    

### 2. Common Technologies for C2 & C3

Researchers distinguish between **C2 (Command and Control)**—the low-bandwidth, high-reliability link to fly the drone—and **C3 (C2 + Communications/Data)**—which includes the heavy payload data like 4K video.

- **Cellular (4G LTE / 5G):** The dominant research domain. 5G **Ultra-Reliable Low-Latency Communication (URLLC)** is the "gold standard" for C2.
    
- **Satcom (LEO):** High interest in Starlink/OneWeb for "Gap Filling" where cellular coverage fails in remote BVLOS areas.
    
- **SDR (Software Defined Radio):** Used to create custom, frequency-agile waveforms that can dodge interference.
    
- **Wi-Fi HaLow (802.11ah):** Emerging for long-range, low-power telemetry (C2) at sub-1GHz frequencies.
    

### 3. Key Problems in BVLOS Communication

Research identifies four "Critical Walls" that prevent seamless BVLOS scaling:

1. **The "Aerial Interference" Problem:** Drones at 100m altitude see too many base stations, causing massive interference that ground users don't face.
    
2. **Handover Instability:** High-speed drones cross "cells" so fast that traditional handover logic fails, leading to lost C2 links.
    
3. **3D Channel Modeling:** Most ground signals move in 2D. Drones face complex "air-to-ground" reflections and Doppler shifts that break standard signals.
    
4. **Security (C2 Hijacking):** The risk of GPS spoofing or C2 jamming is a major research area for BVLOS safety certification.
    

---

### 4. Major Research Domains (The Solutions)

Academic work is currently obsessed with these four "enablers":

|**Domain**|**How it solves BVLOS**|
|---|---|
|**RIS (Reconfigurable Intelligent Surfaces)**|Uses "smart mirrors" on buildings to reflect 5G/6G signals into "dead zones" where a drone might otherwise lose its C2 link.|
|**Reinforcement Learning (RL/DRL)**|Used to teach the drone how to **autonomously change its flight path** to stay in areas with the strongest signal (Connectivity-Aware Path Planning).|
|**Federated Learning (FL)**|Allows a swarm of drones to "learn" how to detect interference locally without sending massive raw data back to a server, saving bandwidth.|
|**ISAC (Integrated Sensing & Comm)**|Uses the communication signal itself as a radar to "sense" obstacles, reducing the need for heavy onboard sensors.|

---

### 5. Pioneer Researchers in the Field

If you are looking for the most cited "founding fathers" of modern UAV communication, these are the names you will find in almost every bibliography:

- **Rui Zhang (National University of Singapore):** Widely considered the most influential figure. He pioneered the math behind **UAV-enabled mobile relaying** and trajectory optimization.
    
- **Yong Zeng (Southeast University):** A former student of Rui Zhang, he leads the work on **Cellular-connected UAVs** and 3D channel modeling.
    
- **Giovanni Geraci (UPF / Ericsson):** The bridge between academia and industry. His work focuses on **Interference Management** and how 5G handles aerial users.
    
- **Walid Saad (Virginia Tech):** A leader in using **Game Theory and Machine Learning** to manage drone swarms and network security.
    
- **Mohammed-Slim Alouini (KAUST):** Known for his work on **Optical (Laser) Wireless Communication** and hybrid Satcom-Daughter drone links.
    

---

### Summary Checklist for a BVLOS Paper Search

If you are starting a literature review, look for these "seminal" papers:

- _Zeng et al., "Wireless Communications with Unmanned Aerial Vehicles: Opportunities and Challenges" (IEEE Communications Magazine, 2016)._
    
- _Geraci et al., "Understanding UAV Cellular Communications: From Basics to 3GPP Standards" (IEEE Access, 2018)._
    

**Would you like me to pull the specific "Abstract" and "Key Contributions" from any of these specific researchers or papers for you?**

#### PhD presentation structure (expose guidance) (lines 338-373)

one usr | multiple user 
execution time 
symptom vs cause vs root cause



### presentation  - 2/3 
Title 
Intro 
Problem statement - literature 
purpose 
RQ 
Methods 
Outline and timeline 

Why / what I don't know - idea of research is answering the unknown 
Alignment   - Purpose and problem statement should be in same direction 

have is Short, clear - there is a problem and path ![[Recommendations_Expose2018_06_EN_web.pdf]]

Key questions to answer What is the core issue of your dissertation / PhD? What is the focus of the dissertation / PhD? Project? 

Which research questions should be investigated in detail in the dissertation/PhD project?
Which results / findings exist? What is the starting point of your research? How do you position your dissertation/PhD project vis a vis this state of the art?

Slide Structure 
- [ ] Title 
- [ ] What is my Project 
- [ ] Constraints /boundary condition built from it 
- [ ] What are current open problems 
- [ ] What is  the purpose 
- [ ] What RQ I answer 
- [ ] How to answer  - Methods - State of art what is done for each domain and what is yet to be realised  - Break it down
- [ ] What is the outcome - Base line and real world 
- [ ] What will be the outcomes answers framework of the results 
- [ ] Time plan 

#### Funding call: BMFTR (Rodney) (lines 379-393)

### CALL  
BMFTR - Rodney
https://www.bmftr.bund.de/SharedDocs/Bekanntmachungen/DE/2023/11/2023-11-08-Bekanntmachung-Stadtquartiere.html?templateQueryString=2023-11-08-Bekanntmachung-Stadtquartiere

https://www.bmftr.bund.de/SharedDocs/Bekanntmachungen/DE/2026/01/2026-01-09-foerderaufruf-drohnengestuetzte-innovationen.html

https://www.fona.de/medien/pdf/SOEF/20260129_TC_II_infoveranstaltung.pdf?m=1770032329&

Meeting with Rodney 27/2
- Already have partners
- Expectation of municipality department 
- topic
---
- topic not decided 
- 

#### IEEE P1920.2 / U2U notes (lines 397-400)

- **IEEE P1920.2 Standard Development" (Ongoing 2026):** Kamesh is currently finalizing the protocols for **U2U (UAV-to-UAV)** communication. This allows a drone far out of range (BVLOS) to "hop" its signal through another drone closer to the base station.
    
- **"Communication Signaling as Traffic Lights" (Late 2025):** He recently proposed a model where communication metadata acts like aerial traffic signals to manage high-density drone traffic in urban environments.
---

#### Notes from Lyuqiao defense (lines 402-427)

Lyuqiao Defense
 - NTN - in V2X
 - Internetworking - cross handover 
 - 8 - Priority based 
 - TN coverage measure and monitor 
 - lack of awareness  - predictive 
 - Q to me movement of UE and Movement of Satellite Direction 
	 - NTN part and TN  - Simulator 

- Q on sat  - Parameters 
- what is your cruiteria on signal params 
- 24 - CQI - MCS
-


- Service  - motivation of using TN
- Multi-cast handover 
- mobility for NTN and TN are separate 
- Time synchronization 
- NTN and TN 
- Location of the TN and NTN 
- Where the satellite is - 
- Downlink scenario
-  Interworking to  Integrating 
-  frank didn't get the meeting 
- Engineering wise 

### From [[mar 2026]]

#### Thoughts + realistic 2026/2027 publication plan (lines 1-35)

### THOUGHTS 

Inputs from Chair - Winter workshop : Focus: **Low Latency communication**  
Second AirMetro : C-SLAM - Multi-link 
PhD : Focus and higher level 
	Comnets 2 + traffic theory - 7 , Comnets 3  (5)
	New module from Winter Semester 
Prof Rafeal - Nw coding 



----

Last month at klagenfurt
Research stay pending work 
![[Klagenfurt-Research-stay.pdf]]

CAN I PLAN  one month work toa paper and 3 months work to Journal 

2026 realistic
1. April -> MAy submission for DRCN with Enrique 
2. April-May-June - July submission for IEEE Access- Simulator Opensource 
3. Aug -Sept - Conference paper with Enrique  -> Verify the methods with flight test data 
4. Nov and Dec - to A2A and Mesh hardware 
5. Mesh ahrdware scenario based testing - Dec 2026
// T2 paper with Enrique and Common Map representation 


2027 
 6. Data port - flight test data 
 7. C2 protocol Multi link - Conf in Jan 
 8. C2 protocol MAVLink - Journal in march 
 9. C2 protocol - multilink- Journal in September 
**Try 5 outta 9** 

#### Frank talk point (lines 37-37)

Points fro Frank talk - Jitter over latency?

#### Design of experiments notes (lines 175-185)

Slides 
Design of experiment 

Conditions impact a study -> impact on outcome 
Experiments tests causation - not correlation 
core pieces of the experiment - dependent / respond variable - that make up the experiment outcome 
inputs and control 
levels of factors 
replication and standard size 

full factoral study and one study at at a time factor

### From [[Apr 2026]]

#### Learning: UAV traffic vs network (lines 2-10)

# LEARNING- GENERAL

- Does UAV traffic pattern looks/ care about network ?
	- Today's traffic pattern don't care about the network - It seem sthe case for the AAM comm ?

![[Literature- organize.pdf]]

K Telecom economy - is Ubiquity to cater to upper part of k? https://www.youtube.com/watch?v=bxezy-P-OXE
Ardu pilot

#### Frank's reply on PhD course requirements (lines 76-84)

# Frank's reply Feb 9th 

 here a quick feedback (we have a protocol with Patricia):  

- so if they suggest courses, we can make counterpropoposals
- if the courses in mean are at least good, there is an automatic process to enroll the candidate
- in addtion to the course they ask for project work (i did not know about it), but they would count publications
- for those with a master better than 2.5, but have a cummulative track (bachelor plus master), I will try to crack this legally with D5

#### Tips: IEEE Access length, thesis acronyms (lines 312-317)

Notes for IEEE access - max upto 20 pages for readability

Prep for LAWN meeting

Tips for thesis
Get all the acronym and convection of terms at the beginning 

### From [[May 2026]]

#### Literature gap vs problem statement; venue links (lines 1-13)

Literature gap and problem statement aren't same 

Problem is direct reflection on lit gap 
problem is urgency , rationale to go after a gap 
Purpose 
- Check ICUAS if deadline extends
- DAUS , ARCI 
- https://www.ei-ce.com/call_for_paper
- https://publishingsupport.iopscience.iop.org/jpcs-forthcoming-volumes/

- Resilient communication is autonomy
" Do simulation work same way in reality ?"
Reliability and Resilience  -> Safety and RisK Event tree

#### Companies to look at (lines 138-140)

B2 Space
Ubotica technologies
Sateliot

#### 2024-2025 PhD meeting minutes highlights (lines 355-375)

2024  - PhD meeting minutes highlights

August
- Hardware purchase
- Tools
- cohstedt visit
- A1 and A3
- Topic presentation - [2024 September](https://tudresdende.sharepoint.com/:f:/t/RTG2947AirMetro/IgCO6BP9PPSWT507zQvIh7bmAauT2YkTqNZRqrCNeB59XRY?e=FZXoS0)
- Cluster dicussion 
- Post workshop discussion
- plan for first half 2025 -> Summer school 

2025
- Janna - Data management tools revisit and setup elabftw etc...
- Summer school and flight tests 
- winter workshop
- Linkedin setup 
- final scale of hardware purchase
- Lab setup, studentb assistance for lab setup
- PhD presentation 

#### Paper notes: experimental UAV data traffic modelling (lines 386-403)

**Experimental UAV Data Traffic Modeling and Network Performance Analysis**
data rate, inter-packet interval and packet length distributions, and identify their main influencing factors
The data traffic appears neither deterministic nor periodic but bursty, with a tendency towards Poisson traffic. We further create an understanding on how the traffic of the investigated UAVs are internally generated and propose a model to analytically capture their traffic processes, which provides an explanation for the observed behavior.

CNPC holds stringent communication requirements to ensure the safe operation of UAVs. Therefore, reliable and robust communication schemes are in demand to ensure flawless operations and public safety.

packet length distributions and study the end-to-end data rate, latency and transmission reliability performance. We identify the influencing factors on the traffic generation and CNPC performance, and study their effects. We model the data traffic of the UAVs and provide an open source data traffic generator for future UAV studies in [8].

The International Telecommunication Union Radiocommunication Sector (ITU-R) analyzes the technical characteristics of CNPC links [9] and found out 7 kbps for Downlink (DL)
Concerning latency, the studies, [13], [5], [14], estimate 40 − 100 ms demand to control UAVs in real-time. Comparably, authors of [15] measured the latency ca. 60 ms in an experiment for Beyond Visual Line-Of-Sight (BVLoS) operations of UAVs and robots. In another experiment regarding network performance measurement of swarm UAVs [16], authors measured the end-to-end latency between 2.4 and 30 ms with varying data traffic load. Contrarily, according to [17], the latency demand ranges from 100 ms to 3 s depending on the application type

As for reliability, 3GPP analyzes the requirements with respect to the types of communication traffic and the level of autonomy [13]. While the majority of the operations hold 10−3 Packet Error Rate (PER) demand, navigation messages that originate from UAV during take-off and landing require 10−4 PER. Similarly, Radio Technical Commission for Aeronautics (RTCA) specifies > 99.976% communication availability and > 99.9% communication continuity for CNPC [18].
Summarizing the presented studies anticipate the data rate requirements between 20 and 200 kbps for DL and up to 50 Mbps for UL, while the latency demand can be as low as 40 ms for CNPC. However, current studies do little to characterize drone traffic beyond average rate, latency and reliability requirements. We aim to take a step toward closing this gap in this work.
All the UAVs use the 802.11g protocol for communication, and we took the measurements at 2.4 GHz. However, capturing the data traffic on the UAVs themselves is not possible as DJI UAVs have proprietary software. Therefore, we utilized an Android phone as Remote Control and as data sniffer to record CNPC UL and DL data on the transport layer. Concurrently, we also used a laptop with Wireless Fidelity (WiFi) card in monitor mode for data capturing on Medium Access Control (MAC) layer. We ran Kismet [26] and tcpdump [27] to capture the traffic on the phone and laptop, respectively.

On DL, it stays approximately between 10 and 20 ms for both UAVs. At 50 m altitude, inter-packet intervals go up to 258 ms, which is due to poor channel performance. As for UL, the intervals are less stable and larger compared to the DL. This effect is caused by varying delays when exceeding the channel capacity with large data rates on the UL, as RF conditions are worsened at higher altitudes. Maximum inter-packet interval goes up to 3 s on DJI Mavic.

#### DRCN / FNWF objectives (lines 413-423)

# DRCN 

Obj: 
1. RCP objective -> Risk class profiling 
2. Evaluation in TN and NTN network 

# FNFW

Obj: 
1. Integrated TN and NTN network - UAV Handover analysis - hurestic method ( No existance of SIB)
2. RCP -> Transaction : Continuity, TT - > Age of Info , Latency 

### From [[June 2026]]

#### Thoughts and links (lines 1-10)

Protocol : SIP, GTP, Diameter, CAP , CAMEL 
LET archi 
WiFI Archi
connectivity is not response
https://harvardonline.harvard.edu/course/innovation-strategy?&utm_source=google&utm_medium=cpc&utm_campaign=fy26_innovation_intl&utm_content=nb&keyword=innovation%20strategy%20course&matchtype=p&gad_source=1&gad_campaignid=23234352362&gbraid=0AAAAAou4sP87bXxnmzUsf0pslzxabbtRz&gclid=Cj0KCQjw_vnQBhCxARIsADcZyxLOSiZnDiU7COUsjTkF7vrsBo6RybpuqWu_YU2ZRKu1qFTg6EGPGwMaArlaEALw_wcB

Algo like _RandomForest_ and _Telemanom_

Comm in different forms - visula, voice, data in UTM and Aircraft but this is not the case for UAv 
 Failure mode analysis - margin of failure 

#### EW talk feedback + Enrique presentation points (lines 212-246)

---

**Timing** 
12 +
Results 
Bullets - box it - main message (slide 7) 
more time spend -  1,2, 3, 

remove 5 
slide 6 on wards no issue 
 1.5 minute 
 
Just mention the challenges - 

Slide self consistent  - very picky - like a pitch 


Enrique presentation
1. urban canyon
2. signals of height 
3. height
4. main and side lobes 
5. spacial diversity 
6. Nulls and no connected 
7. mixed users 
8. RSRP - environment depend ()
9. ML models 
10. absolute position for BS 
11. Linear vs NL pathloss 
12. GNSS vs RSRP 
13. Algo and pathloss 



-----

#### Links + EW 2026 LinkedIn post text (lines 379-415)

---

https://www.barkhauseninstitut.org/fileadmin/user_upload/Publikationen/2021/2021_Kronauer_Latency.pdf

https://arxiv.org/html/2508.11366v1

---


AtRDS dornes 
Ashraf and chao is here 


Simalar to SML with Smonath Airsim - 
Presenstation - e conspicuity 
felix, ashraf, Andrea, 

---


Exploring the 5G- Advanced / 6G Mobile edge resources for U-space services

At European Wireless 2026, our colleague Shreeja Sridharan, under the guidance of Prof Frank, Stanislav Mudriievskyi presented recent work on **“Edge-Native Data Mesh for Real-Time Tactical Deconfliction in 5G-Advanced U-space Traffic Management.”**

The study explores how future U-space Traffic Management systems can leverage **5G-Advanced connectivity, Multi-access Edge Computing (MEC), and data mesh principles** to enable safe, scalable, and real-time coordination of uncrewed aerial systems (UAS).

🔍 **Methodology highlights:**

• Designing an MEC-enabled UTM architecture based on decentralized data mesh principles  
• Evaluating far-edge, metro-edge, and central cloud deployment strategies in high-density 5G-enabled aerial scenarios  
• Analyzing the trade-off between latency, scalability, coordination efficiency, and operational flexibility  
• Exploring how federated data governance can support mission-critical aerial environments

💡 The findings show that far-edge processing provides superior performance for real-time tactical deconfliction, making it highly suitable for dense and safety-critical environments, while metro-edge solutions provide effective regional coordination and reduced dependency on centralized infrastructure.

It was a great opportunity to present this research at **European Wireless 2026** and exchange ideas with the community on the role of  intelligence in wireless networks,  and future communication architectures for resilient aerial connectivity and mobility systems.

#### Aeroconf 2027: track, deadlines, abstract guidance (lines 420-505)

# Aero Conf 
Requirement 

# Track 
# 4.13 CNS Systems and Airborne Networks for Manned and Unmanned Aircraft

This session focuses on communications, navigation and surveillance systems, including on-board and ground-based systems for all vehicles operating in the National Airspace System (NAS): manned and unmanned vehicles, fixed wing and rotor-craft, general aviation, civil transport and military that may carry passengers, cargo or are performing surveillance-type missions. Topics range from concept development, simulation and modeling, technology development and verification, through flight testing and certification. Emerging fields include surface wireless networks, ADS-B, Datacomm, airborne network security, UAS integration, satellite-based CNS, and international activities.

- ![](https://aeroconf-papers.s3.amazonaws.com/production/users/453069794/thumb/IMG_0350.jpg?1746811902)
    
    **Jason Glaneuski**
    
    [jglaneus@gmail.com](mailto:jglaneus@gmail.com)
    
    Program Manager, ATM Systems, US DOT / RITA / Volpe Center : Jason Glaneuski is a Division Chief of the Air Traffic Management Systems Division at the Volpe National Transportation Systems Center (Volpe Center) in Cambridge, MA. His Division applies information technology and operations research disciplines to enhance the capacity, safety, and security of the National Airspace System. A key component of this work is developing concepts and designing automated decision-support tools and capabilities that provide solutions to existing and anticipated traffic flow issues. Mr. Glaneuski is a graduate of Daniel Webster College.
    
- ![](https://www.aeroconf.org/assets/avatars/thumb/missing-861903d964a35e10bcd344561dd6a15db5935c15be3f3270ca2af11b6c76eb5d.png)
    
    **Mark Cockburn**
    
    [mark.cockburn@dot.gov](mailto:mark.cockburn@dot.gov)
    
    Data Scientist, US Department of Transportation: Mark Cockburn is a Data Scientist in the Air Traffic Management Systems Division of the U.S. DOT Volpe Center. He holds a Master's degree in Information Management and is a certified private pilot. Mark supports the FAA with systems and network engineering, leveraging expertise in data science, cybersecurity, and DevOps/System Administration to drive innovation and enhance safety in aviation.


# Deadlines and rules 
Mar 6 - Mar 13, 2027 - Conf in Montana

1. Create account Ensure that paper co-authors also establish accounts to receiver notifications related to a joint paper. 
2. Abstarct submission 
3. Submit your **complete** paper (in pdf format) no later than the **Paper Submission Deadline**, **Oct 2**, at 
4. Review comments are sent by mid-November.
5. **Download review comments** for the paper at your My Submissions page.  If the paper has been **Approved**, respond to suggestions, make necessary corrections, and prepare your **final paper**.
6. Abstract Due Date (300 - 500 words) : July 1, 2026



---


Background and problem statement 
objective and purpose 
methodology 
priciple results and data 
significance and application 
300-500 words


Quantitative and not qualitative

**How large should the initial Abstract paper proposal be?**

It should be about 500 words.

**Q11. What should be in the abstract?**

Your abstract is a stand-alone statement that briefly conveys the essential information of your paper; presents the objective, methods, results, and conclusions of a research project; has a brief, non-repetitive style.

It should state concisely:

1. The work that has been done.
2. The methodology (if important).
3. The principal results (quantitatively, when possible).
4. The significance of the results.

The abstract summarizes the paper and is a justification of the work. It is important that the paper’s abstract be as informative as possible.

**Q12. How do you write an abstract?**

Writing an abstract involves boiling down the essence of a whole paper into no more than three paragraphs that conveys as much new information as possible. One way of writing an effective abstract is to start with a draft of the complete paper and do the following:

1. Highlight the objective and the conclusions that are in the paper's introduction and the discussion.
2. Highlight the results from the discussion or results section of the paper.
3. Compile the above highlighted information into a single paragraph.
4. Delete extra words and phrases.
5. Delete any background information.
6. Rephrase the first sentence so that it starts off with the new information contained in the paper, rather than with the general topic. One way of doing this is to begin the first sentence with the phrase "this paper" or "this study."
7. Revise the paragraph so that the abstract conveys the essential information.

**Q13. What should NOT be in the abstract?**

Formulae, TOC, Author information, addresses, list of keywords, detail as opposed to summary results.

**what is achieved**
**how it is achieved**
**why it is achieved**

#### PhD defense notes (multipath, Brunstrom) + abstract feedback (lines 513-625)

# PhD Defense 
Reliable Multipath Connectivity for RPAS in UAM 

Anna Brunstörm, Karlstad University 


LAAirspace busy 
Safe piloting 
Wireless connectivity 
Reliable Low-latency multipath connectivity 
Reliability and robust connectivity 


Big picture of thesis
end to end - Application , Transport, Wireless Networks - QoS demand 

INFOCOm 2021 
COMST 21 
multipath coonectivity -> 
Access network optimization 
Multipath Transport 

![[Screenshot from 2026-06-25 10-09-47.png]]
cellular network 
Public infrastructure for ground communication 

Handover frequency 
cellular vs LEO 
Packet loss
![[Screenshot from 2026-06-25 10-13-23.png]]

How multipüath should work 
ques - How many redundant links for 5 9's of availability
![[Screenshot from 2026-06-25 10-14-55.png]]

link redundancy - from 
2-4 parallel links for 99.999% reliability 
Quasi -exponential growth - Non linear model
Flows - Vehicles

Bonmin-Taylor 
Gurobi

complete protocol stack 
![[Screenshot from 2026-06-25 10-18-14.png]]


Path utilization 

- heterogeneity in data traffic 
- Congestion control -> queuing delay 
- Retransmission influences but ineffective for improving the reliability and latency 
- 
- Model Based BBR 
-
![[Pasted image 20260625102518.png]]

Bottleneck of congestion control 

UDP based Multipath transport 


Drone small traffic
AirTaxis - higher 



---

Collision detection and avoidance 
Martin 
GNSS , FLARM 

Performance of 

error - FLARM is accurate 
Remote ID 
offset the error 
Timing - latency 

data sets
Horizontal error - LSTM error 


---


Abstarct

- what they do 
- Context first is a choice 
- Big problem- > 
- expected results how to describe the results 
- flight tests -> 

How convince me -> how architecture 
how results - look like
conclusion 

what is my ambition of the result ? 

Less of context and more of actual stuff I do. 


merge both  and reduce (para 1 and 2)

elastic boundary - 


moreover, 

reduce on padded sentences 

#### INTANS note (lines 627-638)

---
send email 
NTN use case  - LEON 

INTANS is TN and NTN 
TANGO  - Patches

Simu 5G  and INET


Results 
Overleaf on Friday 

#### Aeroconf abstract draft (lines 642-692)

---

As the low-altitude economy accelerates, integrating UAVs
into non-segregated airspace demands more than ’best-effort’
wireless connectivity. Moreover, reliability and resilience
within the digital communication domain is now an urgent
priority due to the unmanned and autonomous nature of
UAVs. The Command and Control (C2) communication
system, an essential safety tether for Beyond Visual Line of
Sight (BVLOS) operations requires a rigorous framework to
meet strict aviation specifications, deterministically reliable
and resilient. The existing Required Communication Perfor-
mance (RCP) defines reliability by setting strict static bounds
on parameters like Transaction Time, Continuity, Availability,
and Integrity. Beyond security, a new domain is required
specifically for communication and connectivity: verifying
whether the C2 link is active or impending degradation in C2
message traffic. Therefore, in this work, we address the gap
from C2 reliability to system-level resilience by focusing only
on communication and connectivity paradigm.
This subset is critical because contemporary wireless tech-
nologies are fundamentally not built for C2 communica-
tion when compared to legacy aviation solutions. To solve
this, conventional strategies rely on spatial redundancy and
layered architectures, such as automated ground alerts and
coupled maneuvers - a complexity penalty. Consequently,
this work shifts toward a temporal and behavioral ap-
proach to address the resilience in connectivity, calibrating
system behavior to the operationally functional boundary.
To achieve this, we introduce a behavioral connectivity
resilience model built upon two key contributions. First,
we develop a phase-based C2 system architecture spanning
proactive, reactive, and post-corrective operational windows
to dynamically manage the RCP under potential C2 degrada-
tion condition. The Proactive Phase anticipates and preemp-
tively adjust transmission mechanisms on the C2 system. The
Reactive Phase actively mitigates real-time network delays to
maintain vehicle control during active link stress, while the
Post-Corrective Phase safely governs system resynchroniza-
tion and state restoration. Second, we formulate a dynamic
Operational Margin representation that envelopes these three
phases specifically for Very Low Level (VLL) airspace. This
time-variant behavioral framework is evaluated using a UAV
equipped with a heterogeneous, multi-link communication
suite (WiFi, 5G, and LEO Satcom) compliant with Specific
Assurance and Integrity Level III (SAIL III) and above.
By analyzing performance metrics across each operational
window, we present the derived operational margins for the
evaluated system, demonstrating that the UAV can safely nav-
igate communication anomalies through adaptive, behavioral
control of the C2 system

### From [[July 2026]]

#### Readings + npj suitability assessment of flight-test paper (lines 1-73)

# Readings and thoughts 

1. https://ieeexplore.ieee.org/document/6407436?denied=
2. https://medium.com/@sentalkssane/a-beginners-guide-to-system-design-76d64689788b
3. https://laetimes.com/en/news/easau-space-light - Upsace Light
4. QOS R- required, D- delivered, E- experienced
5. https://github.com/heistp/irtt IRTT and GPRC protocol  - Satcom tests
6. short term latency prediction 
7. lightweight parametric and non parametric model 
8. stable latency vs spikes 
9. CHARACTERIZE -> INVESTIGATE --> INTRODUCE 
10. Low-latency communication are concerned with upper latency quantiles rather than mean latency
11. Exterme Value theory 
12. Generalized Pareto distribution responsiveness vs service reliability 
13. nonpredictive model - emperical destribution 
14. predictive model - regression, classification 
15. DOE - Design of Experiments 
---
To give you a direct, candid assessment as an academic peer: **No, the flight test data _alone_ is highly unlikely to be accepted by a Nature Portfolio journal (like _npj Wireless Technology_).**While a physical flight test comparing 5G, Iridium, and Mesh Wi-Fi for MAVLink command-and-control (C2) is incredibly practical and valuable, it lacks the **novel theoretical contribution** or **fundamental scientific breakthrough** that _Nature_ editors look for.

However, your idea has immense potential. With the right framing and methodological adjustments, you can elevate this from a "simple field report" into a high-impact paper suitable for prestigious IEEE journals or even an _npj_ thematic collection.

### The Reality Check: Why Nature Would likely "Desk Reject"

To understand why, let's look at what _npj Wireless Technology_ evaluates:

|**What Nature Looks For**|**What Your Current Pitch Offers**|
|---|---|
|**Fundamental breakthroughs** (e.g., a new physical-layer modulation, a novel mathematical framework for 3D channel modeling, or AI-native 6G beamforming).|**Empirical measurement** of existing, commercially available technologies (5G, Iridium Satcom, Wi-Fi Mesh) using standard protocols.|
|**Generalizable theories** that can predict wireless behavior across diverse, unseen low-altitude environments.|**Site-specific results** tied to a single 20-minute flight path at a specific location, which may not translate to other geographic areas.|

Essentially, the editors will view this as an **engineering evaluation report** rather than a **scientific discovery**.

### How to Elevate Your Research for High-Impact Journals

If you want to target **npj Wireless Technology** or a top-tier IEEE journal (such as _IEEE Transactions on Vehicular Technology_ or _IEEE Internet of Things Journal_), you must shift your focus from _what_ you measured to _how you model and solve_ the problems you found.

Here is how you can transform your flight test into a high-impact paper:

#### 1. Shift from "Data Presentation" to "Predictive Modeling"

Instead of just showing QoS (Quality of Service) and RCP (Radio Link Control Protocol) metrics at three altitudes, use your empirical data to **build or validate a hybrid propagation model** for low-altitude airspaces (typically under 1000m).

- _The Pitch:_ "We develop a predictive, multi-connectivity channel model for low-altitude UAVs that dynamically maps the handover boundary between cellular, satellite, and mesh networks based on real-time C2 telemetry."
    

#### 2. Propose an Intelligent "Decision Engine"

A 20-minute flight test is the perfect validation tool for a new algorithm. Instead of just testing the three technologies separately, design an **intelligent, adaptive switching algorithm** (e.g., a lightweight machine learning agent on the UAV) that dynamically switches between 5G, Satcom, and Wi-Fi to maintain zero-packet-loss MAVLink C2.

- _The Pitch:_ "We present a reinforcement learning-based hybrid routing protocol that optimizes MAVLink QoS by predicting link degradation before it occurs."
    

#### 3. Address the Satcom-to-Cellular Latency Gap

The latency of Iridium (~hundreds of milliseconds) is vastly different from 5G (<30ms). If you can mathematically model and solve how MAVLink handles these sudden latency spikes during handovers without triggering "failsafe" behaviors, you have a highly publishable paper.

### Recommended Journal Targets

If you keep the paper focused strictly on the **flight test measurements and empirical data**:

- **MDPI Drones or MDPI Sensors:** Very receptive to practical flight tests, empirical data, and experimental setups. Faster publication time.
    
- **IEEE Access:** An open-access journal that values practical engineering contributions, hardware-in-the-loop tests, and empirical measurements.
    
- **IEEE Vehicular Technology Magazine:** Great for high-level system evaluations and real-world trial results.
    

If you add **theoretical depth** (e.g., adaptive switching algorithms, mathematical channel modeling, or predictive QoS algorithms):

- **npj Wireless Technology:** Highly suitable once there is a strong "intelligent connectivity" or "AI-driven" optimization aspect.
    
- **IEEE Transactions on Wireless Communications / Vehicular Technology:** The gold standards for rigorous wireless network optimization.

#### Resilience thesis link (lines 96-96)

Resilience - https://tud.qucosa.de/landing-page/?tx_dlf[id]=https%3A%2F%2Ftud.qucosa.de%2Fapi%2Fqucosa%253A30538%2Fmets

#### Meeting with Roshan (lines 528-535)

# Meeting with Roshan 

1. RIS
2. Mesh wiring and case design 

#### Meetings: Ming (patent), Krim & Jiajing, D3TN (lines 539-663)

# Meeting with Ming - Notes

- 3rd July 
- Discussion on Telemetry 


identify direction 


Satellite IoT 
Establish protocol for security 


Telekom IoT perspetive 

IoT platform 

Iot business - traditional 

connectivity  and mobile or NTN - telecom core - their platform and customer 

patents 
Experiments and papers 

patent idea  - first 

transfer technology - IoT guys -> Vendor -> Business
One concrete - problem 

word document 

coordinate multi point -> bunoi -> time and precision synchronization 

Alternate to GNSS 
 13 pages 
 motivation
Stack, architecture 

How to deploy it in reality 

extract the claims  - max 15 - which is new

Mattius Sena 

CONVINCE THIS IS NEW

Datashare 

randomness mesh beacon - 

---


9/7
# Meeting with Krim and jiajing 

- R2U2 responsivity by injecting faulty 
- guassian distribution to distribute data 

---

# Meeting with D3TN 

1. D3TN - stable e2e 
2. DTN architecture 
	1. Store and forward
	2. Custoday transfer
	3. late binding 
3. Bundle protocol - Bundle layer via shim / convergence layer 

D3TN - Fault toulerant networking 
Felix Walter - SML  met  with Marius Feldmann 
Future connectivity 

Autumn  school - October - communication and drone swarm 

Crazy flie 

Hall - Metal and steel collm - interferences 

REDMASS project 
 use-cases AuV / Drones 
 Heterogeouns DTN - ADhoc links - Adhostic and deterministic links  - Multi-layer 
 opportunistics mechanism of the layers 
ESA based satellite link D2D - ground station 
Encapsulated towards other drone . Internet- host 

bird counting - german admin entities 

kasen beta - Kiwi Grid / beta    - drone autonomous U-space to Elsteheide 
forest 

STARK projects  - Bronclo initiative to support activities in SML 
certification  - LBA 

Alex present on drones 
 - hardware slides 
 - Holybros - redmars

Drone KMU innovative project 
D3TN - University - Subparty funding 
STARK proposals  - Lausitz
SAB projects - 2028 
BMBF 
- Solar plant - semi auto- or auto loading - green mission 

- Feature development on Opportunistic
- New drafts and protocols , routing & Discovery 
- Start with MThesis 
- project acqisition 
- Benutzer ordung - Scientific - separate 
- Marius 
- serious educational games in mixed reality Worlds 
	- Fire brigade training  FoE  
	- SML - panometer 
- Thinking Entrepreneurial 
-  Aug 27th SML - open day 
- https://d3tn.com/projects-redmars.html
- https://arxiv.org/pdf/2510.27325

Sure, I only have their CTO's address, which is [felix.walter](http://felix.walter "http://felix.walter/")@d3tn.com, the other person's Name was Marius Feldmann, so probably marius.feldmann@d3tn.com, they also have a phone number on their website



---

#### Enrique meeting (lines 665-668)

# ENrique Meeting 

1. QoS  Annex 10 vol 6
2. UL, DL TN only NTN only 

#### FNWF idea (lines 680-683)

# FNWF idea 

1. Enrique - Continuity and Complaince 
2. UTM 

#### Peer review notes (HITS paper) (lines 688-709)

# Paper review 

The paper proposes HITS, a bi-level traffic steering framework for multi-RAT vehicular networks combines a coordinated two stage approach - a central GCN-LSTM module (spatio-temporal RAT optimality prediction) with a local SARSA-based RL agent (vehicle-specific adaptive RAT selection).
The valiudation of the use-case is  via OMNeT++/INET/Veins/SUMO/Simu5G co-simulation under two deployment densities (S1, S2), against four baselines NTD, BIL-TS, DQN, MLTS). The goal is to evaluate the effeciency of this approach gains in throughput, PLR, latency, and ping-pong switching rate, plus a symbolic complexity/overhead analysis for deployment feasibility.

PROS

Well-motivated problem framing
Architecturally sound component choices - explained well 
g Big-O signaling/compute complexity of RL deployment 


CONS 
1. The author in the backgorund refered the prior work as BIL-TS lacks a grpah model (vehicular network as evolving graph) but the system design BIL TS is mentioned as adaptive learning integrated with temporal graph model   is inconsistent to clearly distinguish what are the exact takeawys of prior work and what evolvement are introuced here. 
2. In model formulation, the definition of exploration rate could be presented in detail
3. GCN operates as one shared graph or a multiplexed Indexed output is not clearly specified
4. Most of the main claims of the results in abstract match the evaluation, but the latency metrics of the network level (from omnet++) but the latency of HITS architecture is not fully explained. Is this inclusive, or how is this treated in respective scenarios is unclear.
5.  The claimed "95% confidence
intervals are computed where applicable" is not interpreted clearly in presented result metrics . 
Also, the complexity framework mentioned in the performance analysis section is not clearly derived in the results and remarks section. 
6. The system model and abstract present HITS as RAT-agnostic and general (5G/4G/802.11p/WiFi), but only 4G/5G are evaluated, as the claim ultra-dense,heterogeneous multi-RAT scalability are only partially presented. This is abeit stated in the future work. 
7. On other instance, the sensitivity analysis on hyperparameters are fixed (same weight) configurations, which is left also as future extensions. 

### From [[August 2026]]

#### Thought + ESREL link (lines 1-2)

Can I say, I send packet via Stacom- via 5G - Semantic 
https://esra.website/esrel

#### Doodle Labs links (lines 139-140)

https://kb.doodlelabs.com/starlink-satcom-integration-guide
https://doodlelabs.filecloudonline.com/ui/core/index.html?mode=single&path=/SHARED/%21qrj7yyGkC7ddf30uyg3kVGjq3YxZH9155dSoa1pzk/wXGsdYeksvloAM1W#/

#### Tianxiong risk model, A2G reliability, Enrique meeting (lines 241-290)

# Meeting with Tianxiong

Parameters of bigraph model 

four layers of risks 
1. communication  - no more, lost - 
2. take off and landing 
- model recovery 
Mission success rate and 

cube 100 - 10 m/s - 10 s

Drone lost - comm lost each grid MTBF

to do: outage percube perspective 


---

Drone communication - UAV air-to-ground (A2G) link reliability problem
1. Availability - When BS provides connection 
2. Continuity - non-continuity - extends - link loss/ outage condition 

BS, Height of BS   hBSh_{BS} hBS, uav altitude hUAV​

General DIstance equation - 3D distance - I assume UAV is having a straight path 
d(t)=(x(t)−xBS​)2+(y(t)−yBS​)2+(hUAV​−hBS​)2​

where x(t),y(t)x(t), y(t) x(t),y(t) trace the UAV's straight-line path at 10 m/s through the cube. This gives you a distance profile d(t)d(t) d(t), and an elevation angle profile:

θ(t)=arctan⁡ ⁣(hUAV−hBS(x(t)−xBS)2+(y(t)−yBS)2)\theta(t) = \arctan\!\left(\frac{h_{UAV}-h_{BS}}{\sqrt{(x(t)-x_{BS})^2+(y(t)-y_{BS})^2}}\right)θ(t)=arctan((x(t)−xBS​)2+(y(t)−yBS​)2​hUAV​−hBS​​)


---

# Enrique  Meeting 

1. prior 
2. Operational margin 
3. Latency, Velocity operational margin 
4. Prevention - inner loops 
5. Operational margin 
6. Communication Performance envelopes 
7. Enhanced envelop with and without reactive area 
Tasks 
Break it into small parts 

8. Brief to do list 

NVDIA Tool  - Omniverse 

#### Vincent defense + Janna data-management meeting (lines 424-466)

# Vincent defense 

Resilient communication, computation task Distribution and scaling under uncertainity

assymptotical optimum


---

# Meeting with Janna 
1. ENtry of experimnets 
2. datamanagement - elab - setup - intranet

Resources 
	Hardware
	Software 
	Material 
Meta data  - enquiry and grouping entry 

BRIEF LOOK - review 

Experiments 

Document processes 
Flight test and computational research 

We do now computational research - Simulation and other - analysis

Parent and child category 

basic and comprehensive 

basic - less work - data dump 


create one for series


Enter Omnet++ - as resources 

duplicate 

Review - Meta data

#### Roshan (lines 470-473)

# Roshan

1. RIS functionality - in new sionna - verify 
2. path

### From [[Sept 2026]]

#### Standards / reproducibility questions (lines 1-18)

PhD committee Approved the Internship and credits 
Do report 
Present and get it graded
> What assumptions do current testing methodologies make?

> What measurements need to be standardized?

> How should performance be compared between systems?

> What terminology is inconsistent?

> What safety/verification evidence would an industrial user need?

> What would make results reproducible across laboratories?

That gives you a very valuable profile:

**researcher who understands standards because they actually had to validate technology**

#### References (ArduPilot 4G), courses, peer review notes (lines 217-245)

# References 

https://www.bartslinger.com/uas/ardupilot-4g-telemetry-and-video
https://arxiv.org/html/2512.06889v1
https://dev.vimdrones.com/tutorials/ardupilot_lte_network_setup_with_serial_interface/
https://mavlinkhud.com/easydrone4g-setup.html

Courses 
https://www.iata.org/en/training/courses/aviation-law-fundamentals/lrc002elen01/en/


-----
General 
This paper builds an exact reliability model for a catastrophe-prone aerial-satellite tandem relay system for NTN, which is relevant to current demands.  It addresses reliability model, Energy trade off for ensuring data protection, availability and control invariant system  in face of failure, and predictive  methods. 

The paper have sufficient proof and baseline for the claims mentioned in the abstract. But, the following suggestion can be considered by authors to improve the manuscript 
1. The Introduction section  can be improved. eg: this paper address, already presents the contribution in detail and the contribution paragraph sounds repetitive 
2. The background/ related work section is sufficient and the table adds reasonable value to the gaps addressed. 
3. Figures and plots must be improved. The figure 1 and 2 have incomplete / misplaced arrows, which hinders the readers. The plot in figure 14 is missing legend
4. Abbreviations need to be introduced earlier. Eg: PHM, CMTC are never explained within the context of the work. 
5. The referring system is inconsistent - eg: some places have Figure, and some have Fig 
6. It would be better to have a paragraph that states the takeaways from previous section and goal of the current section at its beginning. Eg: There is a paragraph at the beginning of Section 4, but the same is missing in Section 5 
7. The writing can be improved and conclusions/results can be presented better. Eg: The numerical results in 6.10 presents DQN as secondary diagnostics, But teh earlier section never presented this assumption. 
8. In System Model Section, the Formal description is presented before the assumptions and scope (3.3) , which contradicts the goal of system chain representations. 
9. Similarly, certain equations are never validated or quantified later. Eg: 3.7 was mentioned to be used later, but was never justified. This raises accountability issue and rigor in the mathematical framework. 
10. The Numerical results needs to be presented better. Certain plots are not refereed in the justification - eg Figure 7, 8 
11. The summary in the conclusion could refer to respective table and figure to ensure the claims in the abstract are reasonably represented. 
12. The paper fails to address the shortcomings of the assumptions such as fluid approximation , queue-control strategy which will ensure the reproducibility  and novelty of the work. 

#### Aeroconf coherence check + NB-IoT paper notes (lines 257-302)

### Part 1 — Coherence check on Subsections 1 and 2

Overall the two subsections build on each other correctly, but there are three concrete breaks in the chain that a reviewer would catch, plus one placeholder that's now resolvable from what we established last message.

**Gap 1 — Subsection 2 references a state space Subsection 1 never actually defines.** Subsection 2 opens with *"the common state space {S0,SD,S1,S2,S3}\{S_0, S_D, S_1, S_2, S_3\} {S0​,SD​,S1​,S2​,S3​} introduced in previous subsection"* — but Subsection 1 only presents the Proactive/Reactive/Post-corrective phases in prose and Table 1; it never formally writes out the five-symbol state notation. As drafted, a reader hits that reference in Subsection 2 with nothing to look back at. **Fix:** add one sentence to Subsection 1, right after the timing paragraph, formally introducing the notation before the table or timeline discussion needs it.

**Gap 2 — The ΦΛEΠ\Phi\Lambda E\Pi ΦΛEΠ paragraph in Subsection 1 is orphaned.** It's introduced early (citing `panteli2017metrics`), then Subsection 2 never touches it, and it only resurfaces in Subsection 3. That's a three-subsection gap with nothing carrying the reader through. **Fix:** either move this paragraph to open Subsection 3 (where it's actually used), or add a one-line forward-pointer in Subsection 1 ("...developed further in Sec.~3.3 alongside the operational-margin trapezoid") so it doesn't read as abandoned.
![[Pasted image 20260909145600.png]]
**Gap 3 — The "EE E pending" placeholder is now resolvable, not still open.** The red-flagged uncertainty ("Loss (E), pending, most likely as loss of availability") can be closed using the LC2L reconciliation from last exchange: EE E is the S2S_2 S2​ dwell duration, bounded by τsurvive\tau_{survive} τsurvive​, and relates most directly to **Continuity** (sustained loss of the link is precisely a continuity violation), not Availability — Availability is better attributed to Φ\Phi Φ (the pre-disturbance nominal-dwell metric), consistent with how the uploaded LC2L document assigns it. This should be written in as a resolved statement, not left as a pending note, in whichever subsection ends up holding the ΦΛEΠ\Phi\Lambda E\Pi ΦΛEΠ paragraph after Gap 2 is fixed.

**Gap 4 (minor, implementation-level) — Subsection 2's simulator description is still a bullet placeholder, not prose.** The red `\textcolor{red}{Implementation Idea}` list (TN-NTN Simulator, Physical/Protocol methods) needs to become a sentence or two of actual descriptive text tying the OMNeT++ digital-twin validation explicitly to Contribution 2, or it reads as an unfinished note inside a submitted paper.

None of these break the logic — they're continuity/completeness fixes, not conceptual errors. Once Gaps 1–3 are patched, Subsections 1 and 2 read as one continuous argument: define the layer×phase table and its state space → show each layer's sojourn-time model is separately fittable and validated. Subsection 3 below is written to pick up cleanly from that point.


-----


# NBIOT Aeroconf paper 

1. Paramters for the link 

Send/recv, connect - UDP packets 
Monitoring parameters - Cell id, rsrp, snr, 
**`NW-provided_eDRX_value>`** — The extended Discontinuous Reception cycle length the network has granted the UE (for power-saving — lets the UE sleep longer between paging checks).


Vendor specific values 
My RSRP, RSRQ and SNR values are very bad:
• Especially in the case of GEO, the above values are much worse than what one would typically
expect from an NB-IOT (terrestrial) connection.
• RSRP average around –120dBm or a bit less is very good RSRP for GSO NTN.
•
•
RSRQ average around –12dB is just fine.
SNR average around 0dB or a few dB below zero is still fine.


Test ideas : 

3 days every 30 min/ 60 min - Payload size varying and UDP protocol 

Non- monolithic payloads - Cannot be agrregated as in TN 
NB-IoT operates in half-duplex frequency division duplexing, meaning the
modem cannot transmit and receive simultaneously. Delay tolerant reporting

#### LAWN discussion + links to look into (lines 320-338)

# LAWN discussion 

1. Frankfurt crusing and descent + land 
2. 4 base station - gnB - sectors - 3 8* 2 38 901 
3. RIS - doesn't have direct Line of sight 
4. RIS two ways - Path gain only from RIS 
5. site c is primary 
6. Phase gradient refector 


---

Look into it 
- [ ] https://www.iata.org/en/programs/ops-infra/air-traffic-management/5g/
- [ ] https://www.iata.org/en/training/subject-areas/air-navigation-courses/
- [ ] https://www.iata.org/contentassets/badbfd2d36a74f12b021c9dd899ecbad/type-b-messaging-whitepaper-v2.5.pdf
- [ ] https://www.iata.org/contentassets/badbfd2d36a74f12b021c9dd899ecbad/whitepaper_future_aircraft_communications_v1_3.pdf
- [ ] https://www.iata.org/en/programs/ops-infra/air-traffic-management/cns-technologies/#tab-3
- [ ] 

### From [[Oct-2026]]

#### Thesis must be persuasive; cone/sphere/diamond pitch; links (lines 1-22)

![[imagen.png]]
![[IMG20261015143108.jpg]]

**<span style="color:rgb(0, 176, 80)">Thesis must be persuasive</span>** 

Thesis 
Firsts - Pages, structure, chapter str
![[Screenshot from 2026-10-20 16-23-44.png]]


https://ooir.org/journals.php?field=Engineering&category=Telecommunications&metric=jif

**When to use each**

- **Cone:** when people ask "what's your field?", for example at the start of a talk, in a funding application, or when introducing yourself.
- **Sphere:** when people ask "what's new?", for example in reviews, your defence, or the novelty statement of a paper. It's your strongest pitch, because few people combine 3GPP and ICAO RCP.
- **Diamond:** when people ask "how is the thesis organised?", for example in the table of contents or a progress report. Map each middle box to your papers.

One-sentence version for the cone tip: _"I make commercial heterogeneous links (5G, SatCom, Wi-Fi) provably good enough for aviation-grade UAV command and control, measured by a Reliability Margin against ICAO RCP."_

Want me to adjust the labels (e.g., add your actual paper titles into the diamond) or turn these into slides?
https://arxiv.org/pdf/2610.28097

#### Workshop prep, NTN meeting, Nano ping talk (lines 400-433)

# Workshop preparation 

1. presentation
2. poster 
3. breakout session and todos 


# Meeting 
Wingcopter 190k€ 198cm 

---

# Meeting NTN 

1. Device - cell
2.  no new VSAT - industry is looking into

---

# Nano ping - Talk 

reliable connection  top of unreliable network 
![[Screenshot from 2026-10-06 11-21-29.png]]
The goal is not low latency 
Reliable Delivery within application deadline 
![[Screenshot from 2026-10-06 11-31-12.png]]
![[Screenshot from 2026-10-06 11-36-10.png]]
![[Screenshot from 2026-10-06 11-52-12.png]]


codec 


----

#### Simulator notes: NTN uplink fixes (lines 435-460)

Simulator notes

NTN uplink now works, but the link budget wasn't what blocked it, so I haven't changed any power, gain or noise values. Three code bugs stopped every UL packet from going over the satellite. With them fixed, the full 560 s run finishes without errors, and about 16% of the UAV's packets now reach the server over NTN.

**What was broken, and the fixes:**

1. **The UL resource request went out on the wrong carrier** ([NrPhyUeVeinsNtn.cc:436](intans/src/stack/phy/NrPhyUeVeinsNtn.cc#L436)). Simu5G always sends the UE's RAC request on its primary carrier (TN, 5 GHz). The satellite dropped it as "carrier frequency not supported", so it never gave the UAV a UL grant. Now, while attached to NTN, the RAC request goes out on the 30 GHz carrier.
2. **The satellite crashed on packets addressed to the ground** ([leon Ip2NicGnbNtn.cc](leon/src/stack/ip2nic/Ip2NicGnbNtn.cc)). LEON only handled destinations that are a UE or a satellite, so a packet for `server` crashed it. Now the satellite tunnels it in GTP (the standard 5G tunnel to the core network) towards `upfNtn`, the way a terrestrial gNB does. It then relays it over ISL to the satellite serving `ntnGateway` and sends it down to the gateway. This adds a NED parameter `ntnGatewayModule`, default `"ntnGateway"`.
3. **Satellites had no tunnel endpoint** ([simu5g GtpUser.cc:59](simu5g/src/corenetwork/gtp/GtpUser.cc#L59)). Only base stations with a wired link looked up their `gateway` address, and satellites have none, so every tunnelled packet was dropped. Now a base station without a wired link also looks it up, and the lookup fails silently if that gateway doesn't exist, so other LEON setups won't break.

**Run 0, full 560 s, before and after the fixes:**

| | Before (your 30 runs) | After |
|---|---|---|
| Packets reaching the server | 62% | **77%** (frame loss 0.39 → 0.25) |
| Received over NTN (via `upfNtn`) | 0 | **3,379** |
| `nrChannelModel[1] rcvdSinrUl` samples | 0 | **13,612** (mean −7.4 dB) |
| Mean delay | 18.6 ms | 36 ms (now includes satellite paths) |

**About the link budget:** the NTN uplink still runs at a mean of −7.4 dB, compared with 9.2 dB on TN. It works now, but if you want a stronger NTN uplink, raising UAV transmit power from 26 dBm to 33 dBm would add about 7 dB. 33 dBm is the 3GPP TR 38.821 value for a Ka-band VSAT terminal, and your ini already uses that terminal's 1.2 dB noise figure. That changes your scenario, so I'll only do it if you say so.

**Before you rerun:**
- **The 30 runs you already have can't be compared with new runs.** In those, NTN carried no UL at all, so they are effectively TN-only with outages. Rerun all 30.
- **The TN↔NTN ping-pong every 5 s is unchanged.**
- **Rebuild everything:** debug and release libraries are rebuilt for intans, LEON and Simu5G, and the IDE will also rebuild before launch. Keep `veins_launchd` running on port 9999.
- **Simu5G is a modified copy, not stock**, and isn't under git, so this third change isn't tracked anywhere. LEON is a git repo, and fix 2 shows up there as uncommitted changes.

#### MAVLink / RCP notes (lines 464-522)

# MAVlink Notes 

Transaction Identification: All critical C2 message ex-
changes must be cataloged. Common transactions include
Uplink transactions (Emergency Motor Cut-off, Waypoint
Update, Return-to-Home Command), and Downlink (System
Heartbeat, Telemetry Update, Alert Propagation).
2) Criticality and Benchmarking: Each transaction is eval-
uated for the severity of its loss or delay. The transaction with
the strictest latency requirement becomes the “Design Driver.”
For instance, if a geofence breach requires a pilot intervention
within 10 seconds to prevent an excursion from the operational
volume, the entire C2 link is dimensioned to satisfy RCP 10

The performance requirement are formally defined by four
metrics: Availability (A), Transaction Time (TT), Continuity
(C), and Integrity (I).
1) Availability (A): Availability is the probability that the
communication service is operational and capable of initiating
a transaction at any random instant. For aviation safety, this
ensures the link is present when an emergency command needs
to be sent.
2) Transaction Time (TT): The Transaction Time repre-
sents the maximum allowable time for the completion of a
transaction with a specified confidence. It corresponds to the
Expiration Time (ET ) defined in ICAO PBCS, after which the
initiator is required to revert to an alternative procedure [19].
T = THM I + TU plink + TP roc + TDownlink (1)
where THM I is the human-machine interface processing time,
and TP roc is the processing time on the UAS.
3) Continuity (C): Continuity is the probability that a
transaction will be completed within the Transaction Time
(TT), given that the system was available at the start of the
transaction. Kl¨ugel and Schupke [19] model this using the
cumulative distribution function (CDF) of the transaction delay
T :
C(TT) = Pr{T ≤ TT} = (1 − pe) · Fd(TT) (2)
where pe is the probability of packet error/loss, and Fd(t)
is the delay distribution function of the link. Target values
typically range from 0.999 to 0.9999 per flight hour, depending
on the SAIL.
4) Integrity (I): Integrity is the probability of an undetected
error occurring in a completed transaction. This is a function
of the protocol’s error detection capabilities and is typically
required to be < 10−5 per flight hour [8]. In this work, we do
not explore the integrity of the C2 link.
D. Compliance & Allocation
Based on the risk specification of the mission, the RCP
must be strictly achieved. This is ensured through compliance,
which provides the empirical proof that the real-time C2
link satisfies these rigorous operational states. Meanwhile,
allocation serves as the architectural process that breaks down
high-level, end-to-end mission requirements and distributes
them into specific performance envelopes across the entire
C2 ecosystem. To guarantee both precise allocation and
definitive compliance for reliable C2 communication, several
conventional mechanisms such as latency budget allocation
and stochastic verification are utilized to manage system
unpredictability and ensure total operational safety.

#### Meetings: Kerim & Terrence (SLAM), Tianxiong (risk), Ming (lines 529-584)

# Meeting with Kerim and Terrence 

Thesis 
Benchmarking SLAM algorithm 
ORB SLAM 3 

Kerim - SLAM , ORB SLAM 3
Integrate drone sensors to - Barometer , compass, IMU 
GNSS denied Autonomous system outside 
State of art 
- application- war, inspection , mines , Bridge inspection , hazards and disaster zones 
- communication - SLAM - used / made for indoor  - how to bring to outdoor 
- Swarm navigation - computed metrics SLAM 
- Map points - matrix transformation 
- One outdoor drone BArometer, compass, range finder - Factor graph 
- SLAM Scale error 
- all map points necessary?
- time stamped data 
- matrix compression 
- co-visibility 

----

# Tianxiong Meeting 


C2 outage lasting longer than T_LL”, where T_LL is the lost-link timer, or the 10 s window. Per cube: P(H) per entry = P(outage) × (1 − P(recovery within T_LL)) As a rate: λ_H,i = λ_i · (1 − P_rec,i(T_LL))


1. **Define the hazardous event H.** For example, “C2 outage lasting longer than T_LL”, where T_LL is the lost-link timer, or the 10 s window. Per cube: P(H) per entry = P(outage) × (1 − P(recovery within T_LL)) As a rate: λ_H,i = λ_i · (1 − P_rec,i(T_LL))
2. **Combine along a route.** For a route spending time t_i in cube i: P(H during flight) = 1 − Π exp(−λ_H,i · t_i) This turns the cube map directly into a route-level number for planning and for comparing candidate routes.
3. **Weight by severity.** Risk_i = P(H)_i × S_i, where S_i depends on what lies below or around the cube:
    - population density or ground risk class (the SORA ground-risk logic fits here)
    - air-risk class
    - distance to an emergency landing siteThe same outage probability then counts for more over a crowded area than over open land.
**Link to the Reliability Margin.** Per cube, the margin between mean SINR and the threshold, or between achieved and required availability, is a natural explanatory variable. Plotting risk against margin shows how much margin buys how much risk reduction.


4. Biparti graph 
5. Battery and communication  -> risk 
6. Successful rate 
7. Battery - where communication - cotrol
8. Mission complete rate 


Random oriaentation - position, ANtenna and speed - SNR - 69 points - outage

Other git 


----

# Ming Meeting 

1. Done IOT testbed 
2. Topics and Patents 

### From [[Nov 2026]]

#### Main info links (IAMSYM, IEEE) (lines 1-10)

# Main Info 

https://iamsym2026.dglr.de/fileadmin/iamsym2026/IAMSYM2026_20260817050421_abstr.pdf
https://iamsym2026.dglr.de/fileadmin/iamsym2026/IAMSYM2026_20260717074107_abstr.pdf
https://iamsym2026.dglr.de/fileadmin/iamsym2026/IAMSYM2026_20260717093240_abstr.pdf

Follow - https://ieeexplore.ieee.org/author/38234455800

https://www.ieee-jas.net/indexen.htm
https://standards.ieee.org/ieee/1954/10686/

#### U-space workshop call (lines 106-106)

https://uspace-workshop.github.io/2027/organization.html -  Work on this call 

#### AIAA forum track + risk-profile links (lines 193-208)

 AIAA Forum
Venue - which Topic 

Uncrewed and Autonomous Systems
Please direct questions to:
Srikanth Gururajan, Saint Louis University
Anaiya Reliford, Howard University

1. Abstract To dos 

https://gitlab.hrz.tu-chemnitz.de/shsr791g-at-tu-dresden.de/risk-profile/-/blob/main/out_window_1/post/cubes_10s.png?ref_type=heads 

out window 1 - 10 s outage
https://gitlab.hrz.tu-chemnitz.de/shsr791g-at-tu-dresden.de/risk-profile/-/blob/main/out_window/post/rec_cubes_10s.png?ref_type=heads - recovery

Main text and This tex

#### pyCirclize link (lines 249-249)

https://medium.com/@sy.41211/pycirclize-circular-visualization-in-python-b742ec5d45ac

#### Enrique feedback on CNS paper (lines 271-277)

enrique meeting - CNS paper

1. reading paper - final deliverable of a project rather than research contribution 
2. what is final output of research - not clear
3. proposed methods at first cross-domain - show what are future technologies 
4. what demonstrator consist about 
5. Make it clear whar is research output 

#### ASKey router notes (lines 282-291)

ASKey - router mode
IP pass through mode -

get access 
 uSB - A and C 
 magenta - 5G standalone mode 
admin - password 

USB dongle
Dsmeg 

#### Guest lecture: rare-event simulation for aviation safety (lines 296-343)

# Guest Lecture 

Rare event Simulation Methods for Aviation Safety 
 Prof Shortle 

commercial aviation safety

flying is extremely safe . fatal accidents 10 power 7 flight hours  - US part 121

overshoot tracks on runway 

common collision risk is prob of initiating data and modeling events 

input uncertainity 
small missed probabilities adds to risk 


computational complexity 

relative error of simulation 
important sampling  - might bias but using likelihood ratio

parallel tracks collision risk 

stochastic differential equation 
- every time stamp - add noise/ variability to the track 

Simulation - surrogate model - down the collision 

Aircraft flying are geometric elements - contributing to the risk 

Variable independent ? there is feature to capture dependency 

Algorithm: Cross- entropy 

standard deviation is 

important sampling is looking at rare events - tail is shifted 

**5 by 5 used by radio aviation users  - word play for 5G** 

splits and levels - vortex problem 

parameter sensitivity 

stratification 

total risk - probabilities of product 

### From [[2026]]

#### Publications 2026 + links to check (lines 1-20)

# Publications 2026

# Conference 
1. Reliability - AIAA Conf - OCt 2026
2. Deconfliction Algorithm - Sept 2026 
3. Service Migration - Oct 2026
4. https://www.hs-wismar.de/en/iiphdw/iiphdw-2027/call-for-papers/
# Journal 
1. Simulator IEEE Access - Dec 2026
2. Survey  Paper  - Dec 2026
# Milestones 

1. 5G and Satcom A2G flight tests 
2. Mesh nodes Flight test

# Check this 

1. https://sagroups.ieee.org/aercom/
2. https://ieeexplore.ieee.org/document/9080597
3. 

#### Deadline tables, journal links, conference visits (lines 115-176)

# Deadlines

# Conference - highlighted doubt

| Sub-deadline           | Conf                            | happen          | Location             | Content and Collaboration                        |
| ---------------------- | ------------------------------- | --------------- | -------------------- | ------------------------------------------------ |
| May/July               | DRCN                            | October  7-9    | cyprus               | RCP for UAV - tactical - C2 - Handover - Enrique |
| 31st Aug               | FNFW                            | October 20-23   | Portugal             | RCP - TN-NTN handover - Enrique                  |
| ==30th Aug/1st September== | ==VTC spring==                      | ==June 20-23 2027== | ==Hamburg (Germany)==    | ==A2G - Mesh  communication- Wifi Mesh - Own==       |
| 15th November          | DAUS/ARCI                       | Feb 2027 <br>   | Geneva (Switzerland) | Data Mesh - Edge-UTM - Own                       |
| 28th November          | ACM SIGGCOMM (Mobisys) - Dronet | June 2027       | Vietnam              | RIS - UAV communication - (Roshan, Enrique)      |
|                        | Dronecom 2027                   |                 |                      |                                                  |
|                        |                                 |                 |                      |                                                  |

Some more key conferences 
1. AIAA -https://www.aeroconf.org/key-dates | https://www.aeroconf.org/conference-organizers track 4.13
2.   AIAA Aviation Forum 
3. Digital Avionics Systems Conference (DASC 2027)
4. https://www.icin-conference.org/index.php/submissions/
# Journal 


| deadline        | Topic                       | Venue            | Context of the Journal and collaboration                                                   |
| --------------- | --------------------------- | ---------------- | ------------------------------------------------------------------------------------------ |
| Week 1 Aug 2026 |                             | IEEE Access      | INTANS simulator + Github repo opensource (Jiajing and Lyuqiao) and OSel                   |
| ==2027==        | ==A2G - Mesh, 5G, Satcom,== | ==Transactions== | ==one flight test location - diff drone pattern and altitude (Enrique, Roshan) - MAVLink== |
| DEC 2026        | A2G - Mesh, 5G, Satcom,     | dataport         | one flight test location - diff drone pattern and altitude (Roshan, Janna)                 |
| Oct 13          | Heterogenous Multilink      | NPJ              |  to prep methods                                                                           |

https://www.sciencedirect.com/journal/low-altitude-transportation/about/aims-and-scope

Other option: https://www.sciencedirect.com/special-issue/332625/selected-and-extended-papers-from-ieee-icdcn-2026-networking-track-guest-editor-simone-silvestri
https://www.sciencedirect.com/org/journal/drone-systems-and-applications/issues
https://www.worldscientific.com/worldscinet/us
https://www.sciencedirect.com/journal/low-altitude-transportation

Conference deadlines 
-  **15th April- EW** 
- **may 15th - DRCN ** 
- **June 25 - FNFW**
- **Aug 30- VTC spring** 
- July - CCNC / INFOCOM 
- Sp - SESAR innovation days
- OCt - WCNC 
- Nov - VTC spring, ICC
- DEC- EUCNC


Journal Deadlines 
- IEEE Access for simulator - Draft 1 - end May - Mid June 
- JSAC / VTS - A2A link - Mesh and Protocol + Data port - Dec 2026

# Conf Visits 2026

- [x] European Wireless
- [ ] FNWF


# Conf Visits 2027
- [ ] VTC
- [ ] ACM Sigcomm
- [ ] 

## 2027 (copied, originals unchanged in `07 TODOS/2027/`)

### From [[2027]]

#### Link (lines 1-1)

https://wos-journal.info/my

#### Venue research: journals/CFPs for UAV C2, conference links (lines 10-137)

I'll check the current calls for papers across the relevant journals on your list.

I checked the call-for-papers pages of the relevant journals on your list. The short answer is that no open themed special issue matches UAV C2 multi-link reliability exactly. The closest UAV and low-altitude calls closed in the last few weeks. Your best options are one open resilience special issue plus the regular tracks that accept submissions at any time.

**Open themed call that fits**

- **Reliability Engineering & System Safety, "Advanced resilience assessment & enhancement for complex engineering systems exposed to multi-hazards."** Submissions are open until 28 Feb 2027. The scope covers reliability and resilience quantification under cascading disruptive events, and AI-augmented resilience optimization. This is a natural home for your Reliability Margin work if you frame it as a UAV C2 system facing correlated or cascading link outages, such as a 5G coverage hole combined with SatCom blockage. The call is pitched at hazards like disasters, so you would need to argue that link degradation is the "hazard."

**Just closed, but worth an email to the guest editors**

- **IEEE VT Magazine, "Multifunctional Low-Altitude Wireless Networks for ITS."** This was the best match for you. Its topics included air-ground networking and security, reliability, simulations, and real-world deployments, with a deadline of 31 October 2026. VTM often extends its deadlines; its previous two calls were both marked as extended. Ask the guest editors directly whether submissions are still accepted.
- The other low-altitude special issues have closed: ComMag (Low-Altitude Wireless Networks, August 2026, closed), IEEE Network (Low-Altitude Wireless Network, November 2026, closed), IEEE Wireless Communications (Agentic AI-enabled networking for low-altitude unmanned systems, closed), and TVT (LAWN, deadline 1 March 2026).

**Regular tracks that fit your topics well**

- **IEEE TVT.** This is the strongest fit for 3GPP KPI evaluation of aerial UEs over 5G, SatCom and Wi-Fi with multipath or RLNC. It accepts regular submissions at any time.
- **IEEE TAES.** This fits best for the ICAO RCP versus 3GPP angle, since the aviation reviewers will appreciate it. It has no special issues, only occasional special sections, and none are currently listed, so you would submit as a regular paper.
- **IEEE Communications Magazine.** Its Open Call accepts any in-scope subject, and the Mobile Communications and Networks series runs periodically. This suits a high-level article on whether cellular plus SatCom can meet aviation C2 requirements.
- **IEEE AES Magazine.** Good for a tutorial-style article on C2 link performance requirements.
- **Vehicular Communications (Elsevier).** UAV is explicitly in scope.
- **IEEE TCOM.** Only if you have a strong analytical result on sliding-window or RLNC coding over heterogeneous links.

**Not a fit right now**

- **JSAC.** It accepts only submissions to a published call, and its only open calls are on underwater acoustics and the Quantum Series.
- **Wireless Communications and IEEE Network.** Their open special issues are on in-orbit computing, metasurfaces, foundation models and agent networks.
- **Digital Communications and Networks.** Its open call is on semantic communications.
- **IEEE Transactions on Reliability.** Its open special section is on software reliability engineering.
- **COMST.** Only relevant if you write a survey.
- **AIAA Journal.** Too far from networking.

My suggestion is to email the VTM guest editors this week. If the call is truly closed, target TVT for the multi-link and coding results, TAES for the RCP compliance analysis, and the RESS special issue for the Reliability Margin.

Sources:

- [IEEE ComMag CFP](https://www.comsoc.org/publications/magazines/ieee-communications-magazine/cfp)
- [IEEE JSAC CFP](https://www.comsoc.org/publications/journals/ieee-jsac/cfp)
- [IEEE Wireless Communications CFP](https://www.comsoc.org/publications/magazines/ieee-wireless-communications/cfp)
- [IEEE Network CFP](https://www.comsoc.org/publications/magazines/ieee-network/cfp)
- [IEEE VT Magazine](https://vtsociety.org/publication/vtmagazine/)
- [VTM Low-Altitude CFP](https://vtsociety.org/post/announcement/call-papers-multifunctional-low-altitude-wireless-networks-intelligent)
- [TVT LAWN Special Issue](https://vtsociety.org/post/announcement/call-papers-special-issue-low-altitude-wireless-networks-lawn)
- [IEEE TAES](https://ieee-aess.org/publications/taes)
- [RESS Multi-hazard Resilience CFP](https://servicesetu.org/call-for-paper/journals/ress)
- [TRel Software Reliability CFP](https://cyprusconferences.org/issre2026/wp-content/uploads/2026/05/TRel-CfP-Software-Reliability-Engineering-ISSRE2026.pdf)
- [DCN Call for Papers](https://www.keaipublishing.com/en/journals/digital-communications-and-networks/call-for-papers)
- [Vehicular Communications scope](https://www.myhuiban.com/journal/684.md)

# Deadlines 
1 . https://ieee-aess.org/files/ieeeaess/2026-05/cfp_lawn.pdf

# Conference
1. https://pimrc2027.ieee-pimrc.org/
2. https://meditcom2027.ieee-meditcom.org/
3. https://conf.researchr.org/track/issre-2027/issre-2027-papers#call-Call-for-Papers
# Journals 

Research targeting UAV Beyond Visual Line of Sight (BVLOS), Command and Control (C2), and Terrestrial Network / Non-Terrestrial Network (TN/NTN) integration is highly sought after. ==Because your topic explicitly targets reliability and resilience== (e.g., seamless handovers, 3GPP Rel-17/18 NTN standards, multi-connectivity, and backup satellite links during ground cellular outages), your paper spans across Telecommunications, Aerospace, and Intelligent Systems. [1, 2, 3, 4, 5, 6]

The top-tier Web of Science JCR Q1 journals that are the absolute best match for this specific multi-domain topic are categorized below:

## 1. The Ideal Fit: Aerospace + Telecom Systems

- [IEEE Transactions on Aerospace and Electronic Systems] (TAES)
    
    - Why it fits: TAES specifically oversees complex aerospace environments, Command and Control (C2) architectures, telemetry, and avionics. It is highly receptive to papers outlining how TN and NTN components act as redundant safety nets to maintain reliable, resilient drone navigation links.
    - Metrics: Q1 in Aerospace & Electrical Engineering | Impact Factor: 7.0.
    - Advantage: They recently shortened their review cycle timeline (initial reviews down to 45 days). [1, 5, 7, 8, 9, 10]
    
- [IEEE Transactions on Vehicular Technology] (TVT)
    
    - Why it fits: The primary hub for multi-network and integrated routing protocols. If your paper deals with the mathematical optimization of TN-to-NTN vertical handovers, dynamic link selection, or multi-connectivity to guarantee 99.999% reliability for a moving UAV, TVT is a core option.
    - Metrics: Q1 in Telecommunications | Impact Factor: 7.5. [11, 12]
    

## 2. High-Impact Telecom & Networking Frameworks

- [IEEE Internet of Things Journal] (IoT-J)
    
    - Why it fits: This journal frequently publishes research on "Internet of Drones" and aerial nodes operating within an NTN framework. It is perfect if your framework addresses resilience against cyber-physical failures, jamming, or predictive AI-based backup routing when switching between cellular gNBs and LEO satellite networks.
    - Metrics: Q1 | Impact Factor: 8.7 [1, 3, 6, 13]
    
- [IEEE Transactions on Wireless Communications] (TWC)
    
    - Why it fits: Best if your reliability and resilience framework relies on deep mathematical modeling (e.g., stochastic geometry to model NTN outage probability, Markov decision processes for adaptive link switching, or physical layer security for the C2 link).
    - Metrics: Q1 | Impact Factor: ca. 8.9 [3, 6]
    

## 3. Rapid Open Access (Fully JCR Q1)

- [IEEE Open Journal of vehicular Technology] (OJVT)
    
    - Why it fits: If you want a rapid-turnaround, fully Open Access paper that shares the high-prestige pool of TVT. It features a specific technical track for aerial and connected space-air-ground vehicles.
    - Metrics: Q1 | Impact Factor: 6.6
    

To help narrow down the ideal option, tell me a bit more about your methodology:

- Is your framework focused on physical/mathematical modeling (outage probabilities, beamforming), network routing/protocols (handovers, delay-tolerant networks), or system architecture (hardware-in-the-loop, 3GPP-aligned architecture)?
- What is your target timeline for publication?

  

[1] [https://www.researchgate.net](https://www.researchgate.net/publication/403624960_Connectivity-Resilient_Autonomous_Navigation_for_Beyond-Visual-Line-of-Sight_UAV_Systems)

[2] [https://ojs.iscram.org](https://ojs.iscram.org/index.php/Proceedings/article/download/148/121)

[3] [https://ieeexplore.ieee.org](https://ieeexplore.ieee.org/document/10001193/)

[4] [https://arxiv.org](https://arxiv.org/pdf/2208.02683)

[5] [https://www.researchgate.net](https://www.researchgate.net/publication/393274721_Reliable_and_Resilient_Connectivity_and_Coverage_under_Localized_Backhauling_in_UAV-IoT_Networks)

[6] [https://arxiv.org](https://arxiv.org/html/2604.17844v3)

[7] [https://ieee-aess.org](https://ieee-aess.org/publications/taes)

[8] [https://www.resurchify.com](https://www.resurchify.com/impact/details/17336)

[9] [https://journalsearches.com](https://journalsearches.com/journal.php?title=ieee%20transactions%20on%20aerospace%20and%20electronic%20systems)

[10] [https://ieee-aess.org](https://ieee-aess.org/post/announcement/enhancements-ieee-taes-streamlined-processes-and-increased-impact)

[11] [https://journalsearches.com](https://journalsearches.com/journal.php?title=ieee%20transactions%20on%20vehicular%20technology)

[12] [https://wos-journal.info](https://wos-journal.info/journalid/7018)

[13] [https://www.mdpi.com](https://www.mdpi.com/2504-446X/6/11/334)
