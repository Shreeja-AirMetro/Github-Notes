
### Key words from the translated Proposal 
- these future networks will focus not
only on data transport, but also on the storage and calculation of information. These changes
open up relevant potential for UAS equipped with communication and computing technologies,
- Cooperative communication, between mobile nodes as well as intended for AAM, has been a
field of research in its own right for years [FI114] with novel information theories of network
coding, in which the ComNets chair of PI Fitzek is a world leader. Network coding allows the
simultaneous optimization of latency and resilience, whereby the state of the art so far only
allows the trade-off of latency for resilience.
- V2V and D2D currently still have
shortcomings (in particular jitter, which can lead to irregular delays in the transmission of data
packets).
- plan and evaluate an intelligent, fail-safe, low-latency and secure (security)
communication network in the context of the 5G software stack in the 5G campus network and
at European level (in cooperation with the 5G Opera project [218]), which will be set up by UAS.
- LOL!!!! - Quantum security in the network, dialectical approaches with their own protocols or post-Shannon approaches are also being investigated, which may be more suitable against jamming attacks
- The connection of flying devices to stationary communication networks (gateway), and
thus to the Internet, is also a research topic. In addition, AI-supported procedures are being
developed that can react efficiently to dynamic changes in the communication topology.
- Network tests and flight tests will take place in the physical environment of the SML.

Pg 10 
UAS navigation and communication
The 5G mobile communications standard will play a key role in the communication and
interaction of unmanned aerial systems (UAS = UAV, control and communication station) in
urban areas as a central criterion for safety-critical applications, as it offers higher data
transmission speeds, lower latency times and higher availability [108] as well as significantly
increased data integrity through redundancy. With these improvements, UAVs should be able to
communicate, control and monitor more efficiently [109, 110]. Subsequently, 5G can also
significantly improve the transmission of data for entertainment and information purposes on
board air cabs. Such highly scalable mobility applications show a widespread distribution of aircraft, which poses particular challenges for the design of the
communication network: For this purpose, cloud edge computing in combination with 5G can
bring data processing and decision-making closer to end devices and at the same time enable
the transmission of large amounts of data over the network [111]. The meshing of the network
(interconnectivity of nodes, so-called mesh) supports this process by allowing data to be
transmitted not only via a central router, but via several (redundant) paths between nodes. In
addition to distributed processing, this primarily serves the aforementioned robustness
(redundancy of data forwarding via multiple paths), expandability (no network reconfiguration
when adding additional nodes) and increased coverage. A mesh network is therefore suitable
as a flexible and robust solution for setting up a communication network, especially in scenarios
such as AAM [112], where high availability and coverage are required [113]. PI Fitzek is
conducting research in this area on previously ground-based devices [FI114], for cooperative
work in the network [FI115, FI116, FI117] and for transfer to aviation and UAS [FI118, FI119,
FI120]. Several individual or combined methods are available for the real-time navigation of
UAVs:
a) Global Navigation Satellite Systems (GNSS), which are globally available when coupled with
Differential Global Positioning System (DGPS) or Real-Time Kinematic (RTK, improvement of
the position by correction signal) and allow accuracies of a few centimeters, but whose use in
urban areas is impaired by signal shadowing.
b) Inertial Navigation Systems (INS): On-board autonomous positioning based on acceleration
measurement principles with high temporal resolution and short-term accuracy. Due to error
propagation, however, they are less suitable as a stand-alone system and are combined with
GNSS for high accuracy and reliability requirements.
c) 5G: The analysis of signal propagation times in mobile networks also allows position
determination with an accuracy in the sub-meter range. Here, too, there is a loss of accuracy in
urban areas due to signal shadowing and reflections [121].
d) Landmarks: Objects recognizable in the image can serve as control points in
photogrammetric bundle block adjustment methods and thus allow image-based, centimetre-
accurate navigation. The method places high demands on the recognition of landmarks and
real-time processing in photogrammetric aerotriangulation methods.
UAS provide a flexible basis for a wide range of geodata acquisition tasks using cameras or
laser scanners. For the evaluation of UAS image data to generate three-dimensional terrain or
object representations, process chains based on structure-from-motion methods in particular
have become established [EL122, 123]. UAV navigation is not the main focus of such tasks,
since exact orientation parameters are determined a poste- riori in the course of bundle block
adjustment anyway (cf. e.g. [124]). One approach to image-based orientation with 3D city
models is the co-registration of image information and 3D point clouds [MA125]. For this
purpose, the point clouds must be filtered and classified so that only relevant features are
retained for mapping with landmarks. To classify the point clouds, manually created features
(labels) can be used in combination with classifiers from machine learning [126] or continuously
learned convolutional networks [126].
[127] can be used. Elias et al [MA128] determine a co-registration of synthetic images from 3D
models, whereby there is a high requirement for image feature point recognition due to different
radiometric properties. Progress in the field of deep learning-based image classification appears
promising [129, 130]. Although the strategic flight planning takes place before take-off and is
therefore initially not time-critical, for safety reasons it is necessary to update the flight plan data
tactically during the flight, e.g. due to structural changes or temporary objects, which are
extracted in real time from the sensor data (camera, possibly also acoustic sensors at close
range). Object classification methods can be used to detect changes. For example, [131]
presents a procedure that uses machine learning methods to classify small objects in urban and
rural scenes. However, they also emphasize the difficulty of missing training data sets for
changes in street environments. Changes in the terrain caused by UAS were recorded in [EL132,
EL133, EL134] (UAV image stabilization [EL135], elevation models [MA136]). A variety of
algorithms exist for the detection of objects [MA137, EL138] or pedestrians in images, which
can be used in


