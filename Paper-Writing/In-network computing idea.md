- Future core network - communication standard magazine
- in-network computing - academia 
- Nokia guy - semantic - goal-oriented communication 
- object detection inside of network 
- core - management of 
- switch 
- which node is trust worthy - define by core 
- quantum core 
- PQC with Albesmart - Post Quantum cryptography 
- Quantum function secret sharing  - QFSS
- OIA - secure the backhaul - quantum 
- Measurement based quantum computing
- Blind computing
- Q states send by client to Q computer (Server) - blind on algorithm
- blind on outputs 
-  Q Channel - expensive 
- Fibers - compatibility issues 
- QFSS 
- Compatible with 5G core
- Application layer to physical - control plan to core network 
- Layerization - OSI layer with Quantum states
- Repetition rate different from qbit rate 
- Having physical layer completely is important 
- Quantum TCP 
- QFSS - many clients - congestion control at transport layer
- Semantic encoding and decoding 
- basic scheme on your system - OSI layer 
- Trustworthiness - Mapping physical layer - image capture
- its magazine
- standard paper 
- high-level architecture
- new technology - what changes on core
- enhancement on the 5G core 
- 3GPP specification 
- use-case : sensing, synchronization, - ballpark QOS
- crypto- correctness and security 
- connect the quantum computing 
- Quantum server to classical server 
- separated in space and time 
- OSI quantum core to user is difficult - cost and infrastructure 
- then what it can enhance in classical core?

Standardized architecture -> QKD - backhaul 
Trustworthiness between gNB and user - issue ? 
Quantum server  at gNB - blindness protected - Edge 
What can secure between gNB 
NISF - Quantum dots 
measurement - your data is specific to use-case 
Quantum state - quantum teleportation protocol 
computers - coherence time (time to prepare quantum state)
quantum characteristics 
latency - state fidelity
single flow of information 
general purpose core 

- 5G core - general purpose  computing - native core 
Jiajing overleaf 

## Function of Mobile Core Network

