# INTANS simulator 
Published versions 
- VERON
- LEON
- UAV - as User - DRCN
Unpublished version 
- Veins-leon 
- HAP 


# Paper structure 

- Introduction  (3)
	- NTN networks 6G and use-case verticals 
	- Need for open source simulator 
	- Role of Academia in NTN 
	- Contributions
- Background (3)
	- NTN network Regulation and Standards
	- Mobile usecases - NTN network 
	- NTN Simulators 
- Simulator Design concept (4)
	- Architecture of Userplane and structure 
- Omnet++ and Sumo : General Network Implementation (5)
	-  Used frameworks
	- Protocols and Principals (Theory)
	- Implementation layers - general - Network Architecture and code 
- Use-cases, Results (4)
	- Leon case
	- SIB and Car - Veins Leon 
	- UAV Case
	- HAP case 
- Github repository  -. Guide, Code, Csv dataset for above use-cases
- Potential Expansion of the network , Discussion (1)
	- Implementation ideas and structure
	- Hap Use-case 2
	- MEC
- Conclusion and future work (1)
	- Control Plane 
	- Focus on IP networking 
	- Multi-user scenario 
- References 
	- Writing 20-21 pages 
	- Figures 
		- Intans architecture
		- Simulator figure 
		- Layers, Modules figure and connection 
		- Event analysis 
	- Tables
		- State of art 
		- Network parameters genera
		-  Operational parameters for each simulators 
		- KPI comparision table for each use case
	- Plots  (KPI) - SIB - heuristic, Latency, Throughput , Packet loss Ratio , SINR /RSSI  - vs Time - Uplink and downlink as sub plot
		- Leon - plot 
		- SIB and Car Plot 
		- UAV handover plot 
		- HAP plot 




**First Version Submission Target JUNE 1st** 



# Simulator Discussion Points for Open Source 

- Focus on 4 use-cases  (HAP is not mandatory)
- Run the existing simulator , clean up data - have them with proper structure of data collected 
- KPIs - RSRP, RSSI,SINR , Frame level, Packet level  Latency PLR, Throughput
- Tap into all possible data in analysis - excel in analysis part 
- Physical layer throught (MCS theoritical upper bound) application layer throughput (recieved packets)
- Latency - frame level and E2E
- Check old results and format it



# To do Deadline 

- [x] Introduction -
	- [x] Have a rough sketch - Later revision only 
- [ ] Background 
	- [ ] Building 
- [ ] Theoritical Framework 
	- [ ] Sec c 
---- By Friday ----
- [ ] Simulator tools design   _ Monday
- [ ] Usecases and conclusion / future work  - Wednesday 29th