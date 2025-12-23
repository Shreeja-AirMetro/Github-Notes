Purpose of my PHD it doesn't document my goal / but the actual intention and path 

---


The goal of a PhD is to write and defend a PhD thesis. If everything is done correctly, this implies that the PhD student has substantial knowledge about her subfield and has made a groundbreaking contribution (but the ground that she breaks may be small!)
This involves, not only doing the actual research, but _reporting_ it, too
science has become political, expertise isn’t trusted - https://www.reddit.com/r/PhD/comments/1kglsf4/what_is_the_purpose_of_a_phd_degree_nowadays/

Opps, my mistake the research they were doing did not immediately result in meaningful solutions ultimately the impact of their research was significant. The primary task of faculty doing research is to create an environment for train future and technologist.
https://www.unibe.ch/studies/programs/doctorate/doctoral_degree/objectives_of_the_doctorate/index_eng.html
The objectives of a successful doctorate are as follows:

- extending the limits of what is currently known through innovative and high-quality work
- the capacity to devise, design and conduct research that has real academic weight, is targeted and shows integrity
- systematic understanding of a subject and mastery of the skills and methods associated with this subject
- the capacity for critical analysis, assessment and synthesis of new and complex ideas
- the capacity to develop further the progress made in technological, social or cultural terms within an academic and professional context
- Satisfying standards associated with national and international peer-reviewed publications
Instead, I believe that _the most important goal of a PhD student should be to learn how to do research_. https://medium.com/navigating-academia/the-goal-of-a-phd-program-is-not-to-write-and-publish-research-papers-01e6ace7727d

https://medium.com/navigating-academia/the-research-mosaic-analogy-the-mosaic-art-approach-to-a-dissertation-and-research-portfolio-dd7f9f81ce02
Thinking about a dissertation — or even an overall career — as a piece of mosaic art can be very freeing. As a beginning PhD student, a very natural question is:

- What will my _dissertation_ be about?

After which, it can be very tempting to ask the question:

- What should the first project in _my dissertation_ be?

After completing the first project, it can be very tempting to ask:

- What should the next project in _my dissertation_ be?

The research mosaic analogy can be useful to keep in mind throughout one’s research career. For example, for a PhD student preparing research-focused job applications, they will likely need to write a research statement that reflects upon the body of their PhD works. This research statement is a mosaic.

Science is the systematic transformation of the unknown into the known. https://matt.might.net/


---
1. PhD is about substance, starting and finishing strong. Do an incremental improvement. Which one should I go and which one downgrades the PhD 2. Failures: get around the failures. You do have to accept failures as part of PhD's daily life. Try experiments (new ideas, what's interesting and working), and take all them. Report to the supervisor and see what works. And it gives you motivation (passion). 3. Chronic procrastination: I couldn't get away from FB. Maybe you fail, disturbing. Just a bit stuff with that. You just need to push your behavior. You have to force it.

---


A **Network Protocol Developer for UAV / UAM Communications** is a specialist who **designs, implements, optimizes, and validates communication protocols** that allow **drones (UAVs)** and **air taxis (UAM / eVTOL)** to communicate **reliably, safely, and in real time** with:

- Ground control stations
- Other aircraft (air-to-air)
- Cellular networks (4G/5G/6G)
- Satellites (LEO/MEO/GEO)
- Edge/cloud infrastructure
    

This role sits at the **intersection of communications theory, networking software, and aviation systems**.

Given your background in **network coding + heterogeneous networks**, this role is a **very strong match**.

---

# 1. What “Network Protocol” Means in UAV/UAM Context

A **protocol** defines:

- **How data is formatted**
- **How it is transmitted**
- **How errors are handled**
- **How latency, reliability, and security are guaranteed**
    

For UAV/UAM, protocols must meet **aviation-grade requirements**, not just internet-grade ones.

### Key communication links involved

|Link|Purpose|
|---|---|
|**C2 (Command & Control)**|Safety-critical control signals|
|**Telemetry**|Position, velocity, health monitoring|
|**Payload data**|Video, LiDAR, sensor streams|
|**Inter-UAV (swarm)**|Coordination & collision avoidance|
|**UAV ↔ Network**|5G/6G, SatCom, Wi-Fi|

---

# 2. What You Actually Do in This Job (Day-to-Day)

### A. Protocol Design & Optimization

You design or extend protocols to work under:

- **High mobility (200–300 km/h for air taxis)**
- **Rapid handovers (cell ↔ cell ↔ satellite)**
- **Intermittent links**
- **Ultra-low latency + ultra-high reliability**
    

