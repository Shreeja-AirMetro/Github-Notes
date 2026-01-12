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
2. https://www.3gpp.org/technologies/nr-uav
3. https://www.3gpp.org/technologies/urlcc-2022
4. 