
Collaboration with T2 
https://vtsociety.org/post/announcement/call-papers-special-issue-low-altitude-wireless-networks-lawn#:~:text=Low%2DAltitude%20Wireless%20Networks%20(LAWN)%20represent%20a%20paradigm%20shift,across%20aerial%20and%20terrestrial%20nodes.

6/11
- Regular Paper 
- 100-3000m Low-altitude airspace 
- Low-Altitude Wireless Networks (LAWN) represent a paradigm shift from conventional aerial communications by introducing a multifunctional, service-aware, and dynamically reconfigurable 3D network fabric that integrates communication, sensing, control, and distributed computing across aerial and terrestrial nodes. LAWN enables intelligent, mission-driven aerial operations and supports future autonomous systems by combining cross-layer design principles with advanced technologies.
Potential Topic 
- Scalable Air Traffic Management for LAWN
- URLLC for Safety-Critical Applications in LAWN
- Air-to-Ground and Air-to-Air Channel Modeling and Measurement for LAWN


Roshan's direction 

RIS material simulator start with near-field 
Implementation Near-field simulator for FEM - EM scattering 
that can be moved to far-field parameters - by far-field transformers 

Far-field - Antenna gain , reflector 
Ray tracing get RSSI and RSRP 

3D environemnt 

Check 
Ray tracing simulator 
Circuit modeling - cannot  work for physics based flying 

MMwave and RSSI and how it used 
MMwave for drone 
Database of current antennas - geospatial map

HW 
SoA - RSSSI and RSRP of ray tracing from Mmm wave
mmwave for drone operatoin 

Ray tracing

- Latex - write about our goal and discussed
- Sienna at different heights coverage map 
mm wave and the 
- ideal RIS parameters
- multi-physics based 
https://nvlabs.github.io/sionna/rt/index.html 
https://ieee-aess.org/technical-committee/low-altitude-wireless-networks-technical-working-group

https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9424177

Germany government link 
https://gigabitgrundbuch.bund.de/GIGA/DE/Roadmap/start.html
https://gigabitgrundbuch.bund.de/GIGA/DE/_Home/start.html
https://gigabitgrundbuch.bund.de/GIGA/DE/Funklochkarte/start.html
https://gigabitgrundbuch.bund.de/GIGA/DE/Downloads_Suche/Formular.html#searchResult
https://www.geoportal.de/info/tk_03-netzabdeckung_mobilfunk

Openmap
https://opencellid.org/#zoom=14&lat=51.03984&lon=13.73236
https://www.reddit.com/r/cellmapper/comments/hnvqqh/noob_reading_cellmapper_map/

https://www.cellmapper.net/map?MCC=262&MNC=1&type=LTE&latitude=51.05278891249753&longitude=13.23739078683101&zoom=13.861113944109777&showTowers=true&showIcons=true&showTowerLabels=true&clusterEnabled=true&tilesEnabled=true&showOrphans=false&showNoFrequencyOnly=false&showFrequencyOnly=false&showBandwidthOnly=false&DateFilterType=Last&showHex=false&showVerifiedOnly=false&showUnverifiedOnly=false&showLTECAOnly=false&showENDCOnly=false&showBand=0&showSectorColours=true&mapType=roadmap&darkMode=false&imperialUnits=false

https://www.radartutorial.eu/06.antennas/Antenna%20Characteristics.en.html

# 1) How TVT special issues typically review & timing

