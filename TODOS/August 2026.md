Can I say, I send packet via Stacom- via 5G - Semantic 
https://esra.website/esrel

1. 25th Letter 
2. 
# Deadline 

1. DATE - Multipath 
2. Drone Mesh Telemetry 
3. Drone 5G , Satcom Telemetry 
4. Drone mounting
5. simcard


Open Tasks 
1. Study Comnets 1 and 2
2. Setup testbed to data collectiong 
<span style="color:rgb(255, 0, 0)">3. FNWF</span>
3. ElabFTW
4. Student tasks Wiki
5. IEEE Access

# Week 32

- [x] Coments 2 oral exam 
- [x] Tianxiong dicussion 
- [x] SIMCARD Issue - Sebastian
- [x] AirMetro Meeting 
- [ ] Mesh Hardware 
- [x] Student Task wiki 
- [x] Student meeting PPT 
- [ ] IEEE Access Data Collection - V1 complete
- [x] Bianca Docs submit 
- [ ] Jiajing FNWF Discussion 

### Monday
- [x] Tianxiong Meeting 
- [x] AirMetro Meeting 
- [x] Simcard issue Sebastian
- [x] Bianca bills + Excel sheet
- [ ] Study Comnets 2 - finish and start revision 
	- [x] MEC
	- [ ] TSN
	- [x] SDN
	- [ ] Core
	- [x] Slicing
- [x] Student task PPT
- [x] FNWF - initial skeleton

### Tuesday 
- [x] Coments 2
	- [x] TSN
	- [x] 5G
- [ ] Comnets 1 
	- [x] Intro 
	- [x] History
	- [x] Shannon
	- [ ] Source coding
	- [ ] Ex 1 
	- [ ] Ex 2
- [x] Comnets 2 - Rev  - 2 sets
- [x] Sep event registration
### Wednesday 
- [x] Comnets 2 prep - 8 sets of question
- [x] simcard
- [ ] Comnets 1
	- [x] Source coding
	- [x] Aloha
	- [x] Ethernet
	- [ ] Graphs and Flows
	- [ ] Routing
	- [ ] Transport 
	- [ ] NC - 1 and 2
- [x] Tianxiong - 
### Thursday
- [x] Coments 2 prep 
- [x] Oral exam 
- [ ] Comnets 1
	- [ ] Ex 3,
	- [ ] 4,
	- [ ] 5,
	- [ ] 6
- [x] Aeroconf paper - prep
- [x] Bianca email 

### Friday
 - [x] Meeting-Enrique
	 - [x] List tasks 
	 - [x] Overleaf
 - [x] Student task Wiki 
 - [x] Berlin DR
 
 - [ ] Arrange my calculator 
 - [x] Plan weekend and other tasks

- [ ] Comnets 1 - Ex 1-6

---

# Pending tasks 

# email and admin work 

- [x] ming reply
# Simulator 
- [ ] uplink 
- [ ] Data collection
- [ ] IEEE V1

<span style="color:rgb(255, 0, 0)"># FNWF  (cancel)<br>- [x]  FNFW run - data  <br>- [x] FNWF coding</span>

# Hardware 
   - [ ] Mesh hardware
	   - [ ] Help from krishna
	   - [ ] Visit - Basic setup
	   - [ ] Review other parts
# Week 33

- [x] Comnets 1 exam 
- [ ] AirMetro Student Meeting 
- [ ] Mesh hardware
- [ ] Satcom  IOt hardware
# Monday

- [x] Comnets 1 exam prep and Exam
- [x] Admin  tasks 
- [ ] Traffic Theory - L1, L2, L3
# Tuesday

- [ ] Study - Traffic Theory 
	- [ ] L4
	- [ ] L5
	- [ ] L6
	- [ ] L7
- [x] Mesh hardware - help from Krishna requested 
- [x] Simcard
- [x] Sarah reply

https://kb.doodlelabs.com/starlink-satcom-integration-guide
https://doodlelabs.filecloudonline.com/ui/core/index.html?mode=single&path=/SHARED/%21qrj7yyGkC7ddf30uyg3kVGjq3YxZH9155dSoa1pzk/wXGsdYeksvloAM1W#/
# Wednesday
- [x] Omnet++ simulator 
- [x] Meet Jonas
- [x]  Sarah message

- [x] Student Meeting
	- [x] MM prep
- [ ] Study Traffic Theory 
- [ ] Study smartgrid comm
# Thursday
 - [x] Study Smartgrid comm
 - [ ] FNWF prep 
	 - [ ] Fix codes - inputs from Jiajing 
 - [x]  FNWF prep - Discussion Paper 
 - [x] Tasks of paper - Krim
- [ ] Study Traffic Theory 

# Friday

 - [ ] Study Traffic Theory 
 - [x] Study Smartgridcomm
 - [ ] Plan Week

 - [x] Another simcard
 - [x] email Krishna

 - [ ] Meeting with Jiajing Krim 
 - [ ] Bronchi 
 - [ ] Shangqing 
 - [ ] Photo dm 

 - [ ] Visa docs - upload

---
# Week 34
- [ ] Smartgrid exam
- [ ] Traffic Theory exam 
- [ ]  Call Email - Morten
- [ ] Visa appointment friday 
- [ ] NB IOT setup 
- [ ] UTM - Deconfliction 
- [ ] Satcom Hardware
- [ ] Mesh hardware 


# Monday

- [ ] Exam 

# Tuesday




# Wednesday 

- [ ] Exam prep 


# Thursday 

- [ ] Exam 

# Friday 

- [ ] Vacation Berlin appointment

---

# Week 35
- [ ] Backup
- [ ]  ElabFTW
- [ ] Uta Letter
- [ ]  Uspace - Mahdi


---

# Meeting with Tianxiong

Parameters of bigraph model 

four layers of risks 
1. 
2. communication  - no more, lost - 
3. take off and landing 

- model recovery 
Mission success rate and 


cube 100 - 10 m/s - 10 s

Drone lost - comm lost each grid MTBF

to do: outage percube perspective 


---

Drone communication - UAV air-to-ground (A2G) link reliability problem
1. Availability - When BS provides connection 
2. Continuity - non-continuity - extends - link loss/ outage condition 

BS, Height of BS   hBSh_{BS} hBS, uav altitude hUAV​

General DIstance equation - 3D distance - I assume UAV is having a straight path 
d(t)=(x(t)−xBS​)2+(y(t)−yBS​)2+(hUAV​−hBS​)2​

where x(t),y(t)x(t), y(t) x(t),y(t) trace the UAV's straight-line path at 10 m/s through the cube. This gives you a distance profile d(t)d(t) d(t), and an elevation angle profile:

θ(t)=arctan⁡ ⁣(hUAV−hBS(x(t)−xBS)2+(y(t)−yBS)2)\theta(t) = \arctan\!\left(\frac{h_{UAV}-h_{BS}}{\sqrt{(x(t)-x_{BS})^2+(y(t)-y_{BS})^2}}\right)θ(t)=arctan((x(t)−xBS​)2+(y(t)−yBS​)2​hUAV​−hBS​​)


---

# Enrique  Meeting 

1. prior 
2. Operational margin 
3. Latency, Velocity operational margin 
4. Prevention - inner loops 
5. Operational margin 
6. Communication Performance envelopes 
7. Enhanced envelop with and without reactive area 
Tasks 
Break it into small parts 

8. Brief to do list 

NVDIA Tool  - Omniverse 