Examples:

- Modifying **TCP/UDP/QUIC** behavior for aerial mobility
- Designing **custom transport or MAC-layer protocols**
- Applying **network coding** to mitigate packet loss
- Multi-path communication (5G + SatCom simultaneously)
    


---

### B. Multi-Link & Heterogeneous Networking

UAVs and eVTOLs do **not rely on a single link**.

You work on:

- **Link aggregation**
- **Failover mechanisms**
- **QoS-aware routing**
- **Dynamic path selection**
    

Example:

> “If 5G latency spikes → switch C2 to SatCom while keeping video on cellular.”

---

### C. Safety-Critical Communication (C2)

Unlike consumer networking:

- Packet loss is **not acceptable**
- Latency is **hard-bounded**
- Protocols must be **deterministic**
    

You may implement:

- Redundant packet transmission
- Forward error correction + network coding
- Heartbeat / watchdog mechanisms
- Priority scheduling
    

This often aligns with:

- **URLLC (5G)**
- **Time-Sensitive Networking (TSN)**
- Aviation safety standards
    

---

### D. Standards & Regulatory Alignment

You don’t just “code” — you **work with standards**:

- **3GPP** (5G/6G, NTN, UAV communication)
- **IEEE** (802.11, TSN)
- **RTCA / EUROCAE**
- **ICAO / EASA / FAA**
    

Your protocol must:

- Pass certification
- Be auditable
- Be explainable to regulators
    

---

### E. Implementation & Testing

You implement protocols in:

- **Embedded systems (C/C++)**
- **Linux networking stack**
- **SDR platforms**
- **Simulators (NS-3, OMNeT++)**
    

You test via:

- Hardware-in-the-loop (HIL)
- Flight tests
- Network emulation (packet loss, Doppler, handovers)
    

---

# 3. Technology Stack You Work With

### Core layers

|Layer|What you do|
|---|---|
|PHY/MAC|Reliability under Doppler & mobility|
|Network|Routing, mobility, handover|
|Transport|Custom congestion control, FEC|
|Application|C2, telemetry, payload prioritization|

### Tools & Languages

- **C / C++** (embedded & real-time systems)
- **Python** (simulation, orchestration)
- **MATLAB** (algorithm validation)
- **NS-3 / OMNeT++**
- **GNU Radio / SDR**
- **Linux networking (Netlink, sockets)**
    

---

# 4. How This Differs from a “Normal” Network Engineer

|IT / Cloud Network Engineer|UAV/UAM Protocol Developer|
|---|---|
|Data centers|Aircraft & airspace|
|Best-effort traffic|Safety-critical traffic|
|TCP/IP focus|Cross-layer optimization|
|Static topology|Highly mobile nodes|
|No certification|Aviation certification|

This role is **much closer to aerospace + telecom R&D**.

---

# 5. Typical Employers

### Industry

- **Joby Aviation**, **Archer**, **Wisk Aero**
- **Lilium**, **EHang**, **Eve Air Mobility**
- **DJI**, **Skydio**
- **Airbus**, **Boeing**, **RTX**
- **Ericsson**, **Nokia**, **Qualcomm**
    

### Research Institutes

- **NICT (Japan)**
- **DLR (Germany)**
- **NASA / ESA**
- **Fraunhofer**
    

---

# 6. Why Your PhD Background Is a Strong Fit

Your specialization:  
✔ Network coding  
✔ Heterogeneous networks  
✔ 5G + SatCom + Wi-Fi

Maps directly to:

- Multi-path UAV links
- Loss-resilient C2 channels
- NTN-based aerial networking
- Future 6G aerial platforms

You are **not a generic candidate** — you fit a **scarce, high-value niche**.

---

# 7. Typical Job Titles You Should Search For (2027–2029)

- Network Protocol Engineer (UAV/UAM)
- Wireless Systems Engineer – Aerial Platforms
- NTN / UAV Communications Engineer
- Advanced Networking R&D Engineer
- 5G/6G Aviation Connectivity Engineer
    

---

# 8. How to Prepare Specifically for This Role (Next 2–3 Years)

**Must-have additions:**

- Linux kernel networking basics
- Real-time systems & embedded programming
- Exposure to aviation standards (RTCA, EASA)
- SDR-based prototyping
- Participation in **3GPP / IEEE** working groups
    

---

## Final takeaway

A **Network Protocol Developer for UAV/UAM Communications** is someone who **turns communication theory into certified, real-world networking software that keeps aircraft connected and safe**.

