
1. Topic with hansini 

- S. R. Pokhrel, J. Jin and H. L. Vu, "Mobility-Aware Multipath Communication for Unmanned Aerial Surveillance Systems," in _IEEE Transactions on Vehicular Technology_, vol. 68, no. 6, pp. 6088-6098, June 2019, doi: 10.1109/TVT.2019.2912851.
- G. Makropoulos _et al_., "Multi-RAT Dual Connectivity Using MPTCP: Bridging Emulation and Real-System Deployments," _2025 IEEE Conference on Network Function Virtualization and Software-Defined Networking (NFV-SDN)_, Athens, Greece, 2025, pp. 1-6, doi: 10.1109/NFV-SDN66355.2025.11349629.
- H. Alam, A. De Domenico, D. López-Pérez and F. Kaltenberger, "Throughput and Coverage Trade-Off in Integrated Terrestrial and Non-Terrestrial Networks: An Optimization Framework," _2023 IEEE International Conference on Communications Workshops (ICC Workshops)_, Rome, Italy, 2023, pp. 1553-1558, doi: 10.1109/ICCWorkshops57953.2023.10283628.
- F. Salehi, M. Ozger and C. Cavdar, "Reliability and Delay Analysis of 3-Dimensional Networks With Multi-Connectivity: Satellite, HAPs, and Cellular Communications," in _IEEE Transactions on Network and Service Management_, vol. 21, no. 1, pp. 437-450, Feb. 2024, doi: 10.1109/TNSM.2023.3307909.
- Liu, H. and Gui, J., 2026. GPR Hierarchical Synergistic Framework for Multi-Access MPQUIC in SAGINs. _arXiv preprint arXiv:2603.02740_.
- H. Yu, S. Tu, K. K. Ramakrishnan, N. Abu-Ghazaleh, X. Zhang and A. Swami, "M&M: Machine-Learning Enhanced MPQUIC for Resilient Communication with mmWave Networks," _MILCOM 2024 - 2024 IEEE Military Communications Conference (MILCOM)_, Washington, DC, USA, 2024, pp. 950-955, doi: 10.1109/MILCOM61039.2024.10773824.

----

Mobility-Aware Multipath Communication for Unmanned Aerial Surveillance Systems

- Multipath TCP has the potential to exploit heterogeneous wireless paths and achieve robust bandwidth by controlling the dynamics of the convoy of drones.
- heterogenous channel 
- Mobility aware multipath 
- Fluid models of packet flows - fluid model of MPTCP's rate-control dynamics
- Tool - MPTCP trace
- A Lyapunov function is ==a scalar "energy-like" function V(x) used in control theory and dynamical systems to prove the stability of an equilibrium point without having to solve the system's differential equations explicitly==
Reliability and Delay Analysis of 3-Dimensional Networks With Multi-Connectivity: Satellite, HAPs, and Cellular Communications
https://arxiv.org/html/2604.27640  - # Multi-Connectivity for UAVs: A Measurement Study of Integrating Cellular, Aerial Mesh, and LEO Satellite Links
	- However, most prior work on multipath transport has focused on throughput, fairness, and aggregate capacity utilization, while real-time requirements are less explored.
	- Many UAV applications are latency-sensitive and require delay bounds to be satisfied continuously to support safe and effective operation. 
	- Our measurements reveal two practical limitations. First, when the available links do not provide sufficient capacity for the offered load, multipath transport can lead to pronounced sender-side buffering. Second, when the aggregated paths exhibit large round-trip time (RTT) heterogeneity, strict in-order delivery amplifies reordering, causing substantial receiver-side buffering and bursty packet delivery. As a result, latency-sensitive traffic can violate delay constraints even when aggregate capacity is sufficient.
	- Connectivity continuity captures the ability to maintain an end-to-end communication path despite link failures. Service continuity captures the ability to sustain application operation by delivering data within the required delay bounds under the offered load, which implicitly depends on both latency and available capacity.
	- In particular, we enabled the lowest-RTT scheduler to prioritize the path with the smallest round-trip time and thereby minimize end-to-end latency. We also configured the MPTCP congestion control, which is a core transport-layer function alongside data scheduling. Unless otherwise stated, we used TCP Reno congestion control algorithm, a standard TCP variant that reacts to packet loss by reducing (halving) the congestion window. At the receiver, MPTCP enforces strict in-order delivery: packets that arrive out of order are buffered until the missing data is received, and data is released to the application only in sequence. As a result, end-to-end packet age and service continuity are directly influenced by path delay heterogeneity and receiver-side buffering dynamics. We do not employ any application-layer adaptation, packet dropping, or deadline-aware scheduling. This design choice isolates the effects of heterogeneous path delays and the lossless, in-order delivery behavior of MPTCP on the timeliness of real-time traffic.
	- Service continuity -  Let Δ⁡(t) denote the end-to-end packet age at time t, defined as the elapsed time between packet generation at the UAV and packet delivery to the application at the receiver. - Aging
	- Lossless multipath transport protocols enforce reliable and in-order packet delivery at the receiver.
# Core explored ideas 

- Segregation-based schedulers address this directly: the Primary-Path-only Scheduler (PPoS) work adds socket APIs and a kernel modification so an application can mark one subflow as primary for a given traffic class (e.g., UAV control messages) while other paths act as backup, and the same group's follow-up shows this implemented and evaluated in a Linux-kernel MPTCP scheduler
- MPTCP with a lowest-RTT scheduler and found that aggregation preserves end-to-end connectivity under severe link outages, but large RTT heterogeneity between paths amplifies packet reordering, causing substantial receiver-side buffering and bursty delivery — and explicitly flags that most prior multipath-transport work has optimized for throughput, fairness, and aggregate capacity, while real-time, delay-bounded requirements typical of UAV control and telemetry remain comparatively unexplored.


# Gaps 

