// Dated 06.02.2026


Funnel Analogy
![[download.jpeg]]

- can be visualized like the above image 
- each layer contribute to the depth of my research 
- Layer 1 is getting general state of art in communication for BVLOS drone operations pertaining to VLL flights for medical cases - esp moving between the urban and peri urban region 
- This contains all the problems  in drone case (technical , economic and regulatory) and how we can solve them  - more from technical and regulatory 
###  First we talk about multi-link, why satcom is needed in this picture - what is the heterogeneous link architecture -A2A and A2G - technology
IDEA 
- Technology - wifi, satcom and 5G 
- SoA homogeneous - to - heterogeneous links
- A2 A and A2G link arcitecture 
ToDos
- [ ] Find and organize soA 
- [ ] Build the hypothesis - Write as an essay Chapter in my thesis doc 
- [ ] What are the factors building on it aka 2,3,4 anchor

### Second what is reliability and how the regulations work - ICAO and 3GPP conjuncture 
IDEA
- Disjoint 3GPP and ICAO
- Evaluate on Use-case basis ( Enrique collab)
- Evaluation Matrix 
- Map reliability, availability, tT - integrity based on security
ToDos
- [ ] Find the RCp and RLP and write a report and 3GPP points regulation
- [ ] Map my test methods and see how to address this 

### Third What is the current protocol and why it has issues 

IDEA 
- Link to be rilable UDP, TCP 
- Then HARQ matters 
- Size  BW requirements and latencyURLLC 
- Types of protocol STANAG , MAVLINK - what are issues of mavlink and how to adapt to the heterogenous links 
To Dos
- [ ] SOA
- [ ] How to build protocol
- [ ] How to i implement and test MAVLInk
### How to make this heterogeneous link work well - optimized

IDEA
- Physical and logical link parameters
- Network coding what to do to optimize
Todos
- [ ] NW coding notes, todos from Juan
- [ ] Implement stratergy and details 


### Publication plan 

1. **Tutorials -INTANS - summer 2026**
2. Transactions or open Journal - A2A, A2G - 2027 summer
3. **A2A mesh conf - 2026 Winter** 
4. **QoS - Enrique paper - before leaving klagenfurt conf** - DRCN
5. **Magazine QoS methods - summer end 2026**
6. **Protocol - Conference  end 2026**
7. Network coding conf - 2027 summer 
8. Network coding journal 2027 winter 

----


### NEWS


The "Quality-on-Demand" (QoD) API has become the industry-standard "throttle" for drone operators. In 2026, it is no longer just a pilot project; it is a commercialized tool available through major telco platforms like **GSMA Open Gateway**, **T-Mobile DevEdge**, and **Ericsson-owned Vonage**.

Developers use these APIs to solve a critical physics problem: cellular networks are traditionally designed for ground-level users (downlink-heavy), while drones are high-altitude users that require massive, stable **uplink** for 4K video and low-latency **command-and-control (C2)**.

### **1. Top QoD APIs for Drone Developers**

|**API Name**|**Provider**|**Primary Drone Use Case**|
|---|---|---|
|**CAMARA QoD API**|GSMA / Linux Foundation|Standardized across 50+ global telcos (Orange, Telefónica, Vodafone). Used for **BVLOS flight stability**.|
|**T-Mobile QoD - Remote Maneuvering**|T-Mobile US|Specifically tuned for **Remote Drone Maneuvering** with optimized jitter and latency for real-time control.|
|**Vonage Network API (QoD)**|Vonage (Ericsson)|Integrated with **C3 AI** and **Zuper** for industrial field services and automated drone inspections.|
|**Nokia Network as Code**|Nokia / DT|Uses geofencing to **automatically trigger** a QoD boost when a drone enters a specific flight corridor.|

---

### **2. How Developers Use These APIs in Flight**

Drones don't need "premium" speed 100% of the time. Developers use QoD APIs to request "bursts" of priority:

- **The "Emergency Boost":** If a drone’s AI detects a potential obstacle or a critical system error, the application calls the QoD API to instantly drop latency from ~100ms to **<20ms**, giving the pilot or autonomous system immediate control.
    
