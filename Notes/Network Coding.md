
### What is Nw coding 
- Network Coding (NC) represents a paradigm shift from traditional **store-and-forward** routing to **compute-and-forward** processing.
- Instead of simply relaying packets, intermediate nodes (routers, gateways, or drones) mathematically combine multiple input packets into a single output packet. 
- This approach trades computational complexity for significant gains in throughput, reliability, and robustness, particularly in lossy wireless environments like 5G, satellite, and drone networks.
## **Core Principles**

- **Linear Combination**: The fundamental operation involves treating data packets as vectors over a finite field (Galois Field, typically GF(28)GF(28)). A node receives packets AA and BB and forwards a new packet C=αA+βBC=αA+βB, where αα and ββ are random coefficients.
- **Butterfly Effect**: The classic "Butterfly Network" example demonstrates that NC can achieve the multicast capacity limit (max-flow min-cut theorem) which routing alone cannot.[](https://en.wikipedia.org/wiki/Linear_network_coding)​
- **Recoding**: Intermediate nodes can re-combine already coded packets without decoding them first, allowing the "repair" of lost data streams on the fly.
## **Association with Computing**

You asked how NC is associated with computing. The relationship is foundational to the **"In-Network Computing"** and **Edge Computing** paradigms:

- **Communication-Computation Trade-off**: NC consumes CPU cycles (for matrix multiplication in GFGF) to save bandwidth and reduce latency. It effectively converts "transmission problems" into "computation problems."
- **Softwarization (SDN/NFV)**: In modern 5G/6G architectures, NC is often implemented as a **Virtualized Network Function (VNF)**. Instead of fixed hardware encoders, software containers in an Edge Cloud or on a vSwitch perform the coding operations dynamically.[](https://en.wikipedia.org/wiki/Edge_computing)​
- **Edge Intelligence**: For drones and IoT, NC allows the edge network to handle error correction locally (via recoding) rather than relying on distant cloud servers for retransmissions (ARQ), thus enabling ultra-low latency control loops.
### Why it is a good method to investigate for multi-link in drones
- WiFi - BATMAN -> Multi-pathing 
- RLNC 
- COPE opportunistic coding for wifi 
- TNC  - Triangular Network Coding 
In the context of **WiFi, 5G, and Satellite** integration, NC is the "glue" that allows disparate links to act as a single robust pipe.
- LDPC 
- Polar codes
## **Multi-Path TCP + Network Coding (MP-NC)**

- **Concept**: Standard MPTCP (Multi-Path TCP) struggles when links have vastly different latencies (e.g., 5G: 20ms vs. Satellite: 600ms). The fast link waits for the slow link, causing head-of-line blocking.
- **SOTA Solution**: **MP-NC** or **Tuner-coded QUIC**. Instead of sending distinct packets on each path, the sender stripes _coded_ packets across all paths. If the satellite link drops a packet, the receiver reconstructs it using a redundant coded packet arriving via 5G, eliminating the need for a high-latency retransmission request

Ref: https://wlv.openrepository.com/server/api/core/bitstreams/24158f8e-dd75-4ca7-b2cc-e8490ded7d1e/content 
### What are my priorities /parameter that's important 
- **Seamless Handover (Make-Before-Break)**: As a drone moves between 5G cells or switches from 5G to Satellite (e.g., Iridium/Starlink), there is a "handover gap." NC allows the drone to receive coded streams from _both_ the old and new connections simultaneously. As long as it collects enough total degrees of freedom, the data stream remains uninterrupted.
-   **Jitter/Latency Smoothing**: In C2 (Command & Control) links, retransmissions (ARQ) are dangerous because they introduce variable delay (jitter). NC allows "Forward Error Correction" (FEC) but with higher efficiency, ensuring control commands arrive deterministically.
- **Swarm Communication**: For drone swarms, RLNC enables efficient broadcasting. If Drone A wants to send a map update to Drones B, C, and D, it can broadcast coded packets. Drones B, C, and D can share the packets they received with each other to reconstruct the full map, reducing total transmissions by ~40-60%.



###  How to implement Hw level 

###  How to validate with simulation testbed 
- **Steinwurf Kodo**: This is the industry-standard, high-performance C++ library for erasure coding (RLNC). It is highly optimized and used in both research and commercial products.[](https://kodo.steinwurf.com/)​
    - **Relevance**: It has direct bindings/examples for **NS-3** (`kodo-ns3-examples`).[](https://github.com/steinwurf/kodo-ns3-examples)​
- **NS-3**: The most capable simulator for 5G/LTE/WiFi layers. You can integrate Kodo with NS-3 to simulate NC over a realistic 5G NR (New Radio) stack.[](https://omnetplusplus.com/ns3-wireless-network-simulation/)​

- **OMNeT++**: Since you already use this, you can use the **Castalia** or **INET** frameworks. You can wrap C++ NC libraries (like Kodo or custom implementations) into OMNeT++ modules. This is excellent for visualizing packet flows in drone swarms.[](https://docs.omnetpp.org/articles/porting-code-into-omnetpp/)​

- **MATLAB**: Best for **Link-Level Simulations** (Physical layer). Use the "5G Toolbox" to analyze how NC coding gain interacts with modulation schemes (QAM) and channel coding (LDPC/Polar codes)

### Osel work 
