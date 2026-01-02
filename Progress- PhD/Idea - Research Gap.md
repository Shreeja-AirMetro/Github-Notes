###General 

## **Technical Paper Ideas for UAVs under the ITS Architecture and Design Topic**

---

### **1. Title:**

**"A Scalable Architecture for Integrating UAVs into Intelligent Transportation Systems: A UTM-ITS Convergence Approach"**

**Abstract Idea:**  
This paper presents a layered, modular architecture that integrates UAV traffic management (UTM) with existing intelligent transportation systems (ITS) for multi-modal coordination (air, road, water). It defines communication interfaces, control hierarchies, and data fusion strategies to support shared situational awareness across domains. The architecture is evaluated using simulations for urban traffic scenarios with autonomous ground vehicles and delivery drones.

---

### **2. Title:**

**"Edge-Centric ITS Architecture for Real-Time UAV Coordination and Emergency Response"**

**Abstract Idea:**  
This work proposes an edge computing-driven ITS architecture tailored to support UAV-based services (e.g., emergency medical delivery, traffic surveillance). The architecture incorporates local edge servers for low-latency control, AI-based route optimization, and UAV-to-infrastructure (U2I) communication. Case studies demonstrate reduced response time and improved coordination during simulated urban emergencies.

---

### **3. Title:**

**"Hybrid Air-Ground Intelligent Transportation System for Urban Mobility: Architectural Challenges and Solutions"**

**Abstract Idea:**  
This paper analyzes the architectural and systemic challenges of integrating low-altitude UAV operations with smart ground transportation in dense cities. A hybrid ITS-UTM framework is proposed, emphasizing airspace zoning, cooperative sensing, and V2X communication bridges. Emphasis is placed on managing interdependencies like shared weather data, real-time traffic congestion feedback, and coordinated dispatching.

---

### **4. Title:**

**"Blockchain-Enabled ITS Architecture for Secure and Decentralized UAV Traffic Management"**

**Abstract Idea:**  
This research introduces a blockchain-based ITS architecture that supports secure, transparent, and decentralized coordination among UAVs and ground control systems. The proposed design ensures immutable flight logging, smart contract-based access control for shared airspace, and traceable airspace violations. Performance and scalability are analyzed through simulations of urban UAV delivery networks.

---

### **5. Title:**

**"Cognitive ITS Architecture with Integrated UTM for Adaptive UAV Route Planning in Dynamic Environments"**

**Abstract Idea:**  
The paper presents a cognitive ITS framework that leverages machine learning and contextual reasoning to support adaptive flight path planning for UAVs in real-time. The architecture includes learning modules at both the edge and central layers, enabling prediction of congestion zones, airspace risks, and communication bottlenecks.

---

### **6. Title:**

**"Design and Evaluation of a Federated ITS Architecture for UAV Operations Across Jurisdictions"**

**Abstract Idea:**  
This study tackles the architectural challenges of UAV traffic management across multiple city or national jurisdictions. It proposes a federated ITS framework with interoperable communication protocols, shared control policies, and a unified API for policy enforcement and flight data exchange. The paper includes a prototype system and inter-jurisdictional simulation results.


----
WCNC

## Definition of Low-Altitude Communications and Networks