- **Congestion Bypass:** In a "best-effort" network (like a crowded city), drone video often stutters. The QoD API creates a **virtual "fast lane"** specifically for the drone's IMEI, ensuring the video stream doesn't drop even if thousands of people nearby are using 5G.
    
- **Multi-Channel Separation:** Advanced developers use APIs to separate traffic types. They might request a **High-Reliability** profile for telemetry (small data, zero loss) and a **High-Throughput** profile for the 4K sensor feed.
    

---

### **3. Major Industry Moves (Q1 2026)**

- **Skydio’s "Call to Action":** In late 2025, Skydio (the top US drone maker) officially requested that all Mobile Network Operators (MNOs) provide **aviation-authorized QoD APIs** to move the industry toward "Drones as Infrastructure."
    
- **The Postman Integration:** Vonage recently put these Network APIs onto the **Postman API Network** (reaching 40 million developers). This means a drone software startup can now "fork" a QoD collection and integrate cellular prioritization into their flight code in minutes.
    
- **AI-Agent Integration:** A major 2026 trend is **Agentic AI**. Autonomous flight agents now "negotiate" with the network via these APIs. For example, if an AI drone realizes it is running low on battery, it can call a QoD API to ensure its final landing video feed is perfectly stable for the remote supervisor.
    

---

### **4. Cost Model: "Priority as a Service"**

The financial model for these APIs has shifted. Telcos are moving away from flat monthly fees to:

- **Session-Based Pricing:** Pay $0.50 per 15-minute "QoD Session" during a high-stakes inspection.
    
- **Success-Based Pricing:** Pay only when the API successfully delivers the requested 99.9% reliability threshold.
    

**Would you like me to find a sample Python or JSON snippet showing how a developer actually "calls" a CAMARA QoD API to request a latency boost?**

----


System engineering 
https://www.nasa.gov/reference/2-0-fundamentals-of-systems-engineering/
https://www.eng.auburn.edu/~dbeale/ESMDCourse/Chapter2.htm

### Distinctions between Product Verification and Product Validation

From a process perspective, the Product Verification and Product Validation processes may be similar in nature, but the objectives are fundamentally different:

- Verification of a product shows proof of compliance with requirements—that the product can meet each “shall” statement as proven though performance of a test, analysis, inspection, or demonstration (or combination of these).
- Validation of a product shows that the product accomplishes the intended purpose in the intended environment—that it meets the expectations of the customer and other stakeholders as shown through performance of a test, analysis, inspection, or demonstration.

Verification testing relates back to the approved requirements set and can be performed at different stages in the product life cycle. The approved specifications, drawings, parts lists, and other configuration documentation establish the configuration baseline of that product, which may have to be modified at a later time. Without a verified baseline and appropriate configuration controls, later modifications could be costly or cause major performance problems.

Validation relates back to the ConOps document. Validation testing is conducted under realistic conditions (or simulated conditions) on end products for the purpose of determining the effectiveness and suitability of the product for use in mission operations by typical users. Validation can be performed in each development phase using phase products (e.g., models) and not only at delivery using end products.

It is appropriate for verification and validation methods to differ between phases as designs advance. The ultimate success of a program or project may relate to the frequency and diligence of validation efforts during the design process, especially in Pre-Phase A and Phase A during which corrections in the direction of product design might still be made cost-effectively. The question should be continually asked, “Are we building the right product for our users and other stakeholders?” The selection of the verification or validation method is based on engineering judgment as to which is the most effective way to reliably show the product’s conformance to requirements or that it will operate as intended and described in the ConOps.

https://medium.com/swlh/applying-the-systems-engineering-process-to-small-and-medium-sized-businesses-739125754590
https://www.microtool.de/en/knowledge-base/what-is-systems-engineering/#:~:text=It%20(%20Systems%20engineering%20)%20emerged%20in,alone%20could%20not%20handle%20the%20growing%20complexity. 

System Engineering V design - Enrique 
![[Screenshot from 2026-03-06 12-24-51.png]]


### Reliability: "The Ability to Not Fail"

Reliability is a measure of how consistently a system performs its intended function under specified conditions for a specific period. For a UAV, this means the link stays up and the data arrives correctly.

- **Key Metric:** Usually expressed as a probability (e.g., 99.999% or "five nines").
    
- **Focus:** Packet error rates, latency bounds, and signal-to-interference-plus-noise ratio (SINR).
    