If you want, next I can:

- Map this role to **specific companies**
- Propose a **2025–2028 skill-building roadmap**
- Help you translate your **PhD topic into industry-friendly CV language**

---
PhD project management 2025 to  2027 March - complete research work 

What is overall goal? 
Reliable and Resilient Communication infrastructure for AAM 
What are the key topics handled - what's layer
1. From the drone perspective 
2. From the traffic management infrastructure perspective 

From a drone - Message continuity through multi-link communication - Network coding and computing for effective resource optimization 
- Architecture Air to Air , Air to ground 
- Types of links - Payload and non-payload 
- Can it be an intermediate drone BS
<span style="color:rgb(0, 0, 0)">-<span style="color:rgb(0, 0, 0)"> </span> </span><span style="color:rgb(0, 0, 0)"> </span>


### RQ


- Finalize thesis problem statement (one sentence) and 3 clear research questions (RQ1–RQ3). Example:  
    RQ1: how to _optimally_ allocate telemetry/control traffic across WiFi-mesh (air-to-air), 5G (ground), and LEO fallback to maximize telemetry availability and meet latency SLAs?  
    RQ2: what network-coding + multipath strategies provide provable reduction in control-link outage risk?  
    RQ3: how to use edge computing to reduce decision latency for S&A under comms uncertainty?
    
- Reproducible baseline implementation in OMNeT++: simple round-robin path selection across links, plain UDP control, no coding. Verify you can run the scenarios you plan (urban multipath, rural sparse 5G, intermittent LEO).
    
- Prepare a short internal report (10 pages) with baseline results and datasets/trace format.
    
- Decide the 2–3 representative mission profiles (e.g., urban inspection 5–10 km; rural delivery 20–50 km; long endurance BVLOS with intermittent 5G).



