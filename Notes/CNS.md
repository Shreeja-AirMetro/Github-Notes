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

- findings quantified the operational envelope where multi-provider coordination provides net benefit and established empirical baselines for federated UTM deployment strategies.
- International Civil Aviation Organization (ICAO) guidance, the Federal Aviation Administration (FAA) UTM Concept of Operations version 2.0, NASA’s Technical Capability Level (TCL) demonstrations, and the European U-space framework collectively defined core service requirements including International Civil Aviation Organization (ICAO) guidance, the Federal Aviation Administration (FAA) UTM Concept of Operations version 2.0, NASA’s Technical Capability Level (TCL) demonstrations, and the European U-space framework collectively defined** **core service requirements including strategic conflict management, tactical deconfliction, conformance monitoring, and distributed information sharing**

frameworks anticipated operational ecosystems consisting of multiple UAS Service Suppliers (USS) or Common Information Service (CIS) providers interconnected through standardized exchanges and supervised by air navigation service providers or competent authorities

, existing guidance documents intentionally remained implementation-agnostic regarding detailed technical architectures, explicit module boundaries, federation protocols, and ecosystem-level monitoring arrangements. While this flexibility supported innovation, it created challenges for interoperability verification, systematic performance comparison, and the development of evidence-based standards.  flexibility supported innovation, it created challenges for interoperability verification, systematic performance comparison, and the development of evidence-based standards

**Architectural specification gap**: Absence of published experimental frameworks with explicit module boundaries, standardized interfaces, and clear separation of concerns aligned with international frameworks.

**Federation mechanism gap**: Lack of concrete, evaluable implementations for multi-provider coordination including intent exchange protocols, constraint dissemination patterns, and health monitoring aggregation.

**Quantitative evaluation gap**: Limited empirical evidence characterizing performance trade-offs of federated versus centralized configurations across operationally relevant demand and communication regimes.

Research output - five-layer decomposition (strategic planning, tactical monitoring, safety/ecosystem monitoring, identity/security, federation/energy interfaces)
explicit event processing, parametric traffic generation (Poisson arrivals), and communication modeling (exponential delays),

**Do communication have exponential delays** 

---


# ICAO Annex 10  Vol 2

![[Screenshot from 2026-06-05 13-09-53.png]]
![[Screenshot from 2026-06-05 13-11-09.png]]
![[Screenshot from 2026-06-05 13-11-54.png]]![[Screenshot from 2026-06-05 13-12-19.png]]

![[Screenshot from 2026-06-05 13-27-50.png]]![[Screenshot from 2026-06-08 09-43-52.png]]


# Volume III
![[Screenshot from 2026-06-08 10-23-32.png]]
![[Screenshot from 2026-06-08 10-23-46.png]]
![[Screenshot from 2026-06-08 10-24-07.png]]
![[Screenshot from 2026-06-08 10-24-51.png]]


PBCS 9869
![[Screenshot from 2026-06-08 10-26-37.png]]![[Pasted image 20260608102744.png]]
![[Screenshot from 2026-06-08 10-39-08.png]]
![[Screenshot from 2026-06-08 12-15-01.png]]

![[Screenshot from 2026-06-08 12-15-25.png]]


------

# Roshan Meeting - Stratergic Phase - Radio map - 6th OCt 


Risk assesment 
Probability disbruction 
Antenna orientation 
Position 
Monte carlo analyse space 
Avg SINR in each cure - Probability of outage 

Change with Isotropic reciever 
Should We change isotopric
Position variable 

Monte carlo sampling each cube
Full space as cube
https://clickhouse.com/docs/zh/get-started/use-cases/choosing-a-service
https://www.bundesnetzagentur.de/DE/Vportal/TK/Funktechnik/EMF/start.html

Ray tracing changes the role of the two TRs. You no longer need their path-loss or LOS-probability models, because Sionna computes propagation from the actual Frankfurt geometry. They still matter in two other places.

**What you still take from the standards**