Low-altitude communications and networks refer to the systems and technologies that enable seamless connectivity, sensing, control, and data exchange among aerial vehicles (such as drones, unmanned aerial vehicles [UAVs], and electric vertical take-off and landing vehicles [eVTOLs]) and between these vehicles and ground infrastructure, typically within the airspace below 1,000 meters above ground level[1](https://arxiv.org/html/2506.13250v1)[2](https://arxiv.org/html/2506.12308v2)[3](https://arxiv.org/html/2505.04098v1). These networks are foundational to the rapidly growing "low-altitude economy," which encompasses a range of activities—like drone delivery, urban air mobility, surveillance, agriculture, and disaster response—operating in this lower segment of the atmosphere[4](https://www.tranmile.com/blog/Telecommunications/Telecommunications-and-Low-Altitude-Economy)[3](https://arxiv.org/html/2505.04098v1)[5](https://arxiv.org/html/2412.04074v2).

## Key Features and Architecture

**1. Three-Dimensional, Layered Network**

- Low-altitude wireless networks (often called LAWNs or LAINs) are designed as reconfigurable, 3D architectures that integrate aerial nodes (drones, UAVs, eVTOLs) and terrestrial nodes (ground stations, edge servers) to form a unified communication, sensing, and control platform[2](https://arxiv.org/html/2506.12308v2)[6](https://www.sciopen.com/article/10.7527/S1000-6893.2023.28809)[1](https://arxiv.org/html/2506.13250v1).
    
- The architecture typically consists of several tightly coupled functional planes:
    
    - **Data Plane:** Handles high-speed data transmission.
        
    - **Control Plane:** Manages real-time command and control, often with ultra-low latency and high reliability.
        
    - **Sensing Plane:** Enables environmental awareness and navigation through integrated sensing.
        
    - **Auxiliary Computing Plane:** Supports edge intelligence and distributed computing for mission-critical tasks[2](https://arxiv.org/html/2506.12308v2).
        

**2. Integrated Sensing and Communications (ISAC)**

- Modern low-altitude networks often combine wireless communication and radar sensing within the same infrastructure, improving spectrum utilization and enabling both navigation and surveillance functions simultaneously[5](https://arxiv.org/html/2412.04074v2)[2](https://arxiv.org/html/2506.12308v2)[3](https://arxiv.org/html/2505.04098v1).
    

**3. Multi-Platform Integration**

- These networks can incorporate terrestrial, aerial, and even satellite-based nodes to ensure wide coverage, including in remote or rural areas where terrestrial infrastructure may be lacking[3](https://arxiv.org/html/2505.04098v1)[6](https://www.sciopen.com/article/10.7527/S1000-6893.2023.28809).
    

## Distinguishing Characteristics

|Feature|Low-Altitude Networks (LAWN/LAIN)|Conventional Aerial/Terrestrial Networks|
|---|---|---|
|Coverage|3D, below 1,000 m (sometimes up to 3,000 m)|2D (ground) or high-altitude (above 3,000 m)|
|Node Types|UAVs, drones, eVTOLs, ground stations|Cell towers, satellites, aircraft|
|Functional Integration|Communication, sensing, control, computing|Primarily communication or sensing|
|Latency & Reliability|Ultra-low latency (<10ms), high reliability|Varies, often less stringent|
|Density|Can support 100+ aerial vehicles/km²|Lower density in aerial networks|
|Adaptability|Highly dynamic, self-organizing|More static, fixed infrastructure|

## Applications

- **Urban Air Mobility:** Air taxis, drone deliveries, and logistics[4](https://www.tranmile.com/blog/Telecommunications/Telecommunications-and-Low-Altitude-Economy)[3](https://arxiv.org/html/2505.04098v1).
    
- **Surveillance and Security:** Real-time monitoring of airspace and ground activities[5](https://arxiv.org/html/2412.04074v2)[2](https://arxiv.org/html/2506.12308v2).
    
- **Disaster Response:** Rapid deployment of aerial networks for search, rescue, and communication[2](https://arxiv.org/html/2506.12308v2).
    
- **Agriculture:** Crop monitoring, precision spraying, and environmental sensing[4](https://www.tranmile.com/blog/Telecommunications/Telecommunications-and-Low-Altitude-Economy).
    
- **Infrastructure Inspection:** Bridges, power lines, and pipelines[2](https://arxiv.org/html/2506.12308v2).
    

## Challenges

- **Spectrum Management:** Avoiding interference in crowded airspaces[6](https://www.sciopen.com/article/10.7527/S1000-6893.2023.28809)[1](https://arxiv.org/html/2506.13250v1).
    
- **Safety and Control:** Ensuring collision-free, reliable operations among massive numbers of vehicles[5](https://arxiv.org/html/2412.04074v2)[3](https://arxiv.org/html/2505.04098v1).
    
- **Coverage and Connectivity:** Maintaining seamless connections in dense urban or remote areas, sometimes requiring satellite integration[3](https://arxiv.org/html/2505.04098v1).
    
- **Resource Constraints:** Battery life, computing power, and bandwidth limitations[6](https://www.sciopen.com/article/10.7527/S1000-6893.2023.28809)[1](https://arxiv.org/html/2506.13250v1)[2](https://arxiv.org/html/2506.12308v2).
    

## Summary

Low-altitude communications and networks are the technological backbone of the emerging low-altitude economy, enabling safe, efficient, and intelligent operations for a wide range of aerial vehicles and applications in the airspace below 1,000 meters. These networks are characterized by their integration of communication, sensing, and control functions, their three-dimensional and adaptive architecture, and their ability to support dense, mission-critical aerial operations[1](https://arxiv.org/html/2506.13250v1)[2](https://arxiv.org/html/2506.12308v2)[3](https://arxiv.org/html/2505.04098v1).

1. [https://arxiv.org/html/2506.13250v1](https://arxiv.org/html/2506.13250v1)
2. [https://arxiv.org/html/2506.12308v2](https://arxiv.org/html/2506.12308v2)
3. [https://arxiv.org/html/2505.04098v1](https://arxiv.org/html/2505.04098v1)
4. [https://www.tranmile.com/blog/Telecommunications/Telecommunications-and-Low-Altitude-Economy](https://www.tranmile.com/blog/Telecommunications/Telecommunications-and-Low-Altitude-Economy)
5. [https://arxiv.org/html/2412.04074v2](https://arxiv.org/html/2412.04074v2)
6. [https://www.sciopen.com/article/10.7527/S1000-6893.2023.28809](https://www.sciopen.com/article/10.7527/S1000-6893.2023.28809)
7. [https://dl.acm.org/doi/10.1145/3712464.3712506](https://dl.acm.org/doi/10.1145/3712464.3712506)
8. [https://www.zte.com.cn/content/dam/zte-site/res-www-zte-com-cn/mediares/zte/%E6%97%A0%E7%BA%BF%E6%8E%A5%E5%85%A5/%E7%99%BD%E7%9A%AE%E4%B9%A6/Low_altitude_network_by_ISAC.pdf](https://www.zte.com.cn/content/dam/zte-site/res-www-zte-com-cn/mediares/zte/%E6%97%A0%E7%BA%BF%E6%8E%A5%E5%85%A5/%E7%99%BD%E7%9A%AE%E4%B9%A6/Low_altitude_network_by_ISAC.pdf)
9. [https://www.fierce-network.com/sponsored/integrated-sensing-communication-low-altitude-economy-tao-luo](https://www.fierce-network.com/sponsored/integrated-sensing-communication-low-altitude-economy-tao-luo)
10. [https://cdn.techscience.cn/files/CMES/2023/136-2/TSP_CMES_24078/TSP_CMES_24078.pdf](https://cdn.techscience.cn/files/CMES/2023/136-2/TSP_CMES_24078/TSP_CMES_24078.pdf)


---
2/7

There is **no single, definitive count** of how many researchers worldwide have published on topics such as **Advanced Air Mobility (AAM), Regional Air Mobility (RAM), Urban Air Mobility (UAM), drone operations, BVLOS (Beyond Visual Line of Sight), UAS (Unmanned Aircraft Systems), air taxis**, and associated keywords. However, several scientometric and meta-analytical studies provide insight into the scale and growth of research activity in these fields:

- **Urban Air Mobility (UAM):**  
    A meta-analysis covering January 2015 to June 2020 identified about **800 articles** in UAM, electric vehicles, and autonomous vehicles combined[1](https://www.sciencedirect.com/science/article/pii/S0968090X21003788).  
    More recent data shows a dramatic increase: in 2017, there were just **3 UAM publications globally** (all from the US), but by 2023, this number had grown to **426 UAM publications worldwide** in a single year, with significant contributions from the US, Germany, South Korea, the UK, and China[2](https://insights.pluto.im/research-trends-top-10-publications-in-uam/).
    
- **Drone Technology (including UAS, BVLOS, etc.):**  
    A scientometric analysis using Web of Science data found **3,433 publications** on drone technology between 1998 and 2017, with the annual output rising sharply in recent years of that period (e.g., 1,040 publications in 2017 alone)[3](https://digitalcommons.unl.edu/cgi/viewcontent.cgi?article=6366&context=libphilprac). The majority of these publications are collaborative, with research teams typically comprising 3–4 authors per paper.
    
- **Regional Air Mobility (RAM) and Advanced Air Mobility (AAM):**  
    These are newer subfields, often overlapping with UAM and drone research. For example, a NASA white paper on RAM had **21 contributing authors** from academia, government, and industry, reflecting the collaborative and interdisciplinary nature of the field[4](https://www.opp.purdue.edu/AAE/spotlights/2021/2021-0505RAM). However, the total number of unique researchers publishing specifically on RAM or AAM globally is not explicitly quantified in available literature.
    
- **Associated Keywords (BVLOS, air taxis, etc.):**  
    These topics are often embedded within the broader drone and UAM/AAM literature. The total number of researchers active in these areas would be a subset of those publishing on drone technology and UAM.
    

**Key points:**

- The number of unique researchers is difficult to estimate precisely due to overlapping authorship, co-authorship, and the interdisciplinary nature of the field.
    
- **Thousands of researchers** have contributed to the literature on these topics globally, with annual publication numbers in the hundreds to thousands depending on the specific area and timeframe[1](https://www.sciencedirect.com/science/article/pii/S0968090X21003788)[3](https://digitalcommons.unl.edu/cgi/viewcontent.cgi?article=6366&context=libphilprac)[2](https://insights.pluto.im/research-trends-top-10-publications-in-uam/).
    
- The field is experiencing **rapid growth**, especially since 2017, with global participation expanding beyond early leaders like the US and China to include Europe and other regions[2](https://insights.pluto.im/research-trends-top-10-publications-in-uam/).
    

Given the **overlap between these domains** and the collaborative nature of research, the number of unique individuals is likely in the **low thousands**, but the number of publications is much higher due to co-authorship and multiple papers per researcher. The **trend is sharply upward**, indicating increasing global research engagement in advanced and urban air mobility and related drone operations[1](https://www.sciencedirect.com/science/article/pii/S0968090X21003788)[3](https://digitalcommons.unl.edu/cgi/viewcontent.cgi?article=6366&context=libphilprac)[2](https://insights.pluto.im/research-trends-top-10-publications-in-uam/).

1. [https://www.sciencedirect.com/science/article/pii/S0968090X21003788](https://www.sciencedirect.com/science/article/pii/S0968090X21003788)
2. [https://insights.pluto.im/research-trends-top-10-publications-in-uam/](https://insights.pluto.im/research-trends-top-10-publications-in-uam/)
3. [https://digitalcommons.unl.edu/cgi/viewcontent.cgi?article=6366&context=libphilprac](https://digitalcommons.unl.edu/cgi/viewcontent.cgi?article=6366&context=libphilprac)
4. [https://www.opp.purdue.edu/AAE/spotlights/2021/2021-0505RAM](https://www.opp.purdue.edu/AAE/spotlights/2021/2021-0505RAM)
5. [https://escholarship.org/content/qt0656t0dh/qt0656t0dh.pdf](https://escholarship.org/content/qt0656t0dh/qt0656t0dh.pdf)
6. [https://www.sciencedirect.com/science/article/pii/S1361920924004280](https://www.sciencedirect.com/science/article/pii/S1361920924004280)
7. [https://escholarship.org/content/qt0656t0dh/qt0656t0dh.pdf?t=s8xyp8](https://escholarship.org/content/qt0656t0dh/qt0656t0dh.pdf?t=s8xyp8)
8. [https://www.semanticscholar.org/paper/Urban-air-mobility:-A-comprehensive-review-and-with-Garrow-German/6fd851b1e5db465661aa85b0acc6415016fb1d2b](https://www.semanticscholar.org/paper/Urban-air-mobility:-A-comprehensive-review-and-with-Garrow-German/6fd851b1e5db465661aa85b0acc6415016fb1d2b)
9. [https://mdpi-res.com/d_attachment/electronics/electronics-13-00340/article_deploy/electronics-13-00340.pdf?version=1705068336](https://mdpi-res.com/d_attachment/electronics/electronics-13-00340/article_deploy/electronics-13-00340.pdf?version=1705068336)
10. [https://www.ouvrirlascience.fr/excessive-growth-in-the-number-of-scientific-publications/](https://www.ouvrirlascience.fr/excessive-growth-in-the-number-of-scientific-publications/)
Based on available data from major publication databases and recent survey articles, there are **at least 1,000–1,500 peer-reviewed papers** globally as of July 2025 that focus on **5G (and beyond) communications for UAV operations in Advanced Air Mobility (AAM)**, published across IEEE, MDPI, Elsevier, and other leading journals and conferences.

**Supporting evidence:**

- **Survey and Review Papers:**  
    Recent survey articles on UAV communications for 5G and beyond routinely reference **dozens to over 100 primary research papers each**. For example, one 2021 survey on UAV-assisted 5G and beyond wireless networks cites more than 100 relevant studies, and similar surveys on related topics (placement optimization, mmWave, B5G/6G, etc.) each aggregate dozens more[1](https://www.sciencedirect.com/science/article/pii/S1570870524000519).
    
- **Breadth of Topics:**  
    The field covers a wide range of research areas, including:
    
    - UAV integration with 5G/6G networks
        
    - Cellular-connected UAVs
        
    - UAV placement and trajectory optimization for communications
        
    - Millimeter-wave and IoT applications
        
    - Experimental and prototype platforms (e.g., 5G Aero)[2](https://arxiv.org/abs/2506.08386)
        
    - Urban Air Mobility use cases and requirements[3](https://www.mdpi.com/2504-446X/7/9/556)
        
- **Database and Journal Activity:**
    
    - IEEE Xplore, MDPI, ScienceDirect, and similar databases each list **hundreds of articles** with keywords such as "UAV," "5G," "AAM," and "communication" published in the past five years.
        
    - For instance, TU Dortmund's CNI group alone lists dozens of relevant publications in the past few years[4](https://cni.etit.tu-dortmund.de/research/publications/).
        
- **Growth Trend:**
    
    - The number of papers is growing rapidly, with new special issues, conference tracks, and journal articles appearing every month.
        

**Approximate global count (as of July 2025):**

|Database/Publisher|Estimated Papers on 5G/UAV/AAM Communication|
|---|---|
|IEEE Xplore|500–700|
|MDPI|100–200|
|Elsevier/ScienceDirect|100–200|
|Springer, Wiley, arXiv, others|200–400|
|**Total (approx.)**|**1,000–1,500**|

**Note:**

- This estimate is based on publication counts from survey references, database queries, and visible trends in the field[1](https://www.sciencedirect.com/science/article/pii/S1570870524000519)[2](https://arxiv.org/abs/2506.08386)[3](https://www.mdpi.com/2504-446X/7/9/556)[4](https://cni.etit.tu-dortmund.de/research/publications/).
    
- The number is increasing quickly as AAM and 5G/6G integration become more central to both academic and industry research.
    

**In summary:**  
There are **at least 1,000–1,500 peer-reviewed papers worldwide** as of July 2025 focusing on 5G and other advanced communications for UAV operations in AAM, with the number growing steadily each year[1](https://www.sciencedirect.com/science/article/pii/S1570870524000519)[2](https://arxiv.org/abs/2506.08386)[3](https://www.mdpi.com/2504-446X/7/9/556)[4](https://cni.etit.tu-dortmund.de/research/publications/).

1. [https://www.sciencedirect.com/science/article/pii/S1570870524000519](https://www.sciencedirect.com/science/article/pii/S1570870524000519)
2. [https://arxiv.org/abs/2506.08386](https://arxiv.org/abs/2506.08386)
3. [https://www.mdpi.com/2504-446X/7/9/556](https://www.mdpi.com/2504-446X/7/9/556)
4. [https://cni.etit.tu-dortmund.de/research/publications/](https://cni.etit.tu-dortmund.de/research/publications/)
5. [https://www.sciencedirect.com/science/article/pii/S2405896324004683](https://www.sciencedirect.com/science/article/pii/S2405896324004683)
6. [https://www.grandviewresearch.com/industry-analysis/5g-aviation-market-report](https://www.grandviewresearch.com/industry-analysis/5g-aviation-market-report)
7. [https://www.easa.europa.eu/sites/default/files/dfu/uam-full-report.pdf](https://www.easa.europa.eu/sites/default/files/dfu/uam-full-report.pdf)
8. [https://elib.dlr.de/205131/1/Pak%202024%20Can%20Urban%20Air%20Mobility%20become%20reality.pdf](https://elib.dlr.de/205131/1/Pak%202024%20Can%20Urban%20Air%20Mobility%20become%20reality.pdf)
9. [https://arxiv.org/html/2506.08386](https://arxiv.org/html/2506.08386)
10. [https://www.mdpi.com/2504-446X/9/6](https://www.mdpi.com/2504-446X/9/6)


Here’s a clear breakdown of the **State-of-the-Art (SoA)**, **open topics & gaps**, and **acceptance potential** for your proposed survey or Transactions paper on **Multilink**, **UTM**, and **Aerial Communication** in IEEE venues:

---

## 📚 1. State‑of‑the‑Art Summary

### ✅ A) **Multilink & Multi‑Connectivity for UAS/Aerial Systems**

- Multi‑link communications (e.g., combining multiple cellular networks) offer **redundancy and highly reliable connectivity**, achieving up to **99.8 % availability** in maritime UAV SAR applications ([mdpi.com](https://www.mdpi.com/2504-446X/9/6/401?utm_source=chatgpt.com "Communication Infrastructure Design for Reliable UAV Operations ...")).
    
- However, single-cell or single‑tech solutions fall short under diverse conditions.
    
- Surveys (e.g., FACOM) stress that **no single wireless technology suffices**; integrated multi‑technology architectures (e.g. LTE + 5G + mmWave) are critical ([arxiv.org](https://arxiv.org/abs/2111.04175?utm_source=chatgpt.com "A Survey of Wireless Networks for Future Aerial COMmunications (FACOM)")).
    

### ✅ B) **UAS Traffic Management (UTM)**

- Developed frameworks on **UTM/U‑Space**, including architectures, services (flight planning, C2, conflict detection), and field demos (NASA TCL‑4, FAA pilot programs) ([mdpi.com](https://www.mdpi.com/2226-4310/7/7/85?utm_source=chatgpt.com "Fundamental Elements of an Urban UTM - MDPI")).
    
- Communication infrastructure within UTM includes CNPC links and handoff between operators and UTMs.
    
- Various country initiatives (USA, EU, Korea, Japan) have progressed to flight tests, albeit communication resilience remains a challenge ([researchgate.net](https://www.researchgate.net/publication/353743770_A_Survey_of_Wireless_Networks_for_Future_Aerial_Communications_FACOM?utm_source=chatgpt.com "(PDF) A Survey of Wireless Networks for Future Aerial ...")).
    

### ✅ C) **Aerial Communication Technologies**

- Surveys cover **mmWave beamforming**, **multi‑technology SAGIN**, **BVLOS eVTOL connectivity**, etc. ([mdpi.com](https://www.mdpi.com/2079-9292/13/2/340?utm_source=chatgpt.com "Enabling Technologies for the Navigation and Communication of ...")).
    
- Emerging standards (3GPP for UAS CNPC/UTM) are still in early R&D – signaling an architectural and protocol gap .
    

---

## 🕵️‍♂️ 2. Open Topics & Research Gaps

|Topic|Gap / Challenge|
|---|---|
|**Quantitative Frameworks for Redundancy**|Beyond qualitative studies, there's a lack of **systematic models** (e.g., Markov chains) comparing multi-link strategies under real UTM corridor constraints ([mdpi.com](https://www.mdpi.com/2504-446X/9/6/401?utm_source=chatgpt.com "Communication Infrastructure Design for Reliable UAV Operations ...")).|
|**Seamless Handover Across Networks**|UTM needs reliable **handoff between network domains**, including cell, USS, and UTM systems—few field studies exist.|
|**Integrated Architecture for UTM & Multi‑Connectivity**|Present UTM architectures often assume single CMD/C2 links—co-designed architectures for **multi‑link redundancy** are underdeveloped.|
|**Security in Multi‑link and UTM Communications**|Cryptographic authentication for CNPC links, joint sensing & communication, and secure UTM data exchange is under-explored .|
|**5G/6G, mmWave & SAGIN Integration**|Real deployment challenges—antenna design, beam tracking, latency—for mmWave-enabled air mobility systems need deeper investigations .|
|**Standardization and Protocol Gaps**|3GPP architecture definitions for UAS and UTM are still evolving—opportunities for contributions at an architectural or protocol level .|
|**Real Deployments and Testbeds**|Few works combine **simulation + testbed validation** across multi-link, security, and UTM domains.|

---

## 🔃 3. Potential Paper Scopes & Acceptance

### A) **Journal of Selected Areas in Communications (JSAC)**

- A **survey** combining **multi‑link aerial connectivity**, **UTM communication services**, and **security** around emerging standards would fit well.
    
- Ensure you synthesize architectures, field test results, standards, and identify **open problems** like handover, redundancy modeling, and secure CNPC.
    

### B) **IEEE Transactions on Communications / Wireless Communications**

- For an **original Transactions**: propose a **quantitative model or prototype** (e.g., Markov‑chain-based evaluation of multi‑link redundancy in UTM corridors), validated through simulation or testbed.
    
- Add a **security/authentication layer** or handoff mechanism between networks.
    

### C) **IEEE Communications Surveys & Tutorials**

- A full survey/tutorial weaving **multi‑technology aerial links**, **UTM communication infrastructure**, and **secure protocols** would be timely and valuable.
    
- Include taxonomy: technologies (2G/3G/4G/5G/mmWave/SAT), redundancy approaches, architectures (SAGIN), UTM services, standards (3GPP), and security frameworks.
    

---

## 🚀 4. Likelihood of Acceptance & How to Boost It

1. **Timeliness**: Niche area with growing industrial/academic interest.
    
2. **Publication Strategy**:
    
    - **Survey paper** → strong fit for COMST or JSAC as tutorial-style with taxonomy and gap analysis.
        
    - **Research paper** → propose and analyze a **quantitative multi‑link model in real UTM corridor settings**; validated with data or simulations.
        
3. **Novelty**: Highlight combination of **redundancy modeling**, **handover**, and **security** in UTM context—less addressed in existing literature.
    
4. **Validation**: Use open UAV testbeds or public NASA/FAA datasets where possible.
    
5. **Standards Alignment**: Link to 3GPP UAS CNPC and UTM standard roadmaps; show how your work aligns or supports those.
    

---

## 📝 Summary & Next Steps

- **SoA**: Strong qualitative grounding but limited quantitative frameworks.
    
- **Gaps**: Analytics for redundancy/handover/security in real-world UTM corridors; protocol/architecture gaps in standards.
    
- **Paper Potential**: Good for COMST; very feasible for JSAC/Transactions with a solid modeling or testbed component.
    
- **Next**: Define precise scope—e.g., "Queueing/Markov model for CNPC handover in multi-link SAGIN UTM corridors with security overhead."
    

---

Would you like help drilling into a specific angle—say, developing the modeling framework, mapping to standards, or building a taxonomy?

- **Comprehensive, in-depth surveys or tutorials**
- Emphasis on **taxonomies, classification, comparison**, and **future directions**
- Targeted at **both newcomers and advanced researchers**

Given your interest in **Multilink**, **UTM (UAS Traffic Management)**, and **Aerial Communications**, here's an analysis of the **potential of your topic as a survey paper** — specifically for **IEEE Communications Surveys & Tutorials (COMST)**:

---

## ✅ **1. Suitability for IEEE COMST**

### 🎯 IEEE COMST Focus:

- **Comprehensive, in-depth surveys or tutorials**
    
- Emphasis on **taxonomies, classification, comparison**, and **future directions**
    
- Targeted at **both newcomers and advanced researchers**
    

Your topic aligns very well with COMST because:

|Aspect|Evaluation|
|---|---|
|**Timeliness**|✔️ High — aerial communications and UTM systems are emerging fast with 5G/6G and drone integration|
|**Novelty**|✔️ Moderate to High — no unified survey deeply covering **multi-link + UTM + security + standardization**|
|**Technical Depth**|✔️ Strong — opportunity to explore network architectures, performance tradeoffs, redundancy models|
|**Breadth for Tutorial Value**|✔️ Strong — readers from multiple domains (wireless, aviation, edge computing) can benefit|
|**Availability of Literature**|✔️ Sufficient — growing number of papers in IEEE, 3GPP, NASA, ETSI, etc.|
|**Gap in Existing Surveys**|✔️ Strong — most existing surveys treat these **as isolated topics**, not integrated|

---

## 🧠 **2. What Your Survey Should Focus On**

Here’s a structure that would make your survey **highly attractive** to IEEE COMST reviewers:

### **Title Suggestion**

> _“Multi-Link Communications for Aerial Networks and UTM: Architectures, Challenges, and Future Directions”_

### **Proposed Structure**

1. **Introduction**
    
    - Motivation (reliability, UTM integration, 5G/6G role    
    - Contributions of the paper
    - Methodology (how you gathered/labeled the literature)
2. **Background & Foundations**
    
    - Aerial communication basics
    - UTM architecture overview (FAA, NASA, EU U-space)
    - Overview of multi-link and multi-connectivity concepts
3. **Taxonomy and Classification**
    
    - By link technology: LTE, 5G, mmWave, satellite, V2X
    - By mobility: low-altitude (UAV), high-altitude (HAPS), space-based
    - By UTM service (e.g., strategic deconfliction, tactical conflict detection)
4. **Survey of State-of-the-Art**
    
    - Communication models (point-to-point, multi-hop, SAGIN)
    - Reliability and redundancy mechanisms
    - Link handoff and load balancing
    - Use of SDN/NFV in managing multi-link UTM systems
    - Real-world deployments and testbeds
        
5. **Security & Privacy Aspects**
    
    - CNPC link protection
    - Data privacy in UTM systems
    - Challenges in multi-link security (e.g., trust across domains)
6. **Standards and Industry Efforts**
    
    - 3GPP Rel-16/17 UAS features
    - FAA, NASA, ETSI, ITU contributions
7. **Comparative Tables**
    
    - Existing systems vs. research prototypes
    - Protocol-level comparisons
    - Strengths and limitations of current work
        
8. **Open Research Challenges**
    
    - Seamless vertical/horizontal handovers
    - Network slicing for UAS/UTM integration
    - AI for dynamic link selection and mobility prediction
    - Integration with 6G and NTN (non-terrestrial networks)
        
9. **Future Directions**
    
    - Protocol co-design for UTM & aerial connectivity
    - Multi-agent cooperation in spectrum/resource usage
    - Large-scale field testing needs
        
10. **Conclusion**
    

---

## 📈 **3. Paper Acceptance Potential – How Strong?**

|Criteria|Evaluation|
|---|---|
|**Relevance to COMST**|✅ Excellent|
|**Topic Popularity**|✅ Increasing (5G/6G + UAVs + Smart Airspace)|
|**Existing Literature**|✅ Sufficient for comprehensive coverage|
|**Gap in Prior Surveys**|✅ No single survey unifies all aspects (Multi-link + UTM + Security + Standards)|
|**Novelty**|✅ Strong, if you create a compelling taxonomy and synthesis|
|**Likelihood of Acceptance**|**⭐️⭐️⭐️⭐️☆ (4.5/5)** — High, if well-executed|

---

## 🛠 Next Steps to Maximize Acceptance Chances

1. **Clearly define a taxonomy** early in the paper.
2. **Quantitatively compare** existing solutions using tables/metrics.
3. Cite **all key papers, standards, and real deployments** (avoid bias).
4. Cover both **academic** and **industry** perspectives.
5. Include **open challenges and future research directions** in depth.
    

---

Would you like help creating:

- A detailed **taxonomy diagram**
- A **paper outline** in LaTeX
- A **list of 100+ key references** to kickstart your literature review?
    

---

### 📘 **FUNDAMENTAL UAV COMMUNICATION SURVEYS**

1. Mozaffari et al., “A Tutorial on UAVs for Wireless Networks: Applications, Challenges, and Open Problems.” _IEEE Commun. Surv. Tutor._, 2018 [arxiv.org+9arxiv.org+9en.wikipedia.org+9](https://arxiv.org/abs/1803.00680?utm_source=chatgpt.com)
    
2. Li, Fei & Zhang, “UAV Communications for 5G and Beyond: Recent Advances and Future Trends.” arXiv, 2019 [arxiv.org+1en.wikipedia.org+1](https://arxiv.org/abs/1901.06637?utm_source=chatgpt.com)
    
3. Fotouhi et al., “Survey on UAV Cellular Communications: Practical Aspects, Standardization Advancements, Regulation, and Security Challenges.” _IEEE Commun. Surv. Tutor._, 2018 [orbilu.uni.lu+1en.wikipedia.org+1](https://orbilu.uni.lu/handle/10993/53086?utm_source=chatgpt.com)
    
4. Khuwaja et al., “A Survey of Channel Modeling for UAV Communications.” _IEEE Commun. Surv. Tutor._, 2018 [arxiv.org+15dl.acm.org+15orbilu.uni.lu+15](https://dl.acm.org/doi/abs/10.1016/j.comcom.2023.05.013?utm_source=chatgpt.com)
    
5. Khawaja et al., “A Survey of Air-to-Ground Propagation Channel Modeling for UAVs.” _IEEE Commun. Surv. Tutor._, 2019 [dl.acm.org+1orbilu.uni.lu+1](https://dl.acm.org/doi/abs/10.1016/j.comcom.2023.05.013?utm_source=chatgpt.com)
    
6. Gupta, Jain & Vaszkun, “Survey of Important Issues in UAV Communication Networks.” _IEEE Commun. Surv. Tutor._, 2016 [orbilu.uni.lu+2dl.acm.org+2orbilu.uni.lu+2](https://dl.acm.org/doi/abs/10.1016/j.comcom.2023.05.013?utm_source=chatgpt.com)
    

---

### 🛰 **UAV RELAY & NETWORK-LAYER SURVEYS**

7. Li et al., “A Survey on Unmanned Aerial Vehicle Relaying Networks.” _IET Commun._, 2021 [arxiv.org+13ietresearch.onlinelibrary.wiley.com+13digital-library.theiet.org+13](https://ietresearch.onlinelibrary.wiley.com/doi/10.1049/cmu2.12107?utm_source=chatgpt.com)
    
8. Masaracchia et al., “UAV-enabled Ultra-Reliable Low-Latency Communications for 6G.” _IEEE Access_, 2021 [link.springer.com+4dl.acm.org+4orbilu.uni.lu+4](https://dl.acm.org/doi/abs/10.1016/j.comcom.2023.05.013?utm_source=chatgpt.com)
    

---

### 🌐 **AERIAL & SPACE-INTEGRATED NETWORK SURVEYS**

9. Cao et al., “Airborne Communication Networks: A Survey.” _IEEE J. Sel. Areas Commun._, 2018 [mdpi.com+2orbilu.uni.lu+2orbilu.uni.lu+2](https://orbilu.uni.lu/handle/10993/53086?utm_source=chatgpt.com)
    
10. Dao et al., “Survey on Aerial Radio Access Networks: Toward a Comprehensive 6G Access Infrastructure.” _IEEE Commun. Surv. Tutor._, 2021 [orbilu.uni.lu+1dl.acm.org+1](https://orbilu.uni.lu/handle/10993/53086?utm_source=chatgpt.com)
    
11. Baltaci et al., “A Survey of Wireless Networks for Future Aerial COMmunications (FACOM).” arXiv/related to IEEE COMST 2021 [arxiv.org](https://arxiv.org/abs/2111.04175?utm_source=chatgpt.com)
    

---

### 📡 **CNPC & COMMAND AND CONTROL LINKS**

12. Hosseini et al., “UAV Command and Control, Navigation and Surveillance: A Review.” arXiv, 2018 [arxiv.org](https://arxiv.org/abs/1812.02792?utm_source=chatgpt.com)
    
13. Abdalla & Marojevic, “Communications Standards for UAS: The 3GPP Perspective and Research Drivers.” arXiv, 2020 [dl.acm.org+15arxiv.org+15orbilu.uni.lu+15](https://arxiv.org/abs/2009.03533?utm_source=chatgpt.com)
    

---

### 🛡 **SECURITY, RELAY & PROTOCOL SURVEYS**

14. Krishna & Murphy, “A Review on Cybersecurity Vulnerabilities for UAVs.” _IEEE SSRR_, 2017 [en.wikipedia.org+10orbilu.uni.lu+10arxiv.org+10](https://orbilu.uni.lu/handle/10993/53937?utm_source=chatgpt.com)
    
15. Armouri et al., “Softwarization of UAV Networks: A Survey of Applications and Future Trends.” _IEEE Access_, 2020 [orbilu.uni.lu](https://orbilu.uni.lu/handle/10993/53086?utm_source=chatgpt.com)
    

---

### 📋 **UTM / UAS TRAFFIC MANAGEMENT SURVEYS**

16. Survey on UAS Traffic Management. _ACM Comput. Surv._, 2022 [dl.acm.org+1en.wikipedia.org+1](https://dl.acm.org/doi/abs/10.1145/3617992?utm_source=chatgpt.com)
    
17. Alarcón et al., “Procedures for Integration of Drones into Airspace Based on U‑Space Services.” _Aerospace_, 2020 [dl.acm.org](https://dl.acm.org/doi/abs/10.1145/3617992?utm_source=chatgpt.com)
    
18. Alkadi & Shoufan, “UTM Solution Using Crowd‑Sensing and Blockchain.” arXiv, 2021 [dl.acm.org](https://dl.acm.org/doi/abs/10.1145/3617992?utm_source=chatgpt.com)
    

---

### 🧠 **ADVANCED/TREND SURVEYS**

19. Azari et al., “THz‑empowered UAVs in 6G: Opportunities, Challenges, and Trade‑offs.” arXiv, 2022 [orbilu.uni.lu+1orbilu.uni.lu+1](https://orbilu.uni.lu/handle/10993/53086?utm_source=chatgpt.com)
    
20. Lin et al., “The Sky Is Not the Limit: LTE for Unmanned Aerial Vehicles.” _IEEE Commun. Mag._, 2018 [orbilu.uni.lu](https://orbilu.uni.lu/handle/10993/53086?utm_source=chatgpt.com)
    

---

### 📈 **How to Expand to 100+ References**

- **Backward-tracking**: Check each paper’s references for further core works.
    
- **Forward citations**: Use Google Scholar to find recent follow-up studies.
    
- **Filter by topic**:
    
    - **Multi-link/multi-connectivity**: e.g., Link aggregation, SDN/NFV in UAS networks.
        
    - **SAGIN / integrated architectures**: Air-to-ground, satellite-aided networks.
        
    - **UTM communication protocols**: From FAA/NASA whitepapers, 3GPP releases.
        
    - **Security in UTM/multi-link**: Blockchain-based UTM-chain, CNPC encryption schemes.
        
    - **Performance modeling and testbeds**: Markov reliability models, SUAs corridor performance studies.

---

### Ideas and notes from dronnect discussions: 
many of the implementation challenges revolve around handover of and communication amongst systems, to which communication design serves as a supporting function 

---
- What are the research objectives  15/9
	- Multi-link connection 
	- Smart Routing 
	- mmWave to Classic Comm Ghz - how this will pan - collaboration with T2
	- What is outcome of the projects - Like a heatmap and of technologies on height usecase etc..
	- what network coding , computing could do
	- Traditional communication is constrained by transmission distance - UTM / U-Space via internet

Drone data transmission isn't about raw data - its about who can transfer raw data into decisions 

---
<span style="color:rgb(255, 0, 0)">Key words: Data mesh, Cloud migration , Application , 3GPP standards, involvement of 5G, MEC, U-Space, USSP, Federated Information management system </span>

### **What is U-Space?**

- **U-Space** is the European framework (by **EASA & SESAR**) for the **safe, efficient, and scalable integration of drones into airspace**, especially in low-level airspace (up to ~120m).
- It’s the EU’s equivalent to the U.S. **UTM (Unmanned Aircraft System Traffic Management)** concept by the FAA/NASA.
- <span style="color:rgb(255, 0, 0)">U-Space is <b>not just technology</b>, but also <b>rules, services, and infrastructure</b> that enable BVLOS (Beyond Visual Line of Sight) drone operations in a safe and coordinated way.</span> 

### **Impact on UTM (Unmanned Traffic Management)**

- UTM is the **broader global concept** for managing drone traffic; U-Space is the **European implementation** of it.
- U-Space:
    - **Standardizes services** (registration, flight approval, conflict detection, etc.).
    - Pushes for **interoperability** across countries and providers.
    - Introduces a **federated model**, where multiple service providers can operate under the same regulatory umbrella.
- This will allow:
    - **Scalable drone operations** (delivery, inspection, urban air mobility).
    - **Integration with manned aviation** in controlled/uncontrolled airspace.
    - **Automated and digital air traffic management**, reducing human ATC workload.
-
**USSP (U-Space Service Provider):**
- Private/public entities that deliver **U-Space services** (flight planning, traffic info, conflict resolution, tracking, etc.).
- Comparable to “digital ATC for drones”.
- They **don’t control drones**, but provide the **digital infrastructure** and services for safe operation.
- Multiple USSPs can exist — they must **interoperate**.
**CISP (Common Information Services Provider):**
- Ensures a **shared, authoritative data layer** across all USSPs.
- Provides essential info like:
    - Airspace restrictions (NOTAMs, geo-fencing).
    - Weather.
    - Traffic data from surveillance networks.
- Guarantees **interoperability** and **trustworthiness** — so that all drones have the same situational awareness regardless of which USSP they’re connected to.
- Without CISP, U-Space risks fragmentation and safety issues.

### **Role of 5G, Cloud, MEC (Multi-access Edge Computing)**

- **5G:**
    - Ultra-low latency (critical for collision avoidance, real-time tracking).
    - High bandwidth (video feeds, remote piloting).
    - Network slicing (dedicated drone “lanes” in telecom networks).
- **Cloud:**
    - Scalable processing of flight plans, data analytics, AI-based airspace management.
    - Centralized coordination across regions/countries.
    - Supports USSP platforms at national or pan-European scale.
- **MEC (Edge Computing):**
    - Moves computation closer to the drone for **real-time decision-making** (traffic alerts, dynamic rerouting).
    - Reduces dependency on distant cloud data centers.
    - Critical in **dense urban environments** where latency must be <10 ms.

---
PHD 
Short answer: **Your topic is NOT too broad — but your _current framing_ is.**  
You have _all the ingredients_ for a strong, novel PhD, but you need a **sharp, unifying problem statement** and **one core contribution** that everything else (Wi-Fi mesh, 5G, LEO, network coding, resource-aware switching, simulations + testbed) supports.

Below is a clear breakdown to help you understand where the novelty is and how to sharpen focus.

---

# ✅ **1. Is your research topic too broad?**

Right now, your topic spans:

- A2A mesh links (Wi-Fi)
- A2G links (5G)
- LEO satcom
- Network coding & computing
- Real-time adaptive link optimization
- Simulations + real testbed

This is a **system of systems**. It is _broad_, but **PhDs in communication systems are often broad** — if they converge into one main idea.

Broad is **not a problem**.  
**Unfocused is.**

Right now, your novelty isn’t obvious because you are describing _technologies_, not a _problem_.

You need to turn this:

> “I work on mesh Wi-Fi, 5G, LEO, network coding…”

into this:

> “I propose a unified real-time multi-link communication architecture that guarantees reliable UAV BVLOS telemetry by optimally switching and combining Wi-Fi mesh, 5G, and LEO links through adaptive network coding and cross-layer scheduling.”

Now it is clear, and the novelty emerges.

---

# ✅ **2. What novelty do you _already_ have?**

You already have excellent novelty potential in multiple areas:

### **Novelty 1: Multi-link UAV BVLOS Telemetry Optimizer**

A real-time algorithm that:

- _predicts_ link quality
- _combines_ links with coding
- _switches_ links using availability + priority
- _allocates_ bandwidth to telemetry vs. payload

This is highly publishable.

---

### **Novelty 2: Cross-technology convergence**

No one in academia has fully integrated:

- UAV Wi-Fi mesh (A2A)
- 5G (A2G)
- LEO satcom (global coverage)

Especially with **non-payload critical data (C2 telemetry)** where reliability is much stricter than video.

---

### **Novelty 3: Network coding in UAV multi-connectivity**

You can propose:

- RLNC for redundancy
- Fountain codes for LEO fallback
- Predictive coding based on link disruption

This alone is enough for a **first-author IEEE paper**.

---

### **Novelty 4: Simulation + real testbed validation**

90% of researchers ONLY simulate.
Adding real flight or hardware testbed gives HUGE novelty.

---

# ✅ **3. What you still need to do (to avoid “too broad”)**

Define **one central research question**, e.g.:

> “How can a UAV maintain ultra-reliable telemetry communication for BVLOS operations using a dynamic multi-link architecture across Wi-Fi mesh, 5G, and LEO satellite networks?”

Then define **three technical objectives** that feed into this question:

---

## Objective 1 — _Characterize link availability & reliability_

- Measure Wi-Fi A2A ranges
- Evaluate 5G cell-edge performance for UAVs
- Evaluate LEO RTT + jitter patterns

**Output:** A unified probabilistic link model for UAVs.

---

## Objective 2 — _Develop the adaptive telemetry communication algorithm_

This includes:

- Link selection
- Traffic prioritization
- Network coding
- Detour routing across mesh

**Output:** A real-time multi-link controller.

---

## Objective 3 — _Validate on OMNeT++ + testbed_

- Implement your algorithm in OMNeT++
- Integrate with hardware testbed
- Show reliability improvements


**Output:** Real-world proof and performance benchmarks.

---

# ✅ **4. What is missing now (and why it seems “broad”)**

You are missing a **flagship algorithm** with a name.

Every strong PhD needs a “hero contribution”:

- A scheduling algorithm
- A coding scheme
- A multi-link controller
- A distributed routing algorithm
    

Example names:

- **AeroLink-MC**: Multi-Connectivity Link Optimizer
- **SkyCode**: UAV-adaptive network coding
- **FlyRoute**: Mobility-aware mesh routing
- **AeroSwitch**: Predictive link switching
    

We can design such an algorithm together.

---

# ✅ **5. How to reshape your PhD into a focused, novel project**

Here is the formula:

### **Unified Theme**

> _Reliable multi-link telemetry communication for BVLOS UAVs._

### **Primary Novelty**

> _A real-time adaptive communication controller integrating Wi-Fi mesh, 5G, and LEO satcom with network coding to guarantee telemetry reliability._

### **Supporting Components**

- OMNeT++ modelling
- Testbed measurements
- Coding optimization
- Multi-link scheduling

### **Expected Deliverables**

- 3–5 conference papers
- 1–2 journal papers
- 1 tutorial workshop/panel
- A named flagship algorithm
- A dissertation with validations


---



**
Gap 1: Limited Exploration of Multi-Link Communication for UAV BVLOS Operations
- Existing research focuses on single-link communication or dual-link failover mechanisms. There is a lack of frameworks for integrating multiple communication links (e.g., 5G, satellite, and RF) to enhance reliability, coverage, and performance.
- Challenges in link prioritization, switching, and bandwidth allocation in dynamic UAV environments are not adequately addressed.

Gap 2: Lack of Integration Between Data Mesh and UAV Communication Systems
- The application of the Data Mesh paradigm to UAV data, particularly in high-mobility environments such as UAM networks, is largely unexplored.
- How distributed data ownership and real-time data sharing can be achieved while ensuring security and scalability in UAV networks requires investigation.

Gap 3: Insufficient Focus on AoI in Multi-Link Communication for UAM
- AoI is critical for time-sensitive applications in UAM, such as collision avoidance and air traffic management. However, its behavior and optimization in multi-link communication scenarios, especially when coupled with data mesh architectures, are underexplored.
- There is a need for models and algorithms to minimize AoI while ensuring data integrity and consistency across heterogeneous links.
<span style="color:rgb(0, 176, 80)">Topic II: Resilient and Redundant  Multi-link architecture </span>
<span style="color:rgb(0, 176, 80)">Topic III: Network management </span>

---
 - First PhD presentation  - Winter Workshop 2024
 
![[T9_Workshop_presentation- V1.pdf]]
 - PhD talk  - 1
 
 ![[PhD talk -1 1.pdf]]
 - Technological Methods - Multilayered communication Architecture (5G, Satcom, Mesh) - hybrid multipath - Resilient networks
- Multipath —> network coding for traffic types - C2 comm, Payload data ( Video, image)
- Energy Efficiency - endurance- signal strength - RIS support
- Network slicing —> Drone traffic QoS network slice
- Network handwork - internal / external network handovers in Multi-path
- Edge computing ICN -in network computing
- With respect to UTM - external communication - DataMesh , Age of information (AoI) 
---

### Dissertation Setup 

UTM- Data Mesh 

Multilink Simulator VM

Omnet++ NTN 

Air 2 air - WiFi  Mesh setup 

octomap - setup

---

-  Cross-layer optimization 
- Cross-domain determinism 
- Latency - BW tradeoff matrics
- stats | Algebra based solving
- network calculus
- AoI  - Age of information 
- UTM - Data mesh 
- BVLOS - multilink
- network coding 
- rate allocation
- Multi-path 
- MEC 
- Edge computing
- **SNMP** - Simple Network Management protocol - OID - Object identifier MIB- Management information base (OID is numerical and converted to text by MIB) - port 161,162 - polling and traps | SNMP V3 - secure than 1 and 2C
- **streaming network telemetry** Streaming network telemetry is a real-time data collection service in which network devices, such as routers, switches and firewalls, continuously push data related to the network's health to a centralized location.
 ---
 
 **Research Gaps & Challenges**
Network Performance & QoS
Latency & Bandwidth Limitations – Current ATN IPS models are designed for traditional aviation; AAM needs low-latency, high-speed networks (5G/6G, SATCOM, and mesh networks).
Congestion Management – AAM flights in urban areas will require dynamic QoS handling.

 Security & Resilience
Cybersecurity in Highly Connected Networks – Need stronger Zero-Trust Architecture (ZTA) for AAM systems.
Jamming & Spoofing Protections – AAM systems are vulnerable to GPS spoofing, signal interference, and cyberattacks.

 Interoperability & Standardization
Harmonization with 5G & Satellite Networks – Need unified frameworks for hybrid networks (ATN IPS + 5G + SATCOM).
Scalability for High-Density Air Traffic – Existing ATN IPS was not designed for the high volume of AAM flights expected in urban environments.

 AI & Automation in ATN IPS
AI-Driven Air Traffic Routing – Needs more research on autonomous airspace management using AI.
Machine Learning for Network Optimization – Dynamic allocation of network resources for AAM aircraft.

 **Future Research Directions**
 
- 5G/6G Integration for ATN IPS-based AAM Communications
- AI & Blockchain for Secure and Resilient AAM Networking
- Edge Computing for Real-Time Air Traffic Management
- Cross-border AAM Communication Standardization (ICAO + Industry)
- Hybrid ATN IPS-Satellite Architecture for Global UAM Operations
---

- **Adaptive Transport Network (ATN)**
An Adaptive Transport Network (ATN) is designed for high-speed, scalable, and intelligent data transmission, commonly used in modern telecommunications, 5G, data centers, and cloud services.

A. Architecture
ATN architecture is based on three core layers:
Infrastructure Layer (Physical Layer)
    Includes fiber optics, microwave links, and satellite links.
    Uses Dense Wavelength Division Multiplexing (DWDM) for high-bandwidth data transport.
Control Layer
    Manages dynamic routing using Software-Defined Networking (SDN).
    Implements Network Function Virtualization (NFV) for flexible network resource allocation.
Application Layer
    Provides services like IoT, video streaming, cloud computing, and enterprise networks.
    Uses AI/ML for predictive analytics, congestion control, and fault detection.
B. Protocols
Optical Transport Protocols
    SONET/SDH (Synchronous Optical Networking) – Legacy but still used for reliability.
    OTN (Optical Transport Network) – Enables multiplexing of different data streams over fiber.
Packet Transport Protocols
    MPLS-TP (Multiprotocol Label Switching - Transport Profile) – Optimized for scalable and efficient packet-switched networks.
    Carrier Ethernet (CE 2.0) – Standardized by MEF for high-performance Ethernet transport.
Network Control Protocols
    OpenFlow (for SDN) – Controls network traffic by dynamically managing routing decisions.
    BGP (Border Gateway Protocol) & OSPF (Open Shortest Path First) – Used for internet routing and autonomous system interactions.
C. Implementation
5G & Edge Computing: Adaptive transport networks optimize low-latency services like AR/VR and IoT.
AI-Powered Optimization: Real-time monitoring adjusts bandwidth allocation for fluctuating network loads.
Cloud-Integrated Networks: ATN is used by hyperscalers like Google, AWS, and Microsoft Azure to optimize data movement.

- **Automatic Telecommunications Network (ATN**)
An Automatic Telecommunications Network (ATN) is focused on automated call/data routing and management in traditional and modern telecom infrastructures.
A. Architecture
Core Switching Layer
    Uses Softswitches (Software-based Switching) instead of hardware-based switching.
    Implements Session Initiation Protocol (SIP) for VoIP services.
Transport & Access Layer
    Uses PSTN (Public Switched Telephone Network) and IMS (IP Multimedia Subsystem) for call handling.
    Includes fiber, DSL, LTE, 5G networks for connectivity.
Service Layer
    Provides value-added services (VAS) such as voicemail, conference calling, and real-time billing.
B. Protocols
Circuit-Switched Networks
    SS7 (Signaling System 7): Used for call setup and number translation in landline and mobile networks.
    ISUP (ISDN User Part): Manages call control for PSTN and ISDN networks.
Packet-Switched Networks
    SIP (Session Initiation Protocol): Handles VoIP and multimedia calls.
    H.323: Used for video conferencing and VoIP services.
    Diameter & RADIUS: Used for authentication and billing.
Routing & Management Protocols
    BGP (Border Gateway Protocol): Manages routing between different telecom providers.
    LNP (Local Number Portability): Allows users to retain phone numbers across networks.
C. Implementation
4G/5G Networks: Uses IMS for automated call routing and VoLTE services.
AI-Driven Call Routing: Optimizes call connections based on quality and network congestion.
Emergency Communication Systems: Ensures priority call handling for critical services like 911

---

**5G and Satcom in AAM** 
5G 
- Limited coverage 
- Limited LOS dependency
- Handover issues
- Better for low-altitude communication| Smart cities 
- Edge computing 
- Ultra low latency
- High bandwidth 
- Dense network capacity 
Satcom
- Global Coverage 
- Reliable BLOS signal 
- Stable connectivity 
- Resilience to network failure 
- higher latency 
- Low bandwidth 
- Costly than terrestrial network 
- Intercity AAM - high altitude platform
- Cargo and inspection drones usecase
- Backup for 5G 

Some more on AAM- Communication 
Advanced Air Mobility (AAM) envisions integrating innovative aerial transportation systems into urban and regional environments. A critical component of this integration is the development of robust communication network infrastructures to ensure safe and efficient operations. Current research and development efforts have identified several key areas and existing gaps:

**1. Communication Requirements and Challenges:**

- **Coverage and Connectivity:** AAM operations necessitate seamless communication coverage across diverse environments, including urban canyons and rural areas. Ensuring uninterrupted connectivity is essential for command and control (C2) communications and collision avoidance systems. [researchgate.net](https://www.researchgate.net/publication/386093820_Urban_Air_Mobility_Communications_and_Networking_Recent_Advances_Techniques_and_Challenges?utm_source=chatgpt.com)
- **Latency and Data Rates:** Low-latency communication is vital for real-time data exchange between aircraft and ground control stations. High data rates are required to support applications such as high-definition video streaming for surveillance and navigation.
    [researchgate.net](https://www.researchgate.net/publication/386093820_Urban_Air_Mobility_Communications_and_Networking_Recent_Advances_Techniques_and_Challenges?utm_source=chatgpt.com)

**2. Integration of 5G and Satellite Communications:**
- **5G Networks:** The deployment of 5G technology offers potential benefits for AAM, including enhanced data rates and reduced latency. However, challenges remain in ensuring consistent 5G coverage, especially in low-altitude airspace and rural regions.
    [mdpi.com](https://www.mdpi.com/2504-446X/7/9/556?utm_source=chatgpt.com)
    
- **Satellite Communications (Satcom):** Satcom can complement terrestrial networks by providing coverage in areas lacking 5G infrastructure. The integration of Satcom with terrestrial networks is crucial for maintaining continuous connectivity during all flight phases.
    <span style="color:rgb(0, 0, 0)">[arxiv.org](https://arxiv.org/abs/2004.12555?utm_source=chatgpt.com)</span>

**3. Network Infrastructure Development:**

- **Urban Air Mobility (UAM) Corridors:** Establishing dedicated air corridors equipped with the necessary communication infrastructure can facilitate organized and safe AAM operations. Research is ongoing to design these corridors with optimal placement of communication nodes to ensure coverage and reliability.
    [mabe.utk.edu](https://mabe.utk.edu/wang-investigates-autonomous-vehicle-control-for-advanced-air-mobility-systems/?utm_source=chatgpt.com)
- **Multi-Technology Integration:** Relying solely on a single communication technology may not meet all AAM requirements. Integrating multiple technologies, such as 5G, Satcom, and existing aviation communication systems, is being explored to enhance robustness and reliability.
    [arxiv.org](https://arxiv.org/abs/2111.04175?utm_source=chatgpt.com)

**4. Identified Research Gaps:**

- **Standardization:** There is a need for standardized communication protocols and interfaces to ensure interoperability between different aircraft and ground systems.
- **Security:** Ensuring the cybersecurity of communication links is paramount to protect against potential threats and unauthorized access.
- **Scalability:** As AAM operations scale up, the communication network must handle increased traffic without compromising performance.

Addressing these challenges requires collaborative efforts among researchers, industry stakeholders, and regulatory bodies to develop a resilient communication network infrastructure that supports the safe and efficient integration of AAM into the airspace.

Since you have an outline of your PhD research in communication gaps for **Advanced Air Mobility (AAM)**, you should **start engaging in collaborations and research discussions immediately** rather than waiting for results. Early collaboration will provide valuable insights, refine your research direction, and help you secure opportunities with major organizations like **NASA, ICAO, RTCA, EUROCONTROL**, and industry leaders.

---

**Optimization Algorithms & Network Coding for Reliable Multi-Link Architecture in AAM**

To ensure efficient resource utilization, reliability, and seamless connectivity in Advanced Air Mobility (AAM), multi-link architectures must integrate optimization algorithms and network coding techniques. These help manage dynamic network conditions, reduce latency, and maximize throughput.

1. <span style="color:rgb(0, 176, 80)">Optimization Algorithms for Multi-Link AAM Networks</span>

(a) Multi-Path Scheduling & Load Balancing
Multipath TCP (MPTCP) & QUIC
    Dynamically distributes data across multiple links (5G, satellite, Wi-Fi, etc.).
    Optimizes throughput and reduces congestion.
Reinforcement Learning (RL)-Based Scheduling
    AI-driven optimization for selecting the best link dynamically.
    Uses Deep Q-Networks (DQN) or Proximal Policy Optimization (PPO).

(b) Resource Allocation & Spectrum Management
Genetic Algorithms (GA)
    Used for spectrum allocation in a highly dynamic airspace.
    Optimizes power and bandwidth across multiple communication links.
Game Theory-Based Optimization
    Helps AAM vehicles select the best frequency bands and transmission power levels.
    Used for interference mitigation and fair spectrum sharing.

(c) Energy-Aware & Latency-Optimized Routing
Particle Swarm Optimization (PSO)
    Finds the optimal network paths while minimizing power consumption.
    Used in UAV swarm communication.
Ant Colony Optimization (ACO)
    Ideal for real-time adaptive routing in aerial networks.
    Inspired by ant foraging behavior, it selects the best paths dynamically.


<span style="color:rgb(0, 176, 80)">2. Network Coding for Reliability & Efficient Resource Utilization</span>

Network coding (NC) enhances reliability, throughput, and resilience in multi-link AAM networks by enabling coded transmission of data rather than simple forwarding.

(a) Random Linear Network Coding (RLNC)
Allows simultaneous transmission of coded packets across multiple links.
Increases reliability in noisy and high-mobility scenarios.
Reduces retransmissions by allowing receivers to decode missing packets.

(b) Opportunistic Network Coding
Used in multi-hop AAM networks to reduce congestion.
Combines multiple data flows into coded packets, minimizing redundant transmissions.

(c) Multi-Path Network Coding (MNC)
Ensures error-resilient communication over multiple independent paths.
Works well in hybrid 5G + satellite + Wi-Fi architectures.


<span style="color:rgb(0, 176, 80)">3. Hybrid Approach: Combining Optimization Algorithms & Network Coding
</span>

For an effective and reliable multi-link AAM network, a hybrid approach is recommended:
AI-Driven Adaptive Link Selection (using RL)
    Chooses the best communication path based on latency, packet loss, and energy consumption.
Network Coding for Redundancy & Error Correction
    Uses RLNC to minimize retransmissions and improve packet delivery in high-mobility AAM scenarios.
Multi-Objective Optimization
    Uses PSO & Genetic Algorithms to balance bandwidth, power, and delay for optimal performance.


Conclusion
By integrating optimization algorithms (GA, RL, PSO, MPTCP, etc.) and network coding techniques (RLNC, MNC), AAM networks can efficiently utilize resources, reduce latency, and improve reliability in a multi-link environment.

---

**Technologies Similar to Mesh Networks**

Mesh networking is a decentralized network topology where nodes (devices) connect dynamically without relying on a central hub. Several similar or alternative technologies exist that provide self-healing, adaptive, and multi-hop communication for various applications, including Advanced Air Mobility (AAM), IoT, and edge computing.

<span style="color:rgb(0, 176, 80)">1. Ad Hoc Networks</span>
 Definition: Self-organizing networks where nodes communicate without predefined infrastructure.
Mobile Ad Hoc Networks (MANETs)
    Used in military, disaster response, and UAV communication.
    Supports dynamic topology and self-routing.
Vehicular Ad Hoc Networks (VANETs)
    Enables vehicle-to-vehicle (V2V) and vehicle-to-infrastructure (V2I) communication.
    Used in smart transportation and autonomous driving.
Flying Ad Hoc Networks (FANETs)
    UAV-based ad hoc networks for AAM, emergency response, and surveillance.
    Requires high mobility support and low-latency routing.

<span style="color:rgb(0, 176, 80)">2. Software-Defined Networking (SDN)</span>
Definition: Centralized network management enabling dynamic control of routing and resources.
Separates control plane (decision-making) from the data plane (packet forwarding).
Works well with mesh and ad hoc networks to optimize performance.
Used in AAM for dynamic airspace communication.

<span style="color:rgb(0, 176, 80)">
3. Cognitive Radio Networks (CRNs)</span>
Definition: Intelligent networks that dynamically adjust radio frequencies to avoid interference.
Uses AI-driven spectrum sensing to optimize bandwidth.
Can be integrated with mesh networks for adaptive AAM communication.
Works in highly congested RF environments (e.g., urban air mobility corridors).

<span style="color:rgb(0, 176, 80)">4. Delay-Tolerant Networks (DTNs)</span>
Definition: Designed for intermittent connectivity in challenging environments.
Stores and forwards packets until a connection is available.
Ideal for UAV swarms, deep-space communication, and rural AAM operations.
Uses opportunistic routing instead of real-time transmission.

<span style="color:rgb(0, 176, 80)">5. Peer-to-Peer (P2P) Networks</span>
 Definition: Distributed networks where devices share resources without centralized servers.
Similar to mesh networks but more common in file-sharing, blockchain, and decentralized computing.
Applied in edge computing for AAM, where drones and ground stations exchange data without a cloud intermediary.

<span style="color:rgb(0, 176, 80)">6. LPWAN (Low-Power Wide Area Networks)</span>
Definition: Long-range, low-power networks for IoT and sensor-based applications.
LoRaWAN (Long Range Wide Area Network)- Used for long-range, low-data-rate AAM applications (e.g., sensor telemetry).
NB-IoT (Narrowband IoT)- Works in cellular bands for infrastructure-based connectivity.
Sigfox - Ultra-narrowband IoT network for low-power, long-range applications.

<span style="color:rgb(0, 176, 80)">7. Multi-Access Edge Computing (MEC)</span>
 Definition: Brings computing and networking resources closer to the edge (near users).
Reduces latency by processing data near AAM vehicles instead of the cloud.
Works with mesh and SDN for real-time traffic management and AI-driven airspace control.

Conclusion
Each of these mesh-like or alternative network technologies is suitable for different AAM scenarios, including UAV communication, edge computing, and smart infrastructure. A hybrid approach combining mesh, SDN, and cognitive radio can maximize reliability and efficiency in future AAM networks.

---
### Other topics with respect to surveillance and broadcast

- **Robust Path Planning with Obstacle Avoidance for Emergency Response**
    - **Gap:** Existing studies focus on UAV trajectory planning, but real-time obstacle avoidance in emergency situations (e.g., natural disasters, urban air mobility) is underexplored.
    - **Proposed Solution:** Develop AI-powered path optimization algorithms integrating LiDAR, ADS-B, and 5G edge computing for real-time obstacle detection and avoidance.
-   **Joint Trajectory Planning & Communication for Multi-UAV Systems
    - **Gap:** Most studies analyze UAV trajectory and communication separately rather than jointly optimizing both in an intelligent air-ground system.
    - **Proposed Solution:** Design a reinforcement learning-based framework for cooperative trajectory planning and communication scheduling, improving network efficiency and collision avoidance.
- **Interference Mitigation Between UAVs and Civil Aircraft ADS-B Signals**
    - **Gap:** Current studies address ADS-B frequency congestion but lack dynamic interference mitigation strategies in dense UAV environments.
    - **Proposed Solution:** Develop an adaptive spectrum-sharing framework using machine learning to predict congestion and dynamically switch between ADS-B, 5G, and satellite links.
- **Hierarchical ADS-B & 5G Integration for Scalable AAM Networks**
    - **Gap:** While hierarchical ADS-B and 5G UAV monitoring structures exist, they require performance validation in large-scale, real-world AAM scenarios.
    - **Proposed Solution:** Implement and test a multi-layered UAV monitoring system using software-defined networking (SDN) and AI-driven load balancing across ADS-B, 5G, and LEO satellites.
- **6G Space-Air-Ground Networks for Data Collection & Transmission**
    - **Gap:** High-altitude platforms (HAPs) and LEO satellites offer promising solutions, but `cooperative data transmission schemes for UAV swarm communication remain underdeveloped.`
    - **Proposed Solution:** Design an AI-powered multi-hop transmission protocol leveraging HAPs and LEO satellites to enhance connectivity and reduce latency in 6G-integrated AAM operations.
----

Drones at ≤150 m BVLOS are being studied primarily with cellular (LTE/5G) links, mmWave mesh/backhaul, UAV-to-UAV (D2D) links, and relay/UAV-swarm techniques. Main challenges are coverage, interference, reliability and regulatory safety (C2 redundancy, DAA); many papers test solutions via antenna uptilt, beamforming, relays, and link/path planning.

---

## Research trends

This section summarizes the dominant architectures, hardware, and algorithmic trends researchers are pursuing for low-altitude BVLOS communications and points to representative experiments and prototypes. The emphasis in recent (2023–2025) work is on leveraging commercial cellular networks while adding aerial‑specific radio designs and airborne mesh/relay links.

- Cellular-connected drones are a major focus for BVLOS C2 and payload links; field KPI comparisons across low- and mid-band 5G versus LTE show active experimental evaluation of coverage and performance for aerial UEs 
    

- Experimental datasets and flight tests for LTE at low altitudes (30–110 m) are available and used to build aerial propagation models and ML methods for aerial coverage prediction 

- High-throughput, low-latency airborne backhaul using mmWave mesh links is demonstrated in prototypes that place UAVs as self-organizing mmWave relays/backhaul nodes to support bandwidth‑intensive BVLOS applications 

- Aerial beamforming, directional antennas and mmWave sidelink strategies are proposed to mitigate inter‑UAV interference and improve reliability in drone corridors 

- Drone-to-drone (D2D) and sidelink approaches (including 3GPP‑style sidelink/semi‑persistent scheduling) plus dedicated UAV D2D prototypes are being developed for fast local coordination and redundancy in urban airspaces 

- Relay‑UAV concepts (e.g., portable relay kits) and multi‑UAV relays are used in field demonstrations to extend and harden BVLOS links without relying solely on ground infrastructure 
 
- Radio‑layer optimizations for reliability (short‑packet/URLLC design, BLER analysis, altitude-aware resource allocation) and antenna geometry tuning (uptilted BS antennas for corridors) are active topics to maximize reliable C2 ranges 
    

- Recent demos integrate edge processing, 5G links and onboard AI to reduce latency and data backhaul needs while maintaining robust 5G connectivity in BVLOS scenarios 
    
  

Representative citations for the above experimental and simulation advances are available in the literature 

---

## Challenges and solutions

This section frames the principal technical problems for BVLOS at low altitude and lists the concrete solutions validated or proposed in the literature, with examples of supporting studies. The main problems are coverage gaps, interference/visibility to many cells, link reliability and safety‑critical redundancy.

- Coverage holes and antenna geometry: existing cellular BS antennas are down‑tilted for ground UEs, creating reduced coverage at altitude; studies quantify optimal BS uptilt/additional antenna use to maximize corridor coverage and reduce coverage holes 

- Interference and multi‑node coexistence: aerial UEs become visible to many towers and to other UAVs, increasing interference; mmWave beamforming and narrow directional transmissions substantially reduce intra‑airspace interference and increase link reliability in simulations and prototypes 

- Reliability and latency for C2: short‑packet and URLLC‑style design (blocklength, power allocation, beamforming) can be optimized to maximize reliable control range and identify favorable altitude/resource tradeoffs for control links 

- Sparse/non‑urban coverage: cellular coverage outside urban areas can be unreliable for BVLOS; field studies compare LTE vs 5G performance and recommend path/trajectory control and cellular‑aware planning to improve link availability 
    

- Local redundancy and range extension: relay UAVs and self‑organizing UAV meshes provide mission‑level redundancy and gigabit backhaul where ground infrastructure is insufficient; SkyHaul‑style mmWave mesh and relay UAV kits have been prototyped to sustain high‑bandwidth BVLOS services 
    


- Fast local coordination and DAA assistance: D2D/sidelink communications (ad hoc or 3GPP‑style sidelink scheduling) provide low-latency neighbor awareness for collision avoidance and Complementary Detect‑and‑Avoid (DAA) links 

- Practical avionics/stack optimizations: MAVLink compression and pilot‑handover components have been field‑tested to reduce required C2 bandwidth and allow approved BVLOS operations under SORA‑like frameworks 
    


Example solution-to-challenge mapping (bulleted):

- Coverage uplift: BS uptilt and corridor‑specific antenna patterns to increase probability of coverage 

- Interference mitigation: mmWave beamforming and directional antennas on UAVs and ground nodes 
    
 
- Range/availability: relay UAVs and mmWave mesh as airborne backhaul 
    

- C2 reliability: short‑packet optimization and altitude-aware resource allocation (BLER analysis) 
    

- Operational redundancy: D2D/sidelink plus multi‑link designs to complement cellular C2 
    

---

## LAWN classification

This section states whether ≤150 m BVLOS fits the LAWN term and reports what the supplied literature says about altitude labels. The corpus does not provide a formal, citable definition or explicit altitude bands for the term LAWN, so a definitive classification cannot be supported from these papers.

- The supplied papers use terms such as "low‑altitude", "drone corridors" and report experimental altitudes (e.g., LTE flight datasets at 30–110 m and cellular coverage assessments with reliable 4G coverage noted toward ~85 m), but none of the reviewed articles defines a standard LAWN altitude envelope or publishes an authoritative LAWN specification 
    
    Drones at ≤150 m BVLOS are being studied primarily with cellular (LTE/5G) links, mmWave mesh/backhaul, UAV-to-UAV (D2D) links, and relay/UAV-swarm techniques. Main challenges are coverage, interference, reliability and regulatory safety (C2 redundancy, DAA); many papers test solutions via antenna uptilt, beamforming, relays, and link/path planning.

Research trends
This section summarizes the dominant architectures, hardware, and algorithmic trends researchers are pursuing for low-altitude BVLOS communications and points to representative experiments and prototypes. The emphasis in recent (2023–2025) work is on leveraging commercial cellular networks while adding aerial‑specific radio designs and airborne mesh/relay links.

Cellular-connected drones are a major focus for BVLOS C2 and payload links; field KPI comparisons across low- and mid-band 5G versus LTE show active experimental evaluation of coverage and performance for aerial UEs 

Experimental datasets and flight tests for LTE at low altitudes (30–110 m) are available and used to build aerial propagation models and ML methods for aerial coverage prediction 

High-throughput, low-latency airborne backhaul using mmWave mesh links is demonstrated in prototypes that place UAVs as self-organizing mmWave relays/backhaul nodes to support bandwidth‑intensive BVLOS applications 

Aerial beamforming, directional antennas and mmWave sidelink strategies are proposed to mitigate inter‑UAV interference and improve reliability in drone corridors 

Drone-to-drone (D2D) and sidelink approaches (including 3GPP‑style sidelink/semi‑persistent scheduling) plus dedicated UAV D2D prototypes are being developed for fast local coordination and redundancy in urban airspaces 

Relay‑UAV concepts (e.g., portable relay kits) and multi‑UAV relays are used in field demonstrations to extend and harden BVLOS links without relying solely on ground infrastructure 

Radio‑layer optimizations for reliability (short‑packet/URLLC design, BLER analysis, altitude-aware resource allocation) and antenna geometry tuning (uptilted BS antennas for corridors) are active topics to maximize reliable C2 ranges 

Recent demos integrate edge processing, 5G links and onboard AI to reduce latency and data backhaul needs while maintaining robust 5G connectivity in BVLOS scenarios 

Representative citations for the above experimental and simulation advances are available in the literature 

Challenges and solutions
This section frames the principal technical problems for BVLOS at low altitude and lists the concrete solutions validated or proposed in the literature, with examples of supporting studies. The main problems are coverage gaps, interference/visibility to many cells, link reliability and safety‑critical redundancy.

Coverage holes and antenna geometry: existing cellular BS antennas are down‑tilted for ground UEs, creating reduced coverage at altitude; studies quantify optimal BS uptilt/additional antenna use to maximize corridor coverage and reduce coverage holes 

Interference and multi‑node coexistence: aerial UEs become visible to many towers and to other UAVs, increasing interference; mmWave beamforming and narrow directional transmissions substantially reduce intra‑airspace interference and increase link reliability in simulations and prototypes 

Reliability and latency for C2: short‑packet and URLLC‑style design (blocklength, power allocation, beamforming) can be optimized to maximize reliable control range and identify favorable altitude/resource tradeoffs for control links 

Sparse/non‑urban coverage: cellular coverage outside urban areas can be unreliable for BVLOS; field studies compare LTE vs 5G performance and recommend path/trajectory control and cellular‑aware planning to improve link availability 

Local redundancy and range extension: relay UAVs and self‑organizing UAV meshes provide mission‑level redundancy and gigabit backhaul where ground infrastructure is insufficient; SkyHaul‑style mmWave mesh and relay UAV kits have been prototyped to sustain high‑bandwidth BVLOS services 

Fast local coordination and DAA assistance: D2D/sidelink communications (ad hoc or 3GPP‑style sidelink scheduling) provide low-latency neighbor awareness for collision avoidance and Complementary Detect‑and‑Avoid (DAA) links 

Practical avionics/stack optimizations: MAVLink compression and pilot‑handover components have been field‑tested to reduce required C2 bandwidth and allow approved BVLOS operations under SORA‑like frameworks 

Example solution-to-challenge mapping (bulleted):

Coverage uplift: BS uptilt and corridor‑specific antenna patterns to increase probability of coverage 

Interference mitigation: mmWave beamforming and directional antennas on UAVs and ground nodes 

Range/availability: relay UAVs and mmWave mesh as airborne backhaul 

C2 reliability: short‑packet optimization and altitude-aware resource allocation (BLER analysis) 

Operational redundancy: D2D/sidelink plus multi‑link designs to complement cellular C2 

LAWN classification
This section states whether ≤150 m BVLOS fits the LAWN term and reports what the supplied literature says about altitude labels. The corpus does not provide a formal, citable definition or explicit altitude bands for the term LAWN, so a definitive classification cannot be supported from these papers.

The supplied papers use terms such as "low‑altitude", "drone corridors" and report experimental altitudes (e.g., LTE flight datasets at 30–110 m and cellular coverage assessments with reliable 4G coverage noted toward ~85 m), but none of the reviewed articles defines a standard LAWN altitude envelope or publishes an authoritative LAWN specification 

Therefore, based on the provided literature, there is insufficient evidence to assert that 150 m specifically falls inside a defined LAWN category or to give an official LAWN altitude range; the studies instead report tested altitude ranges and emphasize “low‑altitude” without a universal numeric taxonomy 

For practical planning, note that several experimental datasets and planning studies focus on heights well below or up to ~100–110 m, and some path‑planning/coverage analyses cite reliable 4G aerial coverage only to lower heights (e.g., ~85 m in one study) — implying that 150 m is above many tested conditions in those specific experiments 

If you need a regulatory or standards LAWN definition, further authoritative references (standards bodies or regulatory documents) would be required; the supplied academic papers do not contain that definition.

Protocols and technologies
This section compares the principal protocols and radio technologies actively researched for low‑altitude BVLOS operations and gives concrete paper examples. The table lists strengths and representative research demonstrations.

Technology	Typical use case and strengths	Representative research examples
LTE / 4G cellular	Ubiquitous baseline C2/payload links; useful in suburban tests and datasets	Field I/Q datasets and aerial drive tests at 30–110 m used to model propagation and plan BVLOS links 

5G (low/mid/mmWave)	Higher throughput, slicing, flexible numerology, potential URLLC; field KPI studies vs LTE	Experimental 5G vs LTE performance studies in non‑urban/suburban areas and recommendations for trajectory control 

mmWave mesh / airborne backhaul	Gigabit backhaul between UAVs for bandwidth‑intense payloads and offloading	SkyHaul autonomous mmWave mesh and prototype UAV backhaul implementations 

UAV-to-UAV D2D and 3GPP sidelink	Low‑latency neighbor awareness, local coordination, collision avoidance	DroneCAST D2D prototypes and 3GPP sidelink‑style scheduling for drone corridors 

Relay UAVs / multi‑hop airborne relays	Extend range where ground infrastructure is sparse, portable field kits	RUCKUS relay‑UAV kit demonstrations and relay‑based BVLOS field tests 

Short‑packet URLLC / beamformed C2	Reliability/BLER optimization, altitude-aware resource allocation for C2	Closed‑form BLER analysis and optimization for maximizing reliable control range 

Full‑duplex + directional antennas	Spectrum efficiency and co‑channel reuse for multi‑UAV systems	Full‑duplex aerial system designs leveraging directional antennas in simulations/prototypes 

Key protocol/standard notes from the corpus:

Researchers test commercial cellular stacks (LTE/5G) for aerial UEs and propose cellular‑aware path planning and BS antenna changes to suit aerial users 

3GPP sidelink concepts and semi‑persistent scheduling are applied to UAV corridors and inter‑UAV communications in simulation studies to reduce coordination latency and interference 

Mesh and relay architectures (mmWave backhaul) appear in prototypes to support high‑bandwidth BVLOS applications that exceed the capacity of single links 

Satellite links (SATCOM) and wide‑area NTN concepts are mentioned in some operational discussions of situational awareness, but the supplied papers do not include detailed experimental SATCOM performance results for the ≤150 m BVLOS case; therefore specific SATCOM performance claims for this altitude are not supported by the provided corpus.

Regulatory and technical requirements
This section summarizes the regulatory and operational demands that appear in the literature for BVLOS operations, and links those to technical mitigations reported in empirical or simulation studies. The main required elements recurring in the papers are reliable C2, DAA, redundancy and proven link reliability.

Command and control reliability and pilot handover: BVLOS operations require proven, redundant C2 links and the ability to hand over control between pilots/operators; MAVLink optimizations and pilot‑handover components were implemented and used successfully in SORA‑approved BVLOS trials to reduce bandwidth and support multi‑pilot control 

Detect‑and‑Avoid and safety equipment: regulatory expectations for BVLOS include reliable DAA and risk mitigation; one prototype study combined cellular C2 with DAA and a parachute fail‑safe for safer BVLOS operation, showing how avionics and communications must be jointly validated 

Link reliability metrics and design targets: studies derive BLER and URLLC‑style design metrics and use those to choose optimal altitudes, blocklengths and transmit power to maximize reliable C2 range—these analyses provide quantitative tools for meeting technical reliability requirements 

Infrastructure and network planning: regulators typically expect evidence of link availability along the planned route; cellular‑aware path‑planning and extensive aerial drive tests are used to quantify reliable coverage and produce mission plans that meet link‑reliability constraints 

Spectrum, interference and antenna configuration: for operations inside drone corridors, base station antenna uptilt and dedicated corridor antennas are proposed as technical measures to meet coverage/reliability expectations and to limit interference impacts on terrestrial users 

Multi‑link and redundancy best practice: the literature repeatedly recommends multi‑link architectures (cellular + D2D + relay/mesh) so that loss of one link does not compromise safety‑critical control or detect‑and‑avoid data 

Caveats and evidence limits:

The reviewed papers document operational demonstrations, datasets and simulation‑level analyses, but specific regulatory altitude cutoffs or universal performance thresholds (e.g., mandatory link availability percent at exact altitudes) are not given in the corpus; regulatory compliance is shown via case studies (SORA trials, field tests) rather than normative altitude bands 

For setting compliance targets you should combine these technical studies with the applicable authority’s BVLOS guidance and SORA‑style risk assessments; the academic literature provides engineering methods and trial evidence but not finalized regulatory thresholds in the supplied set 

If you want, I can extract the quantitative KPIs reported in specific field experiments (latency, BLER, observed height ranges and coverage radii) from individual papers and present them in a concise table so you can use those numbers for risk assessments or system design.

References
[1]
C. Ellis, M. Zhang, and V. Marojevic, “Interference Analysis and Mitigation for UAV Communications in Drone Corridors,” pp. 1–6, Nov. 2023, doi: 10.1109/wpmc59531.2023.10338970.
[2]
“LTE Mobile Network Technical Feasibility for Unmanned Aerial Vehicle BVLOS operations in a Rural Test Area”, [Online]. Available: https://www.sesarju.eu/sites/default/files/documents/sid/2023/Papers/SIDs_2023_paper_28%20final.pdf
[3]
D. Becker and L. M. Schalk, “Toward robust and efficient communications for urban air mobility,” CEAS Aeronautical Journal, Apr. 2024, doi: 10.1007/s13272-024-00738-6.
[4]
E. W. Madewell et al., “Beyond Visual Line-of-Sight Uncrewed Aerial Vehicle for Search and Locate Operations,” Jan. 2024, doi: 10.2514/6.2024-1695.
[5]
“Communications in urban low-altitude drone logistics networks: Requirements, solutions and challenges”, [Online]. Available: https://ieeexplore.ieee.org/abstract/document/11207189/
[6]
“An Overview of Wireless Communication Protocols and Techniques for Drones”, doi: 10.1007/978-981-97-5621-6_29.
[7]
L. Tomaszewski and R. Kolakowski, “Mobile Services for Smart Agriculture and Forestry, Biodiversity Monitoring, and Water Management: Challenges for 5G/6G Networks,” Telecom, vol. 4, no. 1, pp. 67–99, Jan. 2023, doi: 10.3390/telecom4010006.
[8]
D. Horváth, J. Gazda, E. Slapak, T. Maksymyuk, and M. Dohler, “Evolutionary Coverage Optimization for a Self-Organizing UAV-Based Wireless Communication System,” IEEE Access, vol. 9, pp. 145066–145082, Oct. 2021, doi: 10.1109/ACCESS.2021.3121905.
[9]
A. Navarro, C. de Quinto, and J. A. Hern’andez, “Beyond Visual Line of Sight: UAVs with Edge AI, Connected LLMs, and VR for Autonomous Aerial Intelligence,” arXiv.org, vol. abs/2507.15049, July 2025, doi: 10.48550/arxiv.2507.15049.
[10]
S. M. David, “Network for enabling beyond visual line of sight aircraft command and control communications,” Feb. 2021.
[11]
“Mobile Communications and Parachute Systems for Safe Beyond Visual Line of Sight (BVLoS) UAV Operation,” Nov. 2022, doi: 10.1109/istt56288.2022.9966547.
[12]
K. Xiong, J. Xie, and S. Leng, “eVTOL Communication and Trajectory Optimization in Low-Altitude Economy,” pp. 845–850, Aug. 2024, doi: 10.1109/icccworkshops62562.2024.10693789.
[13]
“Full-Duplex Aerial Communication System for Multiple UAVs with Directional Antennas,” Jan. 2022, doi: 10.1109/ccnc49033.2022.9700503.
[14]
G. E. M. Abro, S. A. Zulkifli, R. J. Masood, V. S. Asirvadam, and A. Laouti, “Comprehensive Review of UAV Detection, Security, and Communication Advancements to Prevent Threats,” Drones, vol. 6, no. 10, pp. 284–284, Oct. 2022, doi: 10.3390/drones6100284.
- Therefore, based on the provided literature, there is insufficient evidence to assert that 150 m specifically falls inside a defined LAWN category or to give an official LAWN altitude range; the studies instead report tested altitude ranges and emphasize “low‑altitude” without a universal numeric taxonomy 
    

- For practical planning, note that several experimental datasets and planning studies focus on heights well below or up to ~100–110 m, and some path‑planning/coverage analyses cite reliable 4G aerial coverage only to lower heights (e.g., ~85 m in one study) — implying that 150 m is above many tested conditions in those specific experiments 

If you need a regulatory or standards LAWN definition, further authoritative references (standards bodies or regulatory documents) would be required; the supplied academic papers do not contain that definition.

---

## Protocols and technologies

This section compares the principal protocols and radio technologies actively researched for low‑altitude BVLOS operations and gives concrete paper examples. The table lists strengths and representative research demonstrations.

|Technology|Typical use case and strengths|Representative research examples|
|---|---|---|
|LTE / 4G cellular|Ubiquitous baseline C2/payload links; useful in suburban tests and datasets|Field I/Q datasets and aerial drive tests at 30–110 m used to model propagation and plan BVLOS links <br><br>2<br><br>.|
|5G (low/mid/mmWave)|Higher throughput, slicing, flexible numerology, potential URLLC; field KPI studies vs LTE|Experimental 5G vs LTE performance studies in non‑urban/suburban areas and recommendations for trajectory control <br><br>1<br><br>.|
|mmWave mesh / airborne backhaul|Gigabit backhaul between UAVs for bandwidth‑intense payloads and offloading|SkyHaul autonomous mmWave mesh and prototype UAV backhaul implementations <br><br>3<br><br>.|
|UAV-to-UAV D2D and 3GPP sidelink|Low‑latency neighbor awareness, local coordination, collision avoidance|DroneCAST D2D prototypes and 3GPP sidelink‑style scheduling for drone corridors <br><br>5<br><br> <br><br>4<br><br>.|
|Relay UAVs / multi‑hop airborne relays|Extend range where ground infrastructure is sparse, portable field kits|RUCKUS relay‑UAV kit demonstrations and relay‑based BVLOS field tests <br><br>6<br><br>.|
|Short‑packet URLLC / beamformed C2|Reliability/BLER optimization, altitude-aware resource allocation for C2|Closed‑form BLER analysis and optimization for maximizing reliable control range <br><br>7<br><br>.|
|Full‑duplex + directional antennas|Spectrum efficiency and co‑channel reuse for multi‑UAV systems|Full‑duplex aerial system designs leveraging directional antennas in simulations/prototypes <br><br>11<br><br>.|

Key protocol/standard notes from the corpus:

- Researchers test commercial cellular stacks (LTE/5G) for aerial UEs and propose cellular‑aware path planning and BS antenna changes to suit aerial users 
    

- 3GPP sidelink concepts and semi‑persistent scheduling are applied to UAV corridors and inter‑UAV communications in simulation studies to reduce coordination latency and interference 
    
- Mesh and relay architectures (mmWave backhaul) appear in prototypes to support high‑bandwidth BVLOS applications that exceed the capacity of single links 
   

Satellite links (SATCOM) and wide‑area NTN concepts are mentioned in some operational discussions of situational awareness, but the supplied papers do not include detailed experimental SATCOM performance results for the ≤150 m BVLOS case; therefore specific SATCOM performance claims for this altitude are not supported by the provided corpus.

---

## Regulatory and technical requirements

This section summarizes the regulatory and operational demands that appear in the literature for BVLOS operations, and links those to technical mitigations reported in empirical or simulation studies. The main required elements recurring in the papers are reliable C2, DAA, redundancy and proven link reliability.

- Command and control reliability and pilot handover: BVLOS operations require proven, redundant C2 links and the ability to hand over control between pilots/operators; MAVLink optimizations and pilot‑handover components were implemented and used successfully in SORA‑approved BVLOS trials to reduce bandwidth and support multi‑pilot control 
 
- Detect‑and‑Avoid and safety equipment: regulatory expectations for BVLOS include reliable DAA and risk mitigation; one prototype study combined cellular C2 with DAA and a parachute fail‑safe for safer BVLOS operation, showing how avionics and communications must be jointly validated 
 
- Link reliability metrics and design targets: studies derive BLER and URLLC‑style design metrics and use those to choose optimal altitudes, blocklengths and transmit power to maximize reliable C2 range—these analyses provide quantitative tools for meeting technical reliability requirements 
    
 
- Infrastructure and network planning: regulators typically expect evidence of link availability along the planned route; cellular‑aware path‑planning and extensive aerial drive tests are used to quantify reliable coverage and produce mission plans that meet link‑reliability constraints 
   
- Spectrum, interference and antenna configuration: for operations inside drone corridors, base station antenna uptilt and dedicated corridor antennas are proposed as technical measures to meet coverage/reliability expectations and to limit interference impacts on terrestrial users 
    
 
- Multi‑link and redundancy best practice: the literature repeatedly recommends multi‑link architectures (cellular + D2D + relay/mesh) so that loss of one link does not compromise safety‑critical control or detect‑and‑avoid data 
    
    
Caveats and evidence limits:

- The reviewed papers document operational demonstrations, datasets and simulation‑level analyses, but specific regulatory altitude cutoffs or universal performance thresholds (e.g., mandatory link availability percent at exact altitudes) are not given in the corpus; regulatory compliance is shown via case studies (SORA trials, field tests) rather than normative altitude bands 
    
    
- For setting compliance targets you should combine these technical studies with the applicable authority’s BVLOS guidance and SORA‑style risk assessments; the academic literature provides engineering methods and trial evidence but not finalized regulatory thresholds in the supplied set 
    
    

If you want, I can extract the quantitative KPIs reported in specific field experiments (latency, BLER, observed height ranges and coverage radii) from individual papers and present them in a concise table so you can use those numbers for risk assessments or system design.

References

[1]

C. Ellis, M. Zhang, and V. Marojevic, “Interference Analysis and Mitigation for UAV Communications in Drone Corridors,” pp. 1–6, Nov. 2023, doi: 10.1109/wpmc59531.2023.10338970.

[2]

“LTE Mobile Network Technical Feasibility for Unmanned Aerial Vehicle BVLOS operations in a Rural Test Area”, [Online]. Available: https://www.sesarju.eu/sites/default/files/documents/sid/2023/Papers/SIDs_2023_paper_28%20final.pdf

[3]

D. Becker and L. M. Schalk, “Toward robust and efficient communications for urban air mobility,” _CEAS Aeronautical Journal_, Apr. 2024, doi: 10.1007/s13272-024-00738-6.

[4]

E. W. Madewell _et al._, “Beyond Visual Line-of-Sight Uncrewed Aerial Vehicle for Search and Locate Operations,” Jan. 2024, doi: 10.2514/6.2024-1695.

[5]

“Communications in urban low-altitude drone logistics networks: Requirements, solutions and challenges”, [Online]. Available: https://ieeexplore.ieee.org/abstract/document/11207189/

[6]

“An Overview of Wireless Communication Protocols and Techniques for Drones”, doi: 10.1007/978-981-97-5621-6_29.

[7]

L. Tomaszewski and R. Kolakowski, “Mobile Services for Smart Agriculture and Forestry, Biodiversity Monitoring, and Water Management: Challenges for 5G/6G Networks,” _Telecom_, vol. 4, no. 1, pp. 67–99, Jan. 2023, doi: 10.3390/telecom4010006.

[8]

D. Horváth, J. Gazda, E. Slapak, T. Maksymyuk, and M. Dohler, “Evolutionary Coverage Optimization for a Self-Organizing UAV-Based Wireless Communication System,” _IEEE Access_, vol. 9, pp. 145066–145082, Oct. 2021, doi: 10.1109/ACCESS.2021.3121905.

[9]

A. Navarro, C. de Quinto, and J. A. Hern’andez, “Beyond Visual Line of Sight: UAVs with Edge AI, Connected LLMs, and VR for Autonomous Aerial Intelligence,” _arXiv.org_, vol. abs/2507.15049, July 2025, doi: 10.48550/arxiv.2507.15049.

[10]

S. M. David, “Network for enabling beyond visual line of sight aircraft command and control communications,” Feb. 2021.

[11]

“Mobile Communications and Parachute Systems for Safe Beyond Visual Line of Sight (BVLoS) UAV Operation,” Nov. 2022, doi: 10.1109/istt56288.2022.9966547.

[12]

K. Xiong, J. Xie, and S. Leng, “eVTOL Communication and Trajectory Optimization in Low-Altitude Economy,” pp. 845–850, Aug. 2024, doi: 10.1109/icccworkshops62562.2024.10693789.

[13]

“Full-Duplex Aerial Communication System for Multiple UAVs with Directional Antennas,” Jan. 2022, doi: 10.1109/ccnc49033.2022.9700503.

[14]

G. E. M. Abro, S. A. Zulkifli, R. J. Masood, V. S. Asirvadam, and A. Laouti, “Comprehensive Review of UAV Detection, Security, and Communication Advancements to Prevent Threats,” _Drones_, vol. 6, no. 10, pp. 284–284, Oct. 2022, doi: 10.3390/drones6100284.

---

## TL;DR

U-Space is the EU implementation of drone traffic services under EU Commission regulations, while UTM is the broader, country-agnostic concept and research area for managing low‑altitude unmanned traffic. Key enablers are reliable multi‑channel communications (5G/LTE, satellite, V2X/ADS‑B/RemoteID), edge/cloud computing for low‑latency processing, and AI-driven automation; several testbeds and integration studies demonstrate prototypes and measurement gaps requiring further research.

---

## U-Space and UTM

U-Space denotes the European operational and regulatory implementation of services to enable large‑scale drone operations; UTM denotes the broader, technology‑neutral concept and research activity for managing unmanned air traffic worldwide. Both aim to allow safe coexistence of manned and unmanned aircraft, but U‑Space is explicitly tied to the EU regulatory framework and SESAR/EC program while UTM appears across FAA/NASA and international research efforts.

- U‑Space scope
    - What it is U‑Space is the EU programme and set of services (digitalized, automated procedures) to manage unmanned traffic in low altitude airspace under the Commission Implementing Regulation(s) referenced in the literature 
        
        1
        
        .
    - Regulatory anchor The recent Commission Implementing Regulation (EU) packages are repeatedly referenced as the legal basis for initial U‑Space services in the supplied papers 
        
    
- UTM scope
    - What it is UTM is the general traffic management concept (FAA/NASA and international research roadmaps) that covers architectures, decision‑making models (centralized vs decentralized), and broad service sets for UAS integration into national airspace systems 
        
        
- Key operational concepts
    - Identification and remote ID network‑level identification and RemoteID functions are core U‑Space/UTM services and are implemented experimentally using cellular technologies in the literature 
        
    
    - Traffic information and conflict management in‑flight monitoring, tactical deconfliction and emergency procedures are described as core UTM/U‑Space functions and are validated in prototype architectures and testbeds 
        
    
- On U1–U4 levels
    - The supplied literature describes a progressive set of U‑Space/U TM services from basic identification and geofencing to flight authorization, traffic information and higher automation, but the exact regulatory text enumerating the U1–U4 labels is not reproduced verbatim in the provided papers; the corpus documents implementations and examples that map onto a staged service progression (basic services → pre‑flight authorization → tactical in‑flight services → high automation) 
        
        


---

## Communication technologies and their role

Reliable, multi‑channel airborne communications are described as the fundamental enabler for almost all UTM/U‑Space functions; the literature evaluates cellular (LTE/LTE‑M/5G), non‑terrestrial/satellite links, ADS‑B/RemoteID and bespoke D2X or V2X links as complementary building blocks.

- 5G and LTE family
    - Why important 5G (and 5G system features such as network slicing, URLLC and MEC) is positioned as the preferred terrestrial backbone to support connectivity, QoS differentiation, and low‑latency uplink/downlink for U‑Space services and remote control/telemetry 
        
    - Architectural integration Reference architectures that integrate 5GS and the U‑Space Service Provider domain are proposed and analysed, including business‑model and slicing implications 
        
        
- LTE‑M and Remote ID use
    - Concrete example An implemented prototype (DroneID5G) used LTE‑M to deliver Network Identification/RemoteID to national Common Information Service Providers and demonstrated handover/reliability and altitude effects on RSRP/RSRQ in flight tests 
        
- Non‑terrestrial and future 6G
    - Space‑air‑ground layering Papers argue for adding satellite/non‑terrestrial layers (aerial relays, satcom) in future 6G visions to extend coverage and resilience in dense urban airspace and to provide multi‑layer routing for UTM services 
        
        
- ADS‑B, RemoteID and multi‑channel proposals
    - Legacy and new systems Reviews discuss ADS‑B, RemoteID and ADS‑B‑like approaches and recommend multi‑channel usage (ADS‑B, cellular RemoteID, dedicated V2X) to increase robustness and backwards compatibility 
        
        
    - Multi‑mode transponders Flight trials extending certified transponders with cellular interfaces (Multi‑Mode‑Transceiver) showed improved visibility to ATM and UTM systems while raising antenna/interference and barometric reference issues 
        
        
- Drone‑to‑drone / D2X links and local messaging
    - Experimental systems Dedicated D2X prototypes (drone‑to‑drone/infrastructure) achieved multi‑km ranges with Mbps data rates in field tests, demonstrating a complementary short/medium range channel for neighbor awareness or DAA messaging 
        
        
- Field measurement warnings
    - Gaps in current networks Urban measurement campaigns report that existing cellular networks were not planned for aerial coverage and show significant KPI degradation and interference issues at altitude — indicating upgrades are needed before relying solely on terrestrial 5G deployments for U‑Space operations 
        
    
---

## Edge computing contributions and applications

Edge computing (MEC/fog/edge AI) is presented as the operational fabric that reduces latency, offloads heavy perception and decision workloads from constrained UAS, and enables local, time‑critical UTM functions.

- Why edge matters for UTM/U‑Space
    - Latency and autonomy Time‑critical services (BVLOS control, dynamic geofencing, rapid conflict resolution) require sub‑second response that is difficult to achieve with distant cloud resources; placing compute near the radio edge or at telco MEC nodes enables those constraints to be met 
        

    - Onboard limits Offloading perception (computer vision), DAA processing, and mission planning to nearby edge servers extends drone capabilities while conserving onboard weight and power 
    
- Specific applications demonstrated
    - Geofencing and BVLOS control A real 5G+edge implementation demonstrated dynamic geofencing and BVLOS control for a delivery drone by offloading computation to an edge node and using 5G for control/telemetry 
        
        
    - Service orchestration and placement Papers propose MEC+NFV orchestration frameworks and solve placement/ILP models to locate UTM services across cloud and MEC to satisfy heterogeneous QoS (URLLC vs best‑effort) 
        
        
    - Distributed UTM/testbeds EuroDRONE and other testbeds operate distributed cloud/edge elements (DroNav and on‑platform transponders) to implement redundancy, local conflict prevention, and asset management 
        
        
- Benefits
    - Lower latency and higher reliability for tactical decisions and DAA close to the aircraft 
        
        
    - Scalability and QoS mapping via network slicing and NFV so different UAS services receive appropriate resources 
       
    - Enablement of edge AI for computer vision, anomaly detection and automated deconfliction without heavy uplink to central clouds 
        
    
---

## Other key enablers and limitations

This section summarizes other technologies cited in the corpus, noting where evidence is present and where it is absent.

- AI and machine learning
    - Role AI/ML enables perception (CV for DAA), autonomous navigation, path planning, conflict prediction and trustable decision‑making; edge AI convergence work surveys these roles and practical challenges (model offloading, freshness, resource constraints) 
    
- Blockchain
    - Evidence in corpus Insufficient evidence — the supplied papers do not present substantive, peer‑documented blockchain implementations for UTM/U‑Space, so no corpus‑backed assessment can be given.
- Cloud computing and NFV
    - Role Cloud (central) and NFV are used for orchestration, historical flight plan storage, large‑scale analytics and failover; NFV/MANO integration with UTM is proposed to place functions across cloud and MEC layers 
        
      
- IoT integration
    - Role UAVs act as IoT nodes and can both consume and provide sensing/communications in smart‑city use cases; surveys discuss IoT‑UAV synergies, data privacy and large‑scale traffic management implications 
    
- Positioning and navigation systems
    - Technologies GNSS remains primary, but cooperative surveillance (ADS‑B, RemoteID, ADS‑B‑like, cellular‑based location) and sensor fusion are emphasized; multi‑mode solutions (transponder + cellular) improve visibility but raise altimetry and interference challenges 
        
 
- Detect and Avoid (DAA) systems
    - Implementations Papers demonstrate DAA by relaying Traffic Information into flight controllers, cooperative DAA using ADS‑B/RemoteID, Wi‑Fi‑based local messaging for separation and multi‑channel strategies for robustness 
        

- Security and Authentication
    - Concerns Communication integrity and lightweight authentication are identified as open needs for UTM; surveys call for secure architectures for links such as ADS‑B and RemoteID because constrained UAS platforms cannot always run conventional crypto stacks 
        
        
---

## Architectures, services, challenges and recent implementations

This closing section sketches typical U‑Space/UTM architecture components, lists key operational services and prototypes, outlines main challenges and research directions, and points to recent developments (2022–2024/early 2025 evidence in the corpus).

- Common architectural components
    - Stakeholders and nodes Typical architectures include UAS operators, U‑Space Service Providers (USSPs), national Common Information Service Providers (CISPs), edge/MEC nodes, cloud control planes and cooperative surveillance sensors/transponders as shown in prototype integrations and testbeds 
        

    
    - Service planes Architectures described in the literature split functions into identification and registration, flight authorization, traffic information and tactical deconfliction, and orchestration/analytics layers hosted across MEC and cloud 
        
    
    - C2 and data links Command‑and‑control (C2) links, telemetry channels, RemoteID/ADS‑B feeds and local V2V/D2X channels are combined in multi‑channel proposals to improve resilience 
        

- Representative services and examples
    - Network Identification / RemoteID Implemented using LTE‑M in the DroneID5G prototype following EU 2021/664 mandates; flight tests measured handovers and link quality at different altitudes 
        
    

    - In‑flight tactical deconfliction and emergency management Implemented in open‑source UTM system prototypes and validated in simulation/remote operator tests 
        
      
    - Highly automated testbeds EuroDRONE used DroNav cloud software + hardware transponders to demonstrate distributed conflict prevention/resolution and asset management 
        
    
- Main technical challenges
    - Communications coverage and interference Cellular networks were often not designed for aerial coverage; urban measurements show KPI degradation at altitude and interference, implying the need for planning and upgrades 
     
    - Heterogeneous integration Combining ADS‑B, RemoteID, cellular, D2X and satellite links while avoiding mutual interference and ensuring consistent semantics is nontrivial 
        
    
    - Security and lightweight authentication Constrained UAS platforms require tailored cryptographic/authentication solutions for UTM messaging 
        
      
    - Scalability and decision‑making Centralized vs decentralized decision tradeoffs, state consistency, and real‑time guarantees under packet loss are active research areas 
        
        

    - DAA for non‑cooperative targets Detecting and safely responding to non‑cooperative intruders remains a core research and testing need 
    
- Future research directions highlighted
    - Edge/cloud orchestration algorithms placement and slicing mechanisms that jointly consider airspace use and radio resources 
        
    
    - Multi‑layer communications research combining terrestrial, aerial relays and satellites for resilience and dense urban capacity 
        
    
    - Robust distributed decision making for decentralized UTM and resilience to imperfect data and packet loss 
    
    - Edge AI pipelines and verification certifiable ML for safety‑critical perception and DAA running at the edge 
 
    - Security architectures lightweight secure protocols and authentication for RemoteID/ADS‑B/UTM APIs 
 
- Recent developments and implementations (2022–2024 cited)
    - DroneID5G (2023) LTE‑M prototype implementing Network Identification and demonstrating RemoteID messaging and DAA relays in flight tests 

    - Edge‑driven geofencing and BVLOS case study (2023) 5G + MEC real system showing dynamic geofencing/BVLOS control for delivery drones 

    - EuroDRONE testbed demonstrations (2019–2022 reporting) distributed DroNav + transponder architecture validating automated conflict resolution in European U‑Space test activities 
        
      
    - MEC/NFV orchestration proposals ILP placement schemes and service orchestration frameworks tailored for UTM services 
        
    
    - 5G aerial coverage measurements campaigns in dense urban settings showing limitations of current networks and calling for aerial‑aware planning 
    
    - Surveys and roadmaps multiple 2021–2024 surveys and roadmaps summarize UTM/U‑Space evolution, integration challenges and high‑priority research needs 
        

---

References

[1]

S. Si-Mohammed _et al._, “Supporting Unmanned Aerial Vehicle Services in 5G Networks: New High-Level Architecture Integrating 5G With U-Space,” _IEEE Vehicular Technology Magazine_, vol. 16, no. 1, pp. 57–65, Mar. 2021, doi: 10.1109/MVT.2020.3036374.

[2]

J. H. Jepsen, R. Singh, and K. B. Jensen, “Investigating the applicability of LTE-M for Network Identification of Unmanned Aerial Systems in U-Space,” pp. 616–625, June 2023, doi: 10.1109/ICUAS57906.2023.10156338.

[3]

“Toward a UTM-based Service Orchestration for UAVs in MEC-NFV Environment,” Jan. 2022, doi: 10.48550/arxiv.2201.00994.

[4]

T. Taleb, A. Ksentini, H. Hellaoui, and O. Bekkouche, “On Supporting UAV Based Services in 5G and Beyond Mobile Systems,” _IEEE Network_, vol. 35, no. 4, pp. 220–227, July 2021, doi: 10.1109/MNET.021.2000358.

[5]

J. H. Jepsen, K. H. Laursen, and K. V. Jensen, “A survey of state-of-the-art U-space research,” Feb. 2024, doi: 10.1109/icara60736.2024.10552989.

[6]

V. Lappas _et al._, “EuroDRONE, a European Unmanned Traffic Management Testbed for U-Space,” _Drones_, vol. 6, no. 2, pp. 53–53, Feb. 2022, doi: 10.3390/drones6020053.

[7]

S. Al-Rubaye, A. Tsourdos, and K. Namuduri, “Advanced Air Mobility Operation and Infrastructure for Sustainable Connected eVTOL Vehicle,” _Drones_, vol. 7, no. 5, pp. 319–319, May 2023, doi: 10.3390/drones7050319.

[8]

V. Lappas _et al._, “EuroDRONE, A European UTM Testbed for U-Space,” Sept. 2020, doi: 10.1109/ICUAS48674.2020.9214020.

[9]

L. Tomaszewski, R. Kolakowski, and S. Kuklinski, “Integration of U-space and 5GS for UAV services,” pp. 767–772, June 2020.

[10]

R. Shrestha, R. Bajracharya, and S. Kim, “6G Enabled Unmanned Aerial Vehicle Traffic Management: A Perspective,” _IEEE Access_, vol. 9, pp. 91119–91136, June 2021, doi: 10.1109/ACCESS.2021.3092039.

[11]

E. Vinogradov, F. Minucci, and S. Pollin, “Wireless Communication for Safe UAVs: From Long-Range Deconfliction to Short-Range Collision Avoidance,” _IEEE Vehicular Technology Magazine_, vol. 15, no. 2, pp. 88–95, Apr. 2020, doi: 10.1109/MVT.2020.2980014.

[12]

A. Schelle, F. Völk, R. T. Schwarz, A. Knopp, and P. Stütz, “Evaluation of a Multi-Mode-Transceiver for Enhanced UAV Visibility and Connectivity in Mixed ATM/UTM Contexts,” _Drones_, vol. 6, no. 4, pp. 80–80, Mar. 2022, doi: 10.3390/drones6040080.

[13]

S. K. Das, “Urban Air Mobility: Vision, Challenges and Opportunities,” pp. 1–6, June 2023, doi: 10.1109/HPSR57248.2023.10148014.

[14]

“Urban Air Mobility: Vision, Challenges and Opportunities,” June 2023, doi: 10.1109/hpsr57248.2023.10148014.

[15]

N. S. Labib, M. R. Brust, G. Danoy, and P. Bouvry, “The Rise of Drones in Internet of Things: A Survey on the Evolution, Prospects and Challenges of Unmanned Aerial Vehicles,” _IEEE Access_, vol. 9, pp. 115466–115487, Aug. 2021, doi: 10.1109/ACCESS.2021.3104963.

[16]

M. Y. Arafat and S. Pan, “Urban Air Mobility Communications and Networking: Recent Advances, Techniques, and Challenges,” _Drones_, vol. 8, no. 12, pp. 702–702, Nov. 2024, doi: 10.3390/drones8120702.

[17]

K. L. Best _et al._, “How to Analyze the Cyber Threat from Drones,” Jan. 2020.

[18]

J. Lieb, G. Peklar, L. Mustafa, and J. Beyerstedt, “Paving the Way Towards a Comprehensive UTM Infrastructure by Evaluating Novel D2X Communication Systems for UAVS in Flight Tests,” pp. 1–9, Apr. 2022, doi: 10.1109/ICNS54818.2022.9771504.

[19]

A. Hamissi and A. Dhraief, “A Survey On The Unmanned Aircraft System Traffic Management,” _ACM Computing Surveys_, Sept. 2023, doi: 10.1145/3617992.

[20]

G. Singh, R. A. Pashchapur, and H. Ballal, “Recent Trends on UAS-UTM Ecosystem and Integration Challenges,” June 2024, doi: 10.1109/icuas60882.2024.10556851.

[21]

A. Bera, Y. Drif, J. Querol, and M. Olivares-Mendez, “Implementation of Edge-driven Geofencing and BVLOS Control for 5G-enabled Delivery Drone,” pp. 68–73, Dec. 2023, doi: 10.1109/gcwkshps58843.2023.10464731.

---
# Autonomous Cross-Layer Resource Orchestration for Ultra-Reliable BVLOS Communication via Coded Heterogeneous Networks

## I. Strategic Context: The Regulatory and Technical Imperative for C2 Resilience

The proposed research direction—combining heterogeneous multi-link communication (Wi-Fi, 5G, Satellite) with Network Coding (NC) to enhance safety and reliability for Beyond Visual Line of Sight (BVLOS) operations—is exceptionally relevant and addresses the fundamental bottleneck to commercial and regulatory acceptance of widespread unmanned aerial systems (UAS). The safe normalization of BVLOS operations, spanning critical sectors such as infrastructure inspection, emergency response, and logistics and long-distance cargo delivery 1, is entirely contingent upon demonstrating guaranteed, uninterrupted communication for Command and Control (C2) traffic.3

### The Requirement for Ultra-Reliable Low-Latency Communication (URLLC)

Regulatory bodies, including the FAA and organizations contributing to 3GPP standards, have established rigorous performance objectives that define the boundary between acceptable operational risk and safety non-compliance.4 These standards transform the reliability goal from a technical aspiration into a non-negotiable safety mandate. Specifically, C2 communication must meet stringent Quality of Service (QoS) requirements, which have been formalized in specifications such as 3GPP Release 18.

The performance objectives vary dramatically depending on the operational mode, confirming the necessity of a flexible, adaptive communication system. For the most safety-critical functions, such as **'Direct stick steering,'** the communication system must provide an End-to-End Latency of **40 milliseconds (ms)** and an application-layer **Reliability of 99.9%**.5 Other functions, such as 'Steer to waypoints,' maintain the 99.9% reliability target but permit a longer latency of 1 second.5 Even video utilized to aid control in non-Visual Line of Sight (non-VLOS), which is synonymous with BVLOS, must achieve 99.9% reliability with a latency ceiling of 140 ms.5

The attainment of the 99.9% reliability figure under all operational conditions is crucial because it directly correlates with the reduction of residual operational risk. Global aviation safety frameworks often employ a scaled approach to authorization, where certification obligations increase with the residual risk introduced by the service.6 By mathematically proving that the proposed technical solution can sustain communication reliability above the mandatory threshold, even during periods of correlated link failure or extreme interference, the research provides quantifiable evidence that the probability of C2 loss is minimized. This, in turn, facilitates the necessary reduction in residual risk required for broad regulatory approval, functioning as the key safety gate for commercial deployment.

### Complexity of Traffic Differentiation

The pronounced differences in required QoS metrics—ranging from ultra-low latency (40 ms for critical maneuvers) to moderately higher latency (5 seconds for ‘Automatic flight on UTM’) 5—preclude the use of a unified, statically provisioned communication policy. An efficient multi-link system must incorporate dynamic traffic differentiation. High-priority, safety-critical traffic must receive maximum resources and coded redundancy, whereas routine telemetry or less time-sensitive route updates (which can tolerate up to 30-second uplink interruptions 5) can utilize less power-intensive or lower-rate backup links. This selective application of high-cost resources, such as advanced network coding and high-power transmitters, is essential for preserving the UAV's limited battery life, ensuring operational endurance, and maximizing energy efficiency.

## II. Heterogeneous Multi-Connectivity: Architecture, Limitations, and Link Constraints

A multi-link architecture comprising Terrestrial-Non-Terrestrial Networks (TNTNs) is indispensable for achieving ubiquitous coverage and robust fault tolerance required for true BVLOS scalability.7 However, simply aggregating disparate links (Wi-Fi, 5G, Satellite) without intelligent management introduces complexity and efficiency challenges.

### Limitations of Constituent Links

Each communication technology presents unique constraints that must be overcome through intelligent system design:

1. **Wi-Fi/Proprietary Links:** While robust proprietary Wi-Fi solutions exist for long-distance communication (via optimizations in the Medium Access Control layer 9), their fundamental constraint is limited range (signal strength degrades rapidly beyond 2 to 3 kilometers) and high susceptibility to interference in densely populated areas utilizing the 2.4 GHz and 5.8 GHz bands.3 Local mesh networks, such as those leveraging Dedicated Short-Range Communications (DSRC) or Cellular Vehicle-to-Everything (C-V2X) infrastructure, are valuable for specific integrated environments but remain highly sensitive to terrain, vegetation, and building obstructions.11
    
2. **5G/Cellular Networks:** Terrestrial cellular networks provide high bandwidth capacity but pose significant challenges for aerial platforms. Drones operate with three-dimensional mobility, experiencing unique propagation characteristics and complexities in managing handovers between multiple ground base stations.10 Ensuring consistent, low-latency communication requires dynamic spectrum, power, and handover management protocols to mitigate the risks associated with rapid, high-altitude transitions.10
    
3. **Satellite Communication (Satcom):** Satcom is necessary for truly global or intercontinental reach, especially when operating far beyond the range of terrestrial 5G infrastructure.12 However, Satcom introduces severe system constraints. High-orbit satellites impose problematic latency unsuitable for real-time C2 (40 ms required).5 Low-orbit (LEO) systems mitigate latency but require frequent, complex handovers and must compensate for Doppler effects.12 Critically, the hardware required for high-bandwidth streaming via satellite is often bulky, heavy (terminals enabling streaming and C2 typically weigh around 1.5 kilograms), and power-hungry, substantially reducing the drone's payload capacity and performance—the defining Size, Weight, and Power (SWaP) constraint.3
    

### The SWaP-Latency Trade-off and Edge Intelligence Necessity

The combination of the strict 40 ms latency requirement for safety-critical C2 and the severe SWaP penalty associated with high-capacity satellite terminals dictates a critical design compromise. The research cannot justify utilizing the expensive, heavy satellite link purely for bulk data throughput, as this limits mission scope and range.3 Instead, the multi-link system must be optimized to reserve the satellite link almost exclusively for low-rate, safety-critical _redundancy_ of the C2 channel (as a last-resort, ultra-reliable backup), utilizing 5G/Wi-Fi for high-bandwidth telemetry and payload data whenever possible.

Furthermore, managing the transition between these heterogeneous links—such as handovers between a 5G cell and a Low Earth Orbit (LEO) satellite beam—is inherently complex and highly sensitive to latency.13 Centralized control solutions are often too slow to react to the rapid 3D topology changes of a UAV network.10 This compels the implementation of onboard, distributed (edge) intelligence, such as machine learning models, to predict signal strength and optimize the handover scheduling algorithm, thereby reducing handover latency significantly and enhancing network stability.14

## III. Network Coding: The Enabler of Efficient Coded Reliability

The combination of heterogeneous links creates highly dynamic, intermittent, and potentially non-correlated communication paths, which is necessary for redundancy but challenging for simple link aggregation. Network Coding (NC) provides the mathematical foundation for converting this redundant architecture into Ultra-Reliable Low-Latency Communication (URLLC).

### Theoretical Superiority of Network Coding

NC schemes, such as Random Linear Network Coding (RLNC) or Complex Field Network Coding (CFNC) 15, enhance reliability by exploiting spatial diversity gains across multiple links or relays.15 Crucially, NC enables the destination to recover the original message from _any_ subset of coded packets, provided enough independent combinations are received. This mechanism is profoundly superior to simple packet replication or duplication (where an entire identical packet must be received via a backup link) because it efficiently uses all available bandwidth.16

For a dynamic aerial channel characterized by fading, intermittent link availability, and external disturbances 17, RLNC is demonstrably more bandwidth-efficient. Quantitative analyses show that RLNC can achieve lower average redundancy per delivered packet, especially in moderate packet loss regimes, compared to simple replication.18 This efficiency gain is critical for bandwidth-constrained UAV platforms 19, where minimizing unnecessary transmission overhead directly impacts energy consumption and operational duration.

Table 1: Comparative Analysis of Redundancy Techniques for BVLOS C2 Traffic

|**Mechanism**|**Reliability Achieved**|**Bandwidth Overhead**|**Diversity Gain**|**Computational Complexity (Onboard)**|**Efficiency in Lossy Links**|
|---|---|---|---|---|---|
|Simple Packet Replication (Duplication)|High, if paths are independent|Extremely High (2x or more)|Path Diversity|Low|Inefficient (wastes capacity)|
|Random Linear Network Coding (RLNC)|Ultra-High (Coding and Path Diversity)|Moderate (Based on dynamic $k/n$)|High|Moderate (Requires optimization)|Excellent (Optimal bandwidth use in high erasure regimes) 18|
|Link Bonding (Non-Coded)|High (Guarantees uptime)|Low (Optimized flow control)|Link Availability|Low|Vulnerable (Fails under correlated deep fades)|

### The Cross-Layer Optimization Problem

While NC can be implemented at a high level—for instance, as an IP-layer module using netfilter frameworks, thus remaining invisible to the layers above and below 18—its maximum potential is only unlocked through a **Cross-Layer Design**.20 In traditional layered network architectures, the coding strategy (network layer decision) remains ignorant of the physical characteristics of the underlying links (PHY/MAC layer state). In dynamic wireless channels, this leads to sub-optimal performance.

The PhD research must address this gap by establishing a formal cross-layer framework. This framework defines the specific protocol interface that allows real-time physical layer metrics—such as predicted channel fading, interference levels, Signal-to-Noise Ratio (SNR), and instantaneous packet loss probability—to dynamically adjust the Network Coding rate ($k/n$) at the network layer. Only by coordinating these layers can the system calculate the minimum required coding redundancy needed to achieve the 99.9% reliability target at that precise moment, thereby minimizing energy consumption and end-to-end latency.21 This Cross-Layer NC Optimization Problem forms the theoretical core of the novelty.

## IV. Defining Novelty: The Intelligent Cross-Layer Optimization Framework

The central challenge in integrated TNTN UAV networks is the dynamic management of power, bandwidth, link selection, and coding redundancy under real-time SWaP and latency constraints.23 This highly complex, time-varying environment exceeds the capability of traditional optimization techniques such as logistic regression or Support Vector Machines (SVM) due to the sheer dimensionality of the state space.23

### Leveraging Deep Reinforcement Learning (DRL)

Reinforcement Learning (RL) provides the ideal solution because it is designed to optimize long-term outcomes (e.g., maximizing mission duration or reliability) in environments with uncertain dynamics.24 Furthermore, the complexity of integrating terrestrial, satellite, and mobile ad hoc network (MANET) characteristics necessitates a distributed control approach. Multi-Agent Deep Deterministic Policy Gradient (MADDPG) algorithms have already demonstrated success in solving resource allocation, user association, and power control problems within integrated terrestrial-satellite networks.8

### Proposed Solution: Hierarchical Multi-Agent Deep Reinforcement Learning (H-MADRL)

The definitive novelty lies in the development of a **Hierarchical Multi-Agent Deep Reinforcement Learning (H-MADRL)** framework tailored specifically for the multi-link, coded UAV communication problem.25 This architecture divides control responsibilities to manage both macro-level strategic planning and micro-level packet handling.

1. **High-Level Agent (Centralized/Cloud):** This agent typically resides at the Ground Control Station (GCS) or a centralized edge cloud. It is responsible for long-term strategic decisions, including overall flight trajectory optimization, non-real-time resource provisioning, and managing large-scale coordination, such as anticipating handovers between major network segments (e.g., from a 5G metropolitan area to a satellite-only region).23
    
2. **Low-Level Agent (Distributed/Onboard):** This agent is integrated into the UAV’s onboard communication computer, reflecting the need for edge computing capabilities.26 Its function is to perform instantaneous, real-time control actions. The low-level agent's key role is the **dynamic tuning of the Network Coding redundancy rate ($k/n$)** for each C2 packet based on immediate channel measurements received from the cross-layer interface. It also handles instantaneous power control for the active radios and high-frequency link selection decisions.25
    

The architectural advantage of the H-MADRL framework is its scalability. While centralized algorithms suffer from decision time increases as the number of access points grows (up to a 90% increase when doubling APs), distributed approaches maintain performance while offering significantly better scalability.25

### Strategic Integration of Reliability and Efficiency

The core intellectual contribution of the H-MADRL design centers on the reward function. The agent is trained not just to guarantee communication, but to do so _efficiently_. The reward structure must be mathematically formulated to heavily penalize any failure to maintain the 99.9% reliability threshold while simultaneously penalizing the application of excessive coding redundancy ($n/k$). By driving the system to be 'just reliable enough' to meet the non-negotiable safety criteria without wasting bandwidth or battery power, the research directly solves the dual problem of regulatory safety compliance and commercial practicality.

To ensure the Low-Level Agent is practical and adheres to strict SWaP constraints, the architectural design must integrate energy-efficient AI. Implementing the learning algorithms using architectures such as Spiking Neural Networks (SNNs) can significantly reduce the power consumption of the onboard AI processor, extending operational time and enabling crucial real-time processing capabilities for critical, low-latency applications like collision avoidance and dynamic C2 management.27

## V. Practical Implementation, Validation, and PhD Roadmap

Transitioning this theoretical framework into a practical, demonstrable system requires a structured roadmap that addresses analytical modeling, high-fidelity simulation, and eventual field validation.

### Onboard System Architecture and Constraints

The physical realization of this research involves creating an integrated onboard communication module, similar to commercial platforms designed for AI and remote link aggregation.28 This module must house the heterogeneous radio interfaces, an IP-layer NC engine capable of real-time encoding/decoding, and the low-SWaP edge processor dedicated to executing the Low-Level H-MADRL agent. The design must prioritize maintaining a minimal SWaP profile while maximizing real-time processing capability, ensuring minimal latency in all C2-critical loops.27

### Phased Validation Strategy

#### Phase 1: Analytical and Link-Level Simulation

The initial phase focuses on establishing the mathematical superiority of the Coded Multi-Link approach. This involves developing an analytical model that precisely links measurable inputs from the Physical (PHY) and Medium Access Control (MAC) layers—such as instantaneous packet erasure probability or predicted link blockage—to the required Network Coding redundancy rate ($k/n$) necessary to maintain 99.9% application-layer reliability. This phase proves the theoretical efficiency of dynamic NC against simple link aggregation or static-rate NC schemes under controlled, simulated intermittent channel conditions.15

#### Phase 2: Network-Level Simulation and H-MADRL Validation

The second phase employs high-fidelity network simulators (optimized for 3D mobility and dynamic topology) to validate the performance of the full H-MADRL framework. The simulations must focus on complex, realistic BVLOS scenarios involving multiple, concurrent link failures (e.g., 5G coverage dropping combined with temporary satellite occlusion). Performance must be benchmarked against standard resource allocation policies (such as simple Q-learning or static primary/backup link selection).8 Success metrics include demonstrating maximized energy efficiency, minimum necessary coding overhead, and achieving significant latency reduction compared to non-optimized handover schemes (research suggests potential reductions exceeding 21 times compared to standard Non-Terrestrial Network handover schemes are achievable through optimized scheduling).14

#### Phase 3: Field Trials and Regulatory Compliance Demonstration

The final validation phase involves moving from simulation to physical field trials, ideally in collaboration with established UAS research consortia or test facilities.30 The primary goal of these trials is to demonstrate the sustained performance of the Coded Multi-Link system against the mandatory 3GPP KPIs under real-world, atmospheric, and mobility challenges. The deployment must show that the system can maintain C2 reliability above $99.9\%$ and latency below $40\text{ ms}$ for safety-critical traffic, even when external environmental conditions deliberately degrade or force the failure of one or more primary communication links. This practical demonstration validates the solution’s practicality and maturity for regulatory acceptance.

## VI. Conclusion and Forward Outlook

The proposed PhD research trajectory is highly relevant, technically sound, and strategically positioned to deliver a novel and practical contribution to the field of communication technology for drones. The fundamental hypothesis—that a combination of heterogeneous connectivity (Wi-Fi, 5G, Satellite) and Network Coding will provide superior safety and reliability for BVLOS operations—is robust and aligns with global industry and regulatory roadmaps.

The path to achieving novel and practical results lies specifically in two tightly interconnected contributions:

1. **Cross-Layer Network Coding Optimization:** Developing the mathematical model and the interface necessary to dynamically adapt the NC redundancy rate based on real-time channel state information from the physical layer. This ensures that the system is _efficiently reliable_ by using the minimum necessary bandwidth to achieve the required 99.9% safety threshold.
    
2. **Intelligent Orchestration via H-MADRL:** Implementing a novel Hierarchical Multi-Agent Deep Reinforcement Learning framework to autonomously manage the dynamic resource allocation, link selection, power control, and NC parameters across the complex Terrestrial-Non-Terrestrial Network structure.
    

By focusing on these areas and rigorously validating the performance against the stringent 40 ms latency and 99.9% reliability criteria, the research will deliver a solution that is both theoretically sophisticated and commercially viable within strict SWaP constraints.

Future research extending from this work should focus on integrating this URLLC C2 backbone with distributed computing architectures. This would enable resource sharing and cooperative task execution in multi-UAV swarms, where the resilient coded backbone could support computationally intensive tasks, such as collaborative deep learning or complex networked airborne computing, directly addressing the limitations of single UAV resource capacity.

### can the research be done without AI and ML? 

This is an excellent question that goes to the heart of the research’s novelty and practical value.

While the fundamental components of your proposed system—multi-link aggregation (Wi-Fi, 5G, Satellite) and Network Coding (NC)—can certainly be designed using traditional, non-AI optimization methods, excluding Artificial Intelligence (AI) and Machine Learning (ML) would significantly compromise the project's ability to achieve the ultra-high performance and efficiency required for commercial and regulatory approval of Beyond Visual Line of Sight (BVLOS) operations.

In essence, AI/ML is the required catalyst that transforms a theoretically redundant system into a highly dynamic, practically _efficient_ system.

Here is a detailed breakdown of why AI and ML are critical to meeting the practical and novelty objectives of your proposed work:

### 1. Handling Dynamic Complexity and High Dimensionality

Traditional optimization techniques, such as logistic regression or Support Vector Machines (SVM), have historically been applied to resource allocation problems in aerial networks. However, they struggle to cope with the unique and highly dynamic environment of a heterogeneous multi-link system in 3D space:  

- **Complexity:** A UAV operating BVLOS is subject to constantly changing channel conditions (fading, interference), rapid 3D mobility, and the non-correlated link status of Wi-Fi, 5G, and Low Earth Orbit (LEO) satellite connections.  
    
- **High-Dimensionality:** Managing the integrated terrestrial-satellite network involves optimizing several concurrent parameters in real-time: link selection, power control, user association, and, in your case, the Network Coding redundancy rate. Simple rule-based logic or non-ML approaches like basic Q-learning are often deemed inadequate due to the high dimensionality of the state space.  
    
- **Novelty:** The use of complex, non-AI algorithms (such as some hybrid optimization heuristics in Flying Ad Hoc Networks ) exists, but the cutting-edge novelty lies in using Deep Reinforcement Learning (DRL) techniques, such as the Multi-Agent Deep Deterministic Policy Gradient (MADDPG) algorithm, which are proven to surpass conventional single-agent learning approaches in addressing resource allocation challenges in integrated terrestrial-satellite networks.  
    

### 2. Achieving Ultra-Low Latency Handover

One of the most critical challenges for BVLOS operation is maintaining the Command and Control (C2) link during handover, especially when the required latency for direct control is only 40 milliseconds. This is where AI offers a massive practical advantage:

- **Predictive Handover:** Simple, non-ML handover schemes rely on reactive decision-making based on current signal strength thresholds. In contrast, integrating a machine learning model for **signal strength prediction** allows the system to proactively schedule the handover to a new link (e.g., switching from 5G to Satellite coverage) before the current link degrades.  
    
- **Quantifiable Performance Gain:** Research demonstrates that using AI-based signal prediction coupled with an efficient handover scheduling algorithm can reduce handover latency by up to **21 times** compared to standard Non-Terrestrial Network (NTN) handover schemes. This level of performance improvement is essential to practically guarantee the sub-40 ms C2 requirement.  
    

### 3. Dynamic Cross-Layer Efficiency (The Core of the Thesis)

The core intellectual contribution of your work is likely the **dynamic optimization of the Network Coding (NC) rate (k/n)** to achieve the 99.9% reliability target with minimum bandwidth overhead.

- **Inefficiency without AI:** Without a real-time, intelligent system, the NC module would be forced to use a conservative, **static redundancy rate** (e.g., sending two or three coded packets for every data packet) to ensure reliability under worst-case link conditions. This constant over-provisioning would dramatically increase bandwidth overhead and consume the UAV’s limited battery life.
    
- **AI-Driven Efficiency:** A Deep Reinforcement Learning (DRL) agent is designed to dynamically calculate the _minimum_ necessary redundancy needed to achieve the 99.9% reliability based on instantaneous, cross-layer channel information (e.g., current packet erasure probability). The agent's reward function can be optimized to penalize excessive redundancy while strictly penalizing reliability failure. This process drives the system to be _just reliable enough_, maximizing energy efficiency and operational endurance.  
    

In summary, while you could build a multi-link, coded prototype without ML using rule-based or conventional mathematical optimization, that system would be energy-inefficient, prone to significant latency spikes during handovers, and likely unable to consistently meet the strict 40 ms latency and 99.9% reliability Key Performance Indicators (KPIs) in realistic, dynamic BVLOS environments. The use of AI/ML, particularly the **Hierarchical Multi-Agent DRL framework** proposed in the research plan, is the defining component that provides the **novelty** and the **practical performance** necessary for a PhD-level contribution.

----
PhD flowchart for review and organizing  v1 from 12/11
![[PhD-Flowchart-v1.pdf]]