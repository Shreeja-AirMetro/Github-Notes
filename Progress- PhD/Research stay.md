Australia, South Korea, and Singapore are global leaders in this field, each with a distinct "flavor" of research that aligns perfectly with your work on **heterogeneous multi-link communication**.

In 2026/2027, these regions are shifting from "How do we connect?" to "How do we stay connected during link failure?"—which is the heart of your research.

---

## 1. Australia: The "Regulatory & Corridors" Experts

Australia is currently a global testbed for "True BVLOS" because of its vast, unpopulated land. Research here is heavily focused on **long-range link switching** (LTE to Satellite).

- **Queensland University of Technology (QUT):** Home to the **Australian Centre for Robotics**. They lead the **ADAC (Digital Airspace Characterisation)** project.
    
    - **The Focus:** Mapping "air risk" in real-time. Their work on heterogeneous links focuses on **link-aware path planning**—where the drone changes its flight path to stay within 5G or Satellite coverage.
        
- **University of Sydney:** They have a strong focus on **6G Non-Terrestrial Networks (NTN)**.
    
    - **Researcher to Watch:** **Prof. Branka Vucetic**. Her team works on **URLLC (Ultra-Reliable Low-Latency)** which is essential for your multi-link switching logic.
        
- **Why approach them:** If your simulator data focuses on **long-distance corridors** or **rural-to-urban transitions**, Australia is the best place to validate it.
    

---

## 2. South Korea: The "K-UAM" & High-Density Hub

South Korea is arguably the most aggressive in deploying **Urban Air Mobility (UAM)**. By late 2026, they plan to have actual air taxi routes operational in Seoul.

- **KAIST (Korea Advanced Institute of Science and Technology):**
    
    - **Researcher:** **Prof. Hyunchul (David) Shim**. He is a pioneer in autonomous flight. His lab works on **resilient C2 links** that can survive the intense interference of a city like Seoul.
        
- **UNIST / Kwangwoon University:** Recently made headlines in 2025/2026 for **433MHz + 5G hybrid communication**.
    
    - **The Innovation:** They are developing hardware that uses low-frequency (433MHz) for long-range "heartbeat" signals and 5G for high-bandwidth data. This is exactly the **heterogeneous multi-link** model you are simulating.
        
- **Why approach them:** If your data focuses on **urban interference** or **high-density drone traffic**, South Korea’s labs are world-class.
    

---

## 3. Singapore: The "Smart Port" & Maritime BVLOS Leader

Singapore’s research is unique because it focuses on **Maritime BVLOS** (Ship-to-Shore) and **tropical weather resilience**.

- **Nanyang Technological University (NTU):**
    
    - **Lab:** **Air Traffic Management Research Institute (ATMRI)**.
        
    - **Key Focus (2026):** They are working on **NOMA (Non-Orthogonal Multiple Access)** for multi-UAV communications. This allows many drones to share the same multi-link infrastructure without "clobbering" each other's signals.
        
- **SUTD (Singapore University of Technology and Design):**
    
    - **Project:** **Future Communications Research & Development Programme (FCP)**.
        
    - **Specifics:** They recently released a **Digital Twin for LEO Mega-Constellations** (Feb 2026). If your simulator includes **Starlink-style satellite links**, SUTD is the primary research partner in Asia.
        
- **Why approach them:** If your research involves **Maritime, Port Logistics,** or **Satellite-Integrated 6G**, Singapore is the leader.
    

---

## ⚖️ Summary Comparison for Your Research Stay

|**Region**|**Primary Strength**|**Perfect for your data if...**|
|---|---|---|
|**Australia (QUT)**|Long-range Corridors|You have data on **switching between 5G and Satellite** over hundreds of km.|
|**South Korea (KAIST)**|Urban Reliability|You have data on **C2 link stability** in "noisy" city environments.|
|**Singapore (NTU/SUTD)**|Maritime & 6G|You have data on **LEO Satellite integration** or ship-to-shore links.|

### **My Recommendation for you:**

Since you are working on **heterogeneous multi-link communication**, the **K-UAM (South Korea)** ecosystem is likely the most relevant. They are currently the only ones building the physical "highways" in the sky that require the exact link-switching logic you are simulating.

**Would you like me to:**

1. Find the **direct lab contact information** for Prof. Hyunchul Shim (KAIST) or the NTU ATMRI team?
    
