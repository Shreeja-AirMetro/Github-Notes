 // Copies from Notion 
### 3GPP 
Pure Satellite/NTN specific specifications:

[TR 38.811](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3234), "Study on New Radio (NR) to support non-terrestrial networks", REL-15 SI FS_NR_nonterr_nw, RAN

[TR 22.822](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3372), "Study on using satellite access in 5G", REL-16 SI FS_5GSAT, SA1

[TR 38.821](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3525), "Study on solutions for NR to support non-terrestrial networks (NTN)", REL-16 SI FS_NR_NTN_solutions, RAN3

[TR 23.737](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3485), "Study on architecture aspects for using satellite access in 5G", SI FS_5GSAT_ARCH, SA2; note: SI started in REL-16 but ended in REL-17

[TR 38.863](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3926), "Non-terrestrial networks (NTN) related RF and co-existence aspects", REL-17 WI NR_NTN_solutions, RAN4

[TS 38.101-5](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3982), "NR; User Equipment (UE) radio transmission and reception; Part 5: Satellite access Radio Frequency (RF) and performance requirements", REL-17 WI  NR_NTN_solutions, RAN4

[TS 38.108](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3934), "NR; Satellite Access Node radio transmission and reception", REL-17 WI NR_NTN_solutions, RAN4

[TS 38.181](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3935), "NR; Satellite Access Node conformance testing", REL-17 WI NR_NTN_solutions, RAN4

[TS 38.521-5](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=4145), "NR; User Equipment (UE) conformance specification; Radio transmission and reception; Part 5: Satellite access Radio Frequency (RF) and performance", REL-17 WI NR_NTN_solutions_plus_CT-UEConTest, RAN5

[TR 38.882](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=4074) "Study on requirements and use cases for network verified UE location for Non-Terrestrial-Networks (NTN) in NR", REL-18 SI FS_NR_NTN_netw_verif_UE_loc, RAN

[TR 37.911](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=4185), "Study on self-evaluation towards the IMT-2020 submission of the 3GPP Satellite Radio Interface Technology", REL-18 SI FS_IMT2020_SAT_eval, SA1

[TR 22.926](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3722), "Guidelines for extraterritorial 5G Systems (5GS)" REL-18 SI FS_5GET, SA1

Generic specifications including Satellite/NTN aspects:

[TS 22.261](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3107), "Service requirements for the 5G system", stage 1 spec from SA1

[TS 23.501](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3144), "System architecture for the 5G System (5GS)", stage 2 spec from SA2, esp. clauses 5.4.10 and 5.4.11

[TS 38.300](https://portal.3gpp.org/desktopmodules/Specifications/SpecificationDetails.aspx?specificationId=3191), "NR; NR and NG-RAN Overall description; Stage-2", RAN2, esp. clause 16.14

Note: Stage 3 aspects are distributed over several specifications (like any other 3GPP feature)

---

### Omnet++


### Simu5G 
- Concept of Modularity from Omnet++
- INET framework 
- Optimization tools like (CPLEX) 
- Simu 5G is a network emulator 


To dos: 
- [ETSI MEC](https://simu5g.org/users-guide/mec):
Model of both MEC system-level and host-level entities: UALCMP, MEC orchestrator, MEC host, MEC platform, MEC services. Radio Network Information and Location Services are implemented. Fully compliant ETSI interfaces towards Device app and MEC app allow one to use real MEC application endpoints with 5G transport and MEC services based on information coming from the 5G network.




----

### Readings

<span style="color:rgb(0, 0, 0)">Proposal of a Reliable Multicast Protocol in a HAP-Satellite Architecture
</span>
- integrated HAP-satellite architecture and propose a reliable multicast protocol that capitalizes upon the HAP-layer to perform local retransmissions. Our protocol relies on a progressive packet-level Forward Error Correction (FEC) scheme. The performance of this multicast protocol has been supported thorough the comparison with a theoretical bound in the literature.
- The large coverage area of Geostationary Earth Orbit (GEO) satellite systems is particularly effective in the delivery of two service categories, that is, broadcast and multicast services [1].
- high propagation delay and the unpredictability of the quality of satellite links.

To overcome this problem, a return link toward the satellite can be employed to communicate retransmission requests to the sender. However, the costly nature of satellite bandwidth and the high transmission power required practically preclude the establishment of return links for broa- cast/multicast services. In this context, High Altitude Platforms (HAP’s) can be used since they are characterized by low propagation delays and favorable path-loss conditions.

- Bent-pipe architecture - the end-to-end path is divided into three independent links each one with different characteristics: i) from the sender (namely, an earth Hub station) to the GEO satellite with high delays and fading conditions that can be compensated operating uplink power control; ii) from the GEO satellite to the HAP without atmospheric fading; iii) from the HAP to end-users with variable fading conditions, but pretty low propagation delays.

- Furthermore, the HAP layer offers the possibility of local retransmissions (from the HAP to user terminals), thus obviating the need to propagate the requests back to the earth Hub station.

- reliable multicast protocol - concept of higher layer coding (hereafter referred to as packet-level Forward Error Correction, FEC) to attain an enhanced network performance. Practically, IP datagrams are coded with FEC (i.e., packet-level FEC) in order to allow the possible recovery of lost packets (i.e., data erasures) without the need of retrans- missions.

- our reliable multicast architecture is split in two parts, thus making the HAP to perform a sort of proxy function; this solution allows a better optimization of the overall data transfer; ii) a more detailed scheme is proposed here for requesting retransmissions of lost data together with the study for the use of timers.

- Packet-level FEC is based on the same philosophy as traditional FEC, that is, it handles packets as if they were bits, and can be used in conjunction with traditional FEC techniques. In [5], the Reed-Solomon Erasure correcting code is examined at the packet level, while the concept of packet-level FEC is described in [6].

- the sender has to transmit k data packets, the packet-level code uses these packets and generates h redundant packets. The sender will eventually transmit n = k + h packets. Hereinafter, the k data packets will be referred to as the Transmission Group (TG), while the h packets will be denoted as Rdata (redundancy data). At the receiver, the TG can be reconstructed if at least any k out of the n packets are correctly received.

