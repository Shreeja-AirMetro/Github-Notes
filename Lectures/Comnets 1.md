13 Lecture

10 exercise
MIT courseware 
ETH Zurich 


---

# ComNets 1 — Exam Study Guide

_Terms, definitions, formulas, and solving steps by lecture topic_

---

## L03 — Shannon's Communication Model & Capacity

**Shannon's communication model (chain):** `Information Source → Transmitter (source coding → channel coding) → Channel (+ Noise Source) → Receiver (channel decoding → source decoding) → Destination`

- Message `m` → source coding → `k` bits → channel coding → `n` bits (n>k, adds redundancy) → sent as signal.
- Shannon's core question: _"reproducing at one point a message selected at another point"_ — reliably, despite noise.

**Delay taxonomy (this course's specific model) — end-to-end delay breaks into:**

|Symbol|Name|Meaning|
|---|---|---|
|PD|Propagation Delay|distance ÷ speed of light (physics-limited)|
|MD|Message Delay|message size ÷ bit rate (reduce via coding/compression)|
|SAD|Sensor & Actuator Delay|time to sense/actuate physically|
|QAD|Queuing & Access Delay|waiting for medium access / queue|
|CD|Computing Delay|processing time at each node|

End-to-end delay = PD + MD + SAD + QAD + CD (summed over every hop/node in the path).

**Key general facts to know (Shannon capacity, examinable even if not in this deck's text layer):**

- **Nyquist (noiseless) max data rate:** `C = 2·B·log2(M)` (B=bandwidth, M=signal levels)
- **Shannon-Hartley (noisy channel) capacity:** `C = B·log2(1 + SNR)` — theoretical upper bound on error-free rate, independent of the coding scheme used (this is the "goal" source+channel coding tries to approach).

---

## L04 — Source Coding, Channel Coding, Reliable Transmission

### Source Coding (compression — remove redundancy)

- **Entropy** `H = −Σ pᵢ·log2(pᵢ)` = theoretical min average bits/symbol (lossless).
- **Huffman coding** — greedy, optimal _prefix-free_ code:
    1. List symbols + probabilities.
    2. Repeatedly merge the **two least probable** nodes into one (sum probabilities).
    3. Assign 0/1 per branch top-down (or bottom-up consistently).
    4. **Rule:** the two least-probable symbols always end up as sibling leaves, same length.
    5. Average length `L = Σ pᵢ·lᵢ` — always `H ≤ L < H+1`.
- **Efficiency** of a code = H / L.

### Channel Coding (add redundancy to survive errors)

- **Hamming distance (h):** min number of differing bits between any two valid codewords.
    - Detects up to `h−1` errors.
    - Corrects up to `⌊(h−1)/2⌋` errors.
- **Repetition/Replication code (factor r):** codeword = bit repeated r times (e.g. r=3 → 000/111). h = r.
- **Parity bit (1D):** add 1 bit so total number of 1s is even (even parity) or odd (odd parity). Detects any **odd** number of bit flips; **cannot correct**; **misses even numbers of flips**.
- **2D (row+column) parity:** arrange data as a matrix, parity per row AND per column (+corner bit).
    - Can correct a **single**-bit error (unique row∩column intersection).
    - Multiple errors in one row can be _detected_ (columns flag it) but not always _corrected_ (row check may miss it if the errors cancel out — ambiguous location).
- **CRC (Cyclic Redundancy Check):** polynomial (mod-2) division.
    1. Append (deg of polynomial) zero bits to data.
    2. XOR-divide by the generator polynomial repeatedly (align leading 1s, shift).
    3. Remainder = CRC, appended to data → transmitted codeword.
    4. Receiver re-divides; remainder `0` ⇒ no error detected.
- **Hamming(n,k) code / Hamming(15,11):**
    - Parity bits at **power-of-2 positions** (1,2,4,8,...); data fills the rest.
    - Parity bit `p_j` covers every position whose binary representation has a 1 in bit position `j` (bit0→p1, bit1→p2, bit2→p3, bit3→p4...).
    - `p_j = XOR of all covered data bits`.
    - **Decoding/correction:** recompute parities from received word, XOR received-vs-recomputed (order p4 p3 p2 p1…) → **syndrome = binary position of the flipped bit** → flip it back.
    - h=3 for standard Hamming code → corrects exactly 1 bit; 2 simultaneous errors → wrongly "corrects" a third bit (need h=4 to detect 2 errors reliably).

### Line/Physical-layer coding

- **NRZ-L:** 1 = one voltage level (+V), 0 = other level (−V), held for the full bit period.
    - - simple, + bandwidth-efficient. − no self-synchronization (long runs of same bit ⇒ clock drift, DC bias).
- Other schemes to know by name: Manchester (self-clocking, transition mid-bit, uses 2× bandwidth), NRZI, RZ, AMI.

---

## L05 — Multiple Access: ALOHA to Scheduled Access

**4 basic multiple-access resource splits:** TDMA (time), FDMA (frequency), CDMA (code), SDMA (space).

**Random access family:**

- **Pure ALOHA:** send whenever ready; vulnerable period = 2× packet time (any overlap from either side collides).
    - `G = λ·t_packet` (offered load, packets per packet-time)
    - **Throughput `S = G·e^(−2G)`**, max ≈18.4% at G=0.5
- **Slotted ALOHA:** transmissions aligned to slots; vulnerable period = 1× packet time.
    - **Throughput `S = G·e^(−G)`**, max ≈36.8% at G=1
- λ (arrival rate) = N terminals × (packets/terminal/second)

**Scheduled/controlled access:**

- **TDMA variants:** Fixed (static slot assignment, wasteful if idle), DSA/Reservation (dynamic, on-demand), Token passing (only token-holder sends), Polling (central unit asks each station in turn), CSMA/CD, CSMA/CA.
- **Polling cycle time:** `T_C = n·(T_Z + T_P + T_S + T_N) + 2·Σ T_L(i)`
    - T_Z = central response time, T_P = peripheral response time
    - T_S = SOH/R (signaling msg transmit time), T_N = (SOH+SP)/R (info msg transmit time)
    - T_L(i) = distance_i × (µs/km) — propagation, counted **twice** (there & back)
    - Relative throughput `T = (n · payload_rate_per_station) / R`

**Solving steps for ALOHA/polling numeric problems:**

1. Get `t_packet` = packet size(bits) / R.
2. Compute λ (or per-station load).
3. Compute G = λ·t_packet.
4. Plug into the throughput formula (pure vs slotted).
5. For polling: build the fixed per-station time budget, add 2×total one-way propagation, multiply/sum over n stations.

---

## L06 — Ethernet, Wi-Fi, Wireless Access Procedures

**Hidden terminal problem:** two stations both reach an AP, but can't hear each other → simultaneous transmission → collision at AP, undetectable by either sender's carrier sense. **Exposed terminal problem:** a station defers because it hears a neighbor transmitting, even though its own intended transmission wouldn't actually interfere — wastes capacity.

**RTS/CTS (Request to Send / Clear to Send):** virtual carrier sensing handshake; fixes hidden terminal (all nearby stations hear at least one of RTS/CTS and set their NAV).

**IFS (Inter-Frame Space) priority hierarchy:** SIFS (Short) < PIFS (PCF) < DIFS (Distributed) — shorter wait = higher priority. High-priority frames (CTS, ACK) sent after SIFS; new contention-based transmissions (RTS, data) wait DIFS + random backoff.

**NAV (Network Allocation Vector):** timer derived from IFS values, carried in frame headers — tells overhearing stations how long the channel will stay busy (virtual carrier sense).

**CSMA/CA (802.11) access procedure (know the sequence):** DIFS → RTS → SIFS → CTS → SIFS → DATA → SIFS → ACK, with other stations deferring via NAV during this exchange; backoff uses a random slot count within the Contention Window (CW).

**System utilization / throughput analysis (WiFi MAC):**

- `T_LP = L_P/R` (data transmit time), `T_LACK = L_ACK/R`
- `T_b(N) = L_b(N) × T_CW,slot` (mean backoff time, depends on mean backoff slots & CW size)
- `T_LP(N) = (T_DIFS + T_b + T_LP) / P_success` (expected time per successful transmission, geometric-series result of repeated collisions)
- `T_ACK(N) = T_ACK + SIFS`
- `T_total(N) = T_LP(N) + T_ACK(N)`
- **Utilization/efficiency `D(N) = (T_LP + T_ACK) / T_total(N)`** — "useful" transmission time ÷ total time spent (incl. overhead/backoff/collisions).
- Larger contention window (CW) → fewer collisions but more backoff wasted time → **there's an optimal CW that depends on N** (more users ⇒ want larger CW).

**802.11 vs LTE/5G multiple access:**

- 802.11 (≤WiFi5): CSMA/CA (contention) + OFDM modulation.
- WiFi6 (802.11ax): OFDMA (scheduled, multi-user).
- LTE: SC-FDMA uplink (lower PAPR), OFDMA downlink.
- TDD (time-split up/down) vs FDD (frequency-split up/down).
- **Latency vs users:** CSMA/CA degrades fast (more users → more collisions → higher latency); OFDMA/scheduled degrades more gracefully but is capacity-limited (slot assignment delay grows).

---

## L07 — Graphs, Flows, and Network Capacity

- **Network capacity via Max-Flow Min-Cut theorem:** the maximum achievable flow from source to sink equals the capacity of the smallest "cut" (set of edges) separating them.
- **Ford–Fulkerson algorithm** (compute max flow):
    1. While an augmenting path (source→sink with spare capacity) exists in the residual graph: find one (e.g. via BFS/DFS).
    2. Push flow = the bottleneck (min residual capacity) along that path.
    3. Update residual capacities (forward −flow, backward +flow).
    4. Repeat until no augmenting path remains → total pushed flow = max flow = min cut value.
- Valid for single-source/single-sink; for multiple simultaneous flows, the simple max-flow model doesn't directly generalize (network coding can sometimes exceed classical max-flow bounds for multicast — this is _why_ network coding matters, see L12/13).
- **Topology capacity comparisons:** chain topology (N nodes, ≤2 neighbors each) vs mesh — mesh gives more alternate paths/higher aggregate capacity & resilience but more complexity; number of hops relates directly to chain length.

---

## L08 — Routing and Path Algorithms

- **Dijkstra's algorithm** (single-source shortest path, non-negative weights):
    
    1. Init: dist(source)=0, all others=∞; unvisited set = all nodes.
    2. Pick unvisited node with smallest known distance.
    3. Relax all its neighbors: if `dist(u) + w(u,v) < dist(v)`, update `dist(v)`.
    4. Mark node visited; repeat until all visited (or target reached).
    
    - Greedy, requires non-negative edge weights.
- **Bellman-Ford** (handles negative weights, detects negative cycles): relax **all** edges, `|V|−1` times.
- **Switching types:** Circuit-switched (dedicated path, fixed capacity reserved — low delay once set up, wasteful if idle) vs Packet-switched (statistically multiplexed, better utilization, variable delay) vs Message-switched (store-and-forward whole messages, historic).
- **Queuing/occupancy formulas:** relate to burstiness of traffic, queue size vs delay trade-off (relevant for M/M/1-style reasoning — know that higher utilization ρ → rapidly increasing queuing delay).

---

## L11 — Transport Layer: UDP, TCP, Congestion Control

**Transport layer tasks (know ~4):** end-to-end delivery, multiplexing/demultiplexing (via ports), segmentation/reassembly, flow control, error control/reliability (TCP only), congestion control (TCP only).

**UDP vs TCP (name 4 differences):** connectionless vs connection-oriented; unreliable vs reliable (ACK/retransmit); no congestion control vs has congestion control; no ordering guarantee vs ordered delivery; lower overhead/latency vs higher overhead. **QUIC:** built on UDP, combines TCP-like reliability + built-in encryption (TLS) + faster handshake + solves head-of-line blocking (per-stream, not per-connection). **Pseudo-header:** extra fields (src/dst IP, protocol, length) prepended only for checksum computation — lets the transport layer checksum "see" IP-layer info to catch misdelivered segments, without actually transmitting it.

**Congestion control — why & design goals:** prevent network collapse from overload; goals: fairness, efficiency, distributed operation, convergence/stability.

- **cwnd (congestion window):** sender-side limit on how much unacknowledged data may be in flight — the actual transmission window = min(cwnd, receiver's advertised window).
- **AIMD (Additive Increase, Multiplicative Decrease):** the core TCP congestion-avoidance rule — increase cwnd by ~1 segment per RTT (additive) when no loss; halve cwnd on loss (multiplicative decrease) — this is what gives TCP flows fairness/convergence.
- **Slow Start:** cwnd starts at 1 segment, **doubles every RTT** (exponential growth) until reaching `ssthresh` (slow start threshold) or a loss occurs.
- **Congestion Avoidance:** once cwnd ≥ ssthresh, switch to linear (additive) growth, +1 segment per RTT.
- **On loss (timeout):** `ssthresh = cwnd/2`, `cwnd` reset to 1 → back to Slow Start.
- **Fast Retransmit:** on 3 duplicate ACKs (triple-duplicate ACK), retransmit the missing segment immediately without waiting for timeout.
- **Fast Recovery:** after fast retransmit, `ssthresh = cwnd/2`, `cwnd = ssthresh` (not reset to 1) → resume Congestion Avoidance directly (avoids the full Slow Start penalty) — this is the key difference between **TCP Tahoe** (no fast recovery, always drops to Slow Start) and **TCP Reno** (has fast recovery).
- **Sketch a cwnd-vs-time graph:** sawtooth — exponential ramp (slow start) → linear ramp (congestion avoidance) → halve on loss → repeat.

**3-Way Handshake:** SYN → SYN-ACK → ACK (establishes sequence numbers both directions before data flows).

**DHCP:** automatically assigns IP addresses (+ subnet mask, gateway, DNS) to devices joining a network. **DNS:** resolves human-readable domain names ↔ IP addresses (hierarchical, distributed lookup).

---

## L12/L13 — Network Coding

**Core idea:** instead of just forwarding/storing packets, intermediate nodes treat packets as **algebraic equations** and combine them (e.g. XOR / linear combinations over a Galois Field). Receivers collect enough independent combinations and **solve the system of equations** (Gaussian elimination) to recover the original data.

- **Why network coding helps — classic examples:**
    
    - _Wireless relay (butterfly-style) example:_ XOR-ing two flows at a relay lets both endpoints extract their needed packet by XOR-ing again with what they already know — cuts the number of transmissions needed vs. plain forwarding.
    - _Multicast example:_ network coding can achieve the **max-flow (min-cut) capacity** for multicast, which plain routing/forwarding generally _cannot_ achieve when multiple sinks are involved — this is the theoretical justification for network coding (beats classical routing).
- **RLNC (Random Linear Network Coding):**
    
    - Each coded packet = random linear combination of source packets over a Galois Field `GF(2^m)` (e.g. GF(2), GF(2²), GF(256)...).
    - Sent together with its **encoding/coding vector** (the coefficients used) so the receiver knows which combination it got.
    - Receiver needs a number of **linearly independent** coded packets ≥ generation size to reach **full rank** and solve for all originals (Gaussian elimination).
    - Larger field size → lower probability of receiving a linearly-dependent (useless) packet, but higher per-packet coefficient overhead.
    - Binary field GF(2): coding reduces to plain **XOR** (cheapest, but weakest — more likely to get dependent/redundant combinations).
    - **Coupon collector problem** analogy: like collecting all N distinct coupons via random draws, the expected number of packets needed to reach full rank grows as ~`N·ln(N)` (diminishing returns — the last few "coupons"/independent packets are the hardest to get).
- **Coding coefficient strategies (compare):**
    
    - _RLNC (fully random):_ max robustness/flexibility, more overhead (need to send coefficients), highest computation (Gaussian elimination).
    - _Systematic:_ first packets sent = uncoded originals directly, coded packets sent only for the "extra"/redundancy — faster decoding if no losses, still recoverable if losses occur.
    - _Sparse codes:_ coefficients mostly zero → cheaper encode/decode, but weaker error-recovery guarantees.
    - _Tunable codes:_ adjustable sparsity/systematic-ness to trade off complexity vs robustness.
- **Recoding:** an intermediate/relay node can re-combine already-coded packets into new coded packets **without decoding first** — cheapest network operation, useful for multi-hop relaying (this is unique to network coding vs. classic store-and-forward).
    
- **Analog Network Coding (ANC):** combine signals directly in the _analog/RF domain_ (overheard/overlapping transmissions) rather than after digital decoding — exploits the natural superposition of radio waves; relevant to wireless relay throughput gains.
    

---

## Cross-Cutting "How to Solve" Recipes (numeric problem types)

|Problem type|Key steps|
|---|---|
|**Huffman tree**|merge 2 smallest probs repeatedly → assign bits top-down → L=Σpᵢlᵢ, H=−Σpᵢlog2pᵢ|
|**Repetition code error probs**|enumerate all 2^r received patterns w/ binomial probabilities → detect = not a valid codeword, decode-wrong = closer (Hamming distance) to wrong codeword|
|**Parity (1D/2D)**|count 1s → parity bit forces odd/even total; 2D = row parities + column parities (+corner)|
|**CRC**|append (deg) zeros → mod-2 (XOR) long division by generator polynomial → remainder = CRC|
|**Hamming(n,k) encode/decode**|parity bits at powers of 2 → each covers positions with matching binary digit → XOR to encode; XOR received-vs-recomputed parities = syndrome = error position|
|**ALOHA throughput**|t_packet = size/R → G=λ·t_packet → S=G·e^(−2G) [pure] or G·e^(−G) [slotted]|
|**Polling cycle time**|fixed per-station time × n + 2×total one-way propagation delay|
|**Efficiency/optimal packet size**|η(L) = [L/(L+H)]·(1−P₀)^(L+H) → dη/dL=0 → solve quadratic in L → plug back for max η|
|**Max-Flow / Min-Cut**|find augmenting paths (Ford-Fulkerson), push bottleneck flow, update residuals, repeat until none left|
|**Dijkstra shortest path**|init dist=∞ (0 for source) → repeatedly pick closest unvisited node, relax neighbors|
|**TCP cwnd sequence diagram**|slow start (double/RTT) until ssthresh or loss → linear +1/RTT (congestion avoidance) → on triple-dup-ACK: fast retransmit + fast recovery (ssthresh=cwnd/2, cwnd=ssthresh) vs on timeout: ssthresh=cwnd/2, cwnd=1|
|**RLNC full rank**|need ≥ generation-size linearly independent coded packets; expected packets needed ≈ N·ln(N) (coupon collector)|

---

_This guide consolidates both your lecture slides (L03–L13) and the worked tutorial exercises (2, 3, 4 solved in detail earlier in this chat). Good luck tomorrow!_