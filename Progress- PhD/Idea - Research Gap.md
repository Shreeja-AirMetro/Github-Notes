**<span style="color:rgb(0, 176, 80)">Topic I:  Multi-Link Communication for UAV in BVLOS and its Integration with Data Mesh and Age of Information for UAM Networks</span>**
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