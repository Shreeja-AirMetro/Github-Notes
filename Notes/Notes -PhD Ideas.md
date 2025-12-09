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