page 15 - 16
Beyond this terrestrial network routing, both communication, navigation and surveillance (CNS)
procedures between aircraft and ground-based surveillance units (air traffic control) have so far
been based on point-to-point data connections and must therefore reliably master the dynamic,
quasi-optical properties of the atmosphere and local topography (including building reflections).
This can only be achieved by fusing different sensors in combination with AI processes and
geovisualization techniques, which is addressed by means of SLAM and multimodal
adaptive navigation (topics 5, 8, sub-area B) in relation to LiDAR video sensors, 5G/6G and
object geometries (landmarks) for drones and verified experimentally in flight tests. This also
includes the integration of geodetic concepts of blur-based and geometric modeling to handle
spatio-temporally variable data quality in navigation tasks. The SML, which is currently being
implemented, is used for experimental research and validation.
dynamic and local emission effects. Topic 6, sub-area A, deals with the determination and
modeling of robust trajectories, taking into account the uncertainty of the system and thus the
reliable traffic forecast as a basis for safe traffic monitoring. Only by including the uncertainty
can practice-relevant, robust statements be obtained. The central source of uncertainty of the
complex microclimatic environmental conditions in urban areas is addressed in topic 7, also
sub-area A, by means of wind and turbulence simulations, among other things. This traffic
conglomerate requires - currently unavailable - robust, fault-tolerant methods from the fields of
flight mechanics, safety modeling, operations research, communications engineering, computer
science, geosensorics, photogrammetry, economics and urban/airfield planning as well as
atmospheric physics. It must be possible to transmit the required traffic data at high frequency
and in real time during the mission. As a result, there are high requirements for robust and
real-time capable communication between the aircraft and the control station in terms of
availability and bandwidth. As they operate at low altitudes and are spatially centered, cell-
based data link technology (e.g. Long Term Evolution (LTE), 5G/6G mobile radio standards)
is a candidate for improving the current data link (UWB, VDL Mode 2, SSR Mode S) for
combined communication and sensing, in addition to smart grid technology installed in
infrastructure (topic 2). In addition to the SML, DLR is providing public 5G infrastructure for
research purposes via the 5G Real Lab project. Topic 9 investigates the possibilities of cell-
based radio networks (5G, IEEE802.11p) for conflict prevention and navigation of individual
aircraft and groups.


References:

