
Structure of the simulator 
The simulator is built on the link-level discrete simulation principles of Omnet++. 
The whole simulator has 2 main contributions at the moment - LEON  (NTN part) and VEINS-LEON which is the integrated TN and NTN for evaluating handover requirements in  V2X scenario.
![alt text](image.png)
The foundation of this is Simu 5G, INET, OS3 %G-NR based simulation framework in Omnet++. Each entity of this setup consists of 4 OSI layers or we can say it follows IT/TCP protocol stack. The corresponding layers are Link layer, Network layer, transport layer and application layer. 
The link layer handles the Network interface card (understands the channel model and simulate the packet transmission), ppp tunnel, x2 tunnel (wired connection between base stations). The network layer is IP trafic management, traffic flow functions and gtp tunnels. 
The transport layer handles TCP, UDP and other transport protocols. The application layer handles the application server and client. 

The UPF and server in the core network handles all the connection through interface layer. 

Omnet.ini is the key file that compiles all the configurations and run the wholistic simulation. This particular script handles 3 main layers that ideally work towards our use-cases
1. Physical layer and channel model 
2. Mobility model  - this handles the mobility of the UE, Satellite etc..
3. Application model - Type of application (VoIP, CBR) and corresponding usecase parameters

// Simplistic structure of the NTN part is found in LEON paper: https://dl.acm.org/doi/abs/10.1145/3661810.3663470 
![alt text](implementation.png)

General Outline of the simulator

![alt text](simulator_architecture.png)


Flow Structure