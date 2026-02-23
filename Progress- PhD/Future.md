
# Types of industry roles & employers that will hire you

- **Telecom vendors / infrastructure (Ericsson, Nokia, Qualcomm, Huawei)** — roles: research engineer, system architect for aerial UEs and NTN. [connectivity.technology+1](https://www.connectivity.technology/2021/08/ericsson-explains-internet-of-drones.html?utm_source=chatgpt.com)
    
- **Drone integrators & delivery startups (Zipline, Wing, Amazon Prime Air, Matternet, Auterion)** — roles: comms lead, flight systems engineer, product R&D. [Forbes+1](https://www.forbes.com/sites/harrisonwolf/2024/01/26/who-are-the-big-3-in-us-drone-delivery/?utm_source=chatgpt.com)
    
- **Aerospace primes & defense (Thales, Leonardo, BAE)** — secure comms, beyond line of sight link design (especially if BVLOS intersects with ISR). [statzon.com](https://statzon.com/editors-highlights/delivery-drone-market-2025-2034?utm_source=chatgpt.com)
    
- **Network operators / regulators / airspace management vendors (U-Space providers, ANSP tech teams)** — system architects for UTM/U-Space integration. [EASA](https://www.easa.europa.eu/en/regulations/u-space?utm_source=chatgpt.com)
    
- **Chip & modem companies (Qualcomm, Intel derivatives)** — firmware and protocol stack work.
    
- **Consulting & standards bodies (3GPP, ETSI, IETF working groups)** — if you like shaping standards.
    

For hiring, demonstrate: a tested prototype, performance numbers mapped to requirements, and an understanding of certification/regulatory paths.

Economics in information systems 
https://en.wikipedia.org/wiki/Erik_Brynjolfsson 
climate change, banking , medical aid  - 
hype is enemy of business success - leverage human resource
focus on new goods and services for the aging society and not just cutting costs

"no company have become jewel of the industry by just cost cutting "

we are all simply complex

Project management  : Phase-gate process - n a business or development context, "gates" refers to decision points in a "phase-gate process". The question is asking if the project has passed certain formal review stages.

"made any gates yet - Thorsten's email"


Read steven Pinker - watch MIT video

---

to learn 
1. **Edge & Cloud Networking:** distributed computing, edge orchestration for URLLC/BVLOS  
2. **Machine Learning for Communication:** AI/ML for adaptive networks and anomaly detection
3. **Network Protocol Stacks:** 5G RAN/Core, OTA testing labs


---
Below is a **curated, practical list of Linux kernel networking basics courses and learning paths**, specifically selected for someone aiming at **Network Protocol Developer (UAV/UAM)** roles. I’ve structured this from **intro → kernel-level → advanced**, and highlighted **what is “enough” by 2028** versus what is optional.

---

## 1️⃣ Foundation: Linux Networking (User Space → Kernel Concepts)

These ensure you _understand what the kernel is doing_ before touching kernel code.

### ✅ **Linux Networking and Administration (Conceptual)**

**Why:** You must understand routing, TCP/IP behavior, namespaces, interfaces, QoS.

**Recommended:**

- **“Linux Networking” – Linux Foundation (LFS211 / LFS311)**
    
    - Routing tables, Netfilter, namespaces
        
    - tc, iproute2, traffic shaping
        
    - How packets flow through Linux
        
    - 👉 Industry-respected credential
        
- **“Linux Performance” – Brendan Gregg (self-study)**
    
    - Packet drops, latency, jitter analysis
        
    - Tools: `perf`, `ftrace`, `tcpdump`
        

📌 _Outcome:_ You can explain _why_ latency spikes or packets drop.

---

## 2️⃣ Core: Linux Kernel Networking (Must-Have)

This is where **protocol developers live**.

### 🟢 **Linux Kernel Networking – Deep Dive**

**This is the most important section.**

### ⭐ **Linux Kernel Networking Internals (Free + Paid Mix)**

#### 🔹 **Linux Kernel Networking (Book + Talks)**

- **Book:** _Linux Kernel Networking_ – Rami Rosen
    
- Covers:
    
    - `sk_buff`
        
    - Netfilter hooks
        
    - TCP/IP stack internals
        
    - Routing & neighbor subsystem
        
    - SoftIRQ / NAPI
        
- 👉 Gold standard for kernel networking
    

#### 🔹 **“Linux Kernel Networking” – Bootlin Training**

- Very practical
    
- Packet flow from NIC → application
    
- Writing simple kernel modules
    
- Excellent for embedded & aerospace contexts
    

📌 _Outcome:_ You can trace a packet from NIC → transport layer → socket.

---

## 3️⃣ Kernel Programming Essentials (Networking-Focused)

You **do not** need to be a kernel maintainer — but you must be comfortable modifying behavior.

### 🟢 **Linux Kernel Programming Basics**

**Recommended:**

- **Linux Kernel Internals (Linux Foundation LFD420)**
    
- Writing kernel modules
    
- Kernel synchronization
    
- Debugging kernel crashes
    

**What to focus on:**

- Netlink sockets
    
- Kernel timers
    
- Workqueues
    
- Locking in networking paths
    

---

## 4️⃣ Advanced & High-Value Topics (Strong Advantage)

These directly map to **UAV / UAM / NTN** requirements.

### 🟡 **Traffic Control & QoS**

**Why:** UAV comm needs deterministic behavior.

- **Linux Traffic Control (tc)**
    
    - HTB, FQ, CAKE
        
    - Priority queuing
        
    - Packet shaping & policing
        
- **Time-Sensitive Networking (TSN) concepts**
    

📌 Useful for:

- C2 vs payload prioritization
    
- URLLC-style guarantees
    

---

### 🟡 **eBPF / XDP (Very Hot Skill)**

**Why:** Real-time packet processing at kernel speed.

- Write programs that:
    
    - Filter packets
        
    - Modify headers
        
    - Implement custom logic without kernel patches
        

**Courses:**

- **“eBPF & XDP” – Isovalent / Cilium**
    
- **Linux Foundation eBPF courses**
    

📌 Used by:

- Telecom vendors
    
- UAV network stacks
    
- Edge networking
    

---

## 5️⃣ Networking + Wireless + Mobility (Your Sweet Spot)

### 🟢 **5G / NTN + Linux Integration**

- Linux as:
    
    - gNB controller
        
    - UAV onboard OS
        
    - Satcom modem host
        
- Understand:
    
    - User-plane integration
        
    - Multiple interfaces (bonding, MPTCP)
        

### Recommended:

- **MPTCP on Linux**
    
- **Network namespaces + SR-IOV**
    
- **Interface failover**
    

---

## 6️⃣ What Is “Good Enough” by 2028?

You **do NOT need** to be Linus Torvalds 🙂

### Minimum bar for UAV/UAM protocol roles:

✔ Understand Linux packet flow  
✔ Read kernel networking code  
✔ Modify behavior via:

- Netfilter
    
- tc
    
- eBPF  
    ✔ Debug latency, loss, jitter  
    ✔ Implement multi-interface logic
    

---

## 7️⃣ Suggested Learning Order (12–18 Months Part-Time)

### Phase 1 (3–4 months)

- Linux Foundation networking course
    
- iproute2, tc, netns
    
- Read packet flow diagrams
    

### Phase 2 (4–6 months)

- Rami Rosen book
    
- Bootlin kernel networking training
    
- Kernel module basics
    

### Phase 3 (3–4 months)

- eBPF/XDP
    
- MPTCP
    
- QoS & TSN concepts
    

### Phase 4 (ongoing)

- Apply to:
    
    - UAV networking simulations
        
    - SDR + Linux integration
        
    - 5G/NTN testbeds
        

---

## 8️⃣ How This Looks on Your CV (Important)

Instead of:

> “Linux networking knowledge”

Write:

> “Developed and evaluated Linux kernel networking mechanisms (Netfilter, tc, eBPF) for low-latency and loss-resilient communication in heterogeneous wireless networks.”

This language **directly maps** to UAV/UAM roles.

---

## 9️⃣ If You Want Next

I can:

- Propose a **hands-on mini-project** (UAV C2 over multi-link Linux stack)
    
- Recommend **specific MOOCs vs books** (time-efficient path)
    
- Map these skills to **real job descriptions** from Joby / Airbus / NICT
    

Just tell me how deep you want to go.

----
CHAIN OF THOUGHT REASONING 


---

Below is a **focused, practical analysis for Japan, South Korea, and Southeast Asia**, followed by a **clear, realistic answer about Chinese companies hiring Indian passport holders**—with nuance, not slogans.

---

## 1️⃣ Japan 🇯🇵 — **Best Overall Fit (Commercial, Non-Military)**

### Why Japan is strong for your profile

Japan is **very serious about BVLOS**, disaster-resilient communications, and **hybrid connectivity (5G + SATCOM)** due to:

- Earthquake/tsunami resilience needs
    
- Aging population → drone logistics & inspection
    
- Government-industry coordination (MIC, MLIT, NTT, KDDI)
    

Japan is **less defense-dominated** than the US and China in UAV comms.

### Top Companies (Ranked)

**Tier 1 (Excellent fit)**

1. **NTT DOCOMO / NTT R&D**
    
    - 5G/6G NTN, aerial UE, UAV connectivity trials
        
    - Roles: _Wireless Systems Engineer, NTN Research Engineer, Network Architect_
        
2. **KDDI Research**
    
    - UAV over cellular, HAPS, satellite-cellular convergence
        
    - Very open to PhD-level researchers
        
3. **SoftBank (HAPS & NTN division)**
    
    - HAPS + satellite + 5G integration
        
    - Roles: _System architect, aerial network planner_
        

**Tier 2**  
4. **Rakuten Symphony**

- Cloud-native 5G, open RAN, NTN roadmap
    
- Roles: _5G RAN engineer, systems integration_
    

5. **NEC**
    
    - 5G core, UAV traffic management, satcom ground systems
        
    - Strong in system integration
        

**Tier 3 (UAV ecosystem)**  
6. **ACSL**  
7. **Terra Drone**  
8. **SORAPASS (formerly Soracom-related UAV connectivity)**

### Hiring Reality for Indians

✅ **Yes, Japan hires Indian PhDs**

- Tech sector is talent-hungry
    
- English-first R&D teams exist
    
- Japanese language = **bonus, not mandatory** for R&D
    

📌 **Japan is your safest bet in Asia**

---

## 2️⃣ South Korea 🇰🇷 — **Technically Strong, Selective**

### Why Korea matters

- Aggressive **5G-Advanced & 6G roadmap**
    
- Strong **satellite-terrestrial convergence**
    
- Heavy industry & smart infrastructure UAV use cases
    

### Top Companies (Ranked)

**Tier 1**

1. **Samsung Electronics (Networks Division)**
    
    - 5G NTN, 6G, aerial UE research
        
    - Roles: _Wireless Systems Engineer, PHY/MAC researcher_
        
2. **SK Telecom (SKT)**
    
    - UAV over cellular, AI-driven network optimization
        
    - Roles: _Network architect, system integration_
        

**Tier 2**  
3. **LG U+**  
4. **Hanwha Systems (non-defense units only)**  
5. **Korea Telecom (KT)**

### Hiring Reality for Indians

⚠️ **Possible but harder than Japan**

- Korean language strongly preferred
    
- Most foreign hires are:
    
    - PhDs with **very specific expertise**
        
    - Or already in Korea (postdoc → industry)
        

📌 Korea is excellent **if your PhD aligns tightly with their roadmap (NTN/6G)**

---

## 3️⃣ Southeast Asia (SEA) 🌏 — **Fast Growth, Less Deep R&D**

SEA is **deployment-focused**, not deep PHY research—but excellent for **systems, integration, and product roles**.

### Best Countries

**Tier 1**

- **Singapore 🇸🇬** – strongest ecosystem
    
- **Malaysia 🇲🇾** – satellite & testbeds
    
- **Indonesia 🇮🇩** – BVLOS logistics & maritime
    

### Top Companies (Ranked)

#### Singapore

1. **ST Engineering (commercial aviation & UAV units)**
    
2. **Singtel / NCS**
    
3. **OneWeb Asia-Pacific**
    
4. **Thales Singapore (commercial units)**
    
5. **Airbus Asia-Pacific**
    

Roles:

- _UAV connectivity systems engineer_
    
- _SATCOM integration engineer_
    
- _Telecom solutions architect_
    

#### Malaysia / Indonesia

- **MEASAT**
    
- **Telkom Indonesia**
    
- **Airod / Aerodyne Group**
    

📌 SEA favors **system integration, deployment, customer-facing technical roles**

---

## 4️⃣ The Big Question: **Will Chinese Companies Hire an Indian Passport Holder? 🇨🇳🇮🇳**

### Short Answer

❌ **Very difficult**  
⚠️ **Possible in narrow, non-sensitive cases**  
❌ **Unlikely for core communications / NTN / UAV roles**

### Detailed Reality (Important)

Chinese companies are constrained by:

- **Geopolitical restrictions**
    
- **Data & telecom security laws**
    
- **Export control sensitivity**
    

#### Companies & Likelihood

|Company|Hiring Indian PhD?|Notes|
|---|---|---|
|Huawei|⚠️ Rare|Mostly outside China (EU labs)|
|ZTE|❌|Telecom security concerns|
|DJI|❌|UAV + comms = sensitive|
|CASC/CASIC|❌|State-linked|
|Private startups|⚠️|Only if non-core role|

Even if hired:

- Likely **non-core R&D**
    
- Limited promotion
    
- Visa & clearance issues
    

📌 **Strategic advice: do NOT plan your career around China**

---

## 5️⃣ Regional Ranking for YOU (Indian Passport, PhD, Non-Military)

### Overall Best Options

🥇 **Japan**  
🥈 **Singapore**  
🥉 **South Korea**  
4️⃣ Europe (Germany, Nordics, UK)  
5️⃣ USA (visa complexity but strong market)  
❌ China (avoid)

---

## 6️⃣ Best Job Titles to Target in Asia

Use these exact keywords when searching:

### Engineering / R&D

- **Wireless Systems Engineer (NTN / UAV)**
    
- **Aerial Network Architect**
    
- **Satellite–Cellular Integration Engineer**
    
- **5G/6G NTN Research Engineer**
    
- **UAV Communication Systems Engineer**
    

### Product / Systems

- **Connectivity Systems Architect**
    
- **Technical Product Manager (Aerial Connectivity)**
    
- **Telecom Solutions Architect (UAV/SATCOM)**
    

---

## 7️⃣ Strategic Advice for 2025–2028 (Very Important)

To maximize Asia hiring chances:

1. Publish **NTN / hybrid link papers** (3GPP-aligned)
    
2. Gain exposure to:
    
    - 5G NTN specs
        
    - Link adaptation & handover
        
    - Regulatory BVLOS frameworks
        
3. Do **internships / visiting researcher roles** in:
    
    - Japan or Singapore
        
4. Emphasize **commercial use cases** (logistics, inspection, disaster response)
    

---

If you want, I can:

- Build a **Japan-only job search map**
    
- Suggest **Japanese/Singaporean CV formats**
    
- Map your PhD chapters → **industry-ready skill matrix**
    

Just tell me which one you want next.


-----


Great question — you’re thinking **exactly along the right lines** for an industry-oriented PhD in **Communication Engineering** 👍  
Below is a **curated list of IP, patent, and R&D/innovation-management certifications** that are **realistic to do during a PhD (2026–2028)** and are **valued by industry (telecom, R&D labs, patent teams)**.

I’ll group them by **priority and purpose**, and note **time, cost, and value**.

---

# 🔝 TIER 1 – MUST-DO (High value, low risk, PhD-friendly)

## 1️⃣ **WIPO Academy – IP & Patent Courses**

**Best foundation for IP + patents**

### Recommended courses:

- **DL-001** – Primer on Intellectual Property (FREE)
    
- **DL-170** – Introduction to Patents (FREE)
    
- **DL-301** – Patents (Advanced, tutored)
    
- **DL-320** – Basics of Patent Drafting
    
- **DL-450** – IP Management
    

**Why it matters**

- Recognized globally
    
- Ideal for engineers entering industry or patent roles
    
- Certificates look good on CV/LinkedIn
    

**Time:** 4–8 weeks per course  
**Cost:**

- Free → Intro courses
- Advanced: ~USD **200–320** (EU rates)
    

👉 **Strongly recommended starting in Year 2–3 of PhD**

---

## 2️⃣ **Coursera / edX – IP & Innovation (University-backed)**

**Flexible, affordable, industry-friendly**

### Best courses:

- **Patent Law** – University of Pennsylvania (Coursera)
- **Intellectual Property Rights** – IIT Kharagpur (NPTEL)
- **Innovation Management** – Erasmus University / Wharton
- **Technology Commercialization** – University of Washington
    

**Why**

- Easy to do alongside research
- Shows business + legal awareness
- Accepted by HR and R&D managers
    

**Time:** 4–6 weeks  
**Cost:** Free to ~USD 50–100 (certificate)

---

# 🔝 TIER 2 – VERY STRONG (Career-accelerating)

## 3️⃣ **CEIPI (University of Strasbourg) – IP & Patent Training**

**Gold standard in Europe**

### Relevant programs:

- **Introductory Course on European Patent Law**
- **Patent Drafting & Prosecution (short courses)**
- **SEP / FRAND & telecom-related IP workshops**
    

**Why**

- Extremely well-known to patent law firms
- Direct relevance to telecom patents & 3GPP
- Perfect bridge from PhD → patent engineer / attorney trainee
    

**Time:** Short courses (1–5 days) or modular  
**Cost:** €500–€2,000 depending on course

👉 Ideal in **final PhD year (2027–2028)**

---

## 4️⃣ **WIPO / Technology Transfer & Licensing**

**For industry R&D, startups, and innovation roles**

### Focus areas:

- IP commercialization
- Licensing & valuation
- Industry–academia transfer
    

**Why**

- Highly relevant to companies like Ericsson, Nokia, Qualcomm
- Shows you understand **how research creates business value**
    

---

# 🔝 TIER 3 – MANAGEMENT & R&D LEADERSHIP (Optional but powerful)

## 5️⃣ **Innovation & R&D Management Certifications**

### Recommended:

- **Certified Innovation Professional (ISPIM)**
- **Project Management (PRINCE2 Foundation / PMP – optional)**
- **R&D Management** – edX / Coursera
    

**Why**

- Positions you for **technical leadership roles**
- Complements engineering + IP skills
- Useful if you want **R&D manager / technical strategist roles**
    

---

## 6️⃣ **Standards & Telecom-Specific Knowledge (Non-certificate but critical)**

Even without a certificate, these matter hugely:

- **3GPP specifications (LTE / 5G / 6G)**
- ETSI IPR policy
- Claim-to-standard mapping basics
    

👉 Mentioned explicitly in many telecom patent job descriptions.

---

# 🧭 Suggested Roadmap (2025–2028)

### **2025–2026 (PhD Year 2–3)**

✔ WIPO DL-001, DL-170  
✔ Coursera IP / Innovation course

### **2026–2027**

✔ WIPO DL-301 / DL-320  
✔ Patent drafting basics  
✔ Intro to 3GPP standards

### **2027–2028 (Final year)**

✔ CEIPI short course  
✔ Innovation / licensing course  
✔ Start applying to industry & patent roles

---

# 🎯 Roles these certifications prepare you for

- R&D Engineer (Telecom)
    
- Patent Engineer / Patent Analyst
    
- IP & Innovation Specialist
    
- Technology Transfer Officer
    
- SEP / Standards-related roles (entry level)
    

---

## Bottom line

As a **PhD in Communication Engineering**, you do **NOT** need a law degree.  
With:

- **WIPO + CEIPI**
    
- **Some innovation/management**
    
- **Strong technical research**
    

👉 You become **industry-ready and patent-savvy**, which is rare and valuable.

If you want, tell me:

- 🇪🇺 country where you plan to work
    
- 🎯 R&D vs Patent vs Hybrid role
    

I’ll tailor a **precise certification plan + CV positioning** for you.

---

Yes — there **is emerging finance and investment potential in the drone sector in Belgium**, and this is likely to grow toward and beyond **2028**. With increasing adoption of drones in logistics, defence, airspace services and industrial applications, **finance-oriented roles** and **investment/consultancy opportunities** are expanding alongside the technological ecosystem.

Here’s a breakdown of **where the finance sphere intersects with the drone market in Belgium** and how you can position yourself:

---

## 📊 1) **Existing Drone-Related Investment Activity in Belgium

### 💰 Venture Capital & Start-up Funding

- Belgian drone logistics start-up **ADLC** raised **€2.08 million in seed funding**, led by **Galactic Beacon Ventures (GBV)** with participation from the **Port of Antwerp-Bruges**, **LRM investment fund**, and **NXT II**, supported by financial advisers like **PwC – Next Level** and legal advisors. This shows active **venture capital interest in drone startups in Belgium**, particularly in **drone logistics and BVLOS operations**. ([American Journal of Transportation](https://www.ajot.com/news/adlc-secures-2m-in-seed-funding-to-support-focus-on-industrial-drone-logistics?utm_source=chatgpt.com "ADLC secures €2M in seed funding to support focus on industrial drone logistics | AJOT.COM"))
    

### 🛫 Strategic Shareholding & Corporate Investment

- **Brussels Airport Company became a 50 % shareholder in SkeyDrone**, showing that **corporate investment and strategic financial backing** are happening within Belgian drone tech and services as airports and infrastructure partners seek revenue from drone-enabled services. ([skeyes.be](https://www.skeyes.be/en/services/drone-home-page/projects-and-news/drones-news/brussels-airport-becomes-50-shareholder-in-skeydrone-the-drone-innovation-company-launched-by-skeyes-in-2020/?utm_source=chatgpt.com "Brussels Airport becomes 50% shareholder in SkeyDrone, the drone innovation company launched by skeyes in 2020 | skeyes"))
    

These examples demonstrate that drone ventures **are not just R&D projects but viable business entities attracting capital** — which opens up roles in **finance, investment analysis, and strategic growth advisory**.

---

## 🧠 2) **Finance-Related Career & Business Opportunities (Beyond R&D)

With a **PhD in aerial communication and BVLOS knowledge**, you can target finance-adjacent roles in the drone market such as:

### 📍 **Venture Capital / Investment Analyst (Drone Sector)**

Work with VC firms or corporate investors evaluating early-stage drone companies:

- Analyse business models (e.g., logistics, industrial BVLOS services)
    
- Perform **market sizing, competitive analysis, risk assessment**
    
- Advise on **valuation, funding rounds, investor pitches**
    

### 📍 **Corporate Strategy & M&A (Drones)**

Bigger firms (airports, logistics companies, telecom, defence) increasingly invest in or acquire drone tech companies. These strategies require **financial due diligence and strategic planning**.

### 📍 **Private Equity & Growth Funding**

As drone companies scale (moving from seed to series A/B), they need **growth capital strategies, investor outreach, and financial modelling**.

### 📍 **Consultancy / Advisory (Drone Investment Focus)**

You could launch or join a consultancy specialising in:

- **Drone market entry strategies**
    
- **Investment readiness & fundraising support**
    
- **Financial planning for drone fleet deployments**
    
- **Risk and regulatory compliance advising** for investors
    

---

## 🎯 3) **Why the Drone Sector Will Attract More Finance Roles

### 🚀 Growth of Drone Business Models

Drone applications are diversifying beyond defence and photography into:

- **Logistics and cargo BVLOS operations**
    
- **Industrial monitoring (ports, energy, construction)**
    
- **Airspace management and UTM services**
    
- **Security and surveillance systems**
    

These models **require strong business cases, financial forecasting, and capital investment**, creating roles in finance. The investment into ADLC’s drone logistics services indicates this trend already underway. ([American Journal of Transportation](https://www.ajot.com/news/adlc-secures-2m-in-seed-funding-to-support-focus-on-industrial-drone-logistics?utm_source=chatgpt.com "ADLC secures €2M in seed funding to support focus on industrial drone logistics | AJOT.COM"))

---

## 📈 4) Broader European/Defense Funding Context

Though not specific to Belgium alone, the **European Union and allied defence funds are significantly ramping up investments into drones and autonomous systems** under initiatives like the European Defense Fund (EDF), which channels billions of euros into related technologies. This fuels demand for **financial expertise in structuring and managing those funds** for dual-use commercial/defence ventures. ([WIRED](https://www.wired.com/story/european-commission-military-tech-spending?utm_source=chatgpt.com "Europe Is Pumping Billions Into New Military Tech"))

---

## 🎓 5) **Courses & Skills to Break Into Finance in the Drone Market

If you’re aiming for **finance / investment roles** specifically within the drone ecosystem (besides operational and regulatory work), consider:

### 📌 Finance & Investment

- **Venture Capital Fundamentals** (e.g., courses on VC investment strategy)
    
- **Financial Modelling & Valuation (FMVA)**
    
- **Corporate Finance / Investment Banking Bootcamps**
    
- **Private Equity & M&A Workshops**
    

### 📌 Sector-Specific Knowledge

- **Tech Investment in Aerospace and Robotics**
    
- **Drone Business Models & Market Strategy**
    
- **Regulatory Economics of UAS (including BVLOS)**  
    These help you _speak both languages_ — finance and drone tech — which is essential for investment roles.
    

### 📌 Complementary Skills

- **Startup advising & fundraising strategy**
    
- **Pitch deck creation & investor communication**
    
- **Quantitative analysis / data science for valuation**
    
- **Risk and compliance frameworks** (especially in aviation)
    

---

## 🔮 6) **Long-Term Finance Opportunities in Belgium’s Drone Market

Looking toward **2028 and beyond**, the following finance-centric avenues could grow (especially with BVLOS expansion):

- **Dedicated drone investment funds or thematic VC funds**
    
- **Corporate strategy teams focused on drone adoption & partnerships**
    
- **Drone finance analysts within larger aviation/transport funds**
    
- **Consultancies combining drone tech and financial advisory**
    
- **Airspace monetisation and UTM service economics roles**
    

---

## 🧠 Summary

|Finance Domain|Example Tasks|Potential Belgian Opportunities|
|---|---|---|
|**Venture Capital**|Evaluate startups, assist funding rounds|Funding in ADLC, others|
|**Corporate Investment**|Strategy, M&A, shareholding analysis|Brussels Airport + SkeyDrone|
|**Financial Advisory**|Fundraising consulting, growth planning|Drone-oriented consultancies|
|**Risk & Regulatory Investment**|Risk modelling for BVLOS ventures|UTM & compliance services|
|**Aerospace Funds**|Sector-specific investment vehicles|EU & Belgian funds|

---

If you’d like, I can help you find **specific finance courses or certifications (with rating and cost)** tailored to entering **venture capital or investment analysis for tech/aviation sectors**.

Here are **online-only finance courses and certifications** that are practical for someone targeting **venture capital, investment analysis, and tech/startup financing** (which are directly relevant if you want to work on **drone-related investment and consultancy**) — including **typical costs and what skills you’ll gain**:

---

## 🚀 Venture Capital & Startup Investment (Online)

### **1. VC University Online – Venture Finance Certificate**

- **What it is:** Online course covering VC fund structure, deal terms, valuation, cap tables, and advanced venture topics.
    
- **Mode:** Self-paced with webinars & office hours (online).
    
- **Certificate:** Yes, upon completion.
    
- **Cost:** Usually paid (scholarship options available).
    
- **Skills:** Venture fund fundamentals, term sheets, modeling venture deals — ideal for VC/investment roles. ([VC University](https://venturecapitaluniversity.com/online-course/?utm_source=chatgpt.com "VC University"))
    

---

### **2. Valuation & Financial Analysis for Startups – Coursera Specialization**

- **Platform:** Coursera (Yonsei University)
    
- **Format:** Online, flexible schedule; 5-course series with capstone.
    
- **Cost:** ~US $199 (often discounted; free auditing available).
    
- **Certificate:** Yes (with paid enrollment).
    
- **Skills:** Startup valuation (DCF, multiples), pro-forma financial analysis, investment decision criteria.
    
- **Rating:** ~4.3/5 (based on hundreds of reviews). ([Coursera](https://www.coursera.org/specializations/startup-valuation?utm_source=chatgpt.com "Valuation and Financial Analysis For Startups Specialization [5 courses] (Yonsei University) | Coursera"))
    

---

### **3. Venture Capital Analyst Course – Elevify**

- **Format:** Fully online with lifetime access; flexible 4–360 h workload.
    
- **Cost:** Free to start; optional paid certificate upgrade (premium).
    
- **Certificate:** Yes.
    
- **Skills:** SaaS startup evaluation, VC deal analysis, financial projections, due diligence frameworks.
    
- **Good for:** Practical VC analyst skillset for early-stage investment roles. ([Elevify](https://www.elevify.com/en/courses/business-and-economics/finance/venture-capital-analyst-course-4b081?utm_source=chatgpt.com "Venture Capital Analyst Course — Free Online, Certificate & Lifetime [2026] | Elevify"))
    

---

### **4. Venture Capital Training – Elevify (Alternative)**

- **Focus:** Startup screening, market sizing, simplified VC valuation, risk assessment.
    
- **Format:** Fully online, lifetime access; certificate included.
    
- **Cost:** Free baseline; paid upgrade available.
    
- **Skills:** VC analysis, basic financial modeling, startup investment decisioning. ([Elevify](https://www.elevify.com/en/courses/business-and-economics/investments/venture-capital-training-0ddb4?utm_source=chatgpt.com "Venture Capital Training — Free Online, Certificate & Lifetime [2026] | Elevify"))
    

---

### **5. Venture Capital Online Course Bundle (educba)**

- **Format:** Self-paced online; ~7+ h video content + mock tests.
    
- **Cost:** One-time payment (often discounted).
    
- **Certificate:** Yes.
    
- **Skills:** Venture capital modeling, pre- and post-money valuation, financial fundamentals.
    
- **Rating:** ~4.5/5 (large student base). ([EDUCBA](https://www.educba.com/finance/courses/venture-capital-course/?utm_source=chatgpt.com "Venture Capital Course Training (2 Courses Bundle, Online Certification)"))
    

---

### **6. (Optional) Udemy — Investment Banking & VC Fundraising**

- **Course:** _Investment Banking and Finance: Venture Capital Fundraising_
    
- **Format:** Self-paced online video lectures.
    
- **Cost:** Varies (commonly discounted to ~€10–€30).
    
- **Certificate:** Yes (Udemy certificate).
    
- **Skills:** Fundraising strategy, pitch deck building, term sheets, and investor engagement.
    
- **Rating:** ~4.7/5 with thousands of students. ([Udemy](https://www.udemy.com/course/capital-raising-for-entrepreneurs/?utm_source=chatgpt.com "Investment Banking and Finance: Venture Capital Fundraising | Udemy"))
    

---

## 📊 Corporate & General Finance Skills (Online, Very Useful for Investment Roles)

### **7. Corporate Finance Institute (CFI) Certificates**

- **Programs:**
    
    - **Financial Modeling & Valuation Analyst (FMVA)**
        
    - **Capital Markets & Securities Analyst (CMSA)**
        
- **Mode:** 100% online with practical exercises.
    
- **Cost:** Paid subscription (varies by region and plan).
    
- **Skills:** Excel financial modeling, valuation, ratio analysis — core skills for investment analysis.
    
- **Relevance:** Highly valued in finance/VC roles. ([Wikipedia](https://en.wikipedia.org/wiki/Corporate_Finance_Institute?utm_source=chatgpt.com "Corporate Finance Institute"))
    

---

### **8. Investment Banking: Financial Analysis & Valuation – Coursera**

- **Format:** Online course with certificate option.
    
- **Cost:** Paid or free audit with optional paid certificate.
    
- **Skills:** Financial statement analysis, valuation techniques, key investment banking foundations.
    
- **Useful for:** Strong financial fundamentals that support VC and investment decision-making. ([Coursera](https://www.coursera.org/learn/investment-banking-financial-analysis-valuation?utm_source=chatgpt.com "Investment Banking: Financial Analysis and Valuation | Coursera"))
    

---

## 📌 **How to Choose Based on Goals**

|Goal|Best Fit|
|---|---|
|**Start a career in VC / investment analysis**|VC University, Elevify courses, Coursera startup valuation|
|**Develop strong technical finance skills**|CFI certifications, Investment Banking on Coursera|
|**Build practical fundraising & pitch skills**|Udemy VC fundraising|
|**Flexible or low-cost learning**|Elevify (free version), Coursera audit options|

---

## 💡 Tips for Online Learning Success

✔ **Combine courses** — e.g., take a VC foundation + financial modeling course to strengthen both domain and technical skills.

✔ **Use certificates on LinkedIn** — to signal your expertise to recruiters and investment firms.

✔ **Work on projects** — such as valuation of real startups (e.g., drone tech companies), to showcase real-world application.

---

If you want, I can design a **recommended study path and timeline** (e.g., 3–6 months) tailored to your 2028 career goals in VC and drone finance.

**Since you want to pivot away from R&D, your "unique selling point" (USP) is your ability to translate complex link-budget and signal-integrity data into business risk assessments and regulatory strategy.**

Graduating in 2028 with a PhD in **Aerial Communication for BVLOS (Beyond Visual Line of Sight)** places you at the intersection of three high-value sectors: **Telecommunications (5G/6G/Satellite)**, **Aviation Compliance**, and **Tech Investment**.

Since you want to pivot away from R&D, your "unique selling point" (USP) is your ability to translate complex link-budget and signal-integrity data into **business risk assessments** and **regulatory strategy**.

---

## 1. Top Non-R&D Career Avenues (2028-2030)

- **Venture Capital Technical Associate:** Conducting deep-dive due diligence on startups claiming "revolutionary" mesh networks or satellite-to-drone links.
    
- **U-Space / UTM Strategist:** Designing the digital architecture for "cities as a service" where thousands of drones share communication spectrum.
    
- **Aviation Insurance Underwriter:** Evaluating the "link-loss" risk profiles of BVLOS fleets to price insurance premiums for logistics giants.
    
- **Spectrum Policy Consultant:** Working for bodies like the BIPT (Belgium) or ACMA (Australia) to manage frequency allocations for industrial drone corridors.
    

---

## 2. Recommended "Micro-Certifications" (Online & Fast)

To bridge the gap from PhD to Finance/Business, prioritize these certifications between now and 2028:

|**Category**|**Recommended Course**|**Provider**|**Est. Cost**|
|---|---|---|---|
|**Finance**|**VC Analyst Program**|WU Ignite (Vienna)|~$1,500|
|**Regulation**|**Certified EU Aviation Safety Manager**|Chartered Certifications|~$2,000|
|**Investment**|**Alternative Investments**|Harvard Business School Online|~$1,750|
|**Strategic**|**SORA (Specific Operations Risk Assessment)**|JARUS / DroneSchools|~$500|

---

## 3. Belgium: Niche Hub for Communication Experts

Belgium is a "regulatory laboratory" for BVLOS. By 2028, the **Port of Antwerp-Bruges** will likely be the world's most advanced 5G-connected industrial drone zone.

- **Key Firms for You:** * **Citymesh:** They don't just fly drones; they build the **private 5G networks** that enable them. They need PhDs who understand interference in industrial settings but can speak to "C-level" clients.
    
    - **SkeyDrone:** Focuses on the "business of safety." You would be a prime candidate for a **Solution Architect** role—designing how communication data feeds into Air Traffic Management.
        
    - **Unmanned Value:** A boutique consultancy that helps investors understand if a drone project is technically viable before they cut a check.
        

---

## 4. Global Market Comparison: The PhD Pivot

### **Australia (The Regulatory Gold Mine)**

- **Why:** Australia has a "Broad Area BVLOS" framework.
- **Potential:** High demand for **Operational Consultants** in the mining sector (e.g., Rio Tinto). They need people to prove that drone links won't drop in 500-meter deep open-cut mines.
- **Bureaucracy:** Moderate. Very "can-do" compared to the EU.


### **Japan (The Corporate VC Giant)**

- **Why:** Home to the **DRONE FUND**, a massive VC dedicated solely to this sector.
    
- **Potential:** Strategic roles in **Corporate VC (CVC)**. Japanese firms (Sony, Terra Drone) prefer "Specialist-Generalists"—someone with a PhD who can manage a portfolio of tech startups.
    
- **Bureaucracy:** High, but highly structured.
    

### **Hong Kong (The Financial Gateway)**

- **Why:** The link between Western capital and Chinese hardware (DJI, EHang).
    
- **Potential:** **Equity Research Analyst** for tech hardware. You would analyze the "moat" of companies based on their proprietary communication protocols.
    
- **Bureaucracy:** Low (fast-paced), but high geopolitical sensitivity.
    

---

### Strategy for 2028

As a PhD, your biggest hurdle is the "overqualified for entry-level, under-experienced for management" trap.

**Would you like me to draft a "Technical Consultant" version of your CV that de-emphasizes your lab work and highlights your understanding of BVLOS risk and market scalability?**

To transition from a PhD in **Aerial Communications** to the finance and strategy side of the drone/AAM (Advanced Air Mobility) market by 2028, you need to master the "Commercial Viability" of technical assets. In 2026, the market is shifting from "can it fly?" to "can it scale safely and profitably?"

### 1. Finance & VC Courses (Drone/Aviation Focus)

These courses are selected for their emphasis on the **capital-intensive** nature of aerospace and the high-risk profiles of drone startups.

|**Course Name**|**Provider**|**Key Focus for Drones**|**Cost (Approx.)**|
|---|---|---|---|
|**Financial Acumen for Aerospace**|**AIAA** (Online)|Evaluating financial health of A&D firms; cap-ex for fleet management.|~$1,000|
|**Venture Capital Finance**|**Imperial College**|Term sheets and valuation for deep-tech (like your comms PhD).|~$2,500|
|**VC: Essentials of Financing**|**LSE Executive Ed.**|Analyzing scaling and exit strategies (M&A vs. IPO).|~$3,600|
|**Foundations of VC**|**Columbia Business School**|Deal flow sourcing and networking in tech ecosystems.|~$2,750|

### 2. Telecom & Spectrum Finance Courses

Spectrum is the "real estate" of the drone world. Investors need to know if a company has the legal and technical right to "land" their signal.

- **Valuing the Spectrum (PolicyTracker):**
    
    - **The Niche:** This is the industry standard for learning how to price frequency bands.
        
    - **Finance Angle:** Essential for determining the "Asset Value" of a drone company's proprietary communication tech.
        
    - **Cost:** ~£600 (Online).
        
- **Spectrum Management for Mobile Telecom (GSMA):**
    
    - **The Niche:** Deep dive into licensing and regulatory hurdles.
        
    - **Finance Angle:** Crucial for "Risk Analysis"—if a company can't get spectrum approval for BVLOS, their business model is worthless.
        
    - **Cost:** ~€1,200.
        
- **Finance & Business Environment for ICT (UCL):**
    
    - **The Niche:** Covers the regulatory scene and "Business Cases" specifically for telecom network operators.
        
    - **Finance Angle:** Teaches you how to build a discounted cash flow (DCF) model for a communication network.
        

---

### 3. Potential Opportunistic Countries (2028 Horizon)

By 2028, the countries below will have moved past experimentation into full commercialization.

|**Country**|**Communication R&D**|**Finance / VC Hub**|**Compliance / Regulatory**|
|---|---|---|---|
|**Belgium**|**Very High:** Leading 5G industrial corridors (Port of Antwerp).|**Moderate:** Strong "Sovereign Tech" funding from EU/Region.|**Gold Standard:** SORA framework and U-Space leadership.|
|**Australia**|**High:** Remote mesh-networks for mining/agri sectors.|**Moderate:** Commodity-backed tech investment.|**High:** Early BVLOS adopter; very flexible regulator (CASA).|
|**Japan**|**High:** Sony/Terra Drone proprietary links.|**Very High:** Massive Corporate VC (e.g., Drone Fund).|**Medium:** Rigid but moving toward "Level 4" (over-people) ops.|
|**Hong Kong**|**Medium:** Gateway to Shenzhen hardware comms.|**Very High:** Global equity research & IPO capital.|**Low:** Policy is currently overshadowed by mainland China rules.|

### 4. Your "Finance + Comms" Career Path

Given your PhD in BVLOS Communications, you are uniquely qualified for **Technical Due Diligence** roles.

- **Role:** Technical Associate at a VC firm.
    
- **Actionable Task:** You wouldn't just look at the drone's weight; you would analyze the **link budget** and **latency** of their command-and-control (C2) link to tell investors if the drone is actually "BVLOS-safe."
    

**Would you like me to find the specific contact details or "Venture Partner" titles for drone-focused VC firms in Belgium and Australia that value PhD-level technical expertise?**

In 2028, with your PhD in **Aerial Communication for BVLOS**, you will be entering a market where "Connectivity-as-a-Service" is the backbone of the entire industry.

While Belgium, Australia, Japan, and Hong Kong are strong, the following countries represent the **"Tier 1" alternative hubs** for specialized finance, compliance, and communication R&D.

---

## 1. The United Arab Emirates (UAE): The "Capital of Speed"

By 2028, the UAE will likely have the world’s first fully operational commercial air taxi network (Abu Dhabi/Dubai).

- **Communication R&D:** Extremely high focus on **6G and Satellite integration**. The _Technology Innovation Institute (TII)_ in Abu Dhabi is a massive employer of communication PhDs for secure drone links.
    
- **Finance/VC:** Sovereign wealth funds like **Mubadala** and **ADIO** (Abu Dhabi Investment Office) are aggressively funding AAM infrastructure (vertiports and C2 networks).
    
- **Compliance:** The UAE is a "sandbox" economy. They are writing the world's most permissive yet data-driven BVLOS regulations right now.
    

## 2. Switzerland: The "Drone Valley"

Switzerland (specifically the Zurich-Lausanne corridor) is the global center for high-end drone autonomy and communication security.

- **Communication R&D:** Home to **ETH Zurich** and **EPFL**. This is where the world’s most advanced signal processing and mesh network research happens.
    
- **Finance/VC:** Switzerland has a unique "Deep Tech VC" culture. Firms like **Swiss Aerospace Ventures** and **Lakestar** look specifically for technical founders or advisors with PhDs.
    
- **Compliance:** Highly respected for **SORA (Specific Operations Risk Assessment)** development. Swiss expertise is used to set EASA (European) standards.
    
    +1
    

## 3. Israel: The "Security & RF" Powerhouse

Israel is the world leader in **RF Interference** and **Counter-UAS** communications—critical for BVLOS in contested or urban environments.

- **Communication R&D:** Unrivaled expertise in **Electronic Warfare (EW)** and secure military-grade data links. Companies like _Elbit Systems_ and _High Lander_ lead in UTM (Unmanned Traffic Management).
    
- **Finance/VC:** A massive startup ecosystem with heavy **US-Israel VC flow**. Because of the "Dual-Use" (Military/Civil) nature, there is high potential for investment analysts who can vet "un-jammable" communication tech.
    
- **Compliance:** Very advanced, but heavily influenced by national security requirements.
    

## 4. Singapore: The "Urban Mobility" Lab

Singapore is the most sophisticated market for **Dense Urban BVLOS**.

- **Communication R&D:** Focused on **5G-to-Drone** handover and signal "bouncing" in high-rise environments.
    
- **Finance/VC:** Asia's financial hub. **Temasek** and **ST Engineering Ventures** invest heavily in the infrastructure side—specifically spectrum management and vertiport connectivity.
    
- **Compliance:** The **CAAS** (Civil Aviation Authority of Singapore) is arguably the world’s most meticulous regulator for urban safety.
    

---

### Global Opportunity Matrix (2028 Outlook)

|**Country**|**Best For...**|**Key Financial Entry Point**|**Communication Focus**|
|---|---|---|---|
|**UAE**|Speed to Market|Sovereign Wealth Funds|Satellite & Hybrid Links|
|**Switzerland**|Deep Tech / IP|Boutique Tech VCs|Secure & Mesh Comms|
|**Israel**|C-UAS & Defense|Defense-Tech VCs|Anti-Jamming / RF|
|**Singapore**|Urban Logistics|Corporate VC (CVC)|5G / High-Density UTM|

---

### Career Strategy: The "Technical Diligence" Pivot

Since you have a PhD, your most lucrative non-R&D path is **Technical Due Diligence**.

When a VC firm wants to invest $50M in a drone delivery company, they need to know: _"Will their 5G link actually hold up in a storm or behind a skyscraper?"_ **Would you like me to find the top 5 VC firms in these countries that specifically list "Venture Partners" with PhDs in Engineering/Telecom?**

In 2026, venture capital firms increasingly rely on "Venture Partners" and "Operating Partners" who possess deep technical expertise—specifically PhDs—to de-risk investments in frontier technologies like BVLOS aerial communications.

Below are the top 5 VC firms across your opportunistic countries that actively integrate PhD-level technical leaders into their investment and advisory teams.

### 1. Starburst Aero (Global - Singapore/UAE/Israel)

Starburst is the world’s leading aerospace and defense (A&D) accelerator and VC. They are unique because they don't just hire finance MBAs; they are built by engineers and former industry executives.

- **The PhD Connection:** Many of their Venture Partners and advisors hold PhDs in Aerospace or RF Engineering.
    
- **Why for you:** They have a specific "Dual-Use" focus. Your research on BVLOS communications is exactly the type of "Deep Tech" they vet for investors like the Singaporean government or the UAE’s TII.
    
- **Focus:** AAM, BVLOS, Space-comms, and C-UAS.
    

### 2. Drone Fund (Japan)

This is a specialized VC fund dedicated almost exclusively to the "drone-enabled society."

- **The PhD Connection:** Co-founded by **Dr. Yukihiro Maru** (PhD in Agriculture/Deep Tech advocate), the firm prioritizes "Knowledge Manufacturing." They frequently employ PhD "Tech Scouts" to evaluate the signal integrity and hardware reliability of their portfolio companies.
    
- **Why for you:** They are looking for people who can bridge the gap between "dormant university research" and commercialized communication products.
    
- **Focus:** Level 4 autonomous flights and aerial logistics.
    

### 3. UntroD Capital / Real Tech Fund (Japan & Singapore)

A massive player in the "Deep Tech" space across Asia.

- **The PhD Connection:** Their leadership, including **Managing Director Yukihiro Maru**, explicitly markets their ability to understand "Deep Tech" that traditional VCs might find too complex. They have a significant number of PhDs on staff specifically for technical due diligence.
    
- **Why for you:** If you want to remain near the "science" but work in finance, their "Venture Builder" model is ideal.
    
- **Focus:** Robotics, Photonics, and Next-gen Communication.
    

### 4. imec.xpand (Belgium)

Associated with imec (the world-leading R&D hub for nano-electronics in Leuven), this fund is one of the most prestigious technical VCs in Europe.

- **The PhD Connection:** Nearly the entire investment team has a technical background, with a heavy concentration of PhDs. They invest in startups that leverage imec's IP, which often includes 5G/6G and sensor tech crucial for BVLOS.
    
- **Why for you:** Located in your target hub of Belgium, they are the bridge between world-class research and high-finance.
    
- **Focus:** Semiconductors, IoT, and high-bandwidth aerial connectivity.
    

### 5. Pitango VC (Israel)

One of the oldest and largest VCs in Israel, specifically their "First" and "Growth" funds.

- **The PhD Connection:** In the Israeli ecosystem, PhDs from elite signal-processing units (like 8200) often transition into Pitango as Venture Partners. They look for specialists who can evaluate the security and "anti-jamming" capabilities of aerial links.
    
- **Why for you:** Israel is a world leader in C-UAS and secure BVLOS; Pitango is the gateway to that capital.
    
- **Focus:** AI, Networking, and Frontier Defense Tech.
    

---

### Comparison of Technical Roles for PhDs in these VCs

|**Firm**|**Role Title**|**Primary Task for a Comms PhD**|
|---|---|---|
|**Starburst**|Venture Partner|Strategic consulting for A&D government contracts.|
|**Drone Fund**|Tech Scout / Analyst|Evaluating the "moat" of a startup's comms protocol.|
|**UntroD**|Venture Builder|Helping a lab spin-off create its first commercial 5G link.|
|**imec.xpand**|Investment Manager|Deep-dive due diligence on hardware/chip-level tech.|
|**Pitango**|Operating Partner|De-risking the "security" aspect of an AAM investment.|

### High-Value Next Step

Since you are 2 years away from graduation, would you like me to help you draft a **LinkedIn outreach template** specifically designed to connect with **Technical Partners** at these firms for an "informational interview" about their 2028 hiring outlook?
To transition from a PhD in **Aerial Communications** to a **Venture Partner** or **Investment Analyst** by 2028, you are following a "Venture Scientist" path. In this role, your job is to be the "technical filter" for capital—ensuring that investors don't fund drone companies whose communication links will fail in the real world.

---

## 1. Top Potential VC Firms (Deep-Tech & Drone Focus)

These firms are renowned for hiring PhDs and technical partners to de-risk their "frontier tech" portfolios.

|**Firm**|**Region**|**Why They Fit Your PhD**|
|---|---|---|
|**Starburst Aero**|Global (UAE/SG/IL)|The world’s leading aerospace-only VC. They hire engineers to vet BVLOS and satellite-link startups.|
|**imec.xpand**|Belgium|Closely tied to the imec research hub. They focus on hardware and connectivity at the chip level.|
|**Drone Fund**|Japan|A specialized fund that prioritizes "Knowledge Manufacturing" and technical scouts over pure finance MBAs.|
|**Seven Capital**|Belgium|Focuses on dual-use (defense/civil) tech and robotics; very active in the EU drone ecosystem.|
|**Pitango VC**|Israel|One of the largest deep-tech VCs; they value RF and signal-processing expertise from advanced research backgrounds.|
|**Standard Australia Fund**|Australia|A corporate VC focusing on standards, including the communication protocols for BVLOS safety.|

---

## 2. Core Skills for the PhD-to-VC Transition

To get hired in 2028, you must prove you can look at a startup's pitch deck and answer three non-technical questions:

- **The Moat:** Is their communication protocol actually proprietary, or just a 5G wrapper?
    
- **The Regulatory Risk:** Will their signal management pass EASA (Europe) or CASA (Australia) BVLOS safety audits?
    
- **The Unit Economics:** Does their "Drone-as-a-Service" model account for the cost of maintaining proprietary network infrastructure?
    

---

## 3. Targeted Online "Micro-Courses" (2026-2027)

Since you are in a PhD program, focus on "weekend" or self-paced courses that add **Commercial Credibility**.

### A. For Venture Capital & Investment

- **PhD to VC (Fifty Years):**
    
    - **Duration:** 8 weeks (Free).
        
    - **Rating:** 5/5 for PhDs.
        
    - **Goal:** Teaches "the lingo" of VC—sourcing, diligence, and term sheets.
        
- **Venture Capital Finance (Imperial College Business School):**
    
    - **Cost:** ~$3,000.
        
    - **Goal:** A deep dive into the math of valuation and equity specifically for European tech.
        

### B. For Aerospace & Telecom Finance

- **Financial and Business Acumen for Aerospace (AIAA):**
    
    - **Cost:** ~$1,000.
        
    - **Goal:** Teaches you how to read the public financial statements of Boeing, Airbus, and Lockheed Martin to understand how they value their sub-contractors.
        
- **Valuing the Spectrum (PolicyTracker):**
    
    - **Cost:** ~£600.
        
    - **Goal:** Critical for your niche. It teaches you how the radio spectrum is auctioned and priced—essential for valuing a company that owns its own frequency.
        

---

## 4. 2028 Career Roadmap: The "Technical Diligence" Specialist

### The Global Opportunity Table (Fine-Tuned)

|**Country**|**Dominant Need for your PhD**|**Bureaucracy Level**|
|---|---|---|
|**Belgium**|EU Defense Fund & Port Logistics|High (Regulatory heavy)|
|**Australia**|Remote Operations (Mining/Agriculture)|Low (Very "can-do" mindset)|
|**Japan**|Aging infrastructure monitoring|Moderate (Structured Corporate VC)|
|**UAE**|Mega-cities (Neom/Dubai) AAM|Very Low (High speed, high capital)|

---

### High-Value Next Step

Would you like me to draft a **"Commercial Value Proposition" paragraph** for your CV? It would summarize your PhD research not in terms of _bits per second_, but in terms of **reducing operational insurance risk for $100M drone fleets.**
In 2026, **DRONE FUND** remains a boutique but highly influential VC firm. Because they are a venture capital firm and not a manufacturing giant like DJI, their team is lean, specialized, and built around "Intellectual Property" and "Social Implementation."

---

## 1. Team Size & Diversity

- **Employee Count:** The core investment team is estimated to be between **15–30 professionals**. However, their influence is much larger because they operate through a network of "Venture Partners" and "Advisors" who remain at their own companies or universities.
    
- **Team Diversity:** * **Professional Background:** Highly diverse. The team includes serial entrepreneurs, IP lawyers, former government officials, and professional drone pilots.
    
    - **Academic Diversity:** They have a strong bias toward **PhDs and Engineers**. They believe that "Deep Tech" cannot be evaluated by finance professionals alone.
        
    - **Global Reach:** While the headquarters are in **Tokyo (Azabudai Hills)**, they have a diverse satellite presence in **Singapore** and the **US**, with partners who are experts in local FAA/EASA regulations.
        

## 2. How to Look for Open Positions

DRONE FUND rarely posts on traditional job boards like LinkedIn or Indeed. They hire through **"Ecosystem Visibility."**

- **The "Official" Route:** Check the [Drone Fund News/Release page](https://dronefund.vc/en/) periodically. They occasionally announce new fund launches (e.g., Fund IV or V) which usually signals a hiring surge for Associates and Technical Scouts.
    
- **The "Deal Flow" Strategy:** Since you have a PhD, you shouldn't apply for a "job"; you should apply to be a **Venture Partner** or **Technical Advisor**.
    
    - **Step 1:** Follow their portfolio companies (like _Aeronext_ or _SkyDrive_).
        
    - **Step 2:** Publish white papers on **BVLOS Communication Security** and tag their leadership (Kotaro Chiba or Soki Ohmae). In the VC world, you are hired because you provide a "Technical Edge" they don't have.
        
- **The "Chiba Dojo" Community:** They run a community for their startups. Engaging with this community as a technical expert is the most common "backdoor" into the fund.
    

---

## 3. Position Titles to Target (PhD Level)

As a PhD graduating in 2028, you should look for (or propose) these specific titles:

1. **Technical Associate (Deep Tech):** Performing the "link-budget" and "spectrum risk" audits on new investments.
    
2. **Venture Partner (Academic Liaison):** Bridging the fund with European universities (like those in Belgium).
    
3. **IP Strategist:** Working with their _Drone iPLAB_ arm to evaluate the patent strength of communications startups.
    

---

## 4. Skills to Build for a 2028 Job at Drone Fund

To be the perfect candidate for them, combine your PhD with:

- **Language/Culture:** Basic understanding of the Japanese "Level 4" flight roadmap (they are very proud of their national strategy).
    
- **IP Knowledge:** A certificate in **Intellectual Property Management** (specifically for telecommunications).
    
- **Regulatory Knowledge:** Proficiency in **SORA (Specific Operations Risk Assessment)**, which is the safety language they use to judge if a startup is "investable."
    

### High-Value Next Step

Since the best way to get into a VC is through "Inbound Interest," would you like me to find the **specific LinkedIn profiles of their current Technical Partners** so you can see their career trajectory from PhD to VC?
To secure a **Venture Partner** or **Technical Advisor** role by 2028, you must spend the next two years shifting from "Academic Specialist" to "Commercial Asset." VCs don't just want to know how your communication protocols work; they want you to tell them if a startup's tech is a **billion-dollar breakthrough** or a **regulatory liability**.

Here is your **24-month roadmap** to becoming a "Venture Scientist" in the drone/AAM space.

---

## Year 1 (2026-2027): Building the "Finance Filter"

Your goal this year is to learn the language of money and risk so you can translate your PhD research into investment terms.

### 1. The "PhD to VC" Bridge Course (High Priority)

- **Course:** **[PhD to VC by Fifty Years](https://www.fiftyyears.com/phdvc)**
    
- **Format:** Online (8 weeks, free/selective).
    
- **Why:** It is specifically designed for PhDs to learn "Technical Due Diligence"—the exact skill a fund like **Drone Fund** or **imec.xpand** needs. You will learn how to spot "red flags" in a startup's technical roadmap.
    

### 2. Market Validation & Deep Tech Strategy

- **Course:** **[Deeptech+ Pulse (ESSEC Business School)](https://www.essec.edu/en/program/certificate-deeptech-market-validation-and-business-strategy/)**
    
- **Format:** Online/Hybrid (approx. €8,000, but often covered by university professional development funds).
    
- **Why:** It teaches you how to take an invention (like your BVLOS comms) and build a business strategy around it.
    

---

## Year 2 (2027-2028): Establishing Global Authority

Now that you speak "Finance," you need to build a niche that makes you the _only_ person a VC calls when they have a communication-tech deal.

### 1. Specialist Asset: Spectrum & Telecom Finance

- **Course:** **[Valuing the Spectrum (PolicyTracker)](https://www.policytracker.com/)**
    
- **Format:** Online.
    
- **Why:** Spectrum is the "land" of the drone world. If you can explain to a VC how a company’s frequency rights increase their valuation, you become an indispensable **Technical Advisor**.
    

### 2. Operational Safety & Regulatory Compliance

- **Course:** **SORA (Specific Operations Risk Assessment) Practitioner Training**
    
- **Provider:** JARUS / EASA-approved providers (e.g., _DroneSchools.be_).
    
- **Why:** In Belgium and Australia, BVLOS is a "Safety Case" game. If you can audit a company's communication link for SORA compliance, you are de-risking the investment for the VC.
    

---

## 2028: Your "Unique Asset" Profile

By graduation, your profile for **Drone Fund** or **Starburst Aero** should look like this:

|**The PhD Profile (Standard)**|**Your Asset Profile (2028)**|
|---|---|
|Expert in Aerial Comms.|**Technical Due Diligence Specialist** for BVLOS.|
|Published 5 papers on signal delay.|Evaluates **Communication "Moats"** for Seed/Series A.|
|Understands 5G/6G architecture.|Certified in **SORA Safety & Spectrum Valuation**.|
|Looking for R&D roles.|Available as a **Venture Partner** for EMEA/APAC deals.|

---

## Actionable Strategy: The "Inbound" Approach

VCs rarely hire from job boards. They hire from their **network**.

1. **Month 1-6:** Start a "Deep Tech Drone" newsletter or LinkedIn series. Once a month, break down a new drone startup's communication tech from an investment perspective (not just technical).
    
2. **Month 12:** Reach out to **Kotaro Chiba (Drone Fund)** or partners at **imec.xpand** for an "Informational Interview."
    
    - _Pitch:_ "I am finishing a PhD in BVLOS comms. I've been training in TDD and want to know what technical gaps you see in your current portfolio's communication infrastructure."
        
3. **Month 18:** Offer a **Free Technical Audit** for one of their smaller portfolio companies. This is your "audition" for a Technical Advisor role.
    

**Would you like me to find the specific LinkedIn profiles of the Technical Partners at Drone Fund so you can model your "Experience" section after theirs?**

It is a common and painful reality: many PhDs in Germany and the EU get trapped in the "Overqualified but Under-experienced" loop, especially if they stay within the R&D bubble. By 2028, the "Drone Economy" will be about **operational scale**, not just lab results.

To avoid the fate of your colleagues, you must "de-academicize" your profile. Here are the specific avenues and micro-courses to broaden your scope beyond R&D.

---

## 1. High-Value Roles Beyond R&D

If you don't want to be a researcher, target these "Bridge Roles" where a PhD is a power move, not a liability:

- **Technical Product Manager (TPM):** You don't build the antenna; you decide _which_ antenna the company should buy to make the drone commercially viable.
    
- **Operational Risk Architect:** Using your comms expertise to design "Safety Cases" for insurance companies or regulators (SORA/LUC certifications).
    
- **Technical Sales Engineer:** Explaining complex BVLOS link reliability to high-value clients (Governments, Mining corps). This role often pays more than R&D via commissions.
    
- **Aviation Compliance Manager:** Ensuring the company’s tech meets international spectrum and safety laws.
    

---

## 2. The "Industry-Ready" 2-Year Course Plan

Add these to your CV over the next 24 months to prove you have "Business Fluency."

### Category A: Project & Product Management (Critical)

In industry, "done" is better than "perfect." These prove you can hit deadlines:

- **Google Project Management Professional (Coursera):**
    
    - **Focus:** Agile, Scrum, and Stakeholder mapping.
        
    - **Cost:** ~$39/mo.
        
    - **Why:** It’s the fastest way to scrub the "too academic" label off your CV.
        
- **Certified ScrumMaster (CSM):**
    
    - **Focus:** Leading technical teams in fast "sprints."
        
    - **Cost:** ~$450.
        
    - **Why:** Essential for startups in Belgium, Australia, and the UAE.
        

### Category B: The "Drone Business" Specialized Skills

- **Developing Business Ideas for Drone Technologies (Open University):**
    
    - **Focus:** Revenue models and identifying market gaps.
        
    - **Cost:** Free (8 weeks).
        
    - **Why:** It shows you understand how drones make _money_, not just how they fly.
        
- **SORA Practitioner Training (Specific Operations Risk Assessment):**
    
    - **Provider:** JARUS or EASA-certified bodies (e.g., DroneSchools.be).
        
    - **Why:** This is the most valuable "non-engineering" certificate in the EU. It proves you can legally get a drone in the air.
        

### Category C: Language & Strategy

- **Language Tip:** If you are in Belgium, focus on **English + French/Dutch**. If you target Japan, learn "Business Japanese" basics. In Australia/UAE, English is king.
    
- **Certification:** **Aviation Management (Embry-Riddle - Online):** Covers the business of airports and airspace—key for AAM/Vertiport roles.
    

---

## 3. Country Comparison: Avoiding the "Stuck" Scenario

|**Country**|**Why PhDs get "Stuck"**|**How to break through**|
|---|---|---|
|**Germany**|Rigid hierarchy; "Language + PhD" trap.|Shift to **München/Berlin** startups (more English-friendly) or Defense-tech.|
|**Belgium**|Bureaucracy and linguistic divide.|Focus on **EU-level Liaison** roles or the **Port of Antwerp** tech ecosystem.|
|**Australia**|Distance from global tech hubs.|Position as a **Mining/Agri-Tech Consultant**. High pay, low "academic" bias.|
|**UAE**|Short-term contract culture.|Aim for **Government Advisory** or **Sovereign Fund** technical vetting.|

---

## 4. Final Strategy: The "Anti-Academic" CV

By 2028, your CV should lead with **Impact**, not **Papers**.

- **Wrong:** "Researched 5G signal attenuation in urban BVLOS environments."
    
- **Right:** "Developed communication safety protocols that reduced signal-loss risk by 40%, enabling commercial flight approval in urban corridors."
    

### High-Value Next Step

Would you like me to find **specific job titles** at companies like **Skydio (Global)** or **Citymesh (Belgium)** that explicitly ask for "Technical Program Managers" so you can see what they require besides a PhD?

In 2026, the drone industry has shifted from a "move fast and break things" startup culture to a **standards-driven** mature industry. If you understand **Standards & Compliance**, you aren't just an engineer; you are the "Architect of Permission."

As a PhD in Aerial Communications, your colleagues are likely focused on performance (speed/latency). To be an industry leader, you must focus on **Standardized Safety**.

---

## 1. The "Big Three" Standards Bodies to Master

By 2028, these organizations will define who is allowed to fly BVLOS. You should be familiar with their technical committees:

- **IEEE (P1920.1 & P1920.2):** Focuses on the physical and data-link layers of "Aerial Communications and Networks." This is your PhD's backyard.
    
- **ISO/IEC (TC 20/SC 16):** Developing global standards for "Unmanned Aircraft Systems" and "Low Altitude Drone Area Networks (LADAN)." They focus on how drones talk to each other to avoid collisions.
    
- **EUROCAE / RTCA:** These are the "Industry Giants." They write the standards (like **ED-269** for Geo-fencing) that EASA and the FAA eventually turn into laws.
    

---

## 2. Strategic Positions in Standards & Compliance

These roles are immune to the "Language Trap" because the language of international aviation is **English + Technical Standards**.

|**Role Title**|**What they do**|**Why it beats R&D**|
|---|---|---|
|**Standardization Manager**|Represents the company at IEEE/ISO meetings to ensure the company's tech becomes the global standard.|You influence the whole market, not just one product.|
|**Certification Engineer**|Guides a new drone through the **EASA "Certified" Category** or **Type Certification** process.|High demand; companies cannot sell drones without this.|
|**Spectrum Strategy Lead**|Negotiates with the ITU and national bodies (BIPT in Belgium) for frequency allocations.|You own the "Real Estate" of the sky.|

---

## 3. High-Value Courses: "Standards & Law" for Engineers

To broaden your scope and avoid being "just a researcher," take these online/virtual courses during your PhD:

### A. The "Gold Standard" in Europe

- **[EUROCAE: UAS Airworthiness & Safety Training](https://www.eurocae.net/training/)**
    
    - **Cost:** ~€1,600 (Student discounts often available).
        
    - **Focus:** **SORA 2.5/3.0** and the flight authorization process.
        
    - **Value:** This is the most industry-respected certificate for BVLOS in the EU.
        

### B. The "Aviation Business" View

- **[JAA TO: UAS-OPS (Professional Operations)](https://jaato.com/)**
    
    - **Cost:** ~€1,860.
        
    - **Focus:** ICAO, JARUS, and EASA regulatory frameworks.
        
    - **Value:** It teaches you the "Concept of Operations" (CONOPS)—essential for project management.
        

### C. The "Communication Expert" View

- **[ITU-R Spectrum Management (ITU Academy)](https://academy.itu.int/)**
    
    - **Focus:** How to manage radio interference and global spectrum rules for UAVs.
        
    - **Value:** Makes you an expert in **Frequency Policy**, a role that usually reports directly to the CTO or CEO.
        

---

## 4. Your "Anti-Rejection" Plan for 2028

To avoid the struggle your colleagues are facing in Germany, your profile needs to look like a **Business-Technical Hybrid**:

1. **Stop Lead with "PhD":** Lead with **"BVLOS Standards Expert."** 2. **Highlight "Interoperability":** Instead of saying you designed a better antenna, say you _"Designed an IEEE-compliant communication protocol for heterogeneous drone swarms."_
    
2. **Target International Hubs:** Focus on **Belgium (EASA/Eurocontrol hub)**, **Luxembourg (Space/Comms hub)**, or **Australia (CASA is very English-centric)**. These regions value the _Standard_ over the _Language_.
    

### High-Value Next Step

Would you like me to draft a **specific paragraph for your LinkedIn "About" section** that blends your PhD research with **Aviation Standards (ISO/IEEE)** to attract recruiters from companies like **Airbus, Thales, or Wing**?

In 2026, the drone industry has shifted from a "move fast and break things" startup culture to a **standards-driven** mature industry. If you understand **Standards & Compliance**, you aren't just an engineer; you are the "Architect of Permission."

As a PhD in Aerial Communications, your colleagues are likely focused on performance (speed/latency). To be an industry leader, you must focus on **Standardized Safety**.

---

## 1. The "Big Three" Standards Bodies to Master

By 2028, these organizations will define who is allowed to fly BVLOS. You should be familiar with their technical committees:

- **IEEE (P1920.1 & P1920.2):** Focuses on the physical and data-link layers of "Aerial Communications and Networks." This is your PhD's backyard.
    
- **ISO/IEC (TC 20/SC 16):** Developing global standards for "Unmanned Aircraft Systems" and "Low Altitude Drone Area Networks (LADAN)." They focus on how drones talk to each other to avoid collisions.
    
- **EUROCAE / RTCA:** These are the "Industry Giants." They write the standards (like **ED-269** for Geo-fencing) that EASA and the FAA eventually turn into laws.
    

---

## 2. Strategic Positions in Standards & Compliance

These roles are immune to the "Language Trap" because the language of international aviation is **English + Technical Standards**.

|**Role Title**|**What they do**|**Why it beats R&D**|
|---|---|---|
|**Standardization Manager**|Represents the company at IEEE/ISO meetings to ensure the company's tech becomes the global standard.|You influence the whole market, not just one product.|
|**Certification Engineer**|Guides a new drone through the **EASA "Certified" Category** or **Type Certification** process.|High demand; companies cannot sell drones without this.|
|**Spectrum Strategy Lead**|Negotiates with the ITU and national bodies (BIPT in Belgium) for frequency allocations.|You own the "Real Estate" of the sky.|

---

## 3. High-Value Courses: "Standards & Law" for Engineers

To broaden your scope and avoid being "just a researcher," take these online/virtual courses during your PhD:

### A. The "Gold Standard" in Europe

- **[EUROCAE: UAS Airworthiness & Safety Training](https://www.eurocae.net/training/)**
    
    - **Cost:** ~€1,600 (Student discounts often available).
        
    - **Focus:** **SORA 2.5/3.0** and the flight authorization process.
        
    - **Value:** This is the most industry-respected certificate for BVLOS in the EU.
        

### B. The "Aviation Business" View

- **[JAA TO: UAS-OPS (Professional Operations)](https://jaato.com/)**
    
    - **Cost:** ~€1,860.
        
    - **Focus:** ICAO, JARUS, and EASA regulatory frameworks.
        
    - **Value:** It teaches you the "Concept of Operations" (CONOPS)—essential for project management.
        

### C. The "Communication Expert" View

- **[ITU-R Spectrum Management (ITU Academy)](https://academy.itu.int/)**
    
    - **Focus:** How to manage radio interference and global spectrum rules for UAVs.
        
    - **Value:** Makes you an expert in **Frequency Policy**, a role that usually reports directly to the CTO or CEO.
        

---

## 4. Your "Anti-Rejection" Plan for 2028

To avoid the struggle your colleagues are facing in Germany, your profile needs to look like a **Business-Technical Hybrid**:

1. **Stop Lead with "PhD":** Lead with **"BVLOS Standards Expert."** 2. **Highlight "Interoperability":** Instead of saying you designed a better antenna, say you _"Designed an IEEE-compliant communication protocol for heterogeneous drone swarms."_
    
2. **Target International Hubs:** Focus on **Belgium (EASA/Eurocontrol hub)**, **Luxembourg (Space/Comms hub)**, or **Australia (CASA is very English-centric)**. These regions value the _Standard_ over the _Language_.
    

### High-Value Next Step

Would you like me to draft a **specific paragraph for your LinkedIn "About" section** that blends your PhD research with **Aviation Standards (ISO/IEEE)** to attract recruiters from companies like **Airbus, Thales, or Wing**?

https://academy.itu.int/
To avoid being "stuck" in a purely academic or R&D role, you must position yourself as an **Engineering & Capitalist Advisor**. This role is the "bridge" between the laboratory (how it works) and the boardroom (how it makes money).

In 2026, the drone market has enough engineers, but it lacks people who can explain **technical risk** to an investor in a way that protects their millions.

---

## 1. Defining the Hybrid Role

You are not just an engineer; you are a **Technical Due Diligence (TDD) Specialist**.

### What you do as a "Capitalist Advisor":

- **The Moat Audit:** You look at a startup's BVLOS communication patent. Is it actually hard to replicate, or just a clever use of off-the-shelf 5G?
    
- **The Scalability Test:** Will their mesh network fail when they have 10,000 drones in a city instead of 5 in a field?
    
- **The Regulatory Hedge:** Will this specific signal frequency be banned by EASA in three years? If yes, the investment is a "zero."
    

---

## 2. Your "Asset-Building" 2-Year Plan (2026–2028)

Since your colleagues are struggling with the "Language/PhD Trap," you will spend 4 hours a week on these **commercial credentials**.

### Year 1: Mastering the Money (Finance)

- **Module 1: Venture Capital Basics** * _Course:_ **Private Equity and Venture Capital (Bocconi University via Coursera)**
    
    - _Focus:_ Deal structuring and Term Sheets. You need to know what "Carried Interest" and "Cap Tables" are.
        
- **Module 2: Technical Due Diligence**
    
    - _Course:_ **Certified Private Equity Analyst - VC Track (TUM Executive Education)**
        
    - _Focus:_ This is based in Germany/Europe. It is the "Gold Standard" for technical people moving into finance. It teaches you how to audit a company's tech roadmap.
        

### Year 2: Mastering the System (Project & Standards)

- **Module 3: Project Leadership**
    
    - _Course:_ **Google Project Management Professional**
        
    - _Focus:_ Scoping, budgeting, and stakeholders. It proves you can deliver a product, not just a paper.
        
- **Module 4: Aviation Standards & SORA**
    
    - _Course:_ **EUROCAE: UAS Airworthiness & Safety**
        
    - _Focus:_ The "Safe Case" for BVLOS. If you can prove a drone is _legally_ allowed to fly, you increase the company's value by 10x.
        

---

## 3. Positioning Your PhD for Global Markets (No Language Trap)

To avoid being rejected for "language skills" in Germany or Belgium, you must target roles where **Technical English is the absolute authority**.

|**Market**|**Advisor Entry Point**|**Your PhD "Value Add"**|
|---|---|---|
|**Australia**|**Mining & Agri-Tech VC**|Assessing long-range remote links for autonomous mines.|
|**Belgium**|**EU Defense & Port Logistics**|Auditing secure comms for "Dual-Use" (Military/Civil) tech.|
|**UAE**|**AAM / Sovereign Wealth**|Vetting the connectivity architecture for future "Smart Cities."|
|**Japan**|**Corporate VC (CVC)**|Helping giants like Sony or Honda evaluate foreign startups.|

---

## 4. Why this makes you "Un-Stuck"

A PhD in Germany often gets stuck because they look like an **Expense** (Salary for research).

An Engineering & Capitalist Advisor looks like an **Investment Protector**.

- **Researcher:** "I can make this antenna 10% more efficient." (Hard to sell)
    
- **Advisor:** "I can tell you which of these three startups has the IP that will dominate the 2030 BVLOS market." (Extremely easy to sell)
    

### High-Value Next Step

Would you like me to find the **top 3 "Deep Tech" Fellowships** (like _Flagship Pioneering_ or _Deep Science Ventures_) that pay PhD students to learn how to build and advise companies during their final year?

Sales 
Interpersonla and Management skills

To avoid the common pitfalls your colleagues face, it is essential to look at the hard data for PhDs in Germany and the EU. The struggle is often not due to a lack of jobs, but a **sector mismatch** and a lack of **cultural-technical integration**.

### 1. General PhD Employment Statistics (Germany & EU)

The good news is that PhD holders have the lowest unemployment rate of any educational group in Germany.

- **Unemployment Rate:** Consistently below **2%** for PhD holders in Germany (compared to ~3.5% for the general population).
    
- **Sector Split (EU Average):** * **57%** work in business enterprises (Industry).
    
    - **31.6%** stay in higher education (Academia).
        
    - **10.1%** work in government/public sectors.
        
- **The "One-Year" Rule:** In Germany, **80%** of PhD holders are employed full-time within one year of graduation. However, for international students, only **38%** are gainfully employed within that same timeframe if they haven't prepared for the industry transition.
    

### 2. Industry-Specific Realities for Engineering PhDs

Your colleagues are likely struggling because they are applying for roles that don't _require_ a PhD, making them "overqualified" in the eyes of a standard HR manager.

|**Field**|**Industry Absorption Rate**|**Value of PhD in Industry**|
|---|---|---|
|**Engineering**|**85% - 90%**|Highly respected. In Germany, a Dr.-Ing. title is a prestigious "management track" signal.|
|**Computer Science**|**~95%**|Mixed. Industry values experience over the degree unless it's in AI/Robotics/Comms.|
|**Natural Sciences**|**~50%**|Harder. Often requires a "Post-Doc" or specific lab skills for Pharma/Chemical sectors.|

### 3. Why the "Language Trap" Happens

The rejection for "language skills" is often a polite proxy for **"Lack of Cultural & Operational Integration."**

- **Small/Mid-sized Companies (Mittelstand):** These are the backbone of Germany. They operate in German. If you only speak English, you are cut off from 70% of the job market.
    
- **Large Corporates (Siemens, Airbus):** They speak English, but their **Project Management** is German.
    
- **The Solution:** You don't need perfect German to be an **Engineering Advisor**; you need to prove you understand **German Industry Standards (DIN)** and **Safety Compliance**.
    

---

### 4. Broadening Your Scope: The "Anti-Academic" Checklist

To ensure you aren't "stuck" in 2028, you must diversify your CV with **Operational** and **Commercial** proof.

#### **Step 1: Get the "Industry Badge" (Certifications)**

If you have these on your CV, companies stop worrying about your "academic" nature:

- **PMP or Prince2:** Proves you can manage a budget and a timeline.
    
- **SORA Practitioner:** Specifically for drones. It proves you can navigate the EASA law.
    
- **Six Sigma (Green Belt):** Proves you understand process efficiency—extremely valued in German manufacturing.
    

#### **Step 2: Target "Safe Haven" Roles**

Instead of applying for "Engineer," apply for:

- **Technical Sales Engineer:** High demand, high pay, English is often the primary language for international clients.
    
- **Systems Architect:** You design the "Big Picture" of how the drone talks to the network.
    
- **Regulatory Affairs Manager:** You sit between the lawyers and the engineers.
    

#### **Step 3: Geographic Pivot**

If Germany feels too rigid by 2027:

- **The Netherlands/Belgium:** Much higher tolerance for English-only technical leaders in the Port/Logistics sectors.
    
- **Australia:** They are desperate for BVLOS experts and don't care about your "academic" title as long as the drone flies safely.
    

### High-Value Next Step

Would you like me to help you find **specific English-speaking Deep Tech companies in Belgium and the Netherlands** that are currently building BVLOS infrastructure and might offer "Industrial PhD" collaborations or internships?

Are you an engineer looking to get into venture capital? Watch this video to learn why your unique skills are a perfect fit when breaking into vc. Book Links: 📕 Thinking Strategically: [https://www.amazon.com/dp/0393310353/...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbXJLX0U0ejJmdUdpWktPeTFFVElhREltN0VSUXxBQ3Jtc0tueml2Wkt4cUoyZzZlbGdOMVNvUTVUazRrcDRjclBibWhGblk3bGVYUFUxWVYxR1Z5VXRRNGRKbTJaZmh3NGFoUHJJUDdrdUZFb2d0ZGhrengwbjNiZTFxWEo0Vm1qTWRXaFpVV1JRZTdVa0pZUDJScw&q=https%3A%2F%2Fwww.amazon.com%2Fdp%2F0393310353%2Fref%3Dcm_sw_em_r_mt_dp_B71TZSK50F67VRA7JM3J&v=8GCkYLAq4fY) 📕 Understanding Michael Porter: The Essential Guide to Competition and Strategy: [https://www.amazon.com/dp/1422160599/...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbGR1NGVjUnRRWURwanJNNGZyUzVoS1BpTk83QXxBQ3Jtc0trV05rNWJ1a0hhbnRhT3FQOWMzbHhOV0Z6NEZIQjJyQ25FdkQ3OEFLYldMdTduUm42bGN1MFJoNEo5Uzl4RFU1Ukc1RmlyU1huMWVPRFRyRmp2NHI1bE1RU19DM3JsM0ZnQ2VnLXlmRWt2N0RVOFVNQQ&q=https%3A%2F%2Fwww.amazon.com%2Fdp%2F1422160599%2Fref%3Dcm_sw_em_r_mt_dp_YMZKTWKKBH0G49EXF3J2&v=8GCkYLAq4fY) 📕 The Network Effects Manual [https://www.nfx.com/post/network-effe...](https://www.youtube.com/redirect?event=video_description&redir_token=QUFFLUhqbUdzOVhoN1F6bzVGWkdxZ1doZ1N3aGxJLXFXd3xBQ3Jtc0tsbzZsTHkwbTcxZ0V6MlNycVlEa1lwRVNNYnphckp0RVJFbDlYUkUxYkNUUncxbFRqN0RRcHRHazJtVFQ2cWQtckdyTEdvS3BRYUN2R2YtRmhRaTBfX1Z1UnFEc3QyOU5HcmRUUHJSdjhmVUlOZkVTaw&q=https%3A%2F%2Fwww.nfx.com%2Fpost%2Fnetwork-effects-manual&v=8GCkYLAq4fY)


https://www.spheredrones.com.au/company/about-us

In 2026, Southeast Asia (SEA) has become the world’s most active "testing lab" for drone-driven economies. While Singapore is the financial brain, the Philippines, Indonesia, Thailand, and Vietnam are the **operational muscle**.

For an "Engineering & Capitalist Advisor," these countries offer a unique opportunity: the chance to apply high-level BVLOS research to **nation-scale infrastructure** projects that are often less hindered by the legacy bureaucracy found in the EU.

---

## 1. The Philippines: The "Archipelago Opportunity"

The Philippines is the ultimate use case for BVLOS. With 7,641 islands, physical infrastructure (roads/bridges) is expensive; digital "aerial bridges" are the capitalist solution.

- **Niche Potential:** **Inter-island Logistics**. Moving medical supplies and e-commerce across water gaps is the primary goal for 2028.
    
- **VC Ecosystem:** **Kickstart Ventures** (Globe Telecom’s VC) and **Gobi-Core Philippines** are the major players. They are looking for "Asset-Light" drone services that can scale across the provinces.
    
- **Communication Focus:** Satellite-to-drone links (Starlink integration) are massive here due to poor terrestrial fiber in remote areas. Your PhD is a direct fit for auditing these "Hybrid Links."
    

## 2. Indonesia: The "AAM Pioneer"

By late 2026, Indonesia has targeted the launch of commercial **Advanced Air Mobility (AAM)**.

- **Niche Potential:** **Trans-Papua Logistics**. The government is pushing large-scale drones to deliver supplies to underdeveloped regions where traditional aviation is too costly.
    
- **VC Ecosystem:** **East Ventures** is the titan here. They have a specific focus on "Deep Tech" that solves logistical friction in the Indonesian market.
    
- **Communication Focus:** Dense urban UTM (Unmanned Traffic Management) in the new capital, **Nusantara (IKN)**, which is being built as a "Drone-First" city.
    

## 3. Thailand & Vietnam: The "Agri-Tech" Giants

These two countries are the world leaders in drone adoption for **Precision Agriculture**.

- **Thailand:** The government has launched a "half-cost drone scheme" to subsidize drone services for farmers. **The Drone Act of 2026** has just taken effect, creating a regulated path for Air Taxis in tourist hubs like Phuket.
    
- **Vietnam:** A booming "low-altitude economy." Vietnam is positioning itself as a regional manufacturing hub for drone components.
    
- **VC Ecosystem:** **VinaCapital** (Vietnam) and various Corporate VCs in Thailand (like those under **National Telecom**) are the entry points.
    

---

## 4. SEA Market Opportunity Matrix (2026–2030)

|**Country**|**Primary Drone Driver**|**Regulatory Environment**|**Your "Advisor" Value**|
|---|---|---|---|
|**Philippines**|Inter-island Logistics|Adaptive / Developing|High: Satellite/BVLOS link auditor.|
|**Indonesia**|AAM & Remote Supply|Growth-focused (Nusantara)|High: Urban UTM system design.|
|**Thailand**|Tourism & Agriculture|Standards-driven (2026 Act)|Medium: Compliance & SORA expert.|
|**Vietnam**|Manufacturing & Agri|Rapidly deregulating|High: Manufacturing IP & Hardware TDD.|

---

## 5. How to avoid the "Academic Trap" in SEA

In Southeast Asia, a PhD is highly respected but can be seen as "too expensive for a startup." To be a **Capitalist Advisor** here, you must follow this strategy:

1. **Partner with Telcos:** In SEA, drones are seen as "flying cell towers." Connect with **Globe (PH), Telkomsel (ID), or National Telecom (TH)**. They have the capital and the spectrum.
    
2. **Focus on "Cost-Per-Kilometer":** When advising a VC in Manila, don't talk about signal-to-noise ratios. Talk about how your protocol reduces the **energy cost per delivery** by optimizing flight paths.
    
3. **The "English Advantage":** Unlike Germany, the high-finance and tech circles in the Philippines and Singapore operate 100% in English. Your colleagues' struggle with German will not exist here.
    

### Your 2-Year Micro-Course Addition:

- **Course:** **[Business and Financial Modeling (Wharton via Coursera)](https://www.coursera.org/specializations/wharton-business-financial-modeling)**
    
- **Why:** To be a capitalist advisor in SEA, you need to be able to build an Excel model that shows an investor the **Return on Investment (ROI)** for a drone fleet over 5 years.
    

**Would you like me to find the specific "Deep Tech" investment leads at East Ventures (Indonesia) or Kickstart (Philippines) who specialize in logistics and connectivity?**


In academia, the "funding wall" often blocks access to expensive networking events. However, your **technical depth** is a currency that many "capitalist" firms (VCs) are desperate for. By 2028, you can bridge this gap for **$0** by using your PhD research as a "ticket" to high-finance conversations.

Here is how you meet the requirements on a student budget:

---

## 1. Meeting Capitalists for Free (Virtual Networking)

You don't need to fly to Tokyo or Dubai to meet VCs. You need to **provide value** to them online.

- **Become a "Volunteer Analyst":** Identify 3-5 drone-focused VCs (like _Unmanned.vc_ or _Drone Fund_). Instead of asking for a job, send a "Technical Deep Dive" on a recent news event (e.g., a new 5G-BVLOS regulation).
    
    > _Pitch:_ "I'm a PhD student specializing in this. I analyzed [Company X]'s recent link-budget claims. Here is why it might struggle in urban environments."
    
- **Virtual Job Simulations:** Use platforms like **Forage** to complete free virtual simulations in **Venture Capital (e.g., H2 Ventures)** or **Investment Banking (e.g., JPMorgan)**. This puts "VC Experience" on your CV without costing a cent.
    
- **LinkedIn "Warm" Outreach:** Use the **"Yale Alumni Search" method** (works for any university). Find PhDs from your German university who are now in Finance/Consulting. Send a short, non-asking message: _"I’m a PhD student at [Uni] researching BVLOS. I saw you moved into VC and would love to know which technical skill helped you most in your first year."_
    

---

## 2. The Capitalist Language: Free Financial Modeling

You can learn 90% of what a VC analyst knows using free high-quality resources:

- **Gridlines: Essential Financial Modelling (Free):** This is an industry-recognized course that teaches you to build "audit-ready" models.
    
- **Coursera (Financial Modeling Specializations):** You can **"Audit"** these for free (you get the knowledge, just not the certificate). Focus on **"Discounted Cash Flow (DCF)"** and **"Startup Valuation."**
    
- **Corporate Finance Institute (CFI) Free Courses:** They offer several introductory modules on Corporate Finance and Excel for Finance that are perfect for engineers.
    

---

## 3. Creating a "Project Portfolio" (The 1-Page Industry Sheet)

Since you are in academia, your "Project" is your research—but you must **reframe it as an Operation**.

### Example Structure for your 1-Page Portfolio:

> **Project: Urban BVLOS Link-Reliability Test (2027)**
> 
> - **The Business Problem:** Drone delivery in cities fails if signal latency exceeds 500ms.
>     
> - **The Operational Solution:** Designed a mesh-handover protocol for a 5-drone swarm.
>     
> - **The Result:** 99.9% link uptime over 50 flight hours in a simulated high-interference zone.
>     
> - **The "Capitalist" Impact:** This reduces the **Insurance Risk Profile** for urban operators, potentially lowering premiums by 15%.
>     

---

## 4. Deadline Timeline to May 2028 Start

- **June 2026 – Dec 2026:** Complete **Gridlines Free Modeling** and start a monthly LinkedIn "Deep Tech Analysis" post.
    
- **Jan 2027 – June 2027:** Apply for **Vencapital** or **Hello Tomorrow** virtual fellowships. These are often remote and low-cost/free for students.
    
- **July 2027 – Dec 2027:** Build your **SORA-compliant portfolio**. Document one academic experiment as if it were a commercial safety case.
    
- **Jan 2028 – March 2028:** High-activity application period for **Technical Associate** or **Consultant** roles in UAE, Australia, or Belgium.
    
- **May 2028:** **Start Date.**
    

**Would you like me to help you draft a "Cold Outreach" email template specifically for a PhD student to send to a VC Partner?**

This [Drone Pilot Portfolio Guide](https://www.youtube.com/watch?v=4_I7LO0PpZ4) explains how to shift your mindset from what _you_ find interesting in your research to what a _client or investor_ wants to see in a professional portfolio.

VC firms don't "open funds" like a store; they follow a **Capital Lifecycle** that lasts about 8–10 years. For companies like **DRONE FUND**, this cycle is the most important indicator of when they will hire a PhD expert like you.

### 1. The Fund Cycle: When to Time Your Application

VCs raise money in "vintages." A new fund (e.g., Fund IV) usually goes through three phases:

|**Phase**|**Duration**|**Hiring Potential for You**|
|---|---|---|
|**Fundraising**|6–12 Months|**Low:** They are busy talking to investors (LPs) to get the money.|
|**Deployment**|2–4 Years|**CRITICAL:** They have "Fresh Dry Powder" (money to spend). They need Technical Advisors to vet 30–50 new startups.|
|**Management**|4–6 Years|**Moderate:** Focus shifts to helping existing portfolio companies grow.|

### 2. Specific Prediction for DRONE FUND

- **Fund I (2017):** $15M — _Deployment completed._
    
- **Fund II (2018):** $45M — _Deployment completed._
    
- **Fund III (2020/2021):** $90M — _Currently in the Management phase._
    
- **Prediction for 2028:** By the time you graduate in May 2028, DRONE FUND will likely be at the peak deployment of **Fund IV** or the very beginning of **Fund V**.
    
- **Strategy:** You want to join a firm right as they announce a **New Fund**. This is when they have the budget for a new high-salaried PhD Technical Associate.
    

---

### 3. Industry "Budget Cycles" (The May 2028 Deadline)

Beyond VC fund launches, the global corporate world follows seasonal hiring patterns. To start in **May 2028**, you must align with these:

- **Q1 (Jan–March 2028): The "New Budget" Surge.**
    
    In the UAE, Japan, and Australia, corporate budgets are refreshed in January. This is the **most active hiring window**. You must have your offer signed by **February 2028** to allow for visa processing.
    
- **Q2 (April–May 2028): The "Pre-Summer" Push.**
    
    Companies want to fill roles before the summer slowdown (EU/UAE) or the end of the Australian financial year (June 30).
    

---

### 4. Your "No-Fund" Networking Strategy

Since you cannot attend expensive meetings, you must use the **"White Paper Ticket"** method:

1. **Track their Portfolios:** VCs don't just have funds; they have "Portfolio Days."
    
2. **The "Expert Review":** Look at a company DRONE FUND recently invested in (e.g., _Wingcopter_).
    
3. **The Cold Move:** Write a 2-page "Technical Analysis" of the communication challenges that company will face in 2028 urban environments.
    
4. **The Delivery:** Send it to a Partner at DRONE FUND on LinkedIn.
    
    - _Message:_ "I'm a PhD at [University] researching the exact bottleneck your portfolio company [X] will face in 2 years. I've drafted a technical mitigation brief for your team. No call needed, just wanted to share the research."
        

> **Why this works:** VCs are obsessed with "Proprietary Deal Flow" and "Technical Moats." By doing their work for them (Due Diligence), you become a "high-value asset" before you even apply.

### 5. Final Safety Net: "The Consulting Bridge"

If you don't have a firm offer by **March 2028**, immediately register as a **Freelance Technical Consultant** in Germany (using your post-study search visa).

- **Service:** "BVLOS Spectrum & Link-Safety Audits for Investors."
    
- **Value:** This keeps your "Professional" status active while you continue to hunt for a full-time Venture Partner role.
    

**Would you like me to find the exact "Investment Thesis" of DRONE FUND III so you can see the specific technical gaps they are looking to fill in their next fund?**


# Transitioning from science to venture capital

[Chiara Decaroli, PhD](https://ch.linkedin.com/in/chiara-decaroli-phd-388aa187)!

### Chiara Decaroli, PhD

Published Jun 19, 2024

[+ Follow](https://www.linkedin.com/signup/cold-join?session_redirect=%2Fpulse%2Ftransitioning-from-science-venture-capital-chiara-decaroli-phd-zctae&trk=article-ssr-frontend-pulse_publisher-author-card)

It's been almost a year since I have transitioned to the world of venture capital. Over the past months, several of you have approached me to ask me what it takes to make the jump from a science/technology profession to VC. Here I am collecting my thoughts which I hope will guide you in your future steps.

### How to transition from science to VC

First of all, I have an academic background in Physics, with a PhD in quantum computing. However, during my PhD years I enjoyed experimenting and joined the entrepreneurship and consulting clubs at ETH Zurich, carrying out 6-months projects with both. With the ETH entrepreneurship program I came up with a startup idea, assembled and led a team to go through the initial phases of ideation, market research, business model creation and product design. With the consulting club I led a group in finding and presenting more efficient pathways for engagement and marketing for one of the leading healthcare non-profit organisations in Switzerland.

I also founded a number of initiatives, focused on interdisciplinarity (The Art & Science Collective: a community mixing scientist and artists in creative workshops and exchanges, Interdisciplinary Interactions: a community bringing together senior professors and intellectuals and younger students across disciplines) and EDI & women in science (Honggerberg ladies lunches: a community for female students in science at ETH meeting once a month for connection). All these involved a ton of 1. fundraising and looking for sponsors, 2. marketing 3. leading teams 4. product design 5. strategy and organisation.

This is all to say that despite being deeply focused on quantum computing and science, I also seeked and exposed myself to activities which involved entrepreneurship at its core. If you are interested in a career either in the startup world or in the "supporting" startups world (VC, PE, CVC etc), I highly recommend engaging in these types of projects and activities to broaden your horizons and get your hands dirty. You can simply start a community, or a project around a passion of yours, and follow its journey to gain skills and insights into what it takes to "start your own business". Of course this might come with a cost, especially if you are surrounded by people who don't "get" the value of not working on a single topic 24/7! In my case reading in a colleague's thesis acknowledgement "I thank CD for reminding us there is more than work in life", while everyone else was thanked for technical help ;)

After my PhD I joined the UK's National Quantum Computing Centre as one of its first employees. Truth be told, these were the early days, we were a team of 6 and were operating in a mode much closer to a startup than an established organisation. I was involved in all main activities and got exposure into the broader UK quantum ecosystems. This was the first step in enlarging and deepening my view of the landscape beyond my expertise (i.e. trapped ions and a handful of well-known full-stack QC companies).

When I applied to Redstone's investment manager role I had with me not only technical knowledge in quantum tech, but also a really good understanding of the UK and broader EU quantum landscape, all its actors, major stakeholders and dynamics. I also had interacted already with many startups and had an extensive academic network. All these ingredients turned out to be fundamental in the job (and in getting selected for it!). So if you'd like to end up in VC, but are just coming out of academia, my suggestion is to potentially consider a role first that gives you a broad understanding of the field, research the landscape, & absolutely make connections outside of your narrow field.

To summarise, if you'd like to transition from science to VC here are my main tips on making the move as successful as possible:

1. have some sort of first-hand entrepreneurship experience - you will need this to connect, understand and assess founders.
2. build a broad understanding of the landscape of a specific field, including startups, market actors, regulator bodies, government positions and latest trends.
3. create a network in the field you're interested in - don't just hang out with your peers in the lab, they know 90% of the same stuff as you!
4. try out a role in consulting/strategy/government or similar that allows you to gain any of the above.

### What does it mean to work in VC

Now, moving on to the job, what it looks like and what makes me like it (aka the questions you guys keep asking!). There are many different roles in the VC industry, starting out with roles that involve more analysis or scouting to more strategic and leadership roles where your opinions and decisions on a specific topic really matter. Depending on the size of the firm, these roles might be less distinct.

My job as an investment manager involves broadly:

a. scouting startups and building a comprehensive view of the landscape in quantum tech, creating a startup funnel and pipeline

b. understanding the market dynamics, market potential/timing and pull for all quantum technologies

## Recommended by LinkedIn

[![From Lab to Launch: Do's, Don'ts & Mindset Shifts for Aspiring Biotech Founders in India](https://media.licdn.com/dms/image/v2/D5612AQGXkOmLn5e74A/article-cover_image-shrink_720_1280/B56Zg2Dn0ZHMAI-/0/1753253576782?e=2147483647&v=beta&t=Cgwww5RYqybQrEL_dLKWkdsaySeum8M95pkcskjFMUw)

From Lab to Launch: Do's, Don'ts & Mindset Shifts for…

Amit Pandey  6 months ago

](https://www.linkedin.com/pulse/from-lab-launch-dos-donts-mindset-shifts-aspiring-biotech-amit-pandey-dowfc)

[![Funding Alone Won’t Save Your Deep Tech Startup—The Right Strategy Will](https://media.licdn.com/dms/image/v2/D4E12AQFAigJSD6Y3-w/article-cover_image-shrink_720_1280/B4EZUPu49AHUAI-/0/1739725708632?e=2147483647&v=beta&t=2ab7Q-YURVX70gULmfMtCbiQIqC461tRvNG6nvzu00o)

Funding Alone Won’t Save Your Deep Tech Startup—The…

Maria Ksenia Witte  11 months ago

](https://www.linkedin.com/pulse/funding-alone-wont-save-your-deep-tech-startupthe-right-witte-gfxke)

[![Altitude Lab: The Accelerator Leading Utah’s Biotech Investment](https://media.licdn.com/dms/image/v2/D5612AQHQl52mLF58xw/article-cover_image-shrink_720_1280/B56Zfq4.gtGQAI-/0/1751992497706?e=2147483647&v=beta&t=OwDrMb1EMY5DmZUGMj2oOasHap6UW8rYoW4K34-JN0k)

Altitude Lab: The Accelerator Leading Utah’s Biotech…

Utah Governor's Office of Economic Opportunity  6 months ago

](https://www.linkedin.com/pulse/altitude-lab-accelerator-leading-utahs-biotech-investment-hjstc)

c. understanding and beging able to assess the technology - leveraging the help of experts where needed

d. writing (a lot!) reports on each startup that is promising, conducting DD (Due Diligence) involving reference calls with market actors

e. talking to all founders, multiple times, discussing all aspects of their company (tech, business, product, team, IP, funding rounds). Assess and select the most promising opportunities

f. presenting the most interesting opportunities to the IC (Investment Committee), advocating for your selection and discussing with them where to dig deeper

g. discussing funding rounds, valuation, term sheets -have an understanding of "realistic" benchmarks within the industry (i.e. what other similar stage companies have raised and are valued at?) and being able to negotiate deals

h. being involved in fundraising for the fund, so you can keep going and invest in the space

In essence, you need to be able to have a deep and broad understanding of technology, markets, commercialisation but also critically be able to judge people and teams, their motivation, their strengths and weaknesses, and their potential. You need to love interacting and talking to people, as a large fraction of your job will be devoted to this. You need to have an interest in building and scaling businesses as you'll be supporting startups in your portfolio with these and any challenges they might have. And you need to stay on top of latest news, trends and breakthroughs. I also think that being decisive, having strong opinions (not too weakly held, as you'll have to advocate for your choices) and being persuasive are fundamental aspects of the job. Finally being able to connect with people, to pick up on their motivations, to be able to "read" them and to establish relationships based on trust, mutual respect and transparency. You will be making recommendations for investment based on well thought-out, evidence-based arguments, paired with intuition, character-understanding and sixth sense for potential.

### A few last words

It is not a job for everyone (it's fast-paced, there is a lot of "content-switching" and little time to prepare for every call, and there is a fair amount of travel involved), but it is a job that will provide you with insights into a field as no other job will, it will allow you to be a part of many different teams building many different products, facing many different challenges and to truly understand the levers that influence the development of technology and innovation.

Deep tech is becoming more and more interesting for VC firms and family offices. To properly assess deep tech startups, a technical background is essential and you will be an asset to the teams, complementing your skills and knowledge with those of colleagues coming from a finance, business or start-up background.

  

Hoping this is of help if you are considering venturing into venture capital ;) I wish you luck on your journey into this fast-paced fascinating world, and for any follow up questions please leave a comment below, and I'll do my best to answer

To listen : https://www.fiftyyears.com/speed

https://www.amazon.com/The-Rare-Find-Talent-Stands/dp/1591845629

Point of hiring VCs

- Growing demand for domain expertise in emerging technologies 
- Recognition of the value of interdisciplinary perspectives



https://e-courses.epo.org/

While there isn't a direct "one-to-one" carbon copy named "Germany:Blend," Germany has a very robust network of organizations that perform the same function: **diversifying the VC talent pipeline** and supporting underrepresented founders through data, fellowships, and networking.

Here are the most potent equivalents in Germany that align with your 2028 "Venture Partner" goal.

---

## 1. encourageventures e.V.

This is perhaps the closest spiritual successor to Chicago:Blend in Germany.

- **Focus:** An all-female network of over 750 investors and mentors.
    
- **Function:** They bundle capital and expertise to support female-led startups.
    
- **For You:** If you are a woman in engineering, this is the premier network for "Capitalist Advising" in Germany. They provide the exact "mentorship + capital" bridge you're looking for.
    

## 2. KfW Capital (Emerging Manager Facility)

KfW is Germany's state-owned investment bank, and they act as the "engine" for VC diversity at a systemic level.

- **The Program:** Their **Emerging Manager Facility** specifically funds smaller VC firms managed by women or gender-diverse teams.
    
- **The Fellowship:** They offer the **"KfW Capital Fellowships Women in VC,"** which pays for the **Certified Private Equity Analyst (CPEA)** training at TU Munich—a perfect certification for your 2028 CV.
    

## 3. Investors4Diversity (I4D)

This is an initiative specifically aimed at the institutional level of German finance.

- **Focus:** They push for gender-balanced management in the top 30 most influential institutional investors in Germany.
    
- **For You:** This is an excellent source for the "Statistics and Data" you need to understand the German market landscape.
    

## 4. Auxxo Female Catalyst Fund

While it is a fund, it operates with a heavy "ecosystem-building" mindset similar to Chicago:Blend.

- **Focus:** Investing in European startups with at least one female founder.
    
- **Networking:** They are a core node in the Berlin "Deep Tech" scene and frequently host events that bridge technical PhDs with investment teams.
    

---

### Comparison: Chicago:Blend vs. German Initiatives

|**Feature**|**Chicago:Blend**|**German Equivalent(s)**|
|---|---|---|
|**Venture Fellowship**|4-month cohort for aspiring VCs|**KfW Capital Fellowship** (CPEA track)|
|**Diversity Data**|Annual VC Diversity Survey|**Investors4Diversity** / German Startup Monitor|
|**Underrepresented Focus**|Women, BIPOC, Non-binary|**encourageventures** / **Auxxo**|
|**Funding Source**|Non-profit / Donations|**Public-Private Partnership** (KfW / EIF)|

---

### Strategy for a PhD Applicant

If you want to use these networks to avoid the "Academic Trap" in Germany:

1. **Join encourageventures:** Even as a student, you can apply as a "Young Talent" or volunteer for their technical screening committees.
    
2. **Apply for the KfW Fellowship:** Target this in 2027. It is the most prestigious way to get the "Capitalist" label on your CV for free.
    
3. **Use the "Berlin Factor":** Almost all these organizations are headquartered in Berlin. Even if your PhD is in another city, your "Digital Networking" should be focused here.
    

**Would you like me to find the application deadlines for the 2027 KfW Capital Fellowships so you can put them in your calendar?**

[Diversity in Venture Capital](https://www.youtube.com/watch?v=suWaG-CR7RA)

This video from Chicago:Blend illustrates their mission of increasing diversity in the VC ecosystem, which mirrors the goals of German initiatives like encourageventures and KfW Capital's diversity programs.

In 2026, Japan has emerged as the most rapidly maturing venture capital (VC) market in Asia. For a PhD holder like yourself, the Japanese ecosystem is particularly attractive because, unlike Silicon Valley which often favors software/apps, Japan’s VC surge is heavily concentrated in **Deep Tech, Robotics, and Physical AI**—the exact domains of your BVLOS and drone research.

---

## 1. Top VC Offices in Japan (The Power Players)

Most VC activity is concentrated in **Tokyo** (specifically the Minato, Shibuya, and Chiyoda wards).

|**Firm Type**|**Key Players**|**Investment Focus**|
|---|---|---|
|**Independent VC**|**Global Brain**, **Coral Capital**, **ANRI**, **Incubate Fund**|Seed to Late-stage; very aggressive in Deep Tech.|
|**Academic-Linked**|**UTEC (University of Tokyo Edge Capital)**|**The Gold Standard** for PhDs. They specifically fund university-born tech.|
|**Corporate VC (CVC)**|**NTT DOCOMO Ventures**, **Sony Innovation Fund**, **SoftBank**|Strategic alignment with telecom/electronics infrastructure.|
|**Government-Backed**|**JIC (Japan Investment Corporation)**|Managing trillions of yen to solve social issues via technology.|

---

## 2. Why Japan has "More" VC Companies Recently

The "Boom" you are seeing in 2026 is the result of a deliberate, multi-year national strategy.

### A. The "10-10-10" Government Stimulus

In 2022, the Japanese government launched a **5-year plan** with a goal of **¥10 trillion ($67B)** in startup investment by 2027.

- **The Result:** Massive amounts of public money have been funneled into private VC funds to "de-risk" investments in difficult hardware (like drones).
    

### B. The Rise of the "CVC" (Corporate Venture Capital)

Japan has a unique density of giant conglomerates (Toyota, Panasonic, Hitachi). In the last 3 years, these companies realized they couldn't innovate fast enough internally.

- **The Trend:** Almost every major Japanese corporation now has its own VC office. This creates a "higher number" of firms compared to countries that rely mostly on independent VCs.
    

### C. The "Deep Tech" Pivot

Global investors are moving away from software toward "Real-Tech." Japan has:

- **Manufacturing Moats:** Unbeatable expertise in sensors, motors, and robotics.
    
- **The Silver Economy:** A shrinking population that _must_ use drones and robots to survive, creating a guaranteed domestic market that VCs love.
    

---

## 3. The "PhD Advantage" in Japan

Japan is one of the few places where the **"Dr." title** on a VC team is not just a bonus—it’s a requirement for credibility.

- **Lower Competition:** While thousands of MBA students fight for VC roles in the US, there are relatively few PhDs in Japan who understand both "Link-Budgets" and "Term Sheets."
    
- **Global Bridge:** Japanese VCs are desperate to expand internationally. An Indian PhD from Germany is seen as a **"Global Navigator"** who can help a Japanese fund invest in European or Australian startups.
    

---

## 4. Strategic "Next Steps" for 2028

### Get on the "SusHi Tech" Radar

Tokyo now hosts a massive annual event called **SusHi Tech Tokyo** (Sustainable High City Tech).

- **Action:** Target the **2027 SusHi Tech Challenge**. Even if you go as a student, it is the highest-density networking event for Japanese VCs and global "Deep Tech" founders.
    

### Target "J-STARX" & "J-Find"

- **J-Find Visa:** As a graduate of a top-tier global university, you may qualify for this specific job-seeking visa which allows you to stay in Japan for up to 2 years to find a role in the startup ecosystem.
    

### High-Value Next Step

Would you like me to look for the **portfolio companies of UTEC (University of Tokyo Edge Capital)** that specialize in aerial communications? This would give you a list of "sister companies" where you could potentially do a 3-month consulting project during your PhD.

https://www.ut-ec.co.jp/english/recruit/utec/

UTEC (University of Tokyo Edge Capital) is one of the most prestigious deep-tech VCs in Asia. Because they are the "preferred" VC for the University of Tokyo, their portfolio focuses on hardware and physical systems where **Aerial Communication** is not just a feature, but the core "moat."

For your PhD background, the following UTEC portfolio companies are the most strategic targets for a technical advisor or venture partner role by 2028:

---

## 1. ACSL (Autonomous Control Systems Laboratory)

ACSL is the "crown jewel" of UTEC’s drone portfolio. They are a spin-off from Chiba University and were the first drone manufacturer to list on the Tokyo Stock Exchange (TSE).

- **The Tech:** They specialize in **proprietary flight controllers** (SOTEN) that do not rely on Chinese-made components, making them the top choice for government and security contracts.
    
- **BVLOS Connection:** Their drones are designed for "Level 4" flights (autonomous flight over populated areas). They rely heavily on redundant, secure C2 (Command and Control) links.
    
- **Your Value:** They need experts to validate their secure communication protocols for international markets (like the US and EU).
    

## 2. ePlane (Ubifly Technologies)

Based in India but backed by UTEC, ePlane is developing electric Vertical Takeoff and Landing (eVTOL) aircraft.

- **The Tech:** Aiming to create the "world's most compact flying taxi" for urban commutes.
    
- **Aerial Comms Focus:** In a dense city like Mumbai or Tokyo, eVTOLs require hyper-reliable, low-latency communication links to prevent mid-air collisions.
    
- **Your Value:** Your PhD research on urban BVLOS interference is directly applicable to their urban air mobility (UAM) safety case.
    

## 3. Metro Weather

While not a drone maker, they are an essential "Enabling Infrastructure" company in UTEC's portfolio.

- **The Tech:** They develop **Doppler LiDAR** systems that map "wind corridors" in 3D in real-time.
    
- **Aerial Comms Focus:** Wind conditions directly affect signal propagation and drone stability. Integrating weather data into the communication link allows for "predictive signal management."
    
- **Your Value:** Bridging the gap between atmospheric data and signal reliability for BVLOS missions.
    

## 4. Medcom

This company focuses on **Hospital DX** and building communication infrastructure.

- **The Tech:** While they started with internal hospital communications, they are expanding into the "Medical Drone" space—delivering blood and organs between hospitals.
    
- **Aerial Comms Focus:** These missions require "zero-fail" communication links to ensure life-saving payloads are tracked every second.
    
- **Your Value:** Designing the high-reliability link-budgets for medical BVLOS corridors.
    

---

### Comparison of UTEC Opportunities for a PhD Specialist

|**Company**|**Core Technical Challenge**|**Strategic Role for You**|
|---|---|---|
|**ACSL**|Anti-jamming / Secure C2 Links|**Standardization Lead** (ISO/IEEE compliance)|
|**ePlane**|Urban Interference & Latency|**Systems Architect** (UAM Link design)|
|**Metro Weather**|Data-Link Integration|**Technical Advisor** (Weather-Signal algorithms)|
|**Medcom**|High-Uptime Critical Comms|**Operations Manager** (Safety-case certification)|

---

### How to use this for your "2028 Plan"

1. **Academic Outreach (2026):** Since you are in a German PhD program, check if your lab has any ties to the **University of Tokyo Graduate School of Engineering**. UTEC often facilitates research collaborations between their startups and international labs.
    
2. **The "Industrial PhD" Pitch:** Reach out to ACSL or ePlane’s CTO on LinkedIn. Offer to use their platform as a "case study" for your research in exchange for data. This is a "free" way to get industry experience.
    
3. **Target the "UTEC 6" Fund:** UTEC recently launched a **$326M fund (UTEC 6)** in 2025. By 2028, they will be looking for "Technical Associates" to manage the growth of the companies they are funding _right now_.
    

**Would you like me to find the contact details of the UTEC "Physical Sciences" investment team so you can follow their specific investment theses on LinkedIn?**

### Priority jobs

1. VC 
2. Project management roles in Tech - drone companies 
3. Tech specialist and project in Telekom companies 
4. R and D 

In 2026, Japan has one of the world's most organized venture capital ecosystems, characterized by a unique blend of **Independent VCs**, **Mega-Bank VCs**, and highly active **Corporate VCs (CVCs)**.

As of 2026, there are over **430 active investors** in Japan. Because listing all 437 is impractical, I have categorized the top-tier players by their "power" and relevance to your background in **Deep Tech, Telecom, and Drones.**

---

## 1. The "Big Three" Bank-Affiliated VCs

These are the most active investors by volume. They have deep pockets and often lead rounds.

- **SMBC Venture Capital:** Consistently the #1 most active investor (170+ investments in recent cycles).
    
- **Mitsubishi UFJ Capital (MUCAP):** Strong focus on ICT, high-tech, and life sciences.
    
- **Mizuho Capital:** Heavily invested in IT and biotechnology with a massive track record of IPOs.
    

## 2. Top Independent VCs (Deep Tech & Global Focus)

These firms are more "entrepreneur-friendly" and often have specialized technical partners.

- **Global Brain Corporation:** One of the largest independent firms; invests in everything from AI to ClimateTech.
    
- **JAFCO Group:** The "veteran" of Japanese VC. They do everything from seed to buyouts.
    
- **Coral Capital:** The "Silicon Valley style" firm in Tokyo. Very influential in the seed-stage ecosystem.
    
- **ANRI:** A leader in seed-stage deep tech (including fusion, robotics, and drones).
    
- **Incubate Fund:** Focuses on being the first investor in a startup (Seed/Founding stage).
    
- **Genesia Ventures:** Focuses on the Japan-Southeast Asia bridge.
    

## 3. Academic & "Sovereign" VCs (Your PhD Backyard)

These firms specifically look for PhD-led research and science-heavy startups.

- **UTEC (University of Tokyo Edge Capital):** The premier deep-tech fund. If your tech is hard to build, you go here.
    
- **JIC Venture Growth Investments (JIC-VGI):** A government-backed fund (Japan Investment Corporation) that targets "National Priority" technologies like drones and semiconductors.
    
- **Keio Innovation Initiative (KII):** Similar to UTEC but linked to Keio University.
    
- **Beyond Next Ventures:** Specializes in "commercializing science" (Deep Tech/Life Science).
    

## 4. Major Corporate VCs (The Drone Industry "Buyers")

In Japan, giants like Sony and Toyota don't just build products; they invest via their own funds.

- **NTT DOCOMO Ventures:** Crucial for your **Aerial Telecom** background.
    
- **Sony Innovation Fund:** Invests in sensing, robotics, and AI.
    
- **SoftBank Ventures Asia (ZVC):** Massive global reach in AI and physical robotics.
    
- **Woven Capital (Toyota):** Focuses specifically on the future of mobility and autonomous systems.
    
- **Panasonic Kurashi Visionary Fund:** Active in AI and robotics integration.
    

---

### Comparison: Where should a PhD start?

|**Category**|**Best For**|**Hiring Potential for PhDs**|
|---|---|---|
|**Academic (UTEC/KII)**|Hard Science / Patents|**High** (Need technical vetting)|
|**Independent (Coral/ANRI)**|Speed / Fast Growth|**Medium** (Need operational help)|
|**Corporate (NTT/Sony)**|Strategic Infrastructure|**High** (Need domain experts)|
|**Bank (SMBC/Mizuho)**|Scale / IPO|**Low** (Prefer finance backgrounds)|

---

### Why this matters for 2028:

By the time you graduate, the **"10-10-10" Government Plan** will have peaked, meaning these funds will be under pressure to show results from their deep-tech portfolios. They will need **Technical Associates** who can help their drone startups navigate global standards (SORA/ISO).

**Would you like me to find the "Technical Associate" job requirements for Global Brain or UTEC to see how they value a PhD versus an MBA?**

To broaden your scope beyond Japan and Germany, you should target regions that are actively "importing" deep-tech talent through specific visas and government-backed funds.

Here is the structured VC and career ecosystem for your **2028 May Deadline** in three high-potential regions.

---

## 1. United Arab Emirates (UAE): The "Fast-Track" Leader

In 2026, the UAE is the global hub for **AAM (Advanced Air Mobility)**. They have the highest concentration of "sovereign" wealth directed at drones.

- **The Structure:**
    
    - **Sovereign/Strategic:** **ADIO (Abu Dhabi Investment Office)** and **ASPIRE** (under ATRC). They don't just invest; they build the infrastructure you'd audit.
        
    - **Hubs/VCs:** **Hub71** (Abu Dhabi) and **Oraseya Capital** (Dubai). These are the "gatekeepers" to the startup ecosystem.
        
    - **Regional VCs:** **Shorooq Partners** and **BECO Capital**. They are increasingly moving into Deep Tech and Logistics.
        
- **The "PhD Move":** Apply for the **10-Year Golden Visa**. As a PhD in Engineering, this is almost guaranteed. It allows you to work as an independent **Venture Partner** without a specific employer tie.
    
- **Timeline Advantage:** Visa processing is often <1 month.
    

## 2. Australia: The "BVLOS Lab"

Australia has vast unpopulated land and a very progressive regulator (CASA), making it the world's best place for long-range drone testing.

- **The Structure:**
    
    - **Independent VCs:** **Blackbird Ventures** (the giant) and **Main Sequence Ventures**. Main Sequence was founded by the CSIRO (Australia's science agency) and _specifically_ hires PhDs to bridge the gap between lab and market.
        
    - **Industry/Project VCs:** **Carthona Capital** and **AirTree**.
        
    - **Government Nodes:** **Drones.gov.au** and the **Emerging Aviation Technology Partnerships (EATP)** program.
        
- **The "PhD Move":** The **Global Talent Visa (Subclass 858)**.
    
    - **Target Sector:** "Defence, Advanced Manufacturing, and Space."
        
    - **Benefit:** Direct Permanent Residency (PR).
        
- **Unique Asset:** If you have **SORA certification**, you can bypass the "academic" stigma immediately—Australia is desperate for SORA-trained safety architects.
    

## 3. Belgium: The "EASA Gateway"

If you want to stay in Europe but avoid the German "Language Trap," Belgium is the center of the **EASA (European Union Aviation Safety Agency)** regulatory universe.

- **The Structure:**
    
    - **Deep Tech Specialists:** **imec.xpand** and **imec.istart**. This is arguably the best deep-tech ecosystem in the world for hardware and connectivity.
        
    - **Regional VCs:** **Gimv** and **Capricorn Partners**.
        
    - **EU Hubs:** **Eurocontrol** (Brussels) and the **Antwerp DronePort**.
        
- **The "PhD Move":** The **EU Blue Card**. It is much easier to transition from a German student visa to a Belgian Blue Card than to a US H1-B.
    
- **Unique Asset:** Focus on **Standardization**. Being the person who understands the "U-Space" regulations for the EU makes you hireable by every VC in Europe.
    

---

### Comparison of 2028 Potential for an Indian Passport + PhD

|**Feature**|**UAE**|**Australia**|**Belgium**|
|---|---|---|---|
|**Visa Ease**|10/10 (Golden Visa)|8/10 (Global Talent)|7/10 (EU Blue Card)|
|**English Dominance**|100%|100%|90% (Technical)|
|**Drone Sector Focus**|Urban Air Taxis (AAM)|Mining & Long-range Agri|Logistics & EU Policy|
|**VC Hiring Style**|Needs "Advisors"|Needs "Operations"|Needs "R&D Strategists"|

---

### 5. Final Safety Net: The "Digital Nomad" Loophole

If you do not have a firm offer by **February 2028**:

1. **Register a "Global Advisor" LLC** in a low-tax jurisdiction (like Estonia/E-Residency or UAE Free Zone).
    
2. **Productize your PhD:** Sell "BVLOS Link Audits" as a service to VCs in these three regions.
    
3. **The Result:** You enter these countries not as a "job seeker" (which is hard for an Indian passport), but as a **Business Owner** or **Consultant**, which has much higher visa approval rates.
    

**Would you like me to find the specific "SORA training providers" in Belgium or Australia so you can get certified before your May 2028 deadline?**

To transition from an academic PhD to a **Tech Associate** (also known as a Venture Associate or Technical Analyst) in a venture capital firm, you must prove that you can move from "discovering knowledge" to "quantifying risk."

By May 2028, your profile must show that you are a **Business-Technical Hybrid**. Here is how to prepare for your three target markets.

---

## 1. Professional Experience: "The VC Proof"

In VC, "Experience" doesn't just mean a job; it means **Deal Flow, Sourcing, and Due Diligence.**

- **VC Internship or Fellowship:** Apply for remote fellowships (e.g., **VC Lab** or **Vencapital**) in late 2027. This puts a "finance" brand on your CV next to your PhD.
    
- **Startup Operator Role:** If you can’t get a VC internship, work part-time or volunteer for a **Seed-stage drone startup** (e.g., helping them with their FCC/EASA link-budget filings). This proves you understand "Startup Speed."
    
- **Industry Standards Work:** Join an IEEE or ISO working group. In your CV, list this as **"Standardization Strategy"** rather than "Committee Work."
    

## 2. Studies & Certifications: "The De-Risking Badge"

Academic papers are "proof of depth"; certifications are "proof of safety."

### **The "Capitalist" Studies (Global)**

- **Financial Modeling:** Complete the **Gridlines "Essential Financial Modelling"** course (Free). It teaches you to build Excel models for infrastructure—the language of VC.
    
- **Venture Capital Due Diligence:** Take a short course on **Technical Due Diligence** (Coursera or specialized VC bootcamps). Focus on "how to spot tech that won't scale."
    

### **The "Safety" Certifications (Target Specific)**

- **Belgium/EU:** **SORA 2.5/3.0 Training.** This is mandatory for BVLOS in the EU. Being a PhD who is also a certified SORA Practitioner makes you a "unicorn" for EU drone VCs.
    
- **Australia:** **CASA RePL (Remote Pilot Licence).** Even if you aren't a pilot, having this shows you understand the Australian legal airspace—a key risk factor for VCs.
    
- **Japan:** **Business Strategy for Robotics.** Focus on certificates that deal with "Physical AI" and manufacturing supply chains.
    

---

## 3. Language & Cultural Prep

To avoid the "Language Trap" you see in Germany, you must pivot your language focus based on the market.

|**Market**|**Language Priority**|**Cultural Strategy**|
|---|---|---|
|**Australia**|**English (Native/Fluent)**|Focus on "Plain English." Australian VCs value directness and "no-nonsense" technical summaries.|
|**Belgium**|**English + Business French**|The drone hub is in Wallonia/Brussels. You don't need French to _code_, but you need it to _network_ with local government funders.|
|**Japan**|**English + JLPT N3 (Minimum)**|In Japan, the PhD ("Hakase") is respected, but you need enough Japanese to participate in a "Nomikai" (after-work drinks) where 90% of VC deals are actually discussed.|

---

## 4. May 2028 Readiness Checklist

|**Category**|**Must-Have by Jan 2028**|**Why?**|
|---|---|---|
|**Portfolio**|**The "1-Page Deal Memo"**|A sample analysis of a real drone startup.|
|**Network**|**50 VC Connections**|Specifically Technical Partners at firms like ANRI (Japan) or Main Sequence (Australia).|
|**Visa**|**Eligibility Check**|J-Find (Japan), Global Talent (Australia), or Blue Card (Belgium).|

### **Your Next Step**

Would you like me to draft a **"Tech Associate" version of your CV**? I can show you how to rewrite an academic "List of Publications" into a **"Technical Due Diligence Portfolio"** that will get a VC Partner's attention.

https://www.angelschool.vc/blog/how-to-get-into-venture-capital-as-an-engineer

https://datadrivenvc.io/
Here are a few **venture capital professionals / investors connected to drone technology and autonomous systems** that you can explore. Note that _specific PhD + engineering + VC profiles focusing on civil drones_ are rare publicly, and many VCs with drone exposure come from broader aerospace/autonomy/defense investing — so I’ve included relevant VC investors with _LinkedIn profiles where available_, and noted where their public information relates to drones or unmanned systems:

---

### 🔎 **1. Kotaro Chiba — Founder/Managing Partner at DRONE FUND**

**Role:** Founder & Managing Partner at **DRONE FUND**, a Tokyo-based venture capital firm specializing in drone and air-mobility startups (seed to early-stage) with investments across global drone tech. ([LinkedIn](https://www.linkedin.com/in/kotaro-chiba-557bb7?utm_source=chatgpt.com "Kotaro Chiba - Private Pilot(FAA/Japan)🛩 / HondaJet ..."))

**LinkedIn:**  
➡️ [https://www.linkedin.com/in/kotaro-chiba-557bb7](https://www.linkedin.com/in/kotaro-chiba-557bb7) ([LinkedIn](https://www.linkedin.com/in/kotaro-chiba-557bb7?utm_source=chatgpt.com "Kotaro Chiba - Private Pilot(FAA/Japan)🛩 / HondaJet ..."))

**Notes:**

- While his academic background is _not uniquely listed as a PhD_, Kotaro is highly connected internationally in drone ventures, and often bridges tech/science/VC communities. ([DRONE FUND - DRONE FUND website](https://dronefund.vc/en/team/kotaro-chiba/?utm_source=chatgpt.com "Kotaro Chiba"))
    

---

### ⭐ **2. Shaun Maguire — Partner involved in drone investments (e.g., Neros & Skydio deals)**

**Role:** Venture Capital Partner (Sequoia Capital) with involvement in autonomous drone company financing (e.g., _Neros_). ([Reuters](https://www.reuters.com/business/aerospace-defense/drone-startup-neros-raises-funding-sequoia-eyes-supplies-ukraine-us-military-2024-05-20/?utm_source=chatgpt.com "Drone startup Neros raises funding from Sequoia, eyes supplies to Ukraine, US military"))

**LinkedIn:**  
➡️ [https://www.linkedin.com/search/results/all/?keywords=Shaun%20Maguire](https://www.linkedin.com/search/results/all/?keywords=Shaun%20Maguire)

**Notes:**

- Sequoia Capital isn’t a drone-specific VC, but Shaun has been publicly linked to drone sector rounds — strong for civil/autonomy investment profiles. ([Reuters](https://www.reuters.com/business/aerospace-defense/drone-startup-neros-raises-funding-sequoia-eyes-supplies-ukraine-us-military-2024-05-20/?utm_source=chatgpt.com "Drone startup Neros raises funding from Sequoia, eyes supplies to Ukraine, US military"))
    

---

### 📌 **3. Investors at Aerospace & Autonomy-Focused VCs**

These firms back drone tech companies; individual partners often have engineering or PhD backgrounds, though public LinkedIn will provide the specific profile details:

|**VC Firm**|**Focus**|LinkedIn Search to Try|
|---|---|---|
|**Andreessen Horowitz (a16z)**|Autonomous drones, UAV tech, AI|[https://www.linkedin.com/company/a16z](https://www.linkedin.com/company/a16z)|
|**Lux Capital**|Deep tech including robotics, drones|[https://www.linkedin.com/company/lux-capital](https://www.linkedin.com/company/lux-capital)|
|**Airbus Ventures**|Aviation & autonomous systems|[https://www.linkedin.com/company/airbus-ventures](https://www.linkedin.com/company/airbus-ventures)|
|**Bessemer Venture Partners**|Enterprise drone applications|[https://www.linkedin.com/company/bessemervp](https://www.linkedin.com/company/bessemervp)|
|**Founders Fund**|Defense & autonomy investments|[https://www.linkedin.com/company/founders-fund](https://www.linkedin.com/company/founders-fund)|

_Search these VC teams on LinkedIn to find individuals — many partners hold engineering or PhD credentials and lead UAV/autonomy investments._ ([Ellty](https://www.ellty.com/blog/drone-investors?utm_source=chatgpt.com "Drone Investors: 30+ Active VCs Funding UAV Startups - Ellty"))

---

### 🔍 **Tips to Locate More Specific Profiles (Engineering + PhD + Drone VC)**

Because current public sources don’t list a ready database of _PhD engineers working in VC solely on civil drone tech_, here’s how you can narrow down:

1. **Search LinkedIn by Keywords:**
    
    - Filters: _“PhD” + “Venture Capital” + “Drone” OR “UAV” OR “Autonomy”_
        
    - Add sectors like _“civil infrastructure drones”_, _“aerial robotics”_, or _“urban air mobility”_.
        
2. **Look at VC Funds with Drone Portfolios:**
    
    - Check partner teams at VC firms investing in aerial autonomy and then check individual bios for **engineering doctorates** (e.g., certain partners at a16z or Lux Capital have technical degrees).
        
3. **Explore Specialized Funds:**
    
    - Firms like **Unmanned.vc** (early-stage drone/defense VC) may have team pages worth checking for technical roles. ([Unmanned](https://unmanned.vc/?utm_source=chatgpt.com "Unmanned.vc | Early-Stage VC for Defence, Drone & Autonomous ..."))
        

---

### 🧠 Why It’s Rare to Find PhD / Civil Drone-Specific VCs Directly

- Most investors in drone tech come from **general tech, aerospace, defense, or robotics investing backgrounds**, not exclusively civil engineering drones.
    
- Many VCs leverage **technical advisors** (often PhDs) rather than the investors themselves holding doctoral engineering degrees.
    

---

If you want, I can help **generate a list of names with LinkedIn links** — just tell me if you want them filtered by geography (e.g., Europe vs US) or _civil drones (infrastructure, delivery, inspection)_ specifically.

Here’s what I found regarding **Unmanned.vc’s location** and **venture capital profiles with links or roles relevant to drones / unmanned systems in Southeast Asia and Europe**. Note: _specific PhD + engineering + VC roles focused on civil drones are rare publicly_, but the following are investors or fund leaders active in areas closely tied to **autonomous systems, UAVs/drones, defense/dual-use and robotics** (many will have strong technical backgrounds and some with engineering/PhD credentials you can verify on LinkedIn).

---

## 📍 **Unmanned.vc — Location & Focus**

**Unmanned.vc**

- A VC fund **based in Tallinn, Estonia**, focused on early-stage startups in _unmanned systems_, drones/UAV technology, AI, robotics, and defense-related tech. ([balticvc.com](https://www.balticvc.com/2025/08/estonian-unmannedvc-joins-to-estban.html?utm_source=chatgpt.com "Estonian Unmanned.vc joins to EstBAN"))
    
- Investment tickets ~€50,000 – €300,000 and backed by deep-tech partners such as Modirum Group with advisory expertise from drone/robotics engineers. ([balticvc.com](https://www.balticvc.com/2025/08/estonian-unmannedvc-joins-to-estban.html?utm_source=chatgpt.com "Estonian Unmanned.vc joins to EstBAN"))
    

---

## 🇪🇺 **European VC Investors / Leaders With Drone / Autonomous Systems Exposure**

Here are **VC professionals and investors** you can investigate on LinkedIn (with LinkedIn profile links where available). Many work at firms that invest in defense tech, autonomy, robotics, or dual-use drone technology — closely related to civil UAV systems:

### 🔹 **Dr. Daniel Carew**

- **LinkedIn:** [https://www.linkedin.com/in/daniel-carew](https://www.linkedin.com/in/daniel-carew)
    
- _Investor / VC_ focused on European defense and technology startups; active as an early-stage investor and board member for tech ventures. ([LinkedIn](https://uk.linkedin.com/in/daniel-carew?utm_source=chatgpt.com "Dr. Daniel Carew - European Defence VC"))
    
- Likely background includes engineering or technical strategy — verify PhD/technical credentials on profile.
    

### 🔹 **Danilashaposhnikov — Partner at Phystech Ventures**

- **LinkedIn:** [https://www.linkedin.com/in/danilashaposhnikov](https://www.linkedin.com/in/danilashaposhnikov)
    
- Partner at **Phystech Ventures**, a VC backing deep-tech hardware and autonomous systems (Phystech invests in robotics, aerospace, AI). ([LinkedIn](https://ae.linkedin.com/in/danilashaposhnikov?utm_source=chatgpt.com "Daniel Shaposhnikov‏ - ‏Partner at Phystech Ventures"))
    
- Search his activity for UAV/autonomy investments.
    

### 🔹 **Uwe Horstmann — General Partner at Project A Ventures (Berlin)**

- **LinkedIn search:** [https://www.linkedin.com/search/results/all/?keywords=Uwe%20Horstmann](https://www.linkedin.com/search/results/all/?keywords=Uwe%20Horstmann)
    
- Project A has been active in defense-tech and related autonomous systems (backer of drone startups such as Stark / Quantum Systems leadership connections). ([Sifted](https://sifted.eu/articles/stark-hire-project-a-defence?utm_source=chatgpt.com "Defence tech Stark hires Project A investor Uwe ..."))
    

### 🔹 **Technical Advisors / Investors Linked to Unmanned.vc Advisory**

(Unmanned.vc has strong industry advisors with engineering and UAV expertise — valuable VC-ecosystem contacts): ([Unmanned](https://unmanned.vc/about-us?utm_source=chatgpt.com "About Us | Strategic Investment in Defence Sector Startups"))

- _Elias Silvola_ — Tech leader at Modirum | Gespi (deep tech & autonomous systems).  
    LinkedIn: [https://www.linkedin.com/search/results/all/?keywords=Elias%20Silvola](https://www.linkedin.com/search/results/all/?keywords=Elias%20Silvola)
    
- _Ellis Huber_ — UAV design expert, co-founder 2RAW Aerials.  
    LinkedIn: [https://www.linkedin.com/search/results/all/?keywords=Ellis%20Huber%202RAW%20Aerials](https://www.linkedin.com/search/results/all/?keywords=Ellis%20Huber%202RAW%20Aerials)
    
- _Joshua Henriques_ — Tech & engineering lead at Modirum Platforms.  
    LinkedIn: [https://www.linkedin.com/search/results/all/?keywords=Joshua%20Henriques%20Modirum](https://www.linkedin.com/search/results/all/?keywords=Joshua%20Henriques%20Modirum)
    

> These advisors typically have engineering or technical R&D experience in unmanned systems, valuable when paired with VC investing.

---

## 🇸🇬 / 🌏 **Southeast Asia VC Investors with Potential Drone / Deep Tech Exposure**

The SEA VC ecosystem isn’t exclusively drone-focused, but several firms and leaders invest in **deep tech, robotics, AI, logistics automation, and autonomous hardware systems** — _often relevant to civil drone markets_ (e.g., logistics, inspection, smart cities):

### 🔹 **Golden Gate Ventures (Singapore)**

- **LinkedIn:** [https://www.linkedin.com/company/golden-gate-ventures/](https://www.linkedin.com/company/golden-gate-ventures/)
    
- Singapore-based VC investing broadly in SEA tech — while not drone-specific, they back deep-tech robotics/enterprise tech where drone startups often participate. ([Wikipedia](https://en.wikipedia.org/wiki/Golden_Gate_Ventures?utm_source=chatgpt.com "Golden Gate Ventures"))
    
- Founders include _Vinnie Lauria_, _Jeffrey Paine_, _Paul Bragiel_ — search LinkedIn for their profiles.
    

### 🔹 **Synexia Ventures / NTT DOCOMO Ventures**

- **LinkedIn:** [https://www.linkedin.com/search/results/all/?keywords=Synexia%20Ventures](https://www.linkedin.com/search/results/all/?keywords=Synexia%20Ventures)
    
- New SEA venture arm targeting **AI, IoT, robotics, and drones** across Singapore, Indonesia, Malaysia, Philippines. ([LinkedIn](https://www.linkedin.com/posts/mohanbelani_ntt-group-launches-southeast-asia-venture-activity-7394285182138204160-I_rB?utm_source=chatgpt.com "NTT Group Launches Synexia Ventures in Southeast Asia - LinkedIn"))
    
- Leadership like **Alan Kuan Hsu** (former KK Fund) blends VC with tech deep-tech focus.
    

---

## 📌 How to Find More Specific “PhD + Engineering + Drone VC” Profiles

Since most VC profiles don’t explicitly list PhD credentials alongside drone focus in public listings, here’s a LinkedIn search syntax you can use directly for more targeted results:

🔍 **LinkedIn search string (copy/paste):**

```
“PhD” AND (venture capital OR VC) AND (drone OR UAV OR unmanned OR autonomy) AND (Europe OR Southeast Asia)
```

This will help locate individuals with documented PhDs and VC roles tied to autonomous systems & drone tech.

---

If you’d like, I can compile a **ready-to-use LinkedIn search list of specific names** (e.g., partners, principals) from firms like **Final Frontier, Draper Associates, Project A, Lux Capital** and others known to invest in dual-use drones — just let me know which region or subsector (civil inspection drones vs defense tech drones) you want prioritized!

Here’s a more **focused list of notable VC investors or investment leaders in East and Southeast Asia** with **links to their LinkedIn profiles where possible**, plus context on relevant VC initiatives in the region that could intersect with _civil drones, UAVs, robotics, autonomy, or related deep tech_. Many of these investors operate in deep-tech/AI/robotics/innovation sectors where _drone startups often get funding and strategic support_ — especially in SEA and East Asia.

---

## 🇸🇬 **Singapore & Southeast Asia — VC Investors (with LinkedIn)**

### **1. Daniel Tay — Vice President, Emerging Technologies, Temasek**

📍 **LinkedIn:** [https://www.linkedin.com/in/danieltaywl](https://www.linkedin.com/in/danieltaywl)

- Vice President in **Emerging Technologies** at Singapore’s **Temasek** (global investment firm). He has experience across science, R&D, product development and early-stage investing, often intersecting deep tech sectors inclusive of automation and spatial computing (which dovetails with advanced UAV/autonomy themes). ([LinkedIn](https://sg.linkedin.com/in/danieltaywl?utm_source=chatgpt.com "Daniel Tay - Deep Tech Investor, VC"))
    

---

### **2. Theodora Lai — Co-Founder & Partner, Moringa Ventures**

📍 **LinkedIn:** [https://www.linkedin.com/in/theodoralai](https://www.linkedin.com/in/theodoralai)

- Co-founder and partner at **Moringa Ventures**, an early-stage investor focused on _technology and deep tech startups_ across SEA — a network that often backs robotics, AI, and autonomous system innovations. ([LinkedIn](https://sg.linkedin.com/in/theodoralai?utm_source=chatgpt.com "Theodora Lai - Co-Founder and Partner, Moringa Ventures"))
    

---

### **3. Alan Ang — Global VC (SEA, China, US, India)**

📍 **LinkedIn:** [https://www.linkedin.com/in/alanangjw](https://www.linkedin.com/in/alanangjw)

- VC investor active across **frontier tech**, including AI, robotics and other areas that overlap with _drone autonomy, sensor fusion, and embedded systems_. His investments span China, Singapore/SEA and the U.S., providing cross-region visibility for deep tech founders. ([LinkedIn](https://sg.linkedin.com/in/alanangjw?utm_source=chatgpt.com "Alan Ang - Global VC (China, US, SEA, India)"))
    

---

### **4. Khailee Ng — Managing Partner, 500 Global**

📍 **Wikipedia profile (linked)**: [https://en.wikipedia.org/wiki/Khailee_Ng](https://en.wikipedia.org/wiki/Khailee_Ng)

- Malaysian venture capitalist with **500 Global**, one of SEA’s most active early stage VC firms. While not drone-exclusive, _500 Global invests broadly in tech including AI and robotics spaces_, which are relevant to UAV startups. ([Wikipedia](https://en.wikipedia.org/wiki/Khailee_Ng?utm_source=chatgpt.com "Khailee Ng"))
    

---

## 📌 **Venture Firms / Programs in SEA with Drone/Deep-Tech Relevance**

These organizations don’t all have publicly listed individual partners with PhDs but are key investing entities in deep tech where drones often reside — good leads for finding specific technical VCs:

### **5. Synexia Ventures (NTT Group – SEA)**

- A new **NTT DOCOMO Ventures**-backed regional fund targeting **AI, IoT, smart cities, robotics and drones** across SEA (Singapore, Malaysia, Indonesia, Philippines). Leadership includes Alan Kuan Hsu (LinkedIn search available). ([LinkedIn](https://www.linkedin.com/posts/mohanbelani_ntt-group-launches-southeast-asia-venture-activity-7394285182138204160-I_rB?utm_source=chatgpt.com "NTT Group Launches Synexia Ventures in Southeast Asia"))
    

---

### **6. SGInnovate (Singapore)**

- Government-linked investor backing **deep tech startups** including robotics, autonomy and enterprise technologies — a major co-investor in hard tech that can include UAV systems or related platforms. ([Wikipedia](https://en.wikipedia.org/wiki/SGInnovate?utm_source=chatgpt.com "SGInnovate"))
    

---

### **7. A2D Ventures**

📍 **LinkedIn:** [https://vn.linkedin.com/company/a2d-sea](https://vn.linkedin.com/company/a2d-sea)

- Early-stage investing platform in SEA that collaborates with angel investors and VC funds; often invests in AI, robotics and next-gen tech verticals relevant to drone/automation segments. ([LinkedIn](https://vn.linkedin.com/company/a2d-sea?utm_source=chatgpt.com "A2D Ventures | LinkedIn"))
    

---

### **8. Earth Venture Capital**

📍 **LinkedIn:** [https://sg.linkedin.com/company/earth-vc](https://sg.linkedin.com/company/earth-vc)

- Based in **Ho Chi Minh City & Singapore**; backs _science-based deep tech_ across emerging Asia — sectors like autonomous systems, aerial robotics and sensing hardware fit within their climate and innovation thesis. ([LinkedIn](https://sg.linkedin.com/company/earth-vc?utm_source=chatgpt.com "Earth Venture Capital | LinkedIn"))
    

---

## 📍 **Japan & East Asia — Strategic Investors**

While Japan and Korea have fewer _named_ VC partners with clear drone portfolios, there are institutional vehicles with strong deep tech/innovation roles:

### **9. Synexia Ventures (SEA + Japan)**

- Part of **NTT Group’s venture push** across Asia for robotics/IoT/drone ecosystems. Leadership like **Alan Kuan Hsu** (LinkedIn search) bridges Japan & SEA startups. ([LinkedIn](https://www.linkedin.com/posts/mohanbelani_ntt-group-launches-southeast-asia-venture-activity-7394285182138204160-I_rB?utm_source=chatgpt.com "NTT Group Launches Synexia Ventures in Southeast Asia"))
    

---

### **10. SoftBank Ventures Asia (SBVA)**

- **SoftBank’s VC arm** across Asia with deep tech/robotics funding track record (e.g., robotics, AI which closely intersects drone autonomy infrastructures). ([Wikipedia](https://en.wikipedia.org/wiki/SoftBank_Group?utm_source=chatgpt.com "SoftBank Group"))
    

---

## 🧠 **Finding More PhD + Engineering Profiles in These Firms**

Because many deep-tech VCs in Asia invest across robotics, AI, IoT and autonomy rather than only drones, _specific LinkedIn searches filtering for “PhD” + “venture capital” + “drone OR UAV OR robotics” in Singapore, Japan, Korea, Malaysia, Vietnam and Indonesia_ will yield higher-precision profiles.

Here’s a good LinkedIn search string you can use:

```
“PhD” AND (“venture capital” OR VC) AND (drone OR UAV OR autonomy OR robotics) AND (Singapore OR Japan OR South Korea OR Indonesia OR Malaysia OR Vietnam)
```

This helps narrow to _technical VCs with doctoral engineering or research backgrounds active in relevant sectors_.

---

## 📍 Unmanned.vc — Location & People

**[Unmanned.vc | Early‑Stage VC for Defence, Drone & Autonomous Startups](https://unmanned.vc/?utm_source=chatgpt.com)**

- **Location:** Tallinn, **Estonia** (Europe) — not Southeast Asia, but worth noting due to a focused unmanned systems thesis with drone tech advisory. ([Unmanned](https://unmanned.vc/?utm_source=chatgpt.com "Unmanned.vc | Early-Stage VC for Defence, Drone & Autonomous Startups"))
    
- Employees with strong technical affiliations include:
    
    - **Tero Silvola** (LinkedIn available via company page)
        
    - **Joshua Henriques**
        
    - **Elias Silvola**  
        These are advisors and fund support roles with deep technical backgrounds in autonomous systems and UAV tech. ([LinkedIn](https://www.linkedin.com/company/unmanned-vcc?utm_source=chatgpt.com "Unmanned.vc | LinkedIn"))
        

---

### Want this list refined to **only investors with PhD engineering degrees** or to include **LinkedIn URLs + summaries of educational background (PhD / tech focus)**? Let me know — I can generate that next.

Here’s a **comprehensive list of venture capital firms and investors in _East Asia and Southeast Asia_** that are **active or relevant to drone and aerospace technology from a _civil/enterprise_ perspective** (e.g., delivery drones, inspection, agri-drones, UTM/air mobility) — including those _with bases in China, Japan, Thailand and SEA_. I also include specific _VCs that focus on drones/aerial mobility_ and nearby investors who back adjacent deep-tech aerospace and autonomous systems.

---

## 🇯🇵 **Japan — Drone & Aerospace-Focused VC**

### **1. DRONE FUND (東京)**

**Focus:** Venture capital specializing _only in drone and air mobility startups_, covering hardware, software and airspace system innovations. It has a portfolio of 40+ companies globally and invests in technologies supporting social implementation of drones and aerial mobility. ([wingcopter.com](https://wingcopter.com/drone-fund?utm_source=chatgpt.com "DRONE FUND – Wingcopter"))  
**Location:** Tokyo, Japan  
**Key Leaders (LinkedIn):**

- **Kotaro Chiba** – Founder & Managing Partner, Venture capitalist active in drone sector. ([LinkedIn](https://www.linkedin.com/in/kotaro-chiba-557bb7?utm_source=chatgpt.com "Kotaro Chiba | LinkedIn - LinkedIn"))  
    🔗 [https://www.linkedin.com/in/kotaro-chiba-557bb7](https://www.linkedin.com/in/kotaro-chiba-557bb7)  
    **Notes:** Globally known as one of the _few VCs dedicated exclusively to drone/air mobility_, with investments in drone delivery, UTM, inspection, and civil applications. ([DRONE FUND - DRONE FUND website](https://dronefund.vc/en/wp-content/uploads/sites/2/2021/04/210416-ENG.pdf?utm_source=chatgpt.com "News Release"))
    

---

### **2. Innovation Network Corporation of Japan (INCJ)**

**Focus:** Major Japanese VC focused on deep tech, aerospace, mobility, and infrastructure innovation — invests in technologies enabling drone automation and aerospace navigation integration. ([SpaceTech Asia](https://www.spacetechasia.com/9-vcs-who-have-invested-in-asia-pacific-space-startups/?utm_source=chatgpt.com "9 VCs who have invested in Asia-Pacific space startups | SpaceTech Asia"))  
**Location:** Tokyo, Japan  
**LinkedIn:** Search “Innovation Network Corporation of Japan INCJ LinkedIn”  
_Good for finding partners / investors with aerospace, robotics, and UTM interests._ ([SpaceTech Asia](https://www.spacetechasia.com/9-vcs-who-have-invested-in-asia-pacific-space-startups/?utm_source=chatgpt.com "9 VCs who have invested in Asia-Pacific space startups | SpaceTech Asia"))

---

### **3. Real Tech Fund (Japan)**

**Focus:** Invests in _deep tech_ including aerospace, navigation, robotics, and infrastructure technology emerging from Japan’s research ecosystem, relevant to drone/air mobility sectors. ([SpaceTech Asia](https://www.spacetechasia.com/9-vcs-who-have-invested-in-asia-pacific-space-startups/?utm_source=chatgpt.com "9 VCs who have invested in Asia-Pacific space startups | SpaceTech Asia"))  
**Location:** Tokyo, Japan  
**LinkedIn:** Search “Real Tech Fund Japan LinkedIn”

---

## 🇨🇳 **China — Tech & Aerospace/Drone-Relevant VC**

China doesn’t yet have many _strictly drone-only VC funds_, but **major technology and industry VCs invest broadly in aerospace, autonomy, AI and sensing tech**, which are fundamental to civil drone/air mobility growth.

### **4. HongShan Capital (红杉中国)**

**Focus:** Large China-focused VC with aerospace, autonomous systems, robotics and AI tech investments. ([Wikipedia](https://en.wikipedia.org/wiki/HongShan?utm_source=chatgpt.com "HongShan"))  
**Location:** Beijing / Shanghai / Hong Kong / Singapore / Tokyo presence. ([Wikipedia](https://en.wikipedia.org/wiki/HongShan?utm_source=chatgpt.com "HongShan"))  
**LinkedIn:** Search “HongShan Capital LinkedIn”

---

### **5. Kuang-Chi (广智控股 & GCI Fund)**

**Focus:** Chinese innovation & investment group backing aerospace, high-tech and smart-cities technologies. It manages a ~$300M global innovation fund targeting aerospace and smart mobility ventures. ([Wikipedia](https://en.wikipedia.org/wiki/Kuang-Chi?utm_source=chatgpt.com "Kuang-Chi"))  
**Location:** Shenzhen / Hong Kong / Global offices. ([Wikipedia](https://en.wikipedia.org/wiki/Kuang-Chi?utm_source=chatgpt.com "Kuang-Chi"))  
**LinkedIn:** Search “Kuang-Chi LinkedIn”

---

### **6. Other China / Asia VCs With Aerospace-Adjacency**

These are _major regionally active VCs often participating in funding autonomous and aerospace technology innovators_ (not drone-specific funds but relevant):

- **ZWC Partners** — Invests in tech across China & SEA; potential relevance to autonomous systems. ([Wikipedia](https://en.wikipedia.org/wiki/ZWC_Partners?utm_source=chatgpt.com "ZWC Partners"))
    
- **Walden International** — VC with strong presence in Asia and historical bets on technology up through robotics and autonomous vehicles. ([Wikipedia](https://en.wikipedia.org/wiki/Walden_International?utm_source=chatgpt.com "Walden International"))
    
- **Shunwei Capital** — Chinese VC typically investing in technology platforms that could include UAV/AI convergence companies. ([Wikipedia](https://en.wikipedia.org/wiki/Shunwei_Capital?utm_source=chatgpt.com "Shunwei Capital"))  
    **LinkedIn:** Search individual firm names + “LinkedIn” to find partners working in aerospace, autonomy & UAV sectors.
    

---

## 🇹🇭 **Thailand & SEA — Relevant VC / CVC / Innovation Funds**

While _drone-exclusive VC firms_ are uncommon in Thailand’s venture ecosystem, several regional funds and corporate venture capital units back **enterprise technologies and industrial automation** — which intersect with civil drone systems (e.g., inspection, logistics, precision agriculture).

### **7. AddVentures by SCG (Thailand)**

**Focus:** Corporate VC under SCG (Siam Cement Group) backing _industrial and enterprise tech_ (incl. AI, automation, logistics) — increasingly intersecting with drone inspection and autonomous systems. ([Techsauce](https://techsauce.co/en/tech-and-biz/cross-border-funding-opportunities-and-hurdles-in-asean-discussion?utm_source=chatgpt.com "3 VCs Gather to Discuss Investment Opportunities and Challenges in ASEAN | Techsauce"))  
**Location:** Bangkok, Thailand  
**LinkedIn:** Search “AddVentures by SCG LinkedIn”  
**Note:** SCG’s investment thesis focuses on industry innovation (infrastructure, logistics, construction) where drones can play a significant role. ([Techsauce](https://techsauce.co/en/tech-and-biz/cross-border-funding-opportunities-and-hurdles-in-asean-discussion?utm_source=chatgpt.com "3 VCs Gather to Discuss Investment Opportunities and Challenges in ASEAN | Techsauce"))

---

### **8. Aerodyne & Partnerships**

Aerodyne isn’t a VC but a **regionally active drone solutions and service provider** that has raised funding from VC firms (e.g., North Summit Capital, Arc Ventures, Leave a Nest), indicating _investment flow into enterprise drone applications (infrastructure inspection & monitoring)_ across SEA including Thailand. ([International Finance](https://internationalfinance.com/featured/drone-specialist-aerodyne-receives-funding-expand-se-asia/?utm_source=chatgpt.com "Drone specialist Aerodyne receives funding to expand in SE Asia"))

- **Aerodyne Group** (LinkedIn search: Aerodyne Group) – Drone services & enterprise solutions; _invested by North Summit Capital & others in Asia_. ([International Finance](https://internationalfinance.com/featured/drone-specialist-aerodyne-receives-funding-expand-se-asia/?utm_source=chatgpt.com "Drone specialist Aerodyne receives funding to expand in SE Asia"))
    

---

## 🌏 **Southeast Asia — Broader Deep-Tech VCs With Drone/Aerospace Overlap**

These firms aren’t exclusively drone-oriented but regularly _invest in robotics, automation, logistics, AI and IoT_ — technologies that intersect with civil drone & air mobility innovations:

### **9. Earth Venture Capital (Singapore & Ho Chi Minh City)**

**Focus:** Science-based deep tech across Southeast Asia with interests in autonomy and sensor technologies (which complement drone systems).  
**LinkedIn:** Search “Earth VC Singapore LinkedIn”

### **10. Synexia Ventures (NTT-backed SEA fund)**

**Focus:** Invests in AI, IoT, robotics, smart logistics — adjacent to drone enterprise sectors.  
**LinkedIn:** Search “Synexia Ventures LinkedIn”

### **11. SGInnovate (Singapore)**

**Focus:** Government-linked investor accelerating deep tech and robotics innovations — often co-invests with VCs in autonomous and aerial technologies.

---

## 🧠 Notes on Finding People (Names + LinkedIn Profiles)

The above firms are high-relevance **investment vehicles**. Many individual partners at these firms have **engineering, PhD or technical backgrounds** and invest in UAV/aviation sectors. Here’s how you can find individuals:

### 🔎 **Search LinkedIn with these patterns**

Copy/paste and run searches on LinkedIn for more precise human profiles:

```
“PhD” AND (“venture capital” OR VC) AND (drone OR UAV OR air mobility OR aerospace) AND (Japan OR China OR Thailand OR Singapore)
```

```
(“Partner” OR “Principal” OR “Investment Director”) AND (aerospace OR drone OR UAV OR autonomy) AND (Singapore OR Tokyo OR Beijing OR Bangkok)
```

This helps you filter **individual investment professionals with technical backgrounds** involved in these sectors.

---

## Summary Table — Key VCs by Country/Region

|Region|VC / Firm|Drone / Aerospace Focus|
|---|---|---|
|**Japan**|DRONE FUND|🎯 Drone & air mobility specialist ([wingcopter.com](https://wingcopter.com/drone-fund?utm_source=chatgpt.com "DRONE FUND – Wingcopter"))|
||INCJ|Aerospace & mobility tech ([SpaceTech Asia](https://www.spacetechasia.com/9-vcs-who-have-invested-in-asia-pacific-space-startups/?utm_source=chatgpt.com "9 VCs who have invested in Asia-Pacific space startups \| SpaceTech Asia"))|
||Real Tech Fund|Deep tech/aerospace relevance ([SpaceTech Asia](https://www.spacetechasia.com/9-vcs-who-have-invested-in-asia-pacific-space-startups/?utm_source=chatgpt.com "9 VCs who have invested in Asia-Pacific space startups \| SpaceTech Asia"))|
|**China**|HongShan Capital|Tech + aerospace relevance ([Wikipedia](https://en.wikipedia.org/wiki/HongShan?utm_source=chatgpt.com "HongShan"))|
||Kuang-Chi GCI Fund|Aerospace/innovation fund ([Wikipedia](https://en.wikipedia.org/wiki/Kuang-Chi?utm_source=chatgpt.com "Kuang-Chi"))|
||ZWC Partners|Tech/China VC ([Wikipedia](https://en.wikipedia.org/wiki/ZWC_Partners?utm_source=chatgpt.com "ZWC Partners"))|
||Walden International|Asia tech VC ([Wikipedia](https://en.wikipedia.org/wiki/Walden_International?utm_source=chatgpt.com "Walden International"))|
|**Thailand/SEA**|AddVentures by SCG|Industrial/automation tech ([Techsauce](https://techsauce.co/en/tech-and-biz/cross-border-funding-opportunities-and-hurdles-in-asean-discussion?utm_source=chatgpt.com "3 VCs Gather to Discuss Investment Opportunities and Challenges in ASEAN \| Techsauce"))|
||Earth VC|Deep tech investor|
||Synexia Ventures|Tech & robotics cluster|
||Aerodyne (startups)|Enterprise drone applications ([International Finance](https://internationalfinance.com/featured/drone-specialist-aerodyne-receives-funding-expand-se-asia/?utm_source=chatgpt.com "Drone specialist Aerodyne receives funding to expand in SE Asia"))|

---

If you want, I can next provide a **list of specific individual partners (with LinkedIn URLs) at these firms** who _actively invest_ in airline, UAV, autonomy & civil drone tech. Just tell me which geography (e.g., Asia only, global with Asia focus) you want emphasized.

https://japan.ahk.de/en/downloads/umfragen-berichte/business-climate-survey-german-business-in-japan-2025?utm_source=chatgpt.com
Got it — this is a **serious, long-range career pivot**, and you’re actually well-positioned if you play it deliberately. Below is a **step-by-step visa + career blueprint from now → 2028**, tailored to **finance / VC in the drone & aerospace ecosystem**, with **Japan, Singapore, and Hong Kong** compared side-by-side.

I’ll be concrete: **what to build each year, what your CV should signal, which visas are realistic, and where the risks are**.

---

# 🎯 Your Target Profile by 2028 (North Star)

By 2028, you want recruiters/partners to see you as:

> **“A PhD-level aerial communications expert who understands drone economics, regulation, and capital allocation in Asia.”**

That means **not** “engineer trying finance”, but:

- **Sector specialist** (drones, aerial comms, autonomy)
    
- **Commercially literate** (valuation, unit economics, GTM)
    
- **Asia-credible** (language + ecosystem exposure)
    

---

# 🧭 OVERVIEW: Best Ecosystem Fit (Honest Take)

|City|VC Access|Drone Relevance|Language Barrier|Visa Friction|Overall Fit|
|---|---|---|---|---|---|
|**Singapore**|⭐⭐⭐⭐⭐|⭐⭐⭐⭐|Low|Low|**BEST ENTRY**|
|**Japan (Tokyo)**|⭐⭐⭐|⭐⭐⭐⭐|High|Medium–High|Strategic but hard|
|**Hong Kong**|⭐⭐⭐⭐|⭐⭐⭐|Low|Medium|Finance-heavy, less drone-native|

**Reality:**  
👉 Most foreigners who succeed in **Japan VC** first build credibility in **Singapore or Europe**, _then_ move to Japan.

---

# 🗺️ STEP-BY-STEP PLAN (2025 → 2028)

## 🔹 2025–2026: Foundation Phase (While Doing PhD)

### 🎓 Academic Positioning (Critical)

Your PhD topic is already excellent — now **reframe it**:

**Instead of:**

> “Aerial communication systems”

**Start saying:**

> “Communications infrastructure for scalable civil drone operations and UTM”

This matters for VC conversations.

---

### 💼 Skills to Add (Non-Negotiable)

You must **formally learn finance** — self-study is not enough.

**By end-2026, you should have:**

- Financial modeling (DCF, venture method)
    
- Startup unit economics (hardware vs SaaS vs services)
    
- Cap tables, dilution, term sheets (SAFE, preferred equity)
    
- Market sizing (TAM/SAM/SOM) for drone verticals
    

**Best options (realistic while PhD):**

- CFA Level 1 (strong signal in Asia)
    
- VC / Startup finance certificates (Wharton, LBS, INSEAD)
    
- Build **2–3 investment memos** on drone startups (personal portfolio)
    

---

### 🌍 Language Strategy (Start Now)

|Destination|Target by 2028|Why|
|---|---|---|
|**Japan**|JLPT **N2 minimum**|VC & corp dev demand it|
|**Singapore**|English only OK|Huge advantage|
|**Hong Kong**|English OK|Mandarin helpful but optional|

👉 If Japan is serious: start Japanese **now**, not 2027.

---

### 📄 CV Version 1 (End of 2026)

Your CV should already look **hybrid**, not academic:

**Top line:**

> PhD Researcher | Aerial Communications & Civil Drone Systems | Investment & Market Analysis

**Sections to include:**

- Research → _Commercial relevance_
    
- Market analysis (drone comms, UTM, BVLOS)
    
- Finance coursework / certifications
    
- Conferences where industry attends (not just academic)
    

---

## 🔹 2026–2027: Industry + Finance Credibility Phase

### 🎯 Goal

Get **real exposure to money or strategy**, not just tech.

---

### 🏢 Job Targets (Germany / Europe)

You **can expect to find work in Germany by 2027–2028**, yes — but **not directly VC**.

**Realistic stepping-stone roles:**

- Corporate development / strategy at drone companies
    
- Product strategy / business analyst (deep tech)
    
- Technology scouting (OEMs, defense, aerospace)
    
- Consulting (deep-tech, infrastructure, aviation)
    

**Target companies:**

- Quantum Systems
    
- Droniq
    
- Airbus Urban Mobility
    
- Helsing (dual-use credibility matters)
    
- Big-4 / strategy consulting (aerospace focus)
    

👉 12–24 months here = **gold** for VC later.

---

### 💰 Parallel: VC Adjacency (Very Important)

While working:

- Scout deals informally
    
- Angel syndicates
    
- Startup mentoring
    
- Write public drone market analyses (LinkedIn / Substack)
    

VCs hire **people they already know**.

---

## 🔹 2027–2028: Asia Pivot Phase

Now you choose **where to land first**.

---

# 🇸🇬 SINGAPORE PATH (Recommended Entry)

### 🎯 Why Singapore First

- English-first VC ecosystem
    
- Strong drone, autonomy, smart-city focus
    
- Friendly visas
    
- Many Japan- and China-linked funds
    

### 🎯 Target Roles

- Investment Analyst / Associate (Deep Tech VC)
    
- Strategy / Corp Dev at drone startups
    
- Government-linked funds (Temasek ecosystem)
    
- Family offices investing in aerospace
    

### 🛂 Visa

- **Employment Pass (EP)**  
    ✔ Employer sponsorship  
    ✔ Very realistic with PhD + experience
    

### 📄 CV by This Point Should Show:

- PhD + industry experience
    
- Deal exposure (even informal)
    
- Asia-relevant market insights
    
- No “pure academic” vibe
    

---

# 🇯🇵 JAPAN PATH (Hard Mode, High Reward)

### 🎯 How Foreigners Actually Enter Japan VC

Almost **never directly**.

**Common paths:**

1. Join **Japanese drone VC from Singapore office**
    
2. Join **corporate venture arm** (NTT, Mitsubishi, Toyota)
    
3. Join **strategy / corp dev**, then move internal
    

### 🎯 Target Organizations

- DRONE FUND
    
- INCJ
    
- Corporate VC arms
    
- Global VC firms with Tokyo offices
    

### 🛂 Visa

- **Highly Skilled Professional (HSP)** → best
    
- Engineer / Specialist in Humanities
    

### 🔑 Requirements Reality

- JLPT N2/N1
    
- Existing Asia VC or strategy experience
    
- Strong sector narrative
    

---

# 🇭🇰 HONG KONG PATH (Finance-Heavy)

### 🎯 Fit

- Better for **finance-first**, less for drone-native VC
    
- Strong for PE, IB, family offices
    
- Increasing China exposure risk
    

### 🛂 Visa

- **Employment Visa** (company sponsorship)
    
- Competitive but doable
    

---

# 📅 YEAR-BY-YEAR CHECKLIST

## ✅ By end-2025

- Finance fundamentals started
    
- Japanese A2–B1
    
- 1–2 drone investment memos
    

## ✅ By end-2026

- CFA L1 or equivalent
    
- VC-style CV
    
- Industry networking active
    

## ✅ By end-2027

- 12+ months industry or strategy role
    
- VC adjacency (projects, scouting)
    
- Japanese approaching N2
    

## ✅ By 2028

- Singapore or Europe-Asia VC role
    
- Japan entry feasible from strength
    

---

# ⚠️ Hard Truths (Important)

- **Japan VC straight from PhD = very unlikely**
    
- **Singapore is the real gateway**
    
- Language is not “nice to have” in Japan — it’s decisive
    
- Your technical niche is an **advantage**, not a liability — if framed commercially
    

---

# 🧠 Final Strategic Advice

If you want the **highest probability of success**:

> **Germany → Industry/Strategy → Singapore VC → Japan VC**

This path aligns with:

- Visa reality
    
- Hiring behavior
    
- How Asia VC ecosystems actually work
    

---

If you want next, I can:

- Rewrite your **future VC-ready CV**
    
- Suggest **exact VC firms** to target in each city
    
- Create a **Japanese-VC interview prep guide**
    
- Build a **deal memo template tailored to drones**
    

Just tell me what you want to tackle next.

Love this question — this is the **cleanest, highest-leverage version** of your plan:  
**PhD → VC directly**, while **systematically preparing on the side** so you’re _credible the moment an opening appears_.

I’ll break this into:

1. **The core VC profile you must build**
    
2. **What to self-learn (exactly)**
    
3. **How to target Japan vs Singapore vs Hong Kong**
    
4. **How to signal VC-readiness without a finance job**
    
5. **What success realistically looks like**
    

No fluff, no “MBA required” nonsense.

---

## 1️⃣ The VC Profile You Must Build (From a PhD)

VCs do **not** hire “finance people”.  
They hire **pattern recognizers** with:

- domain depth
    
- judgment
    
- network
    
- and clear thinking
    

Your PhD gives you **one of the hardest pieces** already.

### Your Target Identity

> **Deep-tech investor candidate specializing in drones, aerial communications, and autonomy economics**

Not:

- “Engineer who wants to do VC”
    
- “Researcher transitioning to finance”
    

This framing is _everything_.

---

## 2️⃣ What to Self-Learn (Side-Preparation Stack)

This is the **minimum viable VC skillset** you must quietly build.

### A. Venture Finance (Non-Optional)

Learn this well enough to **teach it**.

You must be fluent in:

- Venture math (ownership, dilution, exits)
    
- SAFE vs priced rounds
    
- Pre/post money
    
- Fund structure (2/20, reserves)
    
- IRR vs MOIC (VCs care about MOIC)
    

📌 Output expectation:

- You can explain why **most drone startups fail financially**
    
- You can model a drone company in Excel in 2 hours
    

---

### B. Drone-Specific Economics (Your Edge)

This is where you destroy MBA candidates.

You must understand:

- Hardware vs software margins
    
- Fleet economics (CAPEX vs OPEX)
    
- Certification timelines → cash burn
    
- BVLOS regulation → valuation impact
    
- Why civil drones struggle with defensibility
    

📌 Output expectation:

- You can say _which drone business models are VC-backable_
    
- You can kill bad deals politely
    

---

### C. Market & Policy Literacy (Asia-Critical)

VC in Asia is **policy-driven**, not purely market-driven.

You must track:

- Japan MLIT drone policy
    
- Singapore CAAS sandboxing
    
- China supply-chain leverage
    
- Defense vs civil dual-use constraints
    

📌 Output expectation:

- You can explain _why Japan funds drones despite low growth_
    
- You understand where geopolitics blocks exits
    

---

## 3️⃣ How to Target Each Country (Direct PhD → VC)

### 🇸🇬 SINGAPORE (Best First Target)

#### Why Singapore Loves PhDs

- Sector expertise > finance pedigree
    
- English-first
    
- Government-backed funds need tech credibility
    

#### Who Hires You

- Deep-tech VCs
    
- Corporate VC arms
    
- Family offices doing frontier tech
    
- Govt-linked investment platforms
    

#### How to Target

**Your pitch:**

> “I evaluate drone startups from technical feasibility, regulatory risk, and capital efficiency perspectives.”

**Your advantage:**

- You reduce downside risk
    
- You can do technical diligence in-house
    

📌 What to do NOW:

- Write **2–3 public drone investment theses**
    
- Network with Singapore VCs via insight, not job asks
    
- Apply for _analyst / venture fellow_ roles
    

Singapore is the **cleanest PhD → VC jump**.

---

### 🇯🇵 JAPAN (Hard Mode, High Prestige)

#### Why Japan Is Hard

- Relationship-based
    
- Language-gated
    
- Risk-averse
    

#### Where PhDs Fit

- Technical diligence
    
- Corporate VC
    
- Sector-focused funds (drones, robotics)
    

#### How to Target

You do **not** say:

> “I want to work in VC”

You say:

> “I help evaluate drone technologies and markets for investment.”

📌 Critical side-prep:

- Japanese to N2
    
- Learn _Japanese VC thinking_ (risk mitigation, consensus)
    

📌 Realistic entry:

- Analyst / technical associate
    
- Strategy or venture unit
    
- Singapore → Japan transfer
    

Japan values **trust over brilliance**.

---

### 🇭🇰 HONG KONG (Finance-First)

#### Where You Fit

- Family offices
    
- PE/VC hybrids
    
- China-adjacent capital
    

#### Risk

- Less drone-native
    
- More finance-heavy
    
- Higher geopolitical volatility
    

#### How to Target

You position yourself as:

> “Tech specialist supporting investment decisions”

You won’t lead deals early — you support.

---

## 4️⃣ How to Signal VC-Readiness Without a VC Job

This is the **secret** most people miss.

### You Must Produce Public Signal

Do **at least 3** of these:

- Write investment memos (public or semi-public)
    
- Publish drone market breakdowns
    
- Evaluate failed drone startups (post-mortems)
    
- Scout startups for funds informally
    
- Judge startup competitions
    
- Mentor founders
    

📌 VCs hire people they already trust intellectually.

---

## 5️⃣ Your CV Should NOT Look Like This

❌ “PhD researcher seeking VC role”  
❌ “Strong quantitative background”  
❌ “Passionate about investing”

---

## ✅ Your CV SHOULD Look Like This

**Headline:**

> PhD | Aerial Communications & Civil Drone Systems | Venture & Market Analysis

**Sections:**

- Technology → Market translation
    
- Investment analysis (self-initiated)
    
- Regulatory insight
    
- Startup evaluation experience
    

Your CV should scream:

> “I already do VC thinking — you just haven’t paid me yet.”

---

## 6️⃣ Reality Check (Honest Odds)

|Path|Probability|
|---|---|
|PhD → Singapore VC|**High**|
|PhD → Japan VC|Medium (with language + prep)|
|PhD → HK VC|Medium|
|PhD → VC with no side prep|Very low|

Your **domain specificity** massively improves your odds.

---

## 🧠 Final Advice (Very Important)

Do **not** chase VC roles directly.

Instead:

> Become _useful_ to VCs before they hire you.

When a fund realizes:

- you save them time
    
- you reduce technical risk
    
- you think like an investor
    

…they’ll pull you in.

---

If you want next, I can:

- Design your **first drone investment memo**
    
- Help you pick **exact VCs to target**
    
- Rewrite your **PhD narrative for VC**
    
- Build a **12-month side-prep syllabus**
    

Tell me what you want to do next.

Perfect — this is the **bridge between your PhD/tech expertise and the world of VC or corporate finance**. Let’s focus on **finance roles in tech** that are realistic for someone with your background and how they differ across **Singapore, Japan, and Hong Kong**. I’ll also break down **what skills and experience you need for each role**.

---

# 1️⃣ Core Finance Roles in Tech

These are the **roles that actually hire PhDs or engineers into finance in tech/VC-adjacent sectors**:

|Role|What You Do|Why It Fits a Tech PhD|Example Employers|
|---|---|---|---|
|**Corporate Finance / FP&A**|Budgeting, forecasting, financial reporting, scenario modeling|Your quantitative skills + systems thinking|Google, Microsoft, drone OEMs (Quantum Systems, DJI Europe)|
|**Business / Corporate Development**|M&A, partnerships, due diligence|Translate tech feasibility into financial risk/reward|Airbus, Sony, SoftBank Ventures (Japan), Grab/Sea Group (Singapore)|
|**Venture Analyst / Associate (Tech VC)**|Startup evaluation, financial modeling, market sizing|Your sector knowledge + modeling ability|Temasek, DRONE FUND (Japan), Sequoia SEA, GGV Capital|
|**Strategy & Operations (Tech / AI / Drone)**|Unit economics, pricing strategy, scaling operations|Your research mindset|Faction drone startups, robotics OEMs, Uber Elevate spin-offs|
|**Investment Analyst (Family Office / PE)**|Deal sourcing, valuation, portfolio reporting|Tech understanding helps assess risk in frontier sectors|Family offices investing in autonomous systems or robotics|

**Key Insight:** Many of these roles are **“tech-first finance”**, not pure banking. They value your **deep domain knowledge + ability to model financial outcomes**.

---

# 2️⃣ Geographic Differences

### 🇸🇬 Singapore

- **High demand:** Corporate dev, VC, FP&A in tech/AI/drone.
    
- **Visa:** Employment Pass easy with PhD + finance/tech role.
    
- **Language:** English-first, no barrier.
    
- **Tips:**
    
    - Target government-linked funds (Temasek, SGInnovate).
        
    - Network via Singapore Venture Capital Association and industry conferences.
        

### 🇯🇵 Japan

- **High reward, high barrier:** Corporate finance in tech or VC, mostly in Tokyo.
    
- **Visa:** Highly Skilled Professional (HSP) visa, or Engineer/Specialist visa.
    
- **Language:** Japanese N2 required for most corporate/finance roles; English-only roles exist in multinational tech firms.
    
- **Tips:**
    
    - Look for **corporate venture arms** (NTT, DRONE FUND, Mitsubishi).
        
    - Target strategy / tech diligence roles first; later move to VC.
        

### 🇭🇰 Hong Kong

- **Finance-first, tech adjunct:** More opportunities in PE/family offices and VC, but fewer drone-specific roles.
    
- **Visa:** Employment visa; competitive but accessible with strong skills.
    
- **Language:** English sufficient, Mandarin optional but helpful.
    
- **Tips:**
    
    - Focus on family offices investing in tech, robotics, or autonomous systems.
        
    - Hong Kong is finance-heavy; your drone/tech expertise is a differentiator but not required.
        

---

# 3️⃣ Skill Stack Required

To be **finance-ready in tech**, you need:

### Technical Skills

- Financial modeling (Excel, Python optional)
    
- Valuation: DCF, VC method, comparables
    
- Cap table analysis
    
- Scenario analysis for hardware-heavy startups
    

### Analytical Skills

- Market sizing (TAM/SAM/SOM)
    
- Business model analysis (SaaS vs hardware, drones)
    
- Unit economics and revenue modeling
    

### Communication Skills

- Clear, concise writing for investment memos
    
- Ability to present technical + financial analysis to non-engineers
    
- Deal story crafting for VC / corporate finance
    

### Optional but Valuable

- CFA Level 1 (credibility signal)
    
- Python / SQL for data-driven diligence
    
- Industry network (drone meetups, AUVSI, UAV DACH)
    

---

# 4️⃣ Transition Path From PhD

Here’s a **realistic stepping stone**:

1. **PhD in Aerial Communication**
    
    - Focus: Civil drones, UTM, BVLOS.
        
    - Side: Build **investment memos on drone startups**.
        
2. **Industry Experience (2026–2027)**
    
    - Corporate development, strategy, or FP&A at a drone/tech company.
        
    - Your role: Translate tech feasibility into financial decisions.
        
    - Outcome: Gain real **deal exposure + valuation experience**.
        
3. **VC / Tech Finance (2027–2028)**
    
    - Target: Singapore first (lowest barrier), then Japan/HK.
        
    - Roles: Analyst / Associate / Strategy & Ops
        
    - Output: Lead investment memos, help manage portfolios, support deals.
        

---

# 5️⃣ How to Target Roles

### Step 1: Build a CV That Speaks Finance + Tech

- Emphasize your **PhD as domain expertise**
    
- Include **financial modeling projects** on drone startups
    
- Highlight **industry collaborations or consulting**
    

### Step 2: Network & Demonstrate Value

- LinkedIn outreach to **VC analysts, corporate dev leads**
    
- Share insights on **drone market, regulations, or tech investment theses**
    
- Attend **industry conferences** in Asia (Singapore Drone Expo, Japan Drone Forum)
    

### Step 3: Apply for Realistic Roles

- Analyst / Associate / Strategy roles in **tech-focused VC / corporate VC / FP&A**
- Look at **drone startups, robotics firms, or family offices investing in tech**
- Use your PhD to **screen in as technical advisor / due diligence expert** if not directly hired as finance yet
    

---

# 6️⃣ Your Edge in Tech + Finance

- Most VC / finance candidates come from MBA or consulting.
    
- Your **technical PhD + drone expertise** gives you:
    
    - Faster diligence on deep-tech investments
    - Ability to predict tech adoption & risks
    - Access to startup founders who value technical credibility
        

---

I can next **map specific companies and funds in Japan, Singapore, and Hong Kong** that are actively investing in drones / robotics and likely to hire someone with **your exact profile** — including the **roles, expected experience, and hiring likelihood**.

Do you want me to do that?

Here’s a **region‑by‑region map of specific venture capital firms, corporate VCs, and innovation funds in Japan, Singapore, and Hong Kong** that are relevant to **drones, robotics, deep tech, autonomy and adjacent sectors**, plus **roles you could realistically target — even with an Indian passport** (via work visas) if you build the right skills and network.

---

## 🇯🇵 **Japan — Core VC & Strategic Funds**

### **1. DRONE FUND (Tokyo)**

- **Focus:** Dedicated _drone and air mobility_ venture capital — invests across hardware, software and ecosystem players. ([DRONE FUND - DRONE FUND website](https://dronefund.vc/?utm_source=chatgpt.com "DRONE FUND - DRONE FUND"))
    
- **Why it matters:** One of the _few funds globally focused solely on drone tech_.
    
- **Roles to target:**
    
    - **Investment Analyst / Associate (VC)** — support deal screening, diligence, financial modeling.
        
    - **Technical due diligence associate** — evaluate tech feasibility + market fit.
        
    - **Ecosystem/portfolio support roles** — strategy, operations, corporate development.
        
- **Experience expected:** Early‑stage investing, strong knowledge of drone/air mobility economics; Japanese language a huge advantage (can be English‑friendly in international settings).
    
- **Visa:** Skilled work visa (Engineer/Specialist in Humanities/International Services) or Highly Skilled Professional status with employment contract.
    

---

### **2. Globis Capital Partners (Tokyo)**

- **Focus:** Broad VC with _deep tech and robotics_ (invested in robotics startup Telexistence). ([Wikipedia](https://en.wikipedia.org/wiki/Globis_Capital_Partners?utm_source=chatgpt.com "Globis Capital Partners"))
    
- **Why it matters:** Larger, generalist VC that **invests in robotics/deep tech complementing drones**.
    
- **Roles to target:**
    
    - **Investment Associate / Analyst** — support opportunities tied to autonomy & robotics.
        
    - **Market research / sector strategist** (drone + robotics segments).
        
- **Experience expected:** Prior analyst experience, strong financial and technical analysis skills.
    

---

### **3. NOW Venture Capital**

- **Focus:** Japanese early‑stage VC investing in tech startups (not drone‑only but invests broadly). ([Wikipedia](https://zh.wikipedia.org/wiki/NOW%E5%89%B5%E6%8A%95?utm_source=chatgpt.com "NOW創投"))
    
- **Why it helps:** Broader placements can help you break into VC locally before moving into drone/robotics deals.
    

---

### **4. Vertex Ventures Japan (Temasek affiliate)**

- **Focus:** Singapore‑based Vertex Holdings launched a **Japan‑focused fund**, expanding local VC opportunities; not drone‑specific but invests in enterprise/deep tech. ([Financial Times](https://www.ft.com/content/b2e5bdc1-eb8f-427c-b175-1bed7412d206?utm_source=chatgpt.com "Temasek's venture capital arm to launch first Japan-focused fund"))
    
- **Why it matters:** Leverages global network; potentially more opportunities for English‑friendly roles and cross‑border investing.
    

---

## 🇸🇬 **Singapore — Strongest Entry Market for Drone/Robotics VC**

Singapore has a **mature, international VC ecosystem** that invests widely in tech sectors relevant to drones and automation.

### **5. SGInnovate**

- **Type:** Government‑linked innovation investor focused on _deep technology_, including robotics/AI and enabling startups. ([Wikipedia](https://en.wikipedia.org/wiki/SGInnovate?utm_source=chatgpt.com "SGInnovate"))
    
- **Why it matters:** Deep‑tech focus aligns with drones/robots; also excellent for networking and ecosystem access.
    
- **Roles to target:**
    
    - **Investment/portfolio analyst**
        
    - **Sector specialist (robotics/automation/drones)**
        
    - **Startup engagement / ecosystem roles**
        

---

### **6. Synexia Ventures (NTT Group, Singapore)**

- **Focus:** New investment vehicle targeting Southeast Asian startups in areas like AI, IoT, _smart cities, robotics, and drones_. ([ntt-finance.co.jp](https://www.ntt-finance.co.jp/eng/news/251111.html?utm_source=chatgpt.com "NTT Group Establishes Its First Southeast Asia Startup Investment Vehicle, “Synexia Ventures” | What's New | NTT FINANCE CORPORATION"))
    
- **Why it matters:** Strong Japan‑SEA bridge; potentially good for cross‑regional roles and strategy.
    

---

### **7. Golden Gate Ventures**

- **Focus:** Leading SEA VC investing in early‑stage tech (not drone‑specific but active in tech hubs). ([Wikipedia](https://en.wikipedia.org/wiki/Golden_Gate_Ventures?utm_source=chatgpt.com "Golden Gate Ventures"))
    
- **Roles to target:**
    
    - Investment Associate / Analyst with sector specialization
        
    - Scout / Venture Fellow for deep‑tech deals
        
- **Experience expected:** Strong generalist investing skills + sector thesis for drones/robotics.
    

---

### **8. Quest Ventures**

- **Focus:** Singapore‑based VC investing in Asia‑wide tech startups including digital commerce and deep tech. ([Wikipedia](https://en.wikipedia.org/wiki/Quest_Ventures?utm_source=chatgpt.com "Quest Ventures"))
    
- **Why it matters:** Regional footprint and portfolio support roles.
    

---

### **9. Business Angel Network of Southeast Asia (BANSEA)**

- **Focus:** Angel network in Singapore connecting early-stage tech startups with investors — useful for **scouting + angel investing experience** for your VC profile. ([Wikipedia](https://en.wikipedia.org/wiki/Business_Angel_Network_of_Southeast_Asia?utm_source=chatgpt.com "Business Angel Network of Southeast Asia"))
    
- **Roles to target:**
    
    - Internship / syndicate analyst
        
    - Event & portfolio support roles
        

---

## 🇭🇰 **Hong Kong — Finance‑Aligned VC & Innovation Funds**

Hong Kong tends to be stronger in **finance/markets and deep tech investment matching through public programs**, not drone‑only funds — but there _are funds investing in deep tech including robotics, AI, and automation_, and city‑level innovation initiatives.

### **10. Innovation and Technology Venture Fund (ITVF)**

- **Type:** Government‑supported co‑investment fund aimed at attracting VC funds into Hong Kong startups (including robotics and AI). ([itf.gov.hk](https://www.itf.gov.hk/l-eng/ITVF.asp?utm_source=chatgpt.com "The Innovation and Technology Venture Fund (ITVF)"))
    
- **Why it matters:** You could work in roles where public matching capital flows into private VC deals.
    

---

### **11. ZWC Partners**

- **Type:** Asian venture capital firm based in Hong Kong with technology investment focus — invests across China and SEA and has backed motors/AI companies including autonomous mobility startups like Horizon Robotics (via portfolio). ([Wikipedia](https://en.wikipedia.org/wiki/ZWC_Partners?utm_source=chatgpt.com "ZWC Partners"))
    
- **Roles to target:**
    
    - Investment Associate / Analyst
        
    - Sector specialist (deep tech)
        

---

### **12. QBN Capital (HKUST ecosystem)**

- **Focus:** HK‑based fund working with deep tech, semiconductors, and enabling global talent exchange (including diaspora talent). ([e-fund.hkust.edu.hk](https://e-fund.hkust.edu.hk/partners?utm_source=chatgpt.com "Partners | Entrepreneurship Fund | The Hong Kong University of Science and Technology"))
    
- **Why it matters:** Although not directly drone‑specific, it’s relevant for deep‑tech VC careers.
    

---

### **13. HKSTP (Hong Kong Science & Technology Parks)**

- **Not a VC per se**, but a **key innovation cluster** with deal facilitation and investment matching, including robotics and autonomy companies — this ecosystem hub supports deep‑tech ventures and often co‑invests with funds. ([kyodonewsprwire.jp](https://kyodonewsprwire.jp/release/202512090644?utm_source=chatgpt.com "HKSTP Makes Strategic Investment in Singapore Technology Company Vizzio; Forges Innovation Pact to Power Next-Generation AI and Smart City | Vizzio Technologiesのプレスリリース | 共同通信PRワイヤー"))
    
- **Roles to target:**
    
    - Investment portfolio manager / strategy
        
    - Startup scouting & pipeline development
        

---

## 🧭 Roles & Hiring Likelihood (Across Regions)

Here’s how you can **target roles in these funds, as an Indian passport holder** (work visa sponsorship needed but feasible in all three hubs with qualifications and experience):

### 1) **VC Analyst / Associate**

- **What you do:** Due diligence, market sizing, financial modeling, deal support
    
- **Where realistic:**
    
    - **Singapore:** high (English‑friendly, many funds)
        
    - **Japan:** medium (stronger if bilingual or Singapore connections)
        
    - **Hong Kong:** medium (more finance focus, less drone-specific)
        

### 2) **Technical Investment Specialist**

- **What you do:** Evaluate deep tech feasibility (drone/robotics) for investment teams
    
- **Where realistic:**
    
    - **Singapore:** high via SGInnovate & Synexia
        
    - **Japan:** medium–high at DRONE FUND / Globis
        
    - **Hong Kong:** medium via ZWC / QBN if tied to robotics/AI
        

### 3) **Corp Dev / Strategy in Venture or CVC**

- **What you do:** Corporate partnerships, industry strategy, ecosystem building
    
- **Where realistic:**
    
    - **Singapore:** high
        
    - **Japan:** medium
        
    - **Hong Kong:** medium
        

### 4) **Ecosystem / Portfolio Support**

- **What you do:** Startup enablement, events, investor relations
    
- **Where realistic:**
    
    - **Singapore:** high (SGInnovate, BANSEA)
        
    - **Japan:** medium (VC hubs, startup programs)
        
    - **Hong Kong:** medium (HKSTP)
        

---

## 🧠 Visa Considerations (Indian Passport)

**Singapore**

- **Employment Pass (EP):** Common route for VCs and finance/analyst roles; sponsorship by employer required.
    
- Early career roles and internships sometimes support EP applications if salary meets threshold.
    

**Japan**

- **Engineer/Specialist in Humanities/International Services:** Usual visa for VC/finance roles.
    
- **Highly Skilled Professional Visa:** Best long‑term path with points for PhD + work experience + salary.
    

**Hong Kong**

- **General Employment Policy Visa:** Employer sponsorship for finance/VC roles is common.
    
- Deep‑tech domain expertise increases attractiveness for employers.
    

---

## 🧠 Targeting Strategy (Next Steps)

**1. Build sector credibility**

- Publish investment memos on drone/robotics markets
    
- Join community investor groups (BANSEA, Singapore pitch events)
    

**2. Network in ecosystem**

- Attend VC & startup expos in Singapore & Tokyo
    
- Follow and connect with teams in SGInnovate, DRONE FUND, ZWC
    

**3. Apply strategically**

- Tailor CV for **VC analyst / technical investment specialist**
    
- Emphasize PhD + drone system expertise + financial literacy
    

---

If you want, I can compile **specific individual recruiters/partners at each of these VC firms (with LinkedIn where available)** who you should reach out to first — just tell me your **current location and work authorization status** for each region (Japan, Singapore, Hong Kong).

Here’s a *_focused map of _actual investors / partners / recruiters in VC firms and related funds__ across **Japan, Singapore, and Hong Kong** that are _relevant to drones, robotics, deep tech or early‑stage technology investing_ — including **specific names and LinkedIn profiles (where available)** for your outreach strategy. I’ve also noted **roles you can target** and **how accessible each contact might be given you’re currently in Germany on a B‑2 student visa with later work‑visa needs**.

---

# 🇯🇵 **Japan — Niche & Highly Relevant**

### **1. DRONE FUND (Tokyo, Japan)**

A dedicated **drone & air mobility VC** focused on seed to early stages across hardware, software and autonomous systems. ([プレスリリース・ニュースリリース配信シェアNo.1｜PR TIMES](https://prtimes.jp/main/html/rd/p/000000070.000026186.html?utm_source=chatgpt.com "DRONE FUNDが、日本初の大規模なベンチャーキャピタル集積拠点である麻布台ヒルズ「TOKYO VENTURE CAPITAL HUB」へ移転 | DRONE FUNDのプレスリリース"))

**Key People to Reach Out To**

- **Kotaro Chiba** — _Co‑founder / Managing Partner_  
    LinkedIn: [https://www.linkedin.com/in/kotaro-chiba-557bb7](https://www.linkedin.com/in/kotaro-chiba-557bb7) ([LinkedIn](https://www.linkedin.com/in/kotaro-chiba-557bb7?utm_source=chatgpt.com "Kotaro Chiba - Private Pilot(FAA/Japan)   / HondaJet owner / Angel ..."))  
    _Why:_ Founder with strong VC and ecosystem experience; strategic contact for insight on drone/VC demand.
    
- **Soki Omae** — _Co‑founder / Managing Partner_  
    LinkedIn: _(search “Soki Omae LinkedIn Japan”)_
    
    - Very early‑stage investment partner — a good contact for analyst/associate opportunities.
        
- **Daichi Funanami** — _CFO_  
    LinkedIn: _(search “Daichi Funanami LinkedIn”)_
    
    - Finance lead — useful contact if you’re pursuing **finance + tech due diligence roles**.
        

**Target Roles:**

- **Investment Analyst / Associate**
    
- **Technical + financial due diligence associate**
    
- **Portfolio support / operations**
    

**Notes:**  
DRONE FUND is small but highly targeted on drones and air mobility — a great place to enter if you can demonstrate domain, financial or strategy expertise. ([DRONE FUND - DRONE FUND website](https://dronefund.vc/en/team/?utm_source=chatgpt.com "Team - DRONE FUND"))

---

# 🇸🇬 **Singapore — Diverse, International VC Target List**

Singapore has a larger English‑friendly VC ecosystem that often backs early tech and deep tech across Asia.

### **2. Spiral Ventures Pte. Ltd. (Singapore)**

A Japan‑Singapore VC with early‑stage tech focus across Southeast Asia & Japan. ([LinkedIn](https://sg.linkedin.com/company/spiral-ventures-pte-ltd?utm_source=chatgpt.com "Spiral Ventures Pte. Ltd. | LinkedIn"))

**Key People**

- **YUJI HORIGUCHI** — _CEO & Founder_  
    LinkedIn: _(search “Yuji Horiguchi Spiral Ventures LinkedIn Singapore”)_
    
- **Hiroshi Oka** — _Partner_  
    LinkedIn: _(search “Hiroshi Oka Spiral Ventures LinkedIn”)_
    
- **Irawan Ganda** — _Partner_  
    LinkedIn: _(search “Irawan Ganda Spiral Ventures LinkedIn”)_
    

**Target Roles:**

- Analyst / Associate (early‑stage investing)
    
- Sector specialist (tech & robotics focus)
    
- Market strategy and due diligence
    

**Why Singapore:**  
Spiral has a **Japan + SEA angle**, making it a great entry point as an Indian passport holder on EP visa later and a helpful bridge to Japan or broader Asia exposure. ([LinkedIn](https://sg.linkedin.com/company/spiral-ventures-pte-ltd?utm_source=chatgpt.com "Spiral Ventures Pte. Ltd. | LinkedIn"))

---

### **3. Golden Gate Ventures (Singapore)**

A leading **venture capital firm backed by strong partners** investing in early‑stage tech in Southeast Asia. ([goldengate.vc](https://www.goldengate.vc/team?utm_source=chatgpt.com "Team"))

**Team (Key Contacts)**

- **Vinnie Lauria** — _Founding Partner_  
    LinkedIn: _(search “Vinnie Lauria LinkedIn”)_
    
- **Jeffrey Paine** — _Founding Partner_  
    LinkedIn: _(search “Jeffrey Paine LinkedIn”)_
    
- **Justin Hall** — _Partner_  
    LinkedIn: _(search “Justin Hall Golden Gate Ventures LinkedIn”)_
    
- **Angela Toy** — _Partner & COO_  
    LinkedIn: _(search “Angela Toy Golden Gate Ventures LinkedIn”)_
    
- **Michael Lints** — _Partner, MENA_  
    LinkedIn: _(search “Michael Lints Golden Gate Ventures LinkedIn”)_
    

**Target Roles:**

- Investment Associate / Analyst
    
- Sector-focused associate in tech (deep‑tech or robotics)
    
- Analyst with drone thesis
    

**Notes:**  
Golden Gate is one of **Singapore’s largest and most established VCs** — a strong place to build generalist VC experience before niche drone investing. ([goldengate.vc](https://www.goldengate.vc/team?utm_source=chatgpt.com "Team"))

---

### **4. Other Singapore VC Firms (Useful Network Targets)**

**Other firms to identify individual partners/recruiters at:**

- **Quest Ventures** — early‑stage VC with strong regional presence in Singapore. ([Wikipedia](https://en.wikipedia.org/wiki/Quest_Ventures?utm_source=chatgpt.com "Quest Ventures"))
    
- **Family offices / deep‑tech funds** connected to Temasek or government initiatives (e.g., SGInnovate, InvestHK Singapore ecosystem events). ([LinkedIn](https://sg.linkedin.com/company/investhk-singapore?utm_source=chatgpt.com "InvestHK Singapore | LinkedIn"))
    

**Why Singapore First:**  
English ecosystem, open to international recruiters, and EP visas are widely sponsored for qualified roles.

---

# 🇭🇰 **Hong Kong — VC & Innovation Funds**

### **5. Beyond Ventures (Hong Kong)**

A local VC investing across early and growth stage tech. ([LinkedIn](https://hk.linkedin.com/company/beyondventures?utm_source=chatgpt.com "Beyond Ventures 海闊天空創投"))

**Key Contacts**

- **Baniel Cheung** — investor
    
- **Brenda Tang** — investor
    
- **James Chan** — investor
    
- **Sharon Hui Wang** — investor
    

LinkedIn: _(search “Beyond Ventures [name] LinkedIn HK”)_

**Target Roles:**

- Investment analyst / associate
    
- Portfolio associate
    
- Innovation desk (focus on deep tech or robotics adjacent)
    

**Notes:**  
Hong Kong has a **finance + startup nexus** with strong connections to Mainland Chinese funds and Greater Bay Area tech initiatives — useful if your finance career leans toward cross‑border capital. ([LinkedIn](https://hk.linkedin.com/company/beyondventures?utm_source=chatgpt.com "Beyond Ventures 海闊天空創投"))

---

# 🌏 **Other Strategic Contacts to Explore (Regional, Not Drone‑Specific but Helpful)**

### **Jenny Lee — Senior Managing Partner at Granite Asia (Singapore)**

A top‑tier venture capitalist and globally recognized investor. Her profile helps with high‑level networking and market view. ([Wikipedia](https://en.wikipedia.org/wiki/Jenny_Lee_%28venture_capitalist%29?utm_source=chatgpt.com "Jenny Lee (venture capitalist)"))

**LinkedIn:** _(search “Jenny Lee Granite Asia LinkedIn”)_  
**Why:** Great connector in Asia VC ecosystem and experienced in scaling tech ventures.

---

## 📌 How to Reach Out (Template Openers)

### 1) **Informational outreach**

> Hi [Name], I’m a PhD candidate in aerial communications based in Germany. I’m building deep‑tech investment analysis and sector research in drones/robotics. I’d love to connect and learn how [Firm] thinks about early‑stage drone investments in Asia.

### 2) **Value‑adding outreach**

> Hi [Name], I just published a memo analyzing drone hardware economics in ASEAN and Japan. I’d be happy to share if useful — and would appreciate your perspective on how you view this sector from an investment lens.

---

## 📈 Roles to Target (Realistic for Your Profile)

|Firm / Region|Role Type|Likelihood w/ PhD|Visa Feasibility|
|---|---|--:|--:|
|**DRONE FUND (Japan)**|Analyst / Technical Associate|Medium‑High (with Japanese proficiency)|Medium|
|**Spiral Ventures (SG)**|Investment Associate / Analyst|High|High (Employment Pass)|
|**Golden Gate Ventures (SG)**|Analyst / Associate|High|High|
|**Beyond Ventures (HK)**|Analyst / Associate|Medium|Medium|
|**SGInnovate / Ecosystem Funds (SG)**|Sector analyst|High|High|
|**Granite Asia / Senior VCs (SG)**|Strategic insight / network role|Medium|Medium|

---

## 📌 Work Authorization Note — You Can Absolutely Pursue These

As someone **in Germany on a student/academic status with no other current work authorization**, the realistic path is:

1. **Secure an employment offer first**
    
2. **Employer sponsors work visa** in Singapore, Japan or Hong Kong
    
    - Singapore: **Employment Pass**
        
    - Japan: **Engineer/Specialist** or **Highly Skilled Professional**
        
    - Hong Kong: **Employment Visa**
        
3. Your PhD + sector expertise increases attractiveness for analyst/associate roles, especially **in VC and corporate VC**.
    

---

If you want, I can now **generate a message outreach list with pre‑written DM templates** for the contacts above (e.g., tailored emails/LinkedIn messages) and talk through _best timing_ and _follow‑up strategies_ (including how to get replies).

https://therecursive.com/your-comprehensive-guide-for-deep-tech-investors-from-cee-and-dach/

https://www.wallstreetoasis.com/academy#what-is-wso-academy


Here’s a **country-wise overview** of major **Advanced Air Mobility (AAM)** venture capital (VC), private equity (PE), strategic corporate, and finance/backing sources — focused on investments into eVTOL/AAM companies, related technologies, and infrastructure. The AAM ecosystem includes aircraft OEMs, infrastructure (like vertiports), and service platforms.

⚠️ **Note:** Comprehensive, up-to-date lists of all investors per country often require proprietary databases (Crunchbase, PitchBook), and public disclosures vary widely. This overview combines known public funding rounds, equity investments, and strategic finances tied to AAM/eVTOL startups and investors.

---

## 🇺🇸 **United States — Most Active AAM Investors & Funding**

### **Major VC / Strategic Investors**

- **Joby Aviation** (public eVTOL developer): raised **multi-billion USD** in funding; key investors include **Toyota ($500M strategic investment)**, **Delta Air Lines ($60M+)**, **Uber**, **SK Telecom ($100M)**, others totalling approx. **$2B+** funding history. ([Axios](https://www.axios.com/2024/10/02/toyota-joby-aviation-investment-evtol-air-taxi?utm_source=chatgpt.com "Toyota invests $500 million in air taxi startup Joby Aviation"))
    
- **Archer Aviation** (eVTOL): has raised **hundreds of millions** — including a **$300M round led by BlackRock** and institutional investors; also includes finance from United Airlines, Stellantis and Anduril. ([Reuters](https://www.reuters.com/business/aerospace-defense/archer-aviation-raises-300-million-blackrock-backed-funding-2025-02-11/?utm_source=chatgpt.com "Archer Aviation raises $300 million in BlackRock-backed funding"))
    
- **UP.Partners $230M AAM-focused VC Fund:** with backers like **Cathie Wood / ARK Invest, Woven Capital, Alaska Air Group** directed at electric aircraft startups like Beta Technologies. ([Reddit](https://www.reddit.com/r/electricaircraft/comments/qbjmr0?utm_source=chatgpt.com "$230M Venture Capital Fund Targets Electric Air Mobility"))
    

### **PE / Institutional & Strategic Backing**

- **BlackRock** — institutional investor in Archer and other mobility players. ([Reuters](https://www.reuters.com/business/aerospace-defense/archer-aviation-raises-300-million-blackrock-backed-funding-2025-02-11/?utm_source=chatgpt.com "Archer Aviation raises $300 million in BlackRock-backed funding"))
    
- **Stellantis & United Airlines** — financial and strategic backers of Archer via equity and production funding. ([Reuters](https://www.reuters.com/business/aerospace-defense/archer-aviation-raises-300-million-blackrock-backed-funding-2025-02-11/?utm_source=chatgpt.com "Archer Aviation raises $300 million in BlackRock-backed funding"))
    
- **Toyota** — major strategic funder of Joby. ([Axios](https://www.axios.com/2024/10/02/toyota-joby-aviation-investment-evtol-air-taxi?utm_source=chatgpt.com "Toyota invests $500 million in air taxi startup Joby Aviation"))
    
- **Uber & Delta Air Lines** — early and ongoing strategic participants in Joby’s growth. ([Investopedia](https://www.investopedia.com/joby-shares-soar-on-investment-faa-test-flight-approval-7555197?utm_source=chatgpt.com "Joby Shares Soar After $100M Investment, FAA Test Flight Approval"))
    

### **Public Listings / SPACs**

- Joby Aviation is publicly traded on NYSE (symbol: JOBY) following a SPAC merger, giving it broader public equity backing. ([Wikipedia](https://zh.wikipedia.org/wiki/%E4%B9%94%E6%AF%94%E8%88%AA%E7%A9%BA?utm_source=chatgpt.com "乔比航空"))
    

---

## 🇩🇪 **Germany / EU — European VC & Private Equity in AAM**

### **Direct AAM Companies & Funding**

- **Volocopter** (German eVTOL/UAM pioneer): historically raised large VC rounds (e.g., **€200M Series D** with BlackRock, NTT, Avala Capital, Tokyo Century). ([volocopter.com](https://www.volocopter.com/de/newsroom/200-millionen-euro-finanzierungsrunde-in-volocopter-unterzeichnet?utm_source=chatgpt.com "200 Millionen Euro Finanzierungsrunde in Volocopter unterzeichnet - Volocopter"))  
    _Recent insolvency highlights financing challenges in Europe’s AAM sector._ ([The Verge](https://www.theverge.com/2024/10/24/24278673/lilium-air-taxi-evtol-insolvency-operations?utm_source=chatgpt.com "Air taxi maker Lilium is out of money and will cease operations"))
    

### **European VC / Equity Players (may invest in AAM tech)**

- **Newfund Management** (France): early-stage VC potentially active in mobility tech (not AAM exclusive). ([Wikipedia](https://en.wikipedia.org/wiki/Newfund?utm_source=chatgpt.com "Newfund"))
    
- **High-Tech Gründerfonds (HTGF)** (Germany): tech VC/PE fund investing broadly in deep tech — could co-invest in mobility/aerospace startups. ([Wikipedia](https://de.wikipedia.org/wiki/HTGF_%28High-Tech_Gr%C3%BCnderfonds%29?utm_source=chatgpt.com "HTGF (High-Tech Gründerfonds)"))
    

### **Major EU Strategic & Industry Investors (AAM ecosystem)**

- **NEOM (Saudi ARAMCO-linked Smart Region)** — investor in Volocopter Series E. ([volocopter.com](https://www.volocopter.com/de/newsroom/zweites-signing-der-serie-e?utm_source=chatgpt.com "Volocopter sammelt EUR 182 Millionen im zweiten Signing der Serie E ein - Volocopter"))
    
- **Corporate players** like Mercedes-Benz / Geely have historically backed AAM companies (e.g., Volocopter). _Past news suggests corporate strategic backing._
    

---

## 🇬🇧 **United Kingdom**

### **Infrastructure & Investment**

- **Skyports Infrastructure** — UK company building vertiport networks, a key part of AAM infrastructure (may attract PE/VC infrastructure funds). ([Wikipedia](https://en.wikipedia.org/wiki/Skyports_Infrastructure?utm_source=chatgpt.com "Skyports Infrastructure"))
    

### **Global VC Participants with UK presence**

- Some global funds (e.g., BlackRock, Toyota) invest via UK/EU entities into AAM firms with European offices; sector crossover investment is common.
    

---

## 🇧🇷 **Brazil**

- **Eve Air Mobility** (Embraer eVTOL arm) secured **$150M+ debt financing** from banks and has raised significant equity; total funding context ~ $1.2B. ([Advanced Air Mobility Intl](https://www.aaminternational.com/funding-and-investments/?utm_source=chatgpt.com "Deals, Funding & Investments - Advanced Air Mobility Intl"))
    

---

## 🇯🇵 **Japan**

### **AAM OEM & Funding**

- **SkyDrive (Japan)**: secured **¥43 billion+** from Suzuki, Itochu, Development Bank of Japan (DBJ) and others for its SD-05 eVTOL development. ([Wikipedia](https://en.wikipedia.org/wiki/SkyDrive_%28company%29?utm_source=chatgpt.com "SkyDrive (company)"))
    

---

## 🇨🇳 **China**

### **AAM OEM**

- **TCab Tech** — Shanghai-based eVTOL developer (private financing not fully public). ([Wikipedia](https://en.wikipedia.org/wiki/TCab_Tech?utm_source=chatgpt.com "TCab Tech"))
    
- **EHang** — China’s autonomous aerial vehicle company historically funded through public markets and investors (though funding figures vary widely). ([TNMT](https://tnmt.com/newsletter-snippets/some-air-taxis-rise/?utm_source=chatgpt.com "TNMT Market Index Update: Some Air Taxis Rise"))
    

---

## **Cross-Border & Multi-Country VC Firms (Active in AAM/Deep Tech)**

### **Global / US-based but international deals**

- Global VC firms like **Founders Fund**, **Sequoia**, **Andreessen Horowitz / ARK Invest**, **Baillie Gifford**, and others have backed or are positioned to back mobility/AAM startups across geographies. ([Wikipedia](https://en.wikipedia.org/wiki/Founders_Fund?utm_source=chatgpt.com "Founders Fund"))
    

### **General Aerospace VC Lists**

- Databases like _Private Equity List_ catalog many aerospace VCs and PE investors by country (US, UK, France, Germany, China, Japan, etc.), which include investors capable of funding AAM startups. ([Private Equity List](https://privateequitylist.com/investors/venture-capital/aerospace?utm_source=chatgpt.com "Aerospace Venture Capital Firms | Private Equity List"))
    

---

## **Summary Overview by Country**

|Country|Notable AAM VC/PE/Financing Sources|Example AAM Companies Funded|
|---|---|---|
|🇺🇸 **USA**|BlackRock, Toyota, Uber, Delta, SK Telecom, UP.Partners, public markets|Joby Aviation, Archer Aviation|
|🇩🇪 **Germany/EU**|BlackRock (via rounds), NEOM strategic, Newfund, HTGF|Volocopter (historical), EU startups|
|🇬🇧 **UK**|Infrastructure funding (Skyports), global VC participation|Vertiport / services|
|🇧🇷 **Brazil**|Bank/lender financing, Embraer equity|Eve Air Mobility|
|🇯🇵 **Japan**|Suzuki, Itochu, DBJ|SkyDrive|
|🇨🇳 **China**|Private capital, public markets|TCab Tech, EHang|
|🌍 **Global VC**|Founders Fund, ARK, Sequoia, Baillie Gifford|Multiple cross-border AAM startups|

---

## **Notes on Funding Types**

- **Venture Capital (VC):** Early & growth stage equity funding (e.g., Joby, Archer, UP.Partners).
    
- **Private Equity (PE):** Later stage / buyout or infrastructure investment; sometimes corporate PE arms (BlackRock, strategic investors).
    
- **Strategic Corporate:** Airlines, automakers, industrial partners investing for commercial alignment (Toyota, Delta, United).
    
- **Debt/Bank Financing:** Loans and credit lines to support production/certification (Eve). ([Advanced Air Mobility Intl](https://www.aaminternational.com/funding-and-investments/?utm_source=chatgpt.com "Deals, Funding & Investments - Advanced Air Mobility Intl"))
    

---

If you want, I can compile this into a **searchable table or spreadsheet format** with amounts, investors, and timeline details for each funding round!

https://woven.vc/team
https://toyota.ventures/#ethan-sohn

### VC and capital, Private equity, Analyst, Due deligence , bills , International relations 


Apply: https://nfrontventures.com/jobs/venture-capital-internship-tallinn?utm_source=chatgpt.com
https://venturecapitalcareers.com/companies/rocket-internet/jobs/venture-capital-intern-global-founders-capital
https://join.com/companies/firstmomentum12/15604677-venture-scout-remote-in-europe


---
https://www.youtube.com/watch?v=gBHSmwxgLfQ impact of climate change is economical

only global coordination is market economy 
