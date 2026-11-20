15/4 lecture - Rico Introduction
- ICT for Smartgrid comm
-  Discuss with lehnert - leistung punkte  - Student issue 
- organization ablauf
- motivation of the course -> reduce climate change -> emission and fossil energy 
- mobility - energy efficiency sector 
- Internet - control - drahtlose 
- smart grid -> control of generation and consumption 
- 5-10ms 
- 5 min kb of data - sachsen netze 
- visualize the energy grid 
- dymobat , Mobilities for EU 
- verify and optimize the communication
- Topics of interest fro students - Bidirectional charging 
- Differences in Mobilities for EU - Dresden vs Madrid - Power + mobility + Comm 
- smart home
- electric network optimization and monitoring with comnets 
- communication for virtual powerplant 
- KI for Netzoptimization like with weather or external data  - Data from hospital study - prognose 
- Oral exam - dates and appointments are flexible 
- upload the lecture a week prior 



29/4 Lecture 3 

Power line communication (PLC) by Prof Lehnert

- old technology but new research work for digital communication - eg for OFDM and related frameworks 
- hochspannungs leichtung 
- standard for PLC 
- we see only powerline as comm medium 
- smart meter reading done PLC
- standard name as G.hn - ITU standard 
- Stan - Adaptive MAC layer switching - PhD 
- History of PLC 
	- 30s carrier fre transmission on HV Power lines - amplitude modulation @ 150khz 
	- digital transmission FSK  - product standard KNX and used in home automation 
	- 98s broadband PLC 
	- Incompatibility of solutions 
	- 2000s IEEE 1901 BBPLC , 1901.2 NB PLC standard  for meter reading anwendung  then ITU G.hn BB over coax cable , fiber, PLC
- Today application 
	- Smart meter , EV charging (Typ2, AC, CCS, DC)  ladecable (NB-PLC)
	- LAN over powerline 
- Diss - Stan 
	- PLC modem with IP packet 
- Data traffic in smart grid
	- control traffic - smart packets and short delay requirement , load is small 
	- firmware update - overload may happen 
- Peak load clipping 
- Network specification 
	- As a channel  -> Highly distributed physical channel 
	- Background noise, Impulsive noise , Impedance variations 
- varying traffic on app. layer 

Questions - distance  , PoE later then PLC - complimentary?
 shared bus from BS distribution - Logical bus structure 
 - Logical bus structure 
 - high signal attenation - repeater necessary 
 - FDMA . Problem  - Bi directional propogation 
 - filter - frequency - need more frequency  - frequency reuse 
 - how conversion 
 - Powerline signal transmission 
	 - Attenuation 
	 - Noise
	 - Signal Reflections 
	 - Varying char Impedence 
	 - Multi-path propogation 
	 - Frequency selective fading 
	 - Distrurbances from network environment - RF sender - other PLC systems 
- EMC problems
	- upto 85 Mhz 
	- Notching 
- Countermeasures 
	- Spreadspectrum - ultra wideband
	- OFDM 
	- MAC layer 
	- Qos and error handling mechanism 
	- NB PLC -5km 
	- BB PLC - 250m 
- PRIME; G3 , iAd (German) , 
- Survice  NB - PRIME and G3
- OFDM 
- ITU G.hn 
- PLC : PHY model interface, Adaotaton layer to PLC, Application Interfare IP  
- PLC: Adaptation Layer and IPV6
- Instalattion with PLC layers are standards 
- see how the full PLC or adaptation in model happens
- Mobilefunk channel model  Standard impulse scenario
- PLC topography 
- PLC in LV network 
PLC in Home
- Distribution Line carrier 
- WAN  - DLC access node - And Repeater 
- ITU-G.hn - home networking 
	- OFDM 
	- Further stds - G 9960, 9961, 9963  - system architecture PhY , DATA link , MIMO and power spectral density 
	- masked subcarrier  - notching 
	- PHY frame 
		-  12 types of frames 
		- No HARQ? - retransmission 
	- FEC - block size - repitiotion encoder 
	- Payload duration 
		- Size, FEC block, FEC rate without repition , freq band 
