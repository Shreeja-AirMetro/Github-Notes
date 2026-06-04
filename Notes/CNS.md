Sss- Check CNS channels - for discussion related notes
- ![[1571100595 abstract.pdf]]


# Single map representation Discussion with Enrique 


- Information provided
	- The data exchange between the Topics 
	- ![[Screenshot from 2026-04-10 10-07-20.png]]
	-  Communication acts as a backbone between the Air unit and ground unit 
	- Therefore, CNS spans across the complete RPAS system 
	- Goal: Single Map representation at / for digital twin - surveillance 

- Points of consideration (by Enrique)
	-  This is interesting topic to tackle from technology that's new to AAM 
	- Usually this CNS bridge with map is centralized with Radar system - therefore there is a huge involvement with ATM 
	- Our research looks like a logical - functional architecture 
	- Given the complexity and the differences in technology - layering to map key parameters or details of the map representation would be a good beginning approach - that is decentralized 
	- This is today being tackled by UTM GIS planners 
	- How today these SaaS Feet management work? gap here? 
	- We can say Comm tech  provided this info on its own Map Then layered on top of Navigation map and compared the real-time with pre-planned 
	- Comm Radio map can be between the known digital twin and the real-time onboard navigation map or its updates 
	- To reduce the complexity and have effective results - Vertical category of the map information / parameters based on phases of a mission - like strategic, pre-tactical, tactical phases 
	- The density of map information (for comm) can be seen through takeoff , cruising and landing perspective 
	-  Layering of map C and N can address from the perspective of single UAV 
	- But when it comes to Surveillance - Multiple UAV in the airspace must be taken into account - How to define this? 
	-  Where does UTM play a role here - do we use U-space? 
	-  Do the parameters that "validate" the common map representation align with the RCP, RNP, RSP metrics or recommendation - Is there a SoA to address these three alignments for AAM - If not addressing this will be novel


# CNS cluster common map representation

- Common thing Data for safe operation of drone 
- Intentional target : Between drone and GCS 
- Type of data  : C: 
- N: 
- Surveillance  
- Goal: 
- Gap:
- Theoritical frmework 
- Planned actions: 


---

# CNS meeting - 26th May 

1. What are the flight phases  -> Strategic, pre-tactical and tactical 
	1. https://www.easa.europa.eu/sites/default/files/dfu/20230622-_U-space_workshop_-_7bis.pdf
	2. https://www.eurocontrol.int/sites/default/files/2023-09/eurocontrol-network-4dt-conops-v1-0.pdf
	3. U-space provide set of digital requirements / services at each phase 
2. What are the requirements of each flight phases 
3. CDM - common operation picture  in aviation aviation is ==an operational philosophy where airlines, air traffic controllers, and airport operators share real-time data to optimize flights==. This alignment minimizes delays, reduces fuel burn from taxiing, and maximizes runway efficiency through a "common operating picture


Technical , economical, regulatory -> QOS, Methods of execution, scalability
1. Questions corresponding to that 

In the context of Advanced Air Mobility (AAM), executing Beyond Visual Line of Sight (BVLOS) drone operations within Europe’s **U-space framework** requires stringent Communication, Navigation, and Surveillance (CNS) capabilities. These requirements scale in complexity across the **strategic, pre-tactical, and tactical** flight phases to guarantee airspace deconfliction, civil-manned aviation integration, and ground safety.

## 1. CNS Requirements by Flight Phase (Gemini)

### Strategic Phase (Long-term Planning to Day-Minus-1)

This phase focuses on structural safety, system-wide registration, and initial capacity planning. CNS here acts primarily as an **information and data requirement**.

- **Communication:** * **Data Exchange Architecture:** Digital interfaces to registers and e-identities.
    
    - **Strategic Planning Networks:** Requirements for secure internet-based data distribution networks to interface with U-space Service Providers (USSPs) and Common Information Service Providers (CISPs).
        
- **Navigation:**
    
    - **Geo-awareness Data Integration:** Downloading up-to-date 3D digital maps, terrain data, population density datasets, and static airspace constraints (e.g., permanent no-fly zones).
        
- **Surveillance:**
    
    - **Registry Verification:** System-level verification of digital drone IDs, operator credentials, and valid e-registrations across EU databases.
        

### Pre-Tactical Phase (Day-of-Flight to Minutes Before Takeoff)

This phase centers around **Flight Plan Authorization** and initial risk assessment before the aircraft leaves the ground.

- **Communication:**
    
    - **U-space Flight Authorization Service:** Submission of the digital flight plan (4D trajectory: latitude, longitude, altitude, and time) via an internet or cellular link to the USSP.
        
    - **Strategic Deconfliction:** The USSP assesses the path against other drone trajectories and sends back a binding digital approval or modification.
        
- **Navigation:**
    
    - **GNSS Health & Weather Monitoring:** Checking GNSS constellation status (e.g., GPS, Galileo) and Space Weather (solar flares impacting signal accuracy). Receiving real-time localized micro-weather data to ensure environmental limits are not breached.
        
