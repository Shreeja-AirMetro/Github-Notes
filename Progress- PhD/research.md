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
### Distinctions between Product Verification and Product Validation

From a process perspective, the Product Verification and Product Validation processes may be similar in nature, but the objectives are fundamentally different:

- Verification of a product shows proof of compliance with requirements—that the product can meet each “shall” statement as proven though performance of a test, analysis, inspection, or demonstration (or combination of these).
- Validation of a product shows that the product accomplishes the intended purpose in the intended environment—that it meets the expectations of the customer and other stakeholders as shown through performance of a test, analysis, inspection, or demonstration.

Verification testing relates back to the approved requirements set and can be performed at different stages in the product life cycle. The approved specifications, drawings, parts lists, and other configuration documentation establish the configuration baseline of that product, which may have to be modified at a later time. Without a verified baseline and appropriate configuration controls, later modifications could be costly or cause major performance problems.

Validation relates back to the ConOps document. Validation testing is conducted under realistic conditions (or simulated conditions) on end products for the purpose of determining the effectiveness and suitability of the product for use in mission operations by typical users. Validation can be performed in each development phase using phase products (e.g., models) and not only at delivery using end products.

It is appropriate for verification and validation methods to differ between phases as designs advance. The ultimate success of a program or project may relate to the frequency and diligence of validation efforts during the design process, especially in Pre-Phase A and Phase A during which corrections in the direction of product design might still be made cost-effectively. The question should be continually asked, “Are we building the right product for our users and other stakeholders?” The selection of the verification or validation method is based on engineering judgment as to which is the most effective way to reliably show the product’s conformance to requirements or that it will operate as intended and described in the ConOps.