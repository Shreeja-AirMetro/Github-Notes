Drones at ≤150 m BVLOS are being studied primarily with cellular (LTE/5G) links, mmWave mesh/backhaul, UAV-to-UAV (D2D) links, and relay/UAV-swarm techniques. Main challenges are coverage, interference, reliability and regulatory safety (C2 redundancy, DAA); many papers test solutions via antenna uptilt, beamforming, relays, and link/path planning.

---

## Research trends

This section summarizes the dominant architectures, hardware, and algorithmic trends researchers are pursuing for low-altitude BVLOS communications and points to representative experiments and prototypes. The emphasis in recent (2023–2025) work is on leveraging commercial cellular networks while adding aerial‑specific radio designs and airborne mesh/relay links.

- Cellular-connected drones are a major focus for BVLOS C2 and payload links; field KPI comparisons across low- and mid-band 5G versus LTE show active experimental evaluation of coverage and performance for aerial UEs 
    
    1
    
    .
- Experimental datasets and flight tests for LTE at low altitudes (30–110 m) are available and used to build aerial propagation models and ML methods for aerial coverage prediction 
    
    2
    
    .
- High-throughput, low-latency airborne backhaul using mmWave mesh links is demonstrated in prototypes that place UAVs as self-organizing mmWave relays/backhaul nodes to support bandwidth‑intensive BVLOS applications 
    
    3
    
    .
- Aerial beamforming, directional antennas and mmWave sidelink strategies are proposed to mitigate inter‑UAV interference and improve reliability in drone corridors 
    
    4
    
    .
- Drone-to-drone (D2D) and sidelink approaches (including 3GPP‑style sidelink/semi‑persistent scheduling) plus dedicated UAV D2D prototypes are being developed for fast local coordination and redundancy in urban airspaces 
    
    5
    
    .
- Relay‑UAV concepts (e.g., portable relay kits) and multi‑UAV relays are used in field demonstrations to extend and harden BVLOS links without relying solely on ground infrastructure 
    
    6
    
    .
- Radio‑layer optimizations for reliability (short‑packet/URLLC design, BLER analysis, altitude-aware resource allocation) and antenna geometry tuning (uptilted BS antennas for corridors) are active topics to maximize reliable C2 ranges 
    
    7
    
     
    
    8
    
    .
- Recent demos integrate edge processing, 5G links and onboard AI to reduce latency and data backhaul needs while maintaining robust 5G connectivity in BVLOS scenarios 
    
    9
    
    .

Representative citations for the above experimental and simulation advances are available in the literature 

1

 

2

 

3

 

4

 

5

 

6

 

7

 

8

 

9

.

---

## Challenges and solutions

This section frames the principal technical problems for BVLOS at low altitude and lists the concrete solutions validated or proposed in the literature, with examples of supporting studies. The main problems are coverage gaps, interference/visibility to many cells, link reliability and safety‑critical redundancy.

- Coverage holes and antenna geometry: existing cellular BS antennas are down‑tilted for ground UEs, creating reduced coverage at altitude; studies quantify optimal BS uptilt/additional antenna use to maximize corridor coverage and reduce coverage holes 
    
    8
    
    .
- Interference and multi‑node coexistence: aerial UEs become visible to many towers and to other UAVs, increasing interference; mmWave beamforming and narrow directional transmissions substantially reduce intra‑airspace interference and increase link reliability in simulations and prototypes 
    
    4
    
    .
- Reliability and latency for C2: short‑packet and URLLC‑style design (blocklength, power allocation, beamforming) can be optimized to maximize reliable control range and identify favorable altitude/resource tradeoffs for control links 
    
    7
    
    .
- Sparse/non‑urban coverage: cellular coverage outside urban areas can be unreliable for BVLOS; field studies compare LTE vs 5G performance and recommend path/trajectory control and cellular‑aware planning to improve link availability 
    
    1
    
     
    
    2
    
    .