1. P. Fritzson, "Modelica 4 A cyber-physical modeling language and the OpenModelica
environment,= in 2011 7th International Wireless Communications and Mobile
Compu- ting Conference, (IWCMC 2011), Istanbul, Turkey, 2011, pp. 1648-1653, doi:
10.1109/IWCMC.2011.5982782.
2. Z. Ullah, F. Al-Turjman, and L. Mostarda, "Cognition in UAV-Aided 5G and Beyond
Communications: A Survey,= IEEE Trans. Cogn. Commun. Netw., vol. 6, no. 3, pp.
872- 891, 2020, doi: 10.1109/tccn.2020.2968311.
3. M. Rimjha and A. Trani, "Urban Air Mobility: Factors Affecting Vertiport Capacity,=
in 2021 Integrated Communications Navigation and Surveillance Conference
(ICNS), 2021, pp. 1-14, doi: 10.1109/ICNS52807.2021.9441631.
4. [FI114] F. Gabriel, J. Acevedo, and F. H. P. Fitzek, "Network Coding on Wireless Multipath for
Tactile Internet with Latency and Resilience Requirements,= in 2018 IEEE Global
Communications Conference (GLOBECOM): Proceedings : Abu Dhabi, UAE, 9-13
De- cember 2018, Abu Dhabi, United Arab Emirates, 2018, pp. 1-6, doi: 10.1109/GLO-
COM.2018.8647368.
5. [FI115] F. Dressler, C. F. Chiasserini, F. H. P. Fitzek, H. Karl, R. Lo Cigno, and A. Capone et
al, "V-Edge: Virtual Edge Computing as an Enabler for Novel Microservices and Co-
operative Computing,= IEEE Network, 2022, doi: 10.1109/MNET.001.2100491.
6. [FI116]M. Mehrabi, S. Shen, Y. Hai, V. Latzko, G. Koudouridis, and X. Gelabert et al, "Mobil-
ity- and Energy-Aware Cooperative Edge Offloading for Dependent Computation
Tasks,= Network, vol. 1, no. 2, pp. 191-214, 2021. doi: 10.3390/network1020012.
 7. [FI117]R. Torre, I. Leyva-Mayorga, S. Pandi, H. Salah, G. T. Nguyen, and F. H. P. Fitzek,
"Im- plementation of Network-Coded Cooperation for Energy Efficient Content
Distribution in 5G Mobile Small Cells,= IEEE Access, vol. 8, pp. 185964-185980,
2020, doi: 10.1109/ACCESS.2020.3029601.
8. [FI118]F. Granelli, C. Costa, J. Zhang, R. Bassoli, and F. H. P. Fitzek, "Design of an On-
De- mand Agile 5G Multi-Access Edge Computing Platform Using Aerial Vehicles,=
IEEE Communications Standards Magazine, vol. 4, no. 4, pp. 34-41, 2020, doi:
10.1109/MCOMSTD.001.2000016.
9. [FI119]S. Hofmann, V. Megas, M. Ozger, D. Schupke, F. H. P. Fitzek, and C. Cavdar, "Com-
bined Optimal Topology Formation and Rate Allocation for Aircraft to Aircraft Commu-
nications,= in 2019 IEEE International Conference on Communications (ICC):
Proceed- ings : Shanghai, China, May 20-24, 2019, Shanghai, China, 2019, pp. 1-6,
doi: 10.1109/ICC.2019.8761882.
 10. [FI120]S. Pandi, F. Gabriel, O. Zhdanenko, S. Wunderlich, and F. H. P. Fitzek, "MESHMER-
IZE: An Interactive Demo of Resilient Mesh Networks in Drones,= in CCNC 2019:
2019 16th IEEE Annual Consumer Communications & Networking Conference
(CCNC): January 11- 14, 2019 in Las Vegas

- [ ] 




----

### Chapters 

### Introduction 
- AAM 
- Communication in AAM 
- Advent of NTN and drones 
- what communication is expected to do and where are we now 

### Background 
- Regulation the unmet marriage between 3GPP and Drone regulatory side 

### Research parts
- Technology wise 
- Entity wise parts 
- Communication channel and its goal 

### Results and discussions 

### Conclusion future work 

### Appendix 
- Hardware purchase and initial setup 

### Notes
 ![[phD.pdf]]

Treat PhD as own project 
- A **central aim** (main research question or hypothesis)
- **Objectives** (what you must achieve to answer that question)
- **Work Packages (WPs)** (logical groups of tasks that deliver specific outputs)
- A **timeline** (what happens when)
- **Deliverables** (papers, datasets, models, chapters, etc.)

###  work packages and Gantt chart 

To dos:
We are doing this from monograph and publication perspective and to help with 

- [x] Research content and gap 
- [ ] Literature and clear Research hypothesis and questions 
- [x]  Exact To dos and avoid distractions 
- [ ] Classification on type of workloads - Read, write, Implement , Debug and testing, verification, data collection, validation and result preparation
- [x] create a Gantt chart 


