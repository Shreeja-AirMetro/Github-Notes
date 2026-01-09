
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