- Local redundancy and range extension: relay UAVs and self‑organizing UAV meshes provide mission‑level redundancy and gigabit backhaul where ground infrastructure is insufficient; SkyHaul‑style mmWave mesh and relay UAV kits have been prototyped to sustain high‑bandwidth BVLOS services 
    
    3
    
     
    
    6
    
    .
- Fast local coordination and DAA assistance: D2D/sidelink communications (ad hoc or 3GPP‑style sidelink scheduling) provide low-latency neighbor awareness for collision avoidance and Complementary Detect‑and‑Avoid (DAA) links 
    
    5
    
    .
- Practical avionics/stack optimizations: MAVLink compression and pilot‑handover components have been field‑tested to reduce required C2 bandwidth and allow approved BVLOS operations under SORA‑like frameworks 
    
    10
    
    .

Example solution-to-challenge mapping (bulleted):

- Coverage uplift: BS uptilt and corridor‑specific antenna patterns to increase probability of coverage 
    
    8
    
    .
- Interference mitigation: mmWave beamforming and directional antennas on UAVs and ground nodes 
    
    4
    
     
    
    11
    
    .
- Range/availability: relay UAVs and mmWave mesh as airborne backhaul 
    
    3
    
     
    
    6
    
    .
- C2 reliability: short‑packet optimization and altitude-aware resource allocation (BLER analysis) 
    
    7
    
    .
- Operational redundancy: D2D/sidelink plus multi‑link designs to complement cellular C2 
    
    5
    
    .

---

## LAWN classification

This section states whether ≤150 m BVLOS fits the LAWN term and reports what the supplied literature says about altitude labels. The corpus does not provide a formal, citable definition or explicit altitude bands for the term LAWN, so a definitive classification cannot be supported from these papers.

- The supplied papers use terms such as "low‑altitude", "drone corridors" and report experimental altitudes (e.g., LTE flight datasets at 30–110 m and cellular coverage assessments with reliable 4G coverage noted toward ~85 m), but none of the reviewed articles defines a standard LAWN altitude envelope or publishes an authoritative LAWN specification 
    
    Drones at ≤150 m BVLOS are being studied primarily with cellular (LTE/5G) links, mmWave mesh/backhaul, UAV-to-UAV (D2D) links, and relay/UAV-swarm techniques. Main challenges are coverage, interference, reliability and regulatory safety (C2 redundancy, DAA); many papers test solutions via antenna uptilt, beamforming, relays, and link/path planning.

Research trends
This section summarizes the dominant architectures, hardware, and algorithmic trends researchers are pursuing for low-altitude BVLOS communications and points to representative experiments and prototypes. The emphasis in recent (2023–2025) work is on leveraging commercial cellular networks while adding aerial‑specific radio designs and airborne mesh/relay links.

Cellular-connected drones are a major focus for BVLOS C2 and payload links; field KPI comparisons across low- and mid-band 5G versus LTE show active experimental evaluation of coverage and performance for aerial UEs 
1
.
Experimental datasets and flight tests for LTE at low altitudes (30–110 m) are available and used to build aerial propagation models and ML methods for aerial coverage prediction 
2
.
High-throughput, low-latency airborne backhaul using mmWave mesh links is demonstrated in prototypes that place UAVs as self-organizing mmWave relays/backhaul nodes to support bandwidth‑intensive BVLOS applications 
3
.
Aerial beamforming, directional antennas and mmWave sidelink strategies are proposed to mitigate inter‑UAV interference and improve reliability in drone corridors 
4
.
Drone-to-drone (D2D) and sidelink approaches (including 3GPP‑style sidelink/semi‑persistent scheduling) plus dedicated UAV D2D prototypes are being developed for fast local coordination and redundancy in urban airspaces 
5
.
Relay‑UAV concepts (e.g., portable relay kits) and multi‑UAV relays are used in field demonstrations to extend and harden BVLOS links without relying solely on ground infrastructure 
6
.
Radio‑layer optimizations for reliability (short‑packet/URLLC design, BLER analysis, altitude-aware resource allocation) and antenna geometry tuning (uptilted BS antennas for corridors) are active topics to maximize reliable C2 ranges 
7
 
