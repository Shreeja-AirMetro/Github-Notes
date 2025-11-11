

Drones at ≤150 m BVLOS are being studied primarily with cellular (LTE/5G) links, mmWave mesh/backhaul, UAV-to-UAV (D2D) links, and relay/UAV-swarm techniques. Main challenges are coverage, interference, reliability and regulatory safety (C2 redundancy, DAA); many papers test solutions via antenna uptilt, beamforming, relays, and link/path planning.

----

## Research trends

This section summarizes the dominant architectures, hardware, and algorithmic trends researchers are pursuing for low-altitude BVLOS communications and points to representative experiments and prototypes. The emphasis in recent (2023–2025) work is on leveraging commercial cellular networks while adding aerial‑specific radio designs and airborne mesh/relay links.

- Cellular-connected drones are a major focus for BVLOS C2 and payload links; field KPI comparisons across low- and mid-band 5G versus LTE show active experimental evaluation of coverage and performance for aerial UEs [1].  
- Experimental datasets and flight tests for LTE at low altitudes (30–110 m) are available and used to build aerial propagation models and ML methods for aerial coverage prediction [2].  
- High-throughput, low-latency airborne backhaul using mmWave mesh links is demonstrated in prototypes that place UAVs as self-organizing mmWave relays/backhaul nodes to support bandwidth‑intensive BVLOS applications [3].  
- Aerial beamforming, directional antennas and mmWave sidelink strategies are proposed to mitigate inter‑UAV interference and improve reliability in drone corridors [4].  
- Drone-to-drone (D2D) and sidelink approaches (including 3GPP‑style sidelink/semi‑persistent scheduling) plus dedicated UAV D2D prototypes are being developed for fast local coordination and redundancy in urban airspaces [5].  
- Relay‑UAV concepts (e.g., portable relay kits) and multi‑UAV relays are used in field demonstrations to extend and harden BVLOS links without relying solely on ground infrastructure [6].  
- Radio‑layer optimizations for reliability (short‑packet/URLLC design, BLER analysis, altitude-aware resource allocation) and antenna geometry tuning (uptilted BS antennas for corridors) are active topics to maximize reliable C2 ranges [7] [8].  
- Recent demos integrate edge processing, 5G links and onboard AI to reduce latency and data backhaul needs while maintaining robust 5G connectivity in BVLOS scenarios [9].

Representative citations for the above experimental and simulation advances are available in the literature [1] [2] [3] [4] [5] [6] [7] [8] [9].

----

## Challenges and solutions

This section frames the principal technical problems for BVLOS at low altitude and lists the concrete solutions validated or proposed in the literature, with examples of supporting studies. The main problems are coverage gaps, interference/visibility to many cells, link reliability and safety‑critical redundancy.

- Coverage holes and antenna geometry: existing cellular BS antennas are down‑tilted for ground UEs, creating reduced coverage at altitude; studies quantify optimal BS uptilt/additional antenna use to maximize corridor coverage and reduce coverage holes [8].  
- Interference and multi‑node coexistence: aerial UEs become visible to many towers and to other UAVs, increasing interference; mmWave beamforming and narrow directional transmissions substantially reduce intra‑airspace interference and increase link reliability in simulations and prototypes [4].  
- Reliability and latency for C2: short‑packet and URLLC‑style design (blocklength, power allocation, beamforming) can be optimized to maximize reliable control range and identify favorable altitude/resource tradeoffs for control links [7].  
- Sparse/non‑urban coverage: cellular coverage outside urban areas can be unreliable for BVLOS; field studies compare LTE vs 5G performance and recommend path/trajectory control and cellular‑aware planning to improve link availability [1] [2].  
- Local redundancy and range extension: relay UAVs and self‑organizing UAV meshes provide mission‑level redundancy and gigabit backhaul where ground infrastructure is insufficient; SkyHaul‑style mmWave mesh and relay UAV kits have been prototyped to sustain high‑bandwidth BVLOS services [3] [6].  
- Fast local coordination and DAA assistance: D2D/sidelink communications (ad hoc or 3GPP‑style sidelink scheduling) provide low-latency neighbor awareness for collision avoidance and Complementary Detect‑and‑Avoid (DAA) links [5].  
- Practical avionics/stack optimizations: MAVLink compression and pilot‑handover components have been field‑tested to reduce required C2 bandwidth and allow approved BVLOS operations under SORA‑like frameworks [10].

Example solution-to-challenge mapping (bulleted):
- **Coverage** uplift: **BS uptilt** and corridor‑specific antenna patterns to increase probability of coverage [8].  
- **Interference** mitigation: **mmWave beamforming** and **directional antennas** on UAVs and ground nodes [4] [11].  
- **Range/availability**: **relay UAVs** and **mmWave mesh** as airborne backhaul [3] [6].  
- **C2 reliability**: **short‑packet optimization** and altitude-aware resource allocation (BLER analysis) [7].  
- **Operational redundancy**: **D2D/sidelink** plus multi‑link designs to complement cellular C2 [5].

----

## LAWN classification

This section states whether ≤150 m BVLOS fits the LAWN term and reports what the supplied literature says about altitude labels. The corpus does not provide a formal, citable definition or explicit altitude bands for the term LAWN, so a definitive classification cannot be supported from these papers.