### Resilience: "The Ability to Bounce Back"

Resilience is the system's capacity to withstand and recover from disruptions (like jamming, hardware failure, or extreme weather). A resilient system assumes something _will_ go wrong and has a plan to handle it.

- **Key Metric:** Recovery time (how fast does the link come back?) and graceful degradation (can the drone still fly if the video feed cuts out?).
    
- **Focus:** Redundancy, failovers, and adaptive rerouting.
    

---

## 2. 3GPP Standards and Definitions

The 3rd Generation Partnership Project (3GPP) provides the technical specifications for 4G (LTE) and 5G, which are increasingly used for UAV "Command and Control" (C2) and payload communication.

### 3GPP Definition of Reliability

In 3GPP TS 22.261 (Service requirements for the 5G system), reliability is defined as:

> _"The ability to deliver a specific amount of data from a source to a destination within a given time constraint with a success probability."_

For UAVs (specifically "Aerial UE"), the 3GPP Release 15 and 16 standards define **URLLC** (Ultra-Reliable Low-Latency Communications).

- **Standard Target:** $1 - 10^{-5}$ (99.999%) success probability for a 32-byte packet within 1ms user-plane latency.
    

### 3GPP Approach to Resilience

While 3GPP doesn't have a single "resilience coefficient," it addresses resilience through **Redundancy** and **Reliability Features**:

- **Dual Connectivity (Multi-connectivity):** The UAV connects to two base stations (gNBs) simultaneously. If one fails, the other takes over instantly.
    
- **Path Redundancy:** Sending the same data over two different radio paths.
    
- **Network Slicing:** Reserving a specific "lane" of the network specifically for UAV C2 traffic so it isn't disrupted by high-volume smartphone traffic nearby.
|**Organization**|**Term**|**Definition/Focus**|
|---|---|---|
|**ITU-T**|**Reliability**|The probability that an item can perform a required function under given conditions for a given time interval ($R(t)$).|
|**IEEE 802.11ax/be**|**Robustness**|Often used in place of resilience; focuses on maintaining links in "dense" environments with high interference.|
|**RTCA (DO-377A)**|**Continuity**|In aviation, this is the "resilience" of the link—the probability that the system will continue to perform its function without unscheduled interruption during an intended operation.| 

reliability can absolutely be addressed using ICAO terms. In fact, while **3GPP** focuses on the _technical performance_ of the radio link (packets and bits), **ICAO** focuses on the _operational performance_ of the entire communication chain (human-to-human or human-to-machine).

The ICAO framework for this is called **RCP (Required Communication Performance)**, detailed in _Doc 9869_.

|**ICAO Term (RCP)**|**3GPP Equivalent / Focus**|**Definition in UAV Context**|
|---|---|---|
|**Transaction Time**|**End-to-End Latency**|The total time from when a "Turn Left" command is sent until the drone actually acknowledges/executes it.|
|**Continuity**|**Reliability ($1 - \text{PER}$)**|The probability that the command gets through _within_ the Transaction Time. If it takes too long, it’s a continuity failure.|
|**Availability**|**Network Coverage / Uptime**|The probability that the link is actually "up" and usable when the pilot needs to initiate a command.|
|**Integrity**|**Residual Error Rate**|The probability that a command is corrupted (e.g., "Turn 10°" becomes "Turn 100°") without the system noticing.|
## Elements of Reliability (The "Why" and "How")

To achieve high reliability in a UAV system, engineers look at four key "elements." If any of these fail, the reliability of the system drops below the required "five nines" (99.999%).

### A. The Radio Link (Physical Layer)

This is the "strength" of the connection.

- **Signal Quality:** Maintaining a high **SINR** (Signal-to-Interference-plus-Noise Ratio) despite the UAV being high in the air where it "sees" too many towers at once (interference).
    
- **Fading Mitigation:** Using techniques like MIMO (Multiple Input Multiple Output) to handle signal reflections.
    

### B. The Protocol (Data Link Layer)

How the system handles lost data.

- **HARQ (Hybrid ARQ):** If a packet is lost, the system retransmits it instantly at the hardware level.
    
- **Redundancy:** Sending the same packet over two different frequencies or paths (e.g., Satellite + 5G).
    