- **38.901 is still your BS model.** Sionna RT has the 38.901 antenna element built in (`pattern="tr38901"`). Use it in a planar array, set a realistic downtilt through the transmitter's `orientation` (or `look_at` toward a ground point), and use 3 sectors per site. The resulting sidelobe structure is what makes the UAV map realistic. Use the real site positions and heights from the EMF database, not the 25 m and ISD grid.
- **36.777 becomes your sanity check.** Compare path gain against 2D distance at each altitude layer with the UMa-AV and RMa-AV curves. Your map won't match them exactly, and it shouldn't, but large deviations usually point to a scene or material problem. This comparison is also a good validation figure for a paper.

**A minimal setup (Sionna RT 1.x)**

```python
from sionna.rt import load_scene, Transmitter, PlanarArray, RadioMapSolver

scene = load_scene("frankfurt.xml")      # Mitsuba scene from OSM/LoD2
scene.frequency = 3.6e9                  # n78
scene.tx_array = PlanarArray(num_rows=8, num_cols=4,
                             vertical_spacing=0.5, horizontal_spacing=0.5,
                             pattern="tr38901", polarization="V")
scene.rx_array = PlanarArray(num_rows=1, num_cols=1,
                             vertical_spacing=0.5, horizontal_spacing=0.5,
                             pattern="iso", polarization="V")

# one Transmitter per sector, real EMF position/height, downtilt via orientation
scene.add(Transmitter(name="site0_s0", position=[x, y, h_bs],
                      orientation=[yaw, tilt, 0.0], power_dbm=46))

solver = RadioMapSolver()
maps = {h: solver(scene, max_depth=4, samples_per_tx=10**7,
                  cell_size=[5, 5], center=[cx, cy, h], size=[W, L])
        for h in [30, 60, 90, 120]}       # altitude layers for flight planning
```

**Points specific to UAV flight planning**

- **Plot SINR, not only RSS.** At 100 m and above a UAV sees many sites in line of sight. The RSS map will look excellent while SINR collapses, which is the 36.777 effect. The radio map gives you per-transmitter values, so you can compute best-server RSS and SINR from them.
- **Use altitude layers.** Sweep `center[2]` over your planned flight levels and add finer steps where you take off and land.
- **Scene.**
    - Hessen LoD2 gives better roof geometry than OSM extrusions, which matters for rooftop-mounted sites.
    - Assign ITU materials, at least concrete and glass for the towers.
    - Check whether your Sionna version includes edge diffraction and enable it, since it matters below rooftop level.
- **Stadtwald.** Trees aren't in the mesh. Above the canopy this is harmless. For low altitudes over the forest, add a vegetation loss term (38.901 has a foliage model) or treat those areas as uncertain.
- **Validation.** If you or your chair can collect a few RSRP measurements, even from a drive along the Main river, use them to calibrate the materials and transmit powers. Reviewers in this area increasingly expect that.

I can write the full pipeline if that helps: load the EMF site list, place the sectored transmitters with downtilt, run the altitude sweep, and export best-server RSS and SINR maps.


**For a flight-planning radio map, use 36.777 for the flight altitudes and 38.901 for the base stations and the low-altitude parts.**

UAVs in the EU open category fly up to 120 m, and corridors usually sit around 30–120 m. Almost all of the map you care about is therefore above about 22.5 m, where 38.901's UE models are no longer valid. So:

- **Altitude layers above about 22.5 m** (cruise): use the 36.777 aerial path loss, LOS probability and shadowing (UMa-AV in the city, RMa-AV over the Stadtwald).
- **Altitude layers below that** (take-off and landing): use 38.901 UMa/UMi.
- **Every layer:** use the 38.901 BS antenna pattern, with realistic downtilt (around 6–10°). The antenna pattern matters more than the path-loss model for a UAV radio map. At 100 m altitude you are above the main lobe of nearby sites, so RSRP is shaped by sidelobes and nulls, and the strongest cell is often a distant one. If you leave out the pattern, the map will look far too good.