- The supplied papers use terms such as "low‑altitude", "drone corridors" and report experimental altitudes (e.g., LTE flight datasets at 30–110 m and cellular coverage assessments with reliable 4G coverage noted toward ~85 m), but none of the reviewed articles defines a standard LAWN altitude envelope or publishes an authoritative LAWN specification [2] [12].  
- Therefore, based on the provided literature, there is insufficient evidence to assert that 150 m specifically falls inside a defined LAWN category or to give an official LAWN altitude range; the studies instead report tested altitude ranges and emphasize “low‑altitude” without a universal numeric taxonomy [2] [12].  
- For practical planning, note that several experimental datasets and planning studies focus on heights well below or up to ~100–110 m, and some path‑planning/coverage analyses cite reliable 4G aerial coverage only to lower heights (e.g., ~85 m in one study) — implying that 150 m is above many tested conditions in those specific experiments [2] [12].

If you need a regulatory or standards LAWN definition, further authoritative references (standards bodies or regulatory documents) would be required; the supplied academic papers do not contain that definition.

----

## Protocols and technologies

This section compares the principal protocols and radio technologies actively researched for low‑altitude BVLOS operations and gives concrete paper examples. The table lists strengths and representative research demonstrations.

| Technology | Typical use case and strengths | Representative research examples |
|---|---:|---|
| LTE / 4G cellular | Ubiquitous baseline C2/payload links; useful in suburban tests and datasets | Field I/Q datasets and aerial drive tests at 30–110 m used to model propagation and plan BVLOS links [2]. |
| 5G (low/mid/mmWave) | Higher throughput, slicing, flexible numerology, potential URLLC; field KPI studies vs LTE | Experimental 5G vs LTE performance studies in non‑urban/suburban areas and recommendations for trajectory control [1]. |
| mmWave mesh / airborne backhaul | Gigabit backhaul between UAVs for bandwidth‑intense payloads and offloading | SkyHaul autonomous mmWave mesh and prototype UAV backhaul implementations [3]. |
| UAV-to-UAV D2D and 3GPP sidelink | Low‑latency neighbor awareness, local coordination, collision avoidance | DroneCAST D2D prototypes and 3GPP sidelink‑style scheduling for drone corridors [5] [4]. |
| Relay UAVs / multi‑hop airborne relays | Extend range where ground infrastructure is sparse, portable field kits | RUCKUS relay‑UAV kit demonstrations and relay‑based BVLOS field tests [6]. |
| Short‑packet URLLC / beamformed C2 | Reliability/BLER optimization, altitude-aware resource allocation for C2 | Closed‑form BLER analysis and optimization for maximizing reliable control range [7]. |
| Full‑duplex + directional antennas | Spectrum efficiency and co‑channel reuse for multi‑UAV systems | Full‑duplex aerial system designs leveraging directional antennas in simulations/prototypes [11]. |

Key protocol/standard notes from the corpus:
- Researchers test commercial cellular stacks (LTE/5G) for aerial UEs and propose cellular‑aware path planning and BS antenna changes to suit aerial users [1] [2] [8].  
- 3GPP sidelink concepts and semi‑persistent scheduling are applied to UAV corridors and inter‑UAV communications in simulation studies to reduce coordination latency and interference [4].  
- Mesh and relay architectures (mmWave backhaul) appear in prototypes to support high‑bandwidth BVLOS applications that exceed the capacity of single links [3].

Satellite links (SATCOM) and wide‑area NTN concepts are mentioned in some operational discussions of situational awareness, but the supplied papers do not include detailed experimental SATCOM performance results for the ≤150 m BVLOS case; therefore specific SATCOM performance claims for this altitude are not supported by the provided corpus.

----

## Regulatory and technical requirements

This section summarizes the regulatory and operational demands that appear in the literature for BVLOS operations, and links those to technical mitigations reported in empirical or simulation studies. The main required elements recurring in the papers are reliable C2, DAA, redundancy and proven link reliability.

- Command and control reliability and pilot handover: BVLOS operations require proven, redundant C2 links and the ability to hand over control between pilots/operators; MAVLink optimizations and pilot‑handover components were implemented and used successfully in SORA‑approved BVLOS trials to reduce bandwidth and support multi‑pilot control [10].  
- Detect‑and‑Avoid and safety equipment: regulatory expectations for BVLOS include reliable DAA and risk mitigation; one prototype study combined cellular C2 with DAA and a parachute fail‑safe for safer BVLOS operation, showing how avionics and communications must be jointly validated [13].  
- Link reliability metrics and design targets: studies derive BLER and URLLC‑style design metrics and use those to choose optimal altitudes, blocklengths and transmit power to maximize reliable C2 range—these analyses provide quantitative tools for meeting technical reliability requirements [7].  
- Infrastructure and network planning: regulators typically expect evidence of link availability along the planned route; cellular‑aware path‑planning and extensive aerial drive tests are used to quantify reliable coverage and produce mission plans that meet link‑reliability constraints [12].  
- Spectrum, interference and antenna configuration: for operations inside drone corridors, base station antenna uptilt and dedicated corridor antennas are proposed as technical measures to meet coverage/reliability expectations and to limit interference impacts on terrestrial users [8].  
- Multi‑link and redundancy best practice: the literature repeatedly recommends multi‑link architectures (cellular + D2D + relay/mesh) so that loss of one link does not compromise safety‑critical control or detect‑and‑avoid data [3] [5] [6].