### C. The Network (Architectural Layer)

Ensuring the "pipes" are clear.

- **Network Slicing:** 3GPP allows "slicing" a 5G network to give UAVs a dedicated, high-priority lane that isn't slowed down by people watching videos on the ground.
    
- **Handover Stability:** Ensuring the UAV doesn't lose the connection while moving quickly between different cell towers.
    

### D. The Human/Logic (Operational Layer)

The ICAO "Transaction" perspective.

- **Command Confirmation:** A reliable system must confirm the drone received the order.
    
- **Fail-safes:** If the reliability drops below a threshold (e.g., 2 seconds of no signal), the drone must trigger a "Resilience" behavior, like hovering or returning to base.
    

---

## 3. Key Difference in Mindset

- **3GPP** asks: _"What is the probability that this 32-byte packet arrives in 1 millisecond?"_
    
- **ICAO** asks: _"Can the pilot safely separate this drone from another aircraft given the current communication delay and success rate?"_
    

ICAO standards like **RCP 240** (meaning a 240-second maximum transaction time for oceanic flights) are being adapted for UAVs into much stricter "classes" (like RCP 0.1 or 0.4) because drones move and react much faster than a Boeing 747.


The shift toward **RCP 0.1** and **RCP 0.4** represents the "modernization" of aviation standards to fit the high-speed, high-density world of drones. While traditional oceanic flight uses **RCP 240** (allowing 4 minutes for a message transaction), a drone flying in an urban area would be long gone (or crashed) if it took 4 minutes to receive a "Stop" command.

---

## 1. RCP 0.1 and 0.4: The "Fast" Standards

The numbers in RCP (Required Communication Performance) refer to the **Expiration Time (ET)** in seconds.

- **RCP 400 / 240:** The "Legacy" standards. Used for long-range oceanic flight where planes are separated by miles.
    
- **RCP 0.4:** The command must be completed within **0.4 seconds** (400ms) with a 99.9% probability. This is often cited for tactical UAV operations in semi-controlled airspace.
    
- **RCP 0.1:** The command must be completed within **0.1 seconds** (100ms). This is the "Gold Standard" for high-density urban BVLOS (Beyond Visual Line of Sight) and package delivery, where reaction time is critical for collision avoidance.
    

### Comparison: ICAO RCP vs. 3GPP 5G URLLC

|Metric|ICAO RCP 0.1|3GPP 5G URLLC (Rel 16+)|
|---|---|---|
|**Target Time**|100ms (End-to-End)|1ms - 10ms (Radio Layer)|
|**Continuity**|99.9%|99.999%|
|**Availability**|99.99%|99.9% to 99.999%|
|**Context**|Human Pilot-to-UAV|Machine-to-Base Station|

---

## 2. Research Papers & Academic Discussion

There is a growing body of literature specifically bridging the gap between ICAO’s "Aviation Language" and 3GPP’s "Telecom Language."

### Key Paper Themes:

1. **Mapping 5G to RCP:**
    
    - _Reference:_ "Performance Analysis of 5G URLLC for UAV Command and Control." These papers often test if 5G can technically meet the "Continuity" requirements of RCP 0.1.
        
2. **The "Safety-Communication" Link:**
    
    - _Reference:_ "Towards a UAS Handling Qualities Specification" (NASA/FAA-related). These discuss how the **Transaction Time** (RCP) directly impacts the **Total System Error (TSE)** of the drone’s flight path.
        
3. **Multi-Link Resilience:**
    
    - _Reference:_ "Comparative Analysis of Multi-Link Selection Strategies for Next-Generation Aeronautical Communications" (2025/2026). This research focuses on using both Satellite (LEO) and 5G to ensure that if one link fails, the **Continuity** (RCP) is maintained.
        

### Notable Sources for Your Search:

- **ICAO Doc 9869 (PBCS Manual):** This is the foundation. It doesn't focus on drones specifically but defines the RCP framework.
    
- **RTCA DO-377A:** This is the "Minimum Aviation System Performance Standards" (MASPS) for C2 links. It effectively translates RCP into technical requirements for drone manufacturers.
    
- **EUROCONTROL Whitepapers:** Often discuss "U-Space" (the European UTM) and the need for sub-second latency (RCP 0.1–0.5) for urban drone traffic.
    