- A straightforward advantage, stemming from the use of packet-level coding, is that a single redundancy packet can make up for the loss of different data packets at different receivers.

- To aid the deployment of HAP systems, ITU has allocated some spectrum in the 28/31 and 48/47 GHz bands for HAP communications around the world [7]. Albeit the operation of HAP’s at 28/31 GHz is considered advantageous, potentially guaranteeing fewer data transmission errors than at 47/48 GHz, the latter band can be used as well since HAP’s are mainly restricted to line-of-sight communications.

- we can make the assumption that packets (i.e., IP datagrams) are lost according to a random uncorrelated process characterized by an average Packet Error Rate (PER).

- impact of this interference path on system performance is taken into account through an increased PER value with respect to PERs of the other two links.

- relax the requirements for user terminal transmit power and attain lower packet error rates.

- HAP’s have on-board processing capabilities; thus, they can decode the data sent by the Hub station and recover from corrupted TG’s. However, if the TG cannot be decoded, a TG retransmission request (i.e., a NACK) is sent to the Hub station via the GEO satellite. Now let us turn our attention to end-users. If a TG is not correctly received, then the end-user sends a NACK to the relative HAP: lost packets can then be recovered by means of a local procedure that entails retransmissions only from HAP’s. This way, the mean delay of data delivery is signiﬁcantly reduced. This approach implies that the HAP is equipped with a (layer 3) buffer where packets received from the Hub station as well as related redundancy packets are stored until the TG is correctly received by all users in the multicast group.

- Pragmatic General Multicast (PGM) protocol [8]. Moreover, packet-level FEC has been used by different kinds of protocol suites in order to improve network performance [3],[4],[9],[10].

- In both cases, only k information packets of a TG are sent ﬁrst (without redundancy); then, h redundant packets (i.e., Rdata) are sent only if a NACK is received from at least one receiver (i.e., a HAP or a end-user, depending on the multicast level). A retransmission request is iterated until all end-users are able to decode the TG.

- The minimum elevation angle required for reliable communications with the HAP is considered to be 30deg

- HAP coverage area has a radius of about 35 km and the maximum RTDU−HAP for users near the edge of coverage is about 0.27 ms

- 10 Mbit/s and a PER at the IP level equal to 10−3. With this level of PER, and a pretty small num- ber of HAP’s (lower than ten), requests for redundancy packets from HAP’s are almost sporadic.

- A Tranmission group is formed by 10x packets of 1500 bytes - transmitted in 10Mbits/sec channel - transmisson time = S/B - transmisson data /channel Bandwidth = 10x1500

- ηf -link utilization efﬁciency: this metric shows how efﬁciently the link from the HAP’s to end-users is utilized by multicast transmissions. It is obtained as the ratio of the number of all original packets transmitted by the HAP to the total number of packets transmitted.

- Tg - mean HAP-to-user TG delay: this metric indicates the average time interval that is needed in order to deliver successfully a TG to the whole set of end-users.

- We can note that especially for lower values of PERH our protocol achieves an efﬁciency value ηf quite close to the ideal value.

- Our protocol has a lower performance than the theoretical one since, in this case, the impact of timers and possible losses on the return channel, due to collisions and data corruptions, are not considered.

- Reliable eHealth Services Delivery over 3D LEO-based Non-Terrestrial Networks

- Information and Communication Technologies (ICT) and the forthcoming Sixth-Generation (6G) system may revolutionize the doctor-patient relationship and healthcare modalities owing to the introduction of eHealth (or digital health).

Reliable Satellite Routing Algorithm (RSRA) for a 3D NTN based on Low-Earth Orbit (LEO) satellites.

- The system-level performance of proposed RSRA algorithm is assessed through simulation campaigns and compared against a routing approach that neglects LEO satellite reliability.

[1] M. Giordani, M. Polese, M. Mezzavilla, S. Rangan and M. Zorzi, “Toward 6G Networks: Use Cases and Technologies,” in IEEE Communications Magazine, vol. 58, no. 3, pp. 55-61, March 2020. 
[2] C. Suraci, S. Pizzi, F. Montori, M. Di Felice, and G. Araniti, “6G to Take the Digital Divide by Storm: Key Technologies and Trends to Bridge the Gap,” in Future Internet, vol. 14, no. 6, 189, 2022.
[3] F. Rinaldi, H.-L. M¨a¨att¨anen, J. Torsner, S. Pizzi, S. Andreev, A. Iera, Y. Koucheryavy, and G. Araniti, “Non-Terrestrial Networks in 5G & Beyond: A Survey,” in IEEE Access, vol. 8, pp. 165178-165200, 2020. 
[4] G. Araniti, A. Iera, S. Pizzi, and F. Rinaldi, “Toward 6G Non- Terrestrial Networks,” in IEEE Network, vol. 36, no. 1, pp. 113-120, January/February 2022. [5] I. F. Akyildiz, A. Kak, and S. Nie, “6G and Beyond: The Future of Wireless Communications Systems,” in IEEE Access, vol. 8, pp. 133995- 134030, 2020.

- The routing strategy proposed in [11] takes into account the uncertainty of link information in Mobile Edge Computing (MEC) satellites, which are the results of the deployment of MEC servers on LEO satellites

- LEO satellite network by integrating informa- tion on transmission delay, packet loss rate, and available bandwidth. Network throughput and end-to-end delay are the metrics optimized by the solution proposed in [12],

- We consider a 3D NTN system, where regenerative payload- based LEO satellites orbiting the Earth at different altitudes collect data from sensors worn by patients via the service link and transfer gathered data to a target NTN Gateway (NTN- GW) via the feeder link. The communication between LEO satellites takes place via Inter-Satellite Links (ISLs).

- The algorithm determines the reliable routing path P, initialized at line 1, indicating the source LEO satellite ID, the constellation ID to which the source LEO satellite belongs, the next-hop LEO satellite ID, the constellation ID to which the next-hop LEO satellite belongs, the distance between the two satellites, and the time of the ISL. The ISL transmission time and the total transmission time are initialized to zero (lines 2-3).

- The overall transmission delay Ttot is given by the sum of delaysource, the delay over the ISLs, and delay dest

