
C++ Rule of three - Memory based coding - dynamically allocated objects and memory

- Copy constructor
- Copy constructor assignment operator
- Desructor 
Rule of 5 in c++


Structure of the simulator 
The simulator is built on the link-level discrete simulation principles of Omnet++. 
The whole simulator has 2 main contributions at the moment - LEON  (NTN part) and VEINS-LEON which is the integrated TN and NTN for evaluating handover requirements in  V2X scenario.

The foundation of this is Simu 5G, INET, OS3 %G-NR based simulation framework in Omnet++. Each entity of this setup consists of 4 OSI layers or we can say it follows IT/TCP protocol stack. The corresponding layers are Link layer, Network layer, transport layer and application layer. 
The link layer handles the Network interface card (understands the channel model and simulate the packet transmission), ppp tunnel, x2 tunnel (wired connection between base stations). The network layer is IP trafic management, traffic flow functions and gtp tunnels. 
The transport layer handles TCP, UDP and other transport protocols. The application layer handles the application server and client. 

The UPF and server in the core network handles all the connection through interface layer. 

Omnet.ini is the key file that compiles all the configurations and run the wholistic simulation. This particular script handles 3 main layers that ideally work towards our use-cases
1. Physical layer and channel model 
2. Mobility model  - this handles the mobility of the UE, Satellite etc..
3. Application model - Type of application (VoIP, CBR) and corresponding usecase parameters

// Simplistic structure of the NTN part is found in LEON paper: https://dl.acm.org/doi/abs/10.1145/3661810.3663470 


General Outline of the simulator

Omnet++ is the "engine  "which involves the kernel ., IDE and the GUI infrastructure. The small parts must fit into this engine - INET framwork and INET 4.5 provide protocols like TCP/IP, Wi-FI and 5g , TSN , associated routing protocols  AODV , OSPF based networking support 

### INET framework is networking logic

|**Folder**|**What it contains**|**Why it's there**|
|---|---|---|
|**`src`**|**Source Code.** This is the heart of INET. It contains all the C++ files (`.cc`, `.h`), NED files (`.ned`), and message files (`.msg`).|This is where you go to modify protocols or create new ones. It is organized by layers (e.g., `src/inet/transportlayer`).|
|**`include`**|**Header Files.** Usually contains symbolic links or copies of `.h` files from the `src` directory.|It allows other projects (your own simulations) to "find" the INET code easily during the compilation process.|
|**`bin`**|**Executables.** This contains the compiled binary files and helper scripts.|When you run a simulation from the command line, the system looks here for the executable programs.|
|**`doc`**|**Documentation.** Includes API references, user guides, and developer manuals.|It helps users understand how to use the modules without having to read the raw source code.|
|**`examples`**|**Ready-to-run simulations.** Sample networks (like a simple wired LAN or a complex wireless mobile network).|Crucial for learning; you can copy an example and modify it rather than starting from scratch.|

INET framework have realworld accuracy - **Saves Time:** Without INET, if you wanted to simulate a simple web request, you would have to manually code the entire TCP/IP stack, the WiFi physical layer, and the routing logic. INET provides these out-of-the-box.
When you build a simulation in OMNeT++, the **NED files** define the structure (the "map"), the **C++ files** (in `src`) define the behavior (the "logic"), and the **INI file** defines the specific scenario (the "test"). INET provides the vast majority of these C++ and NED components so you don't have to. 

### Simu5G - Cellular link logic

**Simu5G** is an evolution of the older _SimuLTE_ library. It is a specialized framework designed to model the **5G New Radio (NR)** standard.

- **What it adds:** It provides the complex "gNodeB" (5G base station) and "UE" (User Equipment/Phone) modules.
- **Data Plane:** It models the entire 5G stack (SDAP, PDCP, RLC, MAC, and PHY layers).
- **MEC Support:** It includes advanced Multi-access Edge Computing (MEC) models, allowing you to simulate servers sitting right at the edge of the 5G network for low-latency apps.



Flow Structure

3 main layers of changes
- Physical - channel model
-  Mobility 
- Application 


---

Questions to Lyuqiao 

1. How to create Omnet - Air segment -Sperate 
2. Questions on running Veins-Leon
3. Miro board discuss

---

