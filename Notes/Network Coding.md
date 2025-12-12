
### What is Nw coding 
- Network Coding (NC) represents a paradigm shift from traditional **store-and-forward** routing to **compute-and-forward** processing.
- Instead of simply relaying packets, intermediate nodes (routers, gateways, or drones) mathematically combine multiple input packets into a single output packet. 
- This approach trades computational complexity for significant gains in throughput, reliability, and robustness, particularly in lossy wireless environments like 5G, satellite, and drone networks.
## **Core Principles**

- **Linear Combination**: The fundamental operation involves treating data packets as vectors over a finite field (Galois Field, typically GF(28)GF(28)). A node receives packets AA and BB and forwards a new packet C=αA+βBC=αA+βB, where αα and ββ are random coefficients.
- **Butterfly Effect**: The classic "Butterfly Network" example demonstrates that NC can achieve the multicast capacity limit (max-flow min-cut theorem) which routing alone cannot.[](https://en.wikipedia.org/wiki/Linear_network_coding)​
- **Recoding**: Intermediate nodes can re-combine already coded packets without decoding them first, allowing the "repair" of lost data streams on the fly.
### Why it is a good method to investigate for multi-link in drones


### What are my priorities /parameter that's important 


### What are the types of Nw coding algo - SoA

###  How to implement Hw level 

###  How to validate with simulation testbed 


### Osel work 
