
// Organizing the goal and literature

1. What is Air to air communication 
		General Aviation - Air-to-air communication is ==the direct exchange of information between aircraft in flight==. Depending on the context, it uses radio frequencies or advanced digital networks to coordinate flights, share weather and safety details, or conduct military operations without relying on ground-based air traffic control. 
		Audio at a particular frequency  - A2A
		A2G -  LDCAS https://elib.dlr.de/128456/1/uploaded_PID6048681.pdf, ACARS ARINC protocol
			Note : The ATM gives instructions on which aircraft does which flight procedure for avoiding conflict
		Goal of A2A in IAM - **Air-to-Air** communication, coordination, or sensing between aircraft/UAVs operating in the same airspace. This does not resolve conflict , it try to avoid conflict by providing situation awareness - position , altitude, heading, speed and flight path
		What is synonyms to A2A from Telecommunication and its standards -  3GPP (telecom standard orchestrator)3GPP terminology, 3GPP terminology, A2A (Air-to-Air) communication for drones is increasingly treated as a form of D2D (Device-to-Device) communication implemented through 5G sidelink technology.
		5G sidelink  used instead of  - Drone A -> base station -> core network -> basestation-> drone B - it reduces the communication latency as drone A to Drone B 
			The autonomous cars evaluate sidelink - broadcast, unicast messaging systems for collision avoidance , low latency situational awareness 
			https://www.sciencedirect.com/science/article/pii/S0140366422001967
			https://arxiv.org/pdf/2104.11135
		Prominent project for Communication in AAM https://ieeexplore.ieee.org/document/10539166
2. Its role  - A2A communication is only can be used for situational awareless which can provide some support for conflict avoidance. This is due to limitations of 5G propogation challenges , interference and 3D mobility
3. How is it different from Conflict detection and resolution 
			Today EASA  - U-space doesn't allow or envision a communication link only based conflict detection and resolution. 
			The network assisted UTM  - U-Space digital services have 4 categories 
			U1 provides basic foundational services such as UAS registration, identification, support for flight preparation. U2 provides initial operational
			services - flight trajectory planning, safety radius around each
			UAS trajectory and separation margin. U3 introduces advanced
			operational capabilities like real-time geo-awareness of the
			airspace, automated traffic management, tactical deconfliction
			(E2E process of detection, resolution, prevention). Finally, U4
			enables highly automated and fully integrated U-space services
			for seamless integration and coordination with manned aviation for very high-density airspace. 
			The Telecom (5G an)
4. Tools and Network 
		Situational awareness - 5G, Wifi based solution where Drone A and Drone B within a free pathloss range - can exchange - Bidirectional. 
		Gap: Message protocol is not present and there is no instrument / tools on how a flight controller act to it. This needs a backend support with remote operator (A2G) link
5. State of Art 
		1. Air to Air is from a extension of 5G network perspective where UAV is a base station that can provide communication to aerial users (UAVs) - https://ieeexplore.ieee.org/abstract/document/9151343 - <span style="color:rgb(255, 0, 0)">this doesn't fit the IAM goal </span> 
		2. 