8
.
Recent demos integrate edge processing, 5G links and onboard AI to reduce latency and data backhaul needs while maintaining robust 5G connectivity in BVLOS scenarios 
9
.
Representative citations for the above experimental and simulation advances are available in the literature 
1
 
2
 
3
 
4
 
5
 
6
 
7
 
8
 
9
.

Challenges and solutions
This section frames the principal technical problems for BVLOS at low altitude and lists the concrete solutions validated or proposed in the literature, with examples of supporting studies. The main problems are coverage gaps, interference/visibility to many cells, link reliability and safety‑critical redundancy.

Coverage holes and antenna geometry: existing cellular BS antennas are down‑tilted for ground UEs, creating reduced coverage at altitude; studies quantify optimal BS uptilt/additional antenna use to maximize corridor coverage and reduce coverage holes 
8
.
Interference and multi‑node coexistence: aerial UEs become visible to many towers and to other UAVs, increasing interference; mmWave beamforming and narrow directional transmissions substantially reduce intra‑airspace interference and increase link reliability in simulations and prototypes 
4
.
Reliability and latency for C2: short‑packet and URLLC‑style design (blocklength, power allocation, beamforming) can be optimized to maximize reliable control range and identify favorable altitude/resource tradeoffs for control links 
7
.
Sparse/non‑urban coverage: cellular coverage outside urban areas can be unreliable for BVLOS; field studies compare LTE vs 5G performance and recommend path/trajectory control and cellular‑aware planning to improve link availability 
1
 
2
.
Local redundancy and range extension: relay UAVs and self‑organizing UAV meshes provide mission‑level redundancy and gigabit backhaul where ground infrastructure is insufficient; SkyHaul‑style mmWave mesh and relay UAV kits have been prototyped to sustain high‑bandwidth BVLOS services 
3
 
6
.
Fast local coordination and DAA assistance: D2D/sidelink communications (ad hoc or 3GPP‑style sidelink scheduling) provide low-latency neighbor awareness for collision avoidance and Complementary Detect‑and‑Avoid (DAA) links 
5
.
Practical avionics/stack optimizations: MAVLink compression and pilot‑handover components have been field‑tested to reduce required C2 bandwidth and allow approved BVLOS operations under SORA‑like frameworks 
10
.
Example solution-to-challenge mapping (bulleted):

Coverage uplift: BS uptilt and corridor‑specific antenna patterns to increase probability of coverage 
8
.
Interference mitigation: mmWave beamforming and directional antennas on UAVs and ground nodes 
4
 
11
.
Range/availability: relay UAVs and mmWave mesh as airborne backhaul 
3
 
6
.
C2 reliability: short‑packet optimization and altitude-aware resource allocation (BLER analysis) 
7
.
Operational redundancy: D2D/sidelink plus multi‑link designs to complement cellular C2 
5
.
LAWN classification
This section states whether ≤150 m BVLOS fits the LAWN term and reports what the supplied literature says about altitude labels. The corpus does not provide a formal, citable definition or explicit altitude bands for the term LAWN, so a definitive classification cannot be supported from these papers.

The supplied papers use terms such as "low‑altitude", "drone corridors" and report experimental altitudes (e.g., LTE flight datasets at 30–110 m and cellular coverage assessments with reliable 4G coverage noted toward ~85 m), but none of the reviewed articles defines a standard LAWN altitude envelope or publishes an authoritative LAWN specification 
2
 
12
.
Therefore, based on the provided literature, there is insufficient evidence to assert that 150 m specifically falls inside a defined LAWN category or to give an official LAWN altitude range; the studies instead report tested altitude ranges and emphasize “low‑altitude” without a universal numeric taxonomy 
2
 
