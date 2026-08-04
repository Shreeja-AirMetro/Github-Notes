https://github.com/binhfdv/pcl_handson 

16 slides 

L1 - 64

E1  - 16

L3 - 90

L4 - 75

L5 - 31


# ComNets-2 — Final Revision Sheet (last-hour version)

Dense, scannable, exam-day format. Read top to bottom once, then use the rapid-fire section as your final pass.

---

## 1. Master Glossary — every acronym, grouped

**NFV** PNF (Physical NF) · VNF (Virtual NF) · NFVI (NFV Infrastructure) · MANO (Management & Orchestration) · VIM (Virtualized Infra Manager) · VNFM (VNF Manager) · SFC (Service Function Chaining) · DPDK (Data Plane Development Kit) · eBPF (extended Berkeley Packet Filter) · XDP (eXpress Data Path, eBPF extension)

**SDN** CP/DP/MP (Control/Data/Management Plane) · NOS (Network Operating System) · SI/NI (Southbound/Northbound Interface) · TCAM (Ternary Content-Addressable Memory) · TLV/OXM (Type-Length-Value / OpenFlow Extensible Match) · POF (Protocol Oblivious Forwarding) · OVSDB (Open vSwitch Database) · ForCES (Forwarding and Control Element Separation)

**MEC** MCC (Mobile Cloud Computing) · ETSI MEC · QoE (Quality of Experience) · MEC host / MEC system level

**Network Slicing / 5G general** SST (Slice/Service Type) · SD (Slice Differentiator) · eMBB / URLLC / mMTC · IMT-2020 · 5GS (5G System) · UE / gNB / 5GC

**5G Core** SBA (Service-Based Architecture) · CUPS (Control & User Plane Separation) · NRF (Network Repository Function) · AMF (Access & Mobility Mgmt Function) · SMF (Session Mgmt Function) · UPF (User Plane Function) · UDM (Unified Data Mgmt) · PCF (Policy Control Function) · NEF (Network Exposure Function) · AF (Application Function) · NAS (Non-Access Stratum) · NGAP (NG Application Protocol) · SBI (Service-Based Interface) · PFCP (Packet Forwarding Control Protocol) · GTP-U (GPRS Tunneling Protocol – User plane) · TEID (Tunnel Endpoint Identifier) · SCTP (Stream Control Transmission Protocol) · 5GMM / 5GSM (5G Mobility/Session Management) · PDU Session · N1–N9 (reference points)

**5G RAN** SDAP (Service Data Adaptation Protocol) · RRC (Radio Resource Control) · PDCP (Packet Data Convergence Protocol) · RLC (Radio Link Control: TM/UM/AM) · MAC (Medium Access Control) · PHY (Physical layer) · QFI (QoS Flow ID) · MCG/SCG (Master/Secondary Cell Group) · gNB, O-RU/O-DU/O-CU (O-CU-CP/O-CU-UP) · CPRI (Common Public Radio Interface) · Open Fronthaul · F1 interface

**TSN** PTP (Precision Time Protocol, IEEE 1588) · 802.1AS (TSN time sync) · TAS (Time-Aware Shaper, 802.1Qbv) · CBS (Credit-Based Shaper, 802.1Qav) · ATS (Asynchronous Traffic Shaper, 802.1Qcr) · FRER (Frame Replication & Elimination for Reliability, 802.1CB) · PCR (Path Control & Reservation, 802.1Qca) · PSFP (Per-Stream Filtering & Policing, 802.1Qci) · SRP (Stream Reservation Protocol, 802.1Qat/Qcc) · CQF (Cyclic Queuing & Forwarding, 802.1Qch) · DS-TT/NW-TT (Device-Side/Network-Side TSN Translator)

---

## 2. Concept Maps (text mind-maps)

### NFV

