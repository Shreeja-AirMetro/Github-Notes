Here are concise, research-direction bullets summarizing what Enrique Caballero, Aymen Fakhreddine and Christian Bettstetter (Univ. of Klagenfurt) work on in the area of drones, with sources.

1. Interference between drones and terrestrial 4G/5G users — simulation studies showing uplink interference from airborne UAVs can strongly degrade ground-user SIR/throughput; they model drones with 3GPP path-loss and use the Vienna 5G System-Level Simulator. [ACM Digital Library+1](https://dl.acm.org/doi/10.1145/3597060.3597238?utm_source=chatgpt.com)
    
2. Handover and mobility challenges for cellular-connected drones — investigation of cell association, frequent handovers and their impact on connection reliability when UAVs use terrestrial cellular infrastructure. [Semantic Scholar+1](https://www.semanticscholar.org/paper/Handover-Challenges-for-Cellular-Connected-Drones-Fakhreddine-Bettstetter/924cad733e7a20bc65d63f96476c57e13532752d?utm_source=chatgpt.com)
    
3. Drone-mounted access points and experimental evaluation of cellular/LTE performance for UAVs — measurements and experiments to assess achievable throughput and practical limits when drones act as clients or flying access points. [ACM Digital Library+1](https://dl.acm.org/doi/10.1145/3469259.3470489?utm_source=chatgpt.com)
    
4. Integration of multi-drone systems into cellular networks (5G / 6G) — designing techniques and architectures to safely and efficiently operate fleets of UAVs over existing and future mobile networks. [ResearchGate+1](https://www.researchgate.net/profile/Enrique-Caballero-Garces-2?utm_source=chatgpt.com)
    
5. Path planning, job selection and autonomous mission coordination for small/mini drone systems — combining communications-aware path planning and self-organization for applications such as area monitoring, search & rescue and delivery. [bettstetter.com+1](https://bettstetter.com/research/uav/?utm_source=chatgpt.com)
    
6. Use of realistic simulators + empirical setups — they combine system-level simulators (Vienna 5G SLS) with drone-specific 3GPP models and field experiments to validate findings. [ACM Digital Library+1](https://dl.acm.org/doi/pdf/10.1145/3597060.3597238?utm_source=chatgpt.com)
    
7. Focus on wireless-network effects (interference, relaying, synchronization) and practical deployment considerations for UAVs in mobile networks — a lab emphasis visible across Bettstetter’s group publications and project pages. [bettstetter.com+1](https://bettstetter.com/?utm_source=chatgpt.com)
    

18/9 first meeting

- Publication 
- Throughput 
Enrique 
- Aerospace engg
- Drones, Haps worked 
- EASA needs redundancy - SLA assurance - 
- C2 3GPP 
- Data rate is availability , latency and integrity 
- Cellular connected drones : Interference mitigation and 
- side -two secondary beams 
- frq reuse - inteferer in ulink 
- leverage RSRP 
- 5G VCCS System level simulator 
- 36.777 - higher handover 
- handover strategy 
Power control at UAV level alleviated this effect without comm 
Ost fally - Drone-to-drone Aerial mobility DAA, COnflict comm
TACT - NR+ 
Degredation of the link 
take off-landing - radio environment - pathloss  35m 
FASTER 
<span style="color:rgb(255, 0, 0)"><span style="color:rgb(255, 0, 0)"><span style="color:rgb(0, 0, 0)">TUM -  system link level urban mobility</span> </span></span>
Step by Step breakdown 
Research proposal 
Gantt chart 
Macro plan of the stay
Wi-Fi sensing 
Spectrum analysis 

Skills: 
	 - System level simulation 
	 - Physical RF aspects Air to ground 
	 - MATLAB, Python, C++
Accommodation 

---
29/10 
Questions 

1. C2 on Simulator 
2. Housing 

Introduce - C2 - 5G and 
Hanger to Hospital 
Hanger in Wi - Fi 
AAM, IAM, UAM  . Plug address specific 
UAM - drones within urban  - UAM and IAM interchangeable in drones AAM is bigger bubble 
convertible AAM 

IAM bubble Urban  and Regional 
MEO sat -Balloon company 
ulogs for GPS 
C2 and CNPC - aeronautical - aviation  | EU - C2

to dos: 
Image for Introduction 

Q: to work with ROS2 
Lab implement ROS2  
 - Implement the ROS 2  Website 

- University of Colorado - input from ns3 
- asymmetry in downlink - uplink bytes/sec - application data channel - aerial users 
- C2 distribution functions
- 4G, 5G hard handover - smooth for UAVs 
- first Monday of the month presentation 

- Share repository Omnet++ - Enrique 

kornelia.lienbacher@aau.at 

---

1. Refining my PhD scope and key topics
12/1 comments from Bettstetter
- [ ] heterogeneous link paper
- [ ] There is no intra handover in 5G there was soft handover in GSMA and begining LTE because CDMA and same frequency between cells 
- [ ] Vertical handover between technologies 
- [ ] TX switch energy where cellular no more available
- [ ] Make sure to address / highlight the challenges of drones specifically this will increase the novelty 
- [ ] Begin the focus to research questions 
- [ ] is height estimation relavant to satellite as it is relavant to cellular 
- [ ] What is C2 as protocol how mavlink became a protocol how to build a protocol 
- [ ] how many research on drones in satellite communication and then how multi-technology framework build into this overview
- [ ] what are specific scenarios like flying in alps during avalanche for rescue
- [ ] In terms of communication Satcom can be backup does this applies to C2 - command and control. How is this different if put equally 
#### to dos 

- [ ] Simulator parameters
- [ ] read code, cleanup code 
- [ ] setup simulator for Enrique
- [ ] Run sumo simulation for frames
- [ ] Run sumo simulation - implement paket 
- [ ] Data collection 
- [ ] Aerial UE implemetation 
- [ ] State of art and research focus - slide 

### MEETING IN 2 WEEKS -  Deadline 26.01 




---
Resilience 
The term _resilience_ in this context refers to the capabilities that a system must possess in order to deal effectively with unanticipated events.[[1]](https://en.wikipedia.org/wiki/Resilience_engineering#cite_note-1) Resilience engineering examines how systems build, sustain, degrade, and lose these capabilities.[[2]](https://en.wikipedia.org/wiki/Resilience_engineering#cite_note-:5-2)

Resilience engineering researchers have studied multiple safety-critical [domains](https://en.wikipedia.org/wiki/Domain_knowledge "Domain knowledge"), including [aviation](https://en.wikipedia.org/wiki/Aviation "Aviation"), [anesthesia](https://en.wikipedia.org/wiki/Anesthesia "Anesthesia"), [fire safety](https://en.wikipedia.org/wiki/Fire_safety "Fire safety"), space mission control, [military operations](https://en.wikipedia.org/wiki/Military_operation "Military operation"), power plants, air traffic control, [rail engineering](https://en.wikipedia.org/wiki/Railway_engineering "Railway engineering"), health care, and emergency response to both natural and industrial disasters.[[2]](https://en.wikipedia.org/wiki/Resilience_engineering#cite_note-:5-2)[[3]](https://en.wikipedia.org/wiki/Resilience_engineering#cite_note-:2-3)[[4]](https://en.wikipedia.org/wiki/Resilience_engineering#cite_note-:3-4) Resilience engineering researchers have also studied the non-safety-critical domain of software operations.[[5]](https://en.wikipedia.org/wiki/Resilience_engineering#cite_note-5)

Hollnagel perspective -  Resilient performance as requiring four systemic potentials:[[19]](https://en.wikipedia.org/wiki/Resilience_engineering#cite_note-19)

1. The potential to respond
2. The potential to monitor
3. The potential to learn
4. The potential to anticipate.

This has been described in a White Paper from Eurocontrol on Systemic Potentials Management [https://skybrary.aero/bookshelf/systemic-potentials-management-building-basis-resilient-performance](https://skybrary.aero/bookshelf/systemic-potentials-management-building-basis-resilient-performance)

ICAO - https://www.icao.int/sites/default/files/EURNAT/Documents/EUR%20and%20Nat%20Docs/EURNAT-DGCA%20Meetings/EURNAT-DGCA%202024/EURNATDGCA2024-WP04-AppA-EURDoc031.pdf

Crisis A state where nominal and contingency procedures and resources are no longer adequate Resilience A set of properties that: • Protects against disruption • Support a quick recovery after a disruption Air Transportation System The complete set of elements that are necessary for the execution of air transport as defined in the Chicago convention, e.g.:
A Black Swan effect is a metaphor for an unpredictable, high-impact event that is irrationalized in hindsight.

Risk assessment 
ALARP (As Low As Reasonably Practicable). Such criteria have major flaws such as: • What is reasonable? • What is practicable?
