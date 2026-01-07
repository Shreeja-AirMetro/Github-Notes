
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