**One caveat:** both TRs are statistical. They give you average signal strength against distance and height, not "behind this specific tower the signal drops." That works for planning-level coverage maps per altitude layer. For a site-specific map of Frankfurt, where buildings like the Main Tower and the Messeturm cast real shadows, the stronger approach is ray tracing (e.g., Sionna RT or Wireless InSite) on a 3D building model. You'd place the real EMF-database sites in it and use 38.901/36.777 to validate or calibrate. Hessen publishes LoD2 3D building models as open geodata, which as far as I know cover Frankfurt. It's worth checking the HVBG portal.

**ISD = inter-site distance**

ISD is the distance between neighbouring base-station sites in the regular (usually hexagonal) grid that 3GPP uses to lay out a simulated network. Each site typically has 3 sectors. Standard values:

|Scenario|ISD|BS height|
|---|---|---|
|UMi (street-level small cells)|200 m|10 m|
|UMa (city macro)|500 m (200–500 m allowed)|25 m|
|RMa (rural)|1732 m (or 5000 m)|35 m|

Smaller ISD means denser sites, more capacity and more interference. ISD only matters if you build a synthetic grid. With the real EMF site positions there is no single ISD, though you can compute the average nearest-neighbour distance and report it as the "effective ISD" of central Frankfurt.


**Use both, each for its own part of the problem.** They aren't competitors: TR 36.777 is an extension that adds aerial UEs on top of the same deployment scenarios. If your UAVs fly above about 22.5 m, 38.901 alone isn't valid for them.

**What each one covers**

||TR 38.901|TR 36.777|
|---|---|---|
|Purpose|General 5G NR channel model (0.5–100 GHz)|LTE support for aerial vehicles (Rel-15)|
|UE height|Ground and in-building users. UMa UE heights go up to about 22.5 m|Aerial UEs from 1.5 m up to 300 m|
|Scenarios|UMa, UMi, RMa, InH|UMa-AV, UMi-AV, RMa-AV (same BS layouts and BS heights: 25 / 10 / 35 m)|
|Gives you|Layout, BS antenna pattern and downtilt, ground-UE path loss, LOS probability, fast fading|Height-dependent LOS probability, path loss and shadowing for UAVs|
|Frequency|Validated over the full range|Calibrated around 2 GHz. Applying it at 3.5 GHz (n78) is common practice but is an extrapolation|

**How to combine them in practice**

- **Network layout and BS parameters:** take these from 38.901 (25 m UMa, ISD, 3-sector, antenna array and tilt). Or better, use your real EMF-database sites and heights.
- **Ground UEs and UAVs below the threshold:** use 38.901 path loss and LOS. The threshold is about 22.5 m for UMa/UMi and about 10 m for RMa.
- **UAVs above the threshold:** switch to the 36.777 Annex A aerial models. In these models the LOS probability goes to 1 above a certain height (around 100 m in UMa), and path loss tends toward free space.
- **Fast fading:** 36.777 reuses the 38.901 framework, with modified parameters for aerial UEs.

**Which one to name in a paper**

Something like "3GPP TR 38.901 deployment with aerial-UE channel extensions per TR 36.777" is the standard phrasing, and reviewers expect it. Rel-18 NR support for UAVs reused the 36.777 aerial models rather than defining new NR-specific ones, so citing 36.777 for an NR study is accepted. Newer Rel-19 work on 38.901 adds some UAV-related channel modelling, mainly for sensing/ISAC. Check the latest version of 38.901 before you finalise, in case something more directly applicable now exists there.

For a Frankfurt scenario: below 22.5 m, use the 38.901 UMa models. Above that, use the UMa-AV models from 36.777, which are what show the interference effect from many sidelobes that I mentioned earlier.


I'll look up public sources for 5G site locations and antenna heights in Frankfurt.

Yes, but you have to combine sources. No single public dataset gives you "5G base stations in Frankfurt with their heights." There is one official source for real site locations and antenna heights, one crowd-sourced source that tags 5G (NR), and a standard you can fall back on for modelling heights.

