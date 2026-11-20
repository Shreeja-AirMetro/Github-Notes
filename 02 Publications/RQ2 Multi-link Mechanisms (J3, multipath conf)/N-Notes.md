# N7
Check notes
Not using online since 24thfeb 2026 - Think on paperNetwork coding 
### Coding for High Reliability (The "Safety" Link)

For BVLOS, a 1% packet loss can be catastrophic. Coding theory provides the "mathematical armor."

- **Marco Mondelli (2018, EPFL): _"From Polar to Reed-Muller Codes"_**
    
    - **The Impact:** Winner of the **Marconi Society Paul Baran Young Scholar Award**. His work on **Polar Codes** is what allows 5G control channels to be nearly "unbreakable."
        
    - **Why it matters for you:** If you are operating a drone at 50km distance (BVLOS), the "Control" link is likely using the Polar Coding principles Mondelli helped perfect to ensure the "Return to Home" command always gets through.

To understand the difference, it helps to look at **where** the math happens and **why** it’s being used. In short: **Channel coding** protects data from noise on a single wire or airwave, while **Network coding** optimizes how data flows through a complex web of routers or nodes.

---

## 1. Channel Coding (The "Noise Armor")

Channel coding is performed at the **Point-to-Point** level (Physical Layer). Its goal is to ensure that if a "0" is sent through a noisy environment, the receiver doesn't mistakenly read it as a "1."

- **How it works:** It adds **redundancy bits** to a single data stream. If some bits are flipped by interference (noise), the receiver uses the remaining bits to mathematically reconstruct the original message.
    
- **Common Techniques:** LDPC (used in 5G), Polar Codes, and Reed-Solomon.
    
- **Analogy:** Imagine writing a letter and repeating every sentence twice. If a coffee stain blurs one sentence, the reader can still see the second copy to understand the message.
    

---

## 2. Network Coding (The "Traffic Orchestrator")

Network coding happens at the **Network/Link Layer**. Instead of just forwarding packets like a post office, the intermediate nodes (routers or drones) **mix** multiple incoming packets into a single outgoing transmission.

- **How it works:** A router receives Packet A and Packet B. Instead of sending them one after the other (taking two time slots), it performs a mathematical operation—usually an **XOR ($\oplus$)**—and sends a single coded packet ($A \oplus B$).
    
- **The Benefit:** It increases **throughput** and reduces congestion. A receiver with Packet A can "subtract" it from the coded packet to reveal Packet B.
    
- **Analogy:** Two people trying to exchange books across a river. Instead of crossing twice, they both throw their books into a "magic box" in the middle that combines them into one lightweight package, which both can then decode.
    

---

## 3. Key Differences at a Glance

|**Feature**|**Channel Coding**|**Network Coding**|
|---|---|---|
|**Primary Goal**|Error Correction (Reliability)|Throughput & Efficiency (Capacity)|
|**Location**|Transmitter $\rightarrow$ Receiver (1:1)|Internal Network Nodes (Many:Many)|
|**Problem Solved**|Physical Noise / Interference|Congestion / Bottlenecks|
|**Operation**|Adding Redundant Bits|Mathematical Mixing (XOR, Linear)|
|**5G/Drone Use**|Ensures the "Command" signal isn't corrupted by distance.|Allows multiple drones to relay data for each other without clogging the frequency.|

---

## 4. Why this matters for Drones (BVLOS)

In long-range operations, you often use both:

1. **Channel Coding** is what keeps your 5G or Satcom link "locked" when the signal gets weak at 20km away.
    
2. **Network Coding** is used in **Mesh Networking**. If you have a swarm of drones acting as relays, network coding allows them to pass data back to the GCS (Ground Control Station) much faster than traditional "store-and-forward" relaying.
    

**Would you like to see the specific XOR math used in a "Butterfly Network" to see how it doubles throughput?**

### Information Theory (The Shannon View)

In 1948, Claude Shannon repurposed the word to describe the "information content" or "uncertainty" in a message. High entropy means a message is unpredictable; low entropy means it's redundant.

- **The Vibe:** How much "surprise" is in a line of code or a sentence.
    
- **The Math:** $H(X) = -\sum_{i=1}^{n} P(x_i) \log P(x_i)$
-


---

# N4

Mesh HW
A2A communication 

- Can we demonstrate air to air comm  - wifi , and landing or drone with wifi node
- What is protocol
# What is done 