12
.
For practical planning, note that several experimental datasets and planning studies focus on heights well below or up to ~100–110 m, and some path‑planning/coverage analyses cite reliable 4G aerial coverage only to lower heights (e.g., ~85 m in one study) — implying that 150 m is above many tested conditions in those specific experiments 
2
 
12
.
If you need a regulatory or standards LAWN definition, further authoritative references (standards bodies or regulatory documents) would be required; the supplied academic papers do not contain that definition.

Protocols and technologies
This section compares the principal protocols and radio technologies actively researched for low‑altitude BVLOS operations and gives concrete paper examples. The table lists strengths and representative research demonstrations.

Technology	Typical use case and strengths	Representative research examples
LTE / 4G cellular	Ubiquitous baseline C2/payload links; useful in suburban tests and datasets	Field I/Q datasets and aerial drive tests at 30–110 m used to model propagation and plan BVLOS links 
2
.
5G (low/mid/mmWave)	Higher throughput, slicing, flexible numerology, potential URLLC; field KPI studies vs LTE	Experimental 5G vs LTE performance studies in non‑urban/suburban areas and recommendations for trajectory control 
1
.
mmWave mesh / airborne backhaul	Gigabit backhaul between UAVs for bandwidth‑intense payloads and offloading	SkyHaul autonomous mmWave mesh and prototype UAV backhaul implementations 
3
.
UAV-to-UAV D2D and 3GPP sidelink	Low‑latency neighbor awareness, local coordination, collision avoidance	DroneCAST D2D prototypes and 3GPP sidelink‑style scheduling for drone corridors 
5
 
4
.
Relay UAVs / multi‑hop airborne relays	Extend range where ground infrastructure is sparse, portable field kits	RUCKUS relay‑UAV kit demonstrations and relay‑based BVLOS field tests 
6
.
Short‑packet URLLC / beamformed C2	Reliability/BLER optimization, altitude-aware resource allocation for C2	Closed‑form BLER analysis and optimization for maximizing reliable control range 
7
.
Full‑duplex + directional antennas	Spectrum efficiency and co‑channel reuse for multi‑UAV systems	Full‑duplex aerial system designs leveraging directional antennas in simulations/prototypes 
11
.
Key protocol/standard notes from the corpus:

Researchers test commercial cellular stacks (LTE/5G) for aerial UEs and propose cellular‑aware path planning and BS antenna changes to suit aerial users 
1
 
2
 
8
.
3GPP sidelink concepts and semi‑persistent scheduling are applied to UAV corridors and inter‑UAV communications in simulation studies to reduce coordination latency and interference 
4
.
Mesh and relay architectures (mmWave backhaul) appear in prototypes to support high‑bandwidth BVLOS applications that exceed the capacity of single links 
3
.
Satellite links (SATCOM) and wide‑area NTN concepts are mentioned in some operational discussions of situational awareness, but the supplied papers do not include detailed experimental SATCOM performance results for the ≤150 m BVLOS case; therefore specific SATCOM performance claims for this altitude are not supported by the provided corpus.

Regulatory and technical requirements
This section summarizes the regulatory and operational demands that appear in the literature for BVLOS operations, and links those to technical mitigations reported in empirical or simulation studies. The main required elements recurring in the papers are reliable C2, DAA, redundancy and proven link reliability.

