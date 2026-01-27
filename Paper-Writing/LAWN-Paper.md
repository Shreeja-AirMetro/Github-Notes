---
marp: true
theme: default
paginate: true
backgroundColor: #fff
---

# AirMetro Colaboration


Unfying goal of collaboration: Reliable medical delivery between urban- periurban areas minimizing teh risks of signal-related mission failure

Output of Topic 2: Bridging Physics and Networks: By using FEM-based near-field to far-field modeling, the project captures the actual physical behavior of signals (metaphysics), mapping blind spots and use of RIS. 

Output of Topic 9: Multi-Link Optimization: Quality-aware optimizing of multi-technology C2 link on its pre-planned flight path 

---

# LAWN Low Altitude Wireless Networks - Paper 

Link: https://vtsociety.org/post/announcement/call-papers-special-issue-low-altitude-wireless-networks-lawn 

Regular paper - 14 pages including reference and biographies
Submit via IEEE TVT Author portal
Deadline: 15 Feb 2026
10 pt font, single-spaced and double-columned final typesetting

Potential Topic: 

- URLLC for safety-critical applications in LAWN 
- Drone-based delivery, infrastructure inspection and public-safety network 

---
# Motivation
- Drones in BVLOS operation need to handle constant impact on signal quality in changing environment 
- This is critical when a drone needs to land in urban area between or on top of building during an emaergency (like airspace closure)
- URLLC engineered to handle communication that requires extreme stability and speed.(latency: Sub-1ms user plane latency.Reliability Target: 1 - 10^{-5} (99.999% success rate) for a 32-byte packet within 1ms.Availability: Constant connectivity)
- URLLC prioritizes mini slots than regular 1ms slot in LTE/5G - suitable for C2 communication

---
# Gap 
- Lack of connectivity aware trajectory / emergency landing spots planning 
- RIS in SOTA - used on BS for crusing drones | We focus on RIS for landing / takeoff in deep Canyons 
- Mapping Physical "blind spots" to reliabilty outage of URLLC
"If a drone is landing at 5 m/s in an urban canyon, the phase of the reflected signal (RIS at x,y position) changes in milliseconds."

---
# Foundation

Channel Impulse response (with mobility error) -> Channel State information (CSI) with estimated error
CSI -> SINR using effective channel gain -> using shannon or PPV bounds for BLER 

---
# Methods/Implementation 

Physical level: Sionna CIR (tested)
Link level: Finite blocklength mapping (tested)
Network level: RLNC block (N,K) Mapping (yet to test)

Scenario: Frankfurt Urban model - One drone - one 5G basestation and surrounding radio map with nulls/black spots

Simulation setup:
1. Baseline Without RIS
2. With RIS on the Drone (does this add value - weight,scope)
3. With RIS on facade (does height matter?, what other properties)



---
# Results (tentative idea)

- Mathematical limit of drone velocity to RIS update latency for a landing scenario
- Create a safe landing space volume by integrating RIS effectively


---
# Questions

1. Makes sense? 
2. What is Real-Time here for CSI?  CSI might be outdated as drone is constantly mobile?
2. Details on RIS phase updates - useful?
3. FEM not included. Still Novelty seen?

