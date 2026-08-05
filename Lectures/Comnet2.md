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

# ComNets-2 — Full Term Glossary (one-line definitions)

Organized by topic. Each line: **Term** — definition.

---

## NFV — Network Function Virtualization

- **Middlebox** — any intermediary network device performing functions beyond standard IP router forwarding (RFC 3234).
- **PNF (Physical Network Function)** — a network function tightly coupled to dedicated physical hardware.
- **VNF (Virtual Network Function)** — the software equivalent of a PNF, running on general-purpose hardware, providing the same functional behavior.
- **NFVI (NFV Infrastructure)** — the combined hardware and virtualization layer (compute, storage, network) on which VNFs run.
- **MANO (Management and Orchestration)** — the ETSI framework layer responsible for orchestrating NFVI resources and VNF lifecycles.
- **VIM (Virtualized Infrastructure Manager)** — manages/allocates virtualized compute, storage, and network resources within the NFVI.
- **VNFM (VNF Manager)** — manages the lifecycle (instantiation, scaling, termination) of individual VNFs.
- **NFVO (NFV Orchestrator)** — orchestrates end-to-end network services composed of multiple VNFs.
- **Hypervisor (Type 1 / bare-metal)** — virtualization software running directly on hardware; more secure and performant, preferred in data centers.
- **Hypervisor (Type 2 / hosted)** — virtualization software running as an application on top of a host operating system.
- **SFC (Service Function Chaining)** — an ordered sequence of network functions that traffic must traverse, where the order affects correctness.
- **DPDK (Data Plane Development Kit)** — a set of user-space libraries that bypass kernel packet processing to boost throughput, at the cost of hardware-specific complexity.
- **eBPF (extended Berkeley Packet Filter)** — a technology for running sandboxed, verified programs inside the OS kernel at runtime without modifying the kernel itself.
- **XDP (eXpress Data Path)** — an eBPF extension enabling very early, high-speed packet processing before the kernel's normal networking stack.
- **CALVIN** — a low-latency vNF architecture that keeps each vNF entirely in kernel space or entirely in user space (never split) to eliminate context-switching overhead.
- **Stateless NF** — a network function design that centralizes state outside the NF instance, enabling seamless elasticity and fast failover.
- **Flow affinity** — the requirement that all packets of a flow be processed by the same (stateful) NF instance holding that flow's state.

---

## SDN — Software-Defined Networking

- **Data plane** — the part of a network device that forwards packets according to its forwarding table.
- **Control plane** — the logic (protocols like OSPF/BGP) that computes and populates forwarding tables.
- **Management plane** — human/script-driven configuration and monitoring of network devices.
- **Forwarding** — a data-plane action: sending a packet to an outgoing link based on a table lookup.
- **Routing** — a control-plane process: computing the best paths packets should follow.
- **NOS (Network Operating System)** — the SDN controller software that abstracts the network for control applications, analogous to an OS abstracting hardware.
- **Flow** — a set of packets defined by a match/filter criterion that receive identical forwarding treatment.
- **Southbound interface** — the interface between the SDN controller and the forwarding devices (e.g., OpenFlow).
- **Northbound interface** — the interface between the SDN controller and network applications (typically REST APIs).
- **OpenFlow** — the standard southbound protocol defining flow tables (match + action + counters) for programmable switches.
- **TLV / OXM (Type-Length-Value / OpenFlow Extensible Match)** — an extensible field format introduced in OpenFlow v1.2+ for adding new match/port/table fields without redesigning the protocol.
- **POF (Protocol Oblivious Forwarding)** — an approach where switches are protocol-agnostic "white boxes," with packet parsing delegated entirely to the controller.
- **OVSDB (Open vSwitch Database protocol)** — a southbound protocol complementary to OpenFlow, used for advanced virtual switch configuration (QoS, tunnels, queues).
- **ForCES (Forwarding and Control Element Separation)** — an IETF architecture separating control and data planes logically, without requiring a fully external centralized controller.
- **FlowVisor** — an early network hypervisor that slices SDN infrastructure (bandwidth, topology, traffic, CPU, flow tables) across multiple controllers/tenants.
- **Network hypervisor** — software that virtualizes SDN infrastructure so multiple logical networks can share the same physical substrate.

