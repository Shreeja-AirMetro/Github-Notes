Meeting minutes 24/4
- Members introduction 
- Initial steps, activities - use case
- members - technical side - not on UAS /Drone side 
- e-conspicuity 
- set a level of initial technical work  - important to add drone operators 
- Dutch operator - customs use case 
- Produce documents with the findings 
- scenario involved cruising, landing and working flights 
- Artificial scenario - Mission scenario - landing area (Home) - home airspace - Mission area - inverse of open/cruise airspace because you try to stay away from other drones. The technology you need is different 
- Q: The airspace - horizontal /u-space -not relevant here (port) 
- more like wind tunnel different
- 4 or more use-cases
- Sequence of states - transition of C2 
- Timing diagram 
- Real-time - different from perspective of Engg
- Type of data - In-flight navigation  (C2/C3)
- Multiple hardware - C2 telemetry / other hardware is included 
- Agile protocol stack 
- Data link vary - QoS vary 
- Session can have multiple data flows  
- Crypto 
- System configuration and control and access control for all layers 
- bearer agility  - because link need not be available all the time 
- Layer 3 and 4 unification -  user friendly pov 
- Concept of identity - drone, remote pilot 
- 24 bit ICAO for large drone 
- IP address as identifiers (transponders and other not IP traffic) 
- Pre-flight checklist for large drones
- identification and authentication via comm link 
- Modern way - global unique random numbers - mapping to legacy structures through data planes - bundle on the map table (Difficult to make it wrong) 
- UUID 
- What initiatives on the protocol stack must be done 
- CISP - National 
-Todos from AnyWi side
- Connect to EUROCAE , SESAE Corus 
- Drone operators, Network operators  - fill the gap in memberships 
- ![[IMG_20250424_152542 (1).jpg]]




---
12/ 6

Andres

- Rehash on scenarios
-  Dutch Drone Council - EU players
- EU EASA  from EASA 
- Country 
- EUROCONTROL - U-space - actually Uniform 
- huge need for standards 
- write regulation need standards refer to 
- European Drone council ?
- stakeholder and industry associations 
-  Actual descriptions 

-  Flying experiences 
- Gyros , IMUs
- Flight computer 
-  Dev comm - protocol 
- Traffic management - Security and topography
- Get close to metal  - Low level - All key points 
- NTN Petr SoA 

 within 2 weeks  - send report email 
---

Notes on the pre-stage C2 communication Proposal 

![[Pasted image 20250626075734.png]]
   

    - C3 decision amking point
    - 