Command and control reliability and pilot handover: BVLOS operations require proven, redundant C2 links and the ability to hand over control between pilots/operators; MAVLink optimizations and pilot‑handover components were implemented and used successfully in SORA‑approved BVLOS trials to reduce bandwidth and support multi‑pilot control 
10
.
Detect‑and‑Avoid and safety equipment: regulatory expectations for BVLOS include reliable DAA and risk mitigation; one prototype study combined cellular C2 with DAA and a parachute fail‑safe for safer BVLOS operation, showing how avionics and communications must be jointly validated 
13
.
Link reliability metrics and design targets: studies derive BLER and URLLC‑style design metrics and use those to choose optimal altitudes, blocklengths and transmit power to maximize reliable C2 range—these analyses provide quantitative tools for meeting technical reliability requirements 
7
.
Infrastructure and network planning: regulators typically expect evidence of link availability along the planned route; cellular‑aware path‑planning and extensive aerial drive tests are used to quantify reliable coverage and produce mission plans that meet link‑reliability constraints 
12
.
Spectrum, interference and antenna configuration: for operations inside drone corridors, base station antenna uptilt and dedicated corridor antennas are proposed as technical measures to meet coverage/reliability expectations and to limit interference impacts on terrestrial users 
8
.
Multi‑link and redundancy best practice: the literature repeatedly recommends multi‑link architectures (cellular + D2D + relay/mesh) so that loss of one link does not compromise safety‑critical control or detect‑and‑avoid data 
3
 
5
 
6
.
Caveats and evidence limits:

The reviewed papers document operational demonstrations, datasets and simulation‑level analyses, but specific regulatory altitude cutoffs or universal performance thresholds (e.g., mandatory link availability percent at exact altitudes) are not given in the corpus; regulatory compliance is shown via case studies (SORA trials, field tests) rather than normative altitude bands 
10
 
13
 
12
.
For setting compliance targets you should combine these technical studies with the applicable authority’s BVLOS guidance and SORA‑style risk assessments; the academic literature provides engineering methods and trial evidence but not finalized regulatory thresholds in the supplied set 
14
 
12
.
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
    
    2
    
     
    
    12
    
    .
- For practical planning, note that several experimental datasets and planning studies focus on heights well below or up to ~100–110 m, and some path‑planning/coverage analyses cite reliable 4G aerial coverage only to lower heights (e.g., ~85 m in one study) — implying that 150 m is above many tested conditions in those specific experiments 
    
    2
    
     
    
    12
    
    .

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
    
    1
    
     
    
    2
    
     
    
    8
    
    .
- 3GPP sidelink concepts and semi‑persistent scheduling are applied to UAV corridors and inter‑UAV communications in simulation studies to reduce coordination latency and interference 
    
    4
    
    .
- Mesh and relay architectures (mmWave backhaul) appear in prototypes to support high‑bandwidth BVLOS applications that exceed the capacity of single links 
    
    3
    
    .

Satellite links (SATCOM) and wide‑area NTN concepts are mentioned in some operational discussions of situational awareness, but the supplied papers do not include detailed experimental SATCOM performance results for the ≤150 m BVLOS case; therefore specific SATCOM performance claims for this altitude are not supported by the provided corpus.

---

## Regulatory and technical requirements

This section summarizes the regulatory and operational demands that appear in the literature for BVLOS operations, and links those to technical mitigations reported in empirical or simulation studies. The main required elements recurring in the papers are reliable C2, DAA, redundancy and proven link reliability.

- Command and control reliability and pilot handover: BVLOS operations require proven, redundant C2 links and the ability to hand over control between pilots/operators; MAVLink optimizations and pilot‑handover components were implemented and used successfully in SORA‑approved BVLOS trials to reduce bandwidth and support multi‑pilot control 
    
    10
    
    .
- Detect‑and‑Avoid and safety equipment: regulatory expectations for BVLOS include reliable DAA and risk mitigation; one prototype study combined cellular C2 with DAA and a parachute fail‑safe for safer BVLOS operation, showing how avionics and communications must be jointly validated 
    
    13
    
    .
- Link reliability metrics and design targets: studies derive BLER and URLLC‑style design metrics and use those to choose optimal altitudes, blocklengths and transmit power to maximize reliable C2 range—these analyses provide quantitative tools for meeting technical reliability requirements 
    
    7
    
    .
- Infrastructure and network planning: regulators typically expect evidence of link availability along the planned route; cellular‑aware path‑planning and extensive aerial drive tests are used to quantify reliable coverage and produce mission plans that meet link‑reliability constraints 
    
    12
    
    .
