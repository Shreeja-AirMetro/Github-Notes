BVLOS C2 links generally target sub‑second one‑way latency, tens to a few hundred kbps of throughput for C2/DAA data, and “five‑nines‑level” availability/continuity over the mission time.[icao+2](https://www.icao.int/filebrowser/download/4942?fid=4942)​

## Latency requirements

For C2 and safety‑related traffic, most aviation‑grade guidance is in the 100–1000 ms one‑way range, with tighter bounds for time‑critical functions.[icao+2](https://www.icao.int/filebrowser/download/5597?fid=5597)​

- ICAO C2 link material cites 0.5 s one‑way latency at the 99.9% level for C2, with similar or tighter bounds for situational awareness and ATC voice/data.[icao](https://www.icao.int/filebrowser/download/4942?fid=4942)​
    
- RTCA DO‑377/DO‑362A–aligned material describes C2 link one‑way latency <155 ms to support voice/“communicate” functions and <1 s for all other C2 functions, with compliance judged statistically over flight hours.[squarespace+1](https://static1.squarespace.com/static/60e5e3a2bc062b6b10b26d85/t/661f07824fdb711f3d2480b7/1713309574614/Why+RTCA+DO-377+Compliance+is+Essential+to+AAM+-+AURA.pdf)​
    

## Throughput requirements

C2 by itself is light; DAA, ATC relay, and telemetry push it to the tens–hundreds of kbps range, while payload drives Mbps‑class needs.[ntrs.nasa+3](https://ntrs.nasa.gov/api/citations/20220014741/downloads/TM-20205011515-REV1_03.2023.pdf)​

- ICAO C2 link examples assume roughly 150–500 kbps physical rates for C2/SA data, with user payload on the order of a few tens of kbps once headers and security are included.[icao+1](https://www.icao.int/filebrowser/download/5597?fid=5597)​
    
- NASA/RTCA CNPC waveform work shows C2/telemetry modes around 30–100 kbps physical data rate, sufficient for 15–20 Hz control/telemetry plus lower‑rate weather/traffic data; higher‑rate payload (video, LiDAR) is explicitly expected to use separate links with Mbps capacity.[vaibhavbajpai+2](https://vaibhavbajpai.com/documents/papers/proceedings/drones-infocom-2021.pdf)​
    

## Reliability, availability, continuity

BVLOS rulesets and RTCA standards push into aviation‑grade availability and continuity, not typical ICT SLAs.[caas+2](https://www.caas.gov.sg/docs/default-source/default-document-library/ac-anr101-2-2-bvlos-operations-for-ua_301219.pdf)​

- DO‑377‑type expectations:
    
    - Availability on the order of 0.99999 (five nines) over defined exposure (e.g., per flight hour) for the C2 link system.[squarespace](https://static1.squarespace.com/static/60e5e3a2bc062b6b10b26d85/t/661f07824fdb711f3d2480b7/1713309574614/Why+RTCA+DO-377+Compliance+is+Essential+to+AAM+-+AURA.pdf)​
        
    - Continuity targets such as “no interruption longer than 3 s with probability 0.999–0.99999 per flight hour,” depending on phase of flight.[squarespace](https://static1.squarespace.com/static/60e5e3a2bc062b6b10b26d85/t/661f07824fdb711f3d2480b7/1713309574614/Why+RTCA+DO-377+Compliance+is+Essential+to+AAM+-+AURA.pdf)​
        
- Advisory material for BVLOS stresses continuous monitoring of link integrity, bandwidth, latency, and availability, with transmission rates and fallback procedures dimensioned to maintain safe operation under worst‑case conditions.[sciepublish+2](https://www.sciepublish.com/article/pii/241)​
    

In practice, this leads to architectures with multi‑link redundancy (e.g., cellular + satellite), continuous QoS monitoring, and fast failover so that the _effective_ latency, throughput, and availability seen by the C2 application stay within these bounds over the entire BVLOS mission.[groundcontrol+3](https://www.groundcontrol.com/blog/enabling-bvlos-drone-operations-anywhere-on-earth/)​

1. [https://www.icao.int/filebrowser/download/4942?fid=4942](https://www.icao.int/filebrowser/download/4942?fid=4942)
2. [https://static1.squarespace.com/static/60e5e3a2bc062b6b10b26d85/t/661f07824fdb711f3d2480b7/1713309574614/Why+RTCA+DO-377+Compliance+is+Essential+to+AAM+-+AURA.pdf](https://static1.squarespace.com/static/60e5e3a2bc062b6b10b26d85/t/661f07824fdb711f3d2480b7/1713309574614/Why+RTCA+DO-377+Compliance+is+Essential+to+AAM+-+AURA.pdf)
3. [https://www.faa.gov/uas/programs_partnerships/test_sites/TestReport-263_Honeywell_20231120-full-Rev2.pdf](https://www.faa.gov/uas/programs_partnerships/test_sites/TestReport-263_Honeywell_20231120-full-Rev2.pdf)
4. [https://www.icao.int/filebrowser/download/5597?fid=5597](https://www.icao.int/filebrowser/download/5597?fid=5597)
5. [https://ntrs.nasa.gov/api/citations/20220014741/downloads/TM-20205011515-REV1_03.2023.pdf](https://ntrs.nasa.gov/api/citations/20220014741/downloads/TM-20205011515-REV1_03.2023.pdf)
6. [https://vaibhavbajpai.com/documents/papers/proceedings/drones-infocom-2021.pdf](https://vaibhavbajpai.com/documents/papers/proceedings/drones-infocom-2021.pdf)
7. [https://www.caas.gov.sg/docs/default-source/default-document-library/ac-anr101-2-2-bvlos-operations-for-ua_301219.pdf](https://www.caas.gov.sg/docs/default-source/default-document-library/ac-anr101-2-2-bvlos-operations-for-ua_301219.pdf)
8. [https://www.faa.gov/regulations_policies/rulemaking/committees/documents/media/UAS_BVLOS_ARC_FINAL_REPORT_03102022.pdf](https://www.faa.gov/regulations_policies/rulemaking/committees/documents/media/UAS_BVLOS_ARC_FINAL_REPORT_03102022.pdf)
9. [https://www.sciepublish.com/article/pii/241](https://www.sciepublish.com/article/pii/241)
10. [https://www.groundcontrol.com/blog/enabling-bvlos-drone-operations-anywhere-on-earth/](https://www.groundcontrol.com/blog/enabling-bvlos-drone-operations-anywhere-on-earth/)
11. [https://www.dimetor.com/100-connectivity-for-drone-bvlos-flights-the-combination-of-satellite-and-cellular-capabilities-is-the-reality-of-today/](https://www.dimetor.com/100-connectivity-for-drone-bvlos-flights-the-combination-of-satellite-and-cellular-capabilities-is-the-reality-of-today/)
12. [https://www.rtca.org/wp-content/uploads/2020/12/LIST-OF-AVAILABLE-DOCS-AS-OF-SETEMBER-2020-.pdf](https://www.rtca.org/wp-content/uploads/2020/12/LIST-OF-AVAILABLE-DOCS-AS-OF-SETEMBER-2020-.pdf)
13. [https://consultations.caa.co.uk/future-safety/detect-and-avoid-policy-concept-consultation/supporting_documents/CAP3015%20Detect%20and%20Avoid%20Policy.pdf](https://consultations.caa.co.uk/future-safety/detect-and-avoid-policy-concept-consultation/supporting_documents/CAP3015%20Detect%20and%20Avoid%20Policy.pdf)
14. [https://www.easa.europa.eu/en/document-library/easy-access-rules/online-publications/easy-access-rules-unmanned-aircraft-systems?page=4](https://www.easa.europa.eu/en/document-library/easy-access-rules/online-publications/easy-access-rules-unmanned-aircraft-systems?page=4)
15. [https://www.autonomyglobal.co/bvlos-infrastructure-utilities-operations-the-value-proposition-of-section-44807/](https://www.autonomyglobal.co/bvlos-infrastructure-utilities-operations-the-value-proposition-of-section-44807/)
16. [https://www.dronespace.at/jart/prj3/dronespace/data/uploads/europaeisches_regulativ/EAR%20for%20UAS%202022.pdf](https://www.dronespace.at/jart/prj3/dronespace/data/uploads/europaeisches_regulativ/EAR%20for%20UAS%202022.pdf)
17. [https://www.federalregister.gov/documents/2025/08/07/2025-14992/normalizing-unmanned-aircraft-systems-beyond-visual-line-of-sight-operations](https://www.federalregister.gov/documents/2025/08/07/2025-14992/normalizing-unmanned-aircraft-systems-beyond-visual-line-of-sight-operations)
18. [https://www.rtca.org/wp-content/uploads/2020/08/List-of-Available-Docs-December-2019.pdf](https://www.rtca.org/wp-content/uploads/2020/08/List-of-Available-Docs-December-2019.pdf)
19. [https://www.easa.europa.eu/en/downloads/139435/en](https://www.easa.europa.eu/en/downloads/139435/en)
20. [https://assureuas.org/wp-content/uploads/2021/06/A2-Final-Report.pdf](https://assureuas.org/wp-content/uploads/2021/06/A2-Final-Report.pdf)