- MAC Layer - CSMA / CA Contention 
- collision 
- Probability of successful transmission 
- bigger contention window is a disadvantage  
- Access protocol and its performance 
- Throughput to normalized transfer delay 
- Adaptive MAC switching mechanism 
- P-persistent CSMA , non persistent CSMA 
- switching mechanism - polling 
- ns3 simulation 
- Realistic Phy Throughput 
- 2 simple access mechanism instead of 1 complicated 
- Tm Tool performance measurement  - traffic management and analysis 
- seit abhanging 
- Ref - Lampe Book , Smartgrid comm 

---

protocols 

Smartgrid - digital power based communication network 
 - real time connection between producer and user 

Protocol- facilitiate data exchange and energy management 
Categories 
	- communication 
	- Energy 
	- Dual - purpose 
- tradicational comm protocols Modbus 
- SCADA systems  monitoring and control 
- protocol categories, transmissio media 
	- Query architecture 
- Remote terminal unit and TCP (types)
- MOdbus - master slaves-> multiple slaves - reliability  (interference) and security 
- MQTT based IOT protocols 
- "near real time"
- Topic based messaging  -- single level, multi-levels
Protocols and QoS 


LEVELS OF QOS - Timestamp SINR - PAket 
Then whole simulation / one data collection cycle 
Then continuity flight 
Micro - to-macroscopic levels 

OCPP - dual structure protocols 
 common standard between any type of charging station and central energy grid system 
 OCPP 1.6 - smart charging in uni directional 
 OCPP 2.0.1 for bi directional
 OCPP is not a standardized protocol 
 - division of rules between ISO 15118 and  OCPP 

EEBUS dual bus energy protocol 

EEBUS - two protocol stack - SPINE (what) , SHIP (How - path)


13/5 
Bidirectional charging 

- production is not certain 
- Demands for EV (esp in earl evening high demand)
- Transmission system operator has huge responsibility in grid stability 
- Required from Kinetic energy to electrical 
	- Physics based stability
	- Software based stability 
- no meter - no monitoring - no control 
- energy imbalance - frequency imbalance in real time 
- by rule of thumb - 15 min resolution round 
- Spain - So many fluctuation - conventional power plant cannot hold certain frequency 
- Traditional way to manage imbalance is control reserve - maintain power at 50 Hz 
- Types of control reserves
- FCR type is expensive 
- stand by and react - market to capacity for grid control | Standby and mileage pay
- Bidirectional charging - target service group - FCR
- parking lot fuse constraints 
- uncoordinated EV charging introduced PEak usages (highly likely in buildings)
- Degree of freedom 
	- Uni direction - Time and Power 
	- Bi directional - time, power and direction of power 
	- Mobility of the EV cas spatial disadvantage 
		- soln - mobility aware bi-directional charging 
- optimization locally
- parking garage - 5G network instability 
- mesh network for indoor area 
- eMSPs
- energy management locally - > global central coordination 
-  EV - AC and DC charger - BMS of car - issue 
- prediction algorithm for Smart charging in buildings
- sustainable smart charging station 
- Average Emission factors , Marginal emission factor - for planning charging 
- EV - battery degradation - calendar and cycling aging 
- "90% simulation don't work exactly in real-life"
- Use-cases -> Solution from WPs
- MILP and heuristics > better than DRL (agents - rewards) for charging plan generation 
-  redispatch - 3.0

---
Comm networks

Christopher lecture 

Conventional power grid
power plants are distributed across households 

energy - transportation- communication 

private network - tailored network performance 
data privacy - does not leave local premises 
geographically limited 

sensor to intelligence to actual point - latency is key factor 

edge computing and network slicing 


5G network 
 applications - eMBB, mMTC, URLLC (latency - bandwidth tradeoff)

latency compute triangle
autonomous cars - at low latency typical target less than 1ms
increase reliability - whats the mechanism 
 network architecture 
 UE- RAN- core and data network 
4 towers - connected via wired link - radio access network 

user path - UE- RAN - UPF - DN 

edge computing 

sensor perform task and other end there is a controller 

computation closer to the user

network slicing 

end to end approach - logically isolated domains
virtual resource separation 

service level agreement 

no slice - all compete against each  other -> uncoordinated 

slicing in a way coordinated the resources 

private 5G network 


public network have lot of dependencies 
external users affecting 

architecture 
can be deployed as a part of public network  - integrated private network 

