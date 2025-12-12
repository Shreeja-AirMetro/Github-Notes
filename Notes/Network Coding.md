
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

## **Multi-Path TCP + Network Coding (MP-NC)**

- **Concept**: Standard MPTCP (Multi-Path TCP) struggles when links have vastly different latencies (e.g., 5G: 20ms vs. Satellite: 600ms). The fast link waits for the slow link, causing head-of-line blocking.
- **SOTA Solution**: **MP-NC** or **Tuner-coded QUIC**. Instead of sending distinct packets on each path, the sender stripes _coded_ packets across all paths. If the satellite link drops a packet, the receiver reconstructs it using a redundant coded packet arriving via 5G, eliminating the need for a high-latency retransmission request
### What are my priorities /parameter that's important 


### What are the types of Nw coding algo - SoA

###  How to implement Hw level 

###  How to validate with simulation testbed 


### Osel work 