```
NFV
├── WHY: middleboxes = costly, vendor-locked hardware → move to software on general-purpose HW
├── ARCHITECTURE (ETSI)
│   ├── NFVI = data plane (compute+storage+network, virtualization layer)
│   ├── VNFs = software functions running on NFVI
│   └── MANO = orchestrates everything (VIM manages NFVI, VNFM manages VNF lifecycle, NFVO orchestrates services)
├── SFC = ordered chain of VNFs traffic must pass through (order matters)
├── LOW-LATENCY techniques
│   ├── DPDK = user-space bypass, high throughput, HW-specific
│   ├── eBPF/XDP = safe in-kernel programs, low latency, limited complexity
│   └── CALVIN = elementary NFs→kernel, advanced→user space, one vNF per VM, no context switching
└── STATELESS NF = decouple state from processing instance → elasticity + fast failover
```

### SDN

```
SDN
├── WHY: CP+DP tightly coupled in traditional routers → rigid, vendor lock-in, hard to innovate
├── 4 PILLARS: decoupled CP/DP · flow-based forwarding · external control (NOS) · programmability
├── 3 ABSTRACTIONS: forwarding · distribution · specification
├── LAYERS (bottom→top)
│   Infrastructure → Southbound (OpenFlow/OVSDB/ForCES/POF) → Network Hypervisor (FlowVisor)
│   → NOS/Controller (Ryu/ONOS/ODL) → Northbound (REST) → Applications (LB, security, TE, monitoring)
└── OpenFlow: flow table = match + action + counters; miss → default rule or discard
```

### MEC

```
MEC
├── DEFINITION (ETSI): IT/cloud capability at RAN edge, close to subscribers
├── 5 TRAITS: on-premises · proximity · low latency · location-aware · network-context-aware
├── vs FOG vs CLOUDLET: MEC=BS/1 hop; Fog=distributed/1-N hops; Cloudlet=local install/1 hop
├── ENABLERS: SDN (maintain connectivity during app migration) + NFV (automated app provisioning)
├── USE CASES: consumer (AR/VR/gaming) · operator/3rd-party (tracking/security) · network perf (caching)
└── FRAMEWORKS: OpenStack/Kubernetes = cloud platform; ONOS/Calico = SDN platform
```

### Network Slicing

```
SLICING
├── WHY: "one-size-fits-all" can't serve eMBB + URLLC + mMTC simultaneously
├── SLICED DIMENSIONS: bandwidth · topology · device CPU · storage · control plane
├── 5G IDENTIFIERS: SST (type: eMBB/URLLC/mMTC) + SD (differentiator within same SST)
└── 3GPP TASKS: provisioning · association mgmt · interoperating (roaming) · perf/isolation
```

### TSN

```
TSN = IEEE Ethernet standards for determinism, mostly Layer 2
├── PROBLEM: reliability + low latency + sync + cost → beyond fieldbus (ProfiNet/EtherCAT/CAN)
├── DELAY TYPES: processing (integrity+switching=fixed; address lookup=jitter) · queuing (bottleneck)
│                 · transmission (bandwidth) · propagation (distance/medium)
├── 4 PILLARS OF TSN
│   ├── Time sync → PTP (IEEE1588) + 802.1AS (nanosecond accuracy, master/slave hierarchy)
│   ├── Latency & PDV → 802.1Qbv (TAS, TDMA gates) + 802.1Qbu/802.3br (frame preemption)
│   │                    + 802.1Qav (CBS) + 802.1Qcr (ATS) + 802.1Qch (CQF)
│   ├── Ultra-reliability → 802.1CB (FRER: duplicate+eliminate) + 802.1Qca (PCR) + 802.1Qci (PSFP)
│   └── Resource mgmt → 802.1Qat (SRP) + 802.1Qcc (enhanced SRP, centralized config)
└── 5G-TSN (Rel.16): 5GS = virtual TSN bridge; DS-TT/NW-TT translate QoS ↔ TSN stream reqs
```

---

## 3. COMPLETE FLOW — 5G Core: UE Registration → PDU Session → Data Transfer

**Stage 0 — Before Core involved:** UE does cell search (reads SSB/MIB/SIB), performs RACH (4-step random access) to get an RRC connection to the gNB. _(RAN-layer, not Core.)_

**Stage 1 — Registration (5GMM, over NAS)**