- Spectrum, interference and antenna configuration: for operations inside drone corridors, base station antenna uptilt and dedicated corridor antennas are proposed as technical measures to meet coverage/reliability expectations and to limit interference impacts on terrestrial users 
    
    8
    
    .
- Multi‑link and redundancy best practice: the literature repeatedly recommends multi‑link architectures (cellular + D2D + relay/mesh) so that loss of one link does not compromise safety‑critical control or detect‑and‑avoid data 
    
    3
    
     
    
    5
    
     
    
    6
    
    .

Caveats and evidence limits:

- The reviewed papers document operational demonstrations, datasets and simulation‑level analyses, but specific regulatory altitude cutoffs or universal performance thresholds (e.g., mandatory link availability percent at exact altitudes) are not given in the corpus; regulatory compliance is shown via case studies (SORA trials, field tests) rather than normative altitude bands 
    
    10
    
     
    
    13
    
     
    
    12
    
    .
- For setting compliance targets you should combine these technical studies with the applicable authority’s BVLOS guidance and SORA‑style risk assessments; the academic literature provides engineering methods and trial evidence but not finalized regulatory thresholds in the supplied set 
    
    14
    
     
    
    12
    
    .

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
        
        1
        
        .
- UTM scope
    - What it is UTM is the general traffic management concept (FAA/NASA and international research roadmaps) that covers architectures, decision‑making models (centralized vs decentralized), and broad service sets for UAS integration into national airspace systems 
        
        2
        
        .
- Key operational concepts
    - Identification and remote ID network‑level identification and RemoteID functions are core U‑Space/UTM services and are implemented experimentally using cellular technologies in the literature 
        
        3
        
        .
    - Traffic information and conflict management in‑flight monitoring, tactical deconfliction and emergency procedures are described as core UTM/U‑Space functions and are validated in prototype architectures and testbeds 
        
        2
        
         
        
        4
        
        .
- On U1–U4 levels
    - The supplied literature describes a progressive set of U‑Space/U TM services from basic identification and geofencing to flight authorization, traffic information and higher automation, but the exact regulatory text enumerating the U1–U4 labels is not reproduced verbatim in the provided papers; the corpus documents implementations and examples that map onto a staged service progression (basic services → pre‑flight authorization → tactical in‑flight services → high automation) 
        
        3
        
         
        
        2
        
         
        
        4
        
        .

1

 

5

---

## Communication technologies and their role

Reliable, multi‑channel airborne communications are described as the fundamental enabler for almost all UTM/U‑Space functions; the literature evaluates cellular (LTE/LTE‑M/5G), non‑terrestrial/satellite links, ADS‑B/RemoteID and bespoke D2X or V2X links as complementary building blocks.

- 5G and LTE family
    - Why important 5G (and 5G system features such as network slicing, URLLC and MEC) is positioned as the preferred terrestrial backbone to support connectivity, QoS differentiation, and low‑latency uplink/downlink for U‑Space services and remote control/telemetry 
        
    - Architectural integration Reference architectures that integrate 5GS and the U‑Space Service Provider domain are proposed and analysed, including business‑model and slicing implications 
        
        
        .
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
        
        17
        
        .

14

 

6

 

4

 

15

 

10

 

9

 

3

 

16

 

17

---

## Architectures, services, challenges and recent implementations

This closing section sketches typical U‑Space/UTM architecture components, lists key operational services and prototypes, outlines main challenges and research directions, and points to recent developments (2022–2024/early 2025 evidence in the corpus).