---

## 3. The "Elements of Reliability" in this Framework

When you combine ICAO and 3GPP, "Reliability" is composed of these measurable elements:

1. **Latency (Transaction Time):** The "speed" of the link.
    
2. **Success Rate (Continuity):** The "strength" of the link (Probability of success).
    
3. **Error Undetected (Integrity):** The "truth" of the link (protection against bit-flips or hacking).
    
4. **Uptime (Availability):** The "existence" of the link (is there a tower nearby?).
In modern engineering (and increasingly in 3GPP/ICAO discussions), these three elements form a cycle of protection:

### **Redundancy (The "Spare Tire")**

Redundancy is the presence of extra components or paths that aren't strictly necessary for basic function but provide a backup.

- **Spatial Redundancy:** Multiple antennas (MIMO) or multiple ground stations.
    
- **Frequency Redundancy:** Using both 2.4GHz (ISM) and 5G (C-Band) simultaneously.
    
- **Functional Redundancy:** Having both a cellular link and a satellite (LEO) link for the same UAV.
    

### **Robustness (The "Shield")**

This is the inherent "strength" of the system to resist change. A robust system doesn't need to "recover" because it didn't break in the first place.

- **Technical Element:** Using advanced **Channel Coding** (like Polar Codes in 5G) to "fix" corrupted data bits automatically.
    
- **UAV Context:** A robust link can handle the high-speed "doppler shift" (the change in frequency as a drone flies fast) without dropping the connection.
    

### **Recovery (The "First Aid")**

Recovery is the process of restoring service after a failure has occurred.

- **Self-Healing:** If a 5G cell tower goes down, the network automatically reroutes the UAV's data through a neighboring tower.
    
- **Re-acquisition Time:** How many milliseconds it takes for the drone to "re-handshake" with the ground station after a signal blackout.
    

---

## 2. Robustness in 3GPP vs. ICAO

The two standards bodies treat these "Three R's" with slightly different terminology:

|**Element**|**3GPP (5G Perspective)**|**ICAO (Aviation Perspective)**|
|---|---|---|
|**Redundancy**|**Multi-Connectivity / Dual Active:** The UAV is connected to two "cells" at once to avoid handover drops.|**Alternative Routing:** Using independent communication service providers (CSPs) to ensure no single point of failure.|
|**Robustness**|**URLLC (Ultra-Reliable):** High-power signaling and low MCS (Modulation and Coding Schemes) to ensure the signal cuts through noise.|**Integrity:** Ensuring the message isn't altered by interference and remains "trustworthy" for the pilot.|
|**Recovery**|**Radio Link Failure (RLF) Recovery:** Protocols to quickly re-establish a link before the drone enters a "failsafe" mode.|**Continuity:** The probability that the system recovers within the "Maximum Expiration Time" (e.g., the 0.1s in RCP 0.1).|

---

## 3. The "Robustness Cycle" in UAV Operations

To visualize how these elements interact during a flight:

1. **Normal State:** The system is **Reliable** (low packet loss).
    
2. **The Stressor:** The UAV flies behind a building (Shadowing).
    
3. **Robustness Kicks In:** The system uses its "Shield" (Channel Coding) to maintain the link despite the weaker signal.
    
4. **Redundancy Kicks In:** If the signal is too weak, the system flips to a secondary link (e.g., SatCom).
    
5. **Recovery:** Once the UAV clears the building, the primary high-speed 5G link is re-established within milliseconds.
    

---

## 4. Are there papers talking about this?

Yes. If you are looking for the intersection of **Robustness, Redundancy, and Recovery** in UAVs, I recommend searching for:

- **"Resilience-by-Design in Aerial Communication Networks"**: These papers often use the **R3 framework** (Robustness, Resiliency, and Reliability) to categorize 5G features.
    
- **"Cross-Layer Robustness for UAV Command and Control"**: This looks at how the physical radio layer (3GPP) affects the pilot's transaction time (ICAO).
    
- **"Adaptive Link Selection for BVLOS Operations"**: This covers the **Redundancy** aspect—how the drone chooses between different networks to maximize **Availability**.
https://mobile.aau.at/publications/hayat-2016-COMST-surveyUAV.pdf