1. UE → gNB → AMF: **Registration Request** (NAS message, carried via **NGAP** over **SCTP**). UE presents SUCI (or 5G-GUTI if previously registered).
2. AMF ↔ UDM/AUSF: **Authentication** (5G-AKA) — RAND/AUTN exchanged, mutual authentication.
3. **Security Mode Command/Complete** — NAS security context established; messages become ciphered from here on.
4. AMF confirms **Registration Accept** to UE. UE is now in **5GMM-REGISTERED** state.
5. Throughout: AMF used NGAP (to gNB) and NAS (to UE) — this is 5GMM = mobility management, registration, authentication, security.

**Stage 2 — PDU Session Establishment (5GSM, over NAS)**

1. UE → AMF: **PDU Session Establishment Request** (5GSM/NAS, forwarded transparently by AMF).
2. AMF → SMF: selects and forwards request to SMF (via SBI, HTTP/2/REST).
3. SMF: allocates UE IP address, selects UPF, and — via **PFCP over N4** — instructs UPF how to forward (QoS rules, TEIDs).
4. SMF → AMF → gNB → UE: session parameters returned; **QoS Flow(s)** established with QFI.
5. gNB configures **SDAP** (maps QoS flow ↔ radio bearer) and **PDCP/RLC/MAC/PHY** for the radio bearer.
6. UE now has an active **PDU Session** = logical data path from UE to Data Network.

**Stage 3 — Data Transfer (User Plane)**

1. UE sends IP packet → gNB (over the radio bearer, SDAP marks QFI).
2. gNB encapsulates it in **GTP-U** tunnel (UDP port 2152) using the session's **TEID**, sends over **N3** to UPF.
3. UPF de-tunnels, applies QoS/policy enforcement (per QFI), forwards to Data Network over **N6**.
4. Return traffic: UPF re-encapsulates in GTP-U (N3) back to gNB → SDAP/radio bearer → UE.

**Protocol summary table**

|Interface|Between|Protocol|
|---|---|---|
|N1|UE ↔ AMF|NAS (5GMM/5GSM)|
|N2|gNB ↔ AMF|NGAP over SCTP|
|N3|gNB ↔ UPF|GTP-U (user data, UDP/2152)|
|N4|SMF ↔ UPF|PFCP (control)|
|N6|UPF ↔ Data Network|IP|
|SBI (N-x)|AMF/SMF/NRF/...|HTTP/2 + REST|

**Core NFs — one-line each**

- **NRF**: registry — NFs register + discover each other; makes core cloud-native.
- **AMF**: first contact, mobility/registration/security, protocols NAS/NGAP/SBI.
- **SMF**: session lifecycle, IP allocation, controls UPF via PFCP/N4.
- **UPF**: only NF that touches user data; gateway N3↔N6; enforces QoS by QFI marking.

---

## 4. COMPLETE FLOW — 5G RAN: Protocol Stack + Channel Mapping + O-RAN Split

**User-plane stack (top → bottom):**

```
SDAP   → maps QoS flow (QFI, from Core) to a radio bearer
PDCP   → ciphering, integrity, header compression, in-order delivery
RLC    → segmentation/reassembly; TM (none) / UM (no ARQ) / AM (ARQ retransmit)
MAC    → scheduling, multiplexing logical→transport channels, HARQ; separate per MCG/SCG
PHY    → coding, modulation, mapping transport→physical channels, actual air transmission
```

Control plane runs **RRC** in parallel with PDCP (connection setup, mobility/handover, bearer config) — RRC messages themselves flow down through PDCP→RLC→MAC→PHY like any other data.

**Channel mapping (top → bottom):**

```
Logical channels (what):      BCCH, PCCH, CCCH, DCCH, DTCH
        ↓ (MAC multiplexes)
Transport channels (how):     BCH, PCH, DL-SCH, UL-SCH
        ↓ (PHY maps)
Physical channels (air):      PBCH, PDCCH/PUCCH, PDSCH/PUSCH, PRACH
```

Example: RRC signaling → DCCH (logical) → DL-SCH/UL-SCH (transport) → PDSCH/PUSCH (physical).

**Functional split (3GPP Options 1–8):** higher option number = split closer to PHY/RF = more centralized = higher fronthaul bandwidth/latency demand (Option 8 ≈ classic C-RAN). Lower option number = split closer to RRC = more distributed = relaxed fronthaul (Option 2 ≈ PDCP/RLC boundary).

