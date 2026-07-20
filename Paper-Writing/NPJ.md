
# Wishful and ambitious try 

Collection 

# Sustainable and Intelligent Connectivity for Low-Altitude Wireless Networks

Submission status

Open

Submission deadline

13 October 2026 - try for this collection 


1. RCP methods 
2. Physical and logical link analysis 
3. Protocol level C2 link 

**Aviation reliability analysis** leans heavily on a small set of tools, mostly borrowed from systems safety engineering rather than communications theory:

- **Continuous-time Markov chains (CTMC)** are the workhorse — used for avionics system reliability (e.g. modular avionics reconfiguration analysis) and more broadly for modeling failure/recovery transitions, computing probability of failure per hour and related integrity metrics that map directly onto IEC 61508-style safety parameters.
- **Reliability Block Diagrams (RBD)** combined with survival/hazard functions — one cross-layer framework models a wireless link's reliability from packet generation through PHY/MAC/network/application layers using non-repairable-system survival analysis, treating "availability" as the probability a reliable transmission link is present.
- **Generalized Stochastic Petri Nets** for dispatch reliability, and Markov techniques generally, for backup/redundancy compensation modeling.
- On the navigation-integrity side (closest cousin to your "integrity" RCP parameter), **ARAIM for GNSS** builds explicit stochastic error models — Gaussian bounds on orbit/clock error, elevation-dependent variance models — validated against both simulation and real data, specifically to support continuity/availability/integrity guarantees for safety-of-life applications. This is a genuinely useful template because it's solving almost exactly your problem: turning noisy technical measurements into formal integrity/continuity/availability numbers under a certification-grade definition.

**The gap in this list:** none of these methods were built to reconcile heterogeneous RAT statistics. CTMC/RBD approaches assume you already have a well-characterized failure process; they don't tell you how to derive that process consistently from raw 3GPP-style KPIs across structurally different technologies.

### Telecom-side statistical machinery you can borrow

- **Finite-State Markov Channel (FSMC) models** — the standard way to capture burst/correlated fading behavior (rather than treating samples as i.i.d.), used extensively in wireless networked control to derive stability guarantees from channel state transitions.
- These models have also been _learned_ from data via regression trees rather than assumed a priori, which matters for you: with a short campaign you won't want to hand-pick a channel model, you'll want to fit one from what you actually observe.