- TVT’s editorial goal is to complete the **first review cycle within ~3 months**; community-reported stats show **first review ≈ 2.9 months** and **total handling for accepted manuscripts ≈ 7.8 months**, with an **average ~2.7 rounds** of review. That matches expectations for a high-rank IEEE Transactions. [vtsociety.org+1](https://vtsociety.org/publication/ieee-transactions-vehicular-technology/information-editors/first-review-cycle?utm_source=chatgpt.com)
    
- **Acceptance rates** for TVT (and most IEEE Transactions) are not published publicly for every issue. Expect a _low_ acceptance probability for a special issue in a hot topic because high-quality groups target these calls. Community anecdotes indicate high selectivity. [SciRev](https://scirev.org/journal/ieee-transactions-on-vehicular-technology/?utm_source=chatgpt.com)
    

# 2) Is “RIS + RSSI/RSRP conversion for low-altitude drone operation” novel enough?

Short verdict: **Possibly — but only if you add something substantively new.** Here’s why:

What’s already out there

- RIS + UAV (RIS-assisted UAV or RIS-UAV) is a well-established and rapidly growing subfield: surveys, arXiv papers, MDPI and conference/IEEE papers discuss RIS placement, energy/trajectory co-design, channel modeling, and performance gains for UAVs. So _basic_ RIS-UAV proposals are not novel by default. [arXiv+1](https://arxiv.org/abs/2504.02162?utm_source=chatgpt.com)
    
- RSSI ↔ RSRP conversions and their formulas are standard in cellular engineering (RSRP = reference-signal based metric; RSSI measures total received power including noise/interference). Tools and calculators for converting exist because these metrics are widely used in LTE/5G measurements. [Digi International+1](https://www.digi.com/support/knowledge-base/understanding-lte-signal-strength-values?utm_source=chatgpt.com)
    

When your idea _would_ be novel for this TVT LAWN special issue

- You develop a **new measurement model or conversion algorithm tailored to low-altitude aerial channels with RIS in the propagation path** (e.g., account for altitude-dependent multipath, drone body blockage, high Doppler, controllable RIS phase patterns, and dynamic geometry).
    
- **You validate on real hardware or a realistic testbed** (in-flight measurements with RIS assisted links, or a carefully instrumented field experiment). The LAWN call explicitly welcomes real-world prototypes/testbeds — that strongly improves novelty/acceptance chances. [vtsociety.org](https://vtsociety.org/publication/transactions-vehicular-technology/call-papers?utm_source=chatgpt.com)
    
- You demonstrate **practical benefit** (e.g., better link adaptation, more accurate ranging/positioning, improved handover decisions, or improved spectral efficiency) and compare to baseline industry/academic methods (standard RSSI→RSRP heuristics).
    
- You provide **cross-layer insights** (how the conversion affects MAC/handovers, or how RIS control + conversion improves network-level KPIs), since TVT likes system-level/vehicular implications.
    

# 3) Concrete checklist to make the submission competitive for the TVT special issue

1. **Clear novelty statement**: exactly what is new (theory, algorithm, model, dataset, testbed).
    
2. **Channel/modeling contribution**: derive an analytical or data-driven conversion model that captures low-altitude specifics and RIS effects (not just apply LTE formulas blindly). Cite and contrast with standard RSSI/RSRP relations. [Digi International+1](https://www.digi.com/support/knowledge-base/understanding-lte-signal-strength-values?utm_source=chatgpt.com)
    
3. **Validation**: at least high-fidelity simulations with 3D mobility + RIS modeling _and_ (strongly preferred) measured data from a hardware test or proof-of-concept. The special-issue call highlights prototypes/testbeds. [vtsociety.org](https://vtsociety.org/publication/transactions-vehicular-technology/call-papers?utm_source=chatgpt.com)
    
4. **System impact**: show how the conversion matters — e.g., improves handover accuracy, power control, situational awareness in LAWN scenarios.
    
5. **Compare baselines**: standard RSSI→RSRP conversions, RIS-free scenarios, existing RIS-UAV works. [arXiv+1](https://arxiv.org/abs/2012.04775?utm_source=chatgpt.com)
    
6. **Paper preparation**: follow TVT formatting; consider a longer regular paper if you have thorough experiments (TVT allows up to 14 pages for full papers). [vtsociety.org](https://vtsociety.org/publication/transactions-vehicular-technology/call-papers?utm_source=chatgpt.com)
    

# 4) Recommended framing for reviewers (short paragraph you can adapt)

“We propose a _low-altitude channel-aware RSSI→RSRP conversion and calibration method_ that explicitly models RIS-altered propagation and UAV dynamics. We validate via (i) a 3D ray-tracing + mobility simulation study, and (ii) in-flight measurements with a prototype RIS-assisted link. Results show X dB improvement in RSRP estimation accuracy and Y% improvement in handover/throughput compared to standard LTE conversions — demonstrating practical benefit for LAWN deployments.”  
If you can truthfully write something like that, you’ll be in a competitive position.

# 5) Final recommendations / next steps

- If you want, I can:
    
    1. Draft a **short outline** and novelty paragraph (tailored to the TVT LAWN call) you can paste into your submission.
        
    2. Help design an **experiment plan** (simulator + measurement checklist) focusing on RIS effects on RSSI/RSRP at low altitudes.
        
    3. Search for **recent RIS-UAV experimental papers** to cite and to show the gaps your work fills. (I already found surveys and experimental-ish papers; I can fetch more targeted examples.) [arXiv+1](https://arxiv.org/abs/2504.02162?utm_source=chatgpt.com)
        

Would you like me to draft a submission abstract and the “what’s new” paragraph now, or to build a suggested experiment plan (simulator parameters, UAV altitudes, metrics to collect)?

---