2. Help you **re-format your simulator paper's abstract** to appeal specifically to the "Maritime" or "Urban" needs of these universities?

---

Since your topic specifically focuses on **heterogeneous multi-link communication** (LTE, 5G, Satellite, and Mesh) for BVLOS, a research stay at a university with a dedicated **large-scale testbed** is your best move.

By late 2026/early 2027, you will have your simulator data; what you need then is **validation against real-world radio environments** or access to **advanced hardware-in-the-loop (HIL) facilities**.

---

## 1. Top Recommended Professors for Research Stays

### **Option A: The Testbed Leader (USA)**

- **Professor:** **Ismail Guvenc** (North Carolina State University)
    
- **Lab:** **AERPAW** (Aerial Experimentation and Research Platform for Advanced Wireless).
    
- **Why approach him?** Guvenc leads one of the world's only city-scale 5G/6G UAV testbeds. His work is explicitly about **heterogeneous links** (cellular + custom radio).
    
- **Relevance for 2027:** By then, AERPAW will likely be testing integrated satellite-to-UAV links. He is very open to international visitors if you bring a strong simulation model that needs real-world data comparison.
    

### **Option B: The Standardization Expert (USA)**

- **Professor:** **Kamesh Namuduri** (University of North Texas)
    
- **Why approach him?** If your research leans toward **how to manage multiple links safely** (C2 protocols), Kamesh is the chair of the IEEE P1920.2 standard.
    
- **Relevance for 2027:** He focuses on the "Network of Networks" (Ad-hoc + Cellular). A stay here would give your paper a "Standardization" edge, which is highly valued in German academia.
    

### **Option C: The O-RAN & 6G Pioneer (USA/Italy)**

- **Professor:** **Tommaso Melodia** (Northeastern University, Boston)
    
- **Lab:** **WIoT** (Institute for the Wireless Internet of Things) / **Colosseum** (The world’s largest wireless network emulator).
    
- **Why approach him?** His lab uses **Open RAN (O-RAN)** to manage heterogeneous traffic. If your simulator looks at how a network "slices" data for a drone, this is the place.
    
- **Note:** He also has strong ties to **Università di Roma Tor Vergata** (Italy) if you prefer to stay within Europe.
    

### **Option D: The Hardware & URLLC Specialist (Taiwan)**

- **Professor:** Look into the **Communications Engineering faculty** at **National Yunlin University (YunTech)**.
    
- **Why approach them?** As we discussed, they are masters of **HIL (Hardware-in-the-Loop)**.
    
- **Relevance for 2027:** If you want to put your simulator logic into an actual Taiwanese-made drone flight controller, this is the best technical stay.
    

---

## 2. Strategic Timeline for Your Approach

Since you are planning for a **1–2 month stay** in late 2026 or 2027:

- **Now (Early 2026):** Continue your simulator development. Ensure your code is on GitHub and your first "Open Source Simulator" paper is published (this is your "ticket" to a research stay).
    
- **6 Months Before (Mid-2026):** Send your initial "Inquiry of Interest" email. Mention that you have a functional simulator and want to **validate your multi-link switching algorithms** using their specific testbed (AERPAW, Colosseum, etc.).
    
- **The "Germany" Advantage:** Use programs like **DAAD** (German Academic Exchange Service) or **Erasmus+** (if staying in Europe) to secure funding. Professors are much more likely to say "Yes" if you have your own travel/living stipend.
    

---

## 3. Comparison of Stays

|**Destination**|**Primary Value**|**Best if your research is...**|
|---|---|---|
|**NC State (Guvenc)**|Real-world field data.|Focusing on physical signal behavior in cities.|
|**Northeastern (Melodia)**|Software-defined networking.|Focusing on AI-driven link switching/slicing.|
|**YunTech (Taiwan)**|Hardware validation.|Focusing on flight controller response to link loss.|
|**UNT (Namuduri)**|Policy & Standards.|Focusing on regulatory compliance for BVLOS.|

### **How can I help you further?**

Would you like me to:

1. **Draft a "Research Stay Proposal"** template specifically for Prof. Guvenc or Prof. Melodia?
    
2. Search for **DAAD funding deadlines** for 2027 research stays?
    
3. Help you **structure the "Future Work" section** of your current paper to pave the way for this stay?
4. 