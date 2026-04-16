---
marp: true
theme: default
paginate: true
backgroundColor: #fff
---

# Collaboration with Enrique 
# DRCN Conference 
Date: 30.01.2026

---
# Conference 


Deadline: 15th Feb 2026
Submission:  EDAS(deadline don't match)
Rules: English, IEEE Conference 2 column template, 5-8 pages 

# Potential Topics
-  Communication reliability for smart systems (cities, transport, logistics, etc.)
- Network reliability analysis and modelling
- Reliability requirements and metrics for users, businesses, and the society
- Reliable communications in vehicular networks

---
# Motivation 



# State of Art 

---
# Method


---
# Implementation



---


# First draft by Enrique 

![[KLU___TUDresde___RCP_for_unmanned_aerial_vehicles_in_NTN_networks.pdf]]
Key points 
- This work present a systematic methodology to generate a Required Communication Performance (RCP), reinterpreting the current aviation methodology to this drone’s
air segment needs. We maps safety requirements from aviation industry to key performance indicators of 3GPP networks.
- Drones in non-segregated airspace 
- What is non-segregated airspace ? 
- The RCP specification for a drone is not a static value but a safety-derived requirement based on the most stringent communication transaction necessary for the mission’s risk profile.
- Methods - 4 phases 
- Phase 1 : Mission and Risk profiling 
- Phase 2: Transaction Analysis 
- Phase 3: RCP Metrics Specification 
- Phase 4: Compliance and Allocation
- As noted in [2], higher risk operations (e.g., Urban Beyond Visual Line of Sight - BVLOS necessitate more stringent RCP types (e.g., RCP 10) to ensure a Time to Intervention (TTI) sufficient for safety


Shreeja Preparation 
Run the simulator 
- NTN separately 
	- UAV from A to B flies at altitude of 60-100m  (25km) calculate the latency for C2 link 
	- Uplink and Downlink data collection 
- TN separately 
	- UAV from A to B flies at altitude of 60-100m  (25km) calculate the latency for C2 link 
	- Uplink and Downlink data collection 
- TN -NTN together 
- Data capture : RSSI, SINR, Throughput, Jitter , Packet loss 



---

Meeting with Enrique 16/4 
Question (Red) and his points -> Shreeja To dos 


- The RCP specification for a drone is not a static value but a safety-derived requirement based on the most stringent communication transaction necessary for the mission’s risk profile. 
Risk profile 
- Categorize the type  
- Missions occurring in Controlled Airspace (Classes A to C) impose stricter availability requirements due to the need for interaction with Air Traffic Management (ATM).  <span style="color:rgb(255, 0, 0)">DO WE SHOW IN RESULTS</span> 

- Operational Communication Transaction”. [2]. An RCP specification is driven strictly by the most time-critical transaction required to maintain safety boundaries. <span style="color:rgb(255, 0, 0)">TRANSACTION TIME - Is it END TO END</span> 
- <span style="color:rgb(255, 0, 0)">The second consist of an additional non-terrestrial segment (LEO satellite constellation).</span>

- RCP Safety Limit (Expiration Time) remains 8.0 s. <span style="color:rgb(255, 0, 0)">WHERE IS THIS FROM </span> 
- <span style="color:rgb(255, 0, 0)">Eq 4  - End to ENd </span> 
- Latency , SINR <span style="color:rgb(255, 0, 0)"><br>- Check for what are the results required </span> 


Shreeja test - to dos
To send to Enrique - Monday 
1, Output of LEO sat only uplink and downlink 
2, update on TN + NTN setup 

- 