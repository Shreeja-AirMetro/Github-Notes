> [!summary] Summary
> Converted Word doc: early idea for a large EU project on dependable remote control (C2 datalink) of vehicles on land, sea and air using commercial networks; scope, use cases.
>
> **Target / goal:** Seed for a standards-creating EU project.

> Converted from ![[Standards-creating-project-idea-v2.docx]] (original kept in Attachments).

***Very initial idea for a large EU project for dependable remote control of vehicles on land, at sea and in the air.***

**Purpose**

Ensure a dependable data link and related software execution environment for command and control for remote (beyond visual line of sight for the operator) vehicles on land, at sea and in the air. In the case of aircraft, this would refer to drones or UAS in U-space and SORA-based operations.

In an extension to other vehicles, in the case of cars, this for instance includes connections to remote drivers getting driverless taxis unstuck when the safety system has brought the vehicle to a stop, and in the case of vessels it can be aquatic drones or even larger uncrewed boats.

In general, the idea would be to base the functionality on commercially available data communication services (cellular and satellite-based) with the possibility to employ local, private network solutions as well within the same architecture. However, we can also consider more innovative approaches at the low level of networking (radio links, sensors and chips).

***Include***
Some aspects to possibly include. The list is not exhaustive:

- Cybersecurity (to protect the datalink and PNT)
- Positioning, navigation and timing
- Low-level cloud technology for edge and backend to complete the data link
- Maybe the traffic management system, where there are valuable commonalities and/or overlap between the modes
	- UTM (air)
	- Traffic management system (road)
	- Vessel Traffic Systems or similar (sea)

***Use cases, two or more of:***

- Drones
- Highly automated vehicles, including remote driver functionality
- Mobile robotics
- Unmanned ships

***Research questions:***

- Determine real needs and requirements for data link, including latency, bandwidth, packet loss rates, monitorability, human factors needs for remote pilot/driver/captain
- Cybersecurity - Post Quantum Cryptography, Key management, Identity management, European-level systems to allow cross-border operations, shared threat models, incident detection, automated responses
- Human factors for command, control, monitoring of vehicle and cybersecurity status
- More?

**Objectives**

[1] Understand scenarios, needs and requirements for performance of control systems, control links and HMI in real-world operations of remotely controlled vehicles, in primarily a European context, but also with space for global considerations

[2] Design, develop architectures, protocols, and systems to meet those needs and requirements for safe control with the pilot/driver/operator in or on the loop

[3] Demonstrate the technologies developed at a laboratory or highly controlled level in representative use cases

***Notes to objectives***

Re: [1], some aspects related to drones/UAS:

- U-space
- SORA
- Types of operations
	- Delivery
	- Agricultural
	- Physical work (maintenance, repairs, etc.)
	- Search and rescue (SAR)
	- Need for control commands and input
		- Messages for flight control computer/autopilot
		- Direct real-time control input to aircraft’s control curfaces
	- VLOS/eVLOS/BVLOS
- Phases of flight
- Speed (air speed, ground speed)
- Human factors, for instance
	- Remote pilot’s needs for sufficient information to know the state of the system (the C2 link in our case)
		- What information and how should it be presented?
	- Real needs for system reaction times, latencies, round trip times in the sense-think-act loop (or the OODA loop for those who want to be fancy)

Re: [1], some aspects related to driverless cars with remote drivers
- Create a full and safe understanding for the remote driver of the surroundings of the car
- Urban, suburban and rural scenarios
- Scenarios of various degrees of visibility and connectivity/bandwidth

2025-04-22
Morten Larsen
morten.larsen@anywi.com
