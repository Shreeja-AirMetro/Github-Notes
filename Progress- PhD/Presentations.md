13-14th winter workshop 

What's the goal of communication in AAM - CNS 
1. Communication Technology 
2. The actual message 
3. Link quality (Physical and Logical)
4. Optimization 

Nikaulas - DLR - Air to X project IEEE 802.11p (V2X air module)


---
Presentation 4th 

1. Intro and Motivation 
2. Current status /hardware setup 
3. Simulation and next steps for visit 
4. Multilink and network coding methods 
---

Presentation 17/12 
Prep for klagenfurt 

1. RTG 
2. CNS 
3. Challenges of CNS 
4. what are topic entails  - Goal / requirement , Technology in use, Methods , plan of action 
5. PLan of action 3 stage 
	1. Simulation 
	2. testbed and flight test 
	3. Netwokk coding and multipath 
6. Goal of this visit 
	1. Simulation 
	2. Handover 
	3. KPIs 

some comments from my side for your pages:  
title:  
Dr.-Ing. typo2  
germany template ? (Seite 2 instead of side2)  
what is T in T1...T10 ? needs to be explained once4  
different T stlye6  
explain V on the slideKPIs for Availability, Continuity, Transaction Time, Integrity... define exactly please
References
Formatting 
How measure RCP - get a formula/threshold

RC computing and energy effeciency

---

Winter workshop 13-14th preparation 

Stage 1 of the project 
What was initial idea 
- Efficient resource management and link handling of wifi, 5G and satcom link 
- What levels - the UAV, The ground station, UTM network 
- Type of links and data we talk and how its collaborated with AirMetro group 
- what is expected outcome - heatmap 
Where are we - preparatory stage , experimental, validation stage parallel processing with theory and hardware 
- Simulation - VM setup
- Network coding methods and implementation 
Experiment with hardware - 
- Mesh nodes setup 
- LTE dongle setup 

What's next 
- Research visit - topic planned 
- milestones of my project 

---
10/11
- Introduction of CNS cluster from summer school 
- T2 raytracing with T5, T8 (navigation) , T9 and T10 

----
MoM 13/11 Winter Workshop , Moritzburg 

Session on Data Management 
LEGO Metadata for reproducibility

Lego build plan and write description that can be reproduced by other team 

Documentation template is important 
details in the documentation
common naming convention
establish the goal/ vision 
3 sheets of paper 
goal / data providence is important 
visualization  - pictures and drawings / plots to describe the data/ instruction 

----
Next session: eLABFTW

---
Uncertainty optimization  talk by Niklas Schietzold 

- Is this just about Monto carlo 

Modeling and quantification 
Uncertainity models  - Aleotoric - measurable and not reducible 
two major types  
epistemic 
systematic error  or offset - lack of knowledge - identical - theoretically reuseable and reducible 
interval or fuzzy variable 

Combined - hybrid - polymorphic uncertainity 
Limit state function - a quanti we measure 

"often show mean/ one scalar value pro of failure" --> why don't we show all value 
- interpretability 
- comparability 

solving two optimization problem 
x1  and x2 are intervals - mapping with z is a fn a 
min and max in input interval 
fuzzy  - stacking of multiple interval analysis 

Data ( quantity, precision and assesment) based uncertainity modelling choose methods accordingly 

"comparability"
deterministic optimization task  
	 uncertain design parameters , apriori parameters
	 what to do with uncertain output ? 
	 eg 3 design  3 fuzzy intervals - get "center of mass - centroid values (mean)"--> compare them 
	 width of interval - area
	 what is optimal ? 
	 Performance or robustness oriented
	 Vicinity in prob of failure - high uncertainty 
	 Low uncertainity - prob of failure is high and things fail drastically
Polymorphic - Basic soln - FEM - Stocastic analysis - fuzzy analysis - optimizzation

"affine transformation" - what is this 

Steel hook example for stress  - get the variables, get type and ten assign uncertainity model 
goal of alpha level 

Q: 
what is performance and robustness in the steel hook example 
when do you decide to go to this surrogate problems  - not just about mass and stress 

robustness and optimalilty 

Monte carlo - is burst optimizer - go with stocastic problems

increasing # of samples start with probabilistic model 
ecdf - fitted cdf and data pts not extremely low - 
pbox 
weight - scewed "what's moving the fn - holistic sensitivity analysis"

---
Martin's session on Demonstrator 

Martins demons + digital twin 
idea 2 demonstrator : operational based 

Physical 
T7  - overarching goal with urban setting // micro climate - might not be fully satisfied by Wind tunnel 

---
Tushar talk 
LiDAR + event camera for 
SWAP-C

Prep for drones : mechanical assembly, electrical assembly, Software (ARM, Drivers, ROS2, PX4-ROS 2)
Event camera - time decaying filter --> (pixel represent time)Time surface map 

Even camera's quantum efficiency for LiDAR's wavelength is non-trivial 
filter block IR frequency 

frequencies measurement  with event camera 

Angular and translation motions 
 Data visualization - RViz2
 Tushar Goal : A perception based navigation with flight controller for AAM 
 Can IMU be removed with sensor suite 

---

14/11
Martin - Wrap up 
	- Lego 
	- Agenda 

Hartmut's presentation

Using Sharepoint to declare a publication intent 
abstract / mission Statement free for commenting by ALL - lead author decides wisely 
Team work and consistency across RTG 

**comment by Aßmann**
questions of basic research and questions of applied research 
problem formation of technical research and application research 

Sharepoint - timely result on publication 

When is SML coming - reflecting you work 

---

Computational flow dynamics 
PALM Model sytsem - roof geometry - flow parameter is different 
Open Foam  - more case studies 


- 3D urban model 

----
Ideas from Stefan senk talk 

Public defense 30 mins 
- Part 1 - Investigation 
	- Literature 
	- Metrics 
	- Packet delay variations PDV 
	- Time aware shaper 
- Part 2- Methodology - Build and conducting measurements 
	- Build the use-case 
- Part 3 - Selected results 
READ STEFAN SENK THESIS
Wireless system - fading
H of information - instead of latency
