
### GOAL 1 : COMMUNICATION SYSTEM 
It is completely normal for PhD students to feel a "knowledge decay" in areas outside their immediate research niche. Since you have a Master’s background, you don’t need a deep dive into the math—you need a **conceptual refresher** to reconnect the physical layer (Antennas/RF) to the logical layers (Coding/Protocols).

Here is your 30-day "Back to Basics" plan, designed for 1 hour a day.

---

## **Phase 1: The Physical Layer & RF (Days 1–10)**

_Focus: How signals move through space._

|**Day**|**Topic**|**Key Concepts**|**Resource**|
|---|---|---|---|
|**1-2**|**Antenna Fundamentals**|Radiation patterns, Directivity, Polarization|[Antenna-Theory.com](https://www.antenna-theory.com/) (Best site for intuition)|
|**3-4**|**Antenna Gain & Aperture**|$G = \eta D$, Effective area, Isotropic radiators|[All About Circuits - Antenna Gain](https://www.google.com/search?q=https://www.allaboutcircuits.com/technical-articles/understanding-antenna-gain/)|
|**5-6**|**RF Propagation**|Free space path loss (Friis), Fading, Multipath|[NIST RF Propagation Basics](https://www.google.com/search?q=https://www.nist.gov/ctl/rf-propagation)|
|**7-8**|**Impedance & Matching**|VSWR, Smith Charts, Maximum power transfer|[Keysight: RF Fundamentals](https://www.google.com/search?q=https://www.keysight.com/us/en/assets/7018-06337/white-papers/5992-3212.pdf)|
|**9-10**|**Link Budgets**|Noise floor, SNR, $P_{rx} = P_{tx} + G_{tx} + G_{rx} - L$|[IEEE Explorer/Tutorials on Link Budget](https://www.google.com/search?q=https://ieeexplore.ieee.org/abstract/document/9040336)|

---

## **Phase 2: Signal Theory & Nyquist (Days 11–15)**

_Focus: Converting analog reality to digital data._

- **Day 11:** **Sampling Theorem:** Nyquist-Shannon, aliasing, and the sinc function.
    
- **Day 12:** **Quantization:** SQNR (Signal-to-Quantization-Noise Ratio) and bit depth.
    
- **Day 13:** **Baseband Pulse Shaping:** Intersymbol Interference (ISI) and Raised Cosine filters.
    
- **Day 14:** **Digital Modulation (Basics):** ASK, FSK, PSK, and Constellation diagrams.
    
- **Day 15:** **QAM & Bandwidth Efficiency:** How we pack more bits into the same Hz.
    
- **Top Resource:** [DeepSig: ML and Signal Processing](https://www.google.com/search?q=https://www.deepsig.ai/resources) or **MIT OpenCourseWare (6.02 Digital Comm)**.
    

---

## **Phase 3: Channel Coding & Information Theory (Days 16–22)**

_Focus: Dealing with noise and errors._

- **Day 16:** **Shannon’s Capacity:** The $C = B \log_2(1 + SNR)$ limit.
    
- **Day 17:** **Linear Block Codes:** Parity bits, Hamming distance.
    
- **Day 18:** **Cyclic Codes & CRC:** How hardware detects errors quickly.
    
- **Day 19:** **Convolutional Codes:** Viterbi decoding and trellis diagrams.
    
- **Day 20:** **Modern Coding (LDPC/Turbo):** The heavy hitters of 5G and SatCom.
    
- **Day 21:** **MIMO Basics:** Spatial multiplexing and diversity gain.
    
- **Day 22:** **OFDM:** Why we use orthogonal subcarriers (LTE/Wi-Fi).
    
- **Top Resource:** [Complexity Explorer - Information Theory](https://www.complexityexplorer.org/) or **3Blue1Brown (Information Theory series)**.
    

---

## **Phase 4: Protocols & The Stack (Days 23–30)**

_Focus: Moving from a link to a network._

- **Day 23:** **MAC Layer:** ALOHA, CSMA/CA vs. CSMA/CD.
    
- **Day 24:** **Data Link Layer:** Framing, Flow control (Stop-and-wait, Sliding window).
    
- **Day 25:** **The OSI vs. TCP/IP Model:** Encapsulation and headers.
    
- **Day 26:** **IP Addressing & Routing:** IPv4/v6, BGP, OSPF basics.
    
- **Day 27:** **TCP vs. UDP:** Congestion control and reliability.
    
- **Day 28:** **Higher Layers:** TLS/SSL (Security), HTTP/MQTT (IoT applications).
    
- **Day 29:** **SDN & NFV:** How modern PhD research views networking today.
    
- **Day 30:** **Final Synthesis:** Trace a packet from an antenna to a web server.
    
- **Top Resource:** [Computer Networking: A Top-Down Approach (Online Resources)](https://gaia.cs.umass.edu/kurose_ross/online_lectures.htm).
    

---

### **Recommended Quick-Reference Materials**

1. **Video:** [The Engineering Mindset (YouTube)](https://www.google.com/search?q=https://www.youtube.com/%40TheEngineeringMindset) — Excellent for RF and Antenna intuition.
    
2. **Interactive:** [Falstad’s Circuit Simulator](https://www.falstad.com/circuit/) — Use the "Antenna" or "Transmission Line" presets to visualize waves.
    
3. **The "Bible":** _Digital Communications_ by John Proakis (Just skim the summaries/introductions of each chapter).
    

GET IT DONE BY 5th March - Add number everyday

### GOAL 2: PROTOCOL AND ARCHITECTURE 



### GOAL 3: NETWORK CODING 
