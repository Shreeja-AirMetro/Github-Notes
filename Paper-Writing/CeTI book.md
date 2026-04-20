CeTi book structure - NTN

- **What is NTN** - why NTN started, what is NTN , how this is gonna transform the paradigm
- **NTN in 6G** - how sat network came to 5G, Standardization efforts - in terms of architecture
- **NTN for TI** - Why NTN-NR is the best candidate, omnet++ setup with iridium setup
- **Results and Findings -** VERON, LEON - framework and results
- **Future of NTN** - Next steps - on-board processing, in-network computing , handover policies
- **Research contributions to CeTI**
- ICC Paper
- Ref -  Tactile internet
- EU call system
- Related works
- Communication networks. The space room will leverage technological advancements in the CeTI’s Network of Networks (NoN) research room.  First, NoN will cover communication systems connecting space, air, and ground networks in a 3D network. The 3D network offers seamless global connectivity by eliminating coverage dead zones and ensuring ultra-reliable, low-latency communications with high data rates. 

- Through the partnership with Deutsche Telekom, CeTI gains access to terrestrial and satellite connectivity1 , supporting experiments in the Space room. NoN expands this vision by integrating 3D networks, local-area networks (such as time-sensitive networking for deterministic communication), and body-area networks (like data gloves and exoskeletons for multisensory augmentation. Beyond connectivity, NoN will also offer computation at various network domains as cloud computing has been extended into space2 . The available computing resources that NoN offers via its CommercialOff-The-Shelf (COTS) testbed will allow CeTI researchers to implement, deploy, and evaluate innovations, such as joint optimization of handover, offloading, and resource allocation scheme for offloading computation [102] and intelligent scheduling strategies [103] enabled by AI. 

- NoN fosters innovation to support use cases in the Space room through the CeTI Computing and Communication Platform (C3PO) — a fully softwarized environment supporting cross-domain applications. C3PO allows for prototyping solutions in information theory and integrating novel computing platforms to accelerate AI and reduce latency. Additionally, C3PO will enable a fully softwarized 3D network for adaptive, efficient management of these interconnected resources, optimizing latency and reliability across applications in the Space use cases.
-  In section NTN for TI 
- NTN-NR - HAP and LAP 
- Structure: 
1- What NTN means to TI
Use cases - challenges - 
Future NTN addresses these challenges
2- Future part: Demonstrated full potential - open question to meet 
 to address challenges OSI level - 
addressing asymmetric delay
If implemented potential

----

# Planned Journal 
- Target 6G VTC magazine
- Deadline 29th August 
- Paper structure 
- https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10716597

---
https://vtsociety.org/files/ieeevts/2025-04/IEEE%20Future%20Networks%20Special%20Issue%20on%206G.pdf 

Key points about the call: 
- 6G is anticipated to offer a lean network that utilizes intelligence to adapt network topology to support a high quality of experience for connected users. This new technology is set to revolutionize various industries as it will enable the development of innovative applications. 
- Although much is yet to be learned about 6G technology, it is expected it will usher in a new era of connectivity and innovation. For example, 6G will integrate both virtual and physical realities bringing forward new paradigms of data distribution and network operations.
- These networks will expand beyond terrestrial environments, incorporating analytics, energy-efficient mechanisms, and blockchain systems to boost network autonomy and enable self-synthesizing and self-healing operations.

- Articles should be tutorial in nature, and should be written in a style comprehensible to readers outside the specialty of the article. Papers presenting original and state-of-the art research and technical contributions are also considered.
- However, their presentation should be in tutorial or survey style, and should be accessible for all readers. Submissions of highly specialized and detailed technical papers should re-directed to the IEEE Transactions on Vehicular Technology.
-  Option 1: Articles should not exceed 4000 words (Introduction through Conclusions, excluding figures, tables and captions). Title, author affiliations, abstract, references, acknowledgements, and author biographies are also excluded from the word count. Figures and tables should be limited to a combined total of 10 (# figures + # tables ≤ 10).
- Option 2: Articles should not exceed 4500 words (Introduction through Conclusions, excluding figures, tables and captions). Title, author affiliations, abstract, references, acknowledgements, and author biographies are also excluded from the word count. Figures and tables should be limited to a combined total of 8 (# figures + # tables ≤ 8).

- For both options, sub-figures and/or sub-tables are counted as one each. For example, if a paper has 3 tables and 2 figures with 4 sub-figures each (figure x.a, figure x.b, figure x.c and figure x.d), then the total of <FIGURES> + <TABLES> = 11, therefore one sub-figure or table must be removed. Pseudo-code of algorithms is counted as one table.
- The use of mathematical equations must be limited to a maximum of 3. Do not embed equations into the text to include more equations. Embedded equations also count and all equations must be numbered.
- References must be limited to a maximum of 15. Authors’ bios should not exceed 75 words each.


---

# Critical Evaluation of INTANS Paper for IEEE Future Networks Special Issue on 6G

## Executive Summary

The **INTANS (Integrated Network-simulator for Terrestrial And Non-terrestrial Systems)** paper presents a valuable contribution to Non-Terrestrial Network (NTN) simulation, but in its current form, it **does not meet the requirements** for the IEEE Future Networks Special Issue on 6G Technologies and Applications. While the technical work is solid, significant gaps exist that prevent alignment with the special issue's scope and style requirements[1](https://www.ieeevtc.org/vtmagazine/specisu--6G-Tech-App_03.php)[2](https://vtsociety.org/files/ieeevts/2025-04/IEEE%20Future%20Networks%20Special%20Issue%20on%206G.pdf).

3

## Major Gaps and Critical Issues

## **1. Insufficient 6G Integration and Vision**

**Current Status:** The paper focuses primarily on 5G NTN with limited 6G context[4](https://www.mitre.org/sites/default/files/2021-11/pr-21-0214-6g-and-artificial-intelligence-and-machine-learning.pdf)[5](https://paperswithcode.com/paper/overview-of-ai-and-communication-for-6g)[6](https://cris.vtt.fi/en/publications/overview-of-ai-and-communication-for-6g-network-fundamentals-chal).

**Critical Gap:** The paper lacks explicit connection to 6G vision and IMT-2030 framework requirements. Recent 6G research emphasizes:

- Peak data rates up to 200 Gbps (10x improvement over 5G)[7](https://arxiv.org/html/2501.14552v1)
    
- Ultra-low latency (0.1-1 ms)[7](https://arxiv.org/html/2501.14552v1)
    
- Connection density up to 10^8 devices/km²[7](https://arxiv.org/html/2501.14552v1)
    
- Global coverage including space, air, ground, and sea domains[7](https://arxiv.org/html/2501.14552v1)
    

**Recommendation:** Integrate 6G-specific use cases like immersive communication, integrated sensing and communication (ISAC), and AI-native networking[5](https://paperswithcode.com/paper/overview-of-ai-and-communication-for-6g)[8](https://arxiv.org/html/2412.14538v1).

## **2. Missing AI/ML Integration - Critical Deficiency**

**Current Status:** The paper completely lacks AI/ML components, which is a **fundamental requirement** for 6G systems[4](https://www.mitre.org/sites/default/files/2021-11/pr-21-0214-6g-and-artificial-intelligence-and-machine-learning.pdf)[5](https://paperswithcode.com/paper/overview-of-ai-and-communication-for-6g)[9](https://smart-networks.europa.eu/wp-content/uploads/2025/02/ai_ml_white-paper-sns_tb_v1.0.pdf).

**Critical Gap:** All recent 6G literature emphasizes AI as native to 6G networks[10](https://www.everythingrf.com/news/details/20517-wireless-infrastructure-association-explores-the-role-of-ai-native-networks-in-6g). The IEEE Special Issue specifically lists "AI/ML intelligent and autonomous networks" as a core topic[2](https://vtsociety.org/files/ieeevts/2025-04/IEEE%20Future%20Networks%20Special%20Issue%20on%206G.pdf). Key missing elements:

- AI-native network architecture[10](https://www.everythingrf.com/news/details/20517-wireless-infrastructure-association-explores-the-role-of-ai-native-networks-in-6g)
    
- ML-based resource optimization[11](https://www.academia.edu/124276563/Machine_Learning_Empowered_Emerging_Wireless_Networks_in_6G_Recent_Advancements_Challenges_and_Future_Trends)[12](https://www.semanticscholar.org/paper/Machine-Learning-Empowered-Emerging-Wireless-in-6G:-Noman-Hanafi/43086e8cef113d4e56d5be834580dd6326b7ff3b)
    
- Intelligent handover management[13](https://dspace.networks.imdea.org/bitstream/handle/20.500.12761/1522/mobiarch21_daemon_postprint.pdf)
    
- Predictive network analytics[14](https://www.keysight.com/ca/en/assets/3125-1246/application-notes/The-Integration-of-AI-and-6G.pdf)
    

**Recommendation:** Completely redesign the simulator architecture to include AI/ML modules for network intelligence, following the three-stage AI integration: "AI for Network," "Network for AI," and "AI as a Service"[8](https://arxiv.org/html/2412.14538v1)[6](https://cris.vtt.fi/en/publications/overview-of-ai-and-communication-for-6g-network-fundamentals-chal).

## **3. Presentation Style Mismatch**

**Current Status:** Written as a technical conference paper rather than the required tutorial/survey style[2](https://vtsociety.org/files/ieeevts/2025-04/IEEE%20Future%20Networks%20Special%20Issue%20on%206G.pdf).

**Critical Gap:** The IEEE Special Issue requires "state-of-the-art material presented in a tutorial or survey style" that is "accessible for all readers"[2](https://vtsociety.org/files/ieeevts/2025-04/IEEE%20Future%20Networks%20Special%20Issue%20on%206G.pdf). The current paper is too technical and narrow in scope.

**Recommendation:** Restructure as a comprehensive tutorial covering:

- NTN fundamentals for 6G
    
- State-of-the-art simulator comparison
    
- Design principles and implementation guidelines
    
- Future research directions
    

## **4. Limited Technological Scope**

**Current Status:** Focuses only on LEO satellites with basic 3GPP compliance[15](https://omnetpp.org/download-items/OS3.html)[16](https://www.6g-sky.net/assets/images/posts/Performance_Analysis_of_Integrated_5G-NR_TN-NTN.pdf).

**Critical Gap:** Missing key 6G enabling technologies:

- Terahertz communications[7](https://arxiv.org/html/2501.14552v1)[17](https://innovate.ieee.org/innovation-spotlight/machine-learning-wireless-communication-6g/)
    
- Reconfigurable Intelligent Surfaces (RIS)[18](https://riseti.committees.comsoc.org/si-workshop/)
    
- Integrated sensing and communication[19](https://arxiv.org/abs/2507.14856)
    
- Quantum communications[20](https://arxiv.org/pdf/2306.08265.pdf)
    
- Semantic communications[5](https://paperswithcode.com/paper/overview-of-ai-and-communication-for-6g)
    

**Recommendation:** Expand to include multi-tier NTN architecture (LEO/MEO/GEO/UAV) and integrate emerging 6G technologies.

## Comparison with Previous Special Issues

Based on analysis of previous IEEE Future Networks Special Issues[1](https://www.ieeevtc.org/vtmagazine/specisu--6G-Tech-App_03.php)[21](https://www.ieeevtc.org/vtmagazine/specisu--6G-Tech-App_04.php)[22](https://pureportal.strath.ac.uk/files/132841125/David_etal_IEEE_VTM_2021_6G_networks_is_this_an_evolution_or_a.pdf)[23](https://read.nxtbook.com/ieee/vehicular_technology/vehiculartechnology_mar_2023/from_the_editor.html), successful papers typically include:

## **Successful Pattern Analysis:**

1. **Comprehensive surveys** covering multiple aspects of 6G technology
    
2. **Tutorial-style presentation** with extensive background and state-of-the-art review
    
3. **Forward-looking insights** into 6G requirements and challenges
    
4. **AI/ML integration** as a core component
    
5. **Multi-technology coverage** rather than single-tool focus
    

## **INTANS Paper Gaps vs. Successful Papers:**

- Lacks comprehensive survey methodology
    
- Missing tutorial-style educational content
    
- Insufficient coverage of 6G ecosystem
    
- No AI/ML integration
    
- Limited comparative analysis
    

## Specific Recommendations for Suitability

To make the INTANS paper suitable for the IEEE Future Networks Special Issue, the following major revisions are required:

## **1. Restructure as Tutorial-Survey Hybrid**

- **Section 1:** Comprehensive introduction to 6G NTN vision and requirements
    
- **Section 2:** State-of-the-art survey of NTN simulators and tools
    
- **Section 3:** AI/ML integration frameworks for 6G NTN
    
- **Section 4:** INTANS architecture as an exemplar implementation
    
- **Section 5:** Comparative analysis with existing solutions
    
- **Section 6:** Future research directions and open challenges
    

## **2. Integrate AI-Native Architecture**

Add AI/ML components addressing[5](https://paperswithcode.com/paper/overview-of-ai-and-communication-for-6g)[6](https://cris.vtt.fi/en/publications/overview-of-ai-and-communication-for-6g-network-fundamentals-chal)[9](https://smart-networks.europa.eu/wp-content/uploads/2025/02/ai_ml_white-paper-sns_tb_v1.0.pdf):

- **Intelligent resource allocation** using reinforcement learning
    
- **Predictive mobility management** for satellite handovers
    
- **AI-driven network optimization** for dynamic scenarios
    
- **Machine learning-based channel prediction**
    
- **Federated learning** for distributed NTN scenarios
    

## **3. Expand Technological Coverage**

Include 6G-specific technologies:

- **Terahertz band utilization** for satellite links[7](https://arxiv.org/html/2501.14552v1)
    
- **Integrated sensing capabilities** for environment awareness[19](https://arxiv.org/abs/2507.14856)
    
- **Sustainable communication** protocols for energy efficiency[9](https://smart-networks.europa.eu/wp-content/uploads/2025/02/ai_ml_white-paper-sns_tb_v1.0.pdf)
    
- **Quantum-secured communications** for NTN[20](https://arxiv.org/pdf/2306.08265.pdf)
    

## **4. Comprehensive Comparative Analysis**

Develop detailed comparison with:

- **Open-source simulators:** NS-3, StarryNet, OpenSN[24](https://arxiv.org/abs/2502.13704)[25](https://www.usenix.org/system/files/nsdi23-lai-zeqi.pdf)[26](https://arxiv.org/html/2507.03248v1)
    
- **Commercial tools:** STK, MATLAB Satellite Communications Toolbox
    
- **Recent academic simulators:** SNS3, Hypatia[27](https://www.magister.fi/asms-2025-dvb-5gnr-ntn/)[25](https://www.usenix.org/system/files/nsdi23-lai-zeqi.pdf)
    
- **Performance benchmarks** across different scenarios
    

## **5. Tutorial-Style Educational Content**

- **Background tutorials** on 6G NTN fundamentals
    
- **Implementation guidelines** for researchers
    
- **Best practices** for NTN simulation
    
- **Hands-on examples** and case studies
    

## Conclusion

While the INTANS simulator represents solid technical work in NTN simulation, **the paper is not currently suitable** for the IEEE Future Networks Special Issue on 6G Technologies and Applications. The **most critical deficiency is the complete absence of AI/ML integration**, which is fundamental to 6G systems[4](https://www.mitre.org/sites/default/files/2021-11/pr-21-0214-6g-and-artificial-intelligence-and-machine-learning.pdf)[5](https://paperswithcode.com/paper/overview-of-ai-and-communication-for-6g)[9](https://smart-networks.europa.eu/wp-content/uploads/2025/02/ai_ml_white-paper-sns_tb_v1.0.pdf)[10](https://www.everythingrf.com/news/details/20517-wireless-infrastructure-association-explores-the-role-of-ai-native-networks-in-6g).

The paper requires **substantial restructuring** from a technical tool paper to a comprehensive tutorial-survey that covers 6G NTN simulation holistically, integrates AI-native architectures, and provides educational value to the broader research community. Without these major revisions, the paper does not align with the special issue's scope, style requirements, or the broader 6G research vision.

**Recommendation:** Undertake major revision addressing all identified gaps, or consider submission to a more specialized venue focused on simulation tools rather than broad 6G technologies.

1. [https://www.ieeevtc.org/vtmagazine/specisu--6G-Tech-App_03.php](https://www.ieeevtc.org/vtmagazine/specisu--6G-Tech-App_03.php)
2. [https://vtsociety.org/files/ieeevts/2025-04/IEEE%20Future%20Networks%20Special%20Issue%20on%206G.pdf](https://vtsociety.org/files/ieeevts/2025-04/IEEE%20Future%20Networks%20Special%20Issue%20on%206G.pdf)
3. [https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/58228666/f5783423-005b-46af-a956-34a36f816dfe/Extended_INTANS___Integrated_Network_simulator_for_Terrestrial_And_Non_terrestrial_System.pdf](https://ppl-ai-file-upload.s3.amazonaws.com/web/direct-files/attachments/58228666/f5783423-005b-46af-a956-34a36f816dfe/Extended_INTANS___Integrated_Network_simulator_for_Terrestrial_And_Non_terrestrial_System.pdf)
4. [https://www.mitre.org/sites/default/files/2021-11/pr-21-0214-6g-and-artificial-intelligence-and-machine-learning.pdf](https://www.mitre.org/sites/default/files/2021-11/pr-21-0214-6g-and-artificial-intelligence-and-machine-learning.pdf)
5. [https://paperswithcode.com/paper/overview-of-ai-and-communication-for-6g](https://paperswithcode.com/paper/overview-of-ai-and-communication-for-6g)
6. [https://cris.vtt.fi/en/publications/overview-of-ai-and-communication-for-6g-network-fundamentals-chal](https://cris.vtt.fi/en/publications/overview-of-ai-and-communication-for-6g-network-fundamentals-chal)
7. [https://arxiv.org/html/2501.14552v1](https://arxiv.org/html/2501.14552v1)
8. [https://arxiv.org/html/2412.14538v1](https://arxiv.org/html/2412.14538v1)
9. [https://smart-networks.europa.eu/wp-content/uploads/2025/02/ai_ml_white-paper-sns_tb_v1.0.pdf](https://smart-networks.europa.eu/wp-content/uploads/2025/02/ai_ml_white-paper-sns_tb_v1.0.pdf)
10. [https://www.everythingrf.com/news/details/20517-wireless-infrastructure-association-explores-the-role-of-ai-native-networks-in-6g](https://www.everythingrf.com/news/details/20517-wireless-infrastructure-association-explores-the-role-of-ai-native-networks-in-6g)
11. [https://www.academia.edu/124276563/Machine_Learning_Empowered_Emerging_Wireless_Networks_in_6G_Recent_Advancements_Challenges_and_Future_Trends](https://www.academia.edu/124276563/Machine_Learning_Empowered_Emerging_Wireless_Networks_in_6G_Recent_Advancements_Challenges_and_Future_Trends)
12. [https://www.semanticscholar.org/paper/Machine-Learning-Empowered-Emerging-Wireless-in-6G:-Noman-Hanafi/43086e8cef113d4e56d5be834580dd6326b7ff3b](https://www.semanticscholar.org/paper/Machine-Learning-Empowered-Emerging-Wireless-in-6G:-Noman-Hanafi/43086e8cef113d4e56d5be834580dd6326b7ff3b)
13. [https://dspace.networks.imdea.org/bitstream/handle/20.500.12761/1522/mobiarch21_daemon_postprint.pdf](https://dspace.networks.imdea.org/bitstream/handle/20.500.12761/1522/mobiarch21_daemon_postprint.pdf)
14. [https://www.keysight.com/ca/en/assets/3125-1246/application-notes/The-Integration-of-AI-and-6G.pdf](https://www.keysight.com/ca/en/assets/3125-1246/application-notes/The-Integration-of-AI-and-6G.pdf)
15. [https://omnetpp.org/download-items/OS3.html](https://omnetpp.org/download-items/OS3.html)
16. [https://www.6g-sky.net/assets/images/posts/Performance_Analysis_of_Integrated_5G-NR_TN-NTN.pdf](https://www.6g-sky.net/assets/images/posts/Performance_Analysis_of_Integrated_5G-NR_TN-NTN.pdf)
17. [https://innovate.ieee.org/innovation-spotlight/machine-learning-wireless-communication-6g/](https://innovate.ieee.org/innovation-spotlight/machine-learning-wireless-communication-6g/)
18. [https://riseti.committees.comsoc.org/si-workshop/](https://riseti.committees.comsoc.org/si-workshop/)
19. [https://arxiv.org/abs/2507.14856](https://arxiv.org/abs/2507.14856)
20. [https://arxiv.org/pdf/2306.08265.pdf](https://arxiv.org/pdf/2306.08265.pdf)
21. [https://www.ieeevtc.org/vtmagazine/specisu--6G-Tech-App_04.php](https://www.ieeevtc.org/vtmagazine/specisu--6G-Tech-App_04.php)
22. [https://pureportal.strath.ac.uk/files/132841125/David_etal_IEEE_VTM_2021_6G_networks_is_this_an_evolution_or_a.pdf](https://pureportal.strath.ac.uk/files/132841125/David_etal_IEEE_VTM_2021_6G_networks_is_this_an_evolution_or_a.pdf)
23. [https://read.nxtbook.com/ieee/vehicular_technology/vehiculartechnology_mar_2023/from_the_editor.html](https://read.nxtbook.com/ieee/vehicular_technology/vehiculartechnology_mar_2023/from_the_editor.html)
24. [https://arxiv.org/abs/2502.13704](https://arxiv.org/abs/2502.13704)
25. [https://www.usenix.org/system/files/nsdi23-lai-zeqi.pdf](https://www.usenix.org/system/files/nsdi23-lai-zeqi.pdf)
26. [https://arxiv.org/html/2507.03248v1](https://arxiv.org/html/2507.03248v1)
27. [https://www.magister.fi/asms-2025-dvb-5gnr-ntn/](https://www.magister.fi/asms-2025-dvb-5gnr-ntn/)
28. [https://vtsociety.org/files/ieeevts/2025-04/IEEE%20Future%20Networks%20Special%20Issue%20on%206G.pdf](https://vtsociety.org/files/ieeevts/2025-04/IEEE%20Future%20Networks%20Special%20Issue%20on%206G.pdf)
29. [https://vtsociety.org/post/announcement/call-papers-vtm-special-issue-6g-technologies-and-applications](https://vtsociety.org/post/announcement/call-papers-vtm-special-issue-6g-technologies-and-applications)
30. [https://oulurepo.oulu.fi/handle/10024/53587](https://oulurepo.oulu.fi/handle/10024/53587)
31. [https://www.diva-portal.org/smash/get/diva2:1775943/FULLTEXT01.pdf](https://www.diva-portal.org/smash/get/diva2:1775943/FULLTEXT01.pdf)
32. [https://www.dfki.de/en/web/research/projects-and-publications/publication/11471](https://www.dfki.de/en/web/research/projects-and-publications/publication/11471)
33. [https://www.computer.org/digital-library/magazines/ic/cfp-6g-technologies-applications/](https://www.computer.org/digital-library/magazines/ic/cfp-6g-technologies-applications/)
34. [http://liu.diva-portal.org/smash/get/diva2:1485025/FULLTEXT01.pdf](http://liu.diva-portal.org/smash/get/diva2:1485025/FULLTEXT01.pdf)
35. [https://onlinelibrary.wiley.com/doi/10.1002/9781119883111.ch12](https://onlinelibrary.wiley.com/doi/10.1002/9781119883111.ch12)
36. [https://core.ac.uk/download/558943453.pdf](https://core.ac.uk/download/558943453.pdf)
37. [https://proceedingsoftheieee.ieee.org/roadmap-for-6g-wireless-networks/](https://proceedingsoftheieee.ieee.org/roadmap-for-6g-wireless-networks/)
38. [https://www.mdpi.com/journal/futureinternet/special_issues/EJOB091HKU](https://www.mdpi.com/journal/futureinternet/special_issues/EJOB091HKU)
39. [https://vtsociety.org/publication/vtmagazine/past-calls-for-papers](https://vtsociety.org/publication/vtmagazine/past-calls-for-papers)
40. [https://www.wiley-vch.de/de/fachgebiete/ingenieurwesen/shaping-future-6g-networks-978-1-119-76551-6](https://www.wiley-vch.de/de/fachgebiete/ingenieurwesen/shaping-future-6g-networks-978-1-119-76551-6)
41. [https://www.ieeevtc.org/vtmagazine/specisu--6G.php](https://www.ieeevtc.org/vtmagazine/specisu--6G.php)
42. [https://vtsociety.org/files/ieeevts/2025-01/special_issue_CFP_6GTechApp_05.pdf](https://vtsociety.org/files/ieeevts/2025-01/special_issue_CFP_6GTechApp_05.pdf)
43. [https://twitter.com/IEEE_VTS/status/1793938015733137843](https://twitter.com/IEEE_VTS/status/1793938015733137843)
44. [https://www.mdpi.com/journal/futureinternet/special_issues/58IM912Y48](https://www.mdpi.com/journal/futureinternet/special_issues/58IM912Y48)
45. [https://publicacoes.riqual.org/wp-content/uploads/2022/09/troia_xii.pdf](https://publicacoes.riqual.org/wp-content/uploads/2022/09/troia_xii.pdf)
46. [https://www.6gflagship.com/tag/ieee/](https://www.6gflagship.com/tag/ieee/)
47. [https://sci-hub.se/downloads/2020-07-26/03/chowdhury2020.pdf](https://sci-hub.se/downloads/2020-07-26/03/chowdhury2020.pdf)
48. [https://www.academia.edu/98278402/Guest_Editorial_6G_The_Paradigm_for_Future_Wireless_Communications?uc-sb-sw=71544525](https://www.academia.edu/98278402/Guest_Editorial_6G_The_Paradigm_for_Future_Wireless_Communications?uc-sb-sw=71544525)
49. [https://www.ict-ariadne.eu/call-for-paper-ieee-vt-magazine-deadline-1-july-2023/](https://www.ict-ariadne.eu/call-for-paper-ieee-vt-magazine-deadline-1-july-2023/)
50. [https://www.itu.int/dms_pub/itu-s/opb/itujnl/S-ITUJNL-JFETF.V1I1-2020-P09-PDF-E.pdf](https://www.itu.int/dms_pub/itu-s/opb/itujnl/S-ITUJNL-JFETF.V1I1-2020-P09-PDF-E.pdf)
51. [https://arxiv.org/pdf/2102.01420.pdf](https://arxiv.org/pdf/2102.01420.pdf)
52. [https://www.scribd.com/document/470650275/6G](https://www.scribd.com/document/470650275/6G)
53. [https://vtsociety.org/publication/vtmagazine/special-issues](https://vtsociety.org/publication/vtmagazine/special-issues)
54. [https://www.academia.edu/53772884/Defining_6G_Challenges_and_Opportunities_From_the_Guest_Editors_](https://www.academia.edu/53772884/Defining_6G_Challenges_and_Opportunities_From_the_Guest_Editors_)
55. [https://ieee-iotj.org/wp-content/uploads/2020/03/CFP_6G_IoTJ.pdf](https://ieee-iotj.org/wp-content/uploads/2020/03/CFP_6G_IoTJ.pdf)
56. [https://www.ant.uni-bremen.de/sixcms/media.php/102/15080/An%20Open%20Source%20Channel%20Emulator%20for%20Non-Terrestrial%20Networks.pdf](https://www.ant.uni-bremen.de/sixcms/media.php/102/15080/An%20Open%20Source%20Channel%20Emulator%20for%20Non-Terrestrial%20Networks.pdf)
57. [https://ieeevtc.org/vtc2024spring/DATA/PID2024002472.pdf](https://ieeevtc.org/vtc2024spring/DATA/PID2024002472.pdf)
58. [http://ieeevtc.org/vtc2024spring/DATA/PID2024002482.pdf](http://ieeevtc.org/vtc2024spring/DATA/PID2024002482.pdf)
59. [https://omnetpp.org/software/2013/08/14/os3-released.html](https://omnetpp.org/software/2013/08/14/os3-released.html)
60. [https://openresearch.lsbu.ac.uk/download/71d811ed7eff722a0f15d5a95a7db76d3a871efb768b948ea9d042f8314f862e/1063139/Main%20File%20IEEE%20Access.pdf](https://openresearch.lsbu.ac.uk/download/71d811ed7eff722a0f15d5a95a7db76d3a871efb768b948ea9d042f8314f862e/1063139/Main%20File%20IEEE%20Access.pdf)
61. [https://ai4networks.com/files/journals/j-20-8.pdf](https://ai4networks.com/files/journals/j-20-8.pdf)
62. [https://www.semanticscholar.org/paper/System-level-Simulation-and-Performance-Evaluation-Guo-Gao/a9510549d4dd0f4f52e145f392c8bd709eeb3303](https://www.semanticscholar.org/paper/System-level-Simulation-and-Performance-Evaluation-Guo-Gao/a9510549d4dd0f4f52e145f392c8bd709eeb3303)
63. [https://eudl.eu/doi/10.4108/icst.simutools.2013.251580](https://eudl.eu/doi/10.4108/icst.simutools.2013.251580)
64. [https://www.sciencedirect.com/science/article/pii/S2095809925002917](https://www.sciencedirect.com/science/article/pii/S2095809925002917)
65. [https://telematics.poliba.it/wp-content/uploads/publications/2021/WIP__WoWMoM_2021__Satellite_NB_IoT.pdf](https://telematics.poliba.it/wp-content/uploads/publications/2021/WIP__WoWMoM_2021__Satellite_NB_IoT.pdf)
66. [https://thesis.unipd.it/retrieve/b33e2ff2-10b1-42a1-998c-ee1a75b187da/Sandri_Mattia.pdf](https://thesis.unipd.it/retrieve/b33e2ff2-10b1-42a1-998c-ee1a75b187da/Sandri_Mattia.pdf)
67. [https://arxiv.org/html/2410.18301v2](https://arxiv.org/html/2410.18301v2)
68. [https://tetcos.com/ntn.html](https://tetcos.com/ntn.html)
69. [https://www.sciencedirect.com/science/article/pii/S1389128624007904](https://www.sciencedirect.com/science/article/pii/S1389128624007904)
70. [https://www.cse.wustl.edu/~jain/cse574-24/ftp/6greq/index.html](https://www.cse.wustl.edu/~jain/cse574-24/ftp/6greq/index.html)
71. [https://www.mdpi.com/2079-9292/12/15/3306](https://www.mdpi.com/2079-9292/12/15/3306)
72. [https://www.academia.edu/45557861/Artificial_Intelligence_and_Cognitive_Computing_for_6G_Communications_and_Networks_](https://www.academia.edu/45557861/Artificial_Intelligence_and_Cognitive_Computing_for_6G_Communications_and_Networks_)
73. [https://www.academia.edu/120382581/Machine_Learning_in_Beyond_5G_6G_Networks_State_of_the_Art_and_Future_Trends](https://www.academia.edu/120382581/Machine_Learning_in_Beyond_5G_6G_Networks_State_of_the_Art_and_Future_Trends)
74. [https://openreview.net/forum?id=s97GA467St](https://openreview.net/forum?id=s97GA467St)
75. [https://www.sciencedirect.com/science/article/pii/S2666603025000077](https://www.sciencedirect.com/science/article/pii/S2666603025000077)
76. [https://arxiv.org/abs/2412.14538](https://arxiv.org/abs/2412.14538)
77. [https://www.conftool.net/ursi2025/index.php/139-Towards_Trustworthy_AI-Native_Radio_Access_Networks-139.pdf?page=downloadPaper&ismobile=false&filename=139-Towards_Trustworthy_AI-Native_Radio_Access_Networks-139.pdf&form_id=139&form_version=final](https://www.conftool.net/ursi2025/index.php/139-Towards_Trustworthy_AI-Native_Radio_Access_Networks-139.pdf?page=downloadPaper&ismobile=false&filename=139-Towards_Trustworthy_AI-Native_Radio_Access_Networks-139.pdf&form_id=139&form_version=final)