[10] S. Geng, S. Liu, Z. Fanga and S. Gao, “An optimal delay routing algorithm considering delay variation in the LEO satellite communication network,” in Computer Networks, vol. 173, 2020. 
[11] J. Zhou, et al., “Routing Strategy for LEO Satellite Networks Based on Membership Degree Functions,” in Security and Communication Networks 2020, 2020. 
[12] F. Tang, H. Zhang and L. T. Yang, “Multipath Cooperative Routing with Efficient Acknowledgement for LEO Satellite Networks,” in IEEE Transactions on Mobile Computing, vol. 18, no. 1, pp. 179-192, 1 January 2019.

- 3GPP TR 38.821, “Solutions for NR to support non-terrestrial networks (NTN),” Release 16, May 2021.

- Throughput and Capacity Evaluation of 5G New Radio Non-Terrestrial Networks with LEO Satellites

- we address this gap by analyzing and evaluating the throughput and capacity performance of LEO NTN.

- S band with 30 MHz bandwidth serving handheld terminal is about 600 Mbps and the downlink capacity of a LEO satellite in Ka band with 400 MHz bandwidth serving very small aperture terminal (VSAT) is about 7 Gbps.

- In [8], analytical expressions along with geometrical simulations were used for typical satellite orbits (LEO, MEO and GEO) to derive statistical performance quantities such as coverage areas, frequency of handovers, and link absence periods. This work proposed several techniques such as spot turnoff and frequency division to reduce interference in non-GEO systems.

- In [10], the authors focused on the assessment of optical LEO downlinks and pointed out that large networks are required to meet the requirement of latency-critical applications. The work [11] developed a statistical method to estimate the total system throughput and used it to compare the three large LEO satellite constellations: Starlink, OneWeb, and Telesat. In [12], the author provided a preliminary evaluation of the latency performance of Star- link and concluded that a network built with a mega-LEO constellation can provide low latency performance in wide- area communication. The work [13] presented a capacity study of a LEO NTN using multi-input and multi-output (MIMO). In [14], the authors analysed the impact of beam coverage characteristics on the performance of LEO systems