---

## MEC — Mobile/Multi-access Edge Cloud

- **MEC (per ETSI)** — an IT service environment and cloud computing capability located at the edge of the mobile network, close to subscribers.
- **Fog computing** — a distributed computing paradigm placing compute resources near end devices, potentially across multiple hops.
- **Cloudlet** — a small-scale, locally installed cloud data center, typically one hop from the user.
- **Full offloading** — sending an entire computation task from the mobile device to the MEC server.
- **Partial offloading** — splitting a computation task between local device processing and MEC server processing.
- **Mobile edge system level** — the MEC framework layer providing the global system view and handling requests.
- **Mobile edge host level** — the MEC framework layer performing application lifecycle management on a specific host.
- **Virtual machine (VM)** — a software emulation of a full computer, including its own OS, running on shared hardware.
- **Container** — a lightweight packaging of application code and dependencies that shares the host OS kernel.

---

## Network Slicing & 5G Service Types

- **Network slicing** — overlaying multiple isolated virtual networks on a shared physical network domain, each tailored to specific requirements.
- **SST (Slice/Service Type)** — the basic type identifier of a network slice (e.g., eMBB, URLLC, mMTC).
- **SD (Slice Differentiator)** — an identifier distinguishing multiple slices that share the same SST.
- **eMBB (enhanced Mobile Broadband)** — 5G service type optimized for high data rates (e.g., streaming, up to ~20 Gbps peak).
- **URLLC (Ultra-Reliable Low-Latency Communications)** — 5G service type optimized for near-real-time, highly reliable, low-latency applications (e.g., industrial control, robotics).
- **mMTC (massive Machine-Type Communications)** — 5G service type optimized for very high device density, long battery life, and infrequent small data transmissions (e.g., smart metering).
- **IMT-2020** — the ITU framework defining the requirement categories (eMBB/URLLC/mMTC) that 5G systems must meet.
- **UE (User Equipment)** — the end-user device connecting to the mobile network.
- **gNB (Next Generation Node B)** — the 5G base station supporting 5G New Radio.
- **5GC (5G Core)** — the core network processing/control component of the 5G System.

---

## 5G Core Network