Independent private networks 

spectrum usage 

low frequency - higher range 

private networks own frequency domain - 3.7 - 3.8 ghz - BNetzA licenses


Mesh networks 

mesh nodes - access point - management of the network and clients mode 
- self-healing 
- self-configuring 

mobilities for EU

ostra - flooding area - technical infra cannot be permanently installed 

centralized control center 

slicing concept for various operations 
	1. Safety and control 
	2. Video and perception 
	3. IOT and infrastructure 
	4. User and service s
traffic pattern 
network characteristics 
(bandwidth , latency, reliable, energy )
which layer of network place what functions 

5G network layer and functional layer 

Data network 
UPF
Edge
RAN
USer

data requirements - network slice 

flexibity  - integrated and independent 

cost factor 


slice - based on estimation 

demands  - over provisioning of the demands 



---

# Lecture 15th July

Last content 
- Forcasting, prediction and decision-making 
- optimization from grid and user side based on cpacity- behaviour analyisi 
- desicison and forcasting horizon
- inputs
- methods
- duration 
- key problems - variables, drivers, features 
- event prediction - regression, classification and multi-step regression 
- forcasting pipeline - 7 steps with pre and post processing 
- feature category 
- persistence 
- ARIMA
- ML - Linear regression - Desicion tree
- diff tree models 

Ques: 
Cluster : 
remove outliers 


---
# ICT for Smart Grids — Oral Exam Study Guide

_Summary of all 8 lectures, TU Dresden, Sommersemester 2026_

---

## Lecture 1 — Intro & Organisation

- Course is part of Modul "Kommunikationstechnik" (RES-WK-45), alongside "Kommunikationsnetze" (Prof. Fitzek).
- Lecturers: Dr. Rico Radeke, Prof. Ralf Lehnert + guests (Razan Habeeb, Shiwei Shen, Christopher Lehmann, Syed Irtaza Haider).
- Exam: **oral, 30 min** if <15 participants, otherwise written 90 min.
- Two topic areas: (1) Kommunikationsnetze — network principles, OSI model, access methods; (2) ICT for Smart Grids — IoT PHY/MAC layers, databases, ML, network security.

---

## Lecture 2 — Network Technologies

**Power network hierarchy:** generation → Transport (HV, ≥110 kV) → Distribution (MV 10-20 kV, LV 400 V) → Consumer. Voltage levels: UHV ≥220 kV, HV 110 kV, MV 10-20 kV, LV 400 V.

**Future grids:** renewables connect at _all_ layers → volatile generation → need energy buffers + sector coupling + comms network for stability.

**Smart Meter Gateway (SMGW)** — 3 interfaces:

- **WAN**: secure (IP/TLS) link to metering company
- **LMN** (Local Metrological Network): to smart meter(s) — can include gas/water too
- **HAN** (Home Area Network): to HEMS / home devices; controls bidi charging via "switch box"

**NIST (2009) definition of Smart Grid:** integrates generation, transport, storage, management, consumption + communications; goal = save energy. Consists of energy transport + communication + control network.

**Communication requirements table** (per household):

|Application|Data rate|Latency|
|---|---|---|
|Meter reading|10 bps|1–15 min|
|Distributed power control|<100 bps|<1 s|
|Firmware update|>10 kbps|1–10 min|
|Home appliance control|10–10,000 bps|1–60 s|

**Access technologies (LV layer):**

|Tech|Data rate|Latency|Notes|
|---|---|---|---|
|xDSL (VDSL)|1–250 Mbit/s|10–100 ms|copper, non-shared|
|Digital Cable TV (DOCSIS 3.1)|16–1000 Mbit/s|~15 ms|shared, #2 worldwide|
|LTE (4G)|375/100 Mbit/s|~30 ms|shared|
|5G|1/1 Gbit/s|<10 ms (goal 1ms)|shared|
|NB-IoT|30/60 kbit/s|1.5–10 s|robust, reaches basements|
|LTE-m|300/375 kbit/s|50–100 ms|shared|
|LoRaWAN|0.3–50 kBit/s|—|wide area IoT|
|WLAN (802.11)|up to 20 Gbit/s|~20 ms|shared, ≤100 m|
|ZigBee (802.15.4)|≤250 kbit/s|—|wireless sensor nets, battery|
|Starlink|100/25 Mbit/s|~50 ms|shared|
|PLC|—|—|uses existing wires, shared|

