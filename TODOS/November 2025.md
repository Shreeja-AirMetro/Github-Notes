Each month priority and todos : Deadlines and milestones and small section of thoughts and ideas to track back implementation

Weekends: Work on this https://www.cisco.com/c/en/us/tech/index.html and https://www.sharetechnote.com/Home.html 
on Networking protocol 
5G , LTE and WiFi 

Read: 
https://www.dlr.de/en/kn/about-us/departments/communications-systems/aeronautical-communications-group
https://www.ldacs.com/ 

### Goals and Milestones

1. Dronnect Journal paper 
2. mesh device setup 
3. VM phase 1 complete 
### PhD Thoughts 
The PhD research network coding and computation is mandatory for Aerial communication. How the communication and computing via coding part will exists ? 

Explain the communication requirements 
Go to the coding part - Network coding and the crucks and nooks in multi-link communication 

3 big pillars of writing dissertation 
- UAV side of communication 
- GCS and ground infrastructure 
- New network architecture like NTN and particular to this use-case 


Key challenges: In **Advanced Air Mobility (AAM)** — especially low-altitude operations (0–120 m AGL) — drones (UAVs/UAS) must rely on robust, low-latency, and safe communication links for:
- Command and Control (C2/C3)
- Detect and Avoid (DAA)
- Navigation and cooperative behavior
- Integration with U-space / UTM (Unmanned Traffic Management) system

Challenges emerge because this **low-altitude environment** is complex:

- High interference from buildings and ground clutter
- Variable LOS/NLOS conditions
- Limited cellular coverage at 120 m (not optimized for aerial users)
- Spectrum sharing and regulatory issues
- Multi-operator coordination in AAM corridors 

**Big mistake is to assume:  redundancy equals reliability**
  
Latency is going to be your biggest problem for real time flight adjustments.
DTU (Technical University of Denmark) executed extensive 3D measurement campaigns at HCA Airport.  - https://genius.aero/index.php/work-package-1/ 

- NetworkX python package 

### Literature review workflow
	- Find literature , filter and read main
	- Reference manager - Mendeley - Litmaps - connected papers - concenses /scispace for filtering 
	- Notebook LM for research concept and gaps - also concenses
	- Get a structure - suggested structure - scispace
	- content 
**==read from back for review==**
### Big Tasks 


1. Mesh devices 
	- Technical specification of Hardware and figure out the power 
	- Initial test with laptop 
	- Rasp pi test 
	- Pixhawk test 
2. Rasp pi + LTE Dongle 
	- Resolve the LTE dongle and SIM Card issue with Sebastian
	- Dongle test with Laptop
	- Dongle test with Rasp pi 
	- Pixhawk to QGC - via dongle 
3. VM Setup for Multi-Link simulator 
	- Setup multi-link VM simulator  - what are key entities in each machine 
	- Setup  and test Sat link 
	- Setup and test Cell link 
	- Establish Multi-link data with QGC 

### Small Tasks 

1. AirMetro Winter workshop 
	- ~~Recap on TAC meeting - The gap and blocks of methodology~~ 
	- Simulation VM part 
	- Mesh and other hardware idea and Status 
	- Next steps and plan 
	- Klagenfurt Visit 
2. DA presentation for Lyuqiao 
3. Email Sec. of Christian Bettstetter 
4. Find apartment 
5. PhD rebuttal letter 
6. dronnect paper (V1 : by 4th November) (V2: by 10th November) submission by 11th November 
7. Support FMC Review submission 
8. Restart Work with Roshan - Paper 
9. Omnet++ Day with Lyuqiao 
10. ROS2 with lyuqiao 

### Misc
- We have 3 backup online
	-  Obsidian notes - regular backup Github and Gitlab 
	- Official backups Monthly on Gitlab- comnets

- Write project plan with WPs



### Remarks
Week one was less efficient and not really productive 
the planned tasks are pending  - Dronnect paper, Mesh nodes aren't done well

So Friday - 7th Redemption Day 

to dos:

- [x] Create a WP and Milestones 
- [ ] Work on Literature Pipeline and table - What is story to build
- [x] meeting for FMC paper
- [x] Plan next week 
- [x] Weekend - work on paper 
- [x] Tushar Bestellung document 
- [x] Martin CNS group message 
- [x] DA midterm presentation email
- [x] Report submission
	- [x] review with stan 

- [x] Mail Morten and Rodney
Sat 8/11
- [ ] Dronnect paper
Sun 9/11
- [ ] Dronnect paper
- [x] Finalize DA slides - Lyuqiao

Monday 10/11
- [ ] 
- [x] DA mid-term presentation 
- [x] AirMetro Meeting 
- [x] Meeting for CNS group 


Tuesday 12/11
- [x] Falling prize winner meeting 


----
Week 46

- [ ] Dronnect paper
- [ ] Literature organize and reading 
- [ ] Mesh devices Stage 1

---
Takeaway from RTG review 
- More women 
- Post-Doc 
-  elect care person /  diversity manager 
- 4 year contract for second cohort 
----

 Jacob - Prague university UTM , infrastructure AAM - small workshop 

To do: 
- [x] Send the post to Elif 
- [x] Tushar Hw


---

### To learn 
- Wireless communications theory (link budgets, fading, Doppler, MIMO, beamforming).
- Cellular stack familiarity (4G/5G NR concepts, 3GPP specs affecting UAVs; how to read TRs/TSs)
- RF & antenna basics (antenna patterns at altitude, ground interaction).
- basic ML for signal/telemetry analytics.
- Cloud & edge computing (k8s, edge orchestration, low-latency MEC patterns).
- Satellite comms basics (LEO constellations, link budgets, latency constraints). [MDPI](https://www.mdpi.com/2078-2489/15/1/38?utm_source=chatgpt.com)
- Security & authentication for UAV links (secure Remote ID, secure boot/firmware). [Drone as a Service](https://www.droneasaservice.com/blog/faa-remote-id-rule-for-drones/?utm_source=chatgpt.com)
- Certification & regulatory knowledge: SORA, EASA U-Space, FAA BVLOS/Remote ID ecosystems.

---

## week 20th - 1st December 

- [ ] Dronnect paper  
	- [ ] Draft 1
	- [ ] Review and finalize figures
	- [ ] Emails and approval 
- [ ] ROS initial setup reading 
	- [ ] Meeting with Tushar 
- [ ] Omnet++ Setup and initial tutorial with Lyuqiao 
- [ ] Mesh hardware initial setup 
- [ ] Klagenfurt - dienstreise
- [ ] LAWN paper 
	- [ ] reading SOA, Research gap
	- [ ] Meeting and tasks with Roshan 