**1. Real site locations: Bundesnetzagentur EMF-Datenbank (best source)**

In Germany, fixed radio installations with an EIRP of 10 W or more need a site certificate (Standortbescheinigung) from the Bundesnetzagentur before they can go into operation. The resulting EMF database contains all transmitters that need such a certificate, shown on a map, so anyone can look up mobile antennas in their area. Small-cell sites that must be reported are included as well, which matters in a dense area like the Frankfurt core.

For your map (Innenstadt/Bankenviertel, Sachsenhausen, Stadtwald, Offenbach), you can zoom the EMF map to the same area and read off each site. As far as I know, each site entry also lists the antenna mounting heights and safety distances. That gives you real heights, not assumed ones.

The limitation is that a site is not labelled "5G." Most sites in central Frankfurt are multi-band (LTE plus NR), so you need step 2 to tell which ones carry NR.

**2. Telling which sites carry 5G: OpenCelliD**

OpenCelliD is an open, crowd-sourced database of tens of millions of cell records with coordinates, and each record has a radio type, where NR denotes 5G. You can filter for MCC 262 (Germany), `radio = 'NR'`, and the bounding box of your map.

There are two limitations:

- The coordinates are estimated from where phones heard the cell. They are not the mast position and have no height.
- NR coverage in the data is thin.

A practical approach is to snap each OpenCelliD NR record to the nearest EMF site to get the real position and height. CellMapper is often more complete for German NR, but its terms of use restrict scraping.

**3. Base station height for modelling (if you need a synthetic layout)**

3GPP TR 38.901, the standard 5G channel model, uses these values:

- **Urban Macro (UMa):** BS antenna height 25 m (UMi street canyon: 10 m), with inter-site distances of 200–500 m allowed for evaluations.
- **Rural/suburban macro:** BS height 35 m, UT height 1.5 m.
- The UMa assumption is based on the fact that urban macrocells usually have base stations mounted above the surrounding rooftops (about 25–30 m) and users at ground level.

Here is how I'd apply this to your map:

|Area in your map|Suggested 3GPP scenario|h_BS|ISD|
|---|---|---|---|
|Innenstadt, Bankenviertel, Sachsenhausen-Nord, Offenbach centre|UMa, plus UMi small cells in street canyons|25 m (UMi 10 m)|~200–300 m|
|Residential (Niederrad, Oberrad, Lerchesberg)|UMa|25 m|~400–500 m|
|Stadtwald, A3/A5/B3 corridors|RMa|35 m|km scale|

Frankfurt's high-rises are a special case. Real rooftop sites in the core can sit well above 25 m. This is why the EMF heights are worth using for the area where you'll fly.

**A note for UAV links:** antennas at all these heights are down-tilted toward the ground. Above roughly 100 m, a drone mainly sees sidelobes from many sites. This means the true positions and heights from the EMF database shape interference far more than the generic 3GPP values do. This is also why 3GPP TR 36.777 (enhanced LTE support for aerial vehicles) reuses the UMa/RMa layouts and adds aerial-UE heights.

I can write a script that filters an OpenCelliD export to your map's bounding box and NR cells. It produces a CSV and a plot you can merge with the EMF heights. You'd need to download the export yourself, since my workspace can't reach opencellid.org.

Sources:

- [Bundesnetzagentur – EMF / EMF-Karte](https://www.bundesnetzagentur.de/emf)
- [DGUV FAQ – EMF-Datenbank](https://dguv.de/fb-etem/faq/faq_telekom/index.jsp)
- [3GPP TR 38.901 §7.2 Scenarios (itecspec mirror)](https://itecspec.com/3gpp/38.901/s/7.2)
- [Rappaport et al., Overview of mmWave Communications for 5G – propagation models (arXiv:1708.02557)](https://arxiv.org/pdf/1708.02557)
- [OpenCelliD dataset description (ClickHouse docs)](https://clickhouse.com/docs/zh/getting-started/example-datasets/cell-towers)
-

![[Pasted image 20261006105420.png]]