### Satcom 

**Yes, but with a distinction.** In Satellite Communications, "Coding" usually refers to Physical Layer Forward Error Correction (FEC) like **LDPC** or **Turbo Codes** (used in DVB-S2/RCS2 standards), which is standard and mandatory.

**Network Coding (NC)**—specifically the _compute-and-forward_ technique at the Network/Transport layer—is currently an **emerging technology** that is being standardized for specific high-value use cases (like deep space or hybrid bonding) rather than being a default setting in consumer broadband.
- **IETF RFC 8975 (The "Satcom" Guide)**:
    - Titled _"Network Coding for Satellite Systems,"_ this document lays out the architecture for using NC to fix the "TCP over Satellite" problem.
    - It addresses the high packet loss in **Ka-band** (rain fade) and **moving platforms** (planes/ships/drones) where physical layer FEC isn't enough.

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

## **Hardware Implementation of Network Coding for Drone Telemetry**

To implement Network Coding (NC) for a drone with 3 distinct links (Satcom, 5G, WiFi), you need to build a **"Coded Multi-Path Tunnel"**. Unlike standard bonding (which just round-robins packets), this tunnel will proactively generate redundancy so that if the 5G link drops a packet, the Satcom link can fill the gap without asking for a retransmission (which would take too long).

## **1. Hardware Architecture**

The physical setup requires an **Onboard Computer (OBC)** to act as the "Network Coding Router" between the Flight Controller and the modems.

- **Flight Controller (FC):** (e.g., Pixhawk/Cube) - Outputting MAVLink via UART (TELEM1).
- **Onboard Computer (OBC):** (e.g., Raspberry Pi 4/5, Jetson Orin) - Runs the NC logic.
    
- **Modems:**
    - **5G Modem:** USB/M.2 module (e.g., Quectel RM500Q) $\rightarrow$ Interface `wwan0`
    - **Satcom:** (e.g., Iridium/Starlink Mini) $\rightarrow$ Ethernet/USB `eth1`
    - **WiFi:** Internal/External High-Power Card $\rightarrow$ Interface `wlan0`

**Data Flow:**  
`FC` $\xrightarrow{\text{UART}}$ `OBC (NC Encoder)` $\xrightarrow{\text{Split}}$ `Modems` $\dots \dots$ `Ground Server (NC Decoder)` $\xrightarrow{\text{UDP}}$ `QGroundControl`

## **2. The "Low Latency" NC Strategy: Systematic RLNC**

For telemetry (MAVLink), you cannot afford the latency of waiting to fill a "block" of packets before sending them. You must use **Systematic Random Linear Network Coding (S-RLNC)** with a **Sliding Window**.

- **Concept:**
    
    1. **Send the "Native" Packet Immediately:** As soon as MAVLink Packet $P_1$ arrives, send it instantly on the fastest link (5G). **Zero latency penalty.**
    2. **Generate "Repair" Packets:** Simultaneously, mix $P_1$ with previous packets ($P_{1} + \alpha P_{0}$) and send this "coded packet" on the **secondary links** (Satcom/WiFi).
    3. **Receiver Logic:** If $P_1$ arrives fine on 5G, the receiver discards the repair packet. If $P_1$ is lost on 5G, the receiver uses the repair packet from Satcom/WiFi to mathematically recover $P_1$ immediately.
        

---

## **3. Step-by-Step Implementation Guide**

You can build this using Python (for prototyping) or C++ (for production). The following steps assume a Linux environment (Ubuntu) on the OBC.
 **Step A: MAVLink Interception**

Use `MAVProxy` or `pymavlink` to read the serial stream and forward it to your local NC script via UDP.

 **2. The "Low Latency" NC Strategy: Systematic RLNC**

For telemetry (MAVLink), you cannot afford the latency of waiting to fill a "block" of packets before sending them. You must use **Systematic Random Linear Network Coding (S-RLNC)** with a **Sliding Window**.

- **Concept:**
    
    1. **Send the "Native" Packet Immediately:** As soon as MAVLink Packet $P_1$ arrives, send it instantly on the fastest link (5G). **Zero latency penalty.**
        
    2. **Generate "Repair" Packets:** Simultaneously, mix $P_1$ with previous packets ($P_{1} + \alpha P_{0}$) and send this "coded packet" on the **secondary links** (Satcom/WiFi).
        
    3. **Receiver Logic:** If $P_1$ arrives fine on 5G, the receiver discards the repair packet. If $P_1$ is lost on 5G, the receiver uses the repair packet from Satcom/WiFi to mathematically recover $P_1$ immediately.
 

