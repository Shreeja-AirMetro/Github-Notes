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
	- Similar to displacement and expiration time 
	- change the trajectory - waypoint update transaction time 
- <span style="color:rgb(255, 0, 0)">Eq 4  - End to ENd </span> 
- Latency , SINR <span style="color:rgb(255, 0, 0)"><br>- Check for what are the results required </span> 


Shreeja test - to dos
To send to Enrique - Monday 
1, Output of LEO sat only uplink and downlink 
2, update on TN + NTN setup 

-  Do uplink and downlink  - one way transaction 
- patch  - synthetic latency  - synchronize timestamps 


---

# 20/4 Shreeja Simulator to do 

- [ ] Adapt the code veins inet mobiliy in veins leon 
	- [x] Check veins leon output
	- [x] Altitude in Veins Inet 
	- [x] Questions on Air layer with veins inet mobility 
	- [x] Complete adapt code 
22/4 
 - [ ] Compare with Lyuqiao code
 - [ ] Change/ reduce the distance and cell size 
 - [ ] Test this part 
 - [ ] Downlink data - check - initial plot 
 - [ ] prep for tomorrow meeting 
 - [ ] Send to Lyuqiao 
 - [ ] Github V1
23/4
 - [ ] version for TN only  
- [ ] Version for NTN only
- [ ] Compile 

Final dataset (before 3/5)
- [ ] Downlink TN  - data
- [ ] Downlink NTN  - data
- [ ] Uplink TN 
- [ ] Uplink NTN
- [ ] Plots




---

Based on your `.ini` file and the UAV scenario described (100m altitude, 10m/s, intermittent GNB connectivity), your setup is largely correct for a **TN/NTN (Terrestrial/Non-Terrestrial Network)** hybrid simulation.

However, to strictly satisfy **ICAO RCP** validation, there are missing configurations in your `.ini` to ensure all necessary data is recorded in your `.vec` file.

### 1. Verification of Scenario Parameters

- **Altitude & Speed:** Your altitude is set via `*.cars[0].mobility.height = 100 m` (which is standard for small UAVs). At 10m/s, crossing the 800m gaps between your GNBs (defined at 1m, 800m, 1600m) will take about 80 seconds per segment. This provides a good window for handover and "no-connection" analysis.
    
- **Intermittent Connectivity:** You have a large gap between `gNodeB[2]` (1600m) and `gNodeB[3]` (10000m). This perfectly simulates the "no available base station" section you mentioned.
    
- **Dual Connectivity:** You are using `CbrSenderDualConnectivity`. Since RCP applies to the _entire_ communication transaction, this is good for showing how NTN (Satellite) might maintain Continuity/Availability when the TN (GNBs) fails.
    

### 2. Missing `.vec` Records for RCP Analysis

Currently, your `.ini` only explicitly records `endToEndDelay`. To plot against ICAO RCP for **Availability** and **Continuity**, you need to add the following to your `[General]` or `[Config HOdebug]` section:

#### A. Record SINR (For Physical Layer Context)

As we discussed, SINR explains _why_ a transaction failed. Add this to capture the radio quality:

Ini, TOML

```
# Record SINR for both TN and NTN carriers
**.cars[*].cellularNic.nrPhy.sinr:vector.record = true
**.cars[*].cellularNic.nrPhy.snir:vector.record = true
```

#### B. Record Throughput & Packet Success (For Availability)

Availability is calculated based on successful delivery. You need the counts of sent vs. received.

Ini, TOML

```
# App level counts for Availability (PDR)
**.app[*].sentPk:vector.record = true
**.app[*].rcvdPk:vector.record = true

# Throughput to see if the link bandwidth meets RCP minimums
**.app[*].throughput:vector.record = true
```

#### C. Record Packet Drop (For Continuity)

To calculate Continuity, you must know where and why packets were lost (e.g., during the GNB gap).

Ini, TOML

```
# Record drops at the MAC and PHY layers
**.nrMac.packetDrop:vector.record = true
**.nrPhy.packetDrop:vector.record = true
```

### 3. Critical Fix for Transaction Time ($ET$)

The ICAO RCP $ET$ (Expiration Time) is the **round-trip** or **one-way latency** (depending on the specific RCP type). You have:

`.app[*].endToEndDelay:vector.record = true`

**Warning:** In many frameworks (like Simu5G or INET), `endToEndDelay` is only recorded for _received_ packets. For RCP, you also need to account for packets that **never arrived**.

> **Tip:** In your post-simulation analysis (Python/MATLAB), you must treat "Dropped" or "Lost" packets as having an infinite delay ($ET = \infty$) when calculating your Continuity percentiles.

### 4. Summary Checklist for your `.vec` results

After running the simulation, check that your `.vec` file contains these columns:

1. **`timestamp`**: To map results to the UAV's position (especially in the "gap").
    
2. **`endToEndDelay`**: To compare against $TT_{95}$ and $TT_{99.9}$.
    
3. **`sinr`**: To correlate signal drops with the no-coverage area.
    
4. **`rcvdPk` vs `sentPk`**: To calculate the Availability percentage over the total flight duration.
    

Do you plan to use the **NTN (Satellite) link** to fill the gap between GNB 2 and GNB 3, or is the intention to show a complete loss of service in that area?




# Discussion points with Enrique
1. Structure of doc 
2. Intro and background
3. Research goals
4. How to show results 


Intro 
	Integration drones 
		C2 link relaibility 
		Current landscape of drones 
		Why we are doing and what we are doing 
		How to advanced 
		3GPP 
	Research contribution 
	- Simulator build to validate results 

- System model 
- Use-case - requirements - as the target 


delay | higher than transaction time - continuity 

Say  - RCP - Klügel work based  - Agnostics - why  - Pending
Stats of TN 
Availability 
Latency
Continuity 
explore why 
Enrique - explanation 

NTN 
including NTN - could help with outage - Implication in PBCS

Safe way 



---

To Dos  and Plan for next week 

Shreeja To do 
 - [ ]  ISl Drop 
 - [ ] Sync  background intro Pending parts
 - [ ] EDAS

---



NEver attach antenna to carbon fiber - a lot of static 
PLA
decouble the joint of the housing - to the carbon fiber 
Plate have a damper 
fuel engine drones 
disruption in EM wave 


Enrique - sionna 


---