- 3GPP TR 38.811, “Study on New Radio (NR) to Support Non-terrestrial Networks (Release 15)” V15.0.0, August 2018. Available at [http://www](http://www/). [3gpp.org/ftp/Specs/archive/38](http://3gpp.org/ftp/Specs/archive/38) series/38.811/38811-f20.zip. [4] 3GPP TR 38.821, “Solutions for NR to Support Non-terrestrial Networks (Release 16)” V16.0.0, January 2020. Available at [http://www.3gpp.org/](http://www.3gpp.org/) ftp/Specs/archive/38 series/38.821/38821-g00.

[8] F Vatalaro et al., “Analysis of LEO, MEO and GEO Global Mobile Satellite Systems in the Presence of Interference and Fading” IEEE Journal on selected areas in communications, Vol. 13, No. 2., pp. 291- 300, February 1995.
[9] C. Kourogiorgas et al., “System Capacity Evaluation of DVB-S2X Based Medium Earth Orbit Satellite Network Operating at Ka band”, 8th Advanced Satellite Multimedia Systems Conference and the 14th Signal Procvessing for Space Communications Workshop, September 2016, pp. 1-8. 
[10] C. Fuchs, N. Perlot, J. Riedi and J. Perdigues, “Performance Estima- tion of Optical LEO Downlinks,” IEEE Journal on Selected Areas in Communications, vol. 36, no. 5, pp. 1074-1085, May 2018. 
[11] I. del Portillo, B. G. Cameron, and E. F. Crawley, “A Technical Comparison of Three Low Earth Orbit Satellite Constellation Systems to Provide Global Broadband,” 68th International Aeronautical Confer- ence, October 2018. 
[12] M. Handley, “Delay is Not an Option: Low Latency Routing in Space,” Proceedings of the 17th ACM Workshop on Hot Topics in Networks, November 2018, pp. 85-91. 
[13] D. Goto, H. Shibayama, F. Yamashita and T. Yamazato, “LEO-MIMO Satellite Systems for High Capacity Transmission,” 2018 IEEE Global Communications Conference (GLOBECOM), December 2018, pp. 1-6. 
[14] S. Xia, Q. Jiang, C. Zou and G. Li, “Beam Coverage Comparison of LEO Satellite Systems Based on User Diversiﬁcation,” IEEE Access, vol. 7, pp. 181656-181667, 2019.

- S band and Ka band, respectively, whereas the right part shows the downlink SINR, measured at the received physical downlink shared channel (PDSCH) and the left part the user throughput and average cell throughput. We can see that as the user density increases, the SINR decreases in both S band and Ka band. When the user density is between 0.1 and 1, the average number of UEs per cell is less than the number of cells. In this regime, as the user density increases, inter-beam interference increases rapidly, leading to rapid degradation of the SINR.

- The cell throughput is the sum throughput of all users in a cell. As the user density increases, the average user throughput decreases because more users share the system capacity and the inter-beam interference increases. Similarly, the average cell throughput decreases and rapidly converges as the user density increases. For the S band, the average downlink cell throughput converges to about 15.6 Mbps. Normalizing the 15.6 Mbps throughput by the 30 MHz system bandwidth in S band yields a spectral efﬁciency of 0.52 bit/s/Hz. For the Ka band, the average downlink cell throughput converges to about 190 Mbps. Normalizing the 190 Mbps throughput by the 400 MHz system bandwidth in Ka band yields a spectral efﬁciency of 0.47 bit/s/Hz.

- Uplink - S band LEO NTN, the uplink SINR is not high even with very low user density. This is because handheld UE is assumed in the S band LEO NTN and the handheld UE is power limited in the uplink. As a result, the uplink SINR is noise limited and is not much affected by the increased interference resulted from increased user density. In contrast, the Ka band LEO NTN serves VSAT UE, which has high transmit power and is equipped with high gain antenna. Thus, the uplink performance of the Ka band LEO NTN is not power limited. As a result, the corresponding uplink SINR smoothly decreases as the inter-beam interference increases with the user density.

- For the S band, the average uplink cell throughput converges to about 5.4 Mbps. Normalizing the 5.4 Mbps throughput by the 30 MHz system bandwidth in S band yields a spectral efﬁciency of 0.18 bit/s/Hz. For the Ka band, the average uplink cell throughput converges to about 201 Mbps. Normalizing the 201 Mbps throughput by the 400 MHz system bandwidth in Ka band yields a spectral efﬁciency of 0.5 bit/s/Hz.

- The 7 Gbps capacity offered by a LEO satellite in Ka band with 400 MHz bandwidth may serve ﬁxed wireless access. Assuming an average consumption of 2 Mbps per user, a satellite can serve 3500 users. Since the size of the serving area of a satellite is about 105 km2, the user density is 0.035 users/km2, which may correspond to a rural or remote rural scenario. Another use case of the Ka band satellite may be backhauling for cellular networks. Assuming an average consumption of 50 Mbps per rural cell site, a satellite can serve 140 sites in a rural or remote rural scenario. The 600 Mbps capacity offered by a LEO satellite in S band with 30 MHz bandwidth serving handheld UE is less appealing from user density perspective. With 105 km2 serving area size per satellite and an average consumption of 2 Mbps per user, the user density is only 0.003 users/km2.

### ISL in NTN

- Dynamic ISL handover , optimized routing for low latency , Ka-band RF
- OMNeT++ – Can simulate dynamic satellite networking with mobility models. MATLAB/Simulink – Useful for link budget analysis and performance evaluation. Handover management between Satellites
- routing algorithms (AODV, OSPF, SDN-based) for packet forwarding. Packet forwarding
- AODV routing to forward packets between satellites dynamically.
- ISLs form and break depending on distance thresholds.

#### Difference Between Routing and Packet Forwarding

- Routing and packet forwarding are two fundamental concepts in networking, particularly in satellite and terrestrial networks. While they are closely related, they serve different purposes.

|   |   |   |
|---|---|---|
|Feature|Routing|Packet Forwarding|
|Definition|The process of determining the best path for data packets to travel across a network.|The actual transmission of packets along the chosen path.|
|Function|Creates and maintains a routing table based on network topology, metrics, and protocols.|Uses the routing table to move packets from one node to another.|
|Decision Process|Happens at Layer 3 (Network Layer) and involves complex algorithms like Dijkstra’s or Bellman-Ford.|Happens at Layer 2/3 (Data Link/Network Layer) and simply forwards packets based on existing routing decisions.|
|Protocols Used|RIP, OSPF, BGP, AODV, OLSR, DSDV (for path selection).|Ethernet switching, MPLS, SDN, IP forwarding, MAC learning.|
|Dynamism|Dynamic, updates routes based on network changes.|Static, follows routing decisions unless a failure occurs.|
|Complexity|More complex, requires global or distributed network awareness.|Simpler, only checks headers and forwarding table.|
|Example in Satellite Networks|A satellite determines the best inter-satellite link (ISL) to forward data toward a ground station.|A satellite receives a packet and forwards it to the next satellite using ISL without recalculating the route.|

Example in a Satellite Network

- Routing: A LEO satellite decides whether to send data via an ISL to another satellite or downlink to a ground station.
- Packet Forwarding: Once the decision is made, the packet is transmitted over the selected ISL.

Analogy

- Think of routing as planning a road trip using Google Maps, while packet forwarding is driving along the chosen route without reconsidering directions at every turn.
- Would you like an OMNeT++ example demonstrating both concepts? ![🚀](data:image/gif;base64,R0lGODlhAQABAIAAAP///wAAACH5BAEAAAAALAAAAAABAAEAAAICRAEAOw==)​

To Do: 

database and data structure - explain
ISL - data forwarding / data routing
Omnet++ setup - lyuqiao update
Omnet++ —> database connection

ISL Notes

- ISLs as a method to utilize this resource more efficiently and circumvent saturation.
- ISLs can effectively conserve the spectral resources allocated for fixed-satellite services by replacing the up-link/down-link bandwidth of the relay station with the ISL frequency band. An ISL replacing the multiple-hopping system also provides reduced signal propagation delay and improved quality of signal transmission.
- ISL traffic models, network systems architectures, and payload configurations.
- The role of ISLs in those reports was limited to supporting functions of the conventional network systems.
- Regarding those applications. "figure-of merit" factors were derived as part of the development of ISL systems criteria and used to quantify ISL systems advantages.
- ISL categorized based on orbital separation

Learn - ISL restrictions
Frame length - Packet length
Frame / packet delay
Vector and scalar file
Random seed / randomness


- The handover framework is from the perspective of the user. The Internal subnetwork handover (ISL, NR-X2) and external subnetwork handover (between TN-NTN) is dynamic, based on predefined criteria to optimize connectivity.
- Handover Process:

	 - Occurs between two gnodeBs, which may be satellite nodes or terrestrial base stations.
	- Criteria & Trigger Conditions:
		- Involves detailed parameters such as signal strength fluctuations, latency thresholds, and interference levels to determine when a handover should be initiated.

	- Involved Entities:
		- Includes various network components such as satellite and terrestrial gnodeBs, user equipment, and centralized network controllers that coordinate the handover.

	- Variables to be Considered:
	- Key factors such as computing power, caching capabilities, network load, and resource allocation must be assessed.

- Performance Metrics:

- Evaluation of metrics like latency, throughput, packet loss, energy efficiency, and overall service continuity is critical to ensure optimal handover performance in an NTN-TN integrated network.
- Hence, the handover can occur between a terrestrial base station and a satellite gnodeB, GSL
- Standardized Control Plane: Unified network slicing/compute resource management (protocol harmonization) across all sub-networks
- Unified Compliance with 6G core network orchestration standards
- Distributed autonomy with centralized policy enforcement (security and authorization framework)

8/5/25 - NTN meeting 

  Lyuqiao thesis topic- integration and interworking 
- 5GAA report from BMW 
- Cooperative NTN - Itegrated TN 
- Term used for TN and NTN integration 
- Resource allocation - Coordination  - ideally core network 
- What will be the evaluation
-<span style="color:rgb(0, 176, 80)"> Multipath in NTN</span> 
- Stateful and stateless migration - https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=5747347

- ISL -different protocols - omnet++ https://github.com/antoniomolram/Mixim_protocol
- https://github.com/antoniomolram/Mixim_protocol
-  optimization mechanism 

---

### Need for ISL 
- Can we classify the ISL based on needs
-  Packet forwarding - Moving packet from an incoming interface to outgoing interface - diff from routing table - data plane - layer 2, layer 3 bridging 
- Routing - complex decision making of optimal path  (hop count, bandwidth and delay...) - control plane function
- Regenerative payloads (with onboard processing) support packet forwarding at Layer 3 (network layer)
-  Layer 2 Protocols
- **IEEE 802.11 variants**: Optimized for short-range ISLs with COTS components, using directional antennas for Ka/Ku bands - http://klabs.org/mapld05/presento/144_sidibeh_p.pdf | **SpaceWire**: A lightweight protocol for intra-satellite links, extendable to ISLs with modifications
- **Ethernet variants**: Adapted for high-throughput ISLs, often paired with advanced error correction for L-band reliability file:///C:/Users/Shreeja%20Sridharan/Downloads/4.pdf 
- Layer 3 Protocols
- IP routing  - BGP , OSPF 
- Open Standards and Adaptive protocols 


Whats in Layer 1 on FDD ? TDMA, CSMA, FDMA - existing time sync function 

- GEO , LEO - ISL 
- SIB 19 - established 
- SIB 25 - no regulation yet 

---
### 2/6 ISL discussion 

- Phy layer OFDMA
- Define the use of ISL  - Link to requirements and challenges of ISL 
- Type of constellation - circuit orbit geometries 

|Feature|**Walker Star**|**Walker Delta**|
|---|---|---|
|**Orbit Inclination**|Near-polar (~90°)|Lower inclination (<90°)|
|**Coverage Area**|Global, including polar regions|Equatorial and mid-latitudes; limited or no polar coverage|
|**Examples**|Iridium (communications), Polar LEO weather satellites|Galileo (GNSS), Starlink-like patterns|
|**Best For**|Users in **remote, high-latitude, or global-traveling** scenarios|Users in **urban, mid-latitude, and equatorial** regions|
 
- Starlink has Walker delta and use polar coverage using addition layer from Walker star 
- Coverage and service is the key. Constellation isn't deal breaker 
- Iridium - RF based ISL - 2 same plane and 2 lateral plane , deterministic routing and fixed neighbor satellites 
- Starlink - 4-6 laser links (new generation) dynamic routing - high speed mesh based on network congestion, latency optimization, link health and satellite position 


<span style="font-weight:bold; color:rgb(112, 48, 160)">Likely information about Starlink about Chatgpt</span>

- Dynamic Routing Algorithm : Dijkstra , Link state Routing, Equal cost Multi-Path , latency-aware A* search  (Params: Latency, Sat availability, Congestion and BW)
- Topology Aware Path planning : predictive routing - based on where the sat is, - Graph-based overlays of the mesh , Time-expanded graphs
- Transport protocols: MPTCP, QUIC, UDP
- SDN controller - Centralized or semi-distributed  may know how packets move across constellation
- DTN protocols: Bundle protocol, Licklider Transmission Protocol - buffering and rerouting if sat move out of range

|Layer|Likely Protocols / Techniques|
|---|---|
|**Application**|HTTP/3, Cloud API traffic, VoIP|
|**Transport**|QUIC, TCP, MPTCP|
|**Network**|IPv6, Custom routing overlays|
|**Link**|Optical control, ISL protocol stack|
|**Physical**|Free-space laser comms (Gbps scale), beam tracking|
- Do all the satellite needs to connect to GW? 
	-  all satellite can have connection possibility to user on ground, ISL (neighboring sat), TT and C, Gateway or Feeder link (important for Backhaul) 
	- GW to terrestrial internet) is the backbone 
- Primary and Secondary ISL - Similar to Iridium and Starlink (does to some extent too)
	- 3 static - 1 dynamic (to handle rerouting and congestion)
	- Static - computed routes so less overhead 
	- 
- When Packet forwarding in ISL? 
	- Dynamic forwarding enables the network to exploit the shortest or least-congested paths in real time, often reducing latency—especially for long-distance or cross-continental communication
	- Source routing - forwarding mechanism 
	- Forwarding Mechanism is a backup in the context of ISL  - when primary routing fails or become unavailable 
		- l 
- When Routing in ISL ? 
	- Djistra algorithm (shortest path , efficiency based routing mechanism)
- cost for routing condition? 
	- Dynamic routing can incorporate real-time metrics such as link quality, congestion, and satellite location to select the most efficient paths
- How the dynamic and static ISL will impact the network performance - Evaluation metrics 
- Bottleneck : Distribution of users

IGP (Interior Gateway Protocol)- used to exchange routing information **within a single autonomous system (AS)**—typically a single organization or network under a common administrative control. - Routing info protocol (Based on hop count), OSPF ( Dijikstra) , EIGRP (Enhanced Interior Gateway RP)
BGP is exterior gateway protocol - path vector 

- Same orbit link for permanent link 
-  TLE Threshold - simple omnett++ script 
- Constellation  - cross point is important 
- How to connect adjacent orbit satellite ? - same adjacent orbit - same velocity and less doppler 
- Which satellite and when connected to gateway 

Steps to implement in ISL
	- Script preprocessing TLE file
	- Link strategy  
	- Server send to Sat 3, 5 
- Satellite is compound module  - gnb - upf - server
- Sat node has - Gnb and Distributed unit functions 

- <span style="color:rgb(255, 0, 0)">gateway in UPF (5G)
- intermediate user plane
- filter gate 
- simu 5g 
- </span>
- Ground gateway is just a hub - receives the sat RF signals  - convert it to IP 

- Questions 
	- Sat compound module is fine? do we need changes? 
	- Propagation delays and Timing synchronizations


---

13/5  
- DA restructure idea  - Cooperative resource allocation NTN-TN  | Fraunhofer paper
- Verification  - robustness and ubiquity 
- SIB 19, 25 - Ephermis data - 
- SIB message broadcast - check 6G standard 
-<span style="color:rgb(255, 0, 0)"> **Ephemeris data  - check** </span>
- // Performance Analysis
- Autobahn  - no speed limit 
- Mobility of high speed cars - still neglible with LEO sat 
- Mobility prediction - soft ho  - With/without ISL 

Tasks to do Lyuqiao:
1. Check SIB/emphris 
2. Mobility prediction model - Omnet ++ (SoA for DA)
 **ISL and NTN-TN - HO policies**
- Omnet++ - tenser flow
- mobility - ML - DL - seed 

--- 
10/5  to dos 
- Hash how routing table look up? 
- Do each sat have diff mac and ip based on the interface 
- Do gateway and user - have diff ip based on adapters 
- Dynamic routing - 
- I-UPF and UPF  -> omnet++ - how separately within same module 
- how this mimic in Terrestrial nw 
- multiple ground station to the gateway 
- Ground station - Gateway -> NIC + UPF + Server 
- todos 
	-  ip mapping 

compound module has interface- Gnb 

Sat and gw - nodes in same location with connections

Difference - gnb has gates  its connections on satellite node 
 Gnb in Simu 5G is a protocol Stack 
we consider kind of user 
 NTN and TN 
 classify the network and then the interface 
 Public IP address method
- Classify interface based on interface and not based on network node
- UPF is traffic channelizer  - iupf used on sat 
-  where the UPF connecting to the external network ? 

---
UPF acts as a gateway, connecting the 5G network to various data networks, including the internet, enterprise networks, and other service provider networks.
User plane function (UPF) is the "decapsulating and routing" function that extracts user plane traffic from GPRS tunneling protocol (GTP) and route it to the public data network or local network via the best available path
This means the UPF can be deployed closer to the network edge, improving latency and bandwidth utilization
Performances of various UPFs - https://github.com/edgecomllc/eupf 
https://github.com/open5gs/open5gs/discussions/3090 
iUPF -  sits between gNB and Session Anchor - traffic steering and edge computing 
PSA UPF  -  Session Anchor - Primary UPF for the PDU session connecting directly to Data Network  Handles data ingress and egress policy enforcement 
D-UPF - distributed UPF sits closer to network edge - support latency sensitive applications 

- [ ] <span style="color:rgb(255, 0, 0)">Packet Rusher </span> https://github.com/HewlettPackard/PacketRusher -  
Omnet++ Simu 5G 
- - no EPS bearer support – note: a similar concept, "connections", has been implemented, but they are neither dynamic nor statically configurable via some config file
- radio bearers not implemented, not even statically configured radio bearers (dynamically allocating bearers would need the RRC protocol, which is Control Plane so not implemented)


----

8/7 meeting 
X2 characteristics for ISL 
Dynamic ISL - ideas 
HO scheme UE  - criteria's - RSRP, SINR - computation cost 


22/7 
- Channel Model - Macro attenuation (FSP, atmosphere gases and attenuation)
- Service and feeder link 
- Micro part  38.901  - not available in simu 5G  - Link level simulation 
- 901 is 3d channel model - used as 2d model - 613
- 901 specification - fading , doppler shift , 
- How to implement channel model 
- 38.811 - simplified work only for S-Band 
- We use Ka-Band 
-  Focus on doppler shift 
- Existing X2 relay - only on downlink  with queuing 
- Uplink don't work 
- New X2 manager with downlink 
- The issue with X2 manager - issue with dynamic ISL

---
### Options for publication 
https://www.comsoc.org/publications/magazines/ieee-communications-standards-magazine/cfp/toward-6g-ntn-v2x-architectures (based on Lyuqiao DA)
---
To do 15/8 
- Check DA
- UE has dual connectivity LTE / 5G 
- Static ISL is established validation with UE 
- UE can connect only with 5G or LTE stack. This will be an issue for DA. 
- Create a monitoring and automatic HO for DA , but this might cause issue. So, Find Plan B  - potentially a duplicate UE 
- Passive - X2  routings stack 
- X2 to downlink 
- Simu5G - no message from gNB to gNB
- ip2nic to next X2 manager with details 
- Channel broadcast - handover - which node to broadcast 
- update when node is moved - only to UE - channel control model 
- To dos: X2 stack and the manager on the satellite 
---
26/8 

code part finished
Static ISL 
Code commit to GitLab 
config file for testing 
simulate one UE to another UE 
CBR 
simu5G default handover - only buffer downline packet 
Bug: UE - 2 physical layer 

All UE with NR Phy will have LTE Phy
identification

Simu 5g initialization Ip2,  NIC card 
first packet won't be delivered parameter upload doesn't happen in real-time 

packet flow in INTANS
UE - app , udp, ip , NIC, L frame - channel model arrive at NIC of sat - 
Inside NIC sat - ip2 check destination to oneself or other . If other - check the next hop / satellite to send - send via ISl manager (X2 manager) outside of the stack. 
information to next hop with gtp tunnel - X2 to another satellite 
decapsulate at gtp tunnel 
end 

GTP tunnel - check mechanism 

---
9/9 Meeting with lyuqiao 

- Static ISL link works as expected 
- Packet loss from UE   to Sat during one sat to another is avoided now - due to ISL and buffer associated. 
- The buffer on satellite for dynamic link is necessary
- <span style="color:rgb(255, 0, 0)">Issue: The Frequency selection of UL and DL must be different bands, Now its same band. Must be figured out </span> 
- Lyuqiao's to dos: DA workflow, Literature summary, and start implementing Veins
- Check Git update password issue  

 23/9 Lyuqiao meeting 
 Static ISL
 5000 packet - 3/5 - 5min run 
 Bug: 15 mins 500 s - transmission suspended  - GSL switch from Sat to Sat handover causing this issue 

 Propagation delay of GSL of Simu 5G is ignored 
 True end to end propagation delay
Development note: 
 ISL is ideal channel no packet loss
 hard Handover - UE - Sat 1 to Sat 2 - all packets dropped need buffer - for soft handover 
 No buffer at UE - downlink stream - gNb has buffer 
 Terrestrial core in Veins 
 Handover problem - focus on mobility 
 NLOS situation - add buffer (check on UE if sat link available - packet loss)
 
Giang - 23-29th October availability for Mid-term presentation

Gear box 5 - Modulation scheme not fixed 
How many physical layer we need ? we have 5G NR and LTE (LTE disabled)

DA - Smart Handover 
Assumption - TN and NTN Sensing 
LEON all the Ephermis data terrestrial GEo data - general modules 
NTN UE - SIB 25
TN UE - SIB 19 
TN to NTN HO and NTN to TN HO 
Reason for Cross tech HO - Ubiqutous connectivity 

Find what is the HO case/scenario from NTN to TN 
TN to NTN - Moving away from BS  - Distance Inc , SINR decrease impact RSSI, RSRP 
Carrier frequency change - UL and DL  -  Multiple 3GPP 


---
23/10 
- write Andrea slot for mid-term presentation 
	-  10th November 
- ISL static link - without terrestrial end to end can run 
- SUMO integration 
- Static link statistics 
- How to implement dynamic link 
- Can one satellite connect to many sat from same orbit ?
- SIB 25 and SIB 19 for signaling
- DA tough part is handover UE in physical layer 
- 5G coverage - how big is the coverage area 
- scenario for DA 
- ISL packet loss

---
28/10 
ISL no packet loss
SIB 25 was for NTN might not be used as regular broadcast. It will be on-demand message 
SIB 1
Reply Based on that SIB 25 will be implemented 

Midterm - invitation (To do)

Walkthrough DA
Process Car in coverage area - inter handover taken care by ? SIB 
Cross handover to NTN  happens RSSI - signal strength based 

sat to sat - inter handover 
reenter the terrestrial zone 2 - sense time for soft cross handover from NTN 
TN constant broadcast handover packet 

Why SIB 25 cannot work? why it is planned as on-demand message 

ground assumption 

Sat gateway to core network exists
iridium netxt at ground have info about sat 
car UE process by itself - DT and Iridium 
UE handover stratergy - Overhead , power 
UE don't need to do active handover 
vendors need to share information 
soft handover - no freq scanning 

SIB 19 and SIB 25

I am moving away from base station to NTN so SIB 19 will be given by BS about the potential sat with footprint location. So the UE have antenna in idle state and triggers the cross handover through satellite 

SIB only provide Positional data helps to narrow down the list (related position and elevation angle)Sniff Handover packet from TN gnB
distance based candidate list 

From a sat to base station - the UE can sniff/ sense the BS broadcast and establish the connection. On the other hand with regards to SIB 25, the sat master provides the list of BS available under its foot print, which might be counter productive.

SIB is part of system information standard - eg : SIB 1 is primary message 
Excellent question — this goes to the heart of how **radio access networks (RAN)** and **radio resource control (RRC)** manage communication and connectivity in **5G NR (New Radio)** systems.

Let’s break this down clearly:

---

## 🧩 **1. Goal of System Information (SI)**

The **System Information (SI)** in 5G (and earlier generations like LTE) provides the **essential configuration and operational parameters** that a **User Equipment (UE)** needs to:

- Access the network,
    
- Establish initial connection, and
    
- Operate properly in a given cell.
    

In essence, **SI acts as the “network handbook”** broadcast by each base station (gNB), allowing UEs to learn:

- How to connect,
- What frequencies or carriers exist,
- What system features are supported,
- Which services or restrictions apply.

---

## 🏗️ **2. Where SI Fits — RAN & RRC Context**

- **RAN (Radio Access Network)**: Responsible for the air interface — radio transmission, scheduling, and resource allocation.
- **RRC (Radio Resource Control)**: A protocol layer (part of Layer 3) managing signaling between UE and gNB.
- **System Information** is broadcast by the gNB using **RRC messages**.

So, the **RRC layer** carries **SI messages** over the **broadcast control channel (BCCH)**.

---

## 🧱 **3. Types of System Information Messages**

There are **two main categories** in 5G NR:

### **(a) MIB – Master Information Block**

- **Purpose:** Enables basic cell access and decoding of further system information.
    
- **Sent via:** PBCH (Physical Broadcast Channel).
    
- **Contents:**
    - System frame number (SFN)
    - Subcarrier spacing for SIB1
    - Reference signal power, etc.


> Think of MIB as the “doorway” — it gives the UE just enough info to read the next message.

---

### **(b) SIBs – System Information Blocks**

Each **SIB (System Information Block)** contains a specific set of parameters.

#### Common SIBs in 5G NR:

|SIB|Function|
|---|---|
|**SIB1**|Cell access parameters, PLMN info, scheduling of other SIBs, cellBarred status|
|**SIB2**|Radio resource configuration common for access and random access parameters|
|**SIB3–SIB9**|Neighbor cell info, reselection parameters, etc.|
|**SIB10–SIB24**|Reserved or used for MBMS (Multimedia Broadcast Multicast Service) and regional extensions|
|**SIB25 (NTN-specific)**|Terrestrial coverage info for non-terrestrial networks|
|**SIBs for positioning (e.g., SIB17)**|Contains positioning reference signal configuration|

---

## 🛰️ **4. Transmission Mechanism**

- **MIB** → Sent periodically in every cell.
- **SIB1** → Broadcast on BCCH via DL-SCH; scheduling info for other SIBs.
- **Other SIBs** → Can be on-demand in NR (i.e., UE requests them via RRC once connected), unlike LTE where all were periodically broadcast.


This improves **spectral efficiency** and reduces **broadcast overhead** in 5G.

---

## 🤝 **5. UE Use Cases for SI**

A UE uses System Information to:

1. **Perform cell selection/reselection**.
2. **Determine access restrictions** (e.g., roaming, emergency services).
3. **Configure random access (RACH)**.
4. **Handle mobility and inter-RAT measurements**.
5. **Learn NTN or TN coverage information (e.g., via SIB25).**

---

## 🔍 **6. In Summary**

|Concept|Role|Carried by|Used for|
|---|---|---|---|
|**MIB**|Basic cell identity & timing|PBCH|Initial synchronization|
|**SIB1**|Scheduling + access info|BCCH / DL-SCH|Finding other SIBs|
|**SIBx**|Detailed configurations|BCCH / DL-SCH (on-demand)|Connection setup, mobility, NTN/TN info|

---
Exactly — that’s an important and newer part of 5G’s system information design for **Non-Terrestrial Networks (NTN)**.  
Let’s unpack how **SIB25** fits into the broader **System Information (SI)** architecture and what it does for **coverage awareness between NTN and TN**.

---

## 🛰️ **SIB25: NTN/TN Coverage Information Block**

### 🔹 **Purpose**

**SIB25 (System Information Block type 25)** provides **Terrestrial Network (TN) coverage information** to a **User Equipment (UE)** that is currently connected to or camped on a **Non-Terrestrial Network (NTN)** cell.

This allows the UE to:

- Be aware of **terrestrial coverage availability** in its geographical area.
- **Optimize mobility decisions**, i.e., when to attempt reselection or handover to a TN cell.
- **Save power** by avoiding unnecessary searches for terrestrial networks when none are available.


So, think of SIB25 as a **“map of terrestrial coverage visibility”** for UEs operating under satellite (NTN) conditions.

---

## 🧭 **Why It Matters**

In NTN scenarios (e.g., satellite links), the UE can be:

- **Far from any terrestrial base station (gNB)**, or
- **Temporarily within TN coverage zones** (e.g., near urban areas).


Without SIB25, the UE would have to **periodically search for terrestrial cells blindly**, wasting power and time.

SIB25 enables **informed reselection** — the UE only tries terrestrial access when the network indicates coverage exists nearby.

---

## 📡 **What SIB25 Contains**

The **3GPP 38.331** specification defines SIB25 parameters broadly as:

|Parameter|Description|
|---|---|
|**tn-CoverageAreaList**|Lists one or more terrestrial coverage areas (IDs or coordinates).|
|**tn-CoverageAreaInfo**|Provides timing, validity duration, and quality info for each area.|
|**tn-CoverageType**|Indicates type of TN (macro, micro, or local).|
|**tn-PriorityInfo**|Priority of TN coverage relative to current NTN cell.|
|**Validity**|Duration or distance for which the info is valid (to reduce frequent updates).|

The gNB broadcasts SIB25 over the **BCCH** (similar to other SIBs) with periodicity based on network planning.

---

## ⚙️ **How the UE Uses It**

1. **UE camps on an NTN cell.**
2. It decodes **MIB → SIB1 → SIB25**.
3. From SIB25, it learns where terrestrial coverage may exist.
4. Based on location and movement, it decides **when to attempt reselection** to a TN cell.
5. When leaving TN coverage, the UE can return to NTN operation seamlessly.

This enables **hybrid connectivity** — smooth operation between satellite and terrestrial segments.

---

## 🔄 **Network Coordination**

The **core network and RAN** coordinate to:

- Update SIB25 dynamically when terrestrial coverage maps change.
- Ensure NTN cells have up-to-date TN coverage data.
- Manage priorities for UE mobility between NTN ↔ TN.

---

## 📘 **Summary**

|Item|Description|
|---|---|
|**Message Type**|SIB25 (System Information Block type 25)|
|**Defined in**|3GPP TS 38.331 (RRC protocol spec)|
|**Purpose**|Inform NTN UEs of terrestrial coverage availability|
|**Use Case**|Power-efficient mobility & reselection decisions|
|**Benefit**|Reduces blind cell searches; improves service continuity|

---
MIB and SIB1 - minimum system info 
SIB message are cell / area specific

RA procedure to request the SIB - that are on-demand 
RA - random access resources 
what is dedicated channel or dedicated signaling 
Cross handover is a 2 step process

Diagram 
Structure of the simulator 

Plot 

--- 
Post about Midterm presentation

5/11
Meeting on DA presentation

Presentation 15-20 minutes

Without interworking of TN and NTN 
Interhandover 
then passivily disconnected 
Then sniffing for NTN 
Inter NTN handover 
Hard handover 
Smart cross handover  - how 

TBD is Motivation 
Design cross handover 

SIB 19, 25 message note Marking on the slides - legends 
interval of updating the message higher and higher 
Slide 29 - NTN core and TN core 
Seamless service 
NTN 
What is application server doing here?

What is the the goal of Slides from 29 - 34

How to simulator is used 
what's the goal 
What have you built as a part of Thesis 
Working on hard handover plot 
Create the progress graph 

References slide 

---

10/11  Mid-term presentation Lyuqiao 
 - Coverage 
 - cost-efficient NTN 
 - NTN interworking
 - System information block 
 - Mention of standards - ETSI 
 - Mention what's the threshold 
 - Buffering at base station ? 
 - ITS : Intelligent transportation system 
 - Integrated mobility 
 - What's x-ho orchestration
 - what's jittering and why significant in NTN
 - ISL routing 
 - UE navigation driver 

---
SIB 25 
when to trigger sniffing was not decided by SIB 25
Buffering from the sat to TN 
"timing is the issue" 
Buffering internal 
SIB25 is not the criteria to trigger the handover 

"trigger when to do the handover "
Handover packet SIB message is part of LTE packet 
LTE phy frame 
trigger is based on distance 

"sniffing"

Lower packet drop and latency 
buffer - for NTN to TN 

Downlink happening - uplink will be dropped 

UE to NTN gateway - Core network - Server - is the uplink 

Uplink - costumer centric 

with sat and base station - buffering 

where is the application server 
send through the TN network 

burst 

---
25/11

- Mobility module of the sat and UE can run in one scenario and two GUI (SUMO and Omnet++)
- 3 lanes with 3 lanes - cross handover - inter handover 
- link between NTN gateway and satellite - carrier freq is same (2 Ghz) - no separated - 2 Ghz uE to Sat and 30 Ghz sat - gateway 
- 6 gnb from point A to point B 
- Location and testing cross handover from physical layer 
- Now debugging 

Student job
Static link as ISL exists 
dynamic link  - what's the distance based idea to form the link 

// dynamic link - packet routing 
conf the topology - update the table
Mesh network in Omnet++

HW
When to update IP table update based on ever changing topology 
distance based routing - walker star (min set of walker delta)
Mechanism (Markov chain based routing - care about next hop only?!)
Does the destination 
What current ISL topology question 
How many ISL links can one satellite have 
Wi-Fi- Mesh / other -INET  - OSPF v3 802.11

definition of the dynamic / static and ISL  - Inter and cross orbit ISL 

---
To read
 BBU  - RRH separate 
 What are the components of RAN



