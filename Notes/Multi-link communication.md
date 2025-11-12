-  Satellite and cellular data can both be intelligently routed through an SD-WAN connection to cloud services, with separate paths and QoS for C2 and telemetry. https://www.unmannedsystemstechnology.com/2025/04/miniature-satcom-cellular-solutions-for-commercial-bvlos-drone-operations/
- 
- https://www.unmannedsystemstechnology.com/2025/05/ground-control-unveils-rockblock-pro-for-enhanced-satellite-iot-connectivity/
- Look into ips - sessions for drone in 5G


### Air-to-Air Communication

- Short range long range BVLOS
- While no universal global standard exists specifically for air-to-air drone communication, compliance with aviation safety standards (such as ASTM for parachutes and detect-and-avoid systems) is increasingly required for certification 
- Comparison with DAA
	-  Air-to-air communication and DAA are closely linked in drone BVLOS (Beyond Visual Line of Sight) operations because both aim to prevent mid-air collisions and ensure safe integration of drones into shared airspace.
	- DAA systems often incorporate communication capabilities to exchange information with other nearby vehicles (including other drones and manned aircraft) or with air traffic control (ATC). This exchange of information helps coordinate movements and avoid conflicts in shared airspace
	-  In "cooperative" scenarios, drones and aircraft use communication technologies such as ADS-B (Automatic Dependent Surveillance–Broadcast) or TCAS (Traffic Collision Avoidance System) to broadcast and receive identity, position, and trajectory information. This data allows DAA systems to detect cooperative aircraft and make informed decisions to avoid them[1](https://www.flytbase.com/blog/detect-and-avoid-technology)[6](https://www.unmannedsystemstechnology.com/expo/sense-avoid-systems/).
	- Communication systems can also relay DAA sensor data to remote pilots or ground control stations, enabling manual or autonomous evasive actions
		- Air to Air is critical enabler for DAA - basically via broadcast system 
		- But what are the issues with Broadcast? 
		- Why Broadcast via LTE / 5G might not be the best option
		- Air-to-air communication is one input for DAA systems, especially for detecting cooperative aircraft. However, DAA systems go further by using onboard sensors to detect and autonomously avoid both cooperative and non-cooperative threats
- Current regulations and Standards with Air-to-Air communication 
	- **3GPP Release 16 (ETSI TS 122 125 V16.3.0)** defines technical requirements for UAV air-to-air and air-to-ground communications.
	- UAVs must be able to broadcast identity, location, route, speed, and status in short-range for collision avoidance and identification.
	- The system supports direct UAV-to-UAV local broadcast (air-to-air) with:
	    - Range up to 600m, message frequency of at least 10 messages/sec, and end-to-end latency under 100ms.
	    - Payloads between 50–1500 bytes per message.
	    - Operation at relative speeds up to 320 km/h.
	    - Privacy and security features, including protection against spoofing and ensuring confidentiality of identity and operational data.
	- Both centralized (via UTM) and decentralized (direct UAV-to-UAV) traffic management are supported, enabling route updates and conflict resolution in real time

- **Drone Swarm Networking and Control:**
    
    - Research focuses on integrating networking and computational systems for decentralized, self-organized drone swarms, enabling robust air-to-air communication for collision avoidance and formation control.
    - Advances include wireless beamforming, multi-hop drone cooperation for extended range and reliability, and the use of MIMO (multiple-input, multiple-output) antenna systems for high-throughput, low-latency communication in dynamic aerial environments[4](https://pmc.ncbi.nlm.nih.gov/articles/PMC8068910/).
    - Research highlights the need for tight integration between networking and control to ensure reliability, safety, and scalability of drone operations, especially in swarms and high-density airspace[4](https://pmc.ncbi.nlm.nih.gov/articles/PMC8068910/).
- Challenges
	-  Security remains a concern, particularly regarding spoofing, privacy, and non-repudiation in air-to-air communications
	-  Lack of universal standards for direct air-to-air communication between drones from different manufacturers and across different regulatory domains.
	- Lack of universal standards for direct air-to-air communication between drones from different manufacturers and across different regulatory domains.
	- Seamless integration between drone-specific UTM systems and traditional ATC remains a technical and regulatory challenge, especially for cross-border and mixed-traffic operations.
	- Wireless channel reliability, interference mitigation, and antenna configuration for high-mobility, high-altitude drones are active research areas with unresolved technical hurdles
- Collision Avoidance system (CAS) - - Advanced drones like the Skydio 2S demonstrate highly effective autonomous collision avoidance, smoothly navigating complex environments and reacting faster than a human pilot[4](https://skykam.co.uk/best-drones-with-obstacle-avoidance/). These systems excel in environments with static and dynamic obstacles, especially when equipped with AI navigation and 3D mapping.
- CAS does not require other aircraft to be cooperative (i.e., broadcasting their position), making them crucial for non-cooperative threat detection.
- Air-to-air communication (e.g., via ADS-B, direct digital links) enables drones to share position, velocity, and intent data, improving situational awareness and allowing for cooperative avoidance maneuvers.
- Its effectiveness is limited to environments where all relevant aircraft are equipped and actively broadcasting; it cannot detect non-cooperative aircraft or static obstacles.
- Air-to-air comms are thus complementary to CAS: they provide early warning and coordination but do not replace the need for onboard sensing, especially in mixed or uncooperative airspace.
- Collision avoidance systems are highly effective for autonomous obstacle and threat avoidance, especially with non-cooperative targets, but are limited by sensor and environmental factors[1](https://ceur-ws.org/Vol-3362/ISE2022_short13_Kim_Survey.pdf)[4](https://skykam.co.uk/best-drones-with-obstacle-avoidance/)[5](https://rucore.libraries.rutgers.edu/rutgers-lib/64183/). Air-to-air communication is valuable for cooperative safety but depends on all parties being equipped and compliant. 3GPP protocols are evolving to support UAV needs but still overlook some aviation-specific requirements, and significant interoperability issues remain between cellular networks and traditional aviation communication systems, particularly regarding real-time reliability, certification, and regulatory integration.
- 
**Gaps paper address**
**Solutions** 






Wifi -close proximity 
## Can Wi-Fi Be Practically Used for Air-to-Air (A2A) Communication in U-Space?

## Wi-Fi for Drone A2A Communication: Practical Considerations

**Range and Suitability**

- Wi-Fi typically offers a practical communication range of about 100 meters in open environments[2](http://www.epstem.net/en/download/article-file/3456586). This makes it suitable for close-proximity A2A communication, such as:
    
    - Swarm operations
    - Formation flying
    - Collision avoidance in dense, localized U-space scenarios

**Performance Factors**

- **Bandwidth and Latency:** Wi-Fi provides medium bandwidth and relatively low latency, supporting real-time data exchange, telemetry, and even live video between nearby drones[2](http://www.epstem.net/en/download/article-file/3456586).
- **Interference:** Wi-Fi operates in unlicensed bands (2.4 GHz, 5 GHz), making it susceptible to interference from other drones, ground networks, and devices, which can reduce reliability—especially in crowded airspace or urban U-space environments[2](http://www.epstem.net/en/download/article-file/3456586).
- **Mobility:** Wi-Fi protocols are not specifically optimized for high-speed, highly dynamic aerial networks. Rapid topology changes and Doppler effects can disrupt connections, though for slow-moving or hovering drones in close proximity, this is less of an issue.
    

**Security and Reliability**

- Security protocols (WPA2, WPA3) can be applied, but maintaining consistent authentication and encryption in dynamic, ad hoc drone networks is challenging.
- Reliability may degrade with increasing drone density or if many drones share the same channel.

**Regulatory and Operational Context**

- In U-space, EASA and other aviation authorities focus on electronic conspicuity and reliable communication for safety-critical operations[1](https://www.easa.europa.eu/en/downloads/134939/en). Wi-Fi can support this in localized, tactical scenarios but is not suitable for wide-area, high-altitude, or BVLOS (beyond visual line of sight) A2A communication.
- For U-space at low altitudes (up to 150 meters above ground), Wi-Fi can help make drones "electronically conspicuous" to each other and to ground stations, but its use should be limited to scenarios where close proximity and low density are assured[1](https://www.easa.europa.eu/en/downloads/134939/en).
    

## When Is Wi-Fi Practical for A2A in U-Space?

|Use Case|Practicality of Wi-Fi A2A|
|---|---|
|Swarm/formation flying|High|
|Collision avoidance (close)|High|
|Wide-area BVLOS|Low|
|High-density urban U-space|Low to moderate|
|High-speed maneuvers|Low to moderate|

- **Close Proximity:** Wi-Fi is practical for drones operating within 100 meters of each other, such as in swarms or for tactical coordination[2](http://www.epstem.net/en/download/article-file/3456586).
- **Beyond Close Proximity:** For operations requiring greater range, reliability, or regulatory compliance (e.g., BVLOS, integration with U-space service providers), cellular (LTE/5G), ADS-L, or dedicated aviation communication technologies are preferred[1](https://www.easa.europa.eu/en/downloads/134939/en).
    

## Summary

Wi-Fi can be used for air-to-air communication among drones in U-space, but its practicality is limited to close proximity (typically ≤100 meters), low-density, and low-mobility scenarios. It is effective for swarm operations, formation flying, and tactical collision avoidance. For broader U-space integration, higher reliability, and regulatory compliance, Wi-Fi should be complemented or replaced by cellular, ADS-L, or other aviation-grade technologies[1](https://www.easa.europa.eu/en/downloads/134939/en)[2](http://www.epstem.net/en/download/article-file/3456586).

1. [https://www.easa.europa.eu/en/downloads/134939/en](https://www.easa.europa.eu/en/downloads/134939/en)
2. [http://www.epstem.net/en/download/article-file/3456586](http://www.epstem.net/en/download/article-file/3456586)
3. [https://mediatum.ub.tum.de/doc/1079692/1079692.pdf](https://mediatum.ub.tum.de/doc/1079692/1079692.pdf)
4. [https://www.mdpi.com/1424-8220/22/10/3731](https://www.mdpi.com/1424-8220/22/10/3731)
5. [https://www.osti.gov/servlets/purl/1885156](https://www.osti.gov/servlets/purl/1885156)
6. [https://diydrones.com/profiles/blogs/the-case-for-wifi-in-drones](https://diydrones.com/profiles/blogs/the-case-for-wifi-in-drones)
7. [https://www.sesarju.eu/sites/default/files/documents/projects/DREAMS%20U-space%20Scenarios%20v1.0.pdf](https://www.sesarju.eu/sites/default/files/documents/projects/DREAMS%20U-space%20Scenarios%20v1.0.pdf)
8. [https://www.mdpi.com/2504-446X/9/2/108](https://www.mdpi.com/2504-446X/9/2/108)
9. [https://horizoneuropencpportal.eu/sites/default/files/2024-05/sesar-u-space-concept-of-operation-4th-edition-2023.pdf](https://horizoneuropencpportal.eu/sites/default/files/2024-05/sesar-u-space-concept-of-operation-4th-edition-2023.pdf)
10. [https://www.easa.europa.eu/en/downloads/136131/en](https://www.easa.europa.eu/en/downloads/136131/en)
11. [https://www.thi.de/en/research/technology-transfer-center-unmanned-flight-systems/research-areas/projects-ttz/wireless-communications-for-ai-unmanned-flying-1/](https://www.thi.de/en/research/technology-transfer-center-unmanned-flight-systems/research-areas/projects-ttz/wireless-communications-for-ai-unmanned-flying-1/)
12. [https://www.sesarju.eu/sites/default/files/documents/u-space/U-space%20Drone%20Operations%20Europe.pdf](https://www.sesarju.eu/sites/default/files/documents/u-space/U-space%20Drone%20Operations%20Europe.pdf)
13. [https://www.easa.europa.eu/en/downloads/140288/en](https://www.easa.europa.eu/en/downloads/140288/en)
14. [https://www.dlr.de/en/kn/about-us/departments/communications-systems/aeronautical-communications-group](https://www.dlr.de/en/kn/about-us/departments/communications-systems/aeronautical-communications-group)
15. [https://elib.dlr.de/128456/1/uploaded_PID6048681.pdf](https://elib.dlr.de/128456/1/uploaded_PID6048681.pdf)
16. [https://www.autonomyglobal.co/opening-up-europes-skies-the-future-of-drone-operations-with-u-space/](https://www.autonomyglobal.co/opening-up-europes-skies-the-future-of-drone-operations-with-u-space/)
17. [https://xray.greyb.com/drones/communication-protocols-long-range-drone-networks](https://xray.greyb.com/drones/communication-protocols-long-range-drone-networks)
18. [https://orbit-cs.com/press-releases/orbit-communication-systems-introduces-the-innovative-airtrx-family-of-multi-purpose-airborne-satellite-terminals-that-uniquely-enable-continuous-wifi-communication-for-regional-jets](https://orbit-cs.com/press-releases/orbit-communication-systems-introduces-the-innovative-airtrx-family-of-multi-purpose-airborne-satellite-terminals-that-uniquely-enable-continuous-wifi-communication-for-regional-jets)
19. [https://www.thalesgroup.com/en/markets/aerospace/connectivity-solutions/air-to-ground-in-flight-connectivity](https://www.thalesgroup.com/en/markets/aerospace/connectivity-solutions/air-to-ground-in-flight-connectivity)

---
## What is ADS-L Introduced by EASA?

**ADS-L** stands for _Automatic Dependent Surveillance – Light_. It is a new protocol and technical standard introduced by EASA to enhance electronic conspicuity in European airspace, particularly within U-space (the digital airspace management system for drones and manned aircraft).

## Key Features

- **Purpose:**  
    ADS-L is designed as a _minimum standard_ to make manned aircraft conspicuous to U-space Service Providers (USSPs) and, by extension, to unmanned aircraft systems (UAS) operating in U-space airspace[1](https://www.easa.europa.eu/sites/default/files/dfu/4._iconspicuity_ads-l.pdf)[6](https://www.unmannedairspace.info/emerging-regulations/easa-publishes-ads-l-technical-specification-for-srd860-frequency-band-to-support-e-conspicuity-in-u-space/)[8](https://www.easa.europa.eu/en/the-agency/faqs/introduction-ads-l).
    
- **"Light" Concept:**  
    The “L” in ADS-L means “Light”—it is a simplified, lower-cost, and lower-power alternative to traditional ADS-B, making it accessible for general aviation, light aircraft, and drones not equipped with certified ADS-B installations[1](https://www.easa.europa.eu/sites/default/files/dfu/4._iconspicuity_ads-l.pdf)[3](https://www.easa.europa.eu/en/the-agency/faqs/automatic-dependent-surveillance-light-ads-l)[8](https://www.easa.europa.eu/en/the-agency/faqs/introduction-ads-l).
    
- **Transmission:**
    - Operates on the licence-free SRD-860 band (868–869 MHz in Europe), with a transmission power limited to 14 dBm (25 mW ERP)[2](https://www.easa.europa.eu/en/downloads/137503/en)[3](https://www.easa.europa.eu/en/the-agency/faqs/automatic-dependent-surveillance-light-ads-l).
    - Can also be implemented via mobile telephony (future support for 4G/5G is planned)[1](https://www.easa.europa.eu/sites/default/files/dfu/4._iconspicuity_ads-l.pdf)[3](https://www.easa.europa.eu/en/the-agency/faqs/automatic-dependent-surveillance-light-ads-l)
- **Data Broadcast:**
    
    - Relies on GNSS for position data.
    - Transmits position, identification, and other flight parameters at least once per second[2](https://www.easa.europa.eu/en/downloads/137503/en).
    - Designed to be compatible with low-cost devices, mobile phones, and portable conspicuity devices[1](https://www.easa.europa.eu/sites/default/files/dfu/4._iconspicuity_ads-l.pdf)[3](https://www.easa.europa.eu/en/the-agency/faqs/automatic-dependent-surveillance-light-ads-l).

- **Integration:**
    
    - Easily integrated into existing cockpit traffic awareness apps and receivers.
    - Supports both ground and air-based reception, improving situational awareness for all airspace users[3](https://www.easa.europa.eu/en/the-agency/faqs/automatic-dependent-surveillance-light-ads-l)[7](https://www.flarm.com/en/general-aviation/electronic-conspicuity-and-ads-l/).
- **Regulatory Status:**
    
    - Recognized by EASA as a means of compliance for electronic conspicuity in U-space airspace under SERA.6005(c)[2](https://www.easa.europa.eu/en/downloads/137503/en)[3](https://www.easa.europa.eu/en/the-agency/faqs/automatic-dependent-surveillance-light-ads-l)[6](https://www.unmannedairspace.info/emerging-regulations/easa-publishes-ads-l-technical-specification-for-srd860-frequency-band-to-support-e-conspicuity-in-u-space/).
    - No formal ETSO (European Technical Standard Order) or MOPS (Minimum Operational Performance Standards) yet, but manufacturers can obtain a “Non Technical Objection” (NTO) statement from EASA for compliance[2](https://www.easa.europa.eu/en/downloads/137503/en).

## Scope and Limitations

- **Not a Replacement for Certified ADS-B:**  
    ADS-L is not intended for use in IFR operations or as a replacement for certified ADS-B; it is for enhancing situational awareness and safety, especially in uncontrolled or U-space airspace[3](https://www.easa.europa.eu/en/the-agency/faqs/automatic-dependent-surveillance-light-ads-l)[4](https://www.flarm.com/en/blog/easa-introduces-ads-l-in-new-u-space-regulation-further-defines-e-conspicuity/).
- **Focus on Air-to-Ground:**  
    ADS-L is primarily focused on air-to-ground transmission for U-space management, not optimized for direct air-to-air interaction, though it can improve mutual awareness among equipped aircraft[4](https://www.flarm.com/en/blog/easa-introduces-ads-l-in-new-u-space-regulation-further-defines-e-conspicuity/).
## Application to Drones

- EASA is considering the optional or mandated use of ADS-L for drones, especially for BVLOS (Beyond Visual Line of Sight) operations, to improve their visibility to other airspace users and U-space service providers[5](https://www.unmannedairspace.info/uncategorized/easa-developing-plans-to-include-drones-in-its-adsb-l-general-aviation-e-conspicuity-programme/).
- The standard is designed to be extensible and future-proof, with ongoing technical discussions to ensure interoperability between manned and unmanned aircraft[5](https://www.unmannedairspace.info/uncategorized/easa-developing-plans-to-include-drones-in-its-adsb-l-general-aviation-e-conspicuity-programme/).
    

---

**In summary:**  
ADS-L is a low-cost, low-power electronic conspicuity standard introduced by EASA to make both manned and unmanned aircraft visible in U-space airspace. It is designed for easy adoption, using the licence-free SRD-860 band and potentially mobile networks, and is aimed at improving situational awareness and safety, particularly for general aviation and drones operating outside traditional ATC coverage[1](https://www.easa.europa.eu/sites/default/files/dfu/4._iconspicuity_ads-l.pdf)[3](https://www.easa.europa.eu/en/the-agency/faqs/automatic-dependent-surveillance-light-ads-l)[6](https://www.unmannedairspace.info/emerging-regulations/easa-publishes-ads-l-technical-specification-for-srd860-frequency-band-to-support-e-conspicuity-in-u-space/)[8](https://www.easa.europa.eu/en/the-agency/faqs/introduction-ads-l)







- **Cooperative and de-centralized Airspace** 
- Mesh node on raspi pi 
- script that can read data -python script
- py scripts on mesh nodes - libraries constraints 
- direction of comm defined on script
- Mesh node detect Pi - 
- Configure network interface 

---
Multipath - idea  ![[ANYWI_DemoPresentation.pdf]]