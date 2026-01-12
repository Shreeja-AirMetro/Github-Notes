### 3GPP

https://www.3gpp.org/technologies/urlcc-2022 
Putting higher reliability and lower latency together was one of the key expectations of 5G, so it is quite logical that Release 15 (defining the initial 5G Release) introduces "EPC support for E-UTRAN Ultra Reliable Low Latency Communication". As for the brand new 5G Radio part (New Radio, NR), low latency is taken as a key design criteria. Besides, the 4G access is also improved to this respect, with RAN's 4G-only Feature "[Highly Reliable Low Latency Communication for LTE](https://portal.3gpp.org/desktopmodules/WorkItem/WorkItemDetails.aspx?workitemId=750061)".

For the 5G core network, this union of "conflicting requirements" is achieved mostly thanks to the "Local hosting of services", referring to the "Edge Computing" capability.

**eside** Edge, the Core Network improves its QoS Class Identifier (QCIs) mechanism. This was introduced in 4G to handle the QoS on a per-bearer basis. In 5G, several new QCIs values are introduced for ultra reliable and low latency services, for which the Packet Error Loss Rate calculation includes the packets that are not delivered within the Packet Delay Budget. This is intended to cover services such as Discrete Automation, Intelligent Transport Systems and Electricity Distribution.

URLLC is a major axis of enhancement of the 5G System.

In Rel-16, the main improvement for URLLC is the introduction of Redundant transmission for high-reliability communication. : user packets are duplicated and simultaneously transferred to the receiver via two disjoint user plane paths. User packets are duplicated and simultaneously transferred to the receiver via two disjoint user plane paths. The redundant packets are then eliminated at the receiver side. With this, service failure can be avoided even in case the packet transmission via one path occasionally fails or exceeds the delay requirement. Different ways of duplicating the paths are specified (Dual Connectivity, using two N3 and N9 tunnels, using two N3 tunnels).

Other non-radio specific aspects are QoS Monitoring, Dynamic division of Packet Delay Budget, Packet Delay Budget (PDB) and enhancements of session continuity.

As for the Radio aspects, the Physical Layer is improved for the support of URLLC in several ways: new DCI formats, Enhanced PDCCH monitoring capability, Sub-slot based HARQ-ACK feedback, Two HARQ-ACK codebooks constructed simultaneously, PUSCH enhancements, Enhanced inter UE Tx prioritization/multiplexing and Multiple active configured grant configurations for a BWP.

scope of interest 
1. https://www.3gpp.org/technologies/sa6-cc-apps
	- 3GPP TSG SA WG6 [(SA6)](https://www.3gpp.org/3gpp-groups/service-system-aspects-sa/sa-wg6) has, since its inception, championed application layer architecture specifications for mission critical systems (public safety, railways) as well as application enabler layer specifications for supporting the integration of 3GPP systems with other verticals such as - V2X, UAS, IoT. Furthermore, SA6 has developed and specified service frameworks, such as the Common API Framework (CAPIF), the Service Enabler Architecture Layer (SEAL) and Edge Application enablement (EDGEAPP).
	- Rel 17 - II UAS APP
	- REl 18 UAS APP 2.0
	- |[TS23.255](https://www.3gpp.org/ftp/Specs/archive/23_series/23.255/)
	Fuctional architecture and information flows|Application layer support for Uncrewed Aerial System (UAS); Functional architecture and information flows|
	
2. https://www.3gpp.org/technologies/nr-uav
	- The Rel-18 WG RAN2-led work is focused on radio measurements, mobility and interference mitigation enhancements that should allow smooth integration of UAVs within the existing NR networks.
	- As the UAV UE is likely to fly above the rooftops, where Line of Sight (LOS) conditions dominate, it may detect multiple strong neighbour cells and face an increase in interference conditions. Because of that, the NR measurement framework will support height-dependent measurement report triggering (i.e. Events H1 and H2, to be specified in TS 38.331) which will help the network in identifying at what altitude the UAV currently operates. When the network has such knowledge, it may adapt the UAV UE configurations, ensuring the interference level is kept at minimum.
	- 
3. https://www.3gpp.org/technologies/urlcc-2022
https://www.3gpp.org/technologies/tsg-ct-work-on-uas-connectivity-identification-and-tracking

- **UASAPP** - Application layer support for Uncrewed Aerial System: specifies application layer capabilities towards UAS applications on the UAV/UAV Controller and the USS/UTM systems to leverage 3GPP transport capabilities, including support for communication between UAVs within a geographical area, QoS provisioning for C2 communication, monitoring of location deviation, and reporting of UAV events (Refer to [3GPP TS 23.255](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3843)