###  How to validate with simulation testbed 
- **Steinwurf Kodo**: This is the industry-standard, high-performance C++ library for erasure coding (RLNC). It is highly optimized and used in both research and commercial products.[](https://kodo.steinwurf.com/)​
    - **Relevance**: It has direct bindings/examples for **NS-3** (`kodo-ns3-examples`).[](https://github.com/steinwurf/kodo-ns3-examples)​
- **NS-3**: The most capable simulator for 5G/LTE/WiFi layers. You can integrate Kodo with NS-3 to simulate NC over a realistic 5G NR (New Radio) stack.[](https://omnetplusplus.com/ns3-wireless-network-simulation/)​

- **OMNeT++**: Since you already use this, you can use the **Castalia** or **INET** frameworks. You can wrap C++ NC libraries (like Kodo or custom implementations) into OMNeT++ modules. This is excellent for visualizing packet flows in drone swarms.[](https://docs.omnetpp.org/articles/porting-code-into-omnetpp/)​

- **MATLAB**: Best for **Link-Level Simulations** (Physical layer). Use the "5G Toolbox" to analyze how NC coding gain interacts with modulation schemes (QAM) and channel coding (LDPC/Polar codes)
**2. The "Low Latency" NC Strategy: Systematic RLNC**

For telemetry (MAVLink), you cannot afford the latency of waiting to fill a "block" of packets before sending them. You must use **Systematic Random Linear Network Coding (S-RLNC)** with a **Sliding Window**.

- **Concept:**
    
    1. **Send the "Native" Packet Immediately:** As soon as MAVLink Packet $P_1$ arrives, send it instantly on the fastest link (5G). **Zero latency penalty.**
    2. **Generate "Repair" Packets:** Simultaneously, mix $P_1$ with previous packets ($P_{1} + \alpha P_{0}$) and send this "coded packet" on the **secondary links** (Satcom/WiFi).
    3. **Receiver Logic:** If $P_1$ arrives fine on 5G, the receiver discards the repair packet. If $P_1$ is lost on 5G, the receiver uses the repair packet from Satcom/WiFi to mathematically recover $P_1$ immediately.
*On Onboard Computer: Forward Serial MAVLink to local NC Encoder port 5000*
*mavproxy.py --master=/dev/ttyACM0 --baudrate 57600 --out=udp:127.0.0.1:5000*

## **Step B: The NC Encoder (Python Concept)**

You will write a script `nc_sender.py` that listens on port 5000 and stripes data across your 3 interfaces.

- **Library:** Use `kodo` (if you have an academic license) or a simple FEC library like `zfec` or `UDPspeeder` (open source).
- **Socket Binding:** Crucially, you must bind specific sockets to specific network interfaces.

import socket
import struct

*Configuration*
*LINKS = [*
    *('192.168.1.10', 8000, 'wlan0'),  # WiFi (Local IP, Remote Port, Interface)*
    *('10.20.30.40', 8000, 'wwan0'),   # 5G*
    *('100.64.0.1', 8000, 'eth1')      # Satcom*
*]*
*REMOTE_IP = "1.2.3.4" # Ground Station Public IP*

# *Create sockets bound to specific interfaces*
*sockets = []*
*for local_ip, port, iface in LINKS:*
    *s = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)*
    *s.setsockopt(socket.SOL_SOCKET, 25, iface.encode()) # SO_BINDTODEVICE*
    *sockets.append(s)*

*def send_telemetry(data):*
    *# 1. STRATEGY: Send ORIGINAL on 5G (Fastest)*
    *sockets[1].sendto(data, (REMOTE_IP, 8000))*
    
    *# 2. STRATEGY: Send CODED/DUPLICATE on Satcom/WiFi (Reliability)*
    *# Simple "Repetition Coding" (Diversity) for lowest latency:*
    *sockets[2].sendto(data, (REMOTE_IP, 8000)) # Satcom backup*
    
    *# For True NC:*
    *# coded_packet = simple_rlnc_encode(data, previous_packet)*
    *# sockets[0].sendto(coded_packet, (REMOTE_IP, 8000))*

## **Step C: The Ground Station (Decoder)**

The Ground Station (VPS or Static IP) needs to receive packets from all 3 sources, de-duplicate/decode them, and forward a clean stream to QGroundControl.

1. **De-Duplication:** Since you might receive the same packet from 5G and Satcom, you need a sequence number filter.
    
2. **Forwarding:**
*# Pseudo-code for nc_receiver.py*
*seen_packets = set()*

*while True:*
    *data, addr = sock.recvfrom(1024)*
    *seq_num = extract_seq(data)*
    
    *if seq_num not in seen_packets:*
        *seen_packets.add(seq_num)*
        *# Forward to QGC (localhost)*
        *qgc_socket.sendto(data_payload, ("127.0.0.1", 14550))*
    *else:*
        *# Discard duplicate (redundant packet did its job by arriving, but wasn't needed)*
        *pass*

## **Existing Tools (Don't Reinvent the Wheel)**

Since you are a researcher, you might want to focus on the _algorithm_ rather than the plumbing.

1. **UDPspeeder + TinyMapper:**
    
    - **UDPspeeder** is an open-source tool that implements Forward Error Correction (FEC) (a subset of NC) on UDP streams.
    - You can run 3 instances of UDPspeeder (one for each link) and bond them.
    - _Reference:_ [WangYu UDPspeeder GitHub](https://github.com/wangyu-/UDPspeeder)
        
2. **Glorytun:**
    
    - A Multipath UDP tunnel. It handles the "bonding" of 5G/Satcom/WiFi automatically. You can configure it to duplicate packets on critical links (Satcom) for reliability.
3. **Steinwurf Kodo (C++):**
    
    - If you need to publish a paper, write a C++ application using the **Kodo** library. It has built-in "recoding" capabilities which allows you to put a "recoder" node on the drone that dynamically adjusts the redundancy based on channel quality (e.g., if 5G RSSI drops, increase coding rate).

## **5. Performance Tuning for Drone Telemetry**

- **Packet Size:** MAVLink packets are small (~20-200 bytes). NC works best on larger blocks. **Aggregation** is key: Bundle 5-10 MAVLink messages into one 1KB UDP packet before coding. This reduces overhead.
- **Satcom Cost:** Satellite data is expensive.
    
    - _Policy:_ Do not send _everything_ on Satcom. Use NC "Predictive" logic. Only send "Repair Packets" on Satcom if the 5G link stats (RSSI/Ping) show instability.
    - _Heartbeat:_ Send only the crucial "Heartbeat" messages duplicated on Satcom, but full data on 5G.
---


### Osel work 

Caterpillar - Pace RLNC
 - https://ieeexplore.ieee.org/document/8003268
 - https://ieeexplore.ieee.org/abstract/document/8052109 



### New to explore 

- graph model and network coding 
- Link State awareness network coding 
- adaptive network coding scheme 
- 