---
marp: true
theme: default
paginate: true
backgroundColor: #fff
---
Meeting with LyuQiao 

--- 
# Goal 

- UAV as a user flying at 60m - 100m must connect to TN and NTN network based on signal strength to send and receive CBR packets from the server 

---

# Potential Methods - 1

1. Directly use Veins Leon 
	- Veins-Leon is used for  Cars with Veins-Sumo Integration 
	- Alter the speed and Add Z axis 
	- DID NOT WORK - the Z-Axis mobility was not considered by the simulation pipeline
	- Crash after the simulator SUMO opens 

----

# Method - 2

2. SUMO has a add on UAVsimu.py  - DID NOT WORK
	- A python based extension but used only for the mobility of the UAV in xyz axis 
	- UAV cannot be used as a aerial node to test the network parameters 


---

# Method - 3

3. INET 3D Spatial Mobility 
	 - Remove the dependency of UE on Veins-SUMO 
	 - Use the INET only superimposed mobility 
Q: What all framework/code to be mindful 


---

# Outlook 

1. What other possibility 
To do: 
Try 1, 3 methods
Get the error and debug tree - update and discuss with lyuqiao


---
Last meeting fro Lyuqiao 

Points to test 
1.- Do veins mobility have drone  - from Veins INET - extend the x, y, z - rou file 
2. Work with INET model - check the NIC  - adapt 2 phy layers