- **SBA (Service-Based Architecture)** — the 5G Core design where network functions expose/consume services over a shared HTTP/2+REST bus, replacing fixed point-to-point interfaces.
- **CUPS (Control and User Plane Separation)** — separating control-plane and user-plane network functions so the user plane can be placed closer to the user and scaled independently.
- **NRF (Network Repository Function)** — the central registry where NFs register their capabilities and discover other NFs, enabling the 5G Core's cloud-native, dynamic composition.
- **AMF (Access and Mobility Management Function)** — the first point of contact for RAN/UE, handling registration, connection, and mobility management.
- **SMF (Session Management Function)** — manages PDU session lifecycle, UE IP allocation, and QoS, controlling the UPF via PFCP.
- **UPF (User Plane Function)** — the data-plane gateway between the RAN (N3) and the Data Network (N6), enforcing QoS by marking/reading QFI.
- **UDM (Unified Data Management)** — stores and manages subscriber data and subscription profiles.
- **PCF (Policy Control Function)** — provides policy rules to control-plane functions to enforce network policies.
- **NEF (Network Exposure Function)** — securely exposes 5G Core capabilities/data to external applications.
- **AF (Application Function)** — represents third-party or operator applications interacting with the 5G Core (e.g., for policy influence).
- **NAS (Non-Access Stratum)** — the signaling protocol carried between the UE and the core network (AMF), independent of the radio access technology.
- **NGAP (NG Application Protocol)** — the signaling protocol used between the gNB and the AMF over the N2 interface.
- **SBI (Service-Based Interface)** — the HTTP/2+REST interface used by NFs to communicate within the Service-Based Architecture.
- **PFCP (Packet Forwarding Control Protocol)** — the control-plane protocol used by the SMF to configure and control the UPF, over the N4 interface.
- **GTP-U (GPRS Tunneling Protocol – User plane)** — the protocol encapsulating user IP packets in a tunnel between the gNB and UPF (N3), typically over UDP port 2152.
- **TEID (Tunnel Endpoint Identifier)** — a field in the GTP-U header identifying a specific tunnel/PDU session.
- **SCTP (Stream Control Transmission Protocol)** — the transport protocol carrying NGAP signaling between gNB and AMF.
- **5GMM (5G Mobility Management)** — the NAS sub-layer handling UE registration, authentication, mobility, and security procedures.
- **5GSM (5G Session Management)** — the NAS sub-layer handling PDU session establishment, modification, and release.
- **PDU Session** — the logical data connection/path between the UE and a Data Network, carrying one or more QoS flows.
- **QFI (QoS Flow Identifier)** — an identifier marking which QoS flow a packet belongs to, used across RAN and Core.
- **N1–N9** — the standardized 5G Core reference points/interfaces connecting specific pairs of network functions (e.g., N1=UE-AMF, N2=gNB-AMF, N3=gNB-UPF, N4=SMF-UPF, N6=UPF-DN).

---

## 5G RAN — Radio Access Network Protocol Stack

- **SDAP (Service Data Adaptation Protocol)** — maps QoS flows (via QFI) from the core network onto radio bearers; user-plane only.
- **RRC (Radio Resource Control)** — the control-plane protocol managing connection setup/release, mobility/handover, and radio bearer configuration.
- **PDCP (Packet Data Convergence Protocol)** — performs ciphering, integrity protection, header compression, and in-order delivery, for both planes.
- **RLC (Radio Link Control)** — handles segmentation/reassembly and (in some modes) retransmission of radio-layer data.
- **RLC-TM (Transparent Mode)** — no segmentation, reassembly, or retransmission; used for minimal-overhead broadcast/paging messages.
- **RLC-UM (Unacknowledged Mode)** — segmentation/reassembly without retransmission; used for delay-sensitive traffic.
- **RLC-AM (Acknowledged Mode)** — segmentation/reassembly with ARQ retransmission; used for traffic requiring reliable delivery.
- **MAC (Medium Access Control)** — handles scheduling, multiplexing of logical channels onto transport channels, and HARQ.
- **PHY (Physical layer)** — performs coding, modulation, and the actual transmission over the air interface.
- **Logical channel** — defines the type of data being carried between RLC and MAC (e.g., BCCH, PCCH, CCCH, DCCH, DTCH).
- **Transport channel** — defines how data is transported over the radio between MAC and PHY (e.g., BCH, PCH, DL-SCH, UL-SCH).
- **Physical channel** — the actual air-interface resource carrying a transport channel (e.g., PDSCH, PUSCH, PDCCH, PBCH, PRACH).
- **MCG (Master Cell Group)** — the primary serving cell(s) anchored to the primary node, with its own MAC entity.
- **SCG (Secondary Cell Group)** — additional cell(s) from a secondary node used in dual connectivity/carrier aggregation, with its own independent MAC entity.
- **Functional split** — the 3GPP-defined boundary (Options 1–8) at which RAN processing is divided between centralized and distributed units; higher option number = more centralized, higher fronthaul demand.
- **CPRI (Common Public Radio Interface)** — the traditional high-bandwidth fronthaul interface used for full centralization (Option 8-style) C-RAN deployments.

---

## Open RAN & O-RAN

