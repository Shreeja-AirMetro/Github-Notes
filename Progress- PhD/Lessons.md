Lessons from workshop 
- Aßmann -map abstract research findings  to application 
- Be clear about goals target question and map the path 


### 23 months until Oct 2027 
Nov 2027 Begin organizing thesis and writing Dec 2027 - Submit the thesis 

**Until Dec 2025** 

stabilize scope & reproduce baselines

Until Aug 2026 
- Design your core algorithm family (see section B). Implement these algorithms in OMNeT++:
    
    1. Adaptive multipath scheduler (importance-aware; telemetry prioritized).
    2. Network coding layer (systematic RLNC / rateless + selective retransmission).
    3. Availability-aware resource optimizer (predictive: short-term availability estimation + convex optimization for path allocation).
    4. Edge-assisted computation placement for S&A data (locally vs cloud) with SLA constraints.
        
- Simulation experiments: compare Baseline vs (1) vs (1+2) vs (1+2+3) vs (1+2+3+4). Run across mission profiles and channel models (low-altitude aerial channel, ground multipath, LEO latency model).
- Begin drafting a workshop paper (6–8 pages) describing system model and first simulation results.
-  Port the best simulation variants to your testbed: PX4 autopilot + WiFi mesh radios (e.g., Ubiquiti/ath9k or dedicated 802.11n/ac modules), 5G modem (commercial USB modem or dev kit), and LEO emulator (see testing notes below).
- Run bench tests (lab): measure latency, packet loss, handover time between WiFi mesh nodes (air-to-air relay), 5G uplink/downlink performance under interference injection, and satellite link emulation (long RTT, high jitter).
- Conduct controlled flight tests in a safe range (short BVLOS tests under waiver or in collaboration with a test range). Focus on telemetry/control continuity and handover events.
- Submit the workshop paper to a mid-2027 UAV/communications workshop or ICUAS short paper. ICUAS has a specific UAV audience — good place for system/demos.
- - Run extended multi-scenario trials (urban + rural) and produce a cleaned dataset (flight logs, timestamps, link traces, S&A latency events). Make dataset FAIR (clear format, README, sample scripts).
- Perform statistical analysis: compute availability CDFs, end-to-end latency percentiles, mission success probability under interference, and sensitivity analysis vs number of air relays and 5G coverage.


# Algorithms & variants to design and test (concrete)

You should implement a family of algorithms, structured so each incremental addition gives measurable gains:

### 1) **Baseline**

- Simple path selection: first-available path; UDP, no coding. (For comparison.)
    
### 2) **Priority-aware multipath scheduler** (essential)

- Assign weights to traffic classes (telemetry/control highest).
- Use weighted fair multipath allocation across (WiFimesh, 5G, LEO).
- Metrics: 99.9th percentile latency, control packet delivery ratio.
    

### 3) **Systematic network coding layer**

- Implement _systematic RLNC (random linear network coding)_ or Raptor/Q-rateless codes to mask intermittent losses — apply across multiple physical paths (coding across 2–3 paths).
- Compare to standard ARQ and FEC.
- Metrics: goodput, decoding delay, extra overhead.
    

### 4) **Predictive availability estimator + optimizer** (core novelty candidate)

- Short-term link availability predictor (time series / lightweight ML: ARIMA / LSTM / simple Kalman) that uses recent link metrics (RSSI, packet loss, handover events) to predict next-second availability.
- Use predicted availabilities in a constrained optimization that maximizes telemetry delivery probability subject to sending rate / energy constraints (formulated as convex optimization or MIP; use fast heuristics if needed).
- Compare: oracle (perfect prediction), predictor + optimizer, optimizer without prediction.
    

### 5) **Cross-layer scheduling with edge offload**

- Decide when to offload S&A or state estimation to edge node (low latency decision) vs local processing; treat comms availability as stochastic and include decision latency into safety margin.
- Formulate as an MDP and solve via approximate dynamic programming or RL (simple Q-learning) for proof-of-concept.

### 6) **Opportunistic LEO fallback & sat comm integration**

- Implement a LEO fallback module that adapts encoding rate and uses prioritized telemetry; emulate LEO latency (e.g., 40–200 ms for LEO depending on routing) and contact windows.
- Test combined strategy: WiFimesh primary, 5G secondary, LEO tertiary, with coding across available paths.
    

### 7) **Resource aware network coding**

- Adaptive code rate based on available bandwidth and latency; e.g., increase redundancy when predicted availability low.
- Evaluate energy versus reliability tradeoffs.


**Baseline comparisons**: ARQ-only, ARQ+MPTCP, FEC fixed rate, RLNC static, RLNC adaptive with prediction.

# OMNeT++ simulation design → testbed experiments

**OMNeT++ (simulation)**

- Use INET/INET4/INETMANET modules for WiFi mesh, add LTE/5G modules (available extensions) and implement link models for aerial UE (altitude-dependent pathloss). Build scenarios: urban canyon, suburban open, rural long backbone.
    
- Run large-scale Monte-Carlo trials (≥100 runs per scenario) to produce confident CIs on percentiles. Automate with scripts.
    

**Testbed (real)**

- Flight stack: PX4 or ArduPilot with companion computer (Raspberry Pi / NVIDIA Jetson) to run scheduler/encoder.
    
- WiFi mesh: airborne nodes use commodity WiFi modules with external antennas — measure antenna patterns at altitude. Implement air-to-air relay using ad-hoc/mesh mode.
- 5G: use a vendor dev kit or USB modem that can attach to a test 5G cell (private 5G if available) or emulate link with traffic shaper if no real 5G accessible.
- LEO: if no real LEO modem, emulate sat link using an isolated RTT-shaping proxy and jitter/loss profile reflecting sat contact windows. Optionally use a low-rate Iridium/Globalstar dev kit for real sat link but that’s often costly.
- Instrumentation: synchronized timestamps (GPS time), packet capture (tcpdump), and logging of system state and S&A decisions.
    

**Validation steps**

1. Lab bench tests (latency, packet loss under controlled interference).
    
2. Tethered flight tests (if allowed) to validate WiFi mesh handover.
    
3. Short BVLOS flights (use test range / waiver); collect full logs.
    
4. Extended pilots in collaboration with partner (if internship gives access).


---

### Some ideas 

PhD is compounding on results 