- **Surveillance:**
    
    - **Dynamic Constraint Checking:** Verifying temporary airspace restrictions (NOTAMs, temporary dynamic geozones active for state or emergency flights).
        

### Tactical Phase (In-Flight / Real-Time Operations)

The most critical phase for safety, demanding highly reliable, real-time physical CNS links with strict **latency, integrity, and availability** targets.

- **Communication:**
    
    - **Command & Control (C2) Link:** Extremely low-latency, highly secure telemetry link between the Ground Control Station (GCS) and the drone (often utilizing SATCOM or robust 4G/5G cellular networks with dual-SIM routing).
        
    - **Dynamic Geo-fencing Alerts:** The drone must be capable of receiving real-time geozone updates while airborne and automatically modifying its trajectory if an active zone is breached.
        
- **Navigation:**
    
    - **High-Integrity Positioning:** Primary reliance on Multi-Constellation GNSS (Galileo + GPS) enhanced by EGNOS (European Geostationary Navigation Overlay Service) or RTK (Real-Time Kinematic) for centimeter-level accuracy.
        
    - **Alternative Position, Navigation, and Timing (A-PNT):** For high-risk AAM urban environments, dead reckoning, inertial measurement units (IMUs), or vision-based navigation are required as backups during GNSS-jamming/spoofing incidents.
        
- **Surveillance:**
    
    - **Network Remote Identification (Network RID):** The drone must continuously broadcast its current position, altitude, speed, heading, operator ID, and emergency status via the internet to the USSP.
        
    - **Direct Remote ID (DRI):** Local broadcast of the flight state over Bluetooth or Wi-Fi for ground law enforcement and nearby airspace users.
        
    - **Detect and Avoid (DAA):** Active tactical surveillance using cooperative inputs (ADS-B In, FLARM) and non-cooperative sensors (radars, cameras, or LiDAR) to maintain separation from manned aircraft and other drones.
        

## 2. Technical Documentation Framework in the EU

European drone and AAM operations are dictated by a tightly interwoven triad of **Hard Regulation (EASA)**, **Operational Concepts (EUROCONTROL)**, and **Technical Performance Standards (EUROCAE)**.

```
       [ EASA ]  ---> Mandates "What" must be achieved (Regulations / AMC & GM)
          |
  [ EUROCONTROL ] ---> Outlines "How" airspace works (ConOps / Airspace Integration)
          |
     [ EUROCAE ]  ---> Standardizes "Technical Spec" of the hardware (ED-xxx standards)
```

### EASA (European Union Aviation Safety Agency)

EASA provides the overarching European legal mandates. For BVLOS and AAM, the primary documents are:

- **Regulation (EU) 2019/947 & 2019/945:** The foundational European drone regulations. BVLOS operations typically fall into the **"Specific" category**, requiring a **SORA (Specific Operations Risk Assessment)** to calculate safety goals, or the **"Certified" category** for heavy urban AAM / passenger transport.
    
- **Regulation (EU) 2021/664 (The U-space Regulation):** The core legal framework defining the mandatory services (Network RID, Geo-awareness, Flight Authorization, Traffic Information) that enable automated BVLOS.
    
- **AMC & GM to U-space Regulation:** EASA's Acceptable Means of Compliance and Guidance Material which translate abstract laws into practical design objectives for USSPs and operators.
    
- **SC-Light UAS (Special Condition):** EASA's strict certification requirements for the airworthiness of drones used in medium-to-high-risk operations.
    

### EUROCONTROL

EUROCONTROL handles structural ATM integration and network performance.

- **U-space Concept of Operations (ConOps):** Developed heavily alongside the SESAR Joint Undertaking (SESAR JU), these documents act as blueprints for how U-space scales across Europe (from basic Corridors to advanced Urban Air Mobility).
    
- **CNS Evolution Plan:** Outlines the high-level infrastructure map (radio spectrum frequencies, satellite deployment, terrestrial antennas) needed to support legacy aviation alongside millions of new drone movements.
    
- **U-space European Architecture Documents:** Detailing the technical data exchange mechanisms between Air Traffic Control (ATC) and civilian USSPs.
    

### EUROCAE (European Organisation for Civil Aviation Equipment)

EUROCAE creates the granular, technical Minimum Operational Performance Standards (**MOPS**) that manufacturers must meet to pass EASA's requirements.

- **ED-269:** Standard for **Geofencing / Geo-awareness** data, defining how 3D spatial geometry and constraints must be formatted and read by the drone.
    
- **ED-282:** Minimum Operational Performance Standard for **U-space Flight Authorization** and **Network Remote ID**, dictating parameters like update rates, messaging syntax, and security protocols.
    
- **ED-271 / ED-318:** Performance standards for **C2 Data Link Systems**, highlighting structural requirements to combat signal attenuation, latency spikes, and link losses.
    
- **ED-309 / ED-320:** Performance specifications for **Detect and Avoid (DAA)** systems in both cooperative and non-cooperative environments.
    

Are you developing hardware/software to comply with a specific SORA SAIL level, or are you designing a U-space service?


---

https://www.preprints.org/manuscript/202602.0402


https://github.com/nareshdama/UTMsim