---
Chapter ideas for Dissertation 

1. Introduction
2. Communication technology 
	1. 5G 
	2. Satcom
	3. Wi-Fi
	4. Long range traditional aviation communication 
	5. NTN 
3. Data to send and Link | Link Architecture
	1. Network and Protocols  (see how to adapt)
		1. Air to Air 
		2. Air to Ground
	2. Command and control | Critical comm
		1. Telem 
		2. Multi-Modal Nav 
		3. Emergency message 
	3. Payload and non-critical communication
	4.  CNS Cluster - Comm in Nav and Surveillance 
	5. UTM - Edge and data mesh 

5. Link quality and resource aware networks
	2. Physical and RIS
	3. Logical 
		1. Network coding 
		2. Resource aware - link Telemetry monitoring 

6. Application and setup of Multi-link commercial applications 
	 What combination of Multi-link for what scenario 
7. NTN air segment - Drones for Communication
8. Regulation - 3GPP, ETSI, EASA and IEEE standards 
9. Discussion and Conclusion 


---
How to write better 

Never use a metaphor simile or other figure of speech which you are used to seeing in print 
No use a long word when short one would do 
If it is possible to cut word out - cut it out. Dont write long sentences with clauses, sub-clauses 
Never use the passive where you can use the active 
writing is to communicate
Hellen sword book about writing 
George orwell why I write 

--- 

Find origin within that area

Job market needs for skills and demands 

- Lit review - don't just put he said this and he said that (its private notes)
- Specif topic - synthesis to convergence point of convergence and divergence 
- divergence, contradict each other 
- Look for divergence 
- contradictions
- convergence
- omissions


create lit synthesis matrics

Lit synthesis - start with books and survey papers then go down of each problem


---
Defense presentation 
https://www.youtube.com/watch?v=gCL66xH9B_o

Grade often decided on the thesis  - PUT EFFORT ON THESIS
- SUBSTANCE OVER FORM 
- RED THREAD COHERENCE - does everything connect logically 
- DONT SHOW CHARISMATIC - STICK to be profession 
- https://www.youtube.com/watch?v=dv3Bo5jJhWM 
- https://www.youtube.com/watch?v=edQv9OKvfdU



---

Internal and external validity  - in design and methodology 
start thinking about validity and limitation from the beginning

work doesn't happen in a vaccumm

what is done, what hasn't been done - DEVELOP THE GAP IN THE LITERATURE 


Ideal Pages count 
 Intro 15-20
Literature 40-50
Methods - 15-20 
Results 20-40 pages 
discussion - 15-20 

Fully answering RQ


---

Rushing takes longer

Dissertation outline is the blue print 

Prospectus - 10 page plan 
outline shows requirements 

What is outline ? 
1. Know the rules and then start 
2. Rubric and outline provided by insitute 
3. Start with your title - beginning of the journey - Reflect problem, gap, clarity 
4. Chapters  - proposal - first 3 chapter 
5. Intro - background, problem , purpose statement, RQs, Conceptual or theoritical framework, nature of study, key terms , limitations and delimitations and summary 
6. Lit review -  restate problem and purpose as short introduction, desribe your lit stratergy, exploration of conceptual or theoritical framework, supporting literature, identify the gaps and your study fill - summary and way to next chapter
7. Methodology - restate problem and purpose - copy the RQ with same wordings - describe yopur research design - quantitative and qualitative - sampling and population - instruments - data analysis plan , assumptions, scope and limitation , if any ethical consideration, summary and blick to next 

FIRST THREE CHAPTERS IS LIKE CONTRACT 

AFTER RESULTS 
1. repeat rq , process (whatI did as what is mentioned in methodology chapter ), data analysis,results (use table format and present findings clearly), summary
2. Intrepretation  - INTEGRATE WITH THE TIME  _ HOW MY  WORK add knowledge to progress the goal , interpretation and implication , Limitation of my study and recommendation of future study 
3. conclusion and scope of work  and summary 

THEN CHECK  - logic and flow of chapters 
Chap 1-3 also in past tense

Verify that the end answered the problem stated before 





---
conclusion - problems - regulatory level - comm SLA  and involvement of telecom, Industry suppliers and Academics (bottom to top  approach)

global coordination 


---

Did you do the study actually right ?

