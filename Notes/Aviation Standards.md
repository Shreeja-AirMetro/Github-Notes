 Standards & Regulations for ATN IPS in AAM

1.1 ICAO Standards (Global)

ATN IPS is standardized by the International Civil Aviation Organization (ICAO) in:

ICAO Doc 9896 – Technical provisions for ATN IPS (IPv6-based communications)
ICAO Annex 10, Volume III – Communication systems and performance requirements
ICAO Doc 10039 – Global Air Navigation Plan (GANP), including future ATM system improvements
ICAO Doc 9750 – Required Communications Performance (RCP) framework

1.2 FAA & EUROCONTROL Standards (Regional)

FAA NextGen – The U.S. framework for integrating AAM into national airspace (leverages ATN IPS)
EU SESAR (Single European Sky ATM Research) – Uses ATN IPS for future ATM systems
RTCA DO-377A & DO-362A – Standards for IP-based command & control (C2) links for unmanned systems
EUROCAE ED-243 – Security for UAS command and control

1.3 Industry and Cybersecurity Standards

RTCA DO-326A / EUROCAE ED-202A – Aviation cybersecurity standards
IETF RFC 8200 – IPv6 protocol standard for ATN IPS
IEEE 802.11 & 5G/6G – Wireless networking standards relevant to AAM


2. ATN IPS Implementation for AAM

ATN IPS enables secure, real-time, and scalable communication across AAM networks by integrating:

IPv6 Networking – Enables global addressing and improved mobility support for AAM aircraft.
Secure Communication – Uses TLS 1.3, IPsec, and VPNs for encrypted data transfer.
Dynamic Routing (BGP, OSPF, or NEMO) – Ensures reliable air-to-ground and inter-aircraft connectivity.
Edge Computing & Cloud Integration – Supports U-space and UTM (Unmanned Traffic Management) services.
AI-driven Traffic Management – Uses real-time AI models for collision avoidance and air traffic flow optimization.

----

Yes — there **has been activity and formal structures working on related topics in both 3GPP and ICAO**, but it’s important to clarify the **nature of that collaboration**:

---

## ✅ 1. **ICAO Has Established Aviation-Focused Working Groups**

**ICAO does have formal working/advisory groups** that address aviation communications and unmanned systems:

- **Unmanned Aircraft Systems Advisory Group (UAS-AG)** was established to support ICAO in developing guidance and provisions for UAS integration into the airspace. ([ICAO](https://www.icao.int/safety/UA/Pages/Unmanned-Aircraft-Systems-Advisory-Group-%28UAS-AG%29.aspx?utm_source=chatgpt.com "Unmanned Aircraft Systems Advisory Group (UAS-AG)"))
    
- **Communications Panel-Data Communications Infrastructure Working Group (CP-DCIWG)** operates under ICAO’s Communications Panel and is actively advancing aviation communication infrastructure, including hybrid networks that could leverage commercial broadband (e.g., 5G and satellite). ([LinkedIn](https://www.linkedin.com/posts/icao_the-icao-communication-panels-data-communications-activity-7406377527910219776-W6uq?utm_source=chatgpt.com "ICAO CP-DCIWG Advances Hybrid Communication Network and VoIP Solutions | International Civil Aviation Organization posted on the topic | LinkedIn"))
    

→ These groups **are official ICAO bodies** that can interact with outside standards organizations like 3GPP in a liaison/consultative role, but they are _ICAO’s own working structures_ rather than formal ICAO–3GPP joint working groups.

---

## ✅ 2. **3GPP Has Active Working Groups Addressing UAS/Drone Communications**

Within 3GPP itself, there are **internal working items and workgroups** addressing **cellular support for UAVs/UAS**, including:

- Studies and specifications related to UAV connectivity, identification, tracking, quality of service, and network support in various releases (e.g., Release 17, Release 18). ([3GPP](https://www.3gpp.org/technologies/nr-uav?utm_source=chatgpt.com "NR Support for UAVs"))
    
- Work in core network and terminal groups for UAS network functions and APIs (e.g., TS 29.255, TS 29.256). ([3GPP](https://www.3gpp.org/technologies/tsg-ct-work-on-uas-connectivity-identification-and-tracking?utm_source=chatgpt.com "TSG CT work on UAS Connectivity, Identification and Tracking"))
    

These are **standardization activities within 3GPP**, not joint groups with ICAO — but they _reflect 3GPP’s response to aviation needs_.

---

## ❓ 3. **Is There a Formal Joint ICAO–3GPP Working Group?**

- There is **no widely publicized, dedicated “joint working group” labeled specifically as a formal ICAO-3GPP team** that sits independently and alone to co-develop standards.
    
    - Most technical communication between the two comes through **liaison statements, information exchanges, and participation in relevant events** as part of ICAO panels and 3GPP’s liaison mechanisms, rather than a permanent co-owned working group like you’d see inside a single organization. ([3GPP](https://www.3gpp.org/about-us/liaisons-statements?utm_source=chatgpt.com "Liaisons Statements - 3GPP"))
        
- **Formal collaboration often happens indirectly or through other forums**, such as:
    
    - **ITU** (International Telecommunication Union) where both telecom standards and aviation spectrum/coexistence issues are discussed.
        
    - **Industry alliances and consortia** (like Seamless Air Alliance) that include representatives from aviation and 3GPP ecosystem players working on integration. ([Military Aerospace](https://www.militaryaerospace.com/communications/article/14305811/seamless-air-alliance-works-to-integrate-3gpp-5g-satellite-networks-into-aviation-sector?utm_source=chatgpt.com "Seamless Air Alliance works to integrate 3GPP 5G satellite networks into aviation sector | Military Aerospace"))
        

---

## 🔎 4. **Current Status Summary**

**✔ ICAO working groups exist** that tackle aviation communications (e.g., UAS-AG, CP-DCIWG). ([ICAO](https://www.icao.int/safety/UA/Pages/Unmanned-Aircraft-Systems-Advisory-Group-%28UAS-AG%29.aspx?utm_source=chatgpt.com "Unmanned Aircraft Systems Advisory Group (UAS-AG)"))  
**✔ 3GPP has working groups and studies on cellular support for UAVs/UAS.** ([3GPP](https://www.3gpp.org/technologies/nr-uav?utm_source=chatgpt.com "NR Support for UAVs"))  
**✔ There is no single, formal “ICAO-3GPP working group” listed publicly; collaboration primarily occurs via liaison processes and informal/industry engagements**, not co-chaired dual-organization task forces. ([3GPP](https://www.3gpp.org/about-us/liaisons-statements?utm_source=chatgpt.com "Liaisons Statements - 3GPP"))

---

## ⚙ How Collaboration Works in Practice

Instead of establishing a standalone ICAO-3GPP WG:

1. **ICAO panels request input or send liaison statements** to groups like 3GPP (and vice versa) through formal liaison mechanisms. ([3GPP](https://www.3gpp.org/about-us/liaisons-statements?utm_source=chatgpt.com "Liaisons Statements - 3GPP"))
    
2. **3GPP participants (industry and partners) contribute requirements** tied to aviation safety and unmanned systems.
    
3. **Third parties and alliances** sometimes bridge both sides to accelerate harmonization (e.g., Seamless Air Alliance). ([Military Aerospace](https://www.militaryaerospace.com/communications/article/14305811/seamless-air-alliance-works-to-integrate-3gpp-5g-satellite-networks-into-aviation-sector?utm_source=chatgpt.com "Seamless Air Alliance works to integrate 3GPP 5G satellite networks into aviation sector | Military Aerospace"))
    

---

