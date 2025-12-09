
Here are several key academic papers and surveys on antenna placement and propagation modeling related to UAVs:

---

### 📚 Surveys & Reviews

#### • **A Survey of Air‑to‑Ground (AG) Propagation Channel Modeling for UAVs**

Authors: Khawaja, Guvenc, Matolak, Fiebig, Schneckenberger (2019, IEEE Comms Surveys & Tutorials)  
This comprehensive review covers measurement campaigns, large/small-scale fading, Doppler effects, and typical UAV-to-ground channel models across urban, suburban, rural, and over-water scenarios ([elib.dlr.de](https://elib.dlr.de/128128/?utm_source=chatgpt.com "electronic library - A Survey of Air-to-Ground Propagation Channel Modeling for Unmanned Aerial Vehicles")).

#### • **A Review of UAV‑Based Antenna and Propagation Measurements**

Source: MDPI Sensors (2024) / PubMed summary  
Focuses on practical in-situ UAV antenna measurements: optimal mounting, reducing coupling effects, path-loss modeling including altitude-dependent models and ground reflections ([PubMed](https://pubmed.ncbi.nlm.nih.gov/39599171/?utm_source=chatgpt.com "A Review of Unmanned Aerial Vehicle Based Antenna and Propagation Measurements - PubMed")).

---

### 🎯 Targeted Studies

#### • **UWB Air‑to‑Ground Propagation Channel Measurements using UAVs**

Authors: Khawaja, Ozdemir, Erden, Guvenc, Matolak (2018, arXiv)  
Experimental UWB measurement (3.1–4.8 GHz) for different UAV heights/orientations, showing received power depends on elevation-plane antenna pattern ([arXiv](https://arxiv.org/abs/1812.06603?utm_source=chatgpt.com "UWB Air-to-Ground Propagation Channel Measurements and Modeling using UAVs")).

#### • **Propagation Modeling for Mountainous Regions (Ray Tracing)**

Study from MDPI Drones (2024)  
Examines propagation in rugged terrain with RT-based models, detailing foliage loss (up to ~10 dB/m in dense forest) and UHF vs mmWave pathloss ([MDPI](https://www.mdpi.com/2504-446X/8/7/334?utm_source=chatgpt.com "Propagation Modeling of Unmanned Aerial Vehicle (UAV) 5G Wireless Networks in Rural Mountainous Regions Using Ray Tracing"), [Wikipedia](https://en.wikipedia.org/wiki/Egli_model?utm_source=chatgpt.com "Egli model")).

#### • **3D Placement of UAV Base Stations / Relays**

- _Alzenad et al. (2017)_: Maximize coverage with 3D placement algorithms (ES and low-complexity MWA) for UAV-BS ([arXiv](https://arxiv.org/abs/1709.05235?utm_source=chatgpt.com "3D Placement of an Unmanned Aerial Vehicle Base Station for Maximum Coverage of Users with Different QoS Requirements")).
    
- _Cherif et al. (2020)_: Optimal 3D positioning of directional-antenna UAV-BS to serve aerial users while maintaining spectrum-sharing with terrestrial networks ([arXiv](https://arxiv.org/abs/2008.09262?utm_source=chatgpt.com "On the Optimal 3D Placement of a UAV Base Station for Maximal Coverage of UAV Users")).
    
- _Zhao et al. (2023)_: Integrates UAV placement with beamforming for multi-user communications using simulations and field trials ([ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0045790623000897?utm_source=chatgpt.com "3D placement of UAVs with optimal beamforming for multi-user communications - ScienceDirect")).
    

---

### 🛠️ Practical Measurement & Placement Insights

- **Altitude-influenced path loss**: Field studies (e.g., hexacopter with cloverleaf antenna) show Rician K-factor increases with UAV altitude; small-scale fading modeled via log‑logistic or Nakagami distributions ([MDPI](https://www.mdpi.com/1424-8220/24/22/7395?utm_source=chatgpt.com "A Review of Unmanned Aerial Vehicle Based Antenna and Propagation Measurements")).
    
- **Diffraction & scattering**: Knife-edge diffraction models (KED/UTD) validated at mmWave (~28 GHz), with building rooftops introducing significant scattering ([MDPI](https://www.mdpi.com/1424-8220/24/22/7395?utm_source=chatgpt.com "A Review of Unmanned Aerial Vehicle Based Antenna and Propagation Measurements")).
    
- **Antenna placement tips**: Reducing ground coupling and reflections by elevating UAV antennas; ground plane integration improves GNSS RTK performance ([ars.copernicus.org](https://ars.copernicus.org/articles/20/23/2023/?utm_source=chatgpt.com "ARS - Impact of Additional Antenna Groundplanes on RTK-GNSS Positioning Accuracy of UAVs")).
    

---

### ➡️ Suggested Next Steps

1. **Pick foundational surveys**: Start with Khawaja et al. (2019) and the MDPI review for a solid overview.
    
2. **Dive into measurement-focused papers**: Explore UWB AG experiments and altitude-differentiated channel studies to inform practical designs.
    
3. **Investigate UAV base-station placement studies**: For optimization strategies on 3D deployment considering user distribution and regulatory constraints.
    

---

Would you like help obtaining full-text PDFs, or a comparison of their methodologies? I can also look into placing related source code or simulation datasets if you're implementing your own UAV channel model.