|- ![[Pasted image 20250626073517.png]]
- C2 transition - Allign with different levels of c2 requirement
- 
- https://droneller.com/blog/altitude-hold-in-drones/
- We’ll explore two key components that make altitude hold possible: the Barometric Pressure Sensor and the PID Controller.
- Barometric Pressure sensor detect changes in atmospheric pressure as your drone ascends or descends. As you rise in altitude, the air pressure decreases, and the sensor records this drop.
-  PID controller. It’s like the autopilot that ensures your drone maintains that perfect height.
- [PID stands for Proportional-Integral-Derivative,](https://www.omega.com/en-us/resources/pid-controllers#:) but don’t let the name scare you. At its core, it’s a control algorithm that fine-tunes your drone’s throttle to keep it at the desired altitude
- - _Proportional (P):_ This component responds to the immediate error, essentially how far off your drone’s altitude is from the desired height. If it’s too high, the P component reduces throttle; if it’s too low, it increases throttle.
- - _Integral (I):_ The I component looks at the accumulated past errors and corrects any long-term deviations. It’s like smoothing out those occasional bumps in the road.
- _Derivative (D):_ The D component anticipates future errors by considering the rate of change of error. It helps dampen altitude fluctuations, ensuring your drone maintains a steady height.
- Feedback loop : Think of it as a dynamic dance between your drone and the sensors, all while keeping it steady in the sky.
- continuous adjustments based on sensor feedback 
- Initialization and Reference Point: Just like you need a starting point for any journey, altitude hold starts with initialization and setting a reference point.


---
Document to send 

- [ ] Remarks 
- [ ] Add points - experiences

1. C3 definition 
2. C2 information different at different level  - how are going to identify the key data 
3. Built a framework from the general 50kbps bandwidth requirement and latency conditions
4. Not just nav , Battery is also a necessary c2 information 
5. UTM - remote identification / awareness 


---
26/6 


Drone C2 layer 2 ubuntu | Debian 

- autonomous better than Humans 
- manage motorways
- people don't accept technological change
- 

---
Restructure the document 

Below is a **cohesive and structured synthesis** of the key points from both documents, organized by operational phase and emphasizing the critical aspects of BVLOS drone operations for offshore wind turbine inspection, with a focus on C2 (Command and Control) requirements, technical considerations, and regulatory compliance.

  

**BVLOS Drone Operation for Offshore Wind Turbine Inspection**

  

**Mission Overview**

  

- A swarm of drones is deployed from an operational center to perform regular inspections of offshore wind turbines.

- Operations span two distinct geolocations: the operational site (good connectivity) and the offshore turbine area (predominantly poor connectivity)[^1][^2].

- Drones are equipped with LiDAR, cameras, and onboard computers for comprehensive data collection[^1].

- Ensuring a **reliable and resilient C2 link** is critical due to the diverse and challenging operational environment[^1].

  
  

### 1. **Regulatory \& Standardisation Framework**

  

- **CE Marking \& EU Regulations**: Operations fall under the 'specific' category as per Article 5(1) of EU 2019/947, requiring prior authorisation and strict compliance with safety and operational standards[^2].

- **ISO Standards**: ISO 21384-3 and related standards define requirements for safe commercial drone operations, including all flight phases[^2].

- **SORA Framework**: The Specific Operations Risk Assessment (SORA) methodology is used to evaluate and mitigate risks, supporting regulatory approval and U-space authorisation[^2].

  
  

### 2. **Operational Phases \& C2 Link Requirements**

  
| **Phase** | **Key Actions \& C2 Needs** | **Standardisation \& Safety** |

| :-- | :-- | :-- |

| **Takeoff** | - Monitor altitude and position using telemetry and onboard sensors<br>- Real-time data to ground station | - Maintain safe distance from uninvolved persons (EU 2019/947)<br>- Pre-flight checks crucial[^2] |

| **Cruising** | - Maintain stable C2 link despite changing connectivity<br>- Continuous monitoring of navigation and health | - Compliance with operational risk assessments<br>- Evaluate protocol (FTP/UDP/TCP) suitability[^1][^2] |

| **Inspection (Hovering)** | - Precise altitude and position control for detailed data capture<br>- Real-time sensor feedback | - Standardised sensor integration for stability (gyroscope, accelerometer, GPS, altimeter)[^2] |

| **Descent \& Landing** | - Controlled descent with automated systems for safety<br>- Emergency protocols in place | - Adhere to ISO/EU descent protocols<br>- SORA-based risk mitigation and emergency procedures[^2] |





  

### 3. **Technical and C2 Communication Insights**

  

- **C2 Link Characteristics**:

    - **Current Gaps**: Telemetry links (location, battery, temperature) are standard, but current C2 Required Communication Performance (RCP) does not fully meet safety and management needs for BVLOS operations[^1].

    - **Data Rates**: C2 communication typically requires low data rates (>50 Kbps), but must be highly reliable and resilient[^1].

    - **Heterogeneous Multi-Link Setup**: Combining multiple network technologies (e.g., terrestrial, satellite) is necessary to ensure robust coverage, especially offshore[^1].

- **Critical Parameters for Real-Time C2**:

    - Navigation data, battery status, temperature, sensor calibration, and payload health must be monitored in real time[^1].

    - Placement and interference of GNSS and communication antennas can impact reliability and require careful pre-flight checks[^1].

- **Protocol Considerations**:

    - Choice between FTP, UDP, or TCP should be based on network availability and the need for real-time, deterministic responses[^1].

    - Open-source telemetry protocols may have limitations, especially with LEO Satcom links[^1].

  
  

### 4. **Operational Challenges and Risk Mitigation**

  

- **Connectivity Issues**: Offshore environments often have poor connectivity, necessitating resilient C2 solutions and robust pre-flight planning[^1].

- **Sensor Calibration**: Accurate calibration and parameter checks are vital for reliable operation and data integrity[^1].

- **Emergency Procedures**: Automated landing and collision avoidance systems must comply with regulatory standards and be validated through risk assessments (SORA)[^2].

  
  

### 5. **Open Questions and Considerations**

  

- **C3 Link Definition**: According to ICAO, C3 (Command, Control, and Communications) encompasses the essential links for RPAS operation, including integration with traffic management and remote identification systems[^1].

- **Parameter Expansion**: Beyond navigation and battery, other real-time parameters (payload health, sensor status, environmental data) should be considered for C2 communication[^1].

- **Pre-Flight Checks**: Establishing a comprehensive checklist for C2 link health, including sensor calibration and antenna placement, is recommended[^1].

  

**Summary Table: Key Requirements Across Phases**

  
  

| **Phase** | **C2 Requirements** | **Safety/Standardisation** |

| :-- | :-- | :-- |

| Takeoff | Real-time telemetry, stable link | Distance from uninvolved persons, pre-flight |

| Cruising | Resilient multi-link, continuous monitoring | Risk assessment, protocol evaluation |

| Inspection | Precision control, sensor feedback | Standardised sensors, data quality |

| Descent/Landing | Automated systems, emergency protocols | ISO/EU compliance, SORA framework |

  

This integrated structure ensures all critical operational, technical, and regulatory aspects are addressed for **safe and compliant BVLOS drone inspections of offshore wind turbines**.


[^1]: Scenario-1-C2-insights-Shreeja.docx

[^2]: Scenario-1-Offshore-wind-turbines-maintenance-inspection-v0.6.docx

---
1. Status - Activities since last meeting

-----------------------------------------

Picking up background noise in the cellular space, there is an uptick in interest for ==multilink/multibearer technology at the RAT level.== How this will work across diverse technologies (SatCom/WiFi/5G/6G) to be seen.

There has been an interesting event in Rotterdam organised by Rotterdam Droneport, a subsidiary of the Port of Rotterdam that bills themselves as the innovative arm of the enterprise. A couple of notes from my (Morten) side:

- The high end of the speakers (Dutch defence minister, civil servants from the ministry, etc.) all wanted to point out how much we need to do something. They have seen videos from Ukraine and they want the same, preferably on a ==three-week innovation cycle==

- On the practical side of things, those who have tried to use drones for real work complain about practicalities (regulatory, etc.) and still look at each use case or experiment as a single instance

- In the middle there are people (like us?) with maybe some useful contributions - for instance a more structured approach. Such approaches require a lot of work both technical and organisational to fit into a world of high-flying visions supported by more grounded tinkering around single use cases

- Dispite this, some progress on the world of aerial drones and aquatic and ground drones/robots, which are clearly getting closer to each other

- In short - lots of opportunity, but also a lot of work required to drive it forward in a landscape where everybody is shouting that something must be done, but not a lot of effort to concert it

2. Discussion - What is needed?

-------------------------------

From other discussions with industrial drone operators it is clear that the purpose is to achieve a very high degree of automation, while being compliant with European regulations. This is in line with most/all other highly automated industrial/logistics processes, where there is always a control room staffed with one or more persons to keep an eye on things. Take for instance "driverless" trains, where there are supervisors in the control room "driving" remotely 10 or more trains each. 

This means that discussions about BVLOS (which is a prerequisite for truly automated operations) should use the right terminology, and for instance avoid terms like "autonomous", popular in other industries. 

3. Next steps

-------------

Petr will look at terminology around autonomous/automated/remote/etc. for discussions outside strictly aviation-focused communities

Petr (and Morten) will also look at the models (if that is the right word) and abstractions that coudl help bridge the gap between high visions and practical reality of highly automated drone operations


---
2/10
C2 meeting 
Anders
Petr  Janous
Dave Marples

Autonomous definition in EASA ?! 
Model specification and Concepts - Morten presentation 
	 - regulation grounded in reality 
	 - security today incl. post quantum 
	 - aviation procedures, standard operations 
	 - tangible results next to moterway when no people - opportunities are limited
	 - technological pressure is building - Dave - and reg. holding it back 
	 - Mobile networks - what happen iphone came
	 - A disturbance from tech side - step change with procedure and regulation
	 - Q is not a linear process , Nothing happens and everything happens all at ones. Glimmer - what disturbance event is going to be . Military based disturbance 
	 - incre Tech objection can be resolved - logistical regulatory needs to be solved
	 - regulatory is based on feeling - need to figure out what's the problem 
	 - GUTMA - connection 
	 - Morten - T-mobiles - SAIL levels - unknown territory - Dutch - tinkering going on
	 - group visit to Manna 
	 - Event to bring all these people 
	 - birds of the feather - action / stimulus action - commissioned to make one of these? 
	 - SESAR events  - but not suitable 
	 - Open source world puts actions first 
Tasks : 
simple scenarios and definition and models for automation 
validate idea - real-world opüerators of BVLOS flights

---
12/11

Quick updates from last meeting 
Status updates 
	"right contact to the ministry"
	- Stakeholder problems from their perspective 
	- EGNOS Day 
	- 