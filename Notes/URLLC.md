### 3GPP

https://www.3gpp.org/technologies/urlcc-2022 
Putting higher reliability and lower latency together was one of the key expectations of 5G, so it is quite logical that Release 15 (defining the initial 5G Release) introduces "EPC support for E-UTRAN Ultra Reliable Low Latency Communication". As for the brand new 5G Radio part (New Radio, NR), low latency is taken as a key design criteria. Besides, the 4G access is also improved to this respect, with RAN's 4G-only Feature "[Highly Reliable Low Latency Communication for LTE](https://portal.3gpp.org/desktopmodules/WorkItem/WorkItemDetails.aspx?workitemId=750061)".

For the 5G core network, this union of "conflicting requirements" is achieved mostly thanks to the "Local hosting of services", referring to the "Edge Computing" capability.

**eside** Edge, the Core Network improves its QoS Class Identifier (QCIs) mechanism. This was introduced in 4G to handle the QoS on a per-bearer basis. In 5G, several new QCIs values are introduced for ultra reliable and low latency services, for which the Packet Error Loss Rate calculation includes the packets that are not delivered within the Packet Delay Budget. This is intended to cover services such as Discrete Automation, Intelligent Transport Systems and Electricity Distribution.