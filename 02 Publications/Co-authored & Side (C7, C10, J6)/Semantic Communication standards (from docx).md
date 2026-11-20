> [!summary] Summary
> Converted Word doc: status of semantic-communication standardisation (3GPP, ITU-T SG13 semantic-aware networking, ETSI) with references.
>
> **Target / goal:** Standards section input for J6.

> Converted from ![[Semantic Communication Current standards and regulation.docx]] (original kept in Attachments).

**Semantic Communication Current standards and regulation**
Semantic communication represents a fundamental paradigm shift from traditional bit-level transmission toward meaning-aware, task-oriented information exchange for 6G networks.
Today, semantic communication is considered as "application requirement" and not a base-line of the 6G network.
Its regulatory or standardization efforts are focused for the following applications
- Integrated Sensing and Communication (ISAC)
- Native AI/ML integration for network optimization
- Immersive communication and extended reality
- Ubiquitous connectivity
- System and operational aspects including CAPEX/OPEX reduction
3GPP focuses primarily on bit-level communication and radio access protocols with limited support for semantic metrics.
ITU have formed a working group SG13 and  ITU-T SG13 has established liaisons with ETSI, ISO, ITU-T SG16, ITU-T SG17, ITU-T SG20, GSMA, W3C, and OMA to coordinate semantic communication standardization efforts.
With the take off of 3GPP 6G technical specifications and ETSI's semantic interoperability standards are expected to converge with the ITU-T semantic aware networking framework. *[Ref 1]*

**ITU-T Study Group 13 - Semantic-Aware Networking (SAN)**
ITU-T SG13, designated as the lead study group on AI/ML for future networks, has been developing comprehensive specifications for semantic-aware networking since 2023:
 ITU-T TR.Reqts-SAN  *[Ref 2]* is an informative technical report that identifies potential requirements for semantic-aware networking (SAN) in future networks including IMT-2020 and beyond.
General Requirements: Eight fundamental capabilities including domain-specific semantic ontology, semantic annotation, semantic interpretation, semantic translation, semantic cognition, semantic rationality discovery, and self-description/auto-correction​
Service-Level Requirements: Support for diverse services, QoS/QoE assurance, interoperability with legacy systems, and cross/intra-domain semantic model adaptation.
Network Operation Requirements: Distributed semantic resource provisioning, semantic capability exposure, intra-network and inter-network operations with standardized semantic annotation formats.​
Data Processing Requirements: Semantic autocorrection, semantic identification and representation, semantic knowledge tracking/updating, and robust security/privacy protection.​

Identified key capabilities
- Cost-effective auto-data processing: Automatic discovery, classification, and annotation of network data
- Enhanced interoperability: Cross-domain and cross-system semantic translation
- Self-learning: Automatic ML model training on semantically-annotated data
- Network resilience: Anomaly detection and disaster recovery
- Self-evolution: Adaptation to unknown and emerging semantics
Based on the above requirements the new architectural framework *[Ref 3]* mentions **Semantic Knowledge Management Function (SKMF): a network-resident orchestration entity that provides the “knowledge plane” for future semantic-aware communications. which in charge of Life-cycle management of three knowledge bases – source (SKB), channel (CKB) and task (TKB) – covering data ingestion, model training/validation, versioning, upgrade and retirement.**

From Ref 3

**ETSI**
ETSI's Industry Specification Group on Experiential Networked Intelligence (ENI) is developing context-aware AI models and edge intelligence alignment mechanisms. In these specifications the key challenges, goal and requirements of semantic aware communication is mentioned.
 **Intent Translation Functional Block:** a Functional Block recommended to be added within the Policy Management Functional Block that takes part in the process of Intent Translation. It performs lexical analysis, syntactic analysis, semantic analysis and augmentation, either parsing or compiling and, optionally, interpretation of the Intent Policy.  This involves planning, orchestration and framework of semantic annotations and discovery in the network (Which often aligned with the requirement of AI when used with network slicing for specific application)
