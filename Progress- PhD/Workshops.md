
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

Martins demons + digi twin 
idea 2 demonstrator : operational based 

Physical 
T7  - overarching goal with urban setting // micro climate - might not be fully satisfied by Wind tunnel 


