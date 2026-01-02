
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


---

Questions to Lyuqiao 

