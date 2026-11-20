

# Network Coding for Multi-Link UAV Communications: Methods, Integration Strategies, and Recommended Choice

Unmanned Aerial Vehicles (UAVs) engaged in beyond-visual-line-of-sight (BVLOS) missions increasingly rely on heterogeneous links—Wi-Fi, 5G, Ku-band SATCOM, or LTE Direct—to meet stringent command, control, and payload requirements. Network coding offers a principled way to fuse these paths, masking loss and variable capacity while cutting latency. This report surveys current network-coding families, explains how each can be mapped onto the multi-link architecture described in your T9 research program, and identifies the best-fit scheme for low-latency, high-reliability UAV operation.

## Overview

Network coding replaces traditional per-packet retransmission with algebraic mixing, allowing any _k_ innovative packets to reconstruct _k_ originals. New coded packets can be sent proactively (“forward error correction”) or reactively (“on-the-fly”), and they may be generated at the source, at intermediate relays, or both. When different links fluctuate independently, coding across them smooths burst losses and delivers in-order data with fewer round trips, directly supporting your priority of **latency and reliability**.

## Fundamental Categories of Network Coding

|Category|Key Algorithms|Typical Block/Window Size|Feedback Dependency|Latency Profile|Multipath Affinity|Representative UAV Use Cases|
|---|---|---|---|---|---|---|
|Block Fountain Codes|LT[1](https://esa.hi.is/lt_code.html)[2](https://en.wikipedia.org/wiki/Luby_transform_code), Raptor, RaptorQ[3](https://errorcorrectionzoo.org/c/raptor)[4](https://en.wikipedia.org/wiki/Raptor_code)[5](https://www.qualcomm.com/content/dam/qcomm-martech/dm-assets/documents/Raptor_Codes_IEEE_technical_analysis.pdf)|1–65,535 symbols|ACK/NACK optional|Moderate (decoding waits until block complete)|Good (blocks can be striped across paths)|Bulk map/firmware uploads|
|Random Linear Network Coding (RLNC)|Dense RLNC[6](https://www.codeontechnologies.com/technology/rlnc-vs-traditional-codes), Systematic Sparse RLNC (sRLNC)[7](https://asu.elsevierpure.com/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multi-hop-networks)[8](https://www.codeontechnologies.com/technology/rlnc-faq), Sliding-Window RLNC[6](https://www.codeontechnologies.com/technology/rlnc-vs-traditional-codes)|32–512 symbols (block) or sliding window|Optional; enhances rate control|Medium (improves with systematic/sparse)|Excellent (sub-packets recoded per hop)|Telemetry bursts, BVLOS C2 redundancy|
|Instantly Decodable NC (IDNC)|XOR-based IDNC[9](https://arxiv.org/abs/1504.01218)[10](https://elib.dlr.de/81673/1/sc-arq.pdf)[11](https://arxiv.org/abs/1309.1323)|Small (≤10)|Per-packet or small group|Very low (decoding on arrival)|Good (easy XOR per path)|Broadcast of alerts to swarm|
|On-the-Fly Convolutional Codes|Tetrys (RFC 9407)[12](https://www.rfc-editor.org/rfc/rfc9407.html)[13](https://arxiv.org/abs/1204.1428)[14](https://datatracker.ietf.org/doc/rfc9407/)|Elastic window (typically 64-256 symbols)|Lightweight periodic feedback|Ultra-low (decoding within RTT-independent delay)|Designed for multipath[11](https://arxiv.org/abs/1309.1323)[14](https://datatracker.ietf.org/doc/rfc9407/)|Real-time C2, sensor streaming|
|Batched Network Codes|BATS[15](https://www.inc.cuhk.edu.hk/wp-content/uploads/INC/default/files/BATS.pdf)[16](https://openscience.isae-supaero.fr/digitalCollection/DigitalCollectionAttachmentDownloadHandler.ashx?parentDocumentId=8148&documentId=12916&skipWatermark=true&skipCopyright=true)[17](https://pmc.ncbi.nlm.nih.gov/articles/PMC10378412/), BAR recoding[18](https://www.mdpi.com/1099-4300/25/7/1054)|Batch 16–64, sub-batch recoding|None or sparse|Short (batch)|Very good (recoding preserves rank)|Multi-hop swarm relays|
|Physical-Layer & Complex Field NC|CFNC for UAV cooperative links[19](https://www.mdpi.com/1424-8220/20/6/1542)|Symbol-size|Channel pilots|PHY-level|PHY-specific|Formation flying with MIMO relays|
|Transport-Coupled NC|NC-MPTCP[20](https://www.cuiyong.net/lunwen/2012-%E7%BC%BA1/Network_coding_based_multipath_TCP.pdf)[21](https://dspace.mit.edu/handle/1721.1/90422), MPTCP/NC variant|Subflow packets|Implicit TCP ACKs|RTT-coupled|Intrinsic (per-subflow)|Hybrid Wi-Fi/5G downlink|

## Detailed Examination of Major Methods

## 1. Block Fountain Codes (LT, Raptor, RaptorQ)

- **Mechanism**: Rateless encoder generates limitless coded symbols until receivers collect _k+ε_ symbols.
    
- **Pros**: Near-capacity overhead (<1.6% with ε ≤0.02 for RaptorQ)[22](https://www.uni-bamberg.de/fileadmin/ktr/Dateien/Publikationen/RaptorCodesForP2PVideoStreaming.pdf); linear-time encode/decode[4](https://en.wikipedia.org/wiki/Raptor_code)[5](https://www.qualcomm.com/content/dam/qcomm-martech/dm-assets/documents/Raptor_Codes_IEEE_technical_analysis.pdf).
    
- **Cons**: Must buffer entire block; decoding delay scales with block length—undesirable for tight 50 ms UAV control loops.
    
- **Multipath Mapping**: Stripe symbols across interfaces; receivers can mix arrivals. Works well for high-volume imagery downlinks where 100–500 ms latency is tolerable.
    

## 2. Random Linear Network Coding (RLNC)

**a. Dense RLNC**

- Each coded packet is a random linear combination over GF(2^8), requiring Gaussian elimination at the sink[6](https://www.codeontechnologies.com/technology/rlnc-vs-traditional-codes).
    
- High computational cost: O(k³) decode unless optimized.
    

**b. Systematic & Sparse RLNC**

- Sends uncoded originals first, then coded redundancy to lower decoding complexity[8](https://www.codeontechnologies.com/technology/rlnc-faq).
    
- SpaRec algorithms preserve sparsity during recoding in multihop drones, cutting CPU load by ≈60%[7](https://asu.elsevierpure.com/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multi-hop-networks)[23](https://fis.tu-dresden.de/portal/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multihop-networks\(f7528227-6b07-4ff5-9008-358e4cdab93d\).html).
    

**c. Sliding-Window RLNC**

- Encoder maintains rolling window; new packets enter as old ones are ACKed[6](https://www.codeontechnologies.com/technology/rlnc-vs-traditional-codes).
    
- Reduces buffering delay; suitable for 5G-NR links with variable RTT.
    

**Fit to Multi-Link UAV**  
RLNC excels when the UAV acts as a relay node combining flows, or when intermediate ground relays recode for range extension. Systematic RLNC + sliding window can meet sub-100 ms deadlines for telemetry if window ≤32 symbols and GF(2^8) operations are hardware-accelerated.

## 3. Instantly Decodable Network Coding (IDNC)

- Coded packet is XOR of selective originals so that each receiver can resolve _one_ new symbol immediately[9](https://arxiv.org/abs/1504.01218)[10](https://elib.dlr.de/81673/1/sc-arq.pdf).
    
- Highly suited for multicast (e.g., fleet-wide warnings) but sacrifice throughput; coding opportunities shrink as state diverges.
    
- For point-to-point UAV links, gains over simple ARQ are modest unless several ground stations receive the same stream.
    

## 4. Tetrys (On-the-Fly Network Coding)

- **Elastic window** maintains un-ACKed originals; each new source packet triggers a coded packet computed on-the-fly[12](https://www.rfc-editor.org/rfc/rfc9407.html).
    
- **Delay Guarantee**: Recovers any erased packet within a deterministic number of received packets, independent of RTT[13](https://arxiv.org/abs/1204.1428).
    
- **Multipath Extension**: RFC 9407 explicitly allows per-path adaptive redundancy[14](https://datatracker.ietf.org/doc/rfc9407/); optimal policy sends repairs on slower path, natives on faster, ensuring in-order playback[13](https://arxiv.org/abs/1204.1428).
    
- **Complexity**: O(window²) worst-case but with window ≤128 and GF(2^16), software decode fits within 1 ms on ARM-Cortex.
    
- **Experimental Evidence**: Multipath Tetrys cut video freeze time by 55% vs FEC in burst loss tests on dual LTE+SAT paths[13](https://arxiv.org/abs/1204.1428)[16](https://openscience.isae-supaero.fr/digitalCollection/DigitalCollectionAttachmentDownloadHandler.ashx?parentDocumentId=8148&documentId=12916&skipWatermark=true&skipCopyright=true).
    

## 5. Batched Network Coding (BATS) and BAR Refine

- Encodes in small batches; inner random linear transform at relays maintains low buffer, constant header[15](https://www.inc.cuhk.edu.hk/wp-content/uploads/INC/default/files/BATS.pdf)[17](https://pmc.ncbi.nlm.nih.gov/articles/PMC10378412/).
    
- BAR (blockwise adaptive recoding) updates mixing matrix per channel report, improving rank without excess redundancy[18](https://www.mdpi.com/1099-4300/25/7/1054).
    
- Provides strong throughput with moderate delay; ideal for chain-topology swarms where each UAV hops data two to three times.
    

## 6. Transport-Layer Hybrids (Network-Coded MPTCP)

- MPTCP opens subflows across each interface; adding RLNC or XOR inside congestion window removes head-of-line blocking[20](https://www.cuiyong.net/lunwen/2012-%E7%BC%BA1/Network_coding_based_multipath_TCP.pdf)[21](https://dspace.mit.edu/handle/1721.1/90422).
    
- Demonstrated 25% higher goodput than plain MPTCP in Wi-Fi+Iridium vehicular tests[21](https://dspace.mit.edu/handle/1721.1/90422).
    
- Kernel patches exist for Linux 6.x; integration is straightforward with your VM-based multi-link simulator.
    

## Architectural Integration in a Multi-Link UAV Stack

## A. Link-Aware Encoder Scheduling

1. **Path Profiling**: Continuous estimation of per-path RTT, loss, and residual bandwidth via existing QoS probes.
    
2. **Code-Rate Adaptation**:
    
    - For Tetrys: adjust redundancy factor _r_ to keep decoding window occupancy below 50%[12](https://www.rfc-editor.org/rfc/rfc9407.html).
        
    - For RLNC: adapt systematic/coded ratio dynamically (e.g., sender transmits one coded packet every _n_ originals, where _n_ is inversely proportional to aggregated loss).
        
3. **Packet Allocation**:
    
    - **Fast Path (e.g., 5G ≤30 ms RTT)**: send native symbols to minimize decoding delay.
        
    - **Slow Path (e.g., SATCOM ≥550 ms RTT)**: ship coded repairs or low-priority payload.
        

## B. UAV Swarm Relays

- Intermediate UAVs recode rather than forward-store-forward; SpaRec or BAR keeps coefficient sparsity.
    
- Control channel (C2) uses window-32 Tetrys; payload channel can switch to BATS-64 for imagery.
    

## C. Transport Coupling

- Enable _mptcp_cc=’balia’_ with _net.mptcp.mptcp_enabled=1_ on Linux; integrate _kodo-rlnc_ library in user space for subflow coding.
    
- Congestion control remains per subflow; coding hides random losses, presenting smoother ACK clocking.
    

## Comparative Evaluation

## Quantitative Metrics (Typical Settings)

|Metric|Systematic Sliding-Window RLNC|Tetrys|RaptorQ|IDNC|BATS|
|---|---|---|---|---|---|
|Throughput Overhead @10% loss|15%[8](https://www.codeontechnologies.com/technology/rlnc-faq)|12%[12](https://www.rfc-editor.org/rfc/rfc9407.html)|8%[22](https://www.uni-bamberg.de/fileadmin/ktr/Dateien/Publikationen/RaptorCodesForP2PVideoStreaming.pdf)|≤5% but only for multicast[9](https://arxiv.org/abs/1504.01218)|10%[15](https://www.inc.cuhk.edu.hk/wp-content/uploads/INC/default/files/BATS.pdf)|
|Median Recovery Delay (64-byte cmd)|25 ms (window 32)[24](https://arxiv.org/abs/2003.00239)|6 ms (W=32, r=1/3)[12](https://www.rfc-editor.org/rfc/rfc9407.html)|>100 ms (block 256)|1–2 ms[10](https://elib.dlr.de/81673/1/sc-arq.pdf)|18 ms (batch 16)[15](https://www.inc.cuhk.edu.hk/wp-content/uploads/INC/default/files/BATS.pdf)|
|CPU Encode/Decode per 1 Mb|7 ms/12 ms on ARM A57[7](https://asu.elsevierpure.com/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multi-hop-networks)|5 ms/8 ms[12](https://www.rfc-editor.org/rfc/rfc9407.html)|3 ms/20 ms[4](https://en.wikipedia.org/wiki/Raptor_code)|1 ms/1 ms[10](https://elib.dlr.de/81673/1/sc-arq.pdf)|6 ms/9 ms[16](https://openscience.isae-supaero.fr/digitalCollection/DigitalCollectionAttachmentDownloadHandler.ashx?parentDocumentId=8148&documentId=12916&skipWatermark=true&skipCopyright=true)|
|Multipath Scalability (2–4 paths)|High (recoding native)|Very High (RFC 9407)|Medium (stripe only)|High|High|
|Code Feedback Needed|Sparse ACKs|Periodic window update|None|Frequent XOR maps|None|

_(Benchmarks aggregated from sources [7](https://asu.elsevierpure.com/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multi-hop-networks)[12](https://www.rfc-editor.org/rfc/rfc9407.html)[8](https://www.codeontechnologies.com/technology/rlnc-faq)[24](https://arxiv.org/abs/2003.00239)[4](https://en.wikipedia.org/wiki/Raptor_code)[22](https://www.uni-bamberg.de/fileadmin/ktr/Dateien/Publikationen/RaptorCodesForP2PVideoStreaming.pdf)[9](https://arxiv.org/abs/1504.01218)[15](https://www.inc.cuhk.edu.hk/wp-content/uploads/INC/default/files/BATS.pdf)[10](https://elib.dlr.de/81673/1/sc-arq.pdf))._

## Suitability Analysis for Your UAV Multi-Link Scenario

## Mandatory Requirements

1. **Command & Control (≤100 ms E2E, PER 10 ⁻⁵)**
    
2. **Telemetry & Health (≤300 ms, PER 10 ⁻⁴)**
    
3. **Sensor Video (≤500 ms, PER 10 ⁻³)**
    
4. **Bulk Data (no hard latency)**
    

## Method-to-Requirement Mapping

|Requirement|Preferred Code|Rationale|
|---|---|---|
|C2 & Flight Management|**Tetrys**|RTT-independent delay, elastic window absorbs burst loss, proven multipath scheduling[12](https://www.rfc-editor.org/rfc/rfc9407.html)[13](https://arxiv.org/abs/1204.1428)[14](https://datatracker.ietf.org/doc/rfc9407/).|
|Telemetry|Systematic Sliding-Window RLNC|Balances latency with lightweight headers; recoding eases UAV-to-UAV hop[7](https://asu.elsevierpure.com/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multi-hop-networks)[25](https://vtechworks.lib.vt.edu/bitstream/handle/10919/106939/Xu_B_T_2021.pdf?sequence=1).|
|Real-Time Video|Tetrys (low bit-rate) or IDNC for multicast|IDNC ensures instant frame availability when simultaneously streaming to control station and chase plane[9](https://arxiv.org/abs/1504.01218).|
|EO/IR High-Rate Video|BATS with BAR Recoding|Maintains throughput over 3-hop swarm while bounding delay[15](https://www.inc.cuhk.edu.hk/wp-content/uploads/INC/default/files/BATS.pdf)[18](https://www.mdpi.com/1099-4300/25/7/1054).|
|Bulk Map Upload|RaptorQ|Near-capacity efficiency; large block accepted[3](https://errorcorrectionzoo.org/c/raptor)[22](https://www.uni-bamberg.de/fileadmin/ktr/Dateien/Publikationen/RaptorCodesForP2PVideoStreaming.pdf).|

## Implementation Blueprint

## Encoder Module

1. Integrate **Kodo-C++** or **OpenRQ** for RLNC/RaptorQ.
    
2. Add **Tetrys encoder** (open-source C reference from IRTF NWCRG).
    
3. Expose REST API to VM-based link selector to request `(link_id, payload, coding_class)`.
    

## Link Selector

- Real-time decision logic:
    

text

`if packet.qos_class == C2:     use Tetrys_repair on slowest path    use Tetrys_native on fastest path elif packet.qos_class == TELEMETRY:     use sRLNC systematic native on best 2 paths    send redundancy (density 0.2) on path3 ...`

## Receiver

- Maintain per-algorithm decoder instances keyed by flow ID.
    
- Push decoded bytes to UTM stack; raise alarm if Tetrys decoding window >75% full (indicates link outage).
    

## Edge-Case Handling

- **Path Outage**: Coding rate auto-increases to maintain target decoding latency; if all coded traffic shifts to remaining links, congestion control (e.g., BBR) moderates send window.
    
- **Feedback Black-out**: Tetrys accommodates ACK loss[12](https://www.rfc-editor.org/rfc/rfc9407.html); RLNC falls back to higher redundancy after timeout.
    

## Practical Tips and Lessons Learned

1. **Coefficient Field Size**: GF(2^8) suffices for UAV payload; larger GF slows ARM cores without tangible reliability gain[6](https://www.codeontechnologies.com/technology/rlnc-vs-traditional-codes).
    
2. **Header Overhead**: Stick to _sparse_ coefficient vectors (≤8 non-zeros) to keep 20-byte Tetrys header small[12](https://www.rfc-editor.org/rfc/rfc9407.html)[23](https://fis.tu-dresden.de/portal/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multihop-networks\(f7528227-6b07-4ff5-9008-358e4cdab93d\).html).
    
3. **Redundancy Placement**: Empirical trials confirm putting repair on the _longest latency_ path minimizes in-order delay because decoded originals arrive mostly on fast links[13](https://arxiv.org/abs/1204.1428).
    
4. **GPU Offload**: For high-rate RLNC video, CUDA kernels deliver 8× speed-up; not needed for Tetrys C2 stream.
    
5. **Regulatory Compliance**: ICAO RCP requires bound on continuity; Tetrys window sizing offers calculable continuity probability, easing SPACOM safety case paperwork.
    

## Conclusion: Most Suitable Coding Method

Considering the twin goals of **latency** and **reliability**, **Tetrys emerges as the optimal primary coding layer** for UAV multi-link control and telemetry:

- Deterministic recovery delay independent of RTT or path length[12](https://www.rfc-editor.org/rfc/rfc9407.html).
    
- Native support for adaptive redundancy and multi-path scheduling, already documented in RFC 9407 Section 6.1[14](https://datatracker.ietf.org/doc/rfc9407/).
    
- Resilient to feedback loss—critical when SATCOM return channel is impaired[12](https://www.rfc-editor.org/rfc/rfc9407.html).
    
- Proven in dual-path testbeds to halve outage-induced stalls compared with FEC[16](https://openscience.isae-supaero.fr/digitalCollection/DigitalCollectionAttachmentDownloadHandler.ashx?parentDocumentId=8148&documentId=12916&skipWatermark=true&skipCopyright=true).
    

Complement Tetrys with **Systematic Sliding-Window RLNC** for moderate-latency data and **RaptorQ** for bulk transfers to optimize overall spectrum use. The integrated architecture outlined above can be deployed incrementally in your existing VM-based simulator and Omnet++ NTN testbed, positioning the T9 program at the forefront of resilient UAV communications.

1. [https://esa.hi.is/lt_code.html](https://esa.hi.is/lt_code.html)
2. [https://en.wikipedia.org/wiki/Luby_transform_code](https://en.wikipedia.org/wiki/Luby_transform_code)
3. [https://errorcorrectionzoo.org/c/raptor](https://errorcorrectionzoo.org/c/raptor)
4. [https://en.wikipedia.org/wiki/Raptor_code](https://en.wikipedia.org/wiki/Raptor_code)
5. [https://www.qualcomm.com/content/dam/qcomm-martech/dm-assets/documents/Raptor_Codes_IEEE_technical_analysis.pdf](https://www.qualcomm.com/content/dam/qcomm-martech/dm-assets/documents/Raptor_Codes_IEEE_technical_analysis.pdf)
6. [https://www.codeontechnologies.com/technology/rlnc-vs-traditional-codes](https://www.codeontechnologies.com/technology/rlnc-vs-traditional-codes)
7. [https://asu.elsevierpure.com/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multi-hop-networks](https://asu.elsevierpure.com/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multi-hop-networks)
8. [https://www.codeontechnologies.com/technology/rlnc-faq](https://www.codeontechnologies.com/technology/rlnc-faq)
9. [https://arxiv.org/abs/1504.01218](https://arxiv.org/abs/1504.01218)
10. [https://elib.dlr.de/81673/1/sc-arq.pdf](https://elib.dlr.de/81673/1/sc-arq.pdf)
11. [https://arxiv.org/abs/1309.1323](https://arxiv.org/abs/1309.1323)
12. [https://www.rfc-editor.org/rfc/rfc9407.html](https://www.rfc-editor.org/rfc/rfc9407.html)
13. [https://arxiv.org/abs/1204.1428](https://arxiv.org/abs/1204.1428)
14. [https://datatracker.ietf.org/doc/rfc9407/](https://datatracker.ietf.org/doc/rfc9407/)
15. [https://www.inc.cuhk.edu.hk/wp-content/uploads/INC/default/files/BATS.pdf](https://www.inc.cuhk.edu.hk/wp-content/uploads/INC/default/files/BATS.pdf)
16. [https://openscience.isae-supaero.fr/digitalCollection/DigitalCollectionAttachmentDownloadHandler.ashx?parentDocumentId=8148&documentId=12916&skipWatermark=true&skipCopyright=true](https://openscience.isae-supaero.fr/digitalCollection/DigitalCollectionAttachmentDownloadHandler.ashx?parentDocumentId=8148&documentId=12916&skipWatermark=true&skipCopyright=true)
17. [https://pmc.ncbi.nlm.nih.gov/articles/PMC10378412/](https://pmc.ncbi.nlm.nih.gov/articles/PMC10378412/)
18. [https://www.mdpi.com/1099-4300/25/7/1054](https://www.mdpi.com/1099-4300/25/7/1054)
19. [https://www.mdpi.com/1424-8220/20/6/1542](https://www.mdpi.com/1424-8220/20/6/1542)
20. [https://www.cuiyong.net/lunwen/2012-%E7%BC%BA1/Network_coding_based_multipath_TCP.pdf](https://www.cuiyong.net/lunwen/2012-%E7%BC%BA1/Network_coding_based_multipath_TCP.pdf)
21. [https://dspace.mit.edu/handle/1721.1/90422](https://dspace.mit.edu/handle/1721.1/90422)
22. [https://www.uni-bamberg.de/fileadmin/ktr/Dateien/Publikationen/RaptorCodesForP2PVideoStreaming.pdf](https://www.uni-bamberg.de/fileadmin/ktr/Dateien/Publikationen/RaptorCodesForP2PVideoStreaming.pdf)
23. [https://fis.tu-dresden.de/portal/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multihop-networks(f7528227-6b07-4ff5-9008-358e4cdab93d).html](https://fis.tu-dresden.de/portal/en/publications/sparec-sparse-systematic-rlnc-recoding-in-multihop-networks\(f7528227-6b07-4ff5-9008-358e4cdab93d\).html)
24. [https://arxiv.org/abs/2003.00239](https://arxiv.org/abs/2003.00239)
25. [https://vtechworks.lib.vt.edu/bitstream/handle/10919/106939/Xu_B_T_2021.pdf?sequence=1](https://vtechworks.lib.vt.edu/bitstream/handle/10919/106939/Xu_B_T_2021.pdf?sequence=1)
26. [https://www.youtube.com/watch?v=nF_crEtmpBo](https://www.youtube.com/watch?v=nF_crEtmpBo)
27. [https://www.rlmc.edu.pk/rlnc/](https://www.rlmc.edu.pk/rlnc/)
28. [https://github.com/raffidil/arlnc](https://github.com/raffidil/arlnc)
29. [https://gist.github.com/straker/3c98304f8a6a9174efd8292800891ea1](https://gist.github.com/straker/3c98304f8a6a9174efd8292800891ea1)
30. [https://divan.dev/posts/fountaincodes/](https://divan.dev/posts/fountaincodes/)
31. [https://www.rlnc.edu](https://www.rlnc.edu/)
32. [https://en.wikipedia.org/wiki/Kodu_Game_Lab](https://en.wikipedia.org/wiki/Kodu_Game_Lab)
33. [https://en.wikipedia.org/wiki/Fountain_code](https://en.wikipedia.org/wiki/Fountain_code)
34. [https://en.wikipedia.org/wiki/Multipath_TCP](https://en.wikipedia.org/wiki/Multipath_TCP)
35. [https://arxiv.org/abs/2409.11058](https://arxiv.org/abs/2409.11058)
36. [https://blog.cloudflare.com/multi-path-tcp-revolutionizing-connectivity-one-path-at-a-time/](https://blog.cloudflare.com/multi-path-tcp-revolutionizing-connectivity-one-path-at-a-time/)
37. [http://www.mosaic-lab.org/uploads/papers/801a3607-b8a5-4aad-bdea-ecc1ed305561.pdf](http://www.mosaic-lab.org/uploads/papers/801a3607-b8a5-4aad-bdea-ecc1ed305561.pdf)
38. [https://repository.kaust.edu.sa/bitstreams/715709fb-5fbf-4136-84be-2d39d6feae59/download](https://repository.kaust.edu.sa/bitstreams/715709fb-5fbf-4136-84be-2d39d6feae59/download)
39. [https://datatracker.ietf.org/doc/html/draft-irtf-nwcrg-tetrys-04](https://datatracker.ietf.org/doc/html/draft-irtf-nwcrg-tetrys-04)
40. [https://arxiv.org/abs/2408.16365](https://arxiv.org/abs/2408.16365)


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
- You are effectively implementing **Layer 3 Network Coding**. While your Iridium/Starlink modem handles the _Physical_ error correction (LDPC) internally, that only protects the link from "Atmosphere to Antenna." It does _not_ protect against network congestion or handover drops. By adding NC on your **Onboard Computer**, you are adding an end-to-end reliability layer that commercial Satcom modems do not provide by default.
---
### Network coding for hetereogenous multi-link connectivity 
- https://ieeexplore.ieee.org/abstract/document/9498620

### Osel work 

Caterpillar - Pace RLNC
 - https://ieeexplore.ieee.org/document/8003268
 - https://ieeexplore.ieee.org/abstract/document/8052109 
Summary of Osel's work 




### New to explore 

- graph model and network coding - The Kronecker graph model above describes the physical multibeam geometry according to the hexagonal tesselation given by the system model. https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6655239
- Link State awareness network coding 
- adaptive network coding scheme 
- network coding (NC) in the application layer for realizing more stability and reliability.
Network coding in Network (L3) and Application layer (L7)

- Synchronization  other points to explore - https://ieeexplore.ieee.org/abstract/document/8442457/authors#authors 