- Hardware procured - comm established 
# What to do 
- Test the operation 
- Tests mavlink protocol 
- Work on protocol 
- test setup  - idea and to do 

# Goal 


End of march - figure out the protocol and setup to do 

Check notes
Not using online since 24thfeb 2026 - Think on paper

---

# N3

mnet++ Air - NTN simulator 

## What is done 

- The baseline to evaluating the methods are setup 
- Tools are  put in place
## What need to be done 

- Finish the change in simulator and run a test 
- V1 results 
### Goal

- This simulator servers as a baseline to test my methods and compare with realistic multipath 



16/2
- Check the sumo extention on Omnet++ simulator #
- What is the UAV.py extention fit to the storyline 

### Insights 
 - We divide the implementation into 3 parts 
 - 1-  use the UAV.py plugin  in sumo 
	 -  Sumo is just a mobility model and simulator
	 - The network aspects are not present as default  - we need VANET or something like VEINS to enable the network properties
	 - Else the UAV in this plugin is a aerial sensing/ monitor and provide only drone location data with geo coordinates 
 -  2- Use the same SUMO from LEON VEINS and use the UAV as UE with mobility model and test TN and NTN handover 
	 - First to try - VEINS and LEON setup with SUMO - Use a UAV instead of car 
	 - Change  the UAV node - ned file , python mobility bridge and the omnet++ config
 -  3- Create a separate TN- UAV as UE and run the test 


Check notes
Not using online since 24thfeb 2026 - Think on paper

---

# N2

This is about creating a report about the funnel method research questions and state of art complete 

### What is done
- Have unorganized state of art 
- have 4 Hypothesis 
- Rough implementation actions

### What to do 
- Read and organize the SOA for hypothesis 1 to 4 
- Write done what methods are done what you aim to do 
- What is your base line test - show in simulation 
- What is implementation steps and strategies for the actual implementation with flight test data 

### Goal
- presentation at klagenfurt 
- Fix the research hypothesis


### Random 

- We have A2 A and A2G link known - are there standards? how this link orerate ? can there be a set of rules 
- Guess - compare consequences - Compare to observations 


13/1 
How to back my hypothesis 
- [x] Sort the mendeley - add bibtext in to phd folder latex
- [ ] then structure the related SOA info into each segment 
- [ ] Then add the following points - What is the gap - What is done and what can I try / what QOS can it measure 

---

# N0

This is document with regards to NTN and omnet++ simulator froma wholistic perspective 

### What is done 
 - Lyuqiao Integration ISL 
 - Sumo 
 - V2X scenario
 - TN and NTN integrated via SUMO

### Open Tasks 
- Can TN only be in SUMO - or Another Omnet can be used 
- UAV fly via SUMO can be integrated 
- Without UAV fly how to solve this

### Plan of Action 
- Complete open tasks by end of Feb 2026
# Meetings - Collaboration with Satwat

- Presentation  - meeting 

### End Goal 
- Tutorials paper in April 2026 
- Lyuqiao conf or workshop paper

---- 
Check notes
Not using online since 24thfeb 2026 - Think on paper


---

# N1

This is Collab with T2 part with Roshan - Taking the basic Physical link characteriestics to Channel characteristics to params - protocol 

### What is done
- A pipeline of the poa is established
- A trial version of a and tau to channel data is tested 
- The need of RIS and use case esp placement of facade is done

### What to do 
- Coding from PPV and LDPC- need establish 
- protocol header level code to complete 
- Create report 
- Edit the paper with all params and have a version 
Target: end of 15th feb 2026 - revisit later 

### End goal 

- 2 publication with Roshan 


### IEEE TVT Journal 

- Pages 1-12 
- Page 1- 3 - Introduction Motivation, Abstract, Related works  - Table and contribution 
- Page 4-5  General system model 
- page 6-7.5 - Problem formulation - implementation
- Page 8 - 9.5 - Results and analysis 
- Page 10-11 Dicsussion, conclusion, Table of conclusion  Acknow 
- Page 12 - References, Biographies

1. Abstract , title 
2. Introduction 
3. Background
4. System model 
5. System model diagram 
6. Problem formulation and diagram 
7. Impelmetation and table 
8. Results plots
9. Analysis 


Check notes
Not using online since 24thfeb 2026 - Think on paper