- Common architectural components
    - Stakeholders and nodes Typical architectures include UAS operators, U‑Space Service Providers (USSPs), national Common Information Service Providers (CISPs), edge/MEC nodes, cloud control planes and cooperative surveillance sensors/transponders as shown in prototype integrations and testbeds 
        
        3
        
         
        
        7
        
         
        
        4
        
        .
    - Service planes Architectures described in the literature split functions into identification and registration, flight authorization, traffic information and tactical deconfliction, and orchestration/analytics layers hosted across MEC and cloud 
        
        2
        
         
        
        6
        
         
        
        4
        
        .
    - C2 and data links Command‑and‑control (C2) links, telemetry channels, RemoteID/ADS‑B feeds and local V2V/D2X channels are combined in multi‑channel proposals to improve resilience 
        
        18
        
         
        
        11
        
         
        
        9
        
        .
- Representative services and examples
    - Network Identification / RemoteID Implemented using LTE‑M in the DroneID5G prototype following EU 2021/664 mandates; flight tests measured handovers and link quality at different altitudes 
        
        3
        
        .
    - In‑flight tactical deconfliction and emergency management Implemented in open‑source UTM system prototypes and validated in simulation/remote operator tests 
        
        2
        
        .
    - Highly automated testbeds EuroDRONE used DroNav cloud software + hardware transponders to demonstrate distributed conflict prevention/resolution and asset management 
        
        4
        
        .
- Main technical challenges
    - Communications coverage and interference Cellular networks were often not designed for aerial coverage; urban measurements show KPI degradation at altitude and interference, implying the need for planning and upgrades 
        
        12
        
        .
    - Heterogeneous integration Combining ADS‑B, RemoteID, cellular, D2X and satellite links while avoiding mutual interference and ensuring consistent semantics is nontrivial 
        
        10
        
         
        
        9
        
         
        
        11
        
        .
    - Security and lightweight authentication Constrained UAS platforms require tailored cryptographic/authentication solutions for UTM messaging 
        
        17
        
        .
    - Scalability and decision‑making Centralized vs decentralized decision tradeoffs, state consistency, and real‑time guarantees under packet loss are active research areas 
        
        2
        
         
        
        19
        
        .
    - DAA for non‑cooperative targets Detecting and safely responding to non‑cooperative intruders remains a core research and testing need 
        
        16
        
         
        
        18
        
        .
- Future research directions highlighted
    - Edge/cloud orchestration algorithms placement and slicing mechanisms that jointly consider airspace use and radio resources 
        
        6
        
        .
    - Multi‑layer communications research combining terrestrial, aerial relays and satellites for resilience and dense urban capacity 
        
        8
        
         
        
        12
        
        .
    - Robust distributed decision making for decentralized UTM and resilience to imperfect data and packet loss 
        
        2
        
        .
    - Edge AI pipelines and verification certifiable ML for safety‑critical perception and DAA running at the edge 
        
        14
        
        .
    - Security architectures lightweight secure protocols and authentication for RemoteID/ADS‑B/UTM APIs 
        
        17
        
        .
- Recent developments and implementations (2022–2024 cited)
    - DroneID5G (2023) LTE‑M prototype implementing Network Identification and demonstrating RemoteID messaging and DAA relays in flight tests 
        
        3
        
        .
    - Edge‑driven geofencing and BVLOS case study (2023) 5G + MEC real system showing dynamic geofencing/BVLOS control for delivery drones 
        
        13
        
        .
    - EuroDRONE testbed demonstrations (2019–2022 reporting) distributed DroNav + transponder architecture validating automated conflict resolution in European U‑Space test activities 
        
        4
        
        .
    - MEC/NFV orchestration proposals ILP placement schemes and service orchestration frameworks tailored for UTM services 
        
        6
        
        .
    - 5G aerial coverage measurements campaigns in dense urban settings showing limitations of current networks and calling for aerial‑aware planning 
        
        12
        
        .
    - Surveys and roadmaps multiple 2021–2024 surveys and roadmaps summarize UTM/U‑Space evolution, integration challenges and high‑priority research needs 
        
        1
        
         
        
        2
        
         
        
        20
        
         
        
        19
        
        .

3

 

13

 

4

 

6

 

12

 

14

 

17

 

2

 

11

 

9

 

8

 

21

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