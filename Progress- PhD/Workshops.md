
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