Ref : [https://www.etsi.org/deliver/etsi_gr/ENI/001_099/008/02.01.01_60/gr_ENI008v020101p.pdf](https://www.etsi.org/deliver/etsi_gr/ENI/001_099/008/02.01.01_60/gr_ENI008v020101p.pdf)
[https://www.etsi.org/deliver/etsi_gr/ENI/001_099/051/04.01.01_60/gr_ENI051v040101p.pdf](https://www.etsi.org/deliver/etsi_gr/ENI/001_099/051/04.01.01_60/gr_ENI051v040101p.pdf)
In **ETSI GR ENI 008 - Experiential Networked Intelligence (ENI);InTentAware NetworkAutonomicity(ITANA)** , highlights semantic bus enables normalized policy exchange between functional blocks (Data Ingestion, Knowledge Management, Context Awareness, Situation Awareness, and Model-Driven Engineering), ensuring semantic consistency and supporting ontology-based reasoning for component interactions.Then Abstraction and Cross-vendor integration layer. [https://www.etsi.org/deliver/etsi_gr/ENI/001_099/008/02.01.01_60/gr_ENI008v020101p.pdf](https://www.etsi.org/deliver/etsi_gr/ENI/001_099/008/02.01.01_60/gr_ENI008v020101p.pdf%20)
The other set of applications where sematic aware networking and semantic communication is of focus is smart **machine-2-machine (M2M) communication** while maintaining semantic consistency across heterogeneous systems and vendors. This standardization series called as **Smart ApplicationsREFerence(SAREF) ontology** - foundational effort to establish domain-agnostic semantic interoperability across diverse application sectors. [https://smartautomationmag.com/index.php/editorial/industry-news/etsi-releases-3-new-ontology-specifications-for-smart-cities-industry-4-0-and-smart-agriculture](https://smartautomationmag.com/index.php/editorial/industry-news/etsi-releases-3-new-ontology-specifications-for-smart-cities-industry-4-0-and-smart-agriculture)
- TS 103 264: Mapping Specification requirement - semantic interoperability across IoT domains - [https://www.etsi.org/deliver/etsi_ts/103200_103299/103264/04.01.01_60/ts_103264v040101p.pdf](https://www.etsi.org/deliver/etsi_ts/103200_103299/103264/04.01.01_60/ts_103264v040101p.pdf)
- TS 103 267 : SAREF communication framework specification operationalizes semantic communication by defining standardized mechanisms for semantic data exchange, ensuring that meaning preservation is maintained throughout network transmission rather than merely transmitting raw bits. [https://www.etsi.org/deliver/etsi_ts/103200_103299/103267/02.01.01_60/ts_103267v020101p.pdf](https://www.etsi.org/deliver/etsi_ts/103200_103299/103267/02.01.01_60/ts_103267v020101p.pdf)
- TS 103 780 :  provides practical deployment guidelines for SAREF usage over oneM2M infrastructure, establishing standardized approaches for semantic annotation procedures and semantic discovery mechanisms that enable network entities to autonomously identify and interpret semantic resources. [https://www.etsi.org/deliver/etsi_ts/103700_103799/103780/01.01.01_60/ts_103780v010101p.pdf](https://www.etsi.org/deliver/etsi_ts/103700_103799/103780/01.01.01_60/ts_103780v010101p.pdf)
References
1. Recent 6G RAN Meeting - [https://summit2025.one6g.org/wp-content/uploads/Session-1_Buracchini-Enrico_6G-Roadmap-and-Status-in-3GPP-RAN.pdf](https://summit2025.one6g.org/wp-content/uploads/Session-1_Buracchini-Enrico_6G-Roadmap-and-Status-in-3GPP-RAN.pdf)
2. ITU Documents -  Requirements of semantic-aware networking for future networks - website link:  [https://www.itu.int/itu-t/workprog/wp_item.aspx?isn=18431](https://www.itu.int/itu-t/workprog/wp_item.aspx?isn=18431%20) | publication link:  [https://www.itu.int/dms_pub/itu-t/opb/tut/T-TUT-SEMANTIC.AWARE%20C-2023-PDF-E.pdf](https://www.itu.int/dms_pub/itu-t/opb/tut/T-TUT-SEMANTIC.AWARE%20C-2023-PDF-E.pdf)
 Requirements and reference architecture of semantic-aware networking in future networks - Release 2026 - [https://www.itu.int/itu-t/workprog/wp_item.aspx?isn=19137](https://www.itu.int/itu-t/workprog/wp_item.aspx?isn=19137)
3. Architectural Framework for knowledge-based semantic communications over Public IMT Networks - Yet to be released - ITU Draft [https://www.ietf.org/lib/dt/documents/LIAISON/liaison-2025-09-03-itu-t-sg-13-opsawg-new-technical-reports-itu-t-ystraf-kbsc-architectural-framework-for-knowledge-based-semantic-communication-over-p-attachment-2.pdf](https://www.ietf.org/lib/dt/documents/LIAISON/liaison-2025-09-03-itu-t-sg-13-opsawg-new-technical-reports-itu-t-ystraf-kbsc-architectural-framework-for-knowledge-based-semantic-communication-over-p-attachment-2.pdf%20)
Most  high level data presented above collected from here : ITU -T SG 13 - [https://docbox.etsi.org/Workshop/2025/02_AICONFERENCE/SESSION07/ITU-T%20SG13_CARUGI_MARCO.pdf](https://docbox.etsi.org/Workshop/2025/02_AICONFERENCE/SESSION07/ITU-T%20SG13_CARUGI_MARCO.pdf)

Extra
 SG16 - Multimedia and related digital technologies - [https://www.itu.int/en/ITU-T/studygroups/2022-2024/16/Pages/default.aspx](https://www.itu.int/en/ITU-T/studygroups/2022-2024/16/Pages/default.aspx)
SG 16 also connected to SG21 -  Technologies for multimedia, content delivery and cable television

Key information in Ref 2
Recent developments of communication and networking technologies have witnessed a growing
interest on services such as Tactile Internet and virtual reality (VR)/augmented reality (AR)/extended
reality (XR), most of which are data-hungry and can constantly generate a huge volume of data at a
tremendous speed. There is a pressing need to develop novel cost-effective solutions to support
automatic data analysing, processing, and learning for future networks including IMT-2020.
 Semantic-aware networking (SAN) is an important solution to meet the above need and support
diverse smart applications and services based on the network user/device generated data. The key
idea is to adopt machine and human-shared semantic terms and syntax to represent, annotate, analyse, and interpret data and services in the network. SAN seamlessly converges the networking, artificial intelligence and human user-oriented services, and has the potential to enable new features and capabilities in the future networks. In particular, SAN has the potential to enable the following novel features and capabilities:
- Cost-effective auto-data processing/pre-processing: SAN allows the data generated by UEs and services to be automatically discovered, classified, and/or associated with common semantic annotations for easy analysing and processing.
- Enhanced interoperability: based on SAN, the data and services associated with different sources, applications, networks, and systems can be automatically interpreted and converted into the same semantic domain which enables improved data and service interoperation between different application, network and system domains.
- Self-learning and inferencing: in SAN, both the network and/or user UE can utilize semantic- annotated data arrived at the network and/or received by the user equipment to automatically train suitable ML models. The network and/or UE can also infer possible (causal or logical) relations between different semantic annotations as well as syntax in different network systems and protocols.
- Self-evolving and adapting: SAN allows network and UE to identify unrecognizable and/or
 unknown semantics and automatically infer the possible relations between the unknown data
 combination, patterns, and behavior with existing semantics.
 - Network abnormal/disaster discovery and recovery: in SAN, the network is able to identify unusual data traffic patterns, relations, syntax, and rules and can therefore support automatic discover and alarm of network abnormality and disaster. SAN also allows network operators to automatically correct the abnormal data traffic or routing paths based on the pre-identified or pre-trained rules.

**Regulation and Standardization on Trustworthiness**
**ITU-T Trustworthiness Framework**
*Got* *primary* *information from here:* [*https://paul-harvey.org/tag/itu-t/*](https://paul-harvey.org/tag/itu-t/)
ITU-T Y.3051([https://www.itu.int/dms_pub/itu-t/opb/tut/T-TUT-TRUST-2017-PDF-E.pdf](https://www.itu.int/dms_pub/itu-t/opb/tut/T-TUT-TRUST-2017-PDF-E.pdf) ): "The basic principles of trusted environment in ICT infrastructure" – Provides the definition, common requirements, and basic principles for creating trusted environments in ICT infrastructure Key entities who manages the trust here are trust platform  and Access Control Policy and Mapping manager that enforces policies and rules
Interesting resource ITU-T Y.3052 [https://www.itu.int/rec/T-REC-Y.3052-201703-I/en](https://www.itu.int/rec/T-REC-Y.3052-201703-I/en) : "Overview of trust provisioning for information and communication technology infrastructures and services" – Introduces trust relationships, trust evaluation models, and trust provisioning concepts. Defines trustworthiness attributes across three major factors: ability, integrity, and benevolence.

This is further classified and defined of direct and indirect trust. The definition of the attributes are in **Table II.1 – Trustworthiness attributes– Pg:17 Appendix II**

The trustworthiness has a main group for autonomous networks and one of mainstream focus from ITU-2020 (as it is foundation for IoT, AI and other applications) [https://www.itu.int/en/ITU-T/focusgroups/an/Documents/Trustworthiness_AN.pdf](https://www.itu.int/en/ITU-T/focusgroups/an/Documents/Trustworthiness_AN.pdf)
The next stage  ITU-T Y.3062 (approved February 2025) specifies trustworthiness evaluation specifically for IMT-2020 and beyond with autonomous network (AN) functions.

**ETSI**
ETSI has developed comprehensive trustworthiness standards for Trust Service Providers (TSPs):
EN 319 401: General policy requirements for Trust Service Providers covering risk assessment, security requirements, and trust service practice statements
[https://www.etsi.org/deliver/etsi_en/319400_319499/319401/03.01.01_60/en_319401v030101p.pdf](https://www.etsi.org/deliver/etsi_en/319400_319499/319401/03.01.01_60/en_319401v030101p.pdf)
EN 319 403: Part 2 of above document - Conformity assessment requirements for bodies assessing Trust Service Providers (Tbh I don’t find it very relevant to us)
[https://cabforum.org/uploads/ts_11940302v010201p.pdf](https://cabforum.org/uploads/ts_11940302v010201p.pdf)
EN 319 411-1 and 311-2: Policy and security requirements for TSPs issuing certificates, including EU qualified certificates (high level from administrative orchestration perspective)
- 411: [https://cabforum.org/uploads/en_31941101v010202p.pdf](https://cabforum.org/uploads/en_31941101v010202p.pdf)
- 311 : [https://cabforum.org/uploads/en_31941102v020202p.pdf](https://cabforum.org/uploads/en_31941102v020202p.pdf)
There are rest of resources from ETSI focusing on IoT and data security and its associated trustworthiness.

**3GPP**
Within the 3GPP Technical Specification Group Service and System Aspects (TSG SA), the main objectives of 3GPP TSG SA WG3 (SA3) includes defining the requirements and specifying the architectures and protocols for security and privacy in 3GPP systems. [https://www.3gpp.org/3gpp-groups/service-system-aspects-sa/sa-wg3](https://www.3gpp.org/3gpp-groups/service-system-aspects-sa/sa-wg3)
Another interesting part is SA5 – Management, pricing/charging and orchestration

From Industry - [https://www.ngmn.org/wp-content/uploads/NGMN_6G_Trustworthiness.pdf](https://www.ngmn.org/wp-content/uploads/NGMN_6G_Trustworthiness.pdf)
The industry proposes multi-layered trust framework. Some highlights from the above reference.
- Decentralized Trust Foundation: Using distributed ledger technology to address network topology evolution and diverse business models
- Dynamic Trust Models: Evolution from traditional two-way trust (UE-operator) to three-way trust (access devices, industry users, operators) and multi-party trust models for flexible connection modes and MEC deployments.
- Intelligent collaboration: Integrates AI-driven intelligent analysis and coordination mechanisms across distributed security functions to overcome the limitations of signature-based threat detection and enable identification of zero-day attacks (Advanced Persistent Threats)
- Security as Service: Constructs a dynamic resource pool where all security functions are organized and provisioned based on real-time network requirements, supporting atomic-level customization and efficient security implementation
- Trust and risk assessment: Implements multi-dimensional network situation awareness combined with technical proof mechanisms (metrics, KPIs) to continuously measure trust levels, perceive network status, and assess security risks which can enable timely security strategy updates

Note: I didn’t find any 3GPP document on Zero Trust Architecture enabled by 3GPP security – Only Blog posts by company (as a part of security enhancements in Rel 18).