**Selection criteria:** PLC/xDSL reuse existing infra (no civil works); PLC is shared medium but utility owns the LV cabling everywhere. Fiber = non-shared (AON) but installation ongoing.

**Reliability:** SG comms needs very high availability — redundancy (routers, power supplies, alternate paths, alternate tech).

---

## Lecture 3 — Power Line Communications (PLC)

**History:** 1930 carrier freq over HV (AM @150 kHz) → 1990 digital FSK (KNX) → 1998 broadband PLC (proprietary) → 2007 IEEE 1901 (BB-PLC) → 2009 IEEE 1901.2 (NB-PLC) → 2010 ITU G.hn.

**Traffic types:** Control (small packets 64-128B, ms delay, guaranteed first-TX delivery), Firmware update (>1000B, high throughput, retransmit OK), Meter reading (100% reachability needed).

**Channel problems:** attenuation, noise (background Gaussian + impulsive), signal reflections, varying impedance, multi-path propagation, frequency-selective fading. **EMC**: PLC radiates up to 85 MHz → interferes w/ short-wave radio → regulators cap power / notch frequencies.

**Countermeasures:** robust modulation (OFDM, spread-spectrum), efficient MAC layer, error handling.

**NB vs BB PLC:**

||NB-PLC|BB-PLC|
|---|---|---|
|Freq|9–148.5(500) kHz|up to 85 MHz|
|Distance|up to 5 km|up to 250 m|
|Cost|low|higher|
|Speed|80 kbps|500+ Mbps|

**Surviving standards:** NB-PLC → PRIME, G3. BB-PLC → IEEE 1901 (Homeplug), ITU G.hn. Modulation: **OFDM**.

**ITU G.hn:** one standard for coax/telephone/power lines. 3 band profiles:

|Baseband|Subcarriers|Effective range|
|---|---|---|
|25 MHz|1024|1.8–25 MHz|
|50 MHz|2048|1.8–50 MHz|
|100 MHz|4096|1.8–80 MHz|
|Subcarrier spacing: 24.4 kHz (all profiles). Masked: subcarriers 0-74 and 3276-4095 (>80 MHz not allowed by regulation).|||

Standards docs: G.9960 (PHY/architecture), G.9961 (data link layer), G.9963 (MIMO), G.9964 (PSD).

**PHY frame types (12):** MAP/RMAP, MSG, ACK, RTS, CTS, CTMG, PROBE, ACKRQ, BMSG, BACK, ACTMG, FTE. FEC block size 120/540 byte; FEC rates 1/2, 2/3, 5/6, 16/18, 20/21.

**MAC layer:** CSMA/CA (contention-based) vs TDMA (scheduled). **Adaptive MAC switching**: observe traffic load + channel conditions → switch to more efficient protocol; hysteresis at switching point for stability; master-slave architecture; switching happens per MAC cycle (40 ms for G.hn).

- CSMA/CA → TDMA: triggered when load > threshold+w
- TDMA → CSMA/CA: triggered when load < threshold−w

**Performance:** realistic G.hn PHY throughput 70-80 Mbps (1518B payload) or 1-3 Mbps (64B payload). Adaptive switching = "2 simple mechanisms instead of 1 complicated."

---

## Lecture 4 — Smart Grid Protocols

**3 categories:** Communication (Modbus, MQTT — data transfer), Energy (ISO 15118 — energy-specific ops), Dual-Purpose (OCPP, EEBus — both).

### Modbus

- Developed **1979**, application layer (L7), master/slave model.
- Query = Function Code + Data Bytes + Check Field. Response = Function Code + Data/Error + Error Check.
- Key function codes: 01 Read Coils, 03 Read Holding Registers, 04 Read Input Registers, 05 Write Single Coil, 06 Write Single Register, 15/16 Write Multiple Coils/Registers.
- **Modbus RTU**: serial (RS-485), daisy chain, binary, ≤1.2 km, slower, simple/reliable.
- **Modbus TCP**: Ethernet/TCP/IP, encapsulates RTU messages, global distance, faster.
- Packet length: RTU 5-256 bytes; TCP up to 260 bytes (MBAP header).
- Limitations: slow (esp. RTU), basic error handling (CRC only), overhead, poor scalability for large/complex nets.

