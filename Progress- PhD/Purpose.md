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

- **3GPP** (5G/6G, NTN, UAV communication
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
- 