<span style="color:rgb(0, 176, 80)">A **mobile core network** serves as the central nervous system of cellular telecommunications networks, acting as the critical bridge between mobile devices and external networks such as the internet, public switched telephone networks (PSTN), and other mobile networks</span>[1](https://www.tatacommunications.com/knowledge-base/network-core-network-explained/)[2](https://commsbrief.com/what-is-a-mobile-core-network/). The core network functions as the **brain of the mobile network**, responsible for managing and controlling all connected devices and determining what services they are authorized to use[3](https://www.iplook.com/info/what-is-mobile-core-network-i00174i1.html).

## Primary Functions

The mobile core network performs several essential functions that enable seamless mobile communications:

**Authentication and Authorization**: The core network verifies subscriber identity and ensures users have proper authorization to access network services[1](https://www.tatacommunications.com/knowledge-base/network-core-network-explained/)[2](https://commsbrief.com/what-is-a-mobile-core-network/). This includes checking subscriber profiles, validating SIM cards, and managing service entitlements.

**Mobility Management**: The system continuously tracks the location of mobile devices as they move between different cells and network areas, enabling seamless handovers and maintaining connectivity during movement[1](https://www.tatacommunications.com/knowledge-base/network-core-network-explained/)[2](https://commsbrief.com/what-is-a-mobile-core-network/)[4](https://www.linkedin.com/pulse/understanding-core-elements-mobile-network-ran-christian-omeni-cdgcf).

**Call and Data Routing**: The core network handles routing of voice calls, text messages, and data traffic between mobile devices and external networks, ensuring efficient delivery of communications[2](https://commsbrief.com/what-is-a-mobile-core-network/)[4](https://www.linkedin.com/pulse/understanding-core-elements-mobile-network-ran-christian-omeni-cdgcf).

**Session Management**: It manages data sessions, including establishing, maintaining, and terminating connections between mobile devices and external networks[2](https://commsbrief.com/what-is-a-mobile-core-network/)[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC).

**Billing and Charging**: The core network collects usage data and implements charging policies for different services and applications[1](https://www.tatacommunications.com/knowledge-base/network-core-network-explained/)[6](https://www.iotforall.com/the-network-core-of-connectivity).

**Quality of Service (QoS)**: It enforces service quality parameters to ensure proper performance for different types of traffic, from voice calls to high-speed data applications[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC)[7](https://yatebts.com/solutions_and_technology/lte-epc/).

## Core Network Components by Generation

The mobile core network has evolved significantly across different generations of mobile technology, with each generation introducing new architectures and components:

## 2G Core Network Components

**Mobile Switching Center (MSC)**: The central component that performs switching functions for voice calls, SMS management, and serves as the gateway to other networks[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[9](https://en.wikipedia.org/wiki/GSM_core_network).

**Home Location Register (HLR)**: A database that stores and manages subscriber information, including phone numbers, service profiles, and authentication data[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[10](https://tektelic.com/what-it-is/home-location-register/)[11](https://sinch.com/glossary/home-location-register/).

**Visitor Location Register (VLR)**: Temporarily stores information about subscribers currently within the MSC's jurisdiction[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[9](https://en.wikipedia.org/wiki/GSM_core_network).

**Authentication Center (AUC)**: Provides authentication and encryption parameters to protect against fraud and ensure communication privacy[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[9](https://en.wikipedia.org/wiki/GSM_core_network).

## 3G Core Network Components

**MSC Server**: An evolved version of the MSC that handles call routing but is separated from media gateways[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[12](https://en.wikipedia.org/wiki/Mobile_switching_centre_server).

**Serving GPRS Support Node (SGSN)**: Manages data packet delivery between mobile devices and external networks, handling mobility management for devices in its service area[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2).

**Gateway GPRS Support Node (GGSN)**: Acts as a gateway between the cellular network and external packet-switched networks[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2).

**Home Subscriber Server (HSS)**: The evolved version of HLR that holds all user-related and subscription-related data[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[11](https://sinch.com/glossary/home-location-register/).

## 4G Core Network Components (EPC)

**Evolved Packet Core (EPC)**: The unified core network for 4G that replaces separate circuit-switched and packet-switched architectures[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC)[13](https://images.tmcnet.com/online-communities/ngc/pdfs/end-to-end-lte/whitepapers/EPC_Solution_wp_0309.pdf).

**Mobility Management Entity (MME)**: Manages signaling and security for handovers and mobility between LTE networks[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC).

**Serving Gateway (SGW)**: Routes and forwards user data packets while acting as the mobility anchor during handovers[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[14](https://www.cisco.com/c/en/us/products/wireless/sgw-serving-gateway/index.html)[15](https://www.cisco.com/c/en/us/td/docs/wireless/asr_5000/21-27/sgw-admin/21-27-sgw-admin/m_sgwoview.pdf).

**Packet Data Network Gateway (PGW)**: Connects users to external packet data networks, providing policy enforcement, packet filtering, and charging support[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC)[16](https://www.slideshare.net/slideshow/lte-sgw-amp-pgw/70443133).

**Home Subscriber Server (HSS)**: Central database containing user-related and subscription-related information[8](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC).

**Policy and Charging Rules Function (PCRF)**: Manages policy control decisions and flow-based charging functionalities[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC)[17](https://npstc.org/documents/ALU_WP_Intro_to_EPC.pdf).

## 5G Core Network Components

**Access and Mobility Management Function (AMF)**: Handles all connections, user equipment sessions, and mobility management tasks - equivalent to MME in 4G[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html).

**Session Management Function (SMF)**: Manages data sessions and applies network policies[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html).

**User Plane Function (UPF)**: Handles user data processing and serves as the connection point between the radio access network and data networks - equivalent to combined SGW and PGW functions from 4G[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html).

**Network Repository Function (NRF)**: Maintains a registry of all network functions and their supported services[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html).

**Authentication Server Function (AUSF)**: Responsible for SIM authentication and secure network access[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html).

**Unified Data Management (UDM)**: Manages subscriber data - equivalent to HSS in 4G[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html).

**Policy Control Function (PCF)**: Applies policies and shapes network behavior - equivalent to PCRF in 4G[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html).

**Network Slice Selection Function (NSSF)**: Selects appropriate network slices based on service requirements[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html).

## Architecture Evolution

The mobile core network has undergone significant architectural changes:

**Circuit-Switched to Packet-Switched**: Early networks used separate circuit-switched cores for voice and packet-switched cores for data. Modern networks have unified these into all-IP architectures[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC)[13](https://images.tmcnet.com/online-communities/ngc/pdfs/end-to-end-lte/whitepapers/EPC_Solution_wp_0309.pdf)[17](https://npstc.org/documents/ALU_WP_Intro_to_EPC.pdf).

**Flat Architecture**: Modern core networks employ flatter architectures that reduce the number of network elements and simplify data paths, improving performance and reducing latency[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC)[13](https://images.tmcnet.com/online-communities/ngc/pdfs/end-to-end-lte/whitepapers/EPC_Solution_wp_0309.pdf).

**Service-Based Architecture**: 5G introduces a service-based architecture where network functions are modularized and can communicate with each other through standardized interfaces[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[20](https://embeddedcomputing.com/application/networking-5g/5g-primer-part-3-5g-core-network).

**Cloud-Native Design**: Modern core networks are designed as cloud-native, software-based systems that can be deployed flexibly across different cloud infrastructures[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[21](https://www.ericsson.com/en/core-network/5g-core).

## Key Interfaces and Protocols

The mobile core network uses various standardized interfaces and protocols:

**Control Plane and User Plane Separation**: Modern networks separate control plane functions (signaling) from user plane functions (data forwarding) to enable independent scaling and optimization[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[5](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC).

**Standard Interfaces**: Networks use standardized interfaces like S1 (between base stations and core), S11 (between MME and SGW), and N4 (between SMF and UPF in 5G)[22](https://www.eit.lth.se/fileadmin/eit/courses/eitp30/Lp1-2023/L-MobileCore-HO.pdf)[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/).

**Tunneling Protocols**: Technologies like GTP (GPRS Tunneling Protocol) are used to create tunnels for data transmission across the core network[22](https://www.eit.lth.se/fileadmin/eit/courses/eitp30/Lp1-2023/L-MobileCore-HO.pdf)[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/).

The mobile core network represents a sophisticated ecosystem that has evolved from simple circuit-switched systems to complex, software-defined, cloud-native architectures capable of supporting diverse services from basic voice calls to advanced IoT applications and ultra-low latency communications.

1. [https://www.tatacommunications.com/knowledge-base/network-core-network-explained/](https://www.tatacommunications.com/knowledge-base/network-core-network-explained/)
2. [https://commsbrief.com/what-is-a-mobile-core-network/](https://commsbrief.com/what-is-a-mobile-core-network/)
3. [https://www.iplook.com/info/what-is-mobile-core-network-i00174i1.html](https://www.iplook.com/info/what-is-mobile-core-network-i00174i1.html)
4. [https://www.linkedin.com/pulse/understanding-core-elements-mobile-network-ran-christian-omeni-cdgcf](https://www.linkedin.com/pulse/understanding-core-elements-mobile-network-ran-christian-omeni-cdgcf)
5. [https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC](https://www.techtarget.com/searchnetworking/definition/Evolved-Packet-Core-EPC)
6. [https://www.iotforall.com/the-network-core-of-connectivity](https://www.iotforall.com/the-network-core-of-connectivity)
7. [https://yatebts.com/solutions_and_technology/lte-epc/](https://yatebts.com/solutions_and_technology/lte-epc/)
8. [https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2](https://www.linkedin.com/posts/mycommunicationacademy_corenetwork-2g-3g-activity-7211035380127571968-oRC2)
9. [https://en.wikipedia.org/wiki/GSM_core_network](https://en.wikipedia.org/wiki/GSM_core_network)
10. [https://tektelic.com/what-it-is/home-location-register/](https://tektelic.com/what-it-is/home-location-register/)
11. [https://sinch.com/glossary/home-location-register/](https://sinch.com/glossary/home-location-register/)
12. [https://en.wikipedia.org/wiki/Mobile_switching_centre_server](https://en.wikipedia.org/wiki/Mobile_switching_centre_server)
13. [https://images.tmcnet.com/online-communities/ngc/pdfs/end-to-end-lte/whitepapers/EPC_Solution_wp_0309.pdf](https://images.tmcnet.com/online-communities/ngc/pdfs/end-to-end-lte/whitepapers/EPC_Solution_wp_0309.pdf)
14. [https://www.cisco.com/c/en/us/products/wireless/sgw-serving-gateway/index.html](https://www.cisco.com/c/en/us/products/wireless/sgw-serving-gateway/index.html)
15. [https://www.cisco.com/c/en/us/td/docs/wireless/asr_5000/21-27/sgw-admin/21-27-sgw-admin/m_sgwoview.pdf](https://www.cisco.com/c/en/us/td/docs/wireless/asr_5000/21-27/sgw-admin/21-27-sgw-admin/m_sgwoview.pdf)
16. [https://www.slideshare.net/slideshow/lte-sgw-amp-pgw/70443133](https://www.slideshare.net/slideshow/lte-sgw-amp-pgw/70443133)
17. [https://npstc.org/documents/ALU_WP_Intro_to_EPC.pdf](https://npstc.org/documents/ALU_WP_Intro_to_EPC.pdf)
18. [https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)
19. [https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)
20. [https://embeddedcomputing.com/application/networking-5g/5g-primer-part-3-5g-core-network](https://embeddedcomputing.com/application/networking-5g/5g-primer-part-3-5g-core-network)
21. [https://www.ericsson.com/en/core-network/5g-core](https://www.ericsson.com/en/core-network/5g-core)
22. [https://www.eit.lth.se/fileadmin/eit/courses/eitp30/Lp1-2023/L-MobileCore-HO.pdf](https://www.eit.lth.se/fileadmin/eit/courses/eitp30/Lp1-2023/L-MobileCore-HO.pdf)
23. [https://jscingenium.com/en/glossary/what-is-it-and-how-does-core-work/](https://jscingenium.com/en/glossary/what-is-it-and-how-does-core-work/)
24. [https://www.ericsson.com/en/core-network](https://www.ericsson.com/en/core-network)
25. [https://wraycastle.com/blogs/knowledge-base/what-are-core-network-functions](https://wraycastle.com/blogs/knowledge-base/what-are-core-network-functions)
26. [https://www.taoglas.com/blogs/cellular-network-infrastructure-key-components-and-their-functions/](https://www.taoglas.com/blogs/cellular-network-infrastructure-key-components-and-their-functions/)
27. [https://telecomtrustconsulting.com/core-network/](https://telecomtrustconsulting.com/core-network/)
28. [https://www.sciencedirect.com/topics/computer-science/mobile-core-network](https://www.sciencedirect.com/topics/computer-science/mobile-core-network)
29. [https://drivenets.com/resources/education-center/what-is-a-core-network/](https://drivenets.com/resources/education-center/what-is-a-core-network/)
30. [https://cdn.fs.teachablecdn.com/KeB7A6GQSj65tvNDBdZD](https://cdn.fs.teachablecdn.com/KeB7A6GQSj65tvNDBdZD)
31. [https://mvno-index.com/what-is-a-core-mobile-network/](https://mvno-index.com/what-is-a-core-mobile-network/)
32. [https://learn.microsoft.com/en-us/azure/private-5g-core/key-components-of-a-private-mobile-network](https://learn.microsoft.com/en-us/azure/private-5g-core/key-components-of-a-private-mobile-network)
33. [https://www.p1sec.com/blog/key-mobile-network-equipment-and-functions](https://www.p1sec.com/blog/key-mobile-network-equipment-and-functions)
34. [https://www.celona.io/5g-lan/5g-core](https://www.celona.io/5g-lan/5g-core)
35. [https://www.rcrwireless.com/20140509/diameter-signaling-controller-dsc/lte-architecture-overview](https://www.rcrwireless.com/20140509/diameter-signaling-controller-dsc/lte-architecture-overview)
36. [https://www.tutorialspoint.com/lte/pdf/lte_network_architecture.pdf](https://www.tutorialspoint.com/lte/pdf/lte_network_architecture.pdf)
37. [https://niralnetworks.com/5g-core-network-architecture/](https://niralnetworks.com/5g-core-network-architecture/)
38. [https://rintintin.colorado.edu/~gifford/5830-AWL/LTE_Alcatel_White_Paper.pdf](https://rintintin.colorado.edu/~gifford/5830-AWL/LTE_Alcatel_White_Paper.pdf)
39. [https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/Studies/5G/5G_Core_Network.pdf?__blob=publicationFile&v=4](https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/Studies/5G/5G_Core_Network.pdf?__blob=publicationFile&v=4)
40. [https://www.interviewbit.com/blog/lte-architecture/](https://www.interviewbit.com/blog/lte-architecture/)
41. [https://www.devx.com/terms/evolved-packet-core/](https://www.devx.com/terms/evolved-packet-core/)
42. [https://www.slideshare.net/slideshow/lte-core-network/31073724](https://www.slideshare.net/slideshow/lte-core-network/31073724)
43. [https://de.wikipedia.org/wiki/Evolved_Packet_System](https://de.wikipedia.org/wiki/Evolved_Packet_System)
44. [https://www.tutorialspoint.com/lte/lte_network_architecture.htm](https://www.tutorialspoint.com/lte/lte_network_architecture.htm)
45. [https://www.grandmetric.com/5g-core-network-a-short-overview/](https://www.grandmetric.com/5g-core-network-a-short-overview/)
46. [https://ltemobile.de/lte-technik/epc-das-lte-kernnetz/](https://ltemobile.de/lte-technik/epc-das-lte-kernnetz/)
47. [https://de.wikipedia.org/wiki/Mobile-services_Switching_Centre](https://de.wikipedia.org/wiki/Mobile-services_Switching_Centre)
48. [https://www.it-administrator.de/lexikon/mobilfunkvermittlungsstelle.html](https://www.it-administrator.de/lexikon/mobilfunkvermittlungsstelle.html)
49. [https://lightyear.ai/tips/what-is-a-home-location-register](https://lightyear.ai/tips/what-is-a-home-location-register)
50. [https://www.1nce.com/en-us/resources/iot-knowledge-base/iot-connectivity/cellular-networks/how-is-mobile-switching-center](https://www.1nce.com/en-us/resources/iot-knowledge-base/iot-connectivity/cellular-networks/how-is-mobile-switching-center)
51. [https://www.capterra.com/glossary/hlr-home-location-register/](https://www.capterra.com/glossary/hlr-home-location-register/)
52. [https://www.itwissen.info/serving-gateway-LTE-SGW.html](https://www.itwissen.info/serving-gateway-LTE-SGW.html)
53. [https://tektelic.com/what-it-is/mobile-switching-center/](https://tektelic.com/what-it-is/mobile-switching-center/)
54. [https://www.cequens.com/knowledge-hub/glossary/hlr-home-location-register](https://www.cequens.com/knowledge-hub/glossary/hlr-home-location-register)
55. [https://terms.tta.or.kr/dictionary/dictionaryView.do?word_seq=170482-8](https://terms.tta.or.kr/dictionary/dictionaryView.do?word_seq=170482-8)
56. [https://www.mobius-software.com/documentation/Mobius+GMLC+Gateway/MSC+%2528Mobile+Switching+Center%2529](https://www.mobius-software.com/documentation/Mobius+GMLC+Gateway/MSC+%2528Mobile+Switching+Center%2529)
57. [https://seon.io/resources/dictionary/hlr/](https://seon.io/resources/dictionary/hlr/)
58. [https://patents.google.com/patent/CN103428792A/en](https://patents.google.com/patent/CN103428792A/en)
59. [https://www.simbase.com/iot-glossary-dictionary/home-location-register-hlr](https://www.simbase.com/iot-glossary-dictionary/home-location-register-hlr)

# 5G Core Network Architecture and Industry Leadership

## 5G Core Network Components and Architecture

The **5G Core Network (5GC)** represents a fundamental shift from traditional telecommunications architecture to a cloud-native, service-based approach. Unlike previous generations that relied on dedicated hardware, the 5G core is entirely software-based and designed to run on virtualized infrastructure[1](https://www.geeksforgeeks.org/computer-networks/5g-network-architecture/)[2](https://www.digi.com/resources/definitions/5g-standalone).

## Key Network Functions

The 5G core operates through several critical **Network Functions (NFs)** that work together to provide comprehensive network services:

**Core Control Plane Functions:**

- **Access and Mobility Management Function (AMF)**: Manages user authentication, mobility, and connection establishment - essentially the "doorman" of the 5G network[3](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[4](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[5](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
    
- **Session Management Function (SMF)**: Handles session establishment, IP address allocation, and coordinates with user plane functions[3](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[4](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[5](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
    
- **Authentication Server Function (AUSF)**: Provides security and authentication services for user equipment[3](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[4](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[5](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
    
- **Unified Data Management (UDM)**: Stores and manages subscriber data, profiles, and credentials[3](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[4](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[5](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
    
- **Policy Control Function (PCF)**: Manages network policies, quality of service, and traffic rules[3](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[4](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[5](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
    

**Supporting Functions:**

- **Network Repository Function (NRF)**: Acts as a service registry, helping network functions discover and connect with each other[3](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[4](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[5](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
    
- **Network Slice Selection Function (NSSF)**: Selects appropriate network slices based on service requirements[3](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[4](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[5](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
    
- **Network Exposure Function (NEF)**: Safely exposes network capabilities to external applications[3](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[4](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[5](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
    

**User Plane Function:**

- **User Plane Function (UPF)**: Handles actual data traffic routing, packet inspection, and quality of service enforcement - the "traffic controller" of the network[3](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[4](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[5](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
    

## Architecture Principles

The 5G core is built on three foundational technologies:

1. **Service-Based Architecture (SBA)**: Network functions communicate through standardized APIs using HTTP/2 and REST protocols, enabling flexible and dynamic interactions[6](https://www.docomo.ne.jp/english/corporate/technology/rd/technical_journal/bn/vol24_4/001.html)[7](https://embeddedcomputing.com/application/networking-5g/5g-primer-part-3-5g-core-network)[8](https://flolive.net/blog/glossary/5g-core-network-architecture-9-key-network-functions/)
    
2. **Control and User Plane Separation (CUPS)**: This allows independent scaling of control functions and data forwarding components, enabling user plane functions to be deployed closer to the edge[9](https://www.a10networks.com/blog/5g-is-about-to-change-the-world-heres-how-it-works/)[7](https://embeddedcomputing.com/application/networking-5g/5g-primer-part-3-5g-core-network)[10](https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-22610FA3-72E1-44DE-8D0C-649916FAACF3.html)
    
3. **Network Function Virtualization (NFV)**: Traditional hardware-based network functions are replaced with software running on commercial off-the-shelf hardware[9](https://www.a10networks.com/blog/5g-is-about-to-change-the-world-heres-how-it-works/)[7](https://embeddedcomputing.com/application/networking-5g/5g-primer-part-3-5g-core-network)[11](https://sdnfv.zte.com.cn/en/products/VNF/5G-core-network)
    

## Physical Infrastructure and Deployment

## Cloud-Native Architecture

The 5G core's physical structure is fundamentally different from previous generations. Instead of dedicated hardware appliances, the 5G core runs on **cloud-native infrastructure** using containerization and microservices architecture[6](https://www.docomo.ne.jp/english/corporate/technology/rd/technical_journal/bn/vol24_4/001.html)[2](https://www.digi.com/resources/definitions/5g-standalone)[11](https://sdnfv.zte.com.cn/en/products/VNF/5G-core-network).

## Deployment Models

**Hierarchical Data Center Architecture:**

- **National Data Centers**: Host subscriber databases, resource orchestration, and service assurance functions[10](https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-22610FA3-72E1-44DE-8D0C-649916FAACF3.html)[12](https://techdocs.broadcom.com/us/en/vmware-sde/telco-cloud/vmware-telco-cloud-platform/3-1/telco-cloud-reference-architecture-guide/architectural-overview/telco-5g-architecture.html)
    
- **Regional Data Centers**: Contain 5G core user plane functions, voice services, and infrastructure services like DNS and NTP[10](https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-22610FA3-72E1-44DE-8D0C-649916FAACF3.html)[12](https://techdocs.broadcom.com/us/en/vmware-sde/telco-cloud/vmware-telco-cloud-platform/3-1/telco-cloud-reference-architecture-guide/architectural-overview/telco-5g-architecture.html)
    
- **Edge Data Centers**: Deploy user plane functions closer to users for ultra-low latency applications[13](http://www.techtimes.com/articles/309128/20250120/designing-deploying-5g-core-edge-end-end-networking.htm)[14](https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-CEA58D34-49D5-427D-B41B-4FAFFFCB454A.html)[10](https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-22610FA3-72E1-44DE-8D0C-649916FAACF3.html)
    

**Infrastructure Requirements:**

- **Compute Infrastructure**: High-performance servers with significant CPU, memory, and storage resources[15](https://www.semiconductors.org/wp-content/uploads/2020/07/SIA-5G-Report_2.pdf)[16](https://carrier.huawei.com/~/media/CNBGV2/download/products/network-energy/5G-oriented-Data-Center-Facility-en.pdf)
    
- **Network Infrastructure**: High-bandwidth, low-latency connectivity between data centers[14](https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-CEA58D34-49D5-427D-B41B-4FAFFFCB454A.html)[10](https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-22610FA3-72E1-44DE-8D0C-649916FAACF3.html)
    
- **Container Orchestration**: Kubernetes-based platforms for managing containerized network functions[11](https://sdnfv.zte.com.cn/en/products/VNF/5G-core-network)[17](https://www.open5gcore.org/)
    

## Physical Deployment Characteristics

The 5G core requires **significantly more computing resources** than previous generations due to its software-based nature. For example, the power density of 5G equipment is approximately **five times higher** than 4G infrastructure[16](https://carrier.huawei.com/~/media/CNBGV2/download/products/network-energy/5G-oriented-Data-Center-Facility-en.pdf). This has led to the development of specialized **5G-oriented data center facilities** designed to handle the increased computational demands[16](https://carrier.huawei.com/~/media/CNBGV2/download/products/network-energy/5G-oriented-Data-Center-Facility-en.pdf).

## Leading Companies in 5G Core Development and Maintenance

## Market Leaders

Based on recent market analysis and competitive assessments, the **top vendors** in the 5G core network market are:

**Tier 1 Leaders:**

1. **Huawei Technologies** - Despite geopolitical challenges, remains the global leader with strong presence in China and emerging markets, achieving 2.3% year-over-year growth with $50 billion in network sales[18](https://www.huaweicentral.com/huawei-edges-out-ericsson-and-nokia-in-5g-network-market-despite-u-s-sanctions/)[19](https://www.abiresearch.com/press/ericsson-and-huawei-take-the-lead-in-abi-researchs-5g-core-edge-platforms-competitive-ranking-mavenir-affirmed-networks-named-top-challengers/)[20](https://www.abiresearch.com/press/huawei-and-ericsson-take-the-lead-in-abi-researchs-5g-end-to-end-core-network-automation-and-orchestration-vendor-competitive-ranking)
    
2. **Ericsson** - Leading in Western markets with strong commercial deployments, named a leader in Gartner's 2024 Magic Quadrant for 5G Core, powering 34 of 60 commercially live 5G SA networks[21](https://www.ericsson.com/en/news/2024/9/ericsson-named-a-leader-in-the-2024-gartner-magic-quadrant-for-csp-5g-core-network-infrastructure-solutions)[19](https://www.abiresearch.com/press/ericsson-and-huawei-take-the-lead-in-abi-researchs-5g-core-edge-platforms-competitive-ranking-mavenir-affirmed-networks-named-top-challengers/)[20](https://www.abiresearch.com/press/huawei-and-ericsson-take-the-lead-in-abi-researchs-5g-end-to-end-core-network-automation-and-orchestration-vendor-competitive-ranking)
    
3. **Nokia Corporation** - Strong portfolio presence in most Western 5G networks, though facing some revenue challenges with 8% year-over-year decline in network sales[18](https://www.huaweicentral.com/huawei-edges-out-ericsson-and-nokia-in-5g-network-market-despite-u-s-sanctions/)[19](https://www.abiresearch.com/press/ericsson-and-huawei-take-the-lead-in-abi-researchs-5g-core-edge-platforms-competitive-ranking-mavenir-affirmed-networks-named-top-challengers/)[20](https://www.abiresearch.com/press/huawei-and-ericsson-take-the-lead-in-abi-researchs-5g-end-to-end-core-network-automation-and-orchestration-vendor-competitive-ranking)
    

**Tier 2 Vendors:**  
4. **ZTE Corporation** - Strong in Chinese market with 7.8% Q1 2025 growth, focusing on AI-centric 5.5G features[22](https://mobile-magazine.com/top10/top-10-5g-edge-computing-platforms)[19](https://www.abiresearch.com/press/ericsson-and-huawei-take-the-lead-in-abi-researchs-5g-core-edge-platforms-competitive-ranking-mavenir-affirmed-networks-named-top-challengers/)[23](https://www.mordorintelligence.com/industry-reports/5g-core-network-market)  
5. **Samsung Electronics** - Positioned as an agile challenger with significant vRAN commitments and energy reduction initiatives[22](https://mobile-magazine.com/top10/top-10-5g-edge-computing-platforms)[19](https://www.abiresearch.com/press/ericsson-and-huawei-take-the-lead-in-abi-researchs-5g-core-edge-platforms-competitive-ranking-mavenir-affirmed-networks-named-top-challengers/)[23](https://www.mordorintelligence.com/industry-reports/5g-core-network-market)

## Market Dynamics and Trends

**Market Consolidation**: The top four vendors (Ericsson, Huawei, Nokia, and ZTE) account for close to **70% of worldwide revenue** in the 5G core market[23](https://www.mordorintelligence.com/industry-reports/5g-core-network-market)[24](https://telecomlead.com/telecom-equipment/mobile-core-network-vendors-and-investment-trends-in-q1-2025-121082).

**Emerging Competitors**: New entrants are challenging established players, including:

- **Cisco Systems** - Leveraging its networking expertise for 5G core solutions[25](https://www.lightreading.com/virtualization/how-a-new-crop-of-vendors-is-breaking-into-the-5g-core)[26](https://datacentremagazine.com/articles/top-10-5g-infrastructure-companies)
    
- **Hewlett Packard Enterprise (HPE)** - Offering cloud-native 5G core platforms[25](https://www.lightreading.com/virtualization/how-a-new-crop-of-vendors-is-breaking-into-the-5g-core)[26](https://datacentremagazine.com/articles/top-10-5g-infrastructure-companies)
    
- **Mavenir** - Focusing on cloud-native, software-based solutions[25](https://www.lightreading.com/virtualization/how-a-new-crop-of-vendors-is-breaking-into-the-5g-core)[19](https://www.abiresearch.com/press/ericsson-and-huawei-take-the-lead-in-abi-researchs-5g-core-edge-platforms-competitive-ranking-mavenir-affirmed-networks-named-top-challengers/)
    
- **Microsoft** (through Affirmed Networks acquisition) - Though later divested, showing cloud provider interest[25](https://www.lightreading.com/virtualization/how-a-new-crop-of-vendors-is-breaking-into-the-5g-core)[23](https://www.mordorintelligence.com/industry-reports/5g-core-network-market)
    

## Market Size and Growth

The global 5G core network market is experiencing **exponential growth**:

- **2024 Market Size**: USD 4.83 billion to USD 6.1 billion (various estimates)[27](https://market.us/report/5g-core-network-market/)[28](https://www.linkedin.com/pulse/5g-core-market-size-share-scope-trends-forecast-vista-nova-research-kyace/)
    
- **2030-2034 Projections**: USD 37.97 billion to USD 212.6 billion[27](https://market.us/report/5g-core-network-market/)[28](https://www.linkedin.com/pulse/5g-core-market-size-share-scope-trends-forecast-vista-nova-research-kyace/)
    
- **Growth Rate**: 41-46% CAGR (Compound Annual Growth Rate)[27](https://market.us/report/5g-core-network-market/)[28](https://www.linkedin.com/pulse/5g-core-market-size-share-scope-trends-forecast-vista-nova-research-kyace/)
    

## Regional Leadership

**Asia-Pacific** leads the 5G core market with a **40.3% share** and USD 1.9 billion in revenue in 2024[27](https://market.us/report/5g-core-network-market/). This is driven primarily by massive deployments in China and India, where operators have achieved over 90% population coverage[29](https://www.ericsson.com/en/reports-and-papers/mobility-report/dataforecasts/network-coverage).

The 5G core network represents a paradigm shift in telecommunications infrastructure, moving from hardware-centric to software-defined, cloud-native architectures. This transformation is being led by established telecommunications equipment vendors like Huawei, Ericsson, and Nokia, while new cloud-native focused companies are emerging as significant challengers in this rapidly growing market.

1. [https://www.geeksforgeeks.org/computer-networks/5g-network-architecture/](https://www.geeksforgeeks.org/computer-networks/5g-network-architecture/)
2. [https://www.digi.com/resources/definitions/5g-standalone](https://www.digi.com/resources/definitions/5g-standalone)
3. [https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)
4. [https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)
5. [https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation](https://www.scribd.com/presentation/878316121/5G-NG-Core-Architecture-Explanation)
6. [https://www.docomo.ne.jp/english/corporate/technology/rd/technical_journal/bn/vol24_4/001.html](https://www.docomo.ne.jp/english/corporate/technology/rd/technical_journal/bn/vol24_4/001.html)
7. [https://embeddedcomputing.com/application/networking-5g/5g-primer-part-3-5g-core-network](https://embeddedcomputing.com/application/networking-5g/5g-primer-part-3-5g-core-network)
8. [https://flolive.net/blog/glossary/5g-core-network-architecture-9-key-network-functions/](https://flolive.net/blog/glossary/5g-core-network-architecture-9-key-network-functions/)
9. [https://www.a10networks.com/blog/5g-is-about-to-change-the-world-heres-how-it-works/](https://www.a10networks.com/blog/5g-is-about-to-change-the-world-heres-how-it-works/)
10. [https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-22610FA3-72E1-44DE-8D0C-649916FAACF3.html](https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-22610FA3-72E1-44DE-8D0C-649916FAACF3.html)
11. [https://sdnfv.zte.com.cn/en/products/VNF/5G-core-network](https://sdnfv.zte.com.cn/en/products/VNF/5G-core-network)
12. [https://techdocs.broadcom.com/us/en/vmware-sde/telco-cloud/vmware-telco-cloud-platform/3-1/telco-cloud-reference-architecture-guide/architectural-overview/telco-5g-architecture.html](https://techdocs.broadcom.com/us/en/vmware-sde/telco-cloud/vmware-telco-cloud-platform/3-1/telco-cloud-reference-architecture-guide/architectural-overview/telco-5g-architecture.html)
13. [http://www.techtimes.com/articles/309128/20250120/designing-deploying-5g-core-edge-end-end-networking.htm](http://www.techtimes.com/articles/309128/20250120/designing-deploying-5g-core-edge-end-end-networking.htm)
14. [https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-CEA58D34-49D5-427D-B41B-4FAFFFCB454A.html](https://docs.vmware.com/en/VMware-Telco-Cloud-Platform-RAN/2.2/telco-cloud-platform-ran-reference-architecture-guide-22/GUID-CEA58D34-49D5-427D-B41B-4FAFFFCB454A.html)
15. [https://www.semiconductors.org/wp-content/uploads/2020/07/SIA-5G-Report_2.pdf](https://www.semiconductors.org/wp-content/uploads/2020/07/SIA-5G-Report_2.pdf)
16. [https://carrier.huawei.com/~/media/CNBGV2/download/products/network-energy/5G-oriented-Data-Center-Facility-en.pdf](https://carrier.huawei.com/~/media/CNBGV2/download/products/network-energy/5G-oriented-Data-Center-Facility-en.pdf)
17. [https://www.open5gcore.org](https://www.open5gcore.org/)
18. [https://www.huaweicentral.com/huawei-edges-out-ericsson-and-nokia-in-5g-network-market-despite-u-s-sanctions/](https://www.huaweicentral.com/huawei-edges-out-ericsson-and-nokia-in-5g-network-market-despite-u-s-sanctions/)
19. [https://www.abiresearch.com/press/ericsson-and-huawei-take-the-lead-in-abi-researchs-5g-core-edge-platforms-competitive-ranking-mavenir-affirmed-networks-named-top-challengers/](https://www.abiresearch.com/press/ericsson-and-huawei-take-the-lead-in-abi-researchs-5g-core-edge-platforms-competitive-ranking-mavenir-affirmed-networks-named-top-challengers/)
20. [https://www.abiresearch.com/press/huawei-and-ericsson-take-the-lead-in-abi-researchs-5g-end-to-end-core-network-automation-and-orchestration-vendor-competitive-ranking](https://www.abiresearch.com/press/huawei-and-ericsson-take-the-lead-in-abi-researchs-5g-end-to-end-core-network-automation-and-orchestration-vendor-competitive-ranking)
21. [https://www.ericsson.com/en/news/2024/9/ericsson-named-a-leader-in-the-2024-gartner-magic-quadrant-for-csp-5g-core-network-infrastructure-solutions](https://www.ericsson.com/en/news/2024/9/ericsson-named-a-leader-in-the-2024-gartner-magic-quadrant-for-csp-5g-core-network-infrastructure-solutions)
22. [https://mobile-magazine.com/top10/top-10-5g-edge-computing-platforms](https://mobile-magazine.com/top10/top-10-5g-edge-computing-platforms)
23. [https://www.mordorintelligence.com/industry-reports/5g-core-network-market](https://www.mordorintelligence.com/industry-reports/5g-core-network-market)
24. [https://telecomlead.com/telecom-equipment/mobile-core-network-vendors-and-investment-trends-in-q1-2025-121082](https://telecomlead.com/telecom-equipment/mobile-core-network-vendors-and-investment-trends-in-q1-2025-121082)
25. [https://www.lightreading.com/virtualization/how-a-new-crop-of-vendors-is-breaking-into-the-5g-core](https://www.lightreading.com/virtualization/how-a-new-crop-of-vendors-is-breaking-into-the-5g-core)
26. [https://datacentremagazine.com/articles/top-10-5g-infrastructure-companies](https://datacentremagazine.com/articles/top-10-5g-infrastructure-companies)
27. [https://market.us/report/5g-core-network-market/](https://market.us/report/5g-core-network-market/)
28. [https://www.linkedin.com/pulse/5g-core-market-size-share-scope-trends-forecast-vista-nova-research-kyace/](https://www.linkedin.com/pulse/5g-core-market-size-share-scope-trends-forecast-vista-nova-research-kyace/)
29. [https://www.ericsson.com/en/reports-and-papers/mobility-report/dataforecasts/network-coverage](https://www.ericsson.com/en/reports-and-papers/mobility-report/dataforecasts/network-coverage)
30. [https://niralnetworks.com/5g-core-network-architecture/](https://niralnetworks.com/5g-core-network-architecture/)
31. [https://www.amantyatech.com/5g/5g-core](https://www.amantyatech.com/5g/5g-core)
32. [https://www.juniper.net/documentation/us/en/software/junos/agf-user-guide/topics/concept/agf-5g-overview.html](https://www.juniper.net/documentation/us/en/software/junos/agf-user-guide/topics/concept/agf-5g-overview.html)
33. [https://www.intel.com/content/dam/www/central-libraries/us/en/documents/2024-05/intel-5g-sa-core-industry-perspective-no-1-deployment-report-2nd-revision-032124.pdf](https://www.intel.com/content/dam/www/central-libraries/us/en/documents/2024-05/intel-5g-sa-core-industry-perspective-no-1-deployment-report-2nd-revision-032124.pdf)
34. [https://www.grandmetric.com/5g-core-network-functions/](https://www.grandmetric.com/5g-core-network-functions/)
35. [https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/Studies/5G/5G_Core_Network.pdf?__blob=publicationFile&v=4](https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/Studies/5G/5G_Core_Network.pdf?__blob=publicationFile&v=4)
36. [https://www.ericsson.com/en/5g/5g-sa](https://www.ericsson.com/en/5g/5g-sa)
37. [https://www.youtube.com/watch?v=Q6YxHz_07zk](https://www.youtube.com/watch?v=Q6YxHz_07zk)
38. [https://www.ericsson.com/en/core-network/5g-core](https://www.ericsson.com/en/core-network/5g-core)
39. [https://www.linkedin.com/pulse/5g-nr-sa-standalone-architecture-overview-ravi-shekhar-saa0c](https://www.linkedin.com/pulse/5g-nr-sa-standalone-architecture-overview-ravi-shekhar-saa0c)
40. [https://en.wikipedia.org/wiki/5G_network_slicing](https://en.wikipedia.org/wiki/5G_network_slicing)
41. [https://www.grandmetric.com/5g-core-network-a-short-overview/](https://www.grandmetric.com/5g-core-network-a-short-overview/)
42. [https://www.cisco.com/c/en/us/td/docs/wireless/asr_5000/21-28/5g-nsa-solution/21-28-5g-nsa-solution-guide/m_5g-overview.pdf](https://www.cisco.com/c/en/us/td/docs/wireless/asr_5000/21-28/5g-nsa-solution/21-28-5g-nsa-solution-guide/m_5g-overview.pdf)
43. [https://www.supermicro.com/en/glossary/5g-core](https://www.supermicro.com/en/glossary/5g-core)
44. [https://www.sdxcentral.com/5g/definitions/key-elements-5g-network/5g-network-infrastructure/](https://www.sdxcentral.com/5g/definitions/key-elements-5g-network/5g-network-infrastructure/)
45. [https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/Studies/5G/5G_Infrastructure.pdf?__blob=publicationFile&v=3](https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/Studies/5G/5G_Infrastructure.pdf?__blob=publicationFile&v=3)
46. [https://www.nokia.com/core/5g-core/](https://www.nokia.com/core/5g-core/)
47. [https://infohub.delltechnologies.com/en-us/l/dell-telecom-infrastructure-blocks-for-red-hat-4-0-architecture-guide/5g-core-network-use-cases/](https://infohub.delltechnologies.com/en-us/l/dell-telecom-infrastructure-blocks-for-red-hat-4-0-architecture-guide/5g-core-network-use-cases/)
48. [https://5glab.orange.com/en/infrastructure-and-equipment-the-basics-for-understanding-how-5g-works/](https://5glab.orange.com/en/infrastructure-and-equipment-the-basics-for-understanding-how-5g-works/)
49. [https://www.heavy.ai/technical-glossary/5g-infrastructure](https://www.heavy.ai/technical-glossary/5g-infrastructure)
50. [https://www.celona.io/5g-lan/5g-core](https://www.celona.io/5g-lan/5g-core)
51. [https://www.telefonica.de/news/press-releases-telefonica-germany/2024/11/new-core-network-launched-5g-cloud-core-from-o2-telefonica-reaches-one-million-users.html](https://www.telefonica.de/news/press-releases-telefonica-germany/2024/11/new-core-network-launched-5g-cloud-core-from-o2-telefonica-reaches-one-million-users.html)
52. [https://www.marketresearchfuture.com/reports/5g-core-market/companies](https://www.marketresearchfuture.com/reports/5g-core-market/companies)
53. [https://www.lightreading.com/5g/ericsson-nokia-boast-5g-wins-against-each-other-but-fail-to-stop-huawei](https://www.lightreading.com/5g/ericsson-nokia-boast-5g-wins-against-each-other-but-fail-to-stop-huawei)
54. [https://www.emergenresearch.com/blog/top-10-companies-leading-the-5g-network-industry](https://www.emergenresearch.com/blog/top-10-companies-leading-the-5g-network-industry)
55. [https://alepo.com/solutions/5g-core-network-solutions/](https://alepo.com/solutions/5g-core-network-solutions/)
56. [https://www.fierce-network.com/wireless/nokia-ericsson-huawei-score-5g-wins-but-too-early-to-call-winners-analysts](https://www.fierce-network.com/wireless/nokia-ericsson-huawei-score-5g-wins-but-too-early-to-call-winners-analysts)
57. [https://www.sphericalinsights.com/blogs/explore-top-10-5g-services-companies-in-the-global-market-revenue-statistics-trends-innovations-2024-2033](https://www.sphericalinsights.com/blogs/explore-top-10-5g-services-companies-in-the-global-market-revenue-statistics-trends-innovations-2024-2033)
58. [https://map.sciencemediahub.eu/5g/popup/20](https://map.sciencemediahub.eu/5g/popup/20)
59. [https://www.huaweicentral.com/ericsson-nokia-trimmed-20000-jobs-in-2-years-as-huawei-surged-in-5g-field/](https://www.huaweicentral.com/ericsson-nokia-trimmed-20000-jobs-in-2-years-as-huawei-surged-in-5g-field/)
60. [https://www.techsciresearch.com/blog/who-s-leading-the-5g-charge-a-look-at-the-top-5-global-players/4600.html](https://www.techsciresearch.com/blog/who-s-leading-the-5g-charge-a-look-at-the-top-5-global-players/4600.html)
61. [https://www.sdxcentral.com/articles/news/ericsson-nips-huawei-nokia-in-gartners-5g-vendor-ranking/2021/02/](https://www.sdxcentral.com/articles/news/ericsson-nips-huawei-nokia-in-gartners-5g-vendor-ranking/2021/02/)
62. [https://www.expertmarketresearch.com/blogs/top-5g-infrastructure-companies](https://www.expertmarketresearch.com/blogs/top-5g-infrastructure-companies)
63. [https://www.fierce-network.com/wireless/op-ed-tale-two-5g-giants-nokia-silent-ericsson-continues-charm-offensive](https://www.fierce-network.com/wireless/op-ed-tale-two-5g-giants-nokia-silent-ericsson-continues-charm-offensive)
64. [https://www.greyb.com/blog/5g-companies/](https://www.greyb.com/blog/5g-companies/)
65. [https://www.marketsandmarkets.com/ResearchInsight/5g-core-market.asp?srsltid=AfmBOoodcU585tVHDJuUlqA0SlR_l1UcqfTSI6WvGaD6ucrnFfHjEaE8](https://www.marketsandmarkets.com/ResearchInsight/5g-core-market.asp?srsltid=AfmBOoodcU585tVHDJuUlqA0SlR_l1UcqfTSI6WvGaD6ucrnFfHjEaE8)
66. [https://www.sdxcentral.com/news/ericsson-nokia-huawei-samsung-dominate-5g-gear-innovation/](https://www.sdxcentral.com/news/ericsson-nokia-huawei-samsung-dominate-5g-gear-innovation/)
67. [https://www.custommarketinsights.com/report/5g-core-network-market/](https://www.custommarketinsights.com/report/5g-core-network-market/)
68. [https://www.analysysmason.com/research/content/articles/5g-deployments-standalone-rma18/](https://www.analysysmason.com/research/content/articles/5g-deployments-standalone-rma18/)
69. [https://www.analysysmason.com/research/content/short-reports/5g-network-cloud-report-rma16/](https://www.analysysmason.com/research/content/short-reports/5g-network-cloud-report-rma16/)
70. [https://www.thebusinessresearchcompany.com/report/5g-core-global-market-report](https://www.thebusinessresearchcompany.com/report/5g-core-global-market-report)
71. [https://www.counterpointresearch.com/insights/5g-sa-core-deployments-2023/](https://www.counterpointresearch.com/insights/5g-sa-core-deployments-2023/)
72. [https://www.einnews.com/pr_news/719922874/5g-core-market-size-share-revenue-trends-and-drivers-for-2024-2033](https://www.einnews.com/pr_news/719922874/5g-core-market-size-share-revenue-trends-and-drivers-for-2024-2033)
73. [https://blog.tbrc.info/2024/05/5g-core-market-share/](https://blog.tbrc.info/2024/05/5g-core-market-share/)
74. [https://www.analysysmason.com/contentassets/00f7f64a8ebc4a5cb2f3efaefc83060b/analysys_mason_5g_deployments_standalone_apr2022_rma18.pdf](https://www.analysysmason.com/contentassets/00f7f64a8ebc4a5cb2f3efaefc83060b/analysys_mason_5g_deployments_standalone_apr2022_rma18.pdf)
75. [https://www.openpr.com/news/3689293/5g-core-network-market-report-2024-size-growth-trends](https://www.openpr.com/news/3689293/5g-core-network-market-report-2024-size-growth-trends)
76. [https://www.rcrwireless.com/20250521/5g/mobile-core-network-q1-delloro](https://www.rcrwireless.com/20250521/5g/mobile-core-network-q1-delloro)
77. [https://edrawmax.wondershare.com/templates/network-diagram-for-5g.html](https://edrawmax.wondershare.com/templates/network-diagram-for-5g.html)
78. [https://opus.bibliothek.uni-wuerzburg.de/files/32210/Raffeck_et_al_5G_Core_Networks_WueWoWas23_1570913313.pdf](https://opus.bibliothek.uni-wuerzburg.de/files/32210/Raffeck_et_al_5G_Core_Networks_WueWoWas23_1570913313.pdf)
79. [https://moniem-tech.com/2023/10/28/5g-core-network-functions-nfs/](https://moniem-tech.com/2023/10/28/5g-core-network-functions-nfs/)
80. [https://yatebts.com/documentation/concepts/5g-core-network/](https://yatebts.com/documentation/concepts/5g-core-network/)
81. [https://www.huawei.com/~/media/CORPORATE/PDF/white%20paper/5G-Nework-Architecture-Whitepaper-en.pdf](https://www.huawei.com/~/media/CORPORATE/PDF/white%20paper/5G-Nework-Architecture-Whitepaper-en.pdf)
82. [https://www.digi.com/blog/post/5g-network-architecture](https://www.digi.com/blog/post/5g-network-architecture)
83. [https://www.youtube.com/watch?v=_R0ElPgy5bo](https://www.youtube.com/watch?v=_R0ElPgy5bo)
84. [https://www.slideshare.net/slideshow/5-g-core-overview/250518243](https://www.slideshare.net/slideshow/5-g-core-overview/250518243)
85. [https://5g-ppp.eu/wp-content/uploads/2019/07/5G-PPP-5G-Architecture-White-Paper_v3.0_PublicConsultation.pdf](https://5g-ppp.eu/wp-content/uploads/2019/07/5G-PPP-5G-Architecture-White-Paper_v3.0_PublicConsultation.pdf)
86. [https://www.intel.com/content/www/us/en/wireless-network/core-network.html](https://www.intel.com/content/www/us/en/wireless-network/core-network.html)
87. [https://www.cisco.com/c/en/us/td/docs/wireless/ucc/sgw/2023-03/config-admin/b_ucc-5g-cnsgwc-config-and-admin-guide_2023_03/m_5garchitecture.pdf](https://www.cisco.com/c/en/us/td/docs/wireless/ucc/sgw/2023-03/config-admin/b_ucc-5g-cnsgwc-config-and-admin-guide_2023_03/m_5garchitecture.pdf)


# Technical and Vendor Landscape of Mobile Networks: From RAN to Core and Internet Access

The mobile network ecosystem encompasses a complex technical architecture that spans from radio access to core network functions and internet connectivity. This comprehensive landscape involves multiple technology layers, sophisticated vendor ecosystems, and evolving architectural paradigms that collectively enable modern mobile communications.

## Radio Access Network (RAN) Architecture and Components

The **Radio Access Network (RAN)** serves as the critical bridge between mobile devices and the core network, managing radio spectrum efficiently while meeting quality-of-service requirements for users[1](https://tomorrowdesk.com/info/radio-access-network)[2](https://www.techtarget.com/searchnetworking/definition/radio-access-network-RAN). Modern RAN implementations operate across frequency bands ranging from 600 MHz to 39 GHz, utilizing both Frequency Division Duplexing (FDD) and Time Division Duplexing (TDD) modes to optimize spectrum usage[1](https://tomorrowdesk.com/info/radio-access-network).

## Core RAN Components

**Base Station Architecture**: The fundamental component is the **gNodeB (Next Generation NodeB)** in 5G networks, which can be deployed as integrated units or split into distributed components[2](https://www.techtarget.com/searchnetworking/definition/radio-access-network-RAN)[3](https://www.telecomhall.net/t/what-is-radio-access-network-ran/31048). The split architecture includes:

- **Radio Unit (RU)**: Handles radio frequency processing and signal amplification, typically mounted near antennas to minimize transmission losses[1](https://tomorrowdesk.com/info/radio-access-network)[3](https://www.telecomhall.net/t/what-is-radio-access-network-ran/31048)
    
- **Distributed Unit (DU)**: Performs real-time baseband processing, scheduling, and MAC layer functions[2](https://www.techtarget.com/searchnetworking/definition/radio-access-network-RAN)[3](https://www.telecomhall.net/t/what-is-radio-access-network-ran/31048)
    
- **Centralized Unit (CU)**: Manages higher-layer functions including RRC and PDCP protocols[2](https://www.techtarget.com/searchnetworking/definition/radio-access-network-RAN)[3](https://www.telecomhall.net/t/what-is-radio-access-network-ran/31048)
    

**Advanced Technologies**: Modern RAN implementations incorporate **Massive MIMO** (Multiple Input Multiple Output) technology, beamforming capabilities, and carrier aggregation, enabling data rates exceeding 10 Gbps in optimal conditions while maintaining latency below 1 millisecond for critical applications[1](https://tomorrowdesk.com/info/radio-access-network).

## RAN Vendor Landscape

The global RAN market is dominated by established telecommunications equipment vendors. **Huawei continues to lead the 5G RAN market** for the sixth consecutive year as of H1 2024, scoring highly across all assessment categories including Active Antenna Units (AAU), Remote Radio Units (RRU), mmWave technology, Baseband Units (BBU), and energy efficiency[4](https://www.huaweicentral.com/huawei-continues-to-lead-5g-ran-equipment-market-in-h1-2024-globaldata/)[5](https://www.huawei.com/en/news/2024/6/globaldata-5g).

**Market Leadership Rankings**:

1. **Huawei**: Dominates with superior portfolio diversity, module output power, and compactness in AAU products, plus comprehensive mmWave solutions[4](https://www.huaweicentral.com/huawei-continues-to-lead-5g-ran-equipment-market-in-h1-2024-globaldata/)[5](https://www.huawei.com/en/news/2024/6/globaldata-5g)
    
2. **Ericsson**: Leads in portfolio breadth and competitiveness, ranking second in business performance with strong massive MIMO products and energy-efficient baseband units[6](https://www.5gworldpro.com/blog/2024/07/07/market-landscape-ran-vendors-2024/)[7](https://moniem-tech.com/2024/07/05/market-landscape-ran-vendors-2024/)
    
3. **Nokia**: Ranks third in both portfolio and business performance dimensions, with robust RAN solutions and strong baseband capabilities[6](https://www.5gworldpro.com/blog/2024/07/07/market-landscape-ran-vendors-2024/)[7](https://moniem-tech.com/2024/07/05/market-landscape-ran-vendors-2024/)
    
4. **ZTE Corporation**: Has risen to leadership position since 2023, strengthening business performance through market share gains[6](https://www.5gworldpro.com/blog/2024/07/07/market-landscape-ran-vendors-2024/)[7](https://moniem-tech.com/2024/07/05/market-landscape-ran-vendors-2024/)
    
5. **Samsung Networks**: Leads in Open vRAN solutions despite having a less extensive overall portfolio[6](https://www.5gworldpro.com/blog/2024/07/07/market-landscape-ran-vendors-2024/)[7](https://moniem-tech.com/2024/07/05/market-landscape-ran-vendors-2024/)
    

## Open RAN Evolution

**Open RAN** represents a significant architectural shift toward disaggregated, interoperable network components. The technology is expected to capture **6-8% of the total RAN market by the end of 2024**, growing from a smaller base but with accelerating momentum[8](https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir/)[9](https://www.aap.com.au/aapreleases/cision20240124ae19285/)[10](https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir).

**Open RAN Vendor Ecosystem**: Leading Open RAN vendors include Samsung, Mavenir, NEC, Fujitsu, Rakuten Symphony, and Parallel Wireless, which collectively hold around 95-97% of the total Open RAN market share[8](https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir/)[9](https://www.aap.com.au/aapreleases/cision20240124ae19285/)[10](https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir). However, incumbent vendors like Ericsson and Nokia are developing their own Open RAN ecosystems and are expected to create fierce competition in the coming years[8](https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir/)[9](https://www.aap.com.au/aapreleases/cision20240124ae19285/)[10](https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir).

## Transport Network Architecture

The transport network provides the crucial connectivity infrastructure that links RAN components to core network functions, encompassing **fronthaul, midhaul, and backhaul** segments[11](https://www.ciena.com/insights/articles/Primer-Mobile-backhaul-vs-mobile-fronthaul_prx.html)[12](https://www.gsma.com/solutions-and-impact/technologies/networks/gsma_resources/mobile-backhaul-an-overview/)[13](https://www.nokia.com/mobile-transport/).

## Fronthaul Networks

**Fronthaul** connects Remote Radio Heads (RRHs) or Radio Units (RUs) to Baseband Units (BBUs) or Distributed Units (DUs)[11](https://www.ciena.com/insights/articles/Primer-Mobile-backhaul-vs-mobile-fronthaul_prx.html)[14](https://infinitytdc.com/understanding-fronthaul-backhaul-cellular/)[15](https://wraycastle.com/blogs/glossary/what-is-5g-fronthaul-and-backhaul). This connection is essential for transmitting data between radio and baseband processing units, requiring high-capacity, low-latency connections to enable rapid data transmission[15](https://wraycastle.com/blogs/glossary/what-is-5g-fronthaul-and-backhaul).

In 5G networks, fronthaul utilizes **Common Public Radio Interface (CPRI)** or **enhanced CPRI (eCPRI)** protocols to manage the connection between distributed RAN components[14](https://infinitytdc.com/understanding-fronthaul-backhaul-cellular/)[15](https://wraycastle.com/blogs/glossary/what-is-5g-fronthaul-and-backhaul). The fronthaul network must handle increased bandwidth demands from technologies like Massive MIMO and wider channel bandwidths[11](https://www.ciena.com/insights/articles/Primer-Mobile-backhaul-vs-mobile-fronthaul_prx.html)[14](https://infinitytdc.com/understanding-fronthaul-backhaul-cellular/).

## Backhaul Networks

**Backhaul** connects base stations to the mobile core network, serving as the primary data transport path from cell sites to Mobile Switching Centers or core network functions[11](https://www.ciena.com/insights/articles/Primer-Mobile-backhaul-vs-mobile-fronthaul_prx.html)[12](https://www.gsma.com/solutions-and-impact/technologies/networks/gsma_resources/mobile-backhaul-an-overview/)[13](https://www.nokia.com/mobile-transport/). Traditional copper-based T1/E1 connections have largely migrated to high-capacity fiber optic and microwave solutions to support data-intensive applications[11](https://www.ciena.com/insights/articles/Primer-Mobile-backhaul-vs-mobile-fronthaul_prx.html)[14](https://infinitytdc.com/understanding-fronthaul-backhaul-cellular/).

**Backhaul Technologies**:

- **Fiber Optics**: Preferred for urban and suburban deployments due to substantial bandwidth and reliability[14](https://infinitytdc.com/understanding-fronthaul-backhaul-cellular/)
    
- **Microwave Links**: Advantageous for remote or challenging terrain where fiber deployment is impractical[14](https://infinitytdc.com/understanding-fronthaul-backhaul-cellular/)
    
- **Ethernet-over-Fiber**: Typically via 1Gbps physical interfaces for macro cell sites[11](https://www.ciena.com/insights/articles/Primer-Mobile-backhaul-vs-mobile-fronthaul_prx.html)
    

## Transport Network Vendors

The transport network market includes both traditional telecommunications equipment vendors and specialized networking companies:

**Major Players**:

- **Nokia**: Provides comprehensive mobile transport solutions including fronthaul, midhaul, and backhaul technologies[13](https://www.nokia.com/mobile-transport/)
    
- **Ericsson**: Offers end-to-end transport solutions with focus on 5G network slicing and edge computing integration[16](https://www.juniper.net/assets/cn/zh/local/pdf/additional-resources/3200069-en.pdf)
    
- **Ciena**: Specializes in optical networking and software automation, serving service providers and hyperscalers[17](https://mobile-magazine.com/5g-and-iot/top-10-mobile-infrastructure-vendors)
    
- **Juniper Networks**: Focuses on 5G networking and automation solutions with Cloud Metro offerings[17](https://mobile-magazine.com/5g-and-iot/top-10-mobile-infrastructure-vendors)
    

## Core Network Architecture and Evolution

The **5G Core Network (5GC)** represents a fundamental architectural shift from traditional telecommunications infrastructure to a cloud-native, service-based approach[Previous conversation]. Unlike previous generations that relied on dedicated hardware, the 5G core is entirely software-based and designed to run on virtualized infrastructure.

## Network Function Virtualization

The 5G core operates through **Network Functions (NFs)** that communicate via standardized APIs using HTTP/2 and REST protocols[Previous conversation]. Key network functions include:

**Control Plane Functions**:

- **Access and Mobility Management Function (AMF)**: Manages authentication, mobility, and connection establishment
    
- **Session Management Function (SMF)**: Handles session establishment and IP address allocation
    
- **Policy Control Function (PCF)**: Manages network policies and quality of service
    

**User Plane Functions**:

- **User Plane Function (UPF)**: Handles data traffic routing and packet inspection, deployable at network edges for low-latency applications
    

## Network Slicing

**Network slicing** enables operators to create multiple virtualized, independent logical networks on shared physical infrastructure[18](https://www.viavisolutions.com/en-us/5g-network-slicing)[19](https://en.wikipedia.org/wiki/5G_network_slicing)[20](https://www.rcrwireless.com/20180404/5g/understanding-end-to-end-network-slicing-for-5g). Each slice represents an isolated end-to-end network tailored to specific application requirements, from high-reliability services to ultra-low latency applications[18](https://www.viavisolutions.com/en-us/5g-network-slicing)[19](https://en.wikipedia.org/wiki/5G_network_slicing).

**Slicing Architecture Components**:

- **Network Function Virtualization (NFV)**: Moves network functionality to virtual machines on virtualized servers[18](https://www.viavisolutions.com/en-us/5g-network-slicing)
    
- **Software-Defined Networking (SDN)**: Manages traffic flows through centralized control plane APIs[18](https://www.viavisolutions.com/en-us/5g-network-slicing)
    
- **End-to-End Slicing**: Spans RAN, transport, and core network segments[21](https://www.onap.org/wp-content/uploads/sites/20/2020/12/ONAP_Technical-Overview_120720.pdf)
    

## Core Network Vendors

The core network market maintains similar vendor leadership patterns as the RAN market:

**Leading Vendors**:

- **Huawei**: Continues to dominate with comprehensive 5G core solutions and strong presence in China and emerging markets[Previous conversation]
    
- **Ericsson**: Strong in Western markets with cloud-native 5G core solutions and network slicing capabilities[Previous conversation]
    
- **Nokia**: Maintains significant presence with robust core network portfolio[Previous conversation]
    
- **ZTE**: Growing presence particularly in Chinese market with AI-centric 5.5G features[Previous conversation]
    

## Internet Access and External Connectivity

The mobile network's connection to external networks, particularly the Internet, involves sophisticated gateway functions and peering arrangements that enable global connectivity.

## Internet Gateway Functions

**Mobile Core Integration**: The core network provides external packet data network (Internet) connectivity to mobile subscribers while ensuring authentication and service quality adherence[22](https://open-cloud.github.io/arch.html)[23](https://gist.github.com/edecoux/25278021fadbf91c7aca0cfa72ca93d5/). The **Packet Data Network Gateway (P-GW)** in 4G networks and **User Plane Function (UPF)** in 5G networks serve as the primary Internet access points[22](https://open-cloud.github.io/arch.html)[23](https://gist.github.com/edecoux/25278021fadbf91c7aca0cfa72ca93d5/).

**IP-Based Connectivity**: Modern mobile networks utilize IP-based connectivity between RAN and core network components, representing a fundamental shift from earlier circuit-based architectures[22](https://open-cloud.github.io/arch.html)[23](https://gist.github.com/edecoux/25278021fadbf91c7aca0cfa72ca93d5/). This enables seamless integration with Internet protocols and services.

## Edge Computing Integration

**Multi-Access Edge Computing (MEC)** brings computing resources closer to users, reducing latency and improving service quality[24](https://www.linkedin.com/pulse/navigating-future-2024-trends-mobile-operators-network-performance-jpz6f)[25](https://www.samsung.com/global/business/networks/insights/blog/0114-the-path-to-intelligent-networks-a-look-back-at-2024-a-look-ahead-to-2025/?msockid=30fa3b1af1d569bc1fa32d10f0fc6881). Edge computing infrastructure is increasingly deployed at cell sites and regional data centers to support real-time applications and services.

**Edge Deployment Models**:

- **Cell-site Edge**: Computing resources co-located with base stations
    
- **Regional Edge**: Distributed computing nodes serving multiple cell sites
    
- **Central Cloud**: Traditional centralized computing resources
    

## Market Dynamics and Trends

## Overall Market Performance

The global telecom equipment market has experienced mixed performance, with **worldwide revenues declining 11% year-over-year in 2024**, marking the steepest annual decline in more than 20 years[26](https://techblog.comsoc.org/2025/03/22/global-telecom-infrastructure-market-outlook-after-a-dismal-2024/). This decline was broad-based across segments including RAN, optical transport, and core networks[26](https://techblog.comsoc.org/2025/03/22/global-telecom-infrastructure-market-outlook-after-a-dismal-2024/).

**Market Concentration**: The top three vendors - Huawei, Ericsson, and Nokia - continue to dominate, accounting for **37.5% of the total telco network infrastructure market** in annualized Q3 2024[27](https://www.businesswire.com/news/home/20250214480061/en/Telecoms-Largest-Vendors-in-3Q-2024-Key-Market-Shifts-Vendor-Revenue-Performance-and-Future-Trends---ResearchAndMarkets.com). Huawei remains the largest vendor globally with a **31% market share**, though its position is geographically fragmented due to restrictions in Western markets[28](https://mobile-magazine.com/news/huawei-ericsson-nokia-face-telecoms-tech-shift).

## Technology Transformation Trends

**Virtualization Adoption**: The **virtualized RAN (vRAN) market** represents only **10% of the total RAN baseband market** in 2023, with slow growth projected to reach 20% by 2028[29](https://techblog.comsoc.org/2025/01/07/vran-market-disappoints-just-like-openran-and-mobile-5g/). Despite the modest current adoption, the vRAN market is expected to grow significantly, from **$1.5 billion in 2023 to $31.3 billion by 2033** at a CAGR of 35.5%[30](https://market.us/report/virtualized-ran-vran-market/).

**Open RAN Progress**: While Open RAN adoption remains limited, the market is **expected to grow from $2.39 billion in 2024 to $38.71 billion by 2034** with a CAGR of 32.11%[31](https://www.precedenceresearch.com/open-ran-market). North America leads adoption with a 45% market share, driven by regulatory support and 5G deployment initiatives[31](https://www.precedenceresearch.com/open-ran-market).

## Regional Market Dynamics

**Geographic Distribution**: The market demonstrates clear regional splits, with **Asia-Pacific holding 23% of global revenue** and expected to grow at 10% CAGR through 203132. China and emerging markets remain strongholds for Chinese vendors, while Western markets increasingly restrict their participation[28](https://mobile-magazine.com/news/huawei-ericsson-nokia-face-telecoms-tech-shift)[33](https://www.sdxcentral.com/news/ericsson-nokia-huawei-samsung-dominate-5g-gear-innovation/).

**Vendor Positioning**: The telecommunications equipment landscape is experiencing a **"tech shift"** as vendors pivot from hardware-centric to software-defined, AI-powered solutions[28](https://mobile-magazine.com/news/huawei-ericsson-nokia-face-telecoms-tech-shift). This transformation is driven by slowing 5G capital expenditure and the need for operational efficiency improvements[28](https://mobile-magazine.com/news/huawei-ericsson-nokia-face-telecoms-tech-shift).

The mobile network ecosystem continues to evolve rapidly, with traditional equipment vendors adapting to new architectural paradigms while emerging players challenge established market positions through innovative approaches to network disaggregation and virtualization.

1. [https://tomorrowdesk.com/info/radio-access-network](https://tomorrowdesk.com/info/radio-access-network)
2. [https://www.techtarget.com/searchnetworking/definition/radio-access-network-RAN](https://www.techtarget.com/searchnetworking/definition/radio-access-network-RAN)
3. [https://www.telecomhall.net/t/what-is-radio-access-network-ran/31048](https://www.telecomhall.net/t/what-is-radio-access-network-ran/31048)
4. [https://www.huaweicentral.com/huawei-continues-to-lead-5g-ran-equipment-market-in-h1-2024-globaldata/](https://www.huaweicentral.com/huawei-continues-to-lead-5g-ran-equipment-market-in-h1-2024-globaldata/)
5. [https://www.huawei.com/en/news/2024/6/globaldata-5g](https://www.huawei.com/en/news/2024/6/globaldata-5g)
6. [https://www.5gworldpro.com/blog/2024/07/07/market-landscape-ran-vendors-2024/](https://www.5gworldpro.com/blog/2024/07/07/market-landscape-ran-vendors-2024/)
7. [https://moniem-tech.com/2024/07/05/market-landscape-ran-vendors-2024/](https://moniem-tech.com/2024/07/05/market-landscape-ran-vendors-2024/)
8. [https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir/](https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir/)
9. [https://www.aap.com.au/aapreleases/cision20240124ae19285/](https://www.aap.com.au/aapreleases/cision20240124ae19285/)
10. [https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir](https://www.abiresearch.com/press/open-ran-set-to-capture-6-8-of-total-ran-market-by-end-of-2024-fueled-by-initiatives-from-fujitsu-samsung-rakuten-symphony-and-mavenir)
11. [https://www.ciena.com/insights/articles/Primer-Mobile-backhaul-vs-mobile-fronthaul_prx.html](https://www.ciena.com/insights/articles/Primer-Mobile-backhaul-vs-mobile-fronthaul_prx.html)
12. [https://www.gsma.com/solutions-and-impact/technologies/networks/gsma_resources/mobile-backhaul-an-overview/](https://www.gsma.com/solutions-and-impact/technologies/networks/gsma_resources/mobile-backhaul-an-overview/)
13. [https://www.nokia.com/mobile-transport/](https://www.nokia.com/mobile-transport/)
14. [https://infinitytdc.com/understanding-fronthaul-backhaul-cellular/](https://infinitytdc.com/understanding-fronthaul-backhaul-cellular/)
15. [https://wraycastle.com/blogs/glossary/what-is-5g-fronthaul-and-backhaul](https://wraycastle.com/blogs/glossary/what-is-5g-fronthaul-and-backhaul)
16. [https://www.juniper.net/assets/cn/zh/local/pdf/additional-resources/3200069-en.pdf](https://www.juniper.net/assets/cn/zh/local/pdf/additional-resources/3200069-en.pdf)
17. [https://mobile-magazine.com/5g-and-iot/top-10-mobile-infrastructure-vendors](https://mobile-magazine.com/5g-and-iot/top-10-mobile-infrastructure-vendors)
18. [https://www.viavisolutions.com/en-us/5g-network-slicing](https://www.viavisolutions.com/en-us/5g-network-slicing)
19. [https://en.wikipedia.org/wiki/5G_network_slicing](https://en.wikipedia.org/wiki/5G_network_slicing)
20. [https://www.rcrwireless.com/20180404/5g/understanding-end-to-end-network-slicing-for-5g](https://www.rcrwireless.com/20180404/5g/understanding-end-to-end-network-slicing-for-5g)
21. [https://www.onap.org/wp-content/uploads/sites/20/2020/12/ONAP_Technical-Overview_120720.pdf](https://www.onap.org/wp-content/uploads/sites/20/2020/12/ONAP_Technical-Overview_120720.pdf)
22. [https://open-cloud.github.io/arch.html](https://open-cloud.github.io/arch.html)
23. [https://gist.github.com/edecoux/25278021fadbf91c7aca0cfa72ca93d5/](https://gist.github.com/edecoux/25278021fadbf91c7aca0cfa72ca93d5/)
24. [https://www.linkedin.com/pulse/navigating-future-2024-trends-mobile-operators-network-performance-jpz6f](https://www.linkedin.com/pulse/navigating-future-2024-trends-mobile-operators-network-performance-jpz6f)
25. [https://www.samsung.com/global/business/networks/insights/blog/0114-the-path-to-intelligent-networks-a-look-back-at-2024-a-look-ahead-to-2025/?msockid=30fa3b1af1d569bc1fa32d10f0fc6881](https://www.samsung.com/global/business/networks/insights/blog/0114-the-path-to-intelligent-networks-a-look-back-at-2024-a-look-ahead-to-2025/?msockid=30fa3b1af1d569bc1fa32d10f0fc6881)
26. [https://techblog.comsoc.org/2025/03/22/global-telecom-infrastructure-market-outlook-after-a-dismal-2024/](https://techblog.comsoc.org/2025/03/22/global-telecom-infrastructure-market-outlook-after-a-dismal-2024/)
27. [https://www.businesswire.com/news/home/20250214480061/en/Telecoms-Largest-Vendors-in-3Q-2024-Key-Market-Shifts-Vendor-Revenue-Performance-and-Future-Trends---ResearchAndMarkets.com](https://www.businesswire.com/news/home/20250214480061/en/Telecoms-Largest-Vendors-in-3Q-2024-Key-Market-Shifts-Vendor-Revenue-Performance-and-Future-Trends---ResearchAndMarkets.com)
28. [https://mobile-magazine.com/news/huawei-ericsson-nokia-face-telecoms-tech-shift](https://mobile-magazine.com/news/huawei-ericsson-nokia-face-telecoms-tech-shift)
29. [https://techblog.comsoc.org/2025/01/07/vran-market-disappoints-just-like-openran-and-mobile-5g/](https://techblog.comsoc.org/2025/01/07/vran-market-disappoints-just-like-openran-and-mobile-5g/)
30. [https://market.us/report/virtualized-ran-vran-market/](https://market.us/report/virtualized-ran-vran-market/)
31. [https://www.precedenceresearch.com/open-ran-market](https://www.precedenceresearch.com/open-ran-market)
32. [https://www.youtube.com/watch?v=JbjcCyF0tHs](https://www.youtube.com/watch?v=JbjcCyF0tHs)
33. [https://www.sdxcentral.com/news/ericsson-nokia-huawei-samsung-dominate-5g-gear-innovation/](https://www.sdxcentral.com/news/ericsson-nokia-huawei-samsung-dominate-5g-gear-innovation/)
34. [https://publica.fraunhofer.de/entities/publication/f46a9651-567c-4e7e-ae62-80b0110a65a2&rut=15eff4aaace5489e1a9ece73e5ed660e5c9f67925d3d3b01f4e061c11d898d18](https://publica.fraunhofer.de/entities/publication/f46a9651-567c-4e7e-ae62-80b0110a65a2&rut=15eff4aaace5489e1a9ece73e5ed660e5c9f67925d3d3b01f4e061c11d898d18)
35. [https://www.o-ran.org/research-reports/research-report-on-ran-cn-converged-architecture](https://www.o-ran.org/research-reports/research-report-on-ran-cn-converged-architecture)
36. [https://www.cablefree.net/wirelesstechnology/4glte/lte-4g-5g-radio-access-network-ran/](https://www.cablefree.net/wirelesstechnology/4glte/lte-4g-5g-radio-access-network-ran/)
37. [https://www.linkedin.com/pulse/understanding-core-elements-mobile-network-ran-christian-omeni-cdgcf](https://www.linkedin.com/pulse/understanding-core-elements-mobile-network-ran-christian-omeni-cdgcf)
38. [https://simnovus.com/revolutionizing-radio-access-network/](https://simnovus.com/revolutionizing-radio-access-network/)
39. [https://www.rcrwireless.com/20250611/test-and-measurement/open-source-mobile-core](https://www.rcrwireless.com/20250611/test-and-measurement/open-source-mobile-core)
40. [https://www.ericsson.com/en/reports-and-papers/white-papers/security-in-5g-ran-and-core-deployments](https://www.ericsson.com/en/reports-and-papers/white-papers/security-in-5g-ran-and-core-deployments)
41. [https://www.keysight.com/us/en/assets/7121-1103/ebooks/The-Essential-Guide-for-Understanding-O-RAN.pdf](https://www.keysight.com/us/en/assets/7121-1103/ebooks/The-Essential-Guide-for-Understanding-O-RAN.pdf)
42. [https://www.fierce-network.com/wireless/private-wireless-ran-revenues-jump-40-2024-led-huawei-nokia-and-ericsson](https://www.fierce-network.com/wireless/private-wireless-ran-revenues-jump-40-2024-led-huawei-nokia-and-ericsson)
43. [https://www.fujitsu.com/us/products/network/solutions/systems-integration-5g-open-ran.html](https://www.fujitsu.com/us/products/network/solutions/systems-integration-5g-open-ran.html)
44. [https://hackmd.io/@nisshakinaya/BkmhFf6qs](https://hackmd.io/@nisshakinaya/BkmhFf6qs)
45. [https://www.linkedin.com/posts/mohamedabdelmonem5g_ran-open-vran-activity-7214662995694538752-r_7a](https://www.linkedin.com/posts/mohamedabdelmonem5g_ran-open-vran-activity-7214662995694538752-r_7a)
46. [https://conferences.computer.org/iotDI/prev/2016/papers/9948a259.pdf](https://conferences.computer.org/iotDI/prev/2016/papers/9948a259.pdf)
47. [https://www.linkedin.com/pulse/2024-trends-mobile-operators-network-performance-aydin-karaer-orerf](https://www.linkedin.com/pulse/2024-trends-mobile-operators-network-performance-aydin-karaer-orerf)
48. [https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=5464c14e7770cc734cab004a0d55c9841e1ba553](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=5464c14e7770cc734cab004a0d55c9841e1ba553)
49. [https://www.adlittle.com/sites/default/files/reports/adl_mobile_network_architecture.pdf](https://www.adlittle.com/sites/default/files/reports/adl_mobile_network_architecture.pdf)
50. [https://openaccess.city.ac.uk/id/eprint/30802/](https://openaccess.city.ac.uk/id/eprint/30802/)
51. [https://www.computerweekly.com/de/definition/Fronthaul](https://www.computerweekly.com/de/definition/Fronthaul)
52. [https://android.stackexchange.com/questions/236943/set-android-as-internet-gateway-to-local-router-not-mobile-hotspot](https://android.stackexchange.com/questions/236943/set-android-as-internet-gateway-to-local-router-not-mobile-hotspot)
53. [https://arxiv.org/pdf/1611.00566.pdf](https://arxiv.org/pdf/1611.00566.pdf)
54. [https://www.cs.virginia.edu/~bjc8c/papers/zachariah15gateway.pdf](https://www.cs.virginia.edu/~bjc8c/papers/zachariah15gateway.pdf)
55. [https://arxiv.org/pdf/1708.09138.pdf](https://arxiv.org/pdf/1708.09138.pdf)
56. [https://sites.cs.ucsb.edu/~almeroth/papers/084.pdf](https://sites.cs.ucsb.edu/~almeroth/papers/084.pdf)
57. [https://hellofuture.orange.com/wp-content/uploads/sites/56/2024/05/2024-Orange-white-paper-on-Mobile-Network-Technology-Evolutions-Beyond-2030.pdf](https://hellofuture.orange.com/wp-content/uploads/sites/56/2024/05/2024-Orange-white-paper-on-Mobile-Network-Technology-Evolutions-Beyond-2030.pdf)
58. [https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=1d02c45e94c236e77d04ec694c581987f3db8bf0](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=1d02c45e94c236e77d04ec694c581987f3db8bf0)
59. [https://www.ruijie.com/en-global/support/tech-gallery/what-is-internet-gateway](https://www.ruijie.com/en-global/support/tech-gallery/what-is-internet-gateway)
60. [https://www.telecomhall.net/t/telecommunication-network-architecture-integrating-2g-3g-and-4g-lte/33898](https://www.telecomhall.net/t/telecommunication-network-architecture-integrating-2g-3g-and-4g-lte/33898)
61. [https://arxiv.org/pdf/1608.00572.pdf](https://arxiv.org/pdf/1608.00572.pdf)
62. [https://www.nokia.com/mobile-networks/ran/anyran/open-ran/open-ran-explained/](https://www.nokia.com/mobile-networks/ran/anyran/open-ran/open-ran-explained/)
63. [https://prd-mediarepository.cwsfirabarcelona.com/bona/event13/images/cbas/27905/digital-bags/file/1708015958330/2024trends.pdf](https://prd-mediarepository.cwsfirabarcelona.com/bona/event13/images/cbas/27905/digital-bags/file/1708015958330/2024trends.pdf)
64. [https://kigen.com/wp-content/uploads/2024/02/GSMA-Global-Mobile-Trends-2024.pdf](https://kigen.com/wp-content/uploads/2024/02/GSMA-Global-Mobile-Trends-2024.pdf)
65. [https://www.gsma.com/solutions-and-impact/connectivity-for-good/mobile-economy/wp-content/uploads/2024/07/240724-Mobile-Economy-Asia-Pacific-2024-FINAL.pdf](https://www.gsma.com/solutions-and-impact/connectivity-for-good/mobile-economy/wp-content/uploads/2024/07/240724-Mobile-Economy-Asia-Pacific-2024-FINAL.pdf)
66. [http://moodle.mmclab.eu/mod/page/view.php?id=10&lang=en](http://moodle.mmclab.eu/mod/page/view.php?id=10&lang=en)
67. [https://www.ericsson.com/en/blog/2023/7/how-to-build-an-end-to-end-sliced-network-embark-in-this-exciting-journey](https://www.ericsson.com/en/blog/2023/7/how-to-build-an-end-to-end-sliced-network-embark-in-this-exciting-journey)
68. [https://www.lightcounting.com/report/june-2024-telecom-network-transformation-294](https://www.lightcounting.com/report/june-2024-telecom-network-transformation-294)
69. [https://techblog.comsoc.org/2023/06/30/mtn-consulting-leading-telco-network-infrastructure-equipment-vendors/](https://techblog.comsoc.org/2023/06/30/mtn-consulting-leading-telco-network-infrastructure-equipment-vendors/)
70. [https://www.prnewswire.com/news-releases/ericsson-nokia-andrew-and-huawei-take-top-spots-in-abi-researchs-dasdrs-vendors-competitive-ranking-302446672.html](https://www.prnewswire.com/news-releases/ericsson-nokia-andrew-and-huawei-take-top-spots-in-abi-researchs-dasdrs-vendors-competitive-ranking-302446672.html)
71. [https://www.businesswire.com/news/home/20241009002909/en/Telecom-Industry-Vendor-Benchmark-Report-2024-Revenues-Top-Vendors-Key-Vendors-by-YoY-Revenue-Growth-Spending-Outlook---ResearchAndMarkets.com](https://www.businesswire.com/news/home/20241009002909/en/Telecom-Industry-Vendor-Benchmark-Report-2024-Revenues-Top-Vendors-Key-Vendors-by-YoY-Revenue-Growth-Spending-Outlook---ResearchAndMarkets.com)
72. [https://telcomagazine.com/5g-and-iot/top-10-mobile-infrastructure-vendors](https://telcomagazine.com/5g-and-iot/top-10-mobile-infrastructure-vendors)
73. [https://www.lightreading.com/open-ran/how-huawei-and-open-ran-misfires-hurt-ericsson-nokia-and-telcos](https://www.lightreading.com/open-ran/how-huawei-and-open-ran-misfires-hurt-ericsson-nokia-and-telcos)
74. [https://www.futuremarketinsights.com/reports/wireless-telecommunication-services-market-share-analysis](https://www.futuremarketinsights.com/reports/wireless-telecommunication-services-market-share-analysis)
75. [https://www.youtube.com/watch?v=A37mvWHK4J0](https://www.youtube.com/watch?v=A37mvWHK4J0)
76. [https://www.marketsandmarkets.com/ResearchInsight/indoor-5g-companies.asp](https://www.marketsandmarkets.com/ResearchInsight/indoor-5g-companies.asp)
77. [https://www.verifiedmarketresearch.com/blog/top-telecom-equipment-manufacturers/](https://www.verifiedmarketresearch.com/blog/top-telecom-equipment-manufacturers/)
78. [https://www.statista.com/statistics/199359/market-share-of-wireless-carriers-in-the-us-by-subscriptions/](https://www.statista.com/statistics/199359/market-share-of-wireless-carriers-in-the-us-by-subscriptions/)
79. [https://companiesmarketcap.com/telecommunications-equipment/largest-companies-by-market-cap/](https://companiesmarketcap.com/telecommunications-equipment/largest-companies-by-market-cap/)
80. [https://gs.statcounter.com/vendor-market-share/mobile](https://gs.statcounter.com/vendor-market-share/mobile)
81. [https://stlpartners.com/articles/private-cellular/11-companies-innovating-in-private-cellular/](https://stlpartners.com/articles/private-cellular/11-companies-innovating-in-private-cellular/)
82. [https://techhq.com/news/ericsson-nokia-oust-huawei-to-win-5g-contracts-in-singapore/](https://techhq.com/news/ericsson-nokia-oust-huawei-to-win-5g-contracts-in-singapore/)
83. [https://www.canalys.com/newsroom/global-smartphone-market-q1-2024](https://www.canalys.com/newsroom/global-smartphone-market-q1-2024)
84. [https://www.linkedin.com/pulse/mobile-network-telecom-equipment-market-key-trends-ssfsf/](https://www.linkedin.com/pulse/mobile-network-telecom-equipment-market-key-trends-ssfsf/)
85. [https://www.mordorintelligence.com/industry-reports/open-ran-market](https://www.mordorintelligence.com/industry-reports/open-ran-market)
86. [https://www.einpresswire.com/article/760174950/key-driver-transforming-the-network-devices-market-in-2024-rising-use-of-smartphone-proliferation-digital-revolution](https://www.einpresswire.com/article/760174950/key-driver-transforming-the-network-devices-market-in-2024-rising-use-of-smartphone-proliferation-digital-revolution)
87. [https://www.ericsson.com/en/news/2025/7/ericsson-leads-omdia-market-landscape-ran-vendors-2025](https://www.ericsson.com/en/news/2025/7/ericsson-leads-omdia-market-landscape-ran-vendors-2025)
88. [https://www.thebusinessresearchcompany.com/market-insights/global-telecom-equipment-market-2024](https://www.thebusinessresearchcompany.com/market-insights/global-telecom-equipment-market-2024)
89. [https://www.knowledge-sourcing.com/report/v-ran-market](https://www.knowledge-sourcing.com/report/v-ran-market)
90. [https://omdia.tech.informa.com/om121329/market-landscape-ran-vendors-2024](https://omdia.tech.informa.com/om121329/market-landscape-ran-vendors-2024)
91. [https://www.thebusinessresearchcompany.com/market-insights/telecom-equipment-market-2024](https://www.thebusinessresearchcompany.com/market-insights/telecom-equipment-market-2024)
92. [https://cdrdv2-public.intel.com/781301/intel-nt-vran-business-eguide-forintelwebteamonly.pdf](https://cdrdv2-public.intel.com/781301/intel-nt-vran-business-eguide-forintelwebteamonly.pdf)
93. [https://www.analysysmason.com/contentassets/7a45035b6a60466da873bc9d6ae455f8/analysys_mason_automated_ran_virtualisation_dec2021_rma16.pdf](https://www.analysysmason.com/contentassets/7a45035b6a60466da873bc9d6ae455f8/analysys_mason_automated_ran_virtualisation_dec2021_rma16.pdf)
94. [https://www.fiercewireless.com/tech/open-ran-take-6-8-total-ran-market-year-abi](https://www.fiercewireless.com/tech/open-ran-take-6-8-total-ran-market-year-abi)
95. [https://blog.tbrc.info/2024/11/telecom-equipment-market-growth/](https://blog.tbrc.info/2024/11/telecom-equipment-market-growth/)
96. [https://www.redhat.com/en/blog/new-survey-explores-virtualized-ran-4g-and-5g-strategies-opportunities-and-pitfalls](https://www.redhat.com/en/blog/new-survey-explores-virtualized-ran-4g-and-5g-strategies-opportunities-and-pitfalls)
97. [https://www.researchandmarkets.com/reports/5954584/telecom-equipment-global-market-report?srsltid=AfmBOoqa1A5-gshobsEZ7KkVHSBQxIf65g5RiOup4ye5TOELdXDhVFeT](https://www.researchandmarkets.com/reports/5954584/telecom-equipment-global-market-report?srsltid=AfmBOoqa1A5-gshobsEZ7KkVHSBQxIf65g5RiOup4ye5TOELdXDhVFeT)

To do: 
- [x] Read notes
- [x] Read the links opened yesterday
- [x] Jot down points here - build para
- [ ] Through para in latex
- [ ] Rough sketch in latex

---
- What is mobile core network and its functions? 
	- managing, controlling and authorizing 
- How to manage (Goal-oriented communication) the core access to different network by different applications
- key factors of core network - security + correctness - trustworthiness - anything more? 
- control plane of the core network 
	- control plane signaling function and data plane - packet forwarding 
-  cloud - native core --> computing basis 
	- **Service-Based Architecture**: 5G introduces a service-based architecture where network functions are modularized and can communicate with each other through standardized interfaces[18](https://infohub.delltechnologies.com/p/the-5g-core-network-demystified/)[19](https://www.sharetechnote.com/html/5G/5G_NetworkArchitecture.html)[20](https://embeddedcomputing.com/application/networking-5g/5g-primer-part-3-5g-core-network).
	- **Cloud-Native Design**: Modern core networks are designed as cloud-native, software-based systems that can be deployed flexibly across different cloud infrastructure
	- Cloud-based technologies are revolutionizing the entire satellite communications ecosystem. Satellite gateway providers are increasingly adopting cloud-native platforms that allow for more efficient data processing and management. Cloud gateways offer scalable solutions that can be rapidly deployed and managed remotely, allowing for quicker response times and more efficient resource allocation.
	- Edge computing, which involves processing data closer to its source rather than sending it to a centralized data center, is also playing a significant role in improving satellite hub efficiency. By using edge computing, satellite gateways can reduce latency and bandwidth usage, delivering real-time data processing for critical applications like autonomous vehicles, remote healthcare, and disaster recovery.

- An exemplary use case of satellites in 5G is backhauling of cell traffic to connect the
MNO core network with the edges. In current terrestrial deployments, this backhaul is based on fiber connections or microwave links. Thus, the control plane in Release 15 relies
on continuous backhaul connections between the network components. However, a next generation Node B backhauled via satellite has to handle longer signal delays as opposed to short terrestrial connections over fiber. If the gNB itself is mobile, link
outages of varying duration need to be considered for the satellite backhaul link.
- As the traditional borders of network and service layers are vanishing, cross-layer experimental platforms are necessary and allow testing and validation of innovative ideas,
rapid prototyping, and they generally support migration activities. Running testbeds helps finding compatibility issues, bottlenecks and protocol inconsistencies between the different 5G and satellite components. As part of the Satellite and Terrestrial Network for 5G (SaT5G) project, satellite-based backhaul and traffic offloading solutions
- Geographic redundancy is a critical strategy for ensuring the continuous availability of satellite communication systems, especially for mission-critical applications.
-

## Cloud-Native Mobile Core and 5G Implementation Gaps

**Cloud-native mobile core** represents a transformative approach to deploying 5G network functions using containerized, microservices-based architecture built on cloud platforms. This architecture **fully embraces cloud methodologies** and enables **dynamic, scalable, and agile network operations** that can adapt to changing demands in real-time[1](https://builders.intel.com/docs/networkbuilders/cloud-native-5g-core-1646249614.pdf)[2](https://www.samsung.com/global/business/networks/products/core/cloud-core/). The 5G core system has been designed from the ground up to leverage cloud-native principles, incorporating **Service-Based Architecture (SBA)** where network functions are decomposed into smaller, independently deployable microservices[2](https://www.samsung.com/global/business/networks/products/core/cloud-core/)[3](https://www.eurecom.fr/publication/6417/download/comsys-publi-6417.pdf).

The **key benefits** of cloud-native mobile core include **enhanced scalability and flexibility**, enabling operators to quickly scale network resources up or down based on demand[4](https://wraycastle.com/blogs/glossary/how-does-a-cloud-native-architecture-improve-5g). This architecture provides **significant operational efficiency improvements** through automated deployment, management, and healing capabilities, while **reducing total cost of ownership** by utilizing commodity hardware and cloud infrastructure[5](https://www.amantyatech.com/what-is-cloud-native-core-why-should-you-move-to-a-cloud-native-5g-network)[6](https://networkblog.global.fujitsu.com/2023/05/18/beyond-the-hype-sustainable-5g-cloud-native-architecture-and-co-creation/). **Containerization** allows network functions to consume **up to 40% fewer resources** compared to traditional virtual machine-based deployments[7](https://www.f5.com/c/landing/service-providers/5g-makes-a-cloud-native-application-architecture-vital), while **microservices enable rapid development cycles** and independent scaling of individual network components[8](https://www.linkedin.com/pulse/cloud-native-technologies-5g-new-paradigm-network-tayroni-o7mje)[9](https://www.spirent.com/blogs/5g-standalone-and-the-cloud-native-telco-are-taking-off).

However, **significant gaps remain** in achieving full cloud-native implementation of 5G networks. The **primary challenges include infrastructure complexity**, as 5G requires **extensive new infrastructure investments** including small cells, fiber-optic connectivity, and edge computing capabilities[10](https://www.paaet.edu.kw/media/yd0pshpx/challenges-in-the-implementation-of-5g-networks.pdf)[11](https://www.luxcarta.com/blog/5g-network-deployment). **Spectrum availability and management** pose ongoing challenges, with operators struggling to secure sufficient spectrum across different frequency bands while managing **interference and coverage limitations**, particularly with mmWave frequencies[12](https://wds-sicap.com/news-events/hidden-5g-challenges)[10](https://www.paaet.edu.kw/media/yd0pshpx/challenges-in-the-implementation-of-5g-networks.pdf)[13](https://www.rantcell.com/5G-network-deployment-challenges.html).

**Technical implementation gaps** are particularly prominent in **latency management**, where achieving promised **ultra-low latency requirements** remains challenging due to **fiber distance dependencies** and **packet processing delays**[14](https://ceur-ws.org/Vol-2803/paper7.pdf). **Network slicing implementation** faces complexities in maintaining **isolation between virtual network slices** while ensuring **optimal resource allocation** across different service types[12](https://wds-sicap.com/news-events/hidden-5g-challenges)[15](https://www.tataelxsi.com/insights/challenges-and-mitigation-strategies-for-running-5g-on-public-cloud). **Security concerns** have intensified with cloud-native deployments, as **increased connectivity surfaces** create more **potential attack vectors** requiring **robust security frameworks** and **continuous monitoring**[15](https://www.tataelxsi.com/insights/challenges-and-mitigation-strategies-for-running-5g-on-public-cloud)[16](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Informationen-und-Empfehlungen/5-G/Absicherung-5G-Campusnetze/Eigenschaften-5G/Eigenschaften-5G_node.html).

**Operational challenges** include **integration with legacy systems**, where **protocol translation and data migration** between traditional infrastructure and cloud-native environments remain complex[15](https://www.tataelxsi.com/insights/challenges-and-mitigation-strategies-for-running-5g-on-public-cloud). **Vendor lock-in risks** and **interoperability concerns** across different cloud platforms create **strategic challenges** for operators seeking **flexible, multi-vendor solutions**[15](https://www.tataelxsi.com/insights/challenges-and-mitigation-strategies-for-running-5g-on-public-cloud)[17](https://www.thefastmode.com/expert-opinion/35645-cloud-native-development-considerations-perspective-from-a-5g-core-architect). Additionally, **skilled workforce shortages** in cloud-native technologies and **continuous upgrade requirements** to keep pace with **rapidly evolving standards** create ongoing **operational gaps**[18](https://telecom.dingli.com/solving-tough-problems-in-5g-ran-set-up-and-deployment/)[19](https://www.redhat.com/en/blog/service-upgrades-telco-5g-cloud-native-core-caas-infrastructure-no-service-disruption).

**Cost and deployment barriers** continue to impact cloud-native 5G rollout, with **high infrastructure investment requirements** and **uncertain return on investment** for **many deployment scenarios**[10](https://www.paaet.edu.kw/media/yd0pshpx/challenges-in-the-implementation-of-5g-networks.pdf)[11](https://www.luxcarta.com/blog/5g-network-deployment)[20](https://www.gihub.org/articles/5g-networks-bridging-the-infrastructure-gap/). **Regulatory compliance** and **data sovereignty requirements** add complexity to **public cloud deployments**, while **performance optimization** across **diverse deployment environments** remains challenging[15](https://www.tataelxsi.com/insights/challenges-and-mitigation-strategies-for-running-5g-on-public-cloud)[17](https://www.thefastmode.com/expert-opinion/35645-cloud-native-development-considerations-perspective-from-a-5g-core-architect).

1. [https://builders.intel.com/docs/networkbuilders/cloud-native-5g-core-1646249614.pdf](https://builders.intel.com/docs/networkbuilders/cloud-native-5g-core-1646249614.pdf)
2. [https://www.samsung.com/global/business/networks/products/core/cloud-core/](https://www.samsung.com/global/business/networks/products/core/cloud-core/)
3. [https://www.eurecom.fr/publication/6417/download/comsys-publi-6417.pdf](https://www.eurecom.fr/publication/6417/download/comsys-publi-6417.pdf)
4. [https://wraycastle.com/blogs/glossary/how-does-a-cloud-native-architecture-improve-5g](https://wraycastle.com/blogs/glossary/how-does-a-cloud-native-architecture-improve-5g)
5. [https://www.amantyatech.com/what-is-cloud-native-core-why-should-you-move-to-a-cloud-native-5g-network](https://www.amantyatech.com/what-is-cloud-native-core-why-should-you-move-to-a-cloud-native-5g-network)
6. [https://networkblog.global.fujitsu.com/2023/05/18/beyond-the-hype-sustainable-5g-cloud-native-architecture-and-co-creation/](https://networkblog.global.fujitsu.com/2023/05/18/beyond-the-hype-sustainable-5g-cloud-native-architecture-and-co-creation/)
7. [https://www.f5.com/c/landing/service-providers/5g-makes-a-cloud-native-application-architecture-vital](https://www.f5.com/c/landing/service-providers/5g-makes-a-cloud-native-application-architecture-vital)
8. [https://www.linkedin.com/pulse/cloud-native-technologies-5g-new-paradigm-network-tayroni-o7mje](https://www.linkedin.com/pulse/cloud-native-technologies-5g-new-paradigm-network-tayroni-o7mje)
9. [https://www.spirent.com/blogs/5g-standalone-and-the-cloud-native-telco-are-taking-off](https://www.spirent.com/blogs/5g-standalone-and-the-cloud-native-telco-are-taking-off)
10. [https://www.paaet.edu.kw/media/yd0pshpx/challenges-in-the-implementation-of-5g-networks.pdf](https://www.paaet.edu.kw/media/yd0pshpx/challenges-in-the-implementation-of-5g-networks.pdf)
11. [https://www.luxcarta.com/blog/5g-network-deployment](https://www.luxcarta.com/blog/5g-network-deployment)
12. [https://wds-sicap.com/news-events/hidden-5g-challenges](https://wds-sicap.com/news-events/hidden-5g-challenges)
13. [https://www.rantcell.com/5G-network-deployment-challenges.html](https://www.rantcell.com/5G-network-deployment-challenges.html)
14. [https://ceur-ws.org/Vol-2803/paper7.pdf](https://ceur-ws.org/Vol-2803/paper7.pdf)
15. [https://www.tataelxsi.com/insights/challenges-and-mitigation-strategies-for-running-5g-on-public-cloud](https://www.tataelxsi.com/insights/challenges-and-mitigation-strategies-for-running-5g-on-public-cloud)
16. [https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Informationen-und-Empfehlungen/5-G/Absicherung-5G-Campusnetze/Eigenschaften-5G/Eigenschaften-5G_node.html](https://www.bsi.bund.de/EN/Themen/Unternehmen-und-Organisationen/Informationen-und-Empfehlungen/5-G/Absicherung-5G-Campusnetze/Eigenschaften-5G/Eigenschaften-5G_node.html)
17. [https://www.thefastmode.com/expert-opinion/35645-cloud-native-development-considerations-perspective-from-a-5g-core-architect](https://www.thefastmode.com/expert-opinion/35645-cloud-native-development-considerations-perspective-from-a-5g-core-architect)
18. [https://telecom.dingli.com/solving-tough-problems-in-5g-ran-set-up-and-deployment/](https://telecom.dingli.com/solving-tough-problems-in-5g-ran-set-up-and-deployment/)
19. [https://www.redhat.com/en/blog/service-upgrades-telco-5g-cloud-native-core-caas-infrastructure-no-service-disruption](https://www.redhat.com/en/blog/service-upgrades-telco-5g-cloud-native-core-caas-infrastructure-no-service-disruption)
20. [https://www.gihub.org/articles/5g-networks-bridging-the-infrastructure-gap/](https://www.gihub.org/articles/5g-networks-bridging-the-infrastructure-gap/)
21. [https://cis.temple.edu/~wu/research/publications/Publication_files/Cloud-Native%20A%20Platform%20to%20Support%20Containerized%205G%20Core%20Networks%202.pdf](https://cis.temple.edu/~wu/research/publications/Publication_files/Cloud-Native%20A%20Platform%20to%20Support%20Containerized%205G%20Core%20Networks%202.pdf)
22. [https://www.telefonica.de/news/press-releases-telefonica-germany/2024/05/first-5g-core-network-in-the-cloud-for-an-existing-operator-o2-telefonica-sets-new-impulses-in-the-core-network-together-with-nokia-and-aws.html](https://www.telefonica.de/news/press-releases-telefonica-germany/2024/05/first-5g-core-network-in-the-cloud-for-an-existing-operator-o2-telefonica-sets-new-impulses-in-the-core-network-together-with-nokia-and-aws.html)
23. [https://www.ericsson.com/en/cloud-native](https://www.ericsson.com/en/cloud-native)
24. [https://www.f5.com/pdf/solution-overview/deploying-cloud-native-infra-and-5g-core-overview.pdf](https://www.f5.com/pdf/solution-overview/deploying-cloud-native-infra-and-5g-core-overview.pdf)
25. [https://cordis.europa.eu/article/id/119300-moving-mobile-communication-onto-the-cloud](https://cordis.europa.eu/article/id/119300-moving-mobile-communication-onto-the-cloud)
26. [https://www.ericsson.com/en/blog/2020/10/guide-to-building-cloudnative-infrastructure](https://www.ericsson.com/en/blog/2020/10/guide-to-building-cloudnative-infrastructure)
27. [https://publica.fraunhofer.de/entities/publication/262f8f9a-3466-4ef0-ac9d-f6846f10f6d2](https://publica.fraunhofer.de/entities/publication/262f8f9a-3466-4ef0-ac9d-f6846f10f6d2)
28. [https://www.nec.com/en/global/solutions/5g/4G-5G-Converged-Core.html](https://www.nec.com/en/global/solutions/5g/4G-5G-Converged-Core.html)
29. [https://www.5gamericas.org/wp-content/uploads/2019/12/5G-Americas_5G-and-the-Cloud..pdf](https://www.5gamericas.org/wp-content/uploads/2019/12/5G-Americas_5G-and-the-Cloud..pdf)
30. [https://www.agrandtech.com/solutions/cloud-core](https://www.agrandtech.com/solutions/cloud-core)
31. [https://www.pure.ed.ac.uk/ws/portalfiles/portal/480261600/TakanoEtalMobiCom2024OnThePublicCloud.pdf](https://www.pure.ed.ac.uk/ws/portalfiles/portal/480261600/TakanoEtalMobiCom2024OnThePublicCloud.pdf)
32. [https://www.f5.com/de_de/resources/articles/5g-makes-a-cloud-native-application-architecture-vital](https://www.f5.com/de_de/resources/articles/5g-makes-a-cloud-native-application-architecture-vital)
33. [https://www.eurecom.fr/publication/4983/download/comsys-publi-4983.pdf](https://www.eurecom.fr/publication/4983/download/comsys-publi-4983.pdf)
34. [https://images.samsung.com/is/content/samsung/p5/global/business/networks/insights/white-paper/cloud-native-5g-core/Cloud-Native-5G-Core-Samsung-5G-Core-Volume-2.pdf](https://images.samsung.com/is/content/samsung/p5/global/business/networks/insights/white-paper/cloud-native-5g-core/Cloud-Native-5G-Core-Samsung-5G-Core-Volume-2.pdf)
35. [https://www.mpirical.com/blog/5g-cloud-native](https://www.mpirical.com/blog/5g-cloud-native)
36. [https://www-file.huawei.com/-/media/corp2020/pdf/giv/striding-towards-the-intelligent-world/the_intelligent_world_cloud_core_network_2023_en.pdf](https://www-file.huawei.com/-/media/corp2020/pdf/giv/striding-towards-the-intelligent-world/the_intelligent_world_cloud_core_network_2023_en.pdf)
37. [https://www.analysysmason.com/research/content/perspectives/vmware-index-whitepaper-rma16/](https://www.analysysmason.com/research/content/perspectives/vmware-index-whitepaper-rma16/)
38. [https://www.iplook.com/info/what-is-a-cloud-native-5g-network-i00085i1.html](https://www.iplook.com/info/what-is-a-cloud-native-5g-network-i00085i1.html)
39. [https://www.iplook.com/info/common-challenges-in-5g-network-rollouts-and-how-to-solve-them-i00456i1.html](https://www.iplook.com/info/common-challenges-in-5g-network-rollouts-and-how-to-solve-them-i00456i1.html)
40. [https://decisiontele.com/news/perspectives-and-barriers-5g-implementation-and-its-impact-small-and-medium-businesses.html](https://decisiontele.com/news/perspectives-and-barriers-5g-implementation-and-its-impact-small-and-medium-businesses.html)
41. [https://www.spirent.com/assets/webinar-navigating-the-5g-cloud-native-transition-key-opportunities-challenges-and-strategies](https://www.spirent.com/assets/webinar-navigating-the-5g-cloud-native-transition-key-opportunities-challenges-and-strategies)
42. [https://wraycastle.com/blogs/glossary/5g-standalone-deployment-challenges-and-solutions](https://wraycastle.com/blogs/glossary/5g-standalone-deployment-challenges-and-solutions)
43. [https://techlteworld.com/why-6g-and-gaps-in-5g/](https://techlteworld.com/why-6g-and-gaps-in-5g/)
44. [https://www.linkedin.com/pulse/5g-network-implementation-challenges-mohamed-ashif-dlofc](https://www.linkedin.com/pulse/5g-network-implementation-challenges-mohamed-ashif-dlofc)
45. [https://www.ericsson.com/en/blog/2023/11/top-3-challenges-in-cloudifying-5g-ran](https://www.ericsson.com/en/blog/2023/11/top-3-challenges-in-cloudifying-5g-ran)
46. [https://www.tactis.fr/5g-a-technological-gap/?lang=en](https://www.tactis.fr/5g-a-technological-gap/?lang=en)
47. [https://onlinelibrary.wiley.com/doi/10.1155/2023/9586126](https://onlinelibrary.wiley.com/doi/10.1155/2023/9586126)
48. [https://www.tencentcloud.com/techpedia/100419](https://www.tencentcloud.com/techpedia/100419)
49. [https://www.meegle.com/en_us/topics/containerization/containerization-in-5g-networks](https://www.meegle.com/en_us/topics/containerization/containerization-in-5g-networks)
50. [https://www.slideshare.net/slideshow/5g-microservices/123222855](https://www.slideshare.net/slideshow/5g-microservices/123222855)
51. [https://www.intel.com/content/dam/www/public/us/en/documents/white-papers/containers-and-cloud-native-functions-white-paper.pdf](https://www.intel.com/content/dam/www/public/us/en/documents/white-papers/containers-and-cloud-native-functions-white-paper.pdf)
52. [https://www.telecomreview.com/articles/cloud-and-enterprise-business/7181-3-benefits-of-cloud-native-development-for-service-providers](https://www.telecomreview.com/articles/cloud-and-enterprise-business/7181-3-benefits-of-cloud-native-development-for-service-providers)
53. [https://vmblog.com/archive/2023/04/13/the-case-for-cloud-native-in-5g-world-why-telcos-benefit.aspx](https://vmblog.com/archive/2023/04/13/the-case-for-cloud-native-in-5g-world-why-telcos-benefit.aspx)
54. [https://www.itu.int/pub/S-JNL-VOL4.ISSUE2-2023-A21](https://www.itu.int/pub/S-JNL-VOL4.ISSUE2-2023-A21)
55. [https://www.amdocs.com/insights/analyst-report/unlocking-5gs-full-potential-cloud-native-functions-and-service-based](https://www.amdocs.com/insights/analyst-report/unlocking-5gs-full-potential-cloud-native-functions-and-service-based)

# NTN Core Network with Cloud-Native Architecture and Computing Infrastructure

## Architecture Overview

**Non-Terrestrial Networks (NTN)** represent a paradigm shift in 5G deployment, extending cellular connectivity beyond traditional terrestrial infrastructure through satellites, High Altitude Platform Stations (HAPS), and other airborne platforms[1](https://www.3gpp.org/technologies/ntn-overview)[2](https://www.faststreamtech.com/blog/what-are-non-terrestrial-networks-ntns/). When combined with **cloud-native architecture**, NTN creates a distributed, scalable, and intelligent network infrastructure that leverages advanced computing capabilities across space, edge, and terrestrial domains.

![NTN Cloud-Native Architecture - Hierarchical view of space segment, 5G core microservices, and distributed computing infrastructure](https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/b3c81ba2e5733c6f1d0b3339931b229a/c81df622-6532-4960-ba58-68db48c5d8d7/0b14f8ef.png)

NTN Cloud-Native Architecture - Hierarchical view of space segment, 5G core microservices, and distributed computing infrastructure

## Space Segment Architecture

The NTN space segment consists of multiple satellite constellations operating at different orbital altitudes, each serving specific coverage and latency requirements[1](https://www.3gpp.org/technologies/ntn-overview)[3](https://docs.srsran.com/projects/project/en/latest/tutorials/source/ntn/source/index.html).

## Satellite Types and Characteristics

**Low Earth Orbit (LEO) satellites** operate between 160-2000 kilometers altitude, providing **ultra-low latency of 20-40 milliseconds** and high bandwidth capabilities[1](https://www.3gpp.org/technologies/ntn-overview)[4](https://www.sharetechnote.com/html/NTN/NTN_Architecture.html). These satellites move rapidly relative to Earth, requiring sophisticated handover mechanisms and Doppler compensation but offer the best performance for real-time applications[5](https://www.keysight.com/blogs/en/inds/2023/06/15/bridging-the-divide-non-terrestrial-networks-for-5g-and-global-connectivity)[6](https://electronics360.globalspec.com/article/21991/world-s-first-successful-5g-ntn-trial-via-leo-satellite).

**Medium Earth Orbit (MEO) satellites** positioned at 2000-35,786 kilometers provide a **balanced approach with 40-125 milliseconds latency**[7](https://www.ericsson.com/en/blog/2024/10/ntn-payload-architecture). MEO constellations offer regional coverage with fewer satellites than LEO while maintaining reasonable latency for most 5G applications[1](https://www.3gpp.org/technologies/ntn-overview).

**Geostationary Earth Orbit (GEO) satellites** at 35,786 kilometers altitude deliver **wide coverage areas with 250-280 milliseconds latency**[1](https://www.3gpp.org/technologies/ntn-overview)[3](https://docs.srsran.com/projects/project/en/latest/tutorials/source/ntn/source/index.html). While higher latency limits real-time applications, GEO satellites provide stable, continuous coverage ideal for broadcasting and fixed communications[7](https://www.ericsson.com/en/blog/2024/10/ntn-payload-architecture).

## Payload Architecture Types

NTN systems employ two fundamental payload architectures that determine computing distribution and processing capabilities[8](https://www.cambridgeconsultants.com/wp-content/uploads/2023/11/5Gs-future-is-hybrid-the-non-terrestrial-opportunity-whitepaper.pdf)[9](https://www.mediatek.com/tek-talk-blogs/worlds-first-5g-nr-ntn-connection-over-leo-satellites).

**Transparent payload architecture**, also known as "bent-pipe," operates as a **simple radio relay with no onboard processing**[2](https://www.faststreamtech.com/blog/what-are-non-terrestrial-networks-ntns/)[8](https://www.cambridgeconsultants.com/wp-content/uploads/2023/11/5Gs-future-is-hybrid-the-non-terrestrial-opportunity-whitepaper.pdf). The gNB remains ground-based, with satellites merely frequency-converting and amplifying signals. This approach minimizes satellite complexity and cost but limits flexibility and requires extensive ground infrastructure[9](https://www.mediatek.com/tek-talk-blogs/worlds-first-5g-nr-ntn-connection-over-leo-satellites)[10](https://www.mavenir.com/portfolio/mavair/non-terrestrial-network-ntn/).

**Regenerative payload architecture** incorporates **complete gNB functionality onboard the satellite**, enabling advanced signal processing, demodulation, encoding, and inter-satellite links[8](https://www.cambridgeconsultants.com/wp-content/uploads/2023/11/5Gs-future-is-hybrid-the-non-terrestrial-opportunity-whitepaper.pdf)[9](https://www.mediatek.com/tek-talk-blogs/worlds-first-5g-nr-ntn-connection-over-leo-satellites). This architecture provides greater flexibility, improved coverage, and enables sophisticated network functions but requires more complex and expensive satellite platforms[1](https://www.3gpp.org/technologies/ntn-overview)[8](https://www.cambridgeconsultants.com/wp-content/uploads/2023/11/5Gs-future-is-hybrid-the-non-terrestrial-opportunity-whitepaper.pdf).

## Cloud-Native 5G Core Network

The 5G core network implements a **Service-Based Architecture (SBA)** using cloud-native principles, fundamentally transforming how network functions operate and scale[11](https://www.rohde-schwarz.com/us/solutions/wireless-communications-testing/wireless-standards/5g-nr/non-terrestrial-networks-ntn/non-terrestrial-networks-ntn_256719.html)[12](https://www.eurecom.fr/publication/6900/download/comsys-publi-6900.pdf).

## Service-Based Architecture Components

The cloud-native 5G core decomposes traditional monolithic network functions into **containerized microservices** that communicate via **HTTP/2 RESTful APIs**[12](https://www.eurecom.fr/publication/6900/download/comsys-publi-6900.pdf)[13](https://www.rcrwireless.com/20250115/5g/5g-ntn-architecture). Key network functions include:

**Access and Mobility Management Function (AMF)** handles user equipment registration, authentication, and mobility management across terrestrial and satellite networks[13](https://www.rcrwireless.com/20250115/5g/5g-ntn-architecture). In NTN deployments, AMF requires enhanced positioning capabilities to manage satellite constellation handovers[7](https://www.ericsson.com/en/blog/2024/10/ntn-payload-architecture).

**Session Management Function (SMF)** manages user sessions, data flow control, and Quality of Service (QoS) requirements[14](https://arxiv.org/pdf/2103.09156.pdf). For NTN, SMF must coordinate with satellite gateways and handle dynamic routing as satellites move[1](https://www.3gpp.org/technologies/ntn-overview).

**User Plane Function (UPF)** forwards user data packets and can be distributed across edge locations to minimize latency[14](https://arxiv.org/pdf/2103.09156.pdf). In NTN architectures, UPF deployment at satellite gateways and edge locations is crucial for performance optimization[7](https://www.ericsson.com/en/blog/2024/10/ntn-payload-architecture).

**Network Repository Function (NRF)** provides service discovery and maintains profiles of available network functions, essential for dynamic satellite constellation management[13](https://www.rcrwireless.com/20250115/5g/5g-ntn-architecture)[12](https://www.eurecom.fr/publication/6900/download/comsys-publi-6900.pdf).

## Microservices Deployment Benefits

**Containerization** enables network functions to consume **up to 40% fewer resources** compared to traditional virtual machine deployments15. Each microservice can be **independently scaled, updated, and deployed**, providing operational flexibility crucial for dynamic satellite environments[16](https://eu-assets.contentstack.com/v3/assets/blt23eb5bbc4124baa6/blt585b02356a5c34b8/6787fb9c0628712c6f63e890/NTN_Non-Terrestrial-Network_Whitepaper_5G_Non-Terrestrial_Networks_-_Get_Ready_for_Launch.pdf)[17](https://www.ciscolive.com/c/dam/r/ciscolive/emea/docs/2025/pdf/BRKSPG-1583.pdf).

The **Kubernetes-based orchestration** supports deployment across public, private, and hybrid cloud environments, enabling seamless integration between terrestrial and satellite network segments[18](https://athene-forschung.unibw.de/doc/143530/143530.pdf)[19](https://cdn.rohde-schwarz.com/kr/webinars_33/presentation/Presentation_slide_230223.pdf).

## Computing Infrastructure and Importance

Computing capabilities in NTN cloud-native architectures are distributed across multiple layers, each serving specific performance and operational requirements.

## Edge Computing in NTN

**Multi-Access Edge Computing (MEC)** nodes deployed at satellite gateways and ground stations provide **local processing capabilities that significantly reduce latency**[20](https://www.eetasia.com/the-standards-advancing-non-terrestrial-networks-to-5g-and-beyond/)[21](https://builders.intel.com/docs/networkbuilders/cloud-native-5g-core-1646249614.pdf). By processing data closer to users, edge computing mitigates the inherent propagation delays in satellite communications[22](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture)[23](https://www.huawei.com/en/news/2018/2/huawei-chianmobile-microservice-5g-core).

**Satellite edge computing** places processing capabilities directly onboard satellites, particularly LEO constellations, enabling **real-time analytics and local content delivery**[21](https://builders.intel.com/docs/networkbuilders/cloud-native-5g-core-1646249614.pdf)[24](https://www.ericsson.com/en/cloud-native). This approach provides **proximity to users and reduced backhaul requirements**, essential for ultra-reliable low-latency communications (URLLC) over NTN[22](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture).

## Central Cloud Computing

**Centralized 5G core functions** manage global orchestration, subscriber data management, and network-wide policy enforcement[25](https://techcommunity.microsoft.com/blog/telecommunications-industry-blog/what-is-the-5g-service-based-architecture-sba/3831367)[26](https://www.5gtechnologyworld.com/how-does-a-5g-core-work/). The central cloud provides **unified control plane functionality** while supporting distributed user plane deployments across satellite gateways[19](https://cdn.rohde-schwarz.com/kr/webinars_33/presentation/Presentation_slide_230223.pdf).

**Global optimization algorithms** running in central cloud infrastructure enable **network-wide resource allocation and load balancing** across the entire satellite constellation and terrestrial infrastructure[22](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture)[25](https://techcommunity.microsoft.com/blog/telecommunications-industry-blog/what-is-the-5g-service-based-architecture-sba/3831367).

## Distributed Computing Architecture

**High Altitude Platform Stations (HAPS)** serve as intermediate computing nodes, providing **stable, low-latency communication** between satellite and terrestrial tiers[22](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture). HAPS constellations are ideal for **distributed federated learning systems** that optimize network performance across the entire NTN infrastructure[22](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture).

**Inter-satellite processing coordination** enables satellites to share computational loads and maintain service continuity during handovers[22](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture). This distributed approach provides **fault tolerance and resilience** through redundant processing capabilities[1](https://www.3gpp.org/technologies/ntn-overview)[8](https://www.cambridgeconsultants.com/wp-content/uploads/2023/11/5Gs-future-is-hybrid-the-non-terrestrial-opportunity-whitepaper.pdf).

## Computing Importance in NTN Cloud-Native Architecture

## Latency Optimization

Computing distribution is **critical for achieving 5G latency targets** in satellite networks. While GEO satellites inherently introduce 250+ millisecond propagation delays, **edge computing and onboard processing** can reduce application-level latency by eliminating multiple round trips[27](https://www.ericsson.com/en/core-network/guide)[28](https://www.keysight.com/blogs/en/inds/2020/06/30/understanding-5g-service-based-architecture).

**Federated learning across satellite constellations** enables real-time optimization of beam forming, resource allocation, and handover decisions without requiring constant communication with ground-based controllers[22](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture).

## Bandwidth Efficiency

**Local processing at edge nodes** reduces backhaul traffic by **up to 60%** by filtering, aggregating, and processing data before transmission to terrestrial networks[23](https://www.huawei.com/en/news/2018/2/huawei-chianmobile-microservice-5g-core)[24](https://www.ericsson.com/en/cloud-native). This is particularly important for massive IoT deployments where satellites must handle millions of low-bandwidth sensors[29](https://www.rcrwireless.com/20180405/5g/how-do-microservices-impact-5g)[30](https://www.f5.com/c/landing/de_de/service-providers/5g-makes-a-cloud-native-application-architecture-vital).

**Content caching and delivery** at satellite edge computing nodes enables efficient content distribution without overwhelming limited satellite bandwidth[20](https://www.eetasia.com/the-standards-advancing-non-terrestrial-networks-to-5g-and-beyond/)[21](https://builders.intel.com/docs/networkbuilders/cloud-native-5g-core-1646249614.pdf).

## Real-Time Applications Support

**Distributed computing architecture** enables URLLC services over NTN by processing time-critical applications at the network edge[22](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture)[27](https://www.ericsson.com/en/core-network/guide). Applications such as autonomous vehicles, industrial automation, and emergency services require **sub-10 millisecond application response times** that are only achievable through sophisticated computing distribution31.

## Network Intelligence and Automation

**AI/ML capabilities distributed across the computing infrastructure** enable autonomous network management, predictive maintenance, and dynamic resource optimization[32](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4485374)[22](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture). Machine learning algorithms running on satellite processors can **automatically adjust coverage patterns, power levels, and handover parameters** based on real-time traffic patterns and user demands.

**Zero-touch network operations** become feasible through cloud-native automation, reducing operational costs and improving service reliability across the global NTN infrastructure[26](https://www.5gtechnologyworld.com/how-does-a-5g-core-work/)[19](https://cdn.rohde-schwarz.com/kr/webinars_33/presentation/Presentation_slide_230223.pdf).

The integration of computing infrastructure across edge, central, and distributed locations is fundamental to realizing the full potential of 5G NTN systems, enabling unprecedented global connectivity while maintaining the performance standards expected from 5G networks.

1. [https://www.3gpp.org/technologies/ntn-overview](https://www.3gpp.org/technologies/ntn-overview)
2. [https://www.faststreamtech.com/blog/what-are-non-terrestrial-networks-ntns/](https://www.faststreamtech.com/blog/what-are-non-terrestrial-networks-ntns/)
3. [https://docs.srsran.com/projects/project/en/latest/tutorials/source/ntn/source/index.html](https://docs.srsran.com/projects/project/en/latest/tutorials/source/ntn/source/index.html)
4. [https://www.sharetechnote.com/html/NTN/NTN_Architecture.html](https://www.sharetechnote.com/html/NTN/NTN_Architecture.html)
5. [https://www.keysight.com/blogs/en/inds/2023/06/15/bridging-the-divide-non-terrestrial-networks-for-5g-and-global-connectivity](https://www.keysight.com/blogs/en/inds/2023/06/15/bridging-the-divide-non-terrestrial-networks-for-5g-and-global-connectivity)
6. [https://electronics360.globalspec.com/article/21991/world-s-first-successful-5g-ntn-trial-via-leo-satellite](https://electronics360.globalspec.com/article/21991/world-s-first-successful-5g-ntn-trial-via-leo-satellite)
7. [https://www.ericsson.com/en/blog/2024/10/ntn-payload-architecture](https://www.ericsson.com/en/blog/2024/10/ntn-payload-architecture)
8. [https://www.cambridgeconsultants.com/wp-content/uploads/2023/11/5Gs-future-is-hybrid-the-non-terrestrial-opportunity-whitepaper.pdf](https://www.cambridgeconsultants.com/wp-content/uploads/2023/11/5Gs-future-is-hybrid-the-non-terrestrial-opportunity-whitepaper.pdf)
9. [https://www.mediatek.com/tek-talk-blogs/worlds-first-5g-nr-ntn-connection-over-leo-satellites](https://www.mediatek.com/tek-talk-blogs/worlds-first-5g-nr-ntn-connection-over-leo-satellites)
10. [https://www.mavenir.com/portfolio/mavair/non-terrestrial-network-ntn/](https://www.mavenir.com/portfolio/mavair/non-terrestrial-network-ntn/)
11. [https://www.rohde-schwarz.com/us/solutions/wireless-communications-testing/wireless-standards/5g-nr/non-terrestrial-networks-ntn/non-terrestrial-networks-ntn_256719.html](https://www.rohde-schwarz.com/us/solutions/wireless-communications-testing/wireless-standards/5g-nr/non-terrestrial-networks-ntn/non-terrestrial-networks-ntn_256719.html)
12. [https://www.eurecom.fr/publication/6900/download/comsys-publi-6900.pdf](https://www.eurecom.fr/publication/6900/download/comsys-publi-6900.pdf)
13. [https://www.rcrwireless.com/20250115/5g/5g-ntn-architecture](https://www.rcrwireless.com/20250115/5g/5g-ntn-architecture)
14. [https://arxiv.org/pdf/2103.09156.pdf](https://arxiv.org/pdf/2103.09156.pdf)
15. [https://www.youtube.com/watch?v=luJAKxBolew](https://www.youtube.com/watch?v=luJAKxBolew)
16. [https://eu-assets.contentstack.com/v3/assets/blt23eb5bbc4124baa6/blt585b02356a5c34b8/6787fb9c0628712c6f63e890/NTN_Non-Terrestrial-Network_Whitepaper_5G_Non-Terrestrial_Networks_-_Get_Ready_for_Launch.pdf](https://eu-assets.contentstack.com/v3/assets/blt23eb5bbc4124baa6/blt585b02356a5c34b8/6787fb9c0628712c6f63e890/NTN_Non-Terrestrial-Network_Whitepaper_5G_Non-Terrestrial_Networks_-_Get_Ready_for_Launch.pdf)
17. [https://www.ciscolive.com/c/dam/r/ciscolive/emea/docs/2025/pdf/BRKSPG-1583.pdf](https://www.ciscolive.com/c/dam/r/ciscolive/emea/docs/2025/pdf/BRKSPG-1583.pdf)
18. [https://athene-forschung.unibw.de/doc/143530/143530.pdf](https://athene-forschung.unibw.de/doc/143530/143530.pdf)
19. [https://cdn.rohde-schwarz.com/kr/webinars_33/presentation/Presentation_slide_230223.pdf](https://cdn.rohde-schwarz.com/kr/webinars_33/presentation/Presentation_slide_230223.pdf)
20. [https://www.eetasia.com/the-standards-advancing-non-terrestrial-networks-to-5g-and-beyond/](https://www.eetasia.com/the-standards-advancing-non-terrestrial-networks-to-5g-and-beyond/)
21. [https://builders.intel.com/docs/networkbuilders/cloud-native-5g-core-1646249614.pdf](https://builders.intel.com/docs/networkbuilders/cloud-native-5g-core-1646249614.pdf)
22. [https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture](https://www.rcrwireless.com/20210909/5g/what-is-a-service-based-architecture)
23. [https://www.huawei.com/en/news/2018/2/huawei-chianmobile-microservice-5g-core](https://www.huawei.com/en/news/2018/2/huawei-chianmobile-microservice-5g-core)
24. [https://www.ericsson.com/en/cloud-native](https://www.ericsson.com/en/cloud-native)
25. [https://techcommunity.microsoft.com/blog/telecommunications-industry-blog/what-is-the-5g-service-based-architecture-sba/3831367](https://techcommunity.microsoft.com/blog/telecommunications-industry-blog/what-is-the-5g-service-based-architecture-sba/3831367)
26. [https://www.5gtechnologyworld.com/how-does-a-5g-core-work/](https://www.5gtechnologyworld.com/how-does-a-5g-core-work/)
27. [https://www.ericsson.com/en/core-network/guide](https://www.ericsson.com/en/core-network/guide)
28. [https://www.keysight.com/blogs/en/inds/2020/06/30/understanding-5g-service-based-architecture](https://www.keysight.com/blogs/en/inds/2020/06/30/understanding-5g-service-based-architecture)
29. [https://www.rcrwireless.com/20180405/5g/how-do-microservices-impact-5g](https://www.rcrwireless.com/20180405/5g/how-do-microservices-impact-5g)
30. [https://www.f5.com/c/landing/de_de/service-providers/5g-makes-a-cloud-native-application-architecture-vital](https://www.f5.com/c/landing/de_de/service-providers/5g-makes-a-cloud-native-application-architecture-vital)
31. [https://www.youtube.com/watch?v=-JdcnMgnDqs](https://www.youtube.com/watch?v=-JdcnMgnDqs)
32. [https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4485374](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4485374)
33. [https://www.ericsson.com/en/core-network/5g-core](https://www.ericsson.com/en/core-network/5g-core)
34. [https://documentation.nokia.com/mag-c/25-3/books/cpf/service-based-interfaces.html](https://documentation.nokia.com/mag-c/25-3/books/cpf/service-based-interfaces.html)
35. [https://carrier.huawei.com/en/spotlight/5g-core-network](https://carrier.huawei.com/en/spotlight/5g-core-network)
36. [https://devopedia.org/cloud-native-5g-core](https://devopedia.org/cloud-native-5g-core)
37. [https://devopedia.org/5g-service-based-architecture](https://devopedia.org/5g-service-based-architecture)
38. [https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/Studies/5G/5G_Core_Network.pdf?__blob=publicationFile&v=4](https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/Studies/5G/5G_Core_Network.pdf?__blob=publicationFile&v=4)
39. [https://www.samsung.com/global/business/networks/products/core/cloud-core/](https://www.samsung.com/global/business/networks/products/core/cloud-core/)
40. [https://www.3gpp.org/technologies/5g-system-overview](https://www.3gpp.org/technologies/5g-system-overview)
41. [https://www.etsi.org/technologies/multi-access-edge-computing/mec](https://www.etsi.org/technologies/multi-access-edge-computing/mec)
42. [https://arxiv.org/pdf/2503.07272.pdf](https://arxiv.org/pdf/2503.07272.pdf)
43. [https://www.celticnext.eu/propidea/mec-over-ntn-multimedia-edge-computing-over-ntn-12-09-2022/](https://www.celticnext.eu/propidea/mec-over-ntn-multimedia-edge-computing-over-ntn-12-09-2022/)
44. [https://connectivity.esa.int/projects/edgesat](https://connectivity.esa.int/projects/edgesat)
45. [https://mecon.av.it.pt/PDFs/deliverables/Celtic-Next_MECON_D2.1_Review_on_the_current_state_of_the_next_generation_broadband_technologies.pdf](https://mecon.av.it.pt/PDFs/deliverables/Celtic-Next_MECON_D2.1_Review_on_the_current_state_of_the_next_generation_broadband_technologies.pdf)
46. [https://www.veea.com/platform/mec](https://www.veea.com/platform/mec)
47. [https://www.sciencedirect.com/science/article/pii/S1389128624005577](https://www.sciencedirect.com/science/article/pii/S1389128624005577)
48. [https://stlpartners.com/articles/edge-computing/5g-edge-computing/](https://stlpartners.com/articles/edge-computing/5g-edge-computing/)
49. [https://www.sciencedirect.com/science/article/abs/pii/S1389128623004954](https://www.sciencedirect.com/science/article/abs/pii/S1389128623004954)
50. [https://mediastorage.o-ran.org/ecosystem-resources/O-RAN-2025.04.02.WP.O-RAN_NTN_Deployments-v08.4.pdf](https://mediastorage.o-ran.org/ecosystem-resources/O-RAN-2025.04.02.WP.O-RAN_NTN_Deployments-v08.4.pdf)
51. [https://dl.acm.org/doi/10.1145/3579895.3579920](https://dl.acm.org/doi/10.1145/3579895.3579920)
52. [https://connectivity.esa.int/projects/ngnarch](https://connectivity.esa.int/projects/ngnarch)
53. [https://www.telit.com/blog/why-edge-computing-is-crucial-5g-networks/](https://www.telit.com/blog/why-edge-computing-is-crucial-5g-networks/)
54. [https://www.mdpi.com/1424-8220/23/8/3883](https://www.mdpi.com/1424-8220/23/8/3883)
55. [https://5g-acia.org/whitepapers/industrial-5g-edge-computing-use-cases-architecture-and-deployment/](https://5g-acia.org/whitepapers/industrial-5g-edge-computing-use-cases-architecture-and-deployment/)
56. [https://www.sciencedirect.com/science/article/pii/S2590123025000222](https://www.sciencedirect.com/science/article/pii/S2590123025000222)
57. [https://sateliot.space/2022/09/26/sateliot-works-with-aws-on-innovative-cloud-native-5g-satellite-network-to-connect-iot-devices-directly-to-satellites/](https://sateliot.space/2022/09/26/sateliot-works-with-aws-on-innovative-cloud-native-5g-satellite-network-to-connect-iot-devices-directly-to-satellites/)
58. [https://www.sharetechnote.com/html/5G/5G_NTN.html](https://www.sharetechnote.com/html/5G/5G_NTN.html)
59. [https://iotbusinessnews.com/2022/09/27/94040-sateliot-works-with-aws-on-innovative-cloud-native-5g-satellite-network-to-connect-iot-devices-directly-to-satellites/](https://iotbusinessnews.com/2022/09/27/94040-sateliot-works-with-aws-on-innovative-cloud-native-5g-satellite-network-to-connect-iot-devices-directly-to-satellites/)
60. [https://techlteworld.com/5g-ntn-non-terrestrial-networks-overview/](https://techlteworld.com/5g-ntn-non-terrestrial-networks-overview/)
61. [https://mobile-magazine.com/5g-and-iot/sateliot-and-aws-to-build-cloud-native-5g-satellite-network](https://mobile-magazine.com/5g-and-iot/sateliot-and-aws-to-build-cloud-native-5g-satellite-network)
62. [https://www.5gamericas.org/wp-content/uploads/2022/01/5G-Non-Terrestrial-Networks-2022-WP-Id.pdf](https://www.5gamericas.org/wp-content/uploads/2022/01/5G-Non-Terrestrial-Networks-2022-WP-Id.pdf)
63. [https://www.satelliteevolution.com/post/sateliot-works-with-aws-on-innovative-cloud-5g-network-to-connect-iot-devices-to-satellites](https://www.satelliteevolution.com/post/sateliot-works-with-aws-on-innovative-cloud-5g-network-to-connect-iot-devices-to-satellites)
64. [https://www.5gamericas.org/wp-content/uploads/2025/02/WP_New-Developments-and-Advances-in-5G-and-NTN-.pdf](https://www.5gamericas.org/wp-content/uploads/2025/02/WP_New-Developments-and-Advances-in-5G-and-NTN-.pdf)
65. [https://www.slideshare.net/HsiuChiTsai/the-cloudnative-solution-of-integrate-satellite-ground-station-system-and-telecommunication-network-system-cdd6](https://www.slideshare.net/HsiuChiTsai/the-cloudnative-solution-of-integrate-satellite-ground-station-system-and-telecommunication-network-system-cdd6)
66. [https://hackmd.io/@ArIC4mpkTcq2r238nut53g/SJ25qI9Bo](https://hackmd.io/@ArIC4mpkTcq2r238nut53g/SJ25qI9Bo)
67. [https://www.keysight.com/us/en/cmp/topics/non-terrestrial-network-basics-advantages-and-challenges.html](https://www.keysight.com/us/en/cmp/topics/non-terrestrial-network-basics-advantages-and-challenges.html)
68. [https://www.iplook.com/info/iplook-5gc-deployment-series-3-3-cloud-native-architecture-paving-the-future-of-5g-core-networks-i00493i1.html](https://www.iplook.com/info/iplook-5gc-deployment-series-3-3-cloud-native-architecture-paving-the-future-of-5g-core-networks-i00493i1.html)
## Need for Computing in NTN Architecture and Benefits for Goal-Oriented Communication

**Computing infrastructure is fundamentally critical in NTN architecture** to address the inherent challenges of satellite communications while enabling intelligent, adaptive, and efficient network operations[1](https://pubmed.ncbi.nlm.nih.gov/30781604/)[2](https://pmc.ncbi.nlm.nih.gov/articles/PMC6832566/). The **distributed computing paradigm across edge, onboard, and cloud layers** serves as the backbone for **transforming traditional "bent-pipe" relay satellites into intelligent processing nodes** that can make autonomous decisions, optimize resource allocation, and deliver goal-oriented services[3](https://pubmed.ncbi.nlm.nih.gov/31658684/)[4](https://pmc.ncbi.nlm.nih.gov/articles/PMC10181455/).

**The primary need for computing in NTN stems from the unique constraints and requirements of satellite networks**, including **highly variable propagation delays, limited bandwidth, power constraints, and dynamic orbital mechanics**[5](https://techxplore.com/news/2022-10-edge-wings-low-earth-orbit-satellite.html)[6](https://www.sharetechnote.com/html/NTN/NTN_Requirement.html). **Edge computing deployed at satellite gateways and onboard processing capabilities** enable **local data processing and decision-making** that significantly **reduces latency by eliminating multiple round trips** to terrestrial cloud centers[1](https://pubmed.ncbi.nlm.nih.gov/30781604/)[2](https://pmc.ncbi.nlm.nih.gov/articles/PMC6832566/). This is particularly crucial for **LEO satellite networks where satellites move rapidly** and **require real-time handover coordination and beam management**[5](https://techxplore.com/news/2022-10-edge-wings-low-earth-orbit-satellite.html)[7](https://doaj.org/article/e80e9d01ceef45078c71712adcdeb918).

**For goal-oriented communication, computing infrastructure provides transformative benefits** by enabling **semantic communication and intelligent task offloading** that **prioritize information relevance over raw data transmission**[8](http://arxiv.org/pdf/2409.14534.pdf)[9](https://arxiv.org/html/2408.15639v1)[10](https://arxiv.org/abs/2409.14534). **Onboard AI/ML processing capabilities** allow satellites to **implement goal-oriented sampling and multi-user scheduling** that can **handle highly variable delay processes** and **replace traditional exogenous arrivals with intelligent traffic shaping**[11](https://cordis.europa.eu/project/id/101122990)[10](https://arxiv.org/abs/2409.14534). This approach enables **effective data flow using a fraction of the resources** compared to conventional methods by **transmitting only decision-critical information** rather than complete sensor outputs[9](https://arxiv.org/html/2408.15639v1)[12](https://pimrc2025.ieee-pimrc.org/workshop/ws-13-semantic-communications-intelligent-and-integrated-terrestrial-and-non-terrestrial).

**The computing infrastructure supports autonomous network operations** through **distributed intelligence that optimizes resource allocation, manages constellation-wide coordination, and enables predictive maintenance**[13](https://arxiv.org/html/2305.10273v3)[14](https://www.cambridgeconsultants.com/autonomous-non-terrestrial-networks/). **AI-driven algorithms running on satellite processors** can **automatically adjust coverage patterns, power levels, and handover parameters** based on real-time traffic patterns and user demands, achieving **zero-touch network operations** that reduce operational costs while improving service reliability[15](https://openresearch.lsbu.ac.uk/download/71d811ed7eff722a0f15d5a95a7db76d3a871efb768b948ea9d042f8314f862e/1063139/Main%20File%20IEEE%20Access.pdf)[16](https://pdfs.semanticscholar.org/51d7/86415098fdfe2f1b26d4ec4883b4c10b58e6.pdf). Furthermore, **satellite edge computing enables space-based federated learning** where **multiple satellites collaboratively optimize network performance** without requiring constant communication with ground-based controllers, providing **fault tolerance and resilience** through redundant distributed processing capabilities[17](https://arxiv.org/pdf/2409.19869.pdf)[4](https://pmc.ncbi.nlm.nih.gov/articles/PMC10181455/).

1. [https://pubmed.ncbi.nlm.nih.gov/30781604/](https://pubmed.ncbi.nlm.nih.gov/30781604/)
2. [https://pmc.ncbi.nlm.nih.gov/articles/PMC6832566/](https://pmc.ncbi.nlm.nih.gov/articles/PMC6832566/)
3. [https://pubmed.ncbi.nlm.nih.gov/31658684/](https://pubmed.ncbi.nlm.nih.gov/31658684/)
4. [https://pmc.ncbi.nlm.nih.gov/articles/PMC10181455/](https://pmc.ncbi.nlm.nih.gov/articles/PMC10181455/)
5. [https://techxplore.com/news/2022-10-edge-wings-low-earth-orbit-satellite.html](https://techxplore.com/news/2022-10-edge-wings-low-earth-orbit-satellite.html)
6. [https://www.sharetechnote.com/html/NTN/NTN_Requirement.html](https://www.sharetechnote.com/html/NTN/NTN_Requirement.html)
7. [https://doaj.org/article/e80e9d01ceef45078c71712adcdeb918](https://doaj.org/article/e80e9d01ceef45078c71712adcdeb918)
8. [http://arxiv.org/pdf/2409.14534.pdf](http://arxiv.org/pdf/2409.14534.pdf)
9. [https://arxiv.org/html/2408.15639v1](https://arxiv.org/html/2408.15639v1)
10. [https://arxiv.org/abs/2409.14534](https://arxiv.org/abs/2409.14534)
11. [https://cordis.europa.eu/project/id/101122990](https://cordis.europa.eu/project/id/101122990)
12. [https://pimrc2025.ieee-pimrc.org/workshop/ws-13-semantic-communications-intelligent-and-integrated-terrestrial-and-non-terrestrial](https://pimrc2025.ieee-pimrc.org/workshop/ws-13-semantic-communications-intelligent-and-integrated-terrestrial-and-non-terrestrial)
13. [https://arxiv.org/html/2305.10273v3](https://arxiv.org/html/2305.10273v3)
14. [https://www.cambridgeconsultants.com/autonomous-non-terrestrial-networks/](https://www.cambridgeconsultants.com/autonomous-non-terrestrial-networks/)
15. [https://openresearch.lsbu.ac.uk/download/71d811ed7eff722a0f15d5a95a7db76d3a871efb768b948ea9d042f8314f862e/1063139/Main%20File%20IEEE%20Access.pdf](https://openresearch.lsbu.ac.uk/download/71d811ed7eff722a0f15d5a95a7db76d3a871efb768b948ea9d042f8314f862e/1063139/Main%20File%20IEEE%20Access.pdf)
16. [https://pdfs.semanticscholar.org/51d7/86415098fdfe2f1b26d4ec4883b4c10b58e6.pdf](https://pdfs.semanticscholar.org/51d7/86415098fdfe2f1b26d4ec4883b4c10b58e6.pdf)
17. [https://arxiv.org/pdf/2409.19869.pdf](https://arxiv.org/pdf/2409.19869.pdf)
18. [https://www.3gpp.org/technologies/ntn-overview](https://www.3gpp.org/technologies/ntn-overview)
19. [https://inform.tmforum.org/research-and-analysis/proofs-of-concept/5g-ntn-architecture-brings-us-close-to-ubiquitous-connectivity](https://inform.tmforum.org/research-and-analysis/proofs-of-concept/5g-ntn-architecture-brings-us-close-to-ubiquitous-connectivity)
20. [https://www.rohde-schwarz.com/us/solutions/wireless-communications-testing/wireless-standards/5g-nr/non-terrestrial-networks-ntn/non-terrestrial-networks-ntn_256719.html](https://www.rohde-schwarz.com/us/solutions/wireless-communications-testing/wireless-standards/5g-nr/non-terrestrial-networks-ntn/non-terrestrial-networks-ntn_256719.html)
21. [https://www.eurecom.fr/publication/7315/download/comsys-publi-7315.pdf](https://www.eurecom.fr/publication/7315/download/comsys-publi-7315.pdf)
22. [http://testfyra.com/key-benefits-of-non-terrestrial-networks/](http://testfyra.com/key-benefits-of-non-terrestrial-networks/)
23. [https://www.eurecom.fr/publication/6900/download/comsys-publi-6900.pdf](https://www.eurecom.fr/publication/6900/download/comsys-publi-6900.pdf)
24. [https://www.keysight.com/us/en/cmp/topics/non-terrestrial-network-basics-advantages-and-challenges.html](https://www.keysight.com/us/en/cmp/topics/non-terrestrial-network-basics-advantages-and-challenges.html)
25. [https://www.annales.org/enjeux-numeriques/2024/en-2024-03/2024-03-24.pdf](https://www.annales.org/enjeux-numeriques/2024/en-2024-03/2024-03-24.pdf)
26. [https://www.mavenir.com/blog/why-open-ran-in-ntn-can-be-a-game-changer/](https://www.mavenir.com/blog/why-open-ran-in-ntn-can-be-a-game-changer/)
27. [https://www.p1sec.com/blog/5g-beyond-earth-how-non-terrestrial-networks-ntn-are-reshaping-global-connectivity](https://www.p1sec.com/blog/5g-beyond-earth-how-non-terrestrial-networks-ntn-are-reshaping-global-connectivity)
28. [https://pubs.opengroup.org/onlinepubs/7619899/w801.htm](https://pubs.opengroup.org/onlinepubs/7619899/w801.htm)
29. [https://www.mpirical.com/knowledge-base/5g-ntn-non-terrestrial-networks](https://www.mpirical.com/knowledge-base/5g-ntn-non-terrestrial-networks)
30. [https://arxiv.org/html/2404.15278v1](https://arxiv.org/html/2404.15278v1)
31. [https://doaj.org/article/932825fd96c24b0fbd5963303bfcd849](https://doaj.org/article/932825fd96c24b0fbd5963303bfcd849)
32. [https://www.mdpi.com/1424-8220/25/9/2892](https://www.mdpi.com/1424-8220/25/9/2892)
33. [https://orbilu.uni.lu/bitstream/10993/62192/1/LEO%20Satellite%20assisted%20Task%20Offloading%20for%20a%20Near%20Real%20time%20Earth%20Observation%20Service.pdf](https://orbilu.uni.lu/bitstream/10993/62192/1/LEO%20Satellite%20assisted%20Task%20Offloading%20for%20a%20Near%20Real%20time%20Earth%20Observation%20Service.pdf)
34. [https://www.mdpi.com/2673-4001/5/1/5](https://www.mdpi.com/2673-4001/5/1/5)
35. [https://pmc.ncbi.nlm.nih.gov/articles/PMC12074290/](https://pmc.ncbi.nlm.nih.gov/articles/PMC12074290/)
36. [https://www.h-brs.de/en/inf/study/master/autonomous-systems](https://www.h-brs.de/en/inf/study/master/autonomous-systems)
37. [https://arxiv.org/abs/2102.01876](https://arxiv.org/abs/2102.01876)
38. [https://cordis.europa.eu/project/id/101122990/de](https://cordis.europa.eu/project/id/101122990/de)
39. [https://www.mdpi.com/2078-2489/15/1/38](https://www.mdpi.com/2078-2489/15/1/38)
40. [https://www.sciencedirect.com/science/article/pii/S2352864825001154](https://www.sciencedirect.com/science/article/pii/S2352864825001154)
41. [https://www.proquest.com/docview/2785205623](https://www.proquest.com/docview/2785205623)
42. [https://www.youtube.com/watch?v=Mgq2-Sv1N0E](https://www.youtube.com/watch?v=Mgq2-Sv1N0E)
43. [https://researchoutput.ncku.edu.tw/en/publications/semantic-communication-empowered-ntn-for-iot-benefits-and-challen](https://researchoutput.ncku.edu.tw/en/publications/semantic-communication-empowered-ntn-for-iot-benefits-and-challen)
44. [https://www.calian.com/products/resource-management/](https://www.calian.com/products/resource-management/)
45. [https://elib.dlr.de/188152/1/navi.531.full.pdf](https://elib.dlr.de/188152/1/navi.531.full.pdf)
46. [https://vbn.aau.dk/files/784710893/Accepted_Author_Manuscript.pdf](https://vbn.aau.dk/files/784710893/Accepted_Author_Manuscript.pdf)
47. [https://www.magister.fi/blog-satcom-capacity-according-to-demand-flexible-resource-management-via-c-dream/](https://www.magister.fi/blog-satcom-capacity-according-to-demand-flexible-resource-management-via-c-dream/)
48. [https://digital-library.theiet.org/content/books/10.1049/pbte079e_ch13](https://digital-library.theiet.org/content/books/10.1049/pbte079e_ch13)
49. [https://arxiv.org/html/2409.14726v1](https://arxiv.org/html/2409.14726v1)
50. [https://orbilu.uni.lu/bitstream/10993/62188/1/User-Centric_Flexible_Resource_Management_Framework_for_LEO_Satellites_With_Fully_Regenerative_Payload.pdf](https://orbilu.uni.lu/bitstream/10993/62188/1/User-Centric_Flexible_Resource_Management_Framework_for_LEO_Satellites_With_Fully_Regenerative_Payload.pdf)
51. [https://www.taylorfrancis.com/chapters/edit/10.1201/9781032644752-40/onboard-compression-preprocessing-methods-leo-satellite-imagery-review-abhishek-sharma-nidhi-singh-yashvardhan-srivastava-shubhi-sharma-krishna-pratap-singh-harsh-jaiswal-praveen-kumar-parvin-kumar](https://www.taylorfrancis.com/chapters/edit/10.1201/9781032644752-40/onboard-compression-preprocessing-methods-leo-satellite-imagery-review-abhishek-sharma-nidhi-singh-yashvardhan-srivastava-shubhi-sharma-krishna-pratap-singh-harsh-jaiswal-praveen-kumar-parvin-kumar)
52. [https://oulurepo.oulu.fi/bitstream/handle/10024/46000/nbnfi-fe20230913124405.pdf?sequence=1](https://oulurepo.oulu.fi/bitstream/handle/10024/46000/nbnfi-fe20230913124405.pdf?sequence=1)
53. [https://arxiv.org/pdf/2312.11127.pdf](https://arxiv.org/pdf/2312.11127.pdf)
54. [https://arxiv.org/html/2410.07586v1](https://arxiv.org/html/2410.07586v1)
55. [https://arxiv.org/html/2505.01796](https://arxiv.org/html/2505.01796)
56. [https://dl.acm.org/doi/abs/10.1109/MWC.001.1900238](https://dl.acm.org/doi/abs/10.1109/MWC.001.1900238)
57. [https://www.lockheedmartin.com/content/dam/lockheed-martin/space/documents/ai-ml/PIRA-aiaa-6.2022-1472-aiml-mission-processing-onboard-satellites-paper.pdf](https://www.lockheedmartin.com/content/dam/lockheed-martin/space/documents/ai-ml/PIRA-aiaa-6.2022-1472-aiml-mission-processing-onboard-satellites-paper.pdf)
58. [https://arxiv.org/pdf/2409.14726.pdf](https://arxiv.org/pdf/2409.14726.pdf)
59. [https://www.sciencedirect.com/science/article/pii/S2772671124000998](https://www.sciencedirect.com/science/article/pii/S2772671124000998)


# Challenges of Microservices Service-Based Architecture (SBA) Core

The microservices-based Service-Based Architecture (SBA) of the 5G core introduces modularity and agility but shifts complexity into a distributed, API-driven ecosystem. Key challenges include:

## 1. Functional Granularity and Service Decomposition

Determining the “right” size for each microservice is an art. Overly fine-grained services inflate the number of network functions (NFs), increasing inter-service dependencies and management overhead. Coarse granularity, however, undermines the benefits of independent scaling and rapid deployment[1](https://www.ce.cit.tum.de/fileadmin/w00cgn/cm/mir-2018/2018-flinck-talk.pdf).

## 2. Inter-Service Communication Overhead

Every control-plane procedure involves multiple NF interactions over HTTP/2 and RESTful APIs. This high messaging volume leads to signaling storms, elevates control-plane latency, and risks breaching SLAs—especially under massive device registration or network-slice operations[2](https://www.paloaltonetworks.com/blog/cloud-security/seo-5g-sba-vulnerability/)[3](https://cdrdv2-public.intel.com/815078/Cloud-Native_Service_Mesh_Readiness_for_5G_and_Beyond.pdf).

## 3. Service Discovery and Load Balancing

SBA relies on the Network Repository Function (NRF) for NF registration and discovery. Centralized NRF lookups can become a bottleneck at scale, while indirect communication via Service Communication Proxy (SCP) adds another layer that must itself be highly available and secure[4](https://devopedia.org/5g-service-based-architecture)[5](https://www.ericsson.com/en/blog/2024/2/5g-sba-security-release-16-updates).

## 4. Resiliency and Fault Tolerance

Distributed microservices require robust mechanisms for failure detection, retries, and circuit breaking. Without a mature service-mesh or sidecar infrastructure, achieving end-to-end resilience and preserving real-time performance is challenging[3](https://cdrdv2-public.intel.com/815078/Cloud-Native_Service_Mesh_Readiness_for_5G_and_Beyond.pdf).

## 5. Performance and Latency Constraints

Container sidecars and service-mesh proxies introduce additional network hops and processing delays. Kubernetes lacks native telecom-grade features (e.g., ECMP, GTP tunneling), making it nontrivial to meet sub-millisecond control-plane requirements without specialized extensions[1](https://www.ce.cit.tum.de/fileadmin/w00cgn/cm/mir-2018/2018-flinck-talk.pdf)[3](https://cdrdv2-public.intel.com/815078/Cloud-Native_Service_Mesh_Readiness_for_5G_and_Beyond.pdf).

## 6. Security and Trust Management

Replacing ASN.1 with JSON over TLS introduces new vulnerabilities. Implementing OAuth 2.0 for NF-to-NF authorization, managing certificates at scale, and enforcing zero-trust across disparate trust domains demand a comprehensive PKI and continuous compliance monitoring[6](https://www.lfdecentralizedtrust.org/blog/oauth-2.0-authorization-in-5g-core-networks-architecture-workflows-and-security-challenges)[7](https://mediatum.ub.tum.de/doc/1740121/fn735514lbzqz0lm6blll7gxe.TLS_Performance_Evaluation_in_the_5G_Core.pdf).

## 7. Observability and Monitoring

Traditional OAM tools cannot penetrate ephemeral containers or sidecar proxies. Ensuring full-stack observability—tracing, metrics, and logging—across hundreds of distributed microservices requires integrated telemetry, standardized schemas, and minimal performance impact[3](https://cdrdv2-public.intel.com/815078/Cloud-Native_Service_Mesh_Readiness_for_5G_and_Beyond.pdf).

## 8. Vendor Interoperability and Multi-Domain Integration

Different vendors implement CNFs with varied frameworks and IDL interpretations. Guaranteeing seamless interoperability between 4G EPC and 5G SBA, as well as across private, public, and hybrid clouds, demands rigorous conformance testing and open-API governance[3](https://cdrdv2-public.intel.com/815078/Cloud-Native_Service_Mesh_Readiness_for_5G_and_Beyond.pdf).

## 9. Orchestration Complexity

Coordinating NF placement, auto-scaling policies, and service-mesh configurations across edge, core, and central clouds strains Kubernetes and MANO platforms. Stateful data layers (UDR, UDM) further complicate rolling upgrades and dynamic scaling[3](https://cdrdv2-public.intel.com/815078/Cloud-Native_Service_Mesh_Readiness_for_5G_and_Beyond.pdf).

## 10. Legacy System Integration

Integrating monolithic OSS/BSS and legacy IMS functions with cloud-native SBA involves protocol translation, data migration, and unified orchestration—challenges that can erode agility gains unless addressed through phased refactoring and clear interface contracts[8](https://www.tencentcloud.com/techpedia/116547).

Despite these hurdles, targeted enhancements—such as optimized service-mesh frameworks, per-procedure NF consolidation, and telecom-tailored orchestration extensions—can mitigate overhead, bolster security, and fulfill 5G SBA’s promise of agile, scalable, and resilient core networks.

1. [https://www.ce.cit.tum.de/fileadmin/w00cgn/cm/mir-2018/2018-flinck-talk.pdf](https://www.ce.cit.tum.de/fileadmin/w00cgn/cm/mir-2018/2018-flinck-talk.pdf)
2. [https://www.paloaltonetworks.com/blog/cloud-security/seo-5g-sba-vulnerability/](https://www.paloaltonetworks.com/blog/cloud-security/seo-5g-sba-vulnerability/)
3. [https://cdrdv2-public.intel.com/815078/Cloud-Native_Service_Mesh_Readiness_for_5G_and_Beyond.pdf](https://cdrdv2-public.intel.com/815078/Cloud-Native_Service_Mesh_Readiness_for_5G_and_Beyond.pdf)
4. [https://devopedia.org/5g-service-based-architecture](https://devopedia.org/5g-service-based-architecture)
5. [https://www.ericsson.com/en/blog/2024/2/5g-sba-security-release-16-updates](https://www.ericsson.com/en/blog/2024/2/5g-sba-security-release-16-updates)
6. [https://www.lfdecentralizedtrust.org/blog/oauth-2.0-authorization-in-5g-core-networks-architecture-workflows-and-security-challenges](https://www.lfdecentralizedtrust.org/blog/oauth-2.0-authorization-in-5g-core-networks-architecture-workflows-and-security-challenges)
7. [https://mediatum.ub.tum.de/doc/1740121/fn735514lbzqz0lm6blll7gxe.TLS_Performance_Evaluation_in_the_5G_Core.pdf](https://mediatum.ub.tum.de/doc/1740121/fn735514lbzqz0lm6blll7gxe.TLS_Performance_Evaluation_in_the_5G_Core.pdf)
8. [https://www.tencentcloud.com/techpedia/116547](https://www.tencentcloud.com/techpedia/116547)
9. [https://www.outsystems.com/blog/posts/cloud-native-challenges/](https://www.outsystems.com/blog/posts/cloud-native-challenges/)
10. [https://metavshn.com/exploring-scalability-challenges-in-telecom-bss-architectures/](https://metavshn.com/exploring-scalability-challenges-in-telecom-bss-architectures/)
11. [https://www.numberanalytics.com/blog/microservices-for-5g-and-beyond](https://www.numberanalytics.com/blog/microservices-for-5g-and-beyond)
12. [https://www.motadata.com/blog/cloud-native-infrastructure/](https://www.motadata.com/blog/cloud-native-infrastructure/)
13. [https://www.ibis-solutions.rs/en/insights/challenges-in-transforming-telecommunication-network-and-software-architecture/](https://www.ibis-solutions.rs/en/insights/challenges-in-transforming-telecommunication-network-and-software-architecture/)
14. [https://mediastorage.o-ran.org/ngrg-rr/nGRG-RR-2024-11-Research%20Report%20on%20Service-based%20RAN%20for%206G%20network.pdf](https://mediastorage.o-ran.org/ngrg-rr/nGRG-RR-2024-11-Research%20Report%20on%20Service-based%20RAN%20for%206G%20network.pdf)
15. [https://www.sciencedirect.com/science/article/abs/pii/S1389128623005030](https://www.sciencedirect.com/science/article/abs/pii/S1389128623005030)
16. [https://newrelic.com/blog/best-practices/cloud-native-infrastructure-struggles](https://newrelic.com/blog/best-practices/cloud-native-infrastructure-struggles)
17. [https://publica.fraunhofer.de/entities/publication/e2f1b4b3-cd16-4f63-a372-32dece78c83e](https://publica.fraunhofer.de/entities/publication/e2f1b4b3-cd16-4f63-a372-32dece78c83e)
18. [https://middleware.io/blog/cloud-native-infrastructure-challenges/](https://middleware.io/blog/cloud-native-infrastructure-challenges/)
19. [https://www.iplook.com/info/the-opportunities-and-challenges-of-5gc-i00078i1.html](https://www.iplook.com/info/the-opportunities-and-challenges-of-5gc-i00078i1.html)
20. [https://www.cncf.io/blog/2020/09/15/top-7-challenges-to-becoming-cloud-native/](https://www.cncf.io/blog/2020/09/15/top-7-challenges-to-becoming-cloud-native/)
21. [https://www.cloudfabrix.com/marketing/docs/telco-service-assurance-solution-brief-1-0-telecom-talk.pdf](https://www.cloudfabrix.com/marketing/docs/telco-service-assurance-solution-brief-1-0-telecom-talk.pdf)
22. [https://www.datavsn.com/from-legacy-to-cloud-native-challenges-in-core-system-migration/](https://www.datavsn.com/from-legacy-to-cloud-native-challenges-in-core-system-migration/)
23. [https://www.telecomgurukul.com/post/master-service-based-architecture-sba-in-5g-core-with-the-best-trainer](https://www.telecomgurukul.com/post/master-service-based-architecture-sba-in-5g-core-with-the-best-trainer)
24. [https://www.cncf.io/blog/2025/04/14/five-critical-shifts-for-cloud-native-at-a-crossroads/](https://www.cncf.io/blog/2025/04/14/five-critical-shifts-for-cloud-native-at-a-crossroads/)
25. [https://www.vamsitalkstech.com/5g/how-service-meshes-can-enable-5g-architecture/](https://www.vamsitalkstech.com/5g/how-service-meshes-can-enable-5g-architecture/)
26. [https://www.linkedin.com/pulse/service-based-architecture-sba-5g-expand-6g-extend-ran-kumar--c6c6c](https://www.linkedin.com/pulse/service-based-architecture-sba-5g-expand-6g-extend-ran-kumar--c6c6c)
27. [https://mediatum.ub.tum.de/doc/1695118/9z0h8svu330r8up1ejyajrw2s.tnsm-pp5g.pdf](https://mediatum.ub.tum.de/doc/1695118/9z0h8svu330r8up1ejyajrw2s.tnsm-pp5g.pdf)
28. [https://www.linkedin.com/pulse/service-communication-proxy-5g-caught-up-mesh-simon-dredge](https://www.linkedin.com/pulse/service-communication-proxy-5g-caught-up-mesh-simon-dredge)
29. [https://arxiv.org/pdf/2309.14659.pdf](https://arxiv.org/pdf/2309.14659.pdf)
30. [https://core.ac.uk/download/pdf/280342568.pdf](https://core.ac.uk/download/pdf/280342568.pdf)
31. [https://techcommunity.microsoft.com/blog/telecommunications-industry-blog/what-is-the-5g-service-based-architecture-sba/3831367](https://techcommunity.microsoft.com/blog/telecommunications-industry-blog/what-is-the-5g-service-based-architecture-sba/3831367)
32. [https://www.tigera.io/learn/guides/service-mesh/](https://www.tigera.io/learn/guides/service-mesh/)

---
https://www.paloaltonetworks.com/blog/cloud-security/seo-5g-sba-vulnerability/

---
![[Pasted image 20250712175746.png]]

# 6G IMT-2030, NTN, and Quantum Computing: Technology Comparison

## Overview

The convergence of **6G IMT-2030**, **Non-Terrestrial Networks (NTN)**, and **Quantum Computing** represents a revolutionary transformation in wireless communications and networking technologies. Each technology brings unique capabilities and characteristics that will define the future of connectivity and computing.

![Comprehensive Spider Web Chart: 6G IMT-2030, NTN, and Quantum Computing Technology Comparison](https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/240c4039dd9aa052922d28ca974f7b49/8ca1033f-fc33-44d5-ac07-7f774765648f/196eb785.png)

Comprehensive Spider Web Chart: 6G IMT-2030, NTN, and Quantum Computing Technology Comparison

## 6G IMT-2030 Characteristics

**6G IMT-2030** represents the next generation of mobile communication standards, building upon 5G capabilities while introducing revolutionary enhancements[1](https://unidir.org/wp-content/uploads/2024/12/241211_ITU-R-Update-on-WRC-and-IMT-2030.pdf)[2](https://www.ngmn.org/wp-content/uploads/ITU-R_FRAMEWORK_FOR_IMT-2030.pdf). The ITU-R Framework Recommendation M.2160 identifies **15 key capabilities** for 6G technology, with targets that significantly exceed current 5G performance[2](https://www.ngmn.org/wp-content/uploads/ITU-R_FRAMEWORK_FOR_IMT-2030.pdf).

## Key Performance Targets

The 6G system aims to achieve **peak data rates of 50-200 Gbps**[3](https://www.rfwireless-world.com/Tutorials/6G-Wireless-Network-tutorial.html), representing a substantial improvement over 5G capabilities. **Ultra-low latency** targets range from **0.1-1 ms** for air-interface communications[4](https://digitalregulation.org/overview-of-6g-imt-2030/), enabling real-time applications like tactile internet and holographic telepresence[5](https://techblog.comsoc.org/2025/02/13/itu-r-wp-5d-progresses-reports-on-imt-2030-6g-minimum-technology-performance-requirements-evaluation-criteria-methodology/)[6](https://www.rfwireless-world.com/tutorials/6g/6g-wireless-network-tutorial).

**Reliability** specifications target success probabilities of **99.999% (1-10^-5 to 1-10^-7)**[7](https://www.cept.org/Documents/cpg-pta/77266/pta-23-047_imt-2030-6g-spectrum-needs-and-candidate-bands)[4](https://digitalregulation.org/overview-of-6g-imt-2030/), supporting mission-critical applications. The system will support **massive connection density** of **10^6 to 10^8 devices per km²**[4](https://digitalregulation.org/overview-of-6g-imt-2030/), enabling comprehensive IoT deployments.

## Core Technologies

6G networks will leverage **terahertz (THz) communication** for ultra-high bandwidth applications[6](https://www.rfwireless-world.com/tutorials/6g/6g-wireless-network-tutorial)[8](https://techblog.comsoc.org/2024/07/06/itu-r-imt-2030-6g-backgrounder-and-envisioned-capabilities/), along with **AI-driven network management** for dynamic resource allocation and self-optimization[8](https://techblog.comsoc.org/2024/07/06/itu-r-imt-2030-6g-backgrounder-and-envisioned-capabilities/)[9](https://www.cse.wustl.edu/~jain/cse574-24/ftp/6g/index.html). **Integrated Sensing and Communication (ISAC)** will provide dual functionality, combining communication and sensing capabilities[10](https://www.ericsson.com/en/reports-and-papers/white-papers/6g-spectrum-enabling-the-future-mobile-life-beyond-2030)[11](https://www.5gamericas.org/wp-content/uploads/2024/08/ITUs-IMT-2030-Vision_Id.pdf).

The architecture includes **massive MIMO** advancements, **intelligent reflecting surfaces**, and **edge computing** integration to support diverse applications from autonomous vehicles to immersive extended reality experiences[6](https://www.rfwireless-world.com/tutorials/6g/6g-wireless-network-tutorial)[12](https://sci-hub.se/downloads/2019-07-20/e1/10.1109@MVT.2019.2921398.pdf).

## Non-Terrestrial Networks (NTN) Characteristics

**NTN** represents a paradigm shift toward **integrated satellite-terrestrial networks**, providing **ubiquitous global coverage** that complements terrestrial infrastructure[13](https://eprints.lancs.ac.uk/id/eprint/210484/4/one6G_TechnologyOverview_version3.pdf)[14](https://www.itu.int/en/ITU-R/study-groups/rsg5/rwp5d/imt-2030/pages/default.aspx). The 3GPP Release 17 specifications define NTN as networks utilizing satellites, High Altitude Platforms (HAPS), and other airborne platforms[14](https://www.itu.int/en/ITU-R/study-groups/rsg5/rwp5d/imt-2030/pages/default.aspx).

## Coverage and Mobility

NTN excels in **global coverage capability**, reaching remote areas where terrestrial networks are impractical[15](https://www.cse.wustl.edu/~jain/cse574-24/ftp/6g.pdf)[16](https://arxiv.org/pdf/2402.10781.pdf). The system supports **high-speed mobility up to 1200 km/h**[17](https://www.itu.int/en/mediacentre/Pages/PR-2023-12-01-IMT-2030-for-6G-mobile-technologies.aspx), making it ideal for aviation and maritime applications.

**LEO satellites** operating above 600 km altitude provide **lower latency** (tens of milliseconds) compared to **GEO satellites** (up to 500 ms)[15](https://www.cse.wustl.edu/~jain/cse574-24/ftp/6g.pdf)[14](https://www.itu.int/en/ITU-R/study-groups/rsg5/rwp5d/imt-2030/pages/default.aspx). The integration includes both **transparent** and **regenerative payload architectures**, with transparent payloads acting as RF repeaters and regenerative payloads providing on-board processing capabilities[14](https://www.itu.int/en/ITU-R/study-groups/rsg5/rwp5d/imt-2030/pages/default.aspx)[18](https://vtsociety.org/files/ieeevts/2023-10/6G_Wireless_Networks_Vision_Requirements_Architecture_and_Key_Technologies.pdf).

## Advanced Capabilities

NTN systems incorporate **adaptive beam management** with steering capabilities to maintain connectivity as satellites move[15](https://www.cse.wustl.edu/~jain/cse574-24/ftp/6g.pdf)[14](https://www.itu.int/en/ITU-R/study-groups/rsg5/rwp5d/imt-2030/pages/default.aspx). **Optical inter-satellite links** enable high-capacity mesh networks between satellites, reducing dependence on ground infrastructure[19](https://www.intel.in/content/dam/www/central-libraries/xa/en/documents/2023-12/6g-framework-and-technology-1-.pdf).

The technology supports **seamless handover** between terrestrial and satellite networks, with **AI-driven resource management** optimizing spectrum usage and network performance[17](https://www.itu.int/en/mediacentre/Pages/PR-2023-12-01-IMT-2030-for-6G-mobile-technologies.aspx)[16](https://arxiv.org/pdf/2402.10781.pdf). **Disaster resilience** is a key strength, providing emergency communications when terrestrial infrastructure fails[20](https://www.ngmn.org/publications/itu-r-framework-for-imt-2030.html)[21](https://dl.cdn-anritsu.com/en-en/test-measurement/files/Brochures-Datasheets-Catalogs/Leaflet/ntn1-ef1103.pdf).

## Quantum Computing Characteristics

**Quantum Computing** leverages quantum mechanical phenomena including **superposition** and **entanglement** to process information fundamentally differently from classical computers[22](https://www.rfwireless-world.com/terminology/ntn-satellite-integration-with-terrestrial-networks)[23](https://docbox.etsi.org/Workshop/2024/04_ETSI_6G_NTN/SESSION%2004/S4_05_Chuberre.pdf). For 6G networks, quantum technologies offer **exponential speedup** for specific computational problems[24](https://www.3gpp.org/technologies/ntn-overview)[25](https://www.zte.com.cn/global/about/magazine/zte-technologies/2023/1-en/3/5g-ntn-helps-to-build-satellite-ground-converged-network.html).

## Security and Cryptography

Quantum computing provides **quantum-safe cryptography** through **Quantum Key Distribution (QKD)** and **quantum-resistant algorithms**[26](https://cordis.europa.eu/project/id/101096479)[27](https://www.viavisolutions.com/en-us/what-are-non-terrestrial-networks-ntn). This addresses the security challenges posed by quantum computers' ability to break current encryption schemes[28](https://www.satnow.com/community/what-is-non-terrestrial-network-ntn-satellite-communications)[29](https://docbox.etsi.org/Workshop/2024/04_ETSI_6G_NTN/SESSION%2004/S4_06_VIDAL.pdf).

**Quantum entanglement** enables **unconditionally secure communication** channels, as any eavesdropping attempt disturbs the quantum states[23](https://docbox.etsi.org/Workshop/2024/04_ETSI_6G_NTN/SESSION%2004/S4_05_Chuberre.pdf)[30](https://www.rohde-schwarz.com/us/solutions/wireless-communications-testing/wireless-standards/5g-nr/non-terrestrial-networks-ntn/non-terrestrial-networks-ntn_256719.html). The technology supports **ultra-precise sensing** capabilities for enhanced positioning and navigation applications[27](https://www.viavisolutions.com/en-us/what-are-non-terrestrial-networks-ntn)[31](https://www.rfwireless-world.com/Terminology/What-is-NTN-Satellite.html).

## Network Optimization

Quantum algorithms excel at **optimization problems**, enabling superior **resource allocation** and **network management** compared to classical approaches[25](https://www.zte.com.cn/global/about/magazine/zte-technologies/2023/1-en/3/5g-ntn-helps-to-build-satellite-ground-converged-network.html)[31](https://www.rfwireless-world.com/Terminology/What-is-NTN-Satellite.html). **Quantum machine learning** algorithms can process large datasets more efficiently, improving **predictive models** and **decision-making** in 6G systems[24](https://www.3gpp.org/technologies/ntn-overview)[26](https://cordis.europa.eu/project/id/101096479).

The **quantum network utility** metric provides a framework for measuring quantum network performance, considering factors like **quantum fidelity**, **entanglement generation rate**, and **coherence time**[32](https://www.etsi.org/images/Events/2024/NTN_CONFERENCE/6G_NTN_White_Paper_Vision-on-NTN-in-6G_r01_v04.pdf)33[30](https://www.rohde-schwarz.com/us/solutions/wireless-communications-testing/wireless-standards/5g-nr/non-terrestrial-networks-ntn/non-terrestrial-networks-ntn_256719.html).

## Comparative Analysis

## Performance Characteristics

**Latency performance** varies significantly across technologies. 6G IMT-2030 achieves the lowest latency (0.1-1 ms), while NTN faces propagation delays (10-500 ms depending on orbit), and quantum computing offers ultra-fast processing for specific algorithms[1](https://unidir.org/wp-content/uploads/2024/12/241211_ITU-R-Update-on-WRC-and-IMT-2030.pdf)[15](https://www.cse.wustl.edu/~jain/cse574-24/ftp/6g.pdf)[25](https://www.zte.com.cn/global/about/magazine/zte-technologies/2023/1-en/3/5g-ntn-helps-to-build-satellite-ground-converged-network.html).

**Security levels** show quantum computing providing maximum security through quantum-safe cryptography, while 6G and NTN offer enhanced but conventional security measures[24](https://www.3gpp.org/technologies/ntn-overview)[26](https://cordis.europa.eu/project/id/101096479).

**Network coverage** is NTN's primary strength with global reach, while 6G focuses on dense urban and suburban coverage, and quantum computing has limited coverage due to infrastructure requirements[14](https://www.itu.int/en/ITU-R/study-groups/rsg5/rwp5d/imt-2030/pages/default.aspx)[34](https://dl.cdn-anritsu.com/en-en/test-measurement/files/Brochures-Datasheets-Catalogs/Leaflet/ntn1-ef1102.pdf).

## Integration Challenges

**Scalability** presents different challenges for each technology. 6G requires massive infrastructure deployment, NTN needs satellite constellation management, and quantum computing faces qubit scaling limitations[14](https://www.itu.int/en/ITU-R/study-groups/rsg5/rwp5d/imt-2030/pages/default.aspx)[22](https://www.rfwireless-world.com/terminology/ntn-satellite-integration-with-terrestrial-networks)[35](https://hexa-x-ii.eu/wp-content/uploads/2024/02/240213_6G-NTN_v00.pdf).

**Energy efficiency** varies dramatically, with 6G targeting 100x improvement over 5G, NTN constrained by satellite power limitations, and quantum computing requiring significant energy for cooling systems[2](https://www.ngmn.org/wp-content/uploads/ITU-R_FRAMEWORK_FOR_IMT-2030.pdf)[29](https://docbox.etsi.org/Workshop/2024/04_ETSI_6G_NTN/SESSION%2004/S4_06_VIDAL.pdf).

## Future Convergence

The integration of these three technologies promises **revolutionary capabilities** for 2030 and beyond. **6G networks** will provide the high-performance terrestrial foundation, **NTN** will ensure global coverage and mobility, while **quantum computing** will enable unprecedented security and optimization capabilities[34](https://dl.cdn-anritsu.com/en-en/test-measurement/files/Brochures-Datasheets-Catalogs/Leaflet/ntn1-ef1102.pdf)[24](https://www.3gpp.org/technologies/ntn-overview)[26](https://cordis.europa.eu/project/id/101096479).

This convergence will support emerging applications including **holographic communications**, **autonomous systems**, **IoT at global scale**, and **AI-driven services** with quantum-enhanced security and performance[12](https://sci-hub.se/downloads/2019-07-20/e1/10.1109@MVT.2019.2921398.pdf)[16](https://arxiv.org/pdf/2402.10781.pdf)[31](https://www.rfwireless-world.com/Terminology/What-is-NTN-Satellite.html).

The successful integration of 6G IMT-2030, NTN, and quantum computing will create a unified, intelligent, and secure communication ecosystem capable of addressing the diverse connectivity and computing challenges of the future digital society.

1. [https://unidir.org/wp-content/uploads/2024/12/241211_ITU-R-Update-on-WRC-and-IMT-2030.pdf](https://unidir.org/wp-content/uploads/2024/12/241211_ITU-R-Update-on-WRC-and-IMT-2030.pdf)
2. [https://www.ngmn.org/wp-content/uploads/ITU-R_FRAMEWORK_FOR_IMT-2030.pdf](https://www.ngmn.org/wp-content/uploads/ITU-R_FRAMEWORK_FOR_IMT-2030.pdf)
3. [https://www.rfwireless-world.com/Tutorials/6G-Wireless-Network-tutorial.html](https://www.rfwireless-world.com/Tutorials/6G-Wireless-Network-tutorial.html)
4. [https://digitalregulation.org/overview-of-6g-imt-2030/](https://digitalregulation.org/overview-of-6g-imt-2030/)
5. [https://techblog.comsoc.org/2025/02/13/itu-r-wp-5d-progresses-reports-on-imt-2030-6g-minimum-technology-performance-requirements-evaluation-criteria-methodology/](https://techblog.comsoc.org/2025/02/13/itu-r-wp-5d-progresses-reports-on-imt-2030-6g-minimum-technology-performance-requirements-evaluation-criteria-methodology/)
6. [https://www.rfwireless-world.com/tutorials/6g/6g-wireless-network-tutorial](https://www.rfwireless-world.com/tutorials/6g/6g-wireless-network-tutorial)
7. [https://www.cept.org/Documents/cpg-pta/77266/pta-23-047_imt-2030-6g-spectrum-needs-and-candidate-bands](https://www.cept.org/Documents/cpg-pta/77266/pta-23-047_imt-2030-6g-spectrum-needs-and-candidate-bands)
8. [https://techblog.comsoc.org/2024/07/06/itu-r-imt-2030-6g-backgrounder-and-envisioned-capabilities/](https://techblog.comsoc.org/2024/07/06/itu-r-imt-2030-6g-backgrounder-and-envisioned-capabilities/)
9. [https://www.cse.wustl.edu/~jain/cse574-24/ftp/6g/index.html](https://www.cse.wustl.edu/~jain/cse574-24/ftp/6g/index.html)
10. [https://www.ericsson.com/en/reports-and-papers/white-papers/6g-spectrum-enabling-the-future-mobile-life-beyond-2030](https://www.ericsson.com/en/reports-and-papers/white-papers/6g-spectrum-enabling-the-future-mobile-life-beyond-2030)
11. [https://www.5gamericas.org/wp-content/uploads/2024/08/ITUs-IMT-2030-Vision_Id.pdf](https://www.5gamericas.org/wp-content/uploads/2024/08/ITUs-IMT-2030-Vision_Id.pdf)
12. [https://sci-hub.se/downloads/2019-07-20/e1/10.1109@MVT.2019.2921398.pdf](https://sci-hub.se/downloads/2019-07-20/e1/10.1109@MVT.2019.2921398.pdf)
13. [https://eprints.lancs.ac.uk/id/eprint/210484/4/one6G_TechnologyOverview_version3.pdf](https://eprints.lancs.ac.uk/id/eprint/210484/4/one6G_TechnologyOverview_version3.pdf)
14. [https://www.itu.int/en/ITU-R/study-groups/rsg5/rwp5d/imt-2030/pages/default.aspx](https://www.itu.int/en/ITU-R/study-groups/rsg5/rwp5d/imt-2030/pages/default.aspx)
15. [https://www.cse.wustl.edu/~jain/cse574-24/ftp/6g.pdf](https://www.cse.wustl.edu/~jain/cse574-24/ftp/6g.pdf)
16. [https://arxiv.org/pdf/2402.10781.pdf](https://arxiv.org/pdf/2402.10781.pdf)
17. [https://www.itu.int/en/mediacentre/Pages/PR-2023-12-01-IMT-2030-for-6G-mobile-technologies.aspx](https://www.itu.int/en/mediacentre/Pages/PR-2023-12-01-IMT-2030-for-6G-mobile-technologies.aspx)
18. [https://vtsociety.org/files/ieeevts/2023-10/6G_Wireless_Networks_Vision_Requirements_Architecture_and_Key_Technologies.pdf](https://vtsociety.org/files/ieeevts/2023-10/6G_Wireless_Networks_Vision_Requirements_Architecture_and_Key_Technologies.pdf)
19. [https://www.intel.in/content/dam/www/central-libraries/xa/en/documents/2023-12/6g-framework-and-technology-1-.pdf](https://www.intel.in/content/dam/www/central-libraries/xa/en/documents/2023-12/6g-framework-and-technology-1-.pdf)
20. [https://www.ngmn.org/publications/itu-r-framework-for-imt-2030.html](https://www.ngmn.org/publications/itu-r-framework-for-imt-2030.html)
21. [https://dl.cdn-anritsu.com/en-en/test-measurement/files/Brochures-Datasheets-Catalogs/Leaflet/ntn1-ef1103.pdf](https://dl.cdn-anritsu.com/en-en/test-measurement/files/Brochures-Datasheets-Catalogs/Leaflet/ntn1-ef1103.pdf)
22. [https://www.rfwireless-world.com/terminology/ntn-satellite-integration-with-terrestrial-networks](https://www.rfwireless-world.com/terminology/ntn-satellite-integration-with-terrestrial-networks)
23. [https://docbox.etsi.org/Workshop/2024/04_ETSI_6G_NTN/SESSION%2004/S4_05_Chuberre.pdf](https://docbox.etsi.org/Workshop/2024/04_ETSI_6G_NTN/SESSION%2004/S4_05_Chuberre.pdf)
24. [https://www.3gpp.org/technologies/ntn-overview](https://www.3gpp.org/technologies/ntn-overview)
25. [https://www.zte.com.cn/global/about/magazine/zte-technologies/2023/1-en/3/5g-ntn-helps-to-build-satellite-ground-converged-network.html](https://www.zte.com.cn/global/about/magazine/zte-technologies/2023/1-en/3/5g-ntn-helps-to-build-satellite-ground-converged-network.html)
26. [https://cordis.europa.eu/project/id/101096479](https://cordis.europa.eu/project/id/101096479)
27. [https://www.viavisolutions.com/en-us/what-are-non-terrestrial-networks-ntn](https://www.viavisolutions.com/en-us/what-are-non-terrestrial-networks-ntn)
28. [https://www.satnow.com/community/what-is-non-terrestrial-network-ntn-satellite-communications](https://www.satnow.com/community/what-is-non-terrestrial-network-ntn-satellite-communications)
29. [https://docbox.etsi.org/Workshop/2024/04_ETSI_6G_NTN/SESSION%2004/S4_06_VIDAL.pdf](https://docbox.etsi.org/Workshop/2024/04_ETSI_6G_NTN/SESSION%2004/S4_06_VIDAL.pdf)
30. [https://www.rohde-schwarz.com/us/solutions/wireless-communications-testing/wireless-standards/5g-nr/non-terrestrial-networks-ntn/non-terrestrial-networks-ntn_256719.html](https://www.rohde-schwarz.com/us/solutions/wireless-communications-testing/wireless-standards/5g-nr/non-terrestrial-networks-ntn/non-terrestrial-networks-ntn_256719.html)
31. [https://www.rfwireless-world.com/Terminology/What-is-NTN-Satellite.html](https://www.rfwireless-world.com/Terminology/What-is-NTN-Satellite.html)
32. [https://www.etsi.org/images/Events/2024/NTN_CONFERENCE/6G_NTN_White_Paper_Vision-on-NTN-in-6G_r01_v04.pdf](https://www.etsi.org/images/Events/2024/NTN_CONFERENCE/6G_NTN_White_Paper_Vision-on-NTN-in-6G_r01_v04.pdf)
33. [https://www.youtube.com/watch?v=TLnTzwefIuY](https://www.youtube.com/watch?v=TLnTzwefIuY)
34. [https://dl.cdn-anritsu.com/en-en/test-measurement/files/Brochures-Datasheets-Catalogs/Leaflet/ntn1-ef1102.pdf](https://dl.cdn-anritsu.com/en-en/test-measurement/files/Brochures-Datasheets-Catalogs/Leaflet/ntn1-ef1102.pdf)
35. [https://hexa-x-ii.eu/wp-content/uploads/2024/02/240213_6G-NTN_v00.pdf](https://hexa-x-ii.eu/wp-content/uploads/2024/02/240213_6G-NTN_v00.pdf)
36. [https://www.anritsu.com/en-us/test-measurement/solutions/non-terrestrial-networks-test?tm_navigation=solution](https://www.anritsu.com/en-us/test-measurement/solutions/non-terrestrial-networks-test?tm_navigation=solution)
37. [https://www.u-blox.com/en/technologies/ntn](https://www.u-blox.com/en/technologies/ntn)
38. [https://research.chalmers.se/publication/546711/file/546711_Fulltext.pdf](https://research.chalmers.se/publication/546711/file/546711_Fulltext.pdf)
39. [https://article.murata.com/en-eu/article/what-is-a-ntn-of-haps-and-satellites](https://article.murata.com/en-eu/article/what-is-a-ntn-of-haps-and-satellites)
40. [https://www.gsmaintelligence.com/topics/satellite-and-ntn](https://www.gsmaintelligence.com/topics/satellite-and-ntn)
41. [https://en.wikipedia.org/wiki/Quantum_computing](https://en.wikipedia.org/wiki/Quantum_computing)
42. [https://www.gbis.ch/index.php/gbis/article/view/539](https://www.gbis.ch/index.php/gbis/article/view/539)
43. [https://pmc.ncbi.nlm.nih.gov/articles/PMC11047070/](https://pmc.ncbi.nlm.nih.gov/articles/PMC11047070/)
44. [https://www.nqcc.ac.uk/quantum-features/](https://www.nqcc.ac.uk/quantum-features/)
45. [https://arxiv.org/html/2504.17133v1](https://arxiv.org/html/2504.17133v1)
46. [https://www.youtube.com/watch?v=oaXHtNV3fWU](https://www.youtube.com/watch?v=oaXHtNV3fWU)
47. [https://www.ibm.com/think/topics/quantum-computing](https://www.ibm.com/think/topics/quantum-computing)
48. [https://d197for5662m48.cloudfront.net/documents/publicationstatus/181009/preprint_pdf/da2a75cfe63fb78fbf0033fe2af68007.pdf](https://d197for5662m48.cloudfront.net/documents/publicationstatus/181009/preprint_pdf/da2a75cfe63fb78fbf0033fe2af68007.pdf)
49. [https://www.pnas.org/doi/10.1073/pnas.2314103121](https://www.pnas.org/doi/10.1073/pnas.2314103121)
50. [https://neosfer.de/en/quantum-computing-revolutionizing-the-future-of-computational-power/](https://neosfer.de/en/quantum-computing-revolutionizing-the-future-of-computational-power/)
51. [https://www.sciopen.com/article/10.26599/TST.2024.9010118](https://www.sciopen.com/article/10.26599/TST.2024.9010118)
52. [http://arxiv.org/pdf/2210.10752.pdf](http://arxiv.org/pdf/2210.10752.pdf)
53. [https://www.accenture.com/in-en/insights/quantum-computing](https://www.accenture.com/in-en/insights/quantum-computing)
54. [https://dl.acm.org/doi/pdf/10.1145/3663531.3664754](https://dl.acm.org/doi/pdf/10.1145/3663531.3664754)
55. [https://www.brighttalk.com/webcast/19861/638170?player-preauth=YhcVxdw%2FC%2BAShailFBcockOpP9SmDs66a%2Fw%2B3bamHPE%3D](https://www.brighttalk.com/webcast/19861/638170?player-preauth=YhcVxdw%2FC%2BAShailFBcockOpP9SmDs66a%2Fw%2B3bamHPE%3D)
56. [https://itif.org/publications/2018/09/20/itif-technology-explainer-what-quantum-computing/](https://itif.org/publications/2018/09/20/itif-technology-explainer-what-quantum-computing/)
57. [https://www.sciencedirect.com/science/article/pii/S0950584924000594](https://www.sciencedirect.com/science/article/pii/S0950584924000594)
58. [https://www.digitale-technologien.de/DT/Redaktion/EN/Downloads/Publikation/Quantencomputing/240924_benchmarking_for_quantentum_computing.pdf?__blob=publicationFile&v=2](https://www.digitale-technologien.de/DT/Redaktion/EN/Downloads/Publikation/Quantencomputing/240924_benchmarking_for_quantentum_computing.pdf?__blob=publicationFile&v=2)
59. [https://www.energy.gov/science/doe-explainsquantum-computing](https://www.energy.gov/science/doe-explainsquantum-computing)
60. [https://onlinelibrary.wiley.com/doi/10.1002/qute.202300334](https://onlinelibrary.wiley.com/doi/10.1002/qute.202300334)


### 14/7 Meeting with Ming 
Future core network - industry 

Franhofer focus - 5G core now buiding 6G core 
Marius Corici - Towards Service based Access network 
Use cases
2025 NVS (Next generation vision and sustainability conference)

- Our ideas
	- trustworthiness - extract semantic meaning of the packet - where computing is placed
	- QFSS - Blind quantum Computing - issue : client prepare quantum state and quantum channel 
	- Satellite as server - give to different quantum computers - satellite can reconstruct its outputs 
	- Why to blind the quantum service - trustworthiness towards this server 
	- Not just QPUs but with hybrid CPUs 
	- what needs to be done in the core  to quantify the change 
	- How to deal with hybrid quantum classic archi - where is the exposure 
	- Expose quantum as open APIs - rest manage in the black box
	- Exposure at the physical layer ? 
	- Link, or any layer - what benefits end classical user 
	- what interface the classic guys to use the system 
	- Computing as a service - exposure via cloud platform and the integration happens behind this cloud
	- cloud based quantum computing services 
	- offer this platform to the core 
	- QKD  vendors - testbed DEMOQUANT (DT) alias Berlin and Bonn (QKD 900 km - nodes in between relay QKD key) - separate system - integrate this into classical network - step by step 
	- Two channel (QKD and classic - evaluate to replace classic with QKD in long run) - pilot phase 
	- Complexity and new stuff - if need to be realistic and integrate - how other people can integrate and benefit 
	- Distribute the quantum computers 
	- Service mediator in between -
	- Extract quantum random numbers 
	- Technology enablers and services 
	- Future core - dynamic, flexible and extensible 
	- technology enabler 
	- Quantum physical layer  - quantum randomness - create interfaces and enables 
	- Principle to merge 
	- Quantum computing capability 
	- Common best practice principle - service based -  different discovery based implementation
- Dynamic discovery , management - orchestration is mature
- Trustworthiness - enhancement 
- XR devices - more data? focus on information - then service based interface 
- rework on fig 1 
- different between data and information ?
- Figure 1 

---
What is NTN user ? 

trustworthiness , resilience, of the core needs certain growth from 4G towards 6G 
API and protocols - semantic-level 

verification protocol - how to circle back to application level 
Recovery of trustworthiness from classical network 
 verification protocols over the network and core
 and QFSS doesn't have one 
 AUSF 
Hoare logic
5G core - trustworthiness monitoring 
Protocol - Classical  | quantum | Classical 
 NISQ  - Noisy Intermediate Quantum 
Performance indicators for 

| Quantum       | Classical |
| ------------- | --------- |
| state quality |           |
| latency       |           |
| Qubit rate    |           |
|               |           |

---
https://www.science.org/doi/10.1126/science.aam9288 
https://ar5iv.labs.arxiv.org/html/1903.10685 
We add quantum functionalities to the classical core

# Quantum-Classical Hybrid Computing Architecture with Bridge Interface for Edge Computing

Based on the handwritten notes in the image and the focus on optimization and trustworthiness, here's a comprehensive core architecture for a quantum-classical hybrid computing system with edge computing capabilities:

![Core architecture diagram for quantum-classical hybrid computing system with bridge interface and edge computing](https://user-gen-media-assets.s3.amazonaws.com/gpt4o_images/680b6a1b-e866-41c4-864c-9b526571c9ee.png)

Core architecture diagram for quantum-classical hybrid computing system with bridge interface and edge computing

## Core Architecture Overview

The **Quantum-Classical Hybrid Computing Architecture** integrates quantum processing units (QPUs) with classical computing resources through a sophisticated bridge interface, enabling distributed computing across edge, fog, and cloud layers. This architecture is specifically designed for optimization problems and trustworthiness applications1[2](https://www.quera.com/blog-posts/hybrid-quantum-computing-bridging-classical-and-quantum-worlds)[3](https://milvus.io/ai-quick-reference/what-are-hybrid-quantumclassical-algorithms).

## Five-Layer Architecture Framework

## 1. **Application Layer**

The topmost layer hosts quantum algorithms and applications focused on optimization and trustworthiness:

- **Quantum Optimization Algorithms**: QAOA (Quantum Approximate Optimization Algorithm) and VQE (Variational Quantum Eigensolver) for combinatorial optimization problems[4](https://openreview.net/pdf?id=A1JMyqnbdh)[5](https://www.linkedin.com/pulse/architecting-quantum-classical-hybrid-systems-anand-ramachandran-de4ce)
    
- **Quantum Security Protocols**: Quantum key distribution (QKD) and quantum cryptography for trustworthy communications[6](https://www.spinquanta.com/news-detail/hybrid-quantum-classical-algorithms-the-future-of-computing20250123075527)[7](https://arxiv.org/abs/2305.05238)
    
- **Hybrid Algorithm Orchestration**: Manages the execution of quantum-classical workflows[8](https://www.future-of-computing.com/quantum-bridge-shaping-the-future-of-quantum-cybersecurity/)[9](https://milvus.io/ai-quick-reference/what-is-the-role-of-classical-computation-in-hybrid-quantum-systems)
    

## 2. **Runtime/Compiler Layer**

Translates high-level quantum algorithms into executable instructions:

- **Quantum-Classical Code Translation**: Converts hybrid algorithms into quantum circuits and classical subroutines[10](https://intranet.icar.cnr.it/wp-content/uploads/2023/04/RT-ICAR-CS-22-9.pdf)
- **Resource Allocation**: Distributes tasks between quantum and classical processors based on problem characteristics[11](https://arxiv.org/abs/2506.01177)[12](https://www.scitepress.org/Papers/2025/135423/135423.pdf)
- **Optimization Parameter Management**: Handles variational parameters in hybrid algorithms[13](https://ui.adsabs.harvard.edu/abs/2024arXiv240504824I/abstract)[14](https://arxiv.org/abs/2305.14304)
    

## 3. **Hybrid Computing Layer**

The critical **bridge interface** that seamlessly integrates quantum and classical computing:

- **Quantum-Classical Interface (QCI)**: Manages communication between quantum and classical systems using advanced interfacing protocols[15](https://learn.microsoft.com/en-us/azure/quantum/hybrid-computing-overview)[16](https://paperswithcode.com/paper/architectural-vision-for-quantum-computing-in)
    
- **Task Partitioning**: Dynamically allocates computational tasks based on quantum advantage potential[17](https://sc18.supercomputing.org/proceedings/workshops/workshop_files/ws_pmes110s1-file1.pdf)[18](https://arxiv.org/html/2503.18868v1)
    
- **Error Correction and Mitigation**: Implements quantum error correction codes and classical post-processing[19](https://www.scirp.org/pdf/ait2024144_24000432.pdf)[20](https://bpb-us-w2.wpmucdn.com/voices.uchicago.edu/dist/0/2327/files/2019/12/HybridQuantumPMES.pdf)
    
- **Data Format Conversion**: Translates between quantum states and classical data representations[21](https://ionq.com/resources/what-is-hybrid-quantum-computing)
    

## 4. **Control and Measurement Layer**

Provides precise control of quantum operations:

- **Quantum Control Systems**: Generates microwave/optical signals for qubit manipulation[22](https://www.geeksforgeeks.org/computer-organization-architecture/five-layered-architecture-of-quantum-computing/)[9](https://milvus.io/ai-quick-reference/what-is-the-role-of-classical-computation-in-hybrid-quantum-systems)
    
- **Measurement and Readout**: Converts quantum measurements to classical data[8](https://www.future-of-computing.com/quantum-bridge-shaping-the-future-of-quantum-cybersecurity/)[23](https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.4.043221)
    
- **Synchronization**: Ensures proper timing between quantum and classical operations[21](https://ionq.com/resources/what-is-hybrid-quantum-computing)
    

## 5. **Physical Layer**

The hardware foundation supporting both quantum and classical computing:

- **Quantum Processing Units (QPUs)**: Various qubit technologies (superconducting, trapped ion, photonic)[22](https://www.geeksforgeeks.org/computer-organization-architecture/five-layered-architecture-of-quantum-computing/)[24](https://link.aps.org/doi/10.1103/PhysRevX.2.031007)
    
- **Classical Edge Nodes**: Distributed computing resources for local processing[2](https://www.quera.com/blog-posts/hybrid-quantum-computing-bridging-classical-and-quantum-worlds)[25](https://ijact.in/index.php/j/article/download/618/603/1180)
    
- **Interconnection Networks**: High-speed communication between distributed components[26](https://arxiv.org/abs/1010.5022)[27](https://www.ornl.gov/publication/simulating-quantum-classical-interfaces-lindblad-master-equation)
    

## Edge Computing Integration

## **Quantum Edge Intelligence (QEI) Framework**

The architecture incorporates **Quantum Edge Intelligence** principles to enable distributed quantum-classical computing[2](https://www.quera.com/blog-posts/hybrid-quantum-computing-bridging-classical-and-quantum-worlds)[28](https://www.spinquanta.com/news-detail/quantum-computer-architecture):

## **Device Layer**

- **IoT Devices and Sensors**: Collect data for optimization problems
    
- **Edge Quantum Processors**: Small-scale quantum devices for local quantum computation
    
- **Classical Edge Nodes**: Handle preprocessing and postprocessing tasks
    

## **Edge/Fog Layer**

- **Hybrid Computing Nodes**: Combine quantum and classical processing capabilities
    
- **Quantum-Enhanced Edge Servers**: Process optimization problems with quantum acceleration[25](https://ijact.in/index.php/j/article/download/618/603/1180)[29](https://pmc.ncbi.nlm.nih.gov/articles/PMC8700383/)
    
- **Local Optimization Services**: Provide real-time optimization solutions for edge applications
    

## **Cloud/Quantum Layer**

- **Large-Scale QPUs**: Handle complex optimization problems requiring extensive quantum resources
    
- **Quantum Computing as a Service (QCaaS)**: Provide remote access to quantum processors[30](https://quantum.phys.lsu.edu/old-website/seminars/abstracts/Layered_QC_Architecture.pdf)[10](https://intranet.icar.cnr.it/wp-content/uploads/2023/04/RT-ICAR-CS-22-9.pdf)
    
- **Distributed Quantum Networks**: Enable quantum communication across geographically dispersed locations[31](https://arxiv.org/abs/2405.04824)
    

## Bridge Interface Components

## **Quantum-Classical Communication Bridge**

The bridge interface implements several key mechanisms:

1. **Quantum State Preparation and Measurement Interface**
    
    - Converts classical optimization parameters to quantum states
        
    - Translates quantum measurement outcomes to classical results[15](https://learn.microsoft.com/en-us/azure/quantum/hybrid-computing-overview)[16](https://paperswithcode.com/paper/architectural-vision-for-quantum-computing-in)
        
2. **Hybrid Algorithm Execution Engine**
    
    - Orchestrates iterative quantum-classical loops
        
    - Manages parameter optimization using classical algorithms[32](http://tph.tuwien.ac.at/~svozil/publ/2000-interface-newlyformatted.pdf)[13](https://ui.adsabs.harvard.edu/abs/2024arXiv240504824I/abstract)
        
3. **Error Mitigation and Correction Bridge**
    
    - Implements quantum error correction protocols
        
    - Provides classical post-processing for noise mitigation[19](https://www.scirp.org/pdf/ait2024144_24000432.pdf)[20](https://bpb-us-w2.wpmucdn.com/voices.uchicago.edu/dist/0/2327/files/2019/12/HybridQuantumPMES.pdf)
        
4. **Data Security and Trust Interface**
    
    - Quantum key distribution for secure communication
        
    - Device-independent quantum cryptography protocols[6](https://www.spinquanta.com/news-detail/hybrid-quantum-classical-algorithms-the-future-of-computing20250123075527)[33](https://upcommons.upc.edu/bitstream/handle/2117/340433/DCIS2020.pdf)
        

## Optimization and Trustworthiness Applications

## **Optimization Applications**

The architecture supports various optimization problems:

- **Combinatorial Optimization**: Using QAOA for scheduling, routing, and resource allocation[4](https://openreview.net/pdf?id=A1JMyqnbdh)[5](https://www.linkedin.com/pulse/architecting-quantum-classical-hybrid-systems-anand-ramachandran-de4ce)
    
- **Continuous Optimization**: Leveraging VQE for parameter optimization problems[34](https://jisem-journal.com/index.php/journal/article/download/6746/3130/11269)[35](https://phys.org/news/2025-01-physicists-bridge-strategy-stabilize-quantum.html)
    
- **Energy Optimization**: Quantum-enhanced algorithms for power grid and energy system optimization[36](http://arxiv.org/pdf/1010.5022.pdf)[29](https://pmc.ncbi.nlm.nih.gov/articles/PMC8700383/)
    

## **Trustworthiness and Security Features**

- **Quantum-Safe Cryptography**: Post-quantum cryptographic algorithms for long-term security[7](https://arxiv.org/abs/2305.05238)[37](https://www.scirp.org/journal/paperinformation?paperid=137004)
    
- **Quantum Key Distribution**: Unconditionally secure key exchange protocols[6](https://www.spinquanta.com/news-detail/hybrid-quantum-classical-algorithms-the-future-of-computing20250123075527)[38](https://arxiv.org/html/2404.05174v1)
    
- **Device-Independent Security**: Verification protocols that don't require trusted quantum devices[33](https://upcommons.upc.edu/bitstream/handle/2117/340433/DCIS2020.pdf)[39](http://arxiv.org/pdf/2208.09172.pdf)
    
- **Quantum Random Number Generation**: Hardware-based true randomness for cryptographic applications[38](https://arxiv.org/html/2404.05174v1)
    

## Implementation Considerations

## **Hardware Requirements**

- **Quantum Hardware**: NISQ devices with 50-100 qubits for near-term applications[2](https://www.quera.com/blog-posts/hybrid-quantum-computing-bridging-classical-and-quantum-worlds)[22](https://www.geeksforgeeks.org/computer-organization-architecture/five-layered-architecture-of-quantum-computing/)
    
- **Classical Infrastructure**: High-performance computing resources for hybrid algorithms[17](https://sc18.supercomputing.org/proceedings/workshops/workshop_files/ws_pmes110s1-file1.pdf)[21](https://ionq.com/resources/what-is-hybrid-quantum-computing)
    
- **Networking**: Low-latency communication between distributed components[26](https://arxiv.org/abs/1010.5022)[27](https://www.ornl.gov/publication/simulating-quantum-classical-interfaces-lindblad-master-equation)
    

## **Software Stack**

- **Quantum Development Frameworks**: Qiskit, Cirq, PennyLane for quantum circuit development[32](http://tph.tuwien.ac.at/~svozil/publ/2000-interface-newlyformatted.pdf)[10](https://intranet.icar.cnr.it/wp-content/uploads/2023/04/RT-ICAR-CS-22-9.pdf)
    
- **Classical Optimization Libraries**: SciPy, PyTorch for parameter optimization[13](https://ui.adsabs.harvard.edu/abs/2024arXiv240504824I/abstract)[14](https://arxiv.org/abs/2305.14304)
    
- **Hybrid Orchestration Tools**: Middleware for managing quantum-classical workflows[40](https://www.numberanalytics.com/blog/hybrid-quantum-systems-atomic-magnetometry-sensing)[10](https://intranet.icar.cnr.it/wp-content/uploads/2023/04/RT-ICAR-CS-22-9.pdf)
    

## **Performance Metrics**

- **Quantum Advantage**: Measurable speedup over classical algorithms[41](https://quantumzeitgeist.com/hybrid-quantum-systems-bridging-classical-and-quantum-worlds/)[42](https://www.londondaily.news/quantum-computing-architecture/)
    
- **Scalability**: Ability to handle increasing problem sizes[2](https://www.quera.com/blog-posts/hybrid-quantum-computing-bridging-classical-and-quantum-worlds)[25](https://ijact.in/index.php/j/article/download/618/603/1180)
    
- **Fault Tolerance**: Resilience to quantum errors and classical failures[20](https://bpb-us-w2.wpmucdn.com/voices.uchicago.edu/dist/0/2327/files/2019/12/HybridQuantumPMES.pdf)[17](https://sc18.supercomputing.org/proceedings/workshops/workshop_files/ws_pmes110s1-file1.pdf)
    
- **Security Assurance**: Provable security guarantees for cryptographic protocols[6](https://www.spinquanta.com/news-detail/hybrid-quantum-classical-algorithms-the-future-of-computing20250123075527)[7](https://arxiv.org/abs/2305.05238)
    

## Future Developments

This architecture provides a foundation for next-generation quantum-classical hybrid systems that can:

- Scale to larger quantum processors as they become available
    
- Integrate with emerging quantum networking technologies
    
- Support more sophisticated optimization and security applications
    
- Enable truly distributed quantum computing across edge-cloud continuum
    

The modular design ensures that individual components can be upgraded independently, making the architecture adaptable to rapid advances in quantum computing technology while maintaining robust classical computing capabilities for immediate practical applications.

1. [https://pplx-res.cloudinary.com/image/private/user_uploads/58228666/da3e285c-4ff5-4fc1-8dd8-33d34220e7f2/IMG20250718142141.jpg](https://pplx-res.cloudinary.com/image/private/user_uploads/58228666/da3e285c-4ff5-4fc1-8dd8-33d34220e7f2/IMG20250718142141.jpg)
2. [https://www.quera.com/blog-posts/hybrid-quantum-computing-bridging-classical-and-quantum-worlds](https://www.quera.com/blog-posts/hybrid-quantum-computing-bridging-classical-and-quantum-worlds)
3. [https://milvus.io/ai-quick-reference/what-are-hybrid-quantumclassical-algorithms](https://milvus.io/ai-quick-reference/what-are-hybrid-quantumclassical-algorithms)
4. [https://openreview.net/pdf?id=A1JMyqnbdh](https://openreview.net/pdf?id=A1JMyqnbdh)
5. [https://www.linkedin.com/pulse/architecting-quantum-classical-hybrid-systems-anand-ramachandran-de4ce](https://www.linkedin.com/pulse/architecting-quantum-classical-hybrid-systems-anand-ramachandran-de4ce)
6. [https://www.spinquanta.com/news-detail/hybrid-quantum-classical-algorithms-the-future-of-computing20250123075527](https://www.spinquanta.com/news-detail/hybrid-quantum-classical-algorithms-the-future-of-computing20250123075527)
7. [https://arxiv.org/abs/2305.05238](https://arxiv.org/abs/2305.05238)
8. [https://www.future-of-computing.com/quantum-bridge-shaping-the-future-of-quantum-cybersecurity/](https://www.future-of-computing.com/quantum-bridge-shaping-the-future-of-quantum-cybersecurity/)
9. [https://milvus.io/ai-quick-reference/what-is-the-role-of-classical-computation-in-hybrid-quantum-systems](https://milvus.io/ai-quick-reference/what-is-the-role-of-classical-computation-in-hybrid-quantum-systems)
10. [https://intranet.icar.cnr.it/wp-content/uploads/2023/04/RT-ICAR-CS-22-9.pdf](https://intranet.icar.cnr.it/wp-content/uploads/2023/04/RT-ICAR-CS-22-9.pdf)
11. [https://arxiv.org/abs/2506.01177](https://arxiv.org/abs/2506.01177)
12. [https://www.scitepress.org/Papers/2025/135423/135423.pdf](https://www.scitepress.org/Papers/2025/135423/135423.pdf)
13. [https://ui.adsabs.harvard.edu/abs/2024arXiv240504824I/abstract](https://ui.adsabs.harvard.edu/abs/2024arXiv240504824I/abstract)
14. [https://arxiv.org/abs/2305.14304](https://arxiv.org/abs/2305.14304)
15. [https://learn.microsoft.com/en-us/azure/quantum/hybrid-computing-overview](https://learn.microsoft.com/en-us/azure/quantum/hybrid-computing-overview)
16. [https://paperswithcode.com/paper/architectural-vision-for-quantum-computing-in](https://paperswithcode.com/paper/architectural-vision-for-quantum-computing-in)
17. [https://sc18.supercomputing.org/proceedings/workshops/workshop_files/ws_pmes110s1-file1.pdf](https://sc18.supercomputing.org/proceedings/workshops/workshop_files/ws_pmes110s1-file1.pdf)
18. [https://arxiv.org/html/2503.18868v1](https://arxiv.org/html/2503.18868v1)
19. [https://www.scirp.org/pdf/ait2024144_24000432.pdf](https://www.scirp.org/pdf/ait2024144_24000432.pdf)
20. [https://bpb-us-w2.wpmucdn.com/voices.uchicago.edu/dist/0/2327/files/2019/12/HybridQuantumPMES.pdf](https://bpb-us-w2.wpmucdn.com/voices.uchicago.edu/dist/0/2327/files/2019/12/HybridQuantumPMES.pdf)
21. [https://ionq.com/resources/what-is-hybrid-quantum-computing](https://ionq.com/resources/what-is-hybrid-quantum-computing)
22. [https://www.geeksforgeeks.org/computer-organization-architecture/five-layered-architecture-of-quantum-computing/](https://www.geeksforgeeks.org/computer-organization-architecture/five-layered-architecture-of-quantum-computing/)
23. [https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.4.043221](https://journals.aps.org/prresearch/abstract/10.1103/PhysRevResearch.4.043221)
24. [https://link.aps.org/doi/10.1103/PhysRevX.2.031007](https://link.aps.org/doi/10.1103/PhysRevX.2.031007)
25. [https://ijact.in/index.php/j/article/download/618/603/1180](https://ijact.in/index.php/j/article/download/618/603/1180)
26. [https://arxiv.org/abs/1010.5022](https://arxiv.org/abs/1010.5022)
27. [https://www.ornl.gov/publication/simulating-quantum-classical-interfaces-lindblad-master-equation](https://www.ornl.gov/publication/simulating-quantum-classical-interfaces-lindblad-master-equation)
28. [https://www.spinquanta.com/news-detail/quantum-computer-architecture](https://www.spinquanta.com/news-detail/quantum-computer-architecture)
29. [https://pmc.ncbi.nlm.nih.gov/articles/PMC8700383/](https://pmc.ncbi.nlm.nih.gov/articles/PMC8700383/)
30. [https://quantum.phys.lsu.edu/old-website/seminars/abstracts/Layered_QC_Architecture.pdf](https://quantum.phys.lsu.edu/old-website/seminars/abstracts/Layered_QC_Architecture.pdf)
31. [https://arxiv.org/abs/2405.04824](https://arxiv.org/abs/2405.04824)
32. [http://tph.tuwien.ac.at/~svozil/publ/2000-interface-newlyformatted.pdf](http://tph.tuwien.ac.at/~svozil/publ/2000-interface-newlyformatted.pdf)
33. [https://upcommons.upc.edu/bitstream/handle/2117/340433/DCIS2020.pdf](https://upcommons.upc.edu/bitstream/handle/2117/340433/DCIS2020.pdf)
34. [https://jisem-journal.com/index.php/journal/article/download/6746/3130/11269](https://jisem-journal.com/index.php/journal/article/download/6746/3130/11269)
35. [https://phys.org/news/2025-01-physicists-bridge-strategy-stabilize-quantum.html](https://phys.org/news/2025-01-physicists-bridge-strategy-stabilize-quantum.html)
36. [http://arxiv.org/pdf/1010.5022.pdf](http://arxiv.org/pdf/1010.5022.pdf)
37. [https://www.scirp.org/journal/paperinformation?paperid=137004](https://www.scirp.org/journal/paperinformation?paperid=137004)
38. [https://arxiv.org/html/2404.05174v1](https://arxiv.org/html/2404.05174v1)
39. [http://arxiv.org/pdf/2208.09172.pdf](http://arxiv.org/pdf/2208.09172.pdf)
40. [https://www.numberanalytics.com/blog/hybrid-quantum-systems-atomic-magnetometry-sensing](https://www.numberanalytics.com/blog/hybrid-quantum-systems-atomic-magnetometry-sensing)
41. [https://quantumzeitgeist.com/hybrid-quantum-systems-bridging-classical-and-quantum-worlds/](https://quantumzeitgeist.com/hybrid-quantum-systems-bridging-classical-and-quantum-worlds/)
42. [https://www.londondaily.news/quantum-computing-architecture/](https://www.londondaily.news/quantum-computing-architecture/)
43. [https://dl.acm.org/doi/10.1145/3587135.3592190](https://dl.acm.org/doi/10.1145/3587135.3592190)
44. [https://pure.strath.ac.uk/ws/portalfiles/portal/122013009/Chu_etal_APL_2021_Hybrid_quantum_devices_guest_editorial.pdf](https://pure.strath.ac.uk/ws/portalfiles/portal/122013009/Chu_etal_APL_2021_Hybrid_quantum_devices_guest_editorial.pdf)
45. [https://www.quantware.com/press/quantrolox-and-quantware-introduce-quantum-edge-development-kit-for-contralto-a](https://www.quantware.com/press/quantrolox-and-quantware-introduce-quantum-edge-development-kit-for-contralto-a)
46. [https://www.pnas.org/doi/10.1073/pnas.1419326112](https://www.pnas.org/doi/10.1073/pnas.1419326112)
47. [https://www.spinquanta.com/news-detail/quantum-computing-as-a-service](https://www.spinquanta.com/news-detail/quantum-computing-as-a-service)
48. [https://dsg.tuwien.ac.at/~sd/papers/QSW_2023_A_Furutanpey.pdf](https://dsg.tuwien.ac.at/~sd/papers/QSW_2023_A_Furutanpey.pdf)
49. [https://solid.phys.ethz.ch/research/hybrid-quantum-systems.html](https://solid.phys.ethz.ch/research/hybrid-quantum-systems.html)
50. [https://dl.acm.org/doi/pdf/10.1145/3663531.3664751](https://dl.acm.org/doi/pdf/10.1145/3663531.3664751)
51. [https://arxiv.org/html/2411.10487v1](https://arxiv.org/html/2411.10487v1)
52. [https://en.wikipedia.org/wiki/Quantum_optimization_algorithms](https://en.wikipedia.org/wiki/Quantum_optimization_algorithms)
53. [https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4502654](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4502654)
54. [https://arxiv.org/abs/2312.02279](https://arxiv.org/abs/2312.02279)
55. [https://www.sciencedaily.com/releases/2018/01/180131144339.htm](https://www.sciencedaily.com/releases/2018/01/180131144339.htm)
56. [https://quantumzeitgeist.com/quantum-computing-for-energy-optimization-cutting-edge-innovations/](https://quantumzeitgeist.com/quantum-computing-for-energy-optimization-cutting-edge-innovations/)
57. [https://open.hpi.de/courses/qc-optimization2023](https://open.hpi.de/courses/qc-optimization2023)
58. [https://www.etsi.org/technologies/quantum-safe-cryptography](https://www.etsi.org/technologies/quantum-safe-cryptography)
59. [https://quantrolox.com/quantum-edge/](https://quantrolox.com/quantum-edge/)
60. [https://milvus.io/ai-quick-reference/what-are-quantum-algorithms-for-optimization-and-how-do-they-work](https://milvus.io/ai-quick-reference/what-are-quantum-algorithms-for-optimization-and-how-do-they-work)
61. [https://www.fortinet.com/de/resources/cyberglossary/quantum-safe-security](https://www.fortinet.com/de/resources/cyberglossary/quantum-safe-security)
62. [https://simplynuc.com/blog/quantum-computing-and-edge-computing/](https://simplynuc.com/blog/quantum-computing-and-edge-computing/)
63. [https://link.aps.org/doi/10.1103/PRXQuantum.5.020327](https://link.aps.org/doi/10.1103/PRXQuantum.5.020327)
64. [https://ora.ox.ac.uk/objects/uuid:8309d4e8-5f4c-4e86-9381-fcaf2f6626f1/files/m475e807cc0fb7863f201eb294bfb0948](https://ora.ox.ac.uk/objects/uuid:8309d4e8-5f4c-4e86-9381-fcaf2f6626f1/files/m475e807cc0fb7863f201eb294bfb0948)
65. [https://www.dwavequantum.com/learn/featured-applications/?page=13](https://www.dwavequantum.com/learn/featured-applications/?page=13)
66. [https://journals.aps.org/prxquantum/abstract/10.1103/PRXQuantum.5.020327](https://journals.aps.org/prxquantum/abstract/10.1103/PRXQuantum.5.020327)
67. [https://blogs.cisco.com/security/understanding-the-quantum-threat-to-network-security](https://blogs.cisco.com/security/understanding-the-quantum-threat-to-network-security)
68. [https://dl.acm.org/doi/10.1145/3678184](https://dl.acm.org/doi/10.1145/3678184)
69. [https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5015789](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5015789)
70. [https://www.idquantique.com/quantum-safe-security/overview/](https://www.idquantique.com/quantum-safe-security/overview/)

# Computing Inside Mobile Communication Networks – What It Means and Where It Happens

Mobile networks no longer behave like “dumb pipes.” They now embed general-purpose and specialized processors that execute application logic, AI inference, security functions or traffic optimisation **while data are in transit**, a trend often called _computing in communication networks_ (CiCN) or _compute-in-network_.

## 1 Definition

Computing in a communication (mobile) network is the practice of **placing cloud-style processing capability inside the network fabric itself**—from the radio site to the transport layer and core—so that packets can be transformed, analysed or acted on without first travelling to a distant data-centre. It represents a shift from the traditional _store-and-forward_ model to a _compute-and-forward_ paradigm[1](https://shop.elsevier.com/books/computing-in-communication-networks/fitzek/978-0-12-820488-7).

Key characteristics

- Programmable servers or chips sit **along the data path** rather than only at endpoints.
    
- Functions run as virtual machines, containers or data-plane programs.
    
- Typical goals: millisecond latency, traffic off-load, energy savings, privacy, real-time intelligence.
    

## 2 Main Places Where Computation Occurs

|Layer|Typical Physical Location|Latency to User|Example Tasks|Representative Standards / Tech|Sources|
|---|---|---|---|---|---|
|0. On-device|Smartphone / IoT sensor|1–5 ms (local)|AR rendering, sensor fusion, encryption|Mobile chipsets with NPUs|—|
|1. **RAN Edge (MEC)**|MEC server collocated with gNB/eNB cabinet or at distributed unit (DU) site|5–20 ms|Video analytics, V2X safety messages, AR/VR buffering|ETSI MEC, 3GPP SA6[2](https://en.wikipedia.org/wiki/Multi-access_edge_computing)[3](https://portal.etsi.org/portals/0/tbpages/mec/docs/mobile-edge_computing_-_introductory_technical_white_paper_v1%2018-09-14.pdf)||
|2. Transport / Aggregation Edge|Metro PoP, fronthaul/backhaul aggregation router, CU site|10–40 ms|CDN cache, AI model serving, network slicing control|SDN/NFV on COTS servers[4](https://ris.utwente.nl/ws/portalfiles/portal/5353307/MCN_FIA2013_LNCS.pdf)||
|3. **In-Network Devices**|Programmable switches, SmartNICs, FPGA-based base-band units inside RAN or IP routers|<1 ms hop delay|Telemetry, load balancing, header compression, map-reduce pre-filter, ML inference on flows|P4, Tofino, eBPF/XDP[5](https://www.sigarch.org/in-network-computing-draft/)[6](https://www.ike-kunze.de/research/in-network-computing/)||
|4. Cloud Core|Regional or national telco cloud, 5GC UPF, data-centre|40–100 ms|Massive data analytics, network-function virtualisation (AMF, SMF), billing|Kubernetes, OpenStack, O-RAN O-Cloud[4](https://ris.utwente.nl/ws/portalfiles/portal/5353307/MCN_FIA2013_LNCS.pdf)||
|5. Public / Hyperscale Cloud|Internet data-centre|80 ms–1 s|Big-data batch jobs, training of AI models|AWS Wavelength, Azure MEC|—|

## 3 How the Pieces Fit Together

1. **User Equipment (UE)** may pre-process data (e.g., edge AI on a phone).
    
2. **Multi-access Edge Computing (MEC)** servers integrated at or near base stations host latency-critical micro-services—e.g., AR frame prediction or local break-out of traffic to nearby content servers[7](http://arxiv.org/pdf/1702.05309.pdf)[2](https://en.wikipedia.org/wiki/Multi-access_edge_computing).
    
3. **In-network computing** lets the RAN switch or a SmartNIC execute line-rate logic such as counting packets, filtering video frames, or even running inference models, saving back-haul bandwidth and server CPU cycles[5](https://www.sigarch.org/in-network-computing-draft/)[6](https://www.ike-kunze.de/research/in-network-computing/).
    
4. **Virtualised core functions** (UPF, AMF, gNodeB CU) run on telco clouds using NFV; they sit one to a few network hops deeper but still within the operator domain[4](https://ris.utwente.nl/ws/portalfiles/portal/5353307/MCN_FIA2013_LNCS.pdf).
    
5. Heavy workloads that are less delay-sensitive continue to live in regional or public clouds.
    

The result is a **computing continuum** spanning UE → RAN edge → transport edge → core → public cloud, orchestrated by SDN/NFV controllers and often exposed to applications via APIs (e.g., ETSI MEC’s Radio Network Information Service).

## 4 Why Put Computing Inside the Network?

- **Ultra-low latency:** critical for tactile Internet, cloud gaming, XR and connected vehicles; every 10 km of fibre adds ≈50 µs one-way delay.
    
- **Bandwidth savings:** preprocessing or aggregation near the source drops redundant traffic (e.g., local video transcoding or IoT data summarisation)[8](https://www.nokia.com/bell-labs/publications-and-media/publications/architectures-for-coded-mobile-edge-computing/).
    
- **Energy & cost efficiency:** one programmable switch can replace racks of x86 servers for certain packet-level tasks[9](https://azure.microsoft.com/en-us/blog/unlocking-the-potential-of-in-network-computing-for-telecommunication-workloads/)[6](https://www.ike-kunze.de/research/in-network-computing/).
    
- **Security & privacy:** data can be anonymised or inspected close to origin, limiting exposure[3](https://portal.etsi.org/portals/0/tbpages/mec/docs/mobile-edge_computing_-_introductory_technical_white_paper_v1%2018-09-14.pdf).
    
- **Reliability at scale:** distributed computation avoids single cloud bottlenecks and meets 5G/6G availability targets.
    

## 5 Technology Building Blocks

1. **Virtualisation & Containers (NFV/K8s):** deploy network functions and third-party apps on COTS edge servers[4](https://ris.utwente.nl/ws/portalfiles/portal/5353307/MCN_FIA2013_LNCS.pdf).
    
2. **Programmable Data Planes (P4, eBPF, SmartNICs):** realise in-network algorithms at line-rate[5](https://www.sigarch.org/in-network-computing-draft/).
    
3. **Lattice-based _Compute-and-Forward_ codes:** relays compute linear combinations of radio signals, boosting spectral efficiency in dense topologies[10](https://www.numberanalytics.com/blog/deep-dive-into-compute-and-forward)[11](https://oaktrust.library.tamu.edu/bitstream/handle/1969.1/173584/WANG-DISSERTATION-2018.pdf;jsessionid=6934DBD9BD619C1FA7D3668E2D2208BC?sequence=1).
    
4. **Network Slicing:** logical isolation of compute, storage, and radio resources for vertical applications[1](https://shop.elsevier.com/books/computing-in-communication-networks/fitzek/978-0-12-820488-7).
    
5. **AI/ML Accelerators:** GPUs, NPUs or FPGAs embedded in edge nodes for real-time inference.
    

## 6 Take-away

**Computing in communication networks** is the strategic embedding of processing resources throughout the mobile network—from the handset to programmable switches and MEC servers. It physically _takes place wherever it can most effectively meet the delay, bandwidth and energy constraints of the application_, leading to a layered continuum of on-device, RAN-edge, in-network, core-cloud and public-cloud compute locations that work together to deliver 5G/6G services.

1. [https://shop.elsevier.com/books/computing-in-communication-networks/fitzek/978-0-12-820488-7](https://shop.elsevier.com/books/computing-in-communication-networks/fitzek/978-0-12-820488-7)
2. [https://en.wikipedia.org/wiki/Multi-access_edge_computing](https://en.wikipedia.org/wiki/Multi-access_edge_computing)
3. [https://portal.etsi.org/portals/0/tbpages/mec/docs/mobile-edge_computing_-_introductory_technical_white_paper_v1%2018-09-14.pdf](https://portal.etsi.org/portals/0/tbpages/mec/docs/mobile-edge_computing_-_introductory_technical_white_paper_v1%2018-09-14.pdf)
4. [https://ris.utwente.nl/ws/portalfiles/portal/5353307/MCN_FIA2013_LNCS.pdf](https://ris.utwente.nl/ws/portalfiles/portal/5353307/MCN_FIA2013_LNCS.pdf)
5. [https://www.sigarch.org/in-network-computing-draft/](https://www.sigarch.org/in-network-computing-draft/)
6. [https://www.ike-kunze.de/research/in-network-computing/](https://www.ike-kunze.de/research/in-network-computing/)
7. [http://arxiv.org/pdf/1702.05309.pdf](http://arxiv.org/pdf/1702.05309.pdf)
8. [https://www.nokia.com/bell-labs/publications-and-media/publications/architectures-for-coded-mobile-edge-computing/](https://www.nokia.com/bell-labs/publications-and-media/publications/architectures-for-coded-mobile-edge-computing/)
9. [https://azure.microsoft.com/en-us/blog/unlocking-the-potential-of-in-network-computing-for-telecommunication-workloads/](https://azure.microsoft.com/en-us/blog/unlocking-the-potential-of-in-network-computing-for-telecommunication-workloads/)
10. [https://www.numberanalytics.com/blog/deep-dive-into-compute-and-forward](https://www.numberanalytics.com/blog/deep-dive-into-compute-and-forward)
11. [https://oaktrust.library.tamu.edu/bitstream/handle/1969.1/173584/WANG-DISSERTATION-2018.pdf;jsessionid=6934DBD9BD619C1FA7D3668E2D2208BC?sequence=1](https://oaktrust.library.tamu.edu/bitstream/handle/1969.1/173584/WANG-DISSERTATION-2018.pdf;jsessionid=6934DBD9BD619C1FA7D3668E2D2208BC?sequence=1)
12. [https://people.cs.vt.edu/tilevich/papers/FMEC2017.pdf](https://people.cs.vt.edu/tilevich/papers/FMEC2017.pdf)
13. [https://arxiv.org/html/2312.00740v1](https://arxiv.org/html/2312.00740v1)
14. [https://www.politesi.polimi.it/handle/10589/203739](https://www.politesi.polimi.it/handle/10589/203739)
15. [https://uwaterloo.ca/scholar/sites/ca.scholar/files/sshen/files/zhang2024com.pdf](https://uwaterloo.ca/scholar/sites/ca.scholar/files/sshen/files/zhang2024com.pdf)
16. [https://business.columbia.edu/sites/default/files-efs/pubfiles/4834/Chan_Network_Assisted.pdf](https://business.columbia.edu/sites/default/files-efs/pubfiles/4834/Chan_Network_Assisted.pdf)
17. [http://arxiv.org/pdf/1702.05309v1/1000.pdf](http://arxiv.org/pdf/1702.05309v1/1000.pdf)
18. [https://web.stanford.edu/~rezab/dao/notes/L12/cme323_lec12.pdf](https://web.stanford.edu/~rezab/dao/notes/L12/cme323_lec12.pdf)
19. [https://www.educate.elsevier.com/book/details/9780128204887](https://www.educate.elsevier.com/book/details/9780128204887)
20. [https://groups.csail.mit.edu/tds/papers/Gilbert/disc04.pdf](https://groups.csail.mit.edu/tds/papers/Gilbert/disc04.pdf)
21. [https://en.wikipedia.org/wiki/Mobile_edge_computing](https://en.wikipedia.org/wiki/Mobile_edge_computing)
22. [https://en.wikiversity.org/wiki/Computer_Communications](https://en.wikiversity.org/wiki/Computer_Communications)
23. [https://www.5gamericas.org/wp-content/uploads/2019/07/Understanding_Information_Centric_Networking_and_Mobile_Edge_Computing.pdf](https://www.5gamericas.org/wp-content/uploads/2019/07/Understanding_Information_Centric_Networking_and_Mobile_Edge_Computing.pdf)
24. [https://cn.ifn.et.tu-dresden.de/compcombook/](https://cn.ifn.et.tu-dresden.de/compcombook/)
25. [https://www.comp.nus.edu.sg/~gilbert/pubs/VMN-disc.pdf](https://www.comp.nus.edu.sg/~gilbert/pubs/VMN-disc.pdf)
26. [http://arxiv.org/pdf/2407.12558.pdf](http://arxiv.org/pdf/2407.12558.pdf)
27. [https://www.ce.cit.tum.de/hndss/teaching/ss-24/network-coding-inhn0010/](https://www.ce.cit.tum.de/hndss/teaching/ss-24/network-coding-inhn0010/)
28. [https://www.siam.org/publications/siam-news/articles/siam-task-force-anticipates-future-directions-of-computational-science/](https://www.siam.org/publications/siam-news/articles/siam-task-force-anticipates-future-directions-of-computational-science/)
29. [https://en.wikipedia.org/wiki/Linear_network_coding](https://en.wikipedia.org/wiki/Linear_network_coding)
30. [https://arxiv.org/pdf/2312.00303.pdf](https://arxiv.org/pdf/2312.00303.pdf)
31. [https://en.wikipedia.org/wiki/Network_coding](https://en.wikipedia.org/wiki/Network_coding)
32. [https://people.eecs.berkeley.edu/~ngoela/MultiReceiverFunctionComputation_WebVersion_November2012.pdf](https://people.eecs.berkeley.edu/~ngoela/MultiReceiverFunctionComputation_WebVersion_November2012.pdf)
33. [https://note.com/helga_tech_news/n/n3418b90ffbf3](https://note.com/helga_tech_news/n/n3418b90ffbf3)
34. [https://cloud.tencent.com/developer/article/2332149](https://cloud.tencent.com/developer/article/2332149)
35. [http://web.eng.ucsd.edu/~massimo/Papers_files/networkcodingforcomp2001.pdf](http://web.eng.ucsd.edu/~massimo/Papers_files/networkcodingforcomp2001.pdf)
36. [https://eng.ox.ac.uk/computing/projects/in-network-computing/](https://eng.ox.ac.uk/computing/projects/in-network-computing/)
37. [https://arxiv.org/abs/2003.02695](https://arxiv.org/abs/2003.02695)
38. [https://ac.informatik.uni-freiburg.de/teaching/ss_18/netalg/LectureNotes/chapter12.pdf](https://ac.informatik.uni-freiburg.de/teaching/ss_18/netalg/LectureNotes/chapter12.pdf)
39. [https://phoenixnap.com/glossary/network-computing](https://phoenixnap.com/glossary/network-computing)
40. [https://arxiv.org/abs/2005.04592](https://arxiv.org/abs/2005.04592)

### **# Scope/Focus of this paper**  
If I understand correctly, you're proposing quantum-assisted trustworthiness for goal-oriented semantic communication—is that right? I believe this is a very promising topic, and trustworthiness has always been one of the most important priorities for Deutsche Telekom.

### **# Trustworthiness Management**  
Regarding the open questions raised at the beginning of the paper — _“How to define trustworthiness level? And how to monitor__/sense_ _it?”_ — here are some inputs from my side:

### **1) Core Trustworthiness Dimensions**_(Based on ISO/IEC 25010 and NIST SP 800-160)_

- **ISO/IEC 25010****: [Link](https://blog.pacificcert.com/iso-25010-software-quality-requirements-in-the-usa/?utm_source=chatgpt.com)**
- **NIST SP 800-160 Vol. 1****: [Link](https://csrc.nist.gov/pubs/sp/800/160/v1/r1/final?utm_source=chatgpt.com)**

|**Dimension**|**Description**|
|---|---|
|Reliability|Does the entity perform consistently over time?|
|Integrity|Are the data and systems free from unauthorized changes?|
|Security|Is it protected from cyber, physical, and quantum threats?|
|Availability|Is it operational and accessible when needed?|
|Authenticity|Can the identity or source of the entity be verified?|
|Accountability|Can actions be traced to responsible entities or users?|
|Resilience|Can it recover from faults, failures, or attacks?|
|Privacy Compliance|Is personal data handled according to relevant regulations?|

**2) Scoring Model – Quantifying Trustworthiness**

The scoring model provides a structured approach to quantify the trustworthiness of an entity (e.g., device, application, network function, or service). It can assign numeric values as weight to multiple trust-related attributes, enabling consistent and comparable trust assessments.

**3) Real-Time Trust Monitoring**

Ongoing monitoring of trustworthiness is crucial to ensure that network systems and communication endpoints remain trustworthy throughout their lifecycle. Key mechanisms include:

- **Telemetry & Behavioral Analysis**  
    Collect real-time data such as logs, traffic flows, uptime metrics, and behavioral anomalies to identify potential trust degradation.
- **Secure Attestation & Trust Anchors**Leverage hardware-based modules like TPMs or TEEs for cryptographic attestation and tamper detection. In sensitive settings, quantum-secure methods (e.g., QKD or post-quantum signatures) may strengthen inherent eavesdropping detection and integrity assurance.
- **Event-Driven Trust Scoring**  
    Continuously adjust trust levels based on telemetry and attestation outcomes. Positive behavior increases trust scores, while anomalies or failures decrease them, triggering policy-based actions.
- **Centralized Trust Dashboards**  
    Provide real-time visibility of trust status across the network. Dashboards show alerts, trends, and recommended mitigations, enabling proactive trust and risk management.

**Discussion:** the classical trust management in telco world is organized in a centralized way, how about distributed or even decentralized trust management models for Future Mobile Core(FMC)? For example, **Blockchain****,** Self-Sovereign Identity (SSI), Web of Trust (WoT) Models, Federated Trust, or Zero Trust Concept(NIST’s SP 800-207).

---

**# Comments on Figure 2**

- I didn’t get the title of the figure.
- The term **“Quantum Function Secret Sharing”** may be recognized in academic circles, but it is still unfamiliar to most industry practitioners. A short explanation would help industrial readers.
- Figure 2 currently highlights only quantum-related aspects (e.g., security and computing), but does not explain how it ties into goal-oriented **semantic communication**.
- It is also unclear how the **FMC** fits into the architecture diagram and how the Q-Components interact with FMC.

# **Quantum-Classical Network**

From the **Future Mobile Core (FMC)** perspective, the described approach to integrating quantum capabilities into 6G architecture can be understood as follows:

**1****)** **Role of FMC in Hybrid Quantum-Classical Integration**

The **Future Mobile Core** acts as the central control and service plane of the 6G network. It must evolve to accommodate quantum capabilities by:

- **Orchestrating hybrid resources** (classical and quantum) at the service layer.
- Supporting **flexible service-based architecture (SBA)** that allows dynamic deployment of quantum-enabled functions.
- Providing interfaces for **secure, low-latency access** to external quantum resources (e.g., quantum key distribution nodes, quantum compute services).

**2****)** **FMC-Enabled Quantum Functions**

Quantum services may not reside _within_ the core itself but will be **accessible through FMC as service-based extensions**, such as:

- **Quantum-Safe Security Functions**: FMC can route signaling/data traffic through quantum-safe encryption modules (QKD or PQC).
- **Quantum Resource Coordination**: FMC could interact with a **Quantum Resource Function (QRF)** responsible for managing quantum communication endpoints and compute tasks.
- **Quantum-Sensing-Aware Mobility Management**: If quantum sensors support environmental or context-aware services, FMC can integrate their outputs into mobility or session management logic.

**3****)** **Architectural Considerations**

From an FMC standpoint, the hybrid quantum–classical integration implies:

|**FMC Aspect**|**Quantum-Integration Implication**|
|---|---|
|**Service-Based Architecture (SBA)**|Modular functions like AUSF, AMF, and SMF could expose quantum-enhanced interfaces|
|**Security Architecture**|Integration with QKD nodes, quantum-resilient algorithms, and attestation services|
|**Edge Support**|Quantum sensing and computation could be accessed via MEC platforms at the edge|
|**Network Exposure Function (NEF)**|Provide APIs to external quantum services or quantum control planes|
|**Policy and Charging**|Adapt policies for quantum-assisted trust levels and secure resource consumption|

**4)** **Its impact on** **FMC**

- Protocol adaptation (PQC support)
- Cryptographic agility (QKD, PQC, hybrid)
- Integration with quantum key infrastructures
- Expanded trust models
- Rethinking latency, reliability, and resilience, etc.,  in hybrid quantum-classic networks

|**Factor**|**Classical Core Assumption**|**Quantum-Classical Reality**|**FMC Impact**|
|---|---|---|---|
|Latency|Millisecond-level key setup|Delayed/unpredictable quantum key delivery|Pre-buffering, hybrid crypto, tolerant control loops|
|Reliability|Robust with retries and redundancy|Fragile quantum links prone to loss|Fallback key methods, quality-aware routing|
|Resilience|Backup links, geo-redundancy|Must withstand cryptographic or trust-layer failure|Hybrid security models, cross-layer resilience|

**#** **Challenges in the Ongoing 6G Discussions on Future Mobile Core (FMC) in the Telecom Industry**

New Device + New Service + New Architecture + New Technology -> New Core

1. Seamless End-to-End Services  
    How can we extend our portfolio so that we can consistently provide end-to-end services including elements from other technology domains (e.g. goal-oriented semantic communication, quantum compute, new trust models,….)? à Idee: consistently manage and orchestrate multiple elements from different technology domains
2. On-Demand Services  
    How can we simplify the lifecycle management of resources coming from different technology domains to ease the orchestration of e2e services? à Idea: dynamically support customer demand via harmonized lifecycle management of elements
3. API for UE  
    How can we expose these new capabilities towards the customer in a simple manner? à Idea: intent driven management of end-to-end services via API (including APIs for 3rd parties)
4. Service-Federation  
    How can we easily and dynamically embed 3rd party services via interfaces on the control plane and dataplane? à Idea: dynamic integration of services and resources from 3rd parties into end-to-end service
5. Distributed Trust  
    How can all service providers interact in a trusted manner? à Idea:  leverage distributed trust management plane to support trusted interactions with 3rd parties


---
Core: 
https://infohub.delltechnologies.com/en-us/p/the-5g-core-network-demystified/

![[The 5G Core Network Demystified _.pdf]]

https://www.cisco.com/c/en/us/solutions/collateral/service-provider/networking/nonterrestrial-networks-satellite-market-wp.html

https://www.telecomtrainer.com/
https://medium.com/@danilo.j.granados/from-theory-to-practice-implementing-a-5g-core-network-using-open-source-tools-4a6afe1f708b


----
### Writing the proposed framework 

// background talks about 

 - its a radical transition ends with 5G core SBA - Suitable for computing and storing and reduces latency 
but the quantification of trustworthiness is a topic of discussion. 
As we move towards the goal-oriented communication with the semantic level of details in the information 
- Provide a hybrid mobile core architecture (quantum classical that enhance the level of trustworthiness )
- This diagram presents a revolutionary **quantum-enhanced mobile core network architecture** that fundamentally transforms the traditional approach to cellular network design by integrating quantum technologies to enhance **security, resilience, and reliability**
- The design incorporates **quantum circuits alongside classical circuits** to create a hybrid quantum-classical infrastructure that can leverage quantum computing's inherent advantages for **cryptographic security and optimization**
- The proposed architecture introduces groundbreaking features including **quantum interfaces, quantum sessions, and Quantum Function Secret Sharing (QFSS)**[](https://www.themoonlight.io/en/review/quantum-function-secret-sharing) capabilities that enable unprecedented levels of data protection and network integrity
- that provide decentralized authentication and secure communication channels, addressing the fundamental challenge of establishing trustworthiness in distributed mobile networks without relying on centralized authorities
- The architecture enhances **network resilience** through distributed quantum-enabled edge computing capabilities and **intelligent orchestration systems** that can dynamically adapt to threats and network changes[](https://www.ngmn.org/wp-content/uploads/NGMN_6G_Trustworthiness.pdf)[](https://www.ngmn.org/wp-content/uploads/250218_Network_Architecture_Evolution_towards_6G_V1.0.pdf). The integration of **photonic circuits and error control mechanisms** ensures robust quantum state preservation and reliable data transmission even in challenging mobile environments[](https://bura.brunel.ac.uk/bitstream/2438/23766/4/FullText.pdf)[](https://en.wikipedia.org/wiki/Quantum_network). This forward-looking design positions mobile networks to handle the **complex security challenges of 6G and beyond**[](https://www.ngmn.org/wp-content/uploads/NGMN_6G_Trustworthiness.pdf)[](https://arxiv.org/pdf/2504.17133.pdf), where quantum-resistant cryptography and quantum-enhanced network optimization will be essential for maintaining network trustworthiness against both classical and quantum-based attacks

# Quantum Capabilities and Trustworthiness Dimensions in Future Mobile Core Architecture

Based on the attached figure showing the 5G/6G network architecture and the quantum capabilities that could enhance trustworthiness, **quantum technologies fundamentally transform the trust model across multiple dimensions by introducing quantum-secured interfaces, quantum-enhanced authentication mechanisms, and quantum-resilient cryptographic protocols** that address the core trustworthiness vulnerabilities identified in today's 5G networks.

The quantum capabilities illustrated in this future mobile core architecture achieve trustworthiness through **three primary dimensions**: **quantum-secured authentication and key management**, **quantum-enhanced network function isolation and integrity verification**, and **quantum-resistant communication protocols**[](https://arxiv.org/html/2504.17133v1)[](https://dl.acm.org/doi/pdf/10.1145/3659997.3660033). The **Quantum Key Distribution (QKD) mechanisms** provide **information-theoretically secure key exchange** between critical network functions like the AMF, SMF, and UPF, ensuring that **authentication vectors cannot be compromised even by quantum adversaries**[](https://arxiv.org/pdf/2404.10602v1.pdf)[](https://core.ac.uk/download/480164625.pdf). This addresses the fundamental 5G-AKA protocol vulnerabilities where identity mis-binding and replay attacks currently undermine network trustworthiness.

The architecture incorporates **quantum-enhanced service-based interfaces** that replace the current HTTP/2 API communications with **quantum-secured channels** utilizing **Post-Quantum Cryptography (PQC) algorithms** integrated with QKD for hybrid security[](https://dl.acm.org/doi/pdf/10.1145/3659997.3660033)[](http://arxiv.org/pdf/2404.10602.pdf). This dual approach ensures that **network function discovery, registration, and inter-function communication** between elements like the NRF, NSSF, UDM, and AUSF maintain **cryptographic security against both classical and quantum attacks**[](https://cpl.thalesgroup.com/blog/encryption/preparing-5g-networks-for-quantum-era)[](https://arxiv.org/pdf/2504.17133.pdf). The quantum capabilities enable **tamper-evident communication channels** that can detect eavesdropping attempts in real-time, providing **immediate trust verification** across the network fabric[](https://aerospace.org/sites/default/files/2020-07/Touch-Gordon_QKD_20200715.pdf)[](https://www.itu.int/dms_pub/itu-t/opb/tut/T-TUT-QKD-2020-1-PDF-E.pdf).

Furthermore, the quantum-enhanced architecture addresses **network slicing trustworthiness** by implementing **quantum-assisted slice isolation mechanisms** that prevent cross-contamination between network slices[](https://www.huawei.com/en/huaweitech/future-technologies/6g-native-trustworthiness)[](https://dl.ifip.org/db/conf/ondm2024/ondm2024/1570994563.pdf). The quantum principles ensure that **slice-specific trust boundaries** are maintained through **quantum-secured orchestration** of network functions, while **quantum error correction techniques** provide **fault-tolerant communication** that enhances overall network resilience[](https://arxiv.org/pdf/2504.17133.pdf)[](http://arxiv.org/pdf/2404.16463.pdf). This creates a **native trustworthiness framework** where quantum capabilities serve as the foundation for **adaptive security policies**, **real-time threat detection**, and **autonomous trust management** that can dynamically respond to emerging security challenges without manual intervention



The radical transition into a service based architecture in 5G core has provided enhancements to various applications but the  trustworthiness challenges span both technical vulnerabilities and regulatory concerns.  Underlining the foundational authentication system in 5G networks contains critical security flaws that undermine network trustworthiness. Research has revealed that the **5G Authentication and Key Agreement (5G-AKA) protocol suffers from identity misbinding vulnerabilities** that allow malicious actors to impersonate legitimate users. The communication channels between the Authentication Server Function (AUSF) and the Authentication Repository and Processing Function (ARPF).  This fundamental issue emerges from the lack of inadequate cross-authentication of network notes. The microservices in the adopted SBA 5G core architecture introduced significant security risks. 
However, the 
We see the  dimensions of trustworthiness could be achieved with quantum capabilities  by introducing quantum-secured interfaces, quantum-enhanced authentication mechanisms, and quantum-resilient cryptographic protocols that address the core trustworthiness vulnerabilities identified in today's 5G networks. tranfer the current MEC enabled core architure towards a thorough quantum coupled architecture is a step by step process. he quantum capabilities illustrated in this future mobile core architecture achieve trustworthiness through **three primary dimensions**: **quantum-secured authentication and key management**, **quantum-enhanced network function isolation and integrity verification**, and **quantum-resistant communication protocols. The **Quantum Key Distribution (QKD) mechanisms** provide **information-theoretically secure key exchange** between critical network functions like the AMF, SMF, and UPF, ensuring that **authentication vectors cannot be compromised even by quantum adversaries
This addresses the fundamental 5G-AKA protocol vulnerabilities where identity mis-binding and replay attacks currently undermine network trustworthiness.


**quantum technologies fundamentally transform the trust model across multiple dimensions




The quantum capabilities illustrated in this future mobile core architecture achieve trustworthiness through **three primary dimensions**: **quantum-secured authentication and key management**, **quantum-enhanced network function isolation and integrity verification**, and **quantum-resistant communication protocols**[](https://arxiv.org/html/2504.17133v1)[](https://dl.acm.org/doi/pdf/10.1145/3659997.3660033). The **Quantum Key Distribution (QKD) mechanisms** provide **information-theoretically secure key exchange** between critical network functions like the AMF, SMF, and UPF, ensuring that **authentication vectors cannot be compromised even by quantum adversaries**[](https://arxiv.org/pdf/2404.10602v1.pdf)[](https://core.ac.uk/download/480164625.pdf). 

The architecture incorporates **quantum-enhanced service-based interfaces** that replace the current HTTP/2 API communications with **quantum-secured channels** utilizing **Post-Quantum Cryptography (PQC) algorithms** integrated with QKD for hybrid security[](https://dl.acm.org/doi/pdf/10.1145/3659997.3660033)[](http://arxiv.org/pdf/2404.10602.pdf). This dual approach ensures that **network function discovery, registration, and inter-function communication** between elements like the NRF, NSSF, UDM, and AUSF maintain **cryptographic security against both classical and quantum attacks**[](https://cpl.thalesgroup.com/blog/encryption/preparing-5g-networks-for-quantum-era)[](https://arxiv.org/pdf/2504.17133.pdf). The quantum capabilities enable **tamper-evident communication channels** that can detect eavesdropping attempts in real-time, providing **immediate trust verification** across the network fabric[](https://aerospace.org/sites/default/files/2020-07/Touch-Gordon_QKD_20200715.pdf)[](https://www.itu.int/dms_pub/itu-t/opb/tut/T-TUT-QKD-2020-1-PDF-E.pdf).
This creates a **native trustworthiness framework** where quantum capabilities serve as the foundation for **adaptive security policies**, **real-time threat detection**, and **autonomous trust management** that can dynamically respond to emerging security challenges without manual intervention



To overcome the trustworthiness limitations of current 5G networks, quantum technologies offer a transformative path forward. By integrating quantum-secured interfaces, quantum-enhanced authentication mechanisms, and quantum-resilient cryptographic protocols, we can directly address the core vulnerabilities exposed in today’s 5G architecture. Transitioning from the current Multi-access Edge Computing (MEC)-enabled 5G core to a quantum-integrated architecture is a gradual yet crucial process. The envisioned quantum-coupled mobile core enhances trustworthiness across **three key dimensions**: **quantum-secured authentication and key management**, **quantum-enhanced isolation and integrity verification of network functions**, and **quantum-resistant communication protocols**. Central to this architecture is the use of **Quantum Key Distribution (QKD)**, which enables **information-theoretically secure key exchange** between critical functions such as the Access and Mobility Management Function (AMF), Session Management Function (SMF), and User Plane Function (UPF). This ensures that authentication vectors remain immune to compromise—even in the presence of quantum-capable adversaries. Notably, these quantum enhancements directly mitigate the identity misbinding and replay attack vulnerabilities inherent in the 5G-AKA protocol, marking a significant leap toward a truly trustworthy mobile network infrastructure

Quantum Function Secret Sharing (QFSS) and a new class of **Hybrid Quantum-Classical Functions (HQCF)** together offer a cohesive pathway for embedding quantum-grade security into the classical 5G/6G core without wholesale architectural upheaval. QFSS distributes the _function_ that computes sensitive values—such as the 5G-AKA authentication vector—into verifiably private quantum shares held by multiple core network functions (e.g., AMF, SMF, UPF). No single entity ever possesses the complete cryptographic primitive, so even if one slice is compromised, an adversary gains no usable information[](https://arxiv.org/html/2501.18928v1)[](https://drops.dagstuhl.de/opus/volltexte/2023/18314/pdf/LIPIcs-TQC-2023-4.pdf). HQCFs, meanwhile, act as protocol “quilting” elements that translate quantum-secure operations (QFSS-based secret reconstruction, QKD key refresh, post-quantum signatures) into the service-based interfaces and RESTful APIs that dominate today’s cloud-native cores[](https://milvus.io/ai-quick-reference/what-are-hybrid-quantumclassical-algorithms)[](https://www.etsi.org/deliver/etsi_gs/QKD/001_099/014/01.01.01_60/gs_qkd014v010101p.pdf). By interposing HQCFs at strategic control-plane junctures, operators can phase-in quantum protections—starting with QFSS-secured authentication vector generation—while preserving existing orchestration pipelines, state repositories, and DevOps toolchains. In effect, HQCFs smooth the fabric between quantum and classical domains, enabling **information-theoretically secure, mis-binding-proof, and replay-resistant authentication workflows** that directly neutralize the most severe 5G-AKA trustworthiness gaps without sacrificing the agility of microservice deployment.

Quantum-secured interfaces establish **tamper-evident channels**.


Figure \ref{fig:Quantum-assisted core} highlights the Quantum-secured interfaces to establish tamper-evident channels.  Embedding the quantum key distribution via service based APIs between the network functions potentially immediately detect  any eavesdropping or message alteration. Quantum-enhanced authentication mechanisms leverage **Quantum Function Secret Sharing** to split the authentication vector computation across the network functions such as AMF for subscriber authentication and mobility signaling,  SMF guarantees that bearer setup and modification commands between the control plane and UPF are protected by information-theoretic security against both classical and quantum adversaries.The UPF’s packet-forwarding path integrity for data flow, The NRF uses QKD-backed TLS channels to securely advertise and discover service endpoints, to protect northbound API callbacks to third-party applications, guaranteeing that exposed network capabilities and telemetry data remain confidential and tamper-resistant.



between network functions (e.g., AMF, SMF, UPF) by embedding quantum key distribution directly into service-based APIs—ensuring any eavesdropping or message alteration in the figure’s hybrid quantum-classical fabric is immediately detected.  
Quantum-enhanced authentication mechanisms leverage **Quantum Function Secret Sharing** to split the authentication vector computation across multiple HQCF modules—so that, as depicted, no single core node can be compromised to impersonate a user, closing the 5G-AKA identity mis-binding and replay gaps.  
Quantum-resilient cryptographic protocols combine **post-quantum algorithms with continuous QKD key refresh**—illustrated in the diagram by interleaving classical microservices with quantum sessions—to guarantee that even future quantum adversaries cannot decrypt or tamper with control-plane and user-plane traffic, policy-enforcement APIs, the PCF ensures that dynamic QoS and charging rules are transmitted over channels that are provably secure from interception or modification.


# Quantum Key–Embedded Network Functions

**Access and Mobility Management Function (AMF):**  
The AMF integrates a Quantum Key Distribution (QKD) interface to establish tamper-evident session keys for subscriber authentication and mobility signaling, ensuring any attempt to intercept or alter UE registration messages is immediately detectable.

**Session Management Function (SMF):**  
By embedding QKD-derived symmetric keys into its session-establishment APIs, the SMF guarantees that bearer setup and modification commands between the control plane and UPF are protected by information-theoretic security against both classical and quantum adversaries.

**User Plane Function (UPF):**  
The UPF’s packet-forwarding paths leverage continuous QKD-synchronized keys for encrypting user-plane traffic, providing real-time quantum-secured confidentiality and integrity for data flows traversing the mobile core.

**Network Repository Function (NRF):**  
The NRF uses QKD-backed TLS channels to securely advertise and discover service endpoints, ensuring that quantum-secured service registrations and queries cannot be spoofed or replayed.

**Network Slice Selection Function (NSSF):**  
The NSSF embeds quantum-signed slice-selection policies, where QKD-fresh keys validate slice assignments and prevent unauthorized cross-slice access or tampering with slice parameters.

**Authentication Server Function (AUSF):**  
The AUSF distributes QKD-protected authentication vectors, utilizing quantum-resilient key shares so that no single component ever holds enough material to impersonate a subscriber or mount a replay attack.

**Unified Data Management (UDM):**  
The UDM employs QKD-derived keys to encrypt subscriber profile retrieval requests and responses, safeguarding subscription data against eavesdropping and ensuring data provenance in a quantum-secure manner.

**Policy Control Function (PCF):**  
With quantum-anchored keys embedded in its policy-enforcement APIs, the PCF ensures that dynamic QoS and charging rules are transmitted over channels that are provably secure from interception or modification.

**Network Exposure Function (NEF):**  
The NEF leverages QKD sessions to protect northbound API callbacks to third-party applications, guaranteeing that exposed network capabilities and telemetry data remain confidential and tamper-resistant.

**Charging Function (CHF):**  
The CHF integrates QKD keys into its metering and rating interfaces, ensuring that usage records and charging events are cryptographically bound by information-theoretic security against any tampering or fraud.


Figure \ref{fig: Quantum-assisted core} illustrates the integration of quantum-secured interfaces within the mobile core, designed to establish tamper-evident communication channels. By embedding Quantum Key Distribution (QKD) through service-based APIs between network functions, the architecture enables real-time detection of eavesdropping attempts and message tampering. Quantum-enhanced authentication mechanisms further strengthen this architecture by employing **Quantum Function Secret Sharing**, which distributes the computation of authentication vectors across multiple network functions. For example, the Access and Mobility Management Function (AMF) handles subscriber authentication and mobility signaling, while the Session Management Function (SMF) ensures that bearer setup and modification commands between the control plane and the User Plane Function (UPF) remain secure—even against quantum-capable adversaries. Additionally, the integrity of the UPF’s packet-forwarding path is safeguarded to ensure the trustworthiness of user data flow. The Network Repository Function (NRF) utilizes QKD-backed TLS channels to securely advertise and discover service endpoints, protecting northbound API callbacks to third-party applications. This ensures that exposed network capabilities and telemetry data remain confidential, authentic, and resistant to tampering.


between network functions (e.g., AMF, SMF, UPF) by embedding quantum key distribution directly into service-based APIs. This ensure any eavesdropping or message alteration in the figure’s hybrid quantum-classical fabric is immediately detected.  
The envisioned quantum-coupled mobile core enhances trustworthiness across three key facets: 
\begin{itemize}
    \item quantum-secured authentication and key management
    \item quantum-enhanced isolation and integrity verification of network functions
    \item quantum-resistant communication protocols
\end{itemize} 

---
22/7 
- source coding end user - for semantic communication 
- encoding is at the edge 

Controller  MANO 
Meta Data - semantic information instead of raw data - collection 
horizontal and vertical interface 

---
Paper draft last 

- Table weigh actor 
- Score from our use-case requirement (Proposed)
- Subjective - how accurate is our weigh 
- 6 network slicing capacity 
- Spider chart - semantic awareness

Quantify trustworthiness?
Image - schedule from classic to quantum 

----
Proposed methodology/research section 
1. What advancements are happing in the core for different application
2. How to ensure trustworthiness
3. <span style="color:rgb(255, 0, 0)">Trust and trust worthiness introduced at intro?</span> 
4. https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10944627


--
What are points to start from trustworthiness - from background

- In the context of mobile networks, trustworthiness refers to the ability of a system or node to
perform its intended function reliably, securely, and with integrity
- The 3GPP has incorporated trustworthiness into its standards, for example, 3GPP TS 33.501
(Release 18) [3] defines the concept of trust boundaries, where the network is divided into different trust zones, and communication between them is subject to strict security controls.
- practical feasibility of the semantic communication components within the proposed framework,
- Usecase: Semantic computing from UAVs 
- allign some points for UAV

- https://arxiv.org/pdf/2305.13887
- https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10944627
- https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10855638
- https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10944615

---
4/8 Meeting with Ming (updates and plan for submission- Target Journal)

Update fig 5 - formating scales and remove UPF 
From Quantum computing to semantic to Trustworthiness
User chooses the trustworthiness
QFSS - access by User
Quantum Setup 
Connect to tech landscape
Idea - Marketable - Small scale-  Consortium or WG- Standards - Vendors working on it as a product
 try to map sections based on the title
 Meeting tomo
---
5/8 meeting on paper structure 

Trust  - philosophical dimension 

Trustee 
Truster 
Trust models based on regulation 
HW level -> API based core - reach what is the challenges on trust here 
 assumption : All links inside core is trust worthy? - How ? What is hyper scalar -edge / cloud servers 
 Can cloud servers be within core? 
 enhance trustworthiness to users via service providers outside the core 
 What's 0 trust inside network?  (service dependencies)
 Initiation of service - from scratch evaluate the trustworthiness
 Frequency of monitoring 
 Heterogeneous  structure? Trust worthiness? 
 Native trust - when triggered globally it is assumed  / treated as 
 What is the service request here ?
 
 can we have predefined process for the processes
Trustworthiness by design 
likelihood, probability 
security , privacy 

Quantum resistance 
trustee understands sever (linking  the data) is privacy users 

baseline of resilience  (raw data) --> semantic improvement 
security and privacy concerns are probability events 
can they be graphically represented 

client only reconstruct data 
what if the server exposes one client to another 
what privacy exactly means 
what is Metadata 
what is the data  about client that is sent to 
data that used to handover to the server 
how privacy concerns impact resilience 
does safety a factor for security 
unilateral bilateral and multilateral privacy interfaces

Honest, curious, malicious graphs (QFSS blindness) 
user based privacy metrics  - I start with network node don't have privacy 
attacks and privacy concerns 
storage of user / client information 

how to defining the axis of privacy - not included in the graph 
outage due to privacy 

---
31/10 

Comments 
Guest Editor: March 2026, Future Mobile Core  
Comments to the Author:  
(There are no comments. Please check to see if comments were included as a file attachment with this e-mail or as an attachment in your Author Center.)  
  
Reviewer: 1  
  
Comments to the Author  
-This paper addresses an important and forward looking problem in semantic communication with respect to trustworthiness. Its main strength lies in providing a concrete model for balancing trustworthiness across several dimensions.  
  
-The validation of the model on a real-world, critical use case further enhances the proposed framework. The evaluation is also thorough in covering three separate performance metrics that all show positive results leveraging this model  
  
-The model is somewhat ambitious, in that several of the dimensions of trustworthiness are introduced at a high level, but may not be universally measurable or equally important. Only with time and further validation on a number of use cases, it can be further generalized and adopted widely in semantic communication.  
  
Reviewer: 2  
  
Comments to the Author  
Strengths  
1. Very well written manuscript-- technically sound, interesting topic, and forward looking.  
2. Systems-level evaluation and PoC further strengthens the claims.  
  
Weaknesses  
3. The abstract is way too long for a magazine paper, please condense it.  
4. Since the architecture proposes to extend 3GPP core NFs, a paragraph on implications for 3GPP standards within the "Proposed Framework" section would be very much appreciated, especially since this is COMSTD.  
5. The quality of Fig. 4 needs to be improved to make it magazine-worthy. E.g., the text and arrows should not overlap.  
  
Reviewer: 3  
  
Comments to the Author  
This paper introduces a trust-centric semantic-aware networking framework for UAV-assisted disaster-response scenarios, where a multidimensional Quality of Trust (QoT) profile is proposed to capture application-specific trust requirements. To strengthen privacy, integrity, and resilience, the framework integrates quantum-enhanced mechanisms such as quantum-secure communication and function secret sharing. Moreover, a proof-of-concept UAV wildfire-response testbed demonstrates that lightweight trust enforcement can effectively maintain accuracy while preserving the latency and bandwidth efficiency of edge offloading.  
While the topic is interesting, the approach is not technically sound and there are several areas where the manuscript requires significant revisions. Given the nature of the magazine, the reader needs to have multi-disciplinary knowledge to follow the manuscript. The authors are suggested to modify this paper according to the following comments:  
4) The paper positions semantic-aware networking and quantum trust as complementary enablers, but it could benefit from a clearer differentiation from prior semantic networking frameworks.  
5) The discussion of computational overhead of trust monitoring and orchestration is limited. Specifically, practical feasibility in high-load networks remains unclear.  
6) How would the proposed framework handle conflicting trust requirements across multiple simultaneous applications (e.g., privacy-critical vs. latency-critical tasks)?  
7) Can the QoT model be quantitatively benchmarked against existing trust evaluation approaches (e.g., ITU-T Y.305x standards) to demonstrate its relative benefits?  
8) Given the trusted core assumption, how would the framework adapt in a federated or multi-operator environment where the core itself may be partially untrusted?  
9) The testbed description and the proof of concept (PoC) is not solid, with some assumptions, while there are several missing points. There is no schematic of the measurement setup and the data flow, there are no PoC parameters, there is no justification of the use of the previous described sections such as QFSS, several attributes have not values or are vaguely described, e.g., what is the QoT threshold, how the core decides about the flow, where is the trust-aware/unaware mode located, what are the thresholds, how is the synchronization achieved, etc. The evaluation metrics (latency, bandwidth, semantic accuracy) are relatively high-level. More detailed metrics, such as energy consumption of UAVs, computational load on MEC nodes, or trust protocol overhead may be added. The proof-of-concept is limited to a small-scale UAV setup. How scalable is the trust-aware orchestration mechanism when extended to hundreds of UAVs and heterogeneous edge servers in real-time?  
10) A lot of acronyms are not defined or explained throughout the manuscript, e.g., ZTE, PDU. How exactly does hyperscaler work? What exactly is the trust pipe API?  
11) As this manuscript is intended for IEEE Communications Standards Magazine, it would be strengthened by a clearer alignment with ongoing standardization activities, particularly within 3GPP and ITU.  
  
Reviewer: 4  
  
Comments to the Author  
Pros:  
9. The focus on trust-centric design and semantic-aware networking with quantum integration is highly focused in the current research and standardization efforts for mobile networks.  
10. A novel framework for task orchestration in heterogeneous environments is presented by the introduction of the multidimensional Quality of Trust (QoT) profile, which extends the conventional QoS. Beyond traditional trust models, the discussion of blind quantum computing and quantum function secret sharing (QFSS) offers potential future directions.  
11. The UAV-based wildfire response testbed offers a convincing proof of viability while integrated with analytical extrapolation to encrypted and quantum-protected nodes.  
  
Cons:  
4. While QFSS and blind quantum computing have been clear reasoned for being studied, the manuscript would improve with a brief discussion on how feasible it is to deploy them in the near term. For instance, which aspects could be put into practice in the next few years, and which ones are long-term research?  
5. The connection to standardization could be clearer. A brief section that relates the proposed QoT framework to ongoing discussions in SDO(s) would increase its impact and relevance.

----
Shorten Abstract 
Add regulation 
ITU-T , Y.305x - trust and trustworthiness

3GPP and ETSI 
Standardization semantic and trustworthiness


Semantic Communication Current standards and regulation 
Semantic communication represents a fundamental paradigm shift from traditional bit-level transmission toward meaning-aware, task-oriented information exchange for 6G networks.
Today, semantic communication is considered as "application requirement" and not a base-line of the 6G network. 
Its regulatory or standardization efforts are focused for the following applications 
- Integrated Sensing and Communication (ISAC)
- Native AI/ML integration for network optimization
- Immersive communication and extended reality
- Ubiquitous connectivity
- System and operational aspects including CAPEX/OPEX reduction
3GPP focuses primarily on bit-level communication and radio access protocols with limited support for semantic metrics. 
ITU have formed a working group SG13 and  ITU-T SG13 has established liaisons with ETSI, ISO, ITU-T SG16, ITU-T SG17, ITU-T SG20, GSMA, W3C, and OMA to coordinate semantic communication standardization efforts.

With the take off of 3GPP 6G technical specifications and ETSI's semantic interoperability standards are expected to converge with the ITU-T semantic aware networking framework. [Ref 1]

**ITU-T Study Group 13 - Semantic-Aware Networking** (SAN)
ITU-T SG13, designated as the lead study group on AI/ML for future networks, has been developing comprehensive specifications for semantic-aware networking since 2023:
  **ITU-T TR.Reqts-SAN**  [Ref 2] is an informative technical report that identifies potential requirements for **semantic-aware networking (SAN)** in future networks including IMT-2020 and beyond.

**General Requirements:**  
Eight fundamental capabilities including domain-specific semantic ontology, semantic annotation, semantic interpretation, semantic translation, semantic cognition, semantic rationality discovery, and self-description/auto-correction​
**Service-Level Requirements:**  
Support for diverse services, QoS/QoE assurance, interoperability with legacy systems, and cross/intra-domain semantic model adaptation.
**Network Operation Requirements:**  
Distributed semantic resource provisioning, semantic capability exposure, intra-network and inter-network operations with standardized semantic annotation formats.​
**Data Processing Requirements:**  
Semantic autocorrection, semantic identification and representation, semantic knowledge tracking/updating, and robust security/privacy protection.​

Identified key capabilities
- **Cost-effective auto-data processing**: Automatic discovery, classification, and annotation of network data
- **Enhanced interoperability**: Cross-domain and cross-system semantic translation
- **Self-learning**: Automatic ML model training on semantically-annotated data
- **Network resilience**: Anomaly detection and disaster recovery
- **Self-evolution**: Adaptation to unknown and emerging semantics

Based on the above requirements the new architectural framework [Ref 3] mentions Semantic Knowledge Management Function (SKMF): a network-resident orchestration entity that provides the “knowledge plane” for future semantic-aware communications. which in charge of Life-cycle management of three knowledge bases – source (SKB), channel (CKB) and task (TKB) – covering data ingestion, model training/validation, versioning, upgrade and retirement.
![[archi-SAN.png]]

ETSI 
ETSI's Industry Specification Group on Experiential Networked Intelligence (ENI) is developing context-aware AI models and edge intelligence alignment mechanisms. In these specifications the key challenges, goal and requirements of semantic aware communication is mentioned. 
 Intent Translation Functional Block: a Functional Block recommended to be added within the Policy Management Functional Block that takes part in the process of Intent Translation. It performs lexical analysis, syntactic analysis, semantic analysis and augmentation, either parsing or compiling and, optionally, interpretation of the Intent Policy.  This involves planning, orchestration and framework of semantic annotations and discovery in the network (Which often aligned with the requirement of AI when used with network slicing for specific application) 
Ref : https://www.etsi.org/deliver/etsi_gr/ENI/001_099/008/02.01.01_60/gr_ENI008v020101p.pdf
https://www.etsi.org/deliver/etsi_gr/ENI/001_099/051/04.01.01_60/gr_ENI051v040101p.pdf

In ETSI GR ENI 008 - Experiential Networked Intelligence (ENI); InTent Aware Network Autonomicity (ITANA) , highlights semantic bus enables normalized policy exchange between functional blocks (Data Ingestion, Knowledge Management, Context Awareness, Situation Awareness, and Model-Driven Engineering), ensuring semantic consistency and supporting ontology-based reasoning for component interactions. Then Abstraction and Cross-vendor integration layer . https://www.etsi.org/deliver/etsi_gr/ENI/001_099/008/02.01.01_60/gr_ENI008v020101p.pdf 

The other set of applications where sematic aware networking and semantic communication is of focus is smart machine-2-machine (M2M) communication while maintaining semantic consistency across heterogeneous systems and vendors.




References 
1. Recent 6G RAN Meeting - https://summit2025.one6g.org/wp-content/uploads/Session-1_Buracchini-Enrico_6G-Roadmap-and-Status-in-3GPP-RAN.pdf
2. ITU Documents
	1. Requirements of semantic-aware networking for future networks - website link:  https://www.itu.int/itu-t/workprog/wp_item.aspx?isn=18431 | publication link:  https://www.itu.int/dms_pub/itu-t/opb/tut/T-TUT-SEMANTIC.AWARE%20C-2023-PDF-E.pdf
	2. Requirements and reference architecture of semantic-aware networking in future networks - Release 2026 - https://www.itu.int/itu-t/workprog/wp_item.aspx?isn=19137
	3. Architectural Framework for knowledge-based semantic communications over Public IMT Networks - Yet to be released - ITU Draft https://www.ietf.org/lib/dt/documents/LIAISON/liaison-2025-09-03-itu-t-sg-13-opsawg-new-technical-reports-itu-t-ystraf-kbsc-architectural-framework-for-knowledge-based-semantic-communication-over-p-attachment-2.pdf 
	4. Most data presented above collected from here : ITU -T SG 13 - https://docbox.etsi.org/Workshop/2025/02_AICONFERENCE/SESSION07/ITU-T%20SG13_CARUGI_MARCO.pdf
	5. SG16 - Multimedia and related digital technologies - https://www.itu.int/en/ITU-T/studygroups/2022-2024/16/Pages/default.aspx
	6. SG 16 also connected to SG21 -  Technologies for multimedia, content delivery and cable television
	7. 

Key information in Ref 2
Recent developments of communication and networking technologies have witnessed a growing
interest on services such as Tactile Internet and virtual reality (VR)/augmented reality (AR)/extended
reality (XR), most of which are data-hungry and can constantly generate a huge volume of data at a
tremendous speed. There is a pressing need to develop novel cost-effective solutions to support
automatic data analysing, processing, and learning for future networks including IMT-2020 [b-SAN]
[b-ITW].
Semantic-aware networking (SAN) is an important solution to meet the above need and support
diverse smart applications and services based on the network user/device generated data. The key
idea is to adopt machine and human-shared semantic terms and syntax to represent, annotate, analyse, and interpret data and services in the network. SAN seamlessly converges the networking, artificial intelligence and human user-oriented services, and has the potential to enable new features and capabilities in the future networks. In particular, SAN has the potential to enable the following novel features and capabilities:
- Cost-effective auto-data processing/pre-processing: SAN allows the data generated by UEs and services to be automatically discovered, classified, and/or associated with common semantic annotations for easy analysing and processing.
- Enhanced interoperability: based on SAN, the data and services associated with different sources, applications, networks, and systems can be automatically interpreted and converted into the same semantic domain which enables improved data and service interoperation between different application, network and system domains. 
- Self-learning and inferencing: in SAN, both the network and/or user UE can utilize semantic- annotated data arrived at the network and/or received by the user equipment to automatically train suitable ML models. The network and/or UE can also infer possible (causal or logical) relations between different semantic annotations as well as syntax in different network systems and protocols.
- Self-evolving and adapting: SAN allows network and UE to identify unrecognizable and/or
 unknown semantics and automatically infer the possible relations between the unknown data
 combination, patterns, and behavior with existing semantics.
 - Network abnormal/disaster discovery and recovery: in SAN, the network is able to identify unusual data traffic patterns, relations, syntax, and rules and can therefore support automatic discover and alarm of network abnormality and disaster. SAN also allows network operators to automatically correct the abnormal data traffic or routing paths based on the pre-identified or pre-trained rules.
 