DON'T IGNORE THE VALIDITY 
INTERNAL AND EXTERNAL VALIDITY 
- do it right and transferable 
- Validity - how well your results reflect the reality 
- Internal - is the set up properly - committee are okay
- external - what my results mean to outside world 
- Internal - variables and its variation , conclusion matches the sample 
- Sample considered impact external validity 
- Internal validiy = cause and effect
- External validity = tranferability
- avoid selection bais
- answer the question 
- Do the results matter ? - results are results - replication 
- G power tests - for sample size - random sampling 
- No study is perfect - control as much the design - grounding and justifiable 
- Every study has limitations - state them verbatum -
- discuss the validity in methods itself 


--- Write a paper  - For UAVs, Of UAVs, By UAVs - communication network perspective  - end of 2026

---
https://www.youtube.com/watch?v=owtUJm4EhoE

- Dissertation is based on data 
- research create new knowledge 
- data collection depends on the methods
- Methods are based on problem - Quantitative - based on numbers - statistical significance 
- Qualitative - people's perceptions 
- Mixed method - Qual + Quant 
- methods must answer RQ
- Do I have access to data?  Transcribe it 
-  primary and secondary data 
- Check the quality - distribution , bias 



---

Idea from Pit's defense 

- What RQ in which part of the  talk 
- overall talk related meterics 
- - performance, feasibility, explainability 
- Simulation - numerical, stocastic, numerical simulation 
- what is regime 
- outcome - key words 


Validation - what

----
Faulty tree analysis of the multi-link 


https://www.youtube.com/watch?v=OX3DLl_3FkU 
Dissertation 
Political - All reviewers comes with vanish points 
![[Screenshot from 2026-03-11 09-20-54.png]]

Bring novelty in presentation - what is possible now that was impossible before 
explicit about key contribution 
support claim  - don't sound defensive or emotional 
time is important 


Are machines always efficient? I saw a worker using blower by to clean the mud, and leaves and push it down the roof. The device is heavy, and he must use his legs sometime to push, I wonder why a shovel wasn't used?


![[260225_TUD_Self-Assessment Report_2025_ohne Annex.pdf]]


Idea for the plots and connects 

----


It sounds like you are describing a **Regulatory Pilot** or, more specifically, a **Regulatory Greenfield Extension**.

However, the most precise technical term for what you’re describing—where a project is tethered to existing "state-of-the-art" rules because it can’t yet stand on its own—is a **Transition Path** or **Regulated Incubation**.

---

## The Key Concept: Regulatory Coexistence

In these scenarios, the new field isn't "free" to experiment (like a sandbox). Instead, it operates under **Transitional Governance**. Because the technology is so closely linked to existing infrastructure or high-risk sectors (like Aerospace, Nuclear, or Bio-tech), regulators apply "inherited" rules while the new standards are being drafted.

### Sandbox vs. This Setup

The difference essentially comes down to **permission** versus **compliance**.

|**Feature**|**Regulatory Sandbox**|**This Setup (Pilot/Extension)**|
|---|---|---|
|**Primary Goal**|To see _if_ the rules should change.|To see _how_ existing rules apply to new tech.|
|**Independence**|Highly independent; often exempt from certain laws.|**Dependent**; must comply with "state-of-the-art" legacy rules.|
|**Liability**|Often shielded or reduced.|Full liability under existing frameworks.|
|**Exit Strategy**|Graduation to a new license.|Integration into the existing regulatory body.|

---

## What is it called?

### 1. The "Brownfield" Expansion

In engineering and policy, if a project is not a "Greenfield" (completely new/independent) and not a "Sandbox" (experimental), it is often treated as a **Brownfield Extension**. This means you are building something new, but you are forced to use the "plumbing" and "wiring" (the regulations) of the system that came before it.

### 2. Proportional Regulation

If the state is forcing you to follow existing state-of-the-art rules because the project "cannot be treated as independent," they are applying the **Equivalence Principle**. This is the idea that if a new project functions similarly to an old one, it must meet the same safety and legal bars until it proves it is "sui generis" (unique).

### 3. Shadow Regulation

In some niche fields, this is called **Shadowing**. The new project runs alongside existing applications, adhering to their rigorous standards to prove it is at least as safe or effective as the current "state of the art" before it is allowed to have its own dedicated framework.

---