### MQTT

- Developed 1999, v3.1 royalty-free 2010, ISO standard 2016. Application layer, M2M, over TCP/IP.
- **Publish-Subscribe** via a broker; topic-based (e.g. `sensors/temperature/room1`); wildcards `+` (single level) and `#` (multi-level).
- **QoS levels:**
    - QoS 0 (At Most Once): no ACK, may be lost, no duplicates
    - QoS 1 (At Least Once): ACK'd, resent if no ACK → duplicates possible
    - QoS 2 (Exactly Once): 2-step handshake, no loss, no duplicates
- Challenges: QoS trade-offs, interoperability across versions, flat topic hierarchy, broker = single point of failure.
- Limitations: needs TLS for real security; limited bidirectional comms (devices can't talk directly to each other); not for strict real-time.

### OCPP (Open Charge Point Protocol)

- Developed 2009, application layer (L7), connects charging stations ↔ **Central Management System (CMS)**.
- Client-Server: charger = client, central system = server.
- Versions: 1.2, 1.5, 1.6 (widely used), 2.0, 2.0.1.
- **OCPP 1.6**: basic smart charging, real-time monitoring, flexible pricing, improved security.
- **OCPP 2.0.1** (2020): bidirectional charging (V2G) support, improved load balancing, strong security (certificates), supports ISO 15118 (Plug & Charge).
- Charging sequence: Reservation → Identification/Authorization → Charging begins → real-time updates → session ends → invoicing.
- Limitations: not officially ISO-recognized, requires central system, advanced features need newer versions.

### ISO 15118

- Communication standard **between EV and charging station**. First version 2013, latest ISO 15118-20:2022. Categorized as an **Energy Protocol**.
- Features: secure/encrypted comms; **Plug & Charge** (auto-authentication, no manual input); V2G support (bidirectional energy flow).
- Limitations: still evolving, complex security/certificate setup, doesn't cover internal vehicle communication.

### OCPP + ISO 15118 relationship

- **ISO 15118**: EV ↔ Charger. **OCPP**: Charger ↔ CMS.
- Flow: EV states needs (ISO 15118) → Charger relays to CMS (OCPP) → CMS optimizes & sends instructions back → Charger applies to EV.

### EEBus

- Communication standard for **energy management** (smart homes, buildings, EV charging, heat pumps, PV). Not officially standards-body recognized.
- **Two-layer stack:**
    - **SPINE** (Smart Premises Interoperable Neutral message Exchange) — _what_: structures energy info, ensures interoperability.
    - **SHIP** (Smart Home Interface Protocol) — _how_: device-to-device comms, IP-based (TCP/UDP) over Wi-Fi/Ethernet.
    - Mnemonic: "SPINE defines the message, SHIP delivers it."
- How it works: device maps internal data → EEBus message → sent to EMS → EMS optimizes/coordinates → sends commands back.
- Example: EV charger has 0-11 kW flexibility → EMS limits to 5 kW → peak reduced.
- SGAM layers: Physical → Communication (SHIP) → Information (SPINE) → Function.

---

## Lecture 5 — Bidirectional Smart Charging (DymoBat project)

**Context:** German EV share grew from 1.05% (2018) to 13.5% (2024); target 15M EVs by 2030; fleet electrification could need 130 TWh (~25% of today's consumption).

**Conventional grid:** unidirectional, TSO = active (stability/balance), DSO = passive (maintenance). More renewables/EVs → local power imbalance, less inertia, limited visibility (only SCADA gives visibility centrally).

**Control Reserve** (keeps grid at 50 Hz): Positive (freq drops, increase gen/reduce consumption) vs Negative (freq high, decrease gen/increase consumption).

|Type|Activation time|Notes|
|---|---|---|
|FCR|within 30 s|automatic, Europe-wide, first response|
|aFRR|within 5 min|automatic, by TSO in control area|
|mFRR|within 12.5 min|manual, severe imbalances|

- Procurement via **regelleistung.net**; markets: Balancing Capacity (standby) vs Balancing Energy (activated).
- Germany's 4 TSOs cooperate via **Grid Control Cooperation (GCC)**.

**EV potential:** EVs idle ~95% of time, chargers idle ~80%. 10M EVs × 50 kWh = 500 GWh potential storage (even 20% participation = 100 GWh). Target service group: **FCR**.

**Smart charging use cases:**

- **V2H** (Vehicle-to-Home): self-sufficiency, tariff optimization, blackout support
- **V2G** (Vehicle-to-Grid): arbitrage, redispatch, FCR, reactive power balance, CO2-optimized charging
- **V2B** (Vehicle-to-Building): peak load shaving, fleet management
- **V2V** (Vehicle-to-Vehicle): emergency

**Degrees of freedom:** Unidirectional (time+power) → Bidirectional (+direction) → Mobility-aware bidirectional (+space).

**CO2 factors:** AEF (average emissions factor, shared responsibility) vs MEF (marginal emissions factor, full responsibility for marginal change). Use AEF for day-ahead planning, MEF for intraday.

**Battery protection:** minimize charge/idle/discharge transitions; restrict min SoC for discharge; restrict full-cycle equivalents. Aging = calendar aging + cycling aging (temp, C-rate, DoD, throughput).

**4 Work Packages (DymoBat):** WP1 local EMS/DER control, WP2 Hub Coordinator (multi-EMS via 5G Campus Network), WP3 optimization algorithms, WP4 testbeds (Barkhausenbau, SAP e-mobility, virtual sim).

**5 Use Cases:** UC1 predictive optimization (single cell), UC2 Redispatch 3.0 / flexibility market via Hub Coordinator, UC3 multi-site testbeds (hospital, ComfortCharge, SachsenEnergie w/ OCPP 2.1, SAP Walldorf), UC4 5G+mesh comms across testbeds, UC5 fast charging in grid-constrained areas.

---

## Lecture 6 — Communication Networks (5G, Mesh)

**Smart city tech:**

- **Private networks**: licensed spectrum, dedicated infra, tailored performance + privacy/security, but limited geographic coverage.
- **Edge computing**: real-time processing close to core network (latency vs computing power tradeoff).
- **Network slicing**: end-to-end virtual resource separation; benefits = flexibility, security via isolation, guaranteed SLAs.

**5G architecture:** UE → RAN → Core Network (CN) containing **AMF** (Access & Mobility Function), **SMF** (Session Management Function), **UPF** (User Plane Function) → Data Network (DN).

**WLAN vs Mesh:**

- WLAN: unlicensed ISM band, Access Point + Clients, all traffic through AP.
- Wireless Mesh: unlicensed band, distributed management, every node connects to multiple other nodes.
- Mesh characteristics: multi-hop (coverage), self-healing (reroute), self-configuring, scalable, redundant (parallel paths), dynamic topology.
- Mesh as 5G extension: covers shadowing/reflections, indoor/underground areas where 5G signal is weak.

**Mobilities for EU project:** urban mobility, CO2 reduction, EU-funded. Dresden activities: traffic planning, autonomous vehicles, sensors, charging, comms network, data center. Scenario: remote-controlled car → parking → bidi charging based on green energy availability + grid load prediction, using network slicing for different traffic types (real-time commands vs long-term stats).

---

## Lecture 7 — Optimization

**Context:** rising PV at household level → negative residual load possible (Germany, April 10 2023). Residual load = demand − renewable generation. EV charging can shift demand to PV-rich hours.

**DSM strategies:** Peak clipping (reduce max capacity need), Valley filling (increase demand in low-load periods), Load shifting (move load peak→off-peak, same total energy).

**Demand Response (DR):** Incentive-based (external/contractual control) vs Price-based (CPP, RTP, TOU reactive pricing).

**EVs vs stationary batteries as flex resources:**

||Batteries|EVs|
|---|---|---|
|Pros|fast response, high control, decoupled|growing deployment, distributed storage, flexible|
|Cons|high cost, footprint, limited scale|individual flexibility limited, needs aggregation, user constraints|

**Charging control strategies:**

|Approach|Idea|Limitation|
|---|---|---|
|Uncoordinated|charge immediately|grid overload|
|Decentralized|each EV decides|no global optimality|
|**Centralized** ✓|aggregator optimizes all|computational complexity|

**Aggregator role:** collects EV data, infra limits, grid constraints, price signals → coordinates globally → output = charging power per EV per time.

**EV scheduling problem:** Inputs (arrival/departure, energy demand, PV forecast, prices, grid limits) → Decision (charging power per EV per timeslot) → Output (charging schedule).

### 4 Optimization Methods

1. **MILP** (Mixed Integer Linear Programming): continuous vars (power) + integer vars (on/off); linear objective + constraints. **Global optimum**, handles hard constraints, mature solvers — but computationally expensive for large fleets, needs accurate forecasts, hard to model nonlinear behavior.
2. **Heuristics** — rule-based, fast, no optimality guarantee:
    - FCFS (arrival order, no PV/ToU awareness)
    - EDF (prioritize by departure deadline)
    - RRES (equal power split, ignores urgency)
    - LLF (prioritize least remaining flexible time)
    - **SGH** (Schedule Guided Heuristic): Phase A = use available PV first (by priority); Phase B = grid top-up during low ToU prices, override if deadline at risk.
3. **Metaheuristics** — search large solution spaces:
    - Evolutionary Algorithms (**GA** — gene/chromosome/population/fitness function; operators: selection, crossover, mutation)
    - Swarm Intelligence (**PSO**)
    - GA mapping: gene = 1 charging decision, chromosome = full schedule, population = multiple candidate schedules. Constraints handled via repair operators/penalty functions (not inherently enforced).
4. **Deep Reinforcement Learning (DRL)**: learns a policy via agent/environment/state/action/reward.
    - Mapping: Agent=aggregator, Environment=workplace system, State=SoC+time+PV+price, Action=charging power per EV, Reward=cost+PV use+constraint satisfaction, Episode=one charging day.
    - Value-based (DQN, off-policy, discrete) vs Policy-based (PPO, on-policy, continuous/discrete) vs Actor-Critic (**SAC**, off-policy, continuous — best fit here).
    - **SAC**: model-free, off-policy, maximum entropy RL + actor-critic. Actor network = outputs action distribution; Critic network = estimates soft Q-value. Uses twin critics to reduce overestimation bias; more stable than other RL methods but computationally heavy to train, needs lots of data, hard-constraint satisfaction is difficult, "black box."

**MILP vs SGH comparison:** MILP = solver-based, global optimum, higher computation, scalability-limited. SGH = rule-based, good feasible solution, very fast, no optimality guarantee.

**Real example (20 EVs, day-ahead):**

|Method|Cost (€)|Grid Energy (kWh)|PV Share (%)|Peak Import (kW)|
|---|---|---|---|---|
|MILP|25.70|85.67|80.3|47.9|
|GA|30.21|92.45|79.1|34.3|

**Day-ahead vs intraday:** Day-ahead = planning (forecasts) → baseline schedule. Intraday = correction (updated real-time data) → adjusted actions. Suggested hybrid: MILP/GA for day-ahead baseline; SGH/DRL/rolling-horizon MILP for intraday correction.

---

## Lecture 11 — Forecasting

**Why forecasting matters:** every SG decision (battery scheduling, energy trading, EV charging) depends on future info. Wrong forecast → poor decision → higher cost. Optimization _assumes_ future info exists — forecasting is what supplies it.

**Single-step vs multi-step:**

- Single-step: predicts ONE future value; use case = intraday scheduling adjustment
- Multi-step: predicts a SEQUENCE of future values; use case = day-ahead scheduling & market bidding

**Forecast horizons:**

|Horizon|Range|Output|Use cases|Methods|
|---|---|---|---|---|
|Very-short|seconds-min|single-step|freq regulation, gen-demand balance|persistence, moving avg|
|Short (intraday)|1-6h|multi-step trajectory|EV charging control, battery dispatch|statistical, classical ML|
|Day-ahead|24-48h|daily profile|market bidding, scheduling|ML, deep learning|
|Long-term|months-years|trend/peak|capacity/grid planning|trend-based, scenario-based|

**PV vs Load forecasting:** PV driven by solar position/irradiance/clouds (high volatility, zero at night). Load driven by human activity/calendar/temperature (moderate volatility, non-zero at night). EV charging adds a 3rd problem: arrival/departure time, energy demand, SoC.

**Task types:** Regression (single continuous value, e.g., next 15-min load), Classification (discrete label, e.g., plugged in/out), Multi-step regression (sequence, e.g., day-ahead profile).

**Pipeline:** Raw data → cleaning (dedupe, resample, check units, handle outliers/missing values) → feature engineering (scaling: x_scaled=(x−x_min)/(x_max−x_min)) → train/test split (chronological, e.g. 80/20) or cross-validation (walk-forward folds for time series).

### Model families

**Statistical (baseline):**

- **Persistence**: ŷ_{t+1} = y_t (tomorrow = today). Zero computation, can't capture trends.
- **Moving Average**: ŷ_{t+1} = (1/n)Σy_{t-i}. Smooths noise, lags trends, equal weight to all past values.
- **ARIMA**: AR (past values) + I (differencing y'_t = y_t − y_{t-1}, removes trend) + MA (past errors). Requires stationarity; best for linear problems. Recover forecast: ŷ_{t+1} = y_t + ŷ'_{t+1}.

**Machine Learning:**

- **Linear Regression**: ŷ = β0 + β1x1 + β2x2 +... Simple, fast, interpretable, but assumes linearity, can use external features (weather/calendar) unlike ARIMA.
- **Decision Tree**: if-then rules, splits data on best feature/threshold. Interpretable, captures nonlinearity, can overfit.
- **Ensembles**: Random Forest (many trees, trained independently/parallel, averaged/voted — robust, less interpretable) vs XGBoost/LightGBM (trees built sequentially, each correcting previous errors' residuals — very accurate, more compute).

**Deep Learning:**

|Model|Idea|Advantage|
|---|---|---|
|RNN|sequential, reuses prior step info|good for sequences, but vanishing gradient|
|LSTM|adds cell state + 3 gates (forget/input/output)|long-term dependencies|
|GRU|simplifies LSTM, 2 gates (reset/update)|faster training, similar performance|
|Transformer|processes whole sequence at once, attention mechanism|long-range + parallel processing, but data-hungry|

**Model selection guide:** linear relationships → Linear Regression; nonlinear → tree ensembles; temporal dependencies → LSTM/GRU/Transformer; multiple interacting dependencies → hybrid models. No universally best model — depends on EDA + objective + constraints.

**Evaluation metrics:**

- Regression: RMSE (penalizes large errors), MAE (avg absolute error), MAPE (%error), sMAPE (symmetric MAPE)
- Classification: Accuracy, Precision (avoid false alarms), Recall (detect rare events), F1 (balance precision/recall)

**Key insight — average accuracy can mislead:** e.g., 4.5% overall MAPE looks great, but if the 1 peak hour had 40% error while 23 normal hours had 3% error, the peak — the operationally critical moment — was badly missed. **Evaluation strategy should match the operational objective** (e.g., use "Peak MAE" for peak forecasting, not blanket MAPE). Similarly, training can use sample weighting or asymmetric loss to penalize missing peaks more heavily.

**Use case — EV user behavior (workplace charging):** No historical charging data existed → surveyed 149 employees (EV experience, charging habits, V2G awareness, timing concerns) → behavioral segmentation via **Multinomial Logistic Regression** → predicted user type feeds into the smart charging optimizer. Result: Linear 38.9%, Exponential 28.2%, High 23.5%, Low 9.4% preference profiles. Balances company objectives (cost, peak shaving, solar use) against employee objectives (will they let the company use their EV battery?).

---

## High-yield cross-lecture connections

- **ISO 15118 ↔ OCPP** (L4) feeds into **OCPP 2.0.1's V2G support** (L4) which enables the **V2G use cases** in L5.
- **MILP/SGH/GA/DRL** (L7) map onto **Day-ahead vs Intraday** (L7) which needs **Network Slicing** (L6) for differentiated QoS.
- **Forecasting** (L11) supplies the inputs (PV, price, EV arrival/departure) that **Optimization** (L7) consumes — "forecasting is the missing component that makes optimization possible."
- **PLC** (L3) and **5G/NB-IoT** (L2, L6) are alternative access technologies competing on the same requirements table (L2).
- **Control Reserve (FCR/aFRR/mFRR)** (L5) is the real-world balancing service that **V2G-enabled aggregators** (L7) could bid into.