**O-RAN disaggregation:**

```
O-RU (RF + low-PHY)  --[Open Fronthaul, Split 7.2x]-->  O-DU (high-PHY, MAC, RLC)  --[F1, Split 2]-->  O-CU
                                                                                                      ├── O-CU-CP (RRC + PDCP-C)
                                                                                                      └── O-CU-UP (SDAP + PDCP-U)
```

One O-CU pair can serve multiple O-DUs; one O-DU can serve multiple O-RUs. **Open RAN** = the general principle (open interfaces). **O-RAN** = the O-RAN Alliance's specific implementation of that principle.

**O-RAN motivations (know 3):** vendor lock-in mitigation / lower market-entry barrier · flexibility + lower OPEX · cell densification (small cells at high freq.) · AI-enabled functionality (via open data at each interface, RIC) · future-proofing (software upgrades vs. hardware swaps).

---

## 5. Rapid-fire — the exact things people mix up under pressure

- **NRF ≠ UDM.** NRF = registry of _network functions_ (service discovery). UDM = subscriber data.
- **AMF = Access and Mobility Management Function** (not "Authentication Management").
- **SBI = Service-Based Interface** (not "service broadcast information").
- **SMF↔UPF = PFCP over N4** (control). **gNB↔UPF = GTP-U over N3** (user data). Don't swap these.
- **PFCP is deliberately outside the SBI** — for privacy, scalability, flexibility.
- **5GMM** = registration/mobility/security. **5GSM** = PDU session establishment/mgmt. Both ride on NAS. Neither is the RACH/cell-search procedure — that's PHY/MAC-layer, happens _before_ NAS registration.
- **TEID** identifies a specific tunnel/PDU session, not "a user."
- **SDAP is RAN (UE↔gNB)**, marks QFI on the radio side. UPF enforces QoS on the core side by _reading/marking_ QFI — two different mechanisms, don't merge them.
- **MAC layer** = scheduling/multiplexing/HARQ — not routing/forwarding (that's not its job in this stack).
- **RLC modes:** TM = no seg/ARQ (broadcast/paging) · UM = seg, no ARQ (delay-sensitive) · AM = seg + ARQ (reliable).
- **Channel order:** Logical → Transport → Physical (top to bottom, never reversed).
- **Split numbering:** higher number = more centralized/more fronthaul demand (Option 8); lower number = more distributed/relaxed fronthaul (Option 2). O-RAN uses 7.2x (fronthaul, O-RU↔O-DU) and 2 (F1, O-DU↔O-CU).
- **Open RAN vs O-RAN:** Open RAN = principle; O-RAN = the Alliance's specific spec.
- **SDN pillars vs abstractions:** 4 pillars (decouple, flow-based, external control, programmability) ≠ 3 abstractions (forwarding, distribution, specification) — don't conflate.
- **Southbound vs Northbound:** Southbound = controller↔switches (OpenFlow). Northbound = controller↔apps (REST).
- **MEC vs Fog vs Cloudlet:** MEC = base station/RAN, 1 hop, high compute. Fog = distributed near end device, 1–N hops, medium compute. Cloudlet = local install, 1 hop, high compute.
- **SST vs SD:** SST = slice type (eMBB/URLLC/mMTC). SD = differentiates slices sharing the same SST.
- **TSN 4 pillars:** time sync, latency & PDV improvement, ultra-reliability, resource management — know one standard per pillar (802.1AS / 802.1Qbv+Qbu / 802.1CB / 802.1Qat-Qcc).
- **NFV vs cloud computing bottleneck:** cloud = CPU-bound, node-centric; NFV = memory/I/O-bound, network-centric, NUMA-aware, few large VMs.
- **DPDK vs eBPF/XDP:** DPDK = user-space bypass (throughput ↑, HW-specific, complex). eBPF/XDP = in-kernel sandboxed (low latency, safety, limited program complexity).

---

_Good luck. If your mind blanks on an acronym in the room, say what plane/interface it's on first ("that's a core control-plane function...") — it buys you a second and often the rest follows._