## Why "State of the Art" Matters

When a regulator says you must follow the "state of the art" (SOTA), they are usually invoking **Legal Certainty**. They don't want a "regulatory vacuum." By tethering your project to existing applications, they ensure that even if the field is new, the safety and ethical guardrails are already proven.

> **Note:** If you are looking for a term more specific to a certain industry (like Fintech or Medtech), the name might vary. For example, in medicine, this is often called **Post-Market Clinical Follow-up (PMCF)** for devices that are new but based on "equivalent" predicate tech.

**Would you like me to look up specific legal terminology for a particular industry, such as AI, Energy, or Healthcare?**


In the specific context of **Unmanned Advanced Air Mobility (AAM)** and **Integrated Air Mobility (IAM)**, this setup is most commonly referred to as **Evolutionary Certification** or a **Special Condition (SC)** framework.

Because the aviation industry is built on "blood priority" (regulations written after past accidents), the state of the art ($SOTA$) is the baseline. When a new AAM project cannot be treated as independent, it is often managed through **Type Certification by Analogy**.

---

## 1. The Core Terminology: "Special Condition" (SC)

In both FAA (USA) and EASA (Europe) jurisdictions, when an AAM project doesn't fit a "Part 23" (Small Airplane) or "Part 27" (Rotorcraft) box, it is governed by **Special Conditions**.

- **The Setup:** You are forced to inherit the safety objectives of existing crewed aircraft (the state of the art) because the regulator does not yet have a "standalone" rulebook for autonomous AAM.
    
- **The Dependency:** It is not independent because you must prove "Equivalent Level of Safety" ($ELOS$) to legacy systems.
    

---

## 2. Why it isn't a Sandbox: "Certification Basis"

A sandbox allows for "fail fast." Aviation does not. Instead of a sandbox, you are building a **Certification Basis**.

|**Feature**|**Regulatory Sandbox**|**AAM Evolutionary Setup**|
|---|---|---|
|**Philosophy**|"Let's see what happens."|"Prove this is as safe as a commercial jet."|
|**Rules**|Temporary waivers.|**Inherited requirements** from SOTA.|
|**Operational Risk**|Controlled/Isolated.|High (Integrated into National Airspace).|
|**End Goal**|Data collection.|**Type Certificate (TC)** issuance.|

---

## 3. Specific Engineering Terms for this "Trailing" State

If you are looking for the exact name of this "attached" stage in engineering management, it is often called:

- **Means of Compliance (MOC) Mapping:** This is the process of taking an existing regulation (like engine bird-strike requirements) and "trailing" it into an unmanned context where the hardware might be different but the risk remains the same.
    
- **Crawl-Walk-Run Integration:** In IAM, this refers to the period where unmanned systems must follow **IFR (Instrument Flight Rules)**—the current state of the art—before "Digital Flight Rules" (the future independent state) are even legalized.
    
- **The "Gap Analysis" Phase:** When a project is defined entirely by the "gaps" between what it is and what the current law requires it to be.
    

---

## 4. The "Sui Generis" Threshold

The point where the project _can_ be treated as independent is when it achieves **Sui Generis** (of its own kind) status. For AAM, this happens when the regulator moves from **Prescriptive Regulation** (Follow these specific old steps) to **Performance-Based Regulation** (Meet this safety goal however you want).

> **Crucial Difference:** In a sandbox, you are outside the fence. In this AAM setup, you are **inside the fence**, tethered to a legacy "safety anchor" until you prove your new technology can hold the weight of the sky on its own.

**Would you like me to look into the specific EASA SC-VTOL or FAA Power-Lift certification paths to see how they "trail" from existing Part 23/27 regulations?**


---


**Brownfield development** is a term commonly used in the [information technology](https://en.wikipedia.org/wiki/Information_technology "Information technology") industry to describe problem spaces needing the development and deployment of new [software](https://en.wikipedia.org/wiki/Software "Software") systems in the immediate presence of existing (legacy) software applications/systems. The term was introduced in 2008 by Hopkins and Jenkins.[[1]](https://en.wikipedia.org/wiki/Brownfield_\(software_development\)#cite_note-1) This implies that any new [software architecture](https://en.wikipedia.org/wiki/Software_architecture "Software architecture") must take into account and coexist with live software already [in situ](https://en.wikipedia.org/wiki/In_situ).