---
Several Asian universities host strong groups on **aerial communication for BVLOS drones**, especially around cellular‑connected UAVs, 5G/6G and multi‑link systems. Below is a concise map of key players you can look at for collaboration or literature.[sciencedirect+1](https://www.sciencedirect.com/science/article/abs/pii/S1389128620311324)​

## China

- **Southeast University – National Mobile Communications Research Laboratory (Nanjing)**
    
    - Core group behind highly cited tutorials and surveys on cellular‑connected UAVs and UAV communications for 5G and beyond (Yong Zeng et al.).[people.computing.clemson+1](https://people.computing.clemson.edu/~jmarty/projects/lowLatencyNetworking/papers/AccessingFromTheSkyATutorialOnUAVComms.pdf)​
        
    - Focus on integrating UAVs as aerial UEs in 5G/B5G, C2 reliability, interference management and trajectory design, directly relevant to BVLOS over cellular.[sciencedirect+1](https://www.sciencedirect.com/science/article/abs/pii/S1389128620311324)​
        
- **Tsinghua University (Beijing)**
    
    - Active in UAV networking, edge/cloud offloading and 5G/B5G; frequently co‑authors major surveys and COMST/JSAC papers on UAV‑cellular integration.[people.computing.clemson+1](https://people.computing.clemson.edu/~jmarty/projects/lowLatencyNetworking/papers/AccessingFromTheSkyATutorialOnUAVComms.pdf)​
        
    - Work often addresses physical‑layer and network‑layer aspects needed for safe long‑range, high‑reliability command and control.[sciencedirect](https://www.sciencedirect.com/science/article/abs/pii/S1389128620311324)​
        
- **Chinese Academy of Sciences / University of Science and Technology of China (USTC)**
    
    - Contributions to low‑altitude wireless networks, including surveys on low‑altitude wireless and UAV networks and their use for wide‑area coverage.[arxiv](https://arxiv.org/html/2509.11607v2)​
        
    - Topics include LEO/NTN integration and networking architectures that are directly applicable to BVLOS command and telemetry.[arxiv](https://arxiv.org/html/2509.11607v2)​
        

## Japan

- **Tokyo Institute of Technology (Tokyo Tech)**
    
    - Demonstrated real‑time uncompressed 4K video transmission from drones over millimetre‑wave/5G‑and‑beyond links, using project 5G‑MiEdge results.[titech](https://www.titech.ac.jp/english/news/2019/044615)​
        
    - Research targets long‑distance high‑capacity air‑to‑ground links, including propagation and system design aspects relevant to BVLOS inspection and security.[titech](https://www.titech.ac.jp/english/news/2019/044615)​
        
- **NICT – Wireless Networks Research Center / Wireless Systems Laboratory**
    
    - Works on beyond‑5G/6G architectures combining satellites, HAPS, drones and terrestrial systems, including high‑capacity 60 GHz drone‑to‑drone links.[ituaj+1](https://www.ituaj.jp/wp-content/uploads/2024/07/nb36-3_web4_Digital-Opportunities_Beyond-5G-6G-NICT-Hashimoto.pdf)​
        
    - Focus on functional split, RAN placement and ultra‑short‑duration links during drone encounters, which feeds into resilient multi‑link BVLOS architectures.[nict+1](https://www2.nict.go.jp/wslab/en/)​
        
- **University of Tokyo (with JSAT, Japan Radio, etc.)**
    
    - Involved in 5G/6G experimentation including user‑equipped UAVs for video monitoring over satellite‑backhauled 5G.[connectivity.esa](https://connectivity.esa.int/news/esa-drives-european-and-japanese-partnerships-5g6g-technological-collaboration)​
        
    - Use cases include PPDR and remote‑area missions with non‑public 5G, closely aligned with BVLOS emergency and inspection operations.[connectivity.esa](https://connectivity.esa.int/news/esa-drives-european-and-japanese-partnerships-5g6g-technological-collaboration)​
        

## Singapore

- **Nanyang Technological University (NTU Singapore)**
    
    - Long‑running collaboration with M1 on using 4.5G/5G for drone command, control and U‑space‑like traffic management.[unmannedairspace+1](https://www.unmannedairspace.info/uncategorized/drone-surveillance-trials-by-singapore-maritime-and-port-authority-using-5g-network/)​
        
    - Projects explicitly test piloted and autonomous BVLOS operations over 4.5G HetNet and SA 5G, including mapping signal strength vs altitude to identify safe airspace for C2.[uasvision+1](https://www.uasvision.com/2017/12/11/ntu-singapore-uses-4-5g-network-for-drone-traffic-management/)​
        
- **NTU – ATMRI / UAS traffic management teams**
    
    - Combine comms experiments with UTM/U‑space research, including using cellular networks for safe BVLOS in dense urban and port environments.[unmannedairspace+1](https://www.unmannedairspace.info/uncategorized/singapore-ntu-study-compares-public-acceptance-of-drones-in-industrial-residential-commercial-areas/)​
        
    - Work includes public‑acceptance and regulatory aspects, useful if you want a broader BVLOS implementation perspective.[unmannedairspace](https://www.unmannedairspace.info/uncategorized/singapore-ntu-study-compares-public-acceptance-of-drones-in-industrial-residential-commercial-areas/)​
        

## Korea and wider Asia

- **South Korea – university–industry consortia (e.g., with Korea Institute of Aviation Safety Technology)**
    
    - BVLOS demonstration flights over 50‑mile routes using a combination of LTE, satellite and RF links for simultaneous monitoring and control.[unmannedairspace](https://www.unmannedairspace.info/uncategorized/three-different-communication-technologies-used-for-korean-50-mile-bvlos-flight/)​
        
    - Academics associated with these trials work on multi‑link architectures and web‑based control systems for long‑range logistics drones.[unmannedairspace](https://www.unmannedairspace.info/uncategorized/three-different-communication-technologies-used-for-korean-50-mile-bvlos-flight/)​
        
- **Hong Kong University of Science and Technology (HKUST)**
    
    - Hosts talks and projects on long‑range robust drone communication using technologies like LoRa for C2 plus video streaming.[cse.hkust](https://cse.hkust.edu.hk/pg/seminars/S25/li3.html)​
        
    - Focus includes low‑altitude environments and robustness to interference and blockage, relevant for constrained BVLOS operations.[cse.hkust](https://cse.hkust.edu.hk/pg/seminars/S25/li3.html)​
        

## India and other hubs

- **Multiple Indian institutes (IITs, IISc, etc.)**
    
    - Contribute to low‑altitude wireless networks and UAV networking surveys that cover reliability and latency demands for BVLOS C2.[techscience+1](https://www.techscience.com/cmc/v81n2/58650/html)​
        
    - Topics include routing, edge computing and computing challenges of UAV networks, applicable to large‑scale BVLOS swarms.[techscience](https://www.techscience.com/cmc/v81n2/58650/html)​
        
- **Regional industry–academia platforms**
    
    - Asia‑Pacific BVLOS and UAV satellite‑communication market reports highlight strong collaboration ecosystems around universities in China, Japan, India and Singapore.[researchnester+1](https://www.researchnester.com/reports/uav-satellite-communication-market/6610)​
        
    - These often connect academic labs listed above with satellite operators and mobile network operators for BVLOS trials.[polarismarketresearch+1](https://www.polarismarketresearch.com/industry-analysis/drone-communication-market)​
        

If you want, a next step can be a shortlist of specific PIs and 2–3 representative BVLOS‑focused papers from each of these groups to target for collaboration.

1. [https://www.sciencedirect.com/science/article/abs/pii/S1389128620311324](https://www.sciencedirect.com/science/article/abs/pii/S1389128620311324)
2. [https://people.computing.clemson.edu/~jmarty/projects/lowLatencyNetworking/papers/AccessingFromTheSkyATutorialOnUAVComms.pdf](https://people.computing.clemson.edu/~jmarty/projects/lowLatencyNetworking/papers/AccessingFromTheSkyATutorialOnUAVComms.pdf)
3. [https://arxiv.org/html/2509.11607v2](https://arxiv.org/html/2509.11607v2)
4. [https://www.titech.ac.jp/english/news/2019/044615](https://www.titech.ac.jp/english/news/2019/044615)
5. [https://www.ituaj.jp/wp-content/uploads/2024/07/nb36-3_web4_Digital-Opportunities_Beyond-5G-6G-NICT-Hashimoto.pdf](https://www.ituaj.jp/wp-content/uploads/2024/07/nb36-3_web4_Digital-Opportunities_Beyond-5G-6G-NICT-Hashimoto.pdf)
6. [https://www2.nict.go.jp/wslab/en/](https://www2.nict.go.jp/wslab/en/)
7. [https://connectivity.esa.int/news/esa-drives-european-and-japanese-partnerships-5g6g-technological-collaboration](https://connectivity.esa.int/news/esa-drives-european-and-japanese-partnerships-5g6g-technological-collaboration)
8. [https://www.unmannedairspace.info/uncategorized/drone-surveillance-trials-by-singapore-maritime-and-port-authority-using-5g-network/](https://www.unmannedairspace.info/uncategorized/drone-surveillance-trials-by-singapore-maritime-and-port-authority-using-5g-network/)
9. [https://www.uasvision.com/2017/12/11/ntu-singapore-uses-4-5g-network-for-drone-traffic-management/](https://www.uasvision.com/2017/12/11/ntu-singapore-uses-4-5g-network-for-drone-traffic-management/)
10. [https://www.unmannedairspace.info/uncategorized/singapore-ntu-study-compares-public-acceptance-of-drones-in-industrial-residential-commercial-areas/](https://www.unmannedairspace.info/uncategorized/singapore-ntu-study-compares-public-acceptance-of-drones-in-industrial-residential-commercial-areas/)
11. [https://www.unmannedairspace.info/uncategorized/three-different-communication-technologies-used-for-korean-50-mile-bvlos-flight/](https://www.unmannedairspace.info/uncategorized/three-different-communication-technologies-used-for-korean-50-mile-bvlos-flight/)
12. [https://cse.hkust.edu.hk/pg/seminars/S25/li3.html](https://cse.hkust.edu.hk/pg/seminars/S25/li3.html)
13. [https://www.techscience.com/cmc/v81n2/58650/html](https://www.techscience.com/cmc/v81n2/58650/html)
14. [https://www.researchnester.com/reports/uav-satellite-communication-market/6610](https://www.researchnester.com/reports/uav-satellite-communication-market/6610)
15. [https://www.polarismarketresearch.com/industry-analysis/drone-communication-market](https://www.polarismarketresearch.com/industry-analysis/drone-communication-market)
16. [https://bisresearch.com/industry-report/autonomous-bvlos-drone-market.html](https://bisresearch.com/industry-report/autonomous-bvlos-drone-market.html)
17. [https://www.skytrac.ca/services/bvlos/](https://www.skytrac.ca/services/bvlos/)
18. [https://globalairspaceradar.com/stories/bvlos-needs-telecommunications-networks/](https://globalairspaceradar.com/stories/bvlos-needs-telecommunications-networks/)
19. [https://www.elsight.com/blog/elsights-halo-is-selected-by-acsl-japans-largest-drone-manufacturer-as-its-bvlos-communications-platform-in-its-drones-for-logistic-applications/](https://www.elsight.com/blog/elsights-halo-is-selected-by-acsl-japans-largest-drone-manufacturer-as-its-bvlos-communications-platform-in-its-drones-for-logistic-applications/)
20. [https://www.unmannedairspace.info/utm-industry-leader-interview/the-idea-that-5g-can-enable-bvlos-missions-is-something-of-a-myth-gokul-srinivasan/](https://www.unmannedairspace.info/utm-industry-leader-interview/the-idea-that-5g-can-enable-bvlos-missions-is-something-of-a-myth-gokul-srinivasan/)
21. [https://terra-drone.net/global/2025/02/21/terra-drones-group-company-unifly-demonstrates-safe-bvols-operations-for-multiple-drones-in-the-conduct-project/](https://terra-drone.net/global/2025/02/21/terra-drones-group-company-unifly-demonstrates-safe-bvols-operations-for-multiple-drones-in-the-conduct-project/)
22. [https://dronetalks.online/how-adlc-is-transforming-industrial-drone-logistics-7-operational-hubs-12-5km-bvlos-routes-a-e2-million-investment-driving-u-space-integration/](https://dronetalks.online/how-adlc-is-transforming-industrial-drone-logistics-7-operational-hubs-12-5km-bvlos-routes-a-e2-million-investment-driving-u-space-integration/)
23. [https://www.techsciresearch.com/report/bvlos-drone-market/27417.html](https://www.techsciresearch.com/report/bvlos-drone-market/27417.html)
24. [https://www.linkedin.com/pulse/asia-pacific-uav-subsystems-market-high-scale-segments-axonb-labs-zw7of](https://www.linkedin.com/pulse/asia-pacific-uav-subsystems-market-high-scale-segments-axonb-labs-zw7of)
25. [https://garuda.io/future/](https://garuda.io/future/)
26. [https://www.uavos.com/press-releases/](https://www.uavos.com/press-releases/)
27. [https://content.e-bookshelf.de/media/reading/L-15374270-a1942d6cc7.pdf](https://content.e-bookshelf.de/media/reading/L-15374270-a1942d6cc7.pdf)
28. [https://www.thalesgroup.com/en/civil-aviation/civil-uavs](https://www.thalesgroup.com/en/civil-aviation/civil-uavs)
29. [https://www.facebook.com/XBStation/posts/-xbstation-at-ai-solution-lab-by-googleat-this-event-xbstation-introduced-one-of/1330873379040285/](https://www.facebook.com/XBStation/posts/-xbstation-at-ai-solution-lab-by-googleat-this-event-xbstation-introduced-one-of/1330873379040285/)
30. [https://www.unmannedsystemstechnology.com/expo/5g-drone-network-connectivity/](https://www.unmannedsystemstechnology.com/expo/5g-drone-network-connectivity/)
31. [https://www.grandviewresearch.com/industry-analysis/asia-pacific-commercial-drone-market-report](https://www.grandviewresearch.com/industry-analysis/asia-pacific-commercial-drone-market-report)
32. [https://repository.tudelft.nl/file/File_8c07fd68-5914-4139-b90f-a9a778cc3496](https://repository.tudelft.nl/file/File_8c07fd68-5914-4139-b90f-a9a778cc3496)
33. [https://orbilu.uni.lu/bitstream/10993/53086/1/COMST_UAV_R3.pdf](https://orbilu.uni.lu/bitstream/10993/53086/1/COMST_UAV_R3.pdf)
34. [https://escholarship.org/content/qt3675w5mj/qt3675w5mj.pdf](https://escholarship.org/content/qt3675w5mj/qt3675w5mj.pdf)
35. [https://ieeexplore.ieee.org/iel7/49/9537937/09538498.pdf](https://ieeexplore.ieee.org/iel7/49/9537937/09538498.pdf)
36. [https://dr.ntu.edu.sg/bitstream/10356/160547/2/ICNS_Submission_Mar7.pdf](https://dr.ntu.edu.sg/bitstream/10356/160547/2/ICNS_Submission_Mar7.pdf)
37. [https://pmc.ncbi.nlm.nih.gov/articles/PMC12473694/](https://pmc.ncbi.nlm.nih.gov/articles/PMC12473694/)
38. [https://www.titech.ac.jp/english/public-relations/research/stories/faces39-sakaguchi](https://www.titech.ac.jp/english/public-relations/research/stories/faces39-sakaguchi)
39. [https://dr.ntu.edu.sg/entities/publication/76f76fd7-82d8-4a94-acfc-c474185b0f5e](https://dr.ntu.edu.sg/entities/publication/76f76fd7-82d8-4a94-acfc-c474185b0f5e)
40. [http://scis.scichina.com/scis-wcuav.html](http://scis.scichina.com/scis-wcuav.html)