- **Open RAN** — the general industry principle that RAN components should communicate via open, standardized interfaces rather than proprietary ones.
- **O-RAN (O-RAN Alliance)** — the specific organization and specification implementing Open RAN principles, defining O-RU/O-DU/O-CU, exact split points, and interfaces.
- **O-RU (O-RAN Radio Unit)** — handles RF functions and low-PHY processing.
- **O-DU (O-RAN Distributed Unit)** — handles high-PHY, MAC, and RLC layers; can serve multiple O-RUs.
- **O-CU (O-RAN Central Unit)** — handles PDCP and RRC/SDAP; split into O-CU-CP and O-CU-UP; can serve multiple O-DUs.
- **O-CU-CP (Control Plane)** — the O-CU component handling RRC and the control-plane part of PDCP.
- **O-CU-UP (User Plane)** — the O-CU component handling SDAP and the user-plane part of PDCP.
- **Open Fronthaul** — the O-RAN interface between O-RU and O-DU, using split 7.2x (a low-layer PHY split).
- **F1 interface** — the O-RAN interface between O-DU and O-CU, using split 2 (the PDCP/RLC boundary).
- **RIC (RAN Intelligent Controller)** — the O-RAN component enabling AI/ML-based network optimization via interfaces like A1 and E2.

---

## TSN — Time-Sensitive Networking

- **TSN (Time-Sensitive Networking)** — a group of IEEE Ethernet standards enabling deterministic, low-latency, and reliable communication over standard Ethernet.
- **Processing delay** — time spent on packet integrity checking, switching, and address lookup at a network device; address lookup introduces jitter.
- **Queuing delay** — delay caused when multiple packets compete for the same egress port simultaneously.
- **Transmission delay** — time required to push a packet's bits onto the link, determined by bandwidth.
- **Propagation delay** — time for a signal to travel across the physical medium, determined by distance.
- **PTP (Precision Time Protocol, IEEE 1588)** — the base protocol for network-wide clock synchronization used by TSN.
- **802.1AS** — the TSN profile of PTP achieving nanosecond-level time synchronization via a master/slave clock hierarchy.
- **802.1Qbv (Time-Aware Shaper, TAS)** — implements TDMA-like scheduled transmission windows ("gates") to protect time-critical traffic.
- **802.1Qbu / 802.3br (Frame Preemption)** — allows an in-progress best-effort frame to be interrupted so a time-critical frame can be sent immediately, minimizing guard-band waste.
- **802.1Qav (Credit-Based Shaper, CBS)** — a traffic shaping mechanism that smooths bursty traffic using accumulated "credits."
- **802.1Qcr (Asynchronous Traffic Shaper, ATS)** — a shaper providing bounded latency for asynchronous (non-scheduled) traffic.
- **802.1Qch (Cyclic Queuing and Forwarding, CQF)** — a simplified scheduling mechanism using fixed time cycles for queuing and forwarding.
- **802.1CB (FRER — Frame Replication and Elimination for Reliability)** — duplicates frames across multiple paths and eliminates duplicates at the receiver to improve reliability.
- **802.1Qca (Path Control and Reservation, PCR)** — enables explicit path control and resource reservation across the network.
- **802.1Qci (Per-Stream Filtering and Policing, PSFP)** — filters and polices individual traffic streams to protect against misbehaving flows.
- **802.1Qat (Stream Reservation Protocol, SRP)** — announces and reserves network resources along a path for a specific traffic stream.
- **802.1Qcc** — an enhanced, centralized-configuration version of the Stream Reservation Protocol.
- **5GS as virtual TSN bridge** — the 3GPP Release 16 concept of treating the 5G System as a single TSN bridge from the perspective of external TSN devices.
- **DS-TT (Device-Side TSN Translator)** — translates between TSN and 5G QoS requirements on the UE side.
- **NW-TT (Network-Side TSN Translator)** — translates between TSN and 5G QoS requirements on the network side.

---

_Use this alongside the concept-map revision sheet — that document shows how these terms connect; this one nails down exactly what each one means if you're asked to define it cold._