1. Simu5G (https://simu5g.org/users-guide/overview#features)  incorporates all the models from the INET library, which allows one to simulate generic TCP/IP networks including 5G NR layer-2 interfaces. In particular, Simu5G simulates the data plane of the 5G RAN (rel. 16) and core network. It allows simulation of 5G communications in both Frequency Division Duplexing (FDD) and Time Division Duplexing (TDD) modes
2. possibly communicating via the X2 interface to support handover and inter-cell interfer-ence coordination. Dual connectivity between an eNB (LTE base station) and a gNB (5G NR base station) is also available. 3GPP-compliant protocol layers are provided, whereas the physical layer is modelled via realistic, customizable channel models. Resource scheduling in both uplink and downlink directions is supported, with support for Carrier Aggregation and multiple numerologies, as specified by the 3GPP standard (3GPP TR 38.300, TR 38.211). Simu5G supports a large variety of models for mobility of UEs, including vehicular mobility.
3. Nodes

**UEs** and **gNBs** are implemented as compound modules. These can be connected with each other and with other nodes (e.g. routers, applications, etc.) in order to compose networks. The UEs and gNBs are further composed of modules:

- _TCP_ and _UDP_ applications (any INET compatible application)
    
- _TCP_ and _UDP_ transport layers (from INET)
    
- _IP_ layer (from INET)
    
- _NR NIC_ implementing the NR stack at both the gNB and UE. The stack includes all the sublayers (PDCP, RLC, MAC, PHY). At the UE, a dual stack is implemented to allow coexistence between 4G (LTE) and 5G (NR)

## NR resource management[¶](https://simu5g.org/users-guide/overview#nr-resource-management "Link to this heading")

Simu5G currently supports:

- **Carrier Aggregation (CA):** a global carrierAggregation module stores all the information related to the CCs employed in the network. It includes a vector of N ComponentCarrier submodules, whose carrier frequency can be configured via NED/INI. A gNB/UE may be restricted to use only a subset of the available CCs.
    
- **Different numerologies:** as with LTE, a NR radio frame is 10 ms long and consists of 10 subframes, each having 1ms duration. However, NR subframes are further divided into up to 14 slots, which are the NR TTIs. A numerology index defines the slot duration, and UEs are scheduled in slots. In Simu5G, a different numerology can be associated to each CC and configured via NED/INI. gNBs and UEs can be limited to only a subset of numerologies.
    
- **Frequency/Time Division Duplexing (FDD/TDD):** Simu5G supports both FDD and TDD. In FDD, each CC has separate portions for UL and DL spectra. As far as TDD is concerned, NR foresees 62 possible slot formats (3GPP - TR 38.213), where individual symbols in a slot can be DL, UL or flexible (i.e., it can be assigned dynamically to DL or UL transmissions, or kept idle). We model TDD slot formats as properties of the CC, and we associate the slot format to the componentCarrier submodules. In the current version of Simu5G, flexible symbols are used as guard symbols. However, the above modeling allows one to easily design policies to assign flexible symbols to DL or UL dynamically.
Simu5G supports both StandAlone (SA) and E-UTRA/NR Dual Connectivity (ENDC) deployment. where LTE and 5G coexist (3GPP – TR 38.801). In the ENDC configuration, the gNB works as a Secondary Node (SN) for an LTE eNB, which acts as Master Node (MN) and is connected to the Core Network. the LTE eNB model is imported from [SimuLTE](https://simulte.omnetpp.org/), with which Simu5G is fully compatible. The eNB and the gNB are connected through the X2 interface and all NR traffic needs to go through the eNB. According to (3GPP - TR 37.340), the data flow between the eNB and the gNB

According to (3GPP - TR 37.340), the data flow between the eNB and the gNB is shown below. Data destined to a UE served by the eNB (Master Cell Group – MCG - bearer) follows the LTE protocol stack, whereas data destined to a UE served by the gNB (Secondary Cell Group – SCG - bearer) gets into the NR PDCP entity at the eNB and is transferred to its peering NR RLC entity in the gNB, via the X2 interface. The 3GPP standard also supports Split Bearers (SBs). With this feature, data belonging to the same connection can traverse either the eNB or the gNB. The PDCP layer at the UE side will then reorder PDUs coming from LTE/NR RLC layers.


---

### 3GPP Standards

Simu5G does not list every 3GPP document exhaustively, but the documentation and papers point to a Rel‑16-oriented NR data‑plane model built around the main NR RAN and radio spec family (38‑series), plus EN‑DC and channel/TR specs from 36‑ and 37‑series.[scitepress+1](https://www.scitepress.org/Papers/2020/98264/98264.pdf)​

## High‑level 3GPP basis

- Simu5G simulates the 5G RAN and core **data plane** “for 5G NR (Rel. 16)” and explicitly states that it follows 3GPP‑compliant protocol layers, with LTE/NR dual connectivity as per EN‑DC.[simu5g](https://simu5g.org/users-guide/overview)​
    
- The project README and license reiterate that the simulator is “based on 3GPP specifications,” without listing all spec numbers, and that users must handle any related IPR.[github+2](https://github.com/Unipisa/Simu5G)​
    

## Explicitly mentioned 3GPP specs in docs/papers

In the official user guide and the SIMULTECH/Simu5G papers, the following 3GPP documents are explicitly referenced as the basis for specific features (all Release 15/16 family):

- NR overall/architecture and PHY framing:
    
    - TR 38.300 / TR 38.300‑series for NR overall description and protocol architecture.[simu5g](https://simu5g.org/users-guide/overview)​
        
    - TR 38.211 for numerologies, OFDM parameters, and carrier/slot structure.[simu5g](https://simu5g.org/users-guide/overview)​
        
- TDD numerologies and slot formats:
    
    - TR 38.213 for NR TDD with 62 possible slot formats and DL/UL/flexible symbol definitions.[scitepress+1](https://www.scitepress.org/Papers/2020/98264/98264.pdf)​
        
- LTE–NR dual connectivity and multi‑connectivity:
    
    - TR 38.801 for E‑UTRA/NR Dual Connectivity (ENDC) deployment where LTE and 5G coexist.[simu5g](https://simu5g.org/users-guide/overview)​
        
    - TR 37.340 (E‑UTRA and NR; Multi‑connectivity; Stage 2) for EN‑DC / multi‑connectivity operation.[arpi.unipi](https://arpi.unipi.it/retrieve/handle/11568/1039566/609208/SIMULTECH_2020.pdf)​
        
- NR channel model implementation:
    
    - TR 36.803 is cited as the basis of the “realistic 3GPP channel model” used for path loss, LOS probability, fast fading, shadowing, etc.[simu5g+1](https://simu5g.org/neddoc/packages.html)​
        

## Implied spec families (not fully enumerated)

From the architecture and protocol descriptions, Simu5G’s NR stack maps onto the usual 38‑series TS set, even when documents are not named one‑by‑one:

- NR RAN protocol stack (RLC/MAC/PHY) implies reliance on TS 38.3xx/38.2xx families for procedures and parameters, since Simu5G offers:
    
    - 3GPP‑style scheduling (Max C/I, PF, RR) with MCS, TBS, HARQ, etc.[scitepress+1](https://www.scitepress.org/Papers/2020/98264/98264.pdf)​
        
    - Carrier aggregation and multiple numerologies as “specified by the 3GPP standard.”[simu5g](https://simu5g.org/users-guide/overview)​
        
- Papers extending Simu5G with SDAP explicitly ground their implementation in:
    
    - TS 38.331 (RRC) and TS 38.413 (NG‑AP) for SDAP header placement and QoS flow handling.[arxiv](https://arxiv.org/html/2508.12785v1)​
        
    - TS 23.501 for 5G QoS flow concepts (eMBB, URLLC, mMTC QoS characteristics).[arxiv](https://arxiv.org/html/2508.12785v1)​
        

## Practical answer for citing in your work

If you need to state in a paper or proposal which 3GPP standards Simu5G is aligned with, a concise but accurate formulation consistent with the public docs would be:

- “Simu5G implements a 3GPP‑compliant 5G NR Rel‑16 data‑plane stack, following the NR 38‑series specifications (e.g., TR 38.300, TR 38.211, TR 38.213) and EN‑DC/multi‑connectivity as described in TR 38.801 and TR 37.340, with channel models derived from TR 36.803.”[simu5g+3](https://simu5g.org/neddoc/packages.html)​
    

There is no official, exhaustive list of every TS/TR used; instead, Simu5G adheres to the above core NR and EN‑DC specs plus the usual 5G system and QoS documents when features such as SDAP are added.[arxiv+1](https://arxiv.org/html/2508.12785v1)​

1. [https://www.scitepress.org/Papers/2020/98264/98264.pdf](https://www.scitepress.org/Papers/2020/98264/98264.pdf)
2. [https://simu5g.org/users-guide/overview](https://simu5g.org/users-guide/overview)
3. [https://github.com/Unipisa/Simu5G](https://github.com/Unipisa/Simu5G)
4. [https://github.com/Unipisa/Simu5G/blob/master/README.md](https://github.com/Unipisa/Simu5G/blob/master/README.md)
5. [https://github.com/Unipisa/Simu5G/blob/master/LICENSE.md](https://github.com/Unipisa/Simu5G/blob/master/LICENSE.md)
6. [https://arpi.unipi.it/retrieve/handle/11568/1039566/609208/SIMULTECH_2020.pdf](https://arpi.unipi.it/retrieve/handle/11568/1039566/609208/SIMULTECH_2020.pdf)
7. [https://simu5g.org/neddoc/packages.html](https://simu5g.org/neddoc/packages.html)
8. [https://arxiv.org/html/2508.12785v1](https://arxiv.org/html/2508.12785v1)
9. [https://www.3gpp.org/specifications-technologies/specifications-by-series](https://www.3gpp.org/specifications-technologies/specifications-by-series)
10. [https://onlinelibrary.wiley.com/doi/full/10.1155/mse/7283539](https://onlinelibrary.wiley.com/doi/full/10.1155/mse/7283539)
11. [https://www.etsi.org/deliver/etsi_ts/138300_138399/138300/15.03.01_60/ts_138300v150301p.pdf](https://www.etsi.org/deliver/etsi_ts/138300_138399/138300/15.03.01_60/ts_138300v150301p.pdf)
12. [https://www.sciencedirect.com/science/article/abs/pii/S1389128624007448](https://www.sciencedirect.com/science/article/abs/pii/S1389128624007448)
13. [https://simu5g.org](https://simu5g.org/)
14. [https://www.colibri.udelar.edu.uy/jspui/bitstream/20.500.12008/30188/1/Per21.pdf](https://www.colibri.udelar.edu.uy/jspui/bitstream/20.500.12008/30188/1/Per21.pdf)
15. [https://repositorium.uminho.pt/bitstreams/59f89497-82d3-4c64-b3f8-37d93c585390/download](https://repositorium.uminho.pt/bitstreams/59f89497-82d3-4c64-b3f8-37d93c585390/download)

Simu5G's channel model, based on 3GPP TR 36.803, can be customized via `BackgroundChannelModel` parameters or new subclasses for UAVs favoring secondary lobes (e.g., sidelobe-dominant links in NLOS/multipath drone scenarios). This involves tuning antenna patterns, LOS probability, and Ricean K-factor to emphasize sidelobes in path loss/SINR computations.[simu5g+1](https://simu5g.org/neddoc/packages.html)​

## Customization Steps for UAV

1. **Extend BackgroundChannelModel**: In NED/OMNeT++, subclass `BackgroundChannelModel` or `DatarateChannel` to override `computePathLoss()` and incorporate sidelobe gain. Set `losProbability` low (e.g., 0.1 for urban NLOS UAV), Ricean `kFactor` low (e.g., 1-5 dB for multipath dominance), and define antenna pattern with high sidelobe relative gain (e.g., -10 dB vs. main lobe).[github](https://github.com/Unipisa/Simu5G)​
    
2. **Configure Antenna Params**: Use `txPower`, `carrierFrequency`, `height` params; add UAV-specific `antennaTilt` for downward beams where sidelobes dominate at horizon angles. Enable 3D via `use3d=true` for elevation-based lobe selection.[simu5g+1](https://simu5g.org/neddoc/packages.html)​
    
3. **Integrate Mobility**: Pair with UAV mobility (e.g., `LinearMobility` or custom drone trajectory) in `BackgroundUe` or `NRUe`; test sidelobe bias by positioning UAV off-boresight (e.g., 30-60° azimuth). Run with `BackgroundCell` for interference.[github](https://github.com/Unipisa/Simu5G)​
    
4. **Validate**: Use `BackgroundScheduler` stats for resource allocation under sidelobe SINR; extend `computeSnir()` for custom interference from sidelobes.[github](https://github.com/Unipisa/Simu5G)​
    

## Signal Chain Math: Antenna Gain to SINR

The path follows transmitter antenna gain → EIRP → propagation → receiver antenna gain → received power → SINR.

- **Tx Antenna Gain** Gtx(θ,ϕ)G_{tx}(\theta, \phi)Gtx(θ,ϕ): Directional gain at angle (θ,ϕ)(\theta, \phi)(θ,ϕ). For 3GPP-like: main lobe Gm=8G_m = 8Gm=8 dBi, sidelobe Gs=Gm−SLG_s = G_m - SLGs=Gm−SL (SL=15-25 dB). Math: G(θ)=Gm−min⁡(12(θ/θ3dB)2,SL)G(\theta) = G_m - \min(12(\theta / \theta_{3dB})^2, SL)G(θ)=Gm−min(12(θ/θ3dB)2,SL) where θ3dB\theta_{3dB}θ3dB is half-power beamwidth.[3gpp](https://www.3gpp.org/dynareport/38901.htm)​
    
- **EIRP**: Ptx+GtxP_{tx} + G_{tx}Ptx+Gtx (dBm), with PtxP_{tx}Ptx from `txPower` param.[simu5g](https://simu5g.org/neddoc/packages.html)​
    
- **Path Loss** PLPLPL: Free-space + shadow + fast-fading. From TR 36.803: PL=PLlos/nlos+10log⁡10(Xσ)+Ricean fadingPL = PL_{los/nlos} + 10\log_{10}(X_\sigma) + \text{Ricean fading}PL=PLlos/nlos+10log10(Xσ)+Ricean fading, where NLOS favors sidelobes via low LOS prob. Ricean: K=LOS powerNLOS powerK = \frac{\text{LOS power}}{\text{NLOS power}}K=NLOS powerLOS power.[simu5g](https://simu5g.org/neddoc/packages.html)​
    
- **Rx Power** Prx=EIRP−PL+Grx(θr,ϕr)P_{rx} = \text{EIRP} - PL + G_{rx}(\theta_r, \phi_r)Prx=EIRP−PL+Grx(θr,ϕr) (dBm).[simu5g](https://simu5g.org/neddoc/packages.html)​
    
- **Interference**: Sum Ik=Prx,kI_k = P_{rx,k}Ik=Prx,k from interferers kkk (BackgroundUe in sidelobes). Noise N=−174+10log⁡10(BW)+NFN = -174 + 10\log_{10}(BW) + NFN=−174+10log10(BW)+NF (dB, BW=bandwidth).[simu5g](https://simu5g.org/neddoc/packages.html)​
    
- **SINR**: SINR=Prx/(I+N)\text{SINR} = P_{rx} / (I + N)SINR=Prx/(I+N) (linear). In Simu5G: `computeSnir()` aggregates via `getInterference()` from Binder. For UAV sidelobe: tune angles to use GsG_sGs in Gtx/rxG_{tx/rx}Gtx/rx, lowering SINR ~10-20 dB vs. main lobe.[3gpp+1](https://www.3gpp.org/dynareport/38901.htm)​
    

1. [https://simu5g.org/neddoc/packages.html](https://simu5g.org/neddoc/packages.html)
2. [https://github.com/Unipisa/Simu5G](https://github.com/Unipisa/Simu5G)
3. [https://www.3gpp.org/dynareport/38901.htm](https://www.3gpp.org/dynareport/38901.htm)

- ==Rel‑16-oriented NR data‑plane model built around the main NR RAN and radio spec family (38‑series),==
- ==PHY framing== 
	- ==TR 38.300 / TR 38.300‑series for NR overall description and protocol architecture.==
	- ==TR 38.211 for numerologies, OFDM parameters, and carrier/slot structure==
	- ==TDD : TR 38.213 for NR TDD with 62 possible slot formats and DL/UL/flexible symbol definitions==
- ==LTE and 5G== 
	- ==TR 38.801 for E‑UTRA/NR Dual Connectivity (ENDC) deployment where LTE and 5G coexist.​==
	- ==TR 37.340 (E‑UTRA and NR; Multi‑connectivity; Stage 2) for EN‑DC / multi‑connectivity operation.==
	- ==3GPP TR 38.811 is a Technical Report from Release 15 that studies adaptations of New Radio (NR) to enable non-terrestrial networks (NTNs), such as satellite and high-altitude platform systems (HAPS)==
	- ==3GPP specifications define LTE frequencies in TS 36.101 and 5G NR in TS 38.104/38.101, while channel models appear in dedicated TRs like TR 36.942 for LTE and TR 38.901/TR 38.900 for 5G. Antenna patterns in these models distinguish main lobe (primary) from side lobes (secondary), with parameters for lobe gain, width, and sidelobe levels.==
	- ==BackgroundChannelModel : parameters or new subclasses for UAVs favoring secondary lobes (e.g., sidelobe-dominant links in NLOS/multipath drone scenarios). This involves tuning antenna patterns, LOS probability, and Ricean K-factor to emphasize sidelobes in path loss/SINR computations==

### Parameters

1. Mobility of the UE : Linear, stationary and random
2. Antenna and Interference: channel model TX power, Shadowing Ricean or Reyleigh factor, LOS probability, scheduler and traffic generator from BS background cells 
3. Frequency and carrier aggregation No of bands, no of component carriers and bandwidth
4. Omnet++ Message handler 



Air to ground link  - UAV 36.777
BS propagation characteristics - 38. 901 table 7.3.1.

Reileigh - LOS 
NLOS probability 

Urban micro - LOS and NLOS from 38.777
Mobility of drones - don't over complicate - linear as car 
Intercell distance 500m   urban macro case 

---


13/1 
	READING EVERY PART OF THE SIMULATOR 

1. In OMNeT++, INET isn't just a library; it’s a massive collection of "building blocks" (modules) that you piece together to simulate a network.
2. INET supports a wide class of communication networks, including wired, wireless, mobile, ad hoc and sensor
	networks. It contains models for the Internet stack (TCP, UDP, IPv4, IPv6, OSPF, BGP, etc.), link layer protocols
	(Ethernet, PPP, IEEE 802.11, various sensor MAC protocols, etc), refined support for the wireless physical layer,
	MANET routing protocols, DiffServ, MPLS with LDP and RSVP-TE signalling, several application models, and
	many other protocols and components. It also provides support for node mobility, advanced visualization, network
	emulation and more.
	The Packet data structure is capable of representing application packets, TCP segments, IP datagrams, Ethernet
	frames, IEEE 802.11 frames, and all kinds of digital data. It is designed to provide efficient storage, duplication,
	sharing, encapsulation, aggregation, fragmentation, serialization, and data representation selection. Additional
	functionality, such as support for enqueueing data for transmisson and buffering received data for reassembly
	and/or for reordering, is provided as separate C++ data structures on top of Packet.
	The Packet data structure builds on top of another set of data structures called chunks. Chunks provide several alternatives to represent a piece of data. Chunks usually represent application data and protocol headers.
	Signals always encapsulate a packet and also contain a description of the analog domain representation. The most
important physical properties of a signal are the signal duration and the signal power.
	==Within network nodes, supplementary data often needs to be transmitted alongside a packet. For instance, when an application-layer module intends to transfer data using TCP, it must specify a connection identifier for TCP. Similarly, when TCP transmits a segment via IP, IP requires a destination address, and when IP sends a datagram to an Ethernet interface for transmission, a destination MAC address must be specified.==
	==Packet tags are not transmitted from one network node to another. All physical layer protocols delete all packet tags from a packet before sending it to the connected peer or to the transmission medium.==
	==To gather certain statistics, it might be necessary to add metadata to various regions of packet data. For instance, determining the end-to-end delay of a TCP stream necessitates labeling data regions at the source with their creation timestamp. Subsequently, as the data arrives, the receiver calculates the end-to-end delay for each region.==
	**Packet API provides a PacketDissector class which analyzes a packet solely based on the assigned packet protocol and the actual data it contains.**





3. `src/` (The Engine Room) - This is the most important folder. It contains the actual logic for every protocol (TCP, IP, UDP, etc.) and device (Routers, Hosts, Switches) in INET.
- **`.ned` files:** These define the "blueprints" or structure of a module (what gates/connectors it has).
- **`.cc` and `.h` files:** These are the C++ files that define how the module actually behaves.
- `src/` folder is organized to enforce **OSI layer separation** and **interface-based programming*
- **Design Pattern:** INET uses the **"Strategy Pattern"** extensively. For example, if you look at `inet/networklayer/ipv4/`, you’ll see that the `Ipv4` module doesn't hardcode its routing. Instead, it interacts with an `IRoutingTable` interface. This allows you to swap out static routing for dynamic protocols (OSPF, BGP) without touching the IP core. **`.msg` files:** These are the **Message Definitions**.
- **Subfolders:** You will see names like `inet/applications`, `inet/transportlayer`, and `inet/networklayer`. These follow the OSI model logic.
- Routing tables and IP addresses for the interfaces must be configured by the IPv4NetworkConfigurator module. **`inet/common/`:** This is the "Utility Belt." It contains sophisticated base classes like `INETDefs.h` and specialized units (time, distance, power) that ensure type safety across the framework.
 `showcases/` (The "Look What I Can Do" Gallery) Think of these as **interactive demonstrations**. Each showcase focuses on a specific feature—like "Wireless Signal Propagation" or "Energy Consumption."
- **Purpose:** They include a full setup (`.ini`, `.ned`) and a detailed web page explanation
- `bin/` (The Tools) This folder contains executable scripts and utilities that help INET run. Usually, as a beginner, you won't need to touch these files directly; the OMNeT++ IDE uses them in the background to build the project and manage "fingerprint" tests (which check if a simulation still gives the same results after a code change).
`python/` (The Data Assistant) - OMNeT++ and INET are moving toward using Python for **data analysis**.
- **Purpose:** These scripts help you process the `.vec` (vector) and `.sca` (scalar) result files generated after a simulation run.
- **Use Case:** If you want to graph the throughput of your network using Matplotlib or Pandas, the tools here help bridge that gap.
`includes/` (The Shared Library) When you build INET, it creates a set of header files here so that **other projects** (your own simulations) can "see" and use INET's code. It acts as the gateway for your custom project to talk to the INET framework.

### `bin/` — The Build and Execution Pipeline
Advanced users often need to bypass the IDE for headless execution (e.g., on a High-Performance Computing cluster).
- **`run_inet`:** A bash/batch script that sets the `NEDPATH` correctly. If you are running parallel simulations with `opp_run`, you need to understand how this script assembles the environment.
- **`setenv`:** This script exports critical environment variables (`INET_ROOT`, `PATH`). Sourcing this is mandatory for CLI-based workflows or Makefile regeneration.

Inside a network node, protocol modules interact with one another by sending Packet or Message objects.
INET is very flexible in terms of what structure the protocol modules can be connected. Protocols can be connected
directly to each other, or they can be connected through one or more MessageDispatcher modules. This flexibility
allows for the creation of both simple and complex network node architectures.
Simple network nodes can be constructed, for example, using a linear protocol stack, where protocol modules are
directly connected to one another without using message dispatcher modules.
![[Pasted image 20260113122900.png]]


More complex network nodes can be created by grouping protocols into layers and connecting them through
MessageDispatcher modules, which facilitates many-to-one and many-to-many relationships among the protocols
of the layers.

![[Pasted image 20260113122918.png]]

To support the packet dispatching mechanism, certain additional requirements must be met in C++ code:
• protocols must be registered using registerProtocol
• packets must have DispatchProtocolReq tags attached
Applications can simply call the socket class member functions (e.g. bind(), connect(), send(),
close()) to create and configure sockets, and to send and receive packets. They may also use several different
sockets simulatenously.

The L3Socket class provides an easy to use C++ interface to send and receive datagrams using the conceptual
network protocols. The underlying network protocols are implemented in the NextHopForwarding, Flooding,
ProbabilisticBroadcast, and AdaptiveProbabilisticBroadcast modules. - ==IS IT USED; IF WHERE???==

The TunSocket class provides an easy to use C++ interface to send and receive datagrams using a TUN interface.
The underlying TUN interface is implemented in the Tun module.
A TUN interface is basically a virtual network interface which is usually connected to an application (from the
outside) instead of other network devices. It can be used for many networking tasks such as tunneling, or virtual
private networking



For an advanced user, **Simu5G** is more than just a 5G library; it is a specialized extension of the **INET Framework** that replaces the generic wireless stack with a high-fidelity, 3GPP-compliant 5G New Radio (NR) implementation.
Simu5G provides the `NrUe` (User Equipment) and `gNodeB` (Base Station) compound modules. These do not just "simulate" 5G; they implement the full data plane:

- **SDAP (Service Data Adaptation Protocol):** Handles QoS flow-to-DRB (Data Radio Bearer) mapping.
- **PDCP (Packet Data Convergence Protocol):** Manages ciphering and robust header compression (ROHC).
- **RLC (Radio Link Control):** Implements UM (Unacknowledged) and AM (Acknowledged) modes with segmentation.
- **MAC Layer:** Includes complex **Resource Schedulers** (Proportional Fair, Round Robin, MAX C/I) that operate on Resource Blocks (RBs) in the frequency/time domain.
- Physical Layer Fidelity
Unlike INET's simpler unit-disk or scalar radio models, Simu5G uses:

- **Numerology Support:** Configuration of different subcarrier spacings ($15, 30, 60, 120\text{ kHz}$).
- **Channel Modeling:** Integration of realistic path loss (UMi, UMa), fast fading, and shadowing models.
- **CQI/SINR Feedback:** A closed-loop system where UEs report Channel Quality Indicators back to the gNB for adaptive modulation and coding (AMC).

---

Simulation stratergy 
1. **Infrastructure Mode**, where UE1 sends data to UE2 via the 5G network.
2. NED File: Before writing the `.ini` file, you need a network topology that includes at least two UEs, a gNodeB, and the 5G Core (UPF). Simu5G provides a template called `SingleCell_Standalone`.
3. The `.ini` file is where you tell UE1 to "talk" to UE2. For an E2E flow, UE1 will act as a UDP client and UE2 as a UDP server. and a  random seed for reproducibility 
4. Next is setting up IP and routing - mask and master cell i d
5. # IPv4 address assignment
*.configurator.config = xmldoc("demo.xml") # Or let it auto-configure

# Connect UEs to the gNodeB
*.ue1.macCellId = 1
*.ue1.masterId = 1
*.ue2.macCellId = 1
*.ue2.masterId = 1


on top is application setup 

# --- UE1: Sender ---
*.ue1.numApps = 1
*.ue1.app[0].typename = "UdpBasicApp"
*.ue1.app[0].destAddresses = "ue2"      # Target UE2 by its module name
*.ue1.app[0].destPort = 1000            # Port ue2 is listening on
*.ue1.app[0].messageLength = 1000B
*.ue1.app[0].sendInterval = 0.1s        # 10 packets per second
*.ue1.app[0].startTime = 1s

# --- UE2: Receiver ---
*.ue2.numApps = 1
*.ue2.app[0].typename = "UdpSink"       # Simply receives and consumes packets
*.ue2.app[0].localPort = 1000


Then the channel model 
==HOW TO DEFINE THE CARRIER FREQUENCY AND BANDWIDTH==

.gnb.cellConfigurator.carrierFrequency = 2GHz
.gnb.cellConfigurator.bandwidth = 20MHz

Realistic channel modeling
.channelModel.typename = "NRChannelModel"
.channelModel.scenario = "UMa"  # Urban Macrocell

---

EXECUTION - Build the project Makesure that the INET and Simu5G are checked in project references . 
Then make sure demo.xml the IPV4 configurator to assign addresses is set to true 


==Exporting the packets from a simulation into a PCAP file allows further processing with 3rd party tools. The== ==Packet API provides a PcapDump class for creating PCAP files. Packet filtering can be used to reduce the file== ==size and increase performance.==
==PcapDump dump;==
==dump.openPcap("out.pcap", 65535, 0); // maximum length and PCAP type==
==dump.writePacket(simTime(), packet); // record with current time== 

----

Installation guide

The current codebase is available in [https://datashare.tu-dresden.de/s/DHQjt6zsZDXGZFG](https://datashare.tu-dresden.de/s/DHQjt6zsZDXGZFG) (Omnetpp_51525v1.zip)

This codebase is the foundation for DA-Lyuqiao and Air segment inclusion workpackage by Shreeja

System recommendations: OS: Linux (Ubuntu 22.04 recommended)  
CPU: x86_64 RAM: ≥ 4 GB

Simulator recommendations: Omnet++ - version 6.0.1 Sumo - version 1.22.0 General dependencies: python >= 3.10, C++, CMake, Java Specific dependencies: INET 4.5 framework, OS3, Simu5G, Veins, Iridium LEO based satcom TLE file

Output file type: csv, pcap and plot viewer (Omnet++ default)

Reference links: Omnet++ Documentation - [https://omnetpp.org/documentation/](https://omnetpp.org/documentation/) Omnet++ - [https://doc.omnetpp.org/omnetpp/InstallGuide.pdf](https://doc.omnetpp.org/omnetpp/InstallGuide.pdf) Sumo - [https://github.com/eclipse-sumo/sumo](https://github.com/eclipse-sumo/sumo) Veins - [https://veins.car2x.org/documentation/](https://veins.car2x.org/documentation/) INET framework - [https://inet.omnetpp.org/](https://inet.omnetpp.org/) Simu5G - [https://simu5g.org/](https://simu5g.org/)

Installation and Building the project:

1. Install INET 4.5 framework and Simu 5G. Else the corresponding package can be imported from the above codebase
2. Setup Veins into the same working repository.
3. Install Sumo
4. Build INET 4.5 (select build all-> configurations)
5. Install OS3 (make sure to import ubuntu curl package)
6. Compile and run in the following order - INET4.5 -> Simu 5G-> OS3 -> LEON-> Veins -> Veins-leon (Lyuqiao DA part)