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