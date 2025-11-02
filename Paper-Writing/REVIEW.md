1. Paper review measures 
	 - Skim the abstract, introduction and conclusion - identify if the RQ is clear 
	 -  Clarity, Structure , Methods, Results, Discussion and novelty
	 - Strengths , Weaknesses , Relevance 
	 - Ethical aspects in question 
	 - Write a short summary review
---

IEEE transactions of Network and service management 
Initial review Reviewer: 1  
  
Comments to the Author  
Requested Revisions and Clarifications:  
  
1. Please include a comparative table that clearly highlights the strengths of your paper in relation to existing research. This will help contextualize the contributions more effectively.    
  
2. Provide more details on the practical implementation of the multi-agent approach. Specifically, clarify whether UAV agents share their actions with other UAVs and how this interaction influences decision-making.    
  
3. Elaborate on the training process. If the proposed scheme is intended for real-network implementation, explain how it would be deployed in practice.    
  
4. The reward function is currently unclear and could be improved for better clarity and understanding. Please refine its explanation.    
  
5. There appears to be a discrepancy between the reward function in Figure 6 and Equation (37). Please clarify why they differ and ensure consistency between them.    
  
6. The results shown in Figures 8 and 9 appear to follow opposite trends: in Figure 8, coverage decreases as the number of users increases, whereas in Figure 9, throughput increases with more users. Please explain this contradiction.    
  
  
Reviewer: 2  
  
Comments to the Author  
I have the following remarks that can be addressed in a revision of this manuscript.  
p1, l53, c2: replace "of deploying without" with "of deploying AeBSs without"  
p2, l68, c2: remove the repetition of "resource allocation and task scheduling"  
p3, l4, c1: replace "have been done to address" with "addressed"  
p3, l5, c1: remove the repetition of "search and tracking tasks"  
p5, l28, c1: remove the repetition of "In the following"  
p6. C. Problem formulation: Describe in the paragraph the meaning of the tuple term S.  
  
It would be nice if you can address the energy and computation requirements for running the proposed algorithm on the flying platform as this will affect the flight time and flight path management.  
  
Is there any specific reason that the transmit power of both BS and UE/MU is the same, i.e. 1W. Usually this is asymmetric with transmit power of UEs usually a couple of orders of magnitude lower.  
  
  
The manuscript addresses the deployment of AeBS in disaster areas, which is a relevant use-case. A minor addition that could improve the work is to consider the energy requirements from algorithm calculations on-board of the aerial platform, as it will definitely put stringent constraints on the flying time and flight path planning.  
  
Associate Editor  
Comments to the Author:  
The paper addresses the interesting problem of the automated network deployment and service management independent from network assistance, which can be assumed to be unavailable in disaster affected areas. The two reviewers and this guest editor find that the paper has some merits, however, especially Reviewer 1 points to some major deficiencies, related to unclear presentation of related work, implementation, and procedures, as well as technical issues. Therefore, a major revision is recommended.

---
Notes from paper 

Relevant problem - practical scenarios such as natural disasters or temporary
large-scale public events,  the distribution of user clusters is often unknown, posing challenges for the deployment and application of AeBS.
In light of the above considerations, this paper addresses the problem of dynamic deployment of AeBSs without networkside assistance. We propose a new deployment scheme based on DRL, specifically a MAPPO-based multi-agent AeBSs dynamic deployment algorithm for unknown user distributions
hybrid Gaussian model and constructs a partially observable Markov decision process (POMDP).
This results in a quasi-static system where conditions are considered constant during any
given time slot. Specifically, within each time slice, both the user distribution and the positions of the AeBSs are assumed to remain unchanged. The system temporarily does not consider
the interference from the external environment and the impact of terrain factors.
We define the behavior of the AeBSs as a sequential
decision-making process.

The process of dynamically identifying and deploying to the hotspots of the disaster-affected user clusters can be equated to the process of maximizing the collection of environmental
information. To formalize this relationship, we propose the following Theorem 1, which establishes the theoretical basis for this equivalence.
Theorem 1. The process of an AeBS moving from the edge
position to the hotspot area of the disaster-affected MU
cluster can be understood as closely related to the process
of maximizing the information gain.