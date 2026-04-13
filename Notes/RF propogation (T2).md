
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

----

In the world of 5G and the upcoming 6G, the transition from "Far-Field" to "Near-Field" is one of the most significant shifts in how we handle radio signals. As we move to higher frequencies (GHz) and larger antenna arrays, the physical behavior of the wave changes, which directly impacts the data used to manage connections (**Channel State Information** or **CSI**).

---

## 1. The Basics: Near-Field vs. Far-Field

The boundary between these two regions is defined by the **Fraunhofer Distance** (![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABMAAAAYCAYAAAAYl8YPAAABjElEQVR4AeyUPShFYRjH32RC+ZhkkMlAspEUk0KRjDaTgYGySmTwMcqgFIssLMpHiCiKFCnKIGKwSRmIgd//zVvn3nOd17mM9/b/Pc9zn3Pe/33Pc95ulvnHT8Ys/jCjZlaP3TV8wjZ4FWV2yGoZksyRgo8oM61tVoAD8Mpn1orDG8TeWT6L5uAR9mEUWmADXsErt7Nc7lyDEiiHRlBdQN6EX8mZjXG3hj1AfgHpRgF+epNDXDuGGbCSWTFVP2jIOgqUVg3ES7iFZBXSGIRJuAMrmVXbypjg4+TRk9kWOZXqaJ7ACkyBlcyybWWMLn6XppYiB3agBnrBaZhiGspAIygiW8lMh1Nz0tbVrCDMg3RG6IN1cBqh0KzGyU3wBFYye6bqgB7QkZggd8IDzMIeJM9NozmnnyCZqbFL0K/oSLRRn0IptIPbJaWVHl/H58J+CwRnFmh5yyru0Fv/ICcoHbNKHK4gpHTMNC+dyT+ZdbN6GfS2V8khxdmZ/j3ecViAewgpjtkSq7tgEVLqCwAA//+xU7dpAAAABklEQVQDAB1ZQTHPwI9tAAAAAElFTkSuQmCC)). This is a function of the antenna's physical size (![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABEAAAAYCAYAAAAcYhYyAAABS0lEQVR4AeySTSuEURiGh1CKPyApZWNDyUIhH8XC2hILf8F/8CvsLPwDkXxTIhYWZGNjRylfC1Fc1zvvO03nnFlMzXKm+zrPOc9zuuec57ytpQb8miZxE8OejLBlD17hD+7BtRwxf4djmIGKQpMbKnOwA2qewbVMM++BD7A+ScwUmmRJBjfcEp+gWp8sVuEb1iFTymSYSi/sQkrPJK9hAjqhlDLxCtYOHGrQnue9XtLE+/+w6QxSaiM5BOrFITxJF8kpOAXvT4g0TqYbvJKvFZ1Egw427EMtLeaFjTxGJkU/DosNQexjvQKeYpOYKbzOAtk3uIJQXmGLpM/uvi/mmapN+skMwAn8QqEWJrNwCY8wBj4zoSxNbNQFywdQowx+5gV3rJdgDZYhargm5xR0t6H+q2/vMxcMUvcr3SYmpUmyUE+yaRJ3qyE9+QcAAP//piLCOAAAAAZJREFUAwDqbDYxlq9pOQAAAABJRU5ErkJggg==)) and the signal's wavelength (![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAsAAAAYCAYAAAAs7gcTAAAA90lEQVR4AdySPctBYRyHj6ennp6PIMkgWRSl5BuYpCgvg4nV6ItgtBkMQsrgG+AreBmUzWYwGVw/dZ8cbsVicPpd/3Pf//vqnPu8/DhvHJ+Te+xqDQ14yP02qhgLaEEAPLmXtdhRgSJ4YpOXGDt4ScZzBpQ0hMGN7cpaHKlACdw8k+cYG/Bs5ZnsQ9xDHGJwjU1Wr8vqFpSCitCCzoZfBn04Qh1WUIFrbuU/OkMIQhOUCSUKKXCM/M9kChHIwRkU81bKmkjWw6iZpJGFA5jo02sreRo+ybpqgkkNzEMxdNNmFIKM5BMDP4zBFv0ruvtMsk2w9r5evgAAAP//vFxJuQAAAAZJREFUAwAOISAxq2gUEgAAAABJRU5ErkJggg==)):

![](data:image/png;base64,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)

### The Far-Field (Fraunhofer Region)

- **Distance:** Greater than ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABMAAAAYCAYAAAAYl8YPAAABjElEQVR4AeyUPShFYRjH32RC+ZhkkMlAspEUk0KRjDaTgYGySmTwMcqgFIssLMpHiCiKFCnKIGKwSRmIgd//zVvn3nOd17mM9/b/Pc9zn3Pe/33Pc95ulvnHT8Ys/jCjZlaP3TV8wjZ4FWV2yGoZksyRgo8oM61tVoAD8Mpn1orDG8TeWT6L5uAR9mEUWmADXsErt7Nc7lyDEiiHRlBdQN6EX8mZjXG3hj1AfgHpRgF+epNDXDuGGbCSWTFVP2jIOgqUVg3ES7iFZBXSGIRJuAMrmVXbypjg4+TRk9kWOZXqaJ7ACkyBlcyybWWMLn6XppYiB3agBnrBaZhiGspAIygiW8lMh1Nz0tbVrCDMg3RG6IN1cBqh0KzGyU3wBFYye6bqgB7QkZggd8IDzMIeJM9NozmnnyCZqbFL0K/oSLRRn0IptIPbJaWVHl/H58J+CwRnFmh5yyru0Fv/ICcoHbNKHK4gpHTMNC+dyT+ZdbN6GfS2V8khxdmZ/j3ecViAewgpjtkSq7tgEVLqCwAA//+xU7dpAAAABklEQVQDAB1ZQTHPwI9tAAAAAElFTkSuQmCC). In traditional 4G/5G (sub-6 GHz), this is usually just a few meters.
    
- **Waveform:** The radio waves behave like **Plane Waves**. They arrive at the receiver as flat, parallel "sheets."
    
- **Modeling:** We only care about the **angle** of the signal (where it's coming from). The distance doesn't change the shape of the wave.
    

### The Near-Field (Fresnel/Radiative Region)

- **Distance:** Less than ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABMAAAAYCAYAAAAYl8YPAAABjElEQVR4AeyUPShFYRjH32RC+ZhkkMlAspEUk0KRjDaTgYGySmTwMcqgFIssLMpHiCiKFCnKIGKwSRmIgd//zVvn3nOd17mM9/b/Pc9zn3Pe/33Pc95ulvnHT8Ys/jCjZlaP3TV8wjZ4FWV2yGoZksyRgo8oM61tVoAD8Mpn1orDG8TeWT6L5uAR9mEUWmADXsErt7Nc7lyDEiiHRlBdQN6EX8mZjXG3hj1AfgHpRgF+epNDXDuGGbCSWTFVP2jIOgqUVg3ES7iFZBXSGIRJuAMrmVXbypjg4+TRk9kWOZXqaJ7ACkyBlcyybWWMLn6XppYiB3agBnrBaZhiGspAIygiW8lMh1Nz0tbVrCDMg3RG6IN1cBqh0KzGyU3wBFYye6bqgB7QkZggd8IDzMIeJM9NozmnnyCZqbFL0K/oSLRRn0IptIPbJaWVHl/H58J+CwRnFmh5yyru0Fv/ICcoHbNKHK4gpHTMNC+dyT+ZdbN6GfS2V8khxdmZ/j3ecViAewgpjtkSq7tgEVLqCwAA//+xU7dpAAAABklEQVQDAB1ZQTHPwI9tAAAAAElFTkSuQmCC). In mmWave (24-52 GHz) and 6G (100+ GHz) with large antenna arrays, this region can extend to **dozens or even hundreds of meters**.
    
- **Waveform:** The waves are **Spherical**. Because the receiver is so close to a large antenna, the "curve" of the wave is noticeable.
    
- **Modeling:** We must care about both the **angle** and the **exact distance (depth)**.
    

---

## 2. Impact on Channel State Information (CSI)

CSI is the "status report" the receiver sends to the base station so it knows how to beamform (aim) the signal. In 5G, URLLC (**Ultra-Reliable Low-Latency Communication**) depends on perfect CSI to avoid dropped packets and delays.

### The "Curse" of Near-Field for CSI

1. **Increased Complexity:** In the far-field, the base station only needs a 2D map (angle) to find you. In the near-field, it needs a **3D map** (angle + distance). This makes the CSI much "heavier" and harder to calculate quickly.
    
2. **Spatial Non-Stationarity:** Because the receiver is so close, different parts of a large antenna array might "see" different environments or obstacles. The CSI isn't uniform across the antenna, requiring more processing power to align the signal.
    

### The "Gift" for URLLC

1. **Beam Focusing (Not just Steering):** In the far-field, we "steer" a beam in a direction. In the near-field, we can **"focus"** a beam to a specific spot in 3D space (like a magnifying glass focusing sunlight).
    
2. **Reduced Interference:** Because the beam is focused on a specific point rather than a general direction, it doesn't "leak" onto other users as much. This increases the **Reliability** part of URLLC.
    
3. **Higher Degrees of Freedom:** Near-field spherical waves allow for more data streams (MIMO) even in simple environments, which helps maintain the high data rates required for low-latency tasks like remote surgery or industrial robotics.
    

---

## 3. How They Are Connected

The connection between these domains is essentially a **trade-off between mathematical complexity and signal precision.**

|**Feature**|**Far-Field (Traditional)**|**Near-Field (High GHz / Large Arrays)**|
|---|---|---|
|**Wave Shape**|Plane (Flat)|Spherical (Curved)|
|**CSI Focus**|Angle only|Angle + Distance (Depth)|
|**URLLC Benefit**|Simple to calculate (Low Latency)|High Precision/Focus (High Reliability)|
|**Challenge**|Higher interference|Massive processing overhead|

### Summary for 5G/6G

As 5G uses higher frequencies (![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAwAAAAYCAYAAADOMhxqAAABBElEQVR4AdySr4pCQRjFh2WX3bB59wG2LAqiYjCYBNGX8B2sNoNZQTDoaxhEBAUxmEQQk8UiWMQoNn9HnHDnzghWL+d3v5n5zmHm/nkzT16vHvjifbRhAStIgnn00E0MZZjCH/xCMPBJswpDaMA/TCAYKND8AZku1D3c5B5JRxjT6YNU46Z5kXqTGxixWoI57EBjoZ2YmuCRsnQ3EJO7gwzf3BKwhph8gTQurevdM4xKjeiKMan7wvJeI8UX0A5HXFuIyRfI4JqBV27gA5d20BdmGJcN6IN1aefhHQbglQ306Op3UFDjA3OvbKBD9wwVqENQNtDCoePkqCcIygaCBrfxdOAKAAD//0zXmmEAAAAGSURBVAMAeqMhMbSf3XYAAAAASUVORK5CYII=)) like 28 GHz, the wavelength (![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAsAAAAYCAYAAAAs7gcTAAAA90lEQVR4AdySPctBYRyHj6ennp6PIMkgWRSl5BuYpCgvg4nV6ItgtBkMQsrgG+AreBmUzWYwGVw/dZ8cbsVicPpd/3Pf//vqnPu8/DhvHJ+Te+xqDQ14yP02qhgLaEEAPLmXtdhRgSJ4YpOXGDt4ScZzBpQ0hMGN7cpaHKlACdw8k+cYG/Bs5ZnsQ9xDHGJwjU1Wr8vqFpSCitCCzoZfBn04Qh1WUIFrbuU/OkMIQhOUCSUKKXCM/M9kChHIwRkU81bKmkjWw6iZpJGFA5jo02sreRo+ybpqgkkNzEMxdNNmFIKM5BMDP4zBFv0ruvtMsk2w9r5evgAAAP//vFxJuQAAAAZJREFUAwAOISAxq2gUEgAAAABJRU5ErkJggg==)) gets smaller. If we also use larger antennas (![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABEAAAAYCAYAAAAcYhYyAAABS0lEQVR4AeySTSuEURiGh1CKPyApZWNDyUIhH8XC2hILf8F/8CvsLPwDkXxTIhYWZGNjRylfC1Fc1zvvO03nnFlMzXKm+zrPOc9zuuec57ytpQb8miZxE8OejLBlD17hD+7BtRwxf4djmIGKQpMbKnOwA2qewbVMM++BD7A+ScwUmmRJBjfcEp+gWp8sVuEb1iFTymSYSi/sQkrPJK9hAjqhlDLxCtYOHGrQnue9XtLE+/+w6QxSaiM5BOrFITxJF8kpOAXvT4g0TqYbvJKvFZ1Egw427EMtLeaFjTxGJkU/DosNQexjvQKeYpOYKbzOAtk3uIJQXmGLpM/uvi/mmapN+skMwAn8QqEWJrNwCY8wBj4zoSxNbNQFywdQowx+5gV3rJdgDZYhargm5xR0t6H+q2/vMxcMUvcr3SYmpUmyUE+yaRJ3qyE9+QcAAP//piLCOAAAAAZJREFUAwDqbDYxlq9pOQAAAABJRU5ErkJggg==)), the Fraunhofer distance (![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADcAAAAYCAYAAABeIWWlAAAD/0lEQVR4AdyXR6gUWRSG28k5J2aYYYYJzMAEmJnF5GhOiFlBBRXUhWAGFwqKGEDFhQtBwYRgQEVFMeesC8W0MKCoCxMmMIt+X1v3UV1d1dqP9vHw8X91bp1zq2+dWze9p3JP8F9NJzeUvlwFO6A+PFbVZHKdyeQu1IM+sAS+hUfR9EeplKwTT+5vgjvhKmi7YSupj/ixpqC2cTkBLeBh+pUKFyGul7g5ALvgL0hVSO4nopNhEHwDx2AKDIBKaRQ/5Itics9zMdlT2IepIxXmQVzXuPkZTHISNlUhudFEe8N6sMEu2OMwHN6FpMbj2A334DY4jwKHuD8HY8EkMEXqjsffn4stpacJ2iFbsEldxzEN/Bh+HIqFMjn5BfdEeB3UTS4r4EVoDkn1w2EHYHJTuTiPAjZmrBf+ZI/jyn3HpSU0AL8AJlMNiayELIXfb5dWwcTkBsEvIP6VQsN+ekJF+j3yrI5s3Czjxs5qhvUFMXm9wnUgONccIf9QLqW2BEt9Xb++K29r6tWBApnYHTx14X84AkFhJTsYHAnrMw7JrJ51mPrIn17Axh2qvqzDyN7+FH+WXiDwPeyBUlpI8DP4Awpkcjr2clkLQVZ29XSsx/0h/gwFh6G9dolymp6NnB9Gtj+2B7gFrMPOhqOQpVYE7AhMSYU61i+oGJIrcHIzDM5Ae3DRwBTIIfkGno2QpR+iwPnI+tX8enE2RbE0Y9sz0wIJn9vEZXxtwAUI80BpyXUg5H7UGOu8wBTJIalzjZcM/ov8WyNbjnmHyi9DVvuE8rLeIkqOBkeIo43bB0om51wYSciVbD82S85PN3uHbVodG3KxOEnQhjFlySHmXCr10HsE7dxx2CGgXIC0eeLJfYxnDnhMcuenmPuXiysbpkrvU3LvcUi6ZXBbJFdE59xgIi5YmLLk6ue7ZD30CQHbX4pdDK6a27EmZ7sUc7mQnCvTfDz2QHwe/IbP8yCmSn5Vb/xxbRLHvmfHvgRmQbmy82zzbMaDX+HfAPvA98Xk5Zd+k1ITyCsk5xHmSzxdwVOKpwwXghHcH4a4wri2gbj/LW7GwARoBFpM2XIhCZtz8uEPcLj1uNh1omwnYPIqWjVN7jVCnihc/VwofPmv8b0NynOm1g44TcEOwOQ8grmXyWYcTmxXrh8pL4fqymmwIOPhz/E/B543PXhQrJJD0wR9Pv/uJneFcJ0S3CKmenLxsBvquh2414kbqJu1Z1R7larVkvPefdNOSvsBFzAXq9DhyToeDF7FeQGq5pzlmiO7Jbchez+7RhkRv1wZ1R97VfdXF4aKNFSbkvPg7j+wyblU7URrU3JuO543q51M8sHalNwMXs5NGVMZ1abkKpNR7FfuAwAA///iSX1BAAAABklEQVQDAGyDrTFulkSSAAAAAElFTkSuQmCC)) grows. This means more users will naturally fall into the **Near-Field** zone. For URLLC to work, engineers are developing "Near-Field CSI" models that can handle spherical waves without adding too much computational delay.

**Would you like me to calculate the specific Near-Field boundary for a particular 5G frequency and antenna size?**

To make your paper stand out for the **LAWN** special issue, you must clearly define the "Sidelobe Cliff"—a phenomenon that is often overlooked in ground-centric 5G research but is a "killer" for aerial URLLC.

Below is the detailed breakdown of this concept and a concrete simulation scenario modeled after a European urban environment (e.g., Frankfurt or Berlin).

---

## 1. The "Sidelobe Cliff" Explained

The **Sidelobe Cliff** refers to the sudden and catastrophic drop in signal strength (SINR) that a drone experiences when its vertical or horizontal movement causes it to fall out of a radiation lobe and into an **antenna null**.

### Why it happens to Drones:

- **The Downtilt Paradox:** In European urban centers, 5G Base Stations (BS) are typically mounted at 20–30m and tilted **downwards** (by ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABEAAAAXCAYAAADtNKTnAAABf0lEQVR4AeyTvSuFYRjGH+RrEIUBZREZLUrZWIwoBhb/gCiTlFA2iSglFtkMBoNBlBQZfGQxWHyUIpTBZ4rf9eTWk9P7nuUMZzin6/dc9/12n+u87/M+J9ul4JO+IY083RrswCaox+IVPk4XoxswBS2wBeuQA1IeywBMwhAUgJeFVNAtwwwcgqTQKopKkKZZjmEEDmAOvCxkkK4IVsA0QTEGNyB9s+yBtM/yAl4W0k73ALdg0p6MW4O/QqgPaxRSQlMHd9ADu6DbHcZzwXRJ0QxSE8sFeCmk1FfOleEaasXboBMWwbRA8Q7aXPkStZdCCn3lXDk+Cl/wDKvQBw1gOqKYhVP4k0Kefrsr/BFM2iPV3VriUIgN3/8b1B3pUrGWOBTyycAJ5EMo21Q9Wng9oVaILuqo11DYFyn9Rsu3tcRhITqp1wzqNGbheu29+Dzof4RFy0LeGOmAWjiHM9Db6cd1UrFoWYgmdHj06/U01aBXiSVXGJJ8OmIiE5K4MT8AAAD//68zvxoAAAAGSURBVAMAyKpAL4rcB20AAAAASUVORK5CYII=) to ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABsAAAAXCAYAAAD6FjQuAAAB1UlEQVR4AeyUyytuURjGt3M6xzV/gCgyEaGIGIkwUEphIBOFlISJgeQ+kAnFxEByS4zIyKVMTAwMDWXAiAzknlt+z26tj9jfrWTC1/Nbz7vevdZ611pfe/9xvvH3s4pFcLMp4KVIklNwBiewCIkQkt5fYwIzqmALxsBLsyQfIRPaoRJ2IR6ssglGQGvk4T7ZYpq4QbYUisBLxSS1IY09JV6FbkiGXpDSafR8CO+BFlBxzHFssQl6WdAG2jn2SflkCqETrNZNUGO8HB+EO8MAXgaubDG3E6TRJv4xRpvCXN24rePEGn8y/t4ebCecYpNMaoAOsLKFD0xiGW+FaEMjvgSuwimmk80x6xKs6kwwavwc1/+la60lVl45wrf/zO2E2aQxvhn6YBOsbgkWYB7uwSd/J4vwjfAOYkivgBYcxkOSv2KBJmsj0wzYhyYIWf6KaUF/i/TzQCfTFT4TS+NqghFusWoWrIB6eAHpP00OBNXHYvr2Kaf35uPpMlhtBv7CGugaj/ErkGOBpYU1ooRmDy4gCtQ/xLchDiS9Y/oG6hT6rOWSTAKd7AgPKltsh5EFoJdRJxKp9PWpucalLhrlvdD/yOPAssUCj/qip7/FvuQiv/UaXwEAAP//RrJZhQAAAAZJREFUAwAQYkQvkuyU5wAAAABJRU5ErkJggg==)) to serve pedestrians.
    
- **The Geometry:** A drone at 50m is physically _above_ the main beam. It relies on **Upper Sidelobes**, which are intentionally suppressed by manufacturers (usually 18–20 dB lower than the main lobe) to avoid interference with other cells.
    
- **The "Cliff" Effect:** As the drone descends for an emergency landing, it crosses the boundaries between these lobes. Because the antenna's radiation pattern is highly directive, the transition from a "Side Lobe" to a "Null" is spatially very sharp. A move of just **10–20 cm** can result in a **15–25 dB drop** in signal power.
    

### The CSI Failure:

Standard CSI feedback loops (e.g., every 5ms or 10ms) are too slow to track this "cliff." By the time the BS receives the CSI and adjusts the beam, the drone has already entered a null. This leads to:

1. **CSI Aging:** The channel state is "stale" the moment it’s calculated.
    
2. **Burst Packet Loss:** The C2 link drops for several milliseconds—violating URLLC’s strict 1ms latency and 99.999% reliability requirements.
    

---

## 2. Simulation Scenario: European Urban POV

To align with the LAWN call, your simulation needs a realistic 3D environment. Let’s design a scenario based on a **German "Business District"** (e.g., Frankfurt's _Europaviertel_).

### A. The Environment (The "Scene")

- **Building Architecture:** A mix of "Old Town" stone buildings (20m) and modern glass-facade skyscrapers (60m+). Glass is critical because it creates strong **specular reflections** (multipath) which Sionna handles perfectly.
    
- **BS Placement:** A Macro-BS on a 25m rooftop.
    
- **RIS Placement:** A ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAD4AAAAXCAYAAABTYvy6AAACv0lEQVR4AeyWWchNURiGNzJnChcokogLpQwlLoRkSGYyJMOdKMWNlCklQ0JuKJLcUURxIcqVXEgZcqEUSpkjRebn+Tur9jnO3vsM26/Of07vs761vnX2Xt+317B3+6iN/pqJt7WJL53x8TyA83ATroFtTKL20HMG/oeMreZY44kvIforcAimwnW4CB2gnIbi3AJJ/XT9M9Uda0h8ACGegiNwB5Q3H0RlIJTTYZxdoLWVS6wh8c1E3wPOQpDLeBeNF1CqGThewldobeUSa0h8PtG/BZPBtMg9vrulVly4tPX7UIp70lsL6W4HSZpNR0fIUi6xmnhvRhoBr2AF3ILbsA3KBbIe/wV4A9XILeMqKneNZ8U8On5AmnKL1cT7Fkbqh50E02AmOEMnsXH1pGHix7DV6jgXdId1EJcH6RQcG+A3pCm3WE28a2Gk/tgd4FP/iD0Ha2AMBG2nsg++Qy3aykXTYSWoiRSuLNs/qWcpt1hN/H1htGfYdxDknre+1AKGwGi4BLXqFxeuhrmwE/aC9/+ErUS5xWriIcHXJSM787p6WcBBcMYwdcn7nuAOG+EyfIBKlVusJv6NUe9BZ4grHGwue/1zKB6B+zDQjfYqsF26d3GX1WS8B2AUTAAPVExFyi1WE3dEP/2GUQnJUo087LQ3LMCDyddRwDMBd+RZoO+0jQzc034oLeN/zp7Lfhb1apLPJdaQuF9szwnAw8skfG144HgS+91O11/qVPD4Xi9UU804ev2uX4R9CsoDbS0VH4RQzVQusYbEvzDcAhgOj+E+OJObsC5jTJF8j7vsdS6nuAt+gGAStT+KosX0PoS43PM+ZMcK50m8v7SeS6whcW/+hMIARmIHw1FIkgn0odPVIWOpX4U0+X3wIOEPn/G798N5QjNVdccaTzx1pEbrbCbeaDOalU9zxrOeUKP1/wEAAP//aNco+gAAAAZJREFUAwDrmKwv7X+KowAAAABJRU5ErkJggg==) element RIS (approx. ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACIAAAAXCAYAAABu8J3cAAACIUlEQVR4AeyVO2tUQRSA1we+LQRBEBHEQgQVxEZtFFGxUhtbLUQFERER/AsKPvCBj8LCSknSJKQICXk1IYSEJBBIkz6BNIGEFHl/32Vn2OzubLbILimynG/OmTNnzpw7O3fuztwW+dWzkHM88z8Yg59wGKLUs5BvrPoaLsIx+A5RyhWyg9FTsJlygGTn4RIsQjM8hLh+NHAeh/vQDp9gM2WeZEehFZSTNBOwApmEQl7Sa4ObcA1qKftI/hjeQZRQyFc8F+AFuHWomoln5TPZ/0CUUEh01Nh4Sn7/+i/oGxCl2kJ2MWMQ3K1J9BF4Dy3QDSY9iPZpXagP+y0UyhU6Z2EarsMDiFJtIavMeAOd4IK/0W7vXfQANEED/IXb8BE8A2fQindGI8YrsHBZ92ZWW4inu4ck42BSz9QUtjJE4w71ot01VK7fBu6BMktzArwaAnfoR0kVYnAMKjAsyO6ITZ7lvB7Oa1Xw+Zfa35BUIamJYYGlMgGhyMKh1AMVxmR2qpBUAs9KNrHKJpW/ZHoqMFXI7pIMlR2pPCWzigvZS4Q+34xySTyohOSC1j5kA85BZVLOlw2kGhd1zHvAkz5DxyvYvt+CDvom3YP2bniCVkZpHoGv8S+08p/mAzwHc6Fy3iVdGhsRCjH4MsH7wZ2Q09i3YA4W4CroFz+Q3hnP8IU5fmG9a37g8wNnnPhQuCpLKKRyVB1Gtwsp3uTtHSnekTUAAAD//xRDspUAAAAGSURBVAMAHMNML8hZlgAAAAAASUVORK5CYII=)) mounted on the landing building's facade at 40m height.
    

### B. The Emergency Landing Path

The drone is flying at **50m (cruise)** when it receives an "Airspace Closure" command. It must land on a **35m rooftop** of a nearby building.

1. **Phase 1 (The Sidelobe Zone):** At 50m, the drone is in the Far-Field, served by the 2nd upper sidelobe of the BS. SINR is low but stable.
    
2. **Phase 2 (The Descent/The Cliff):** As it drops from 50m to 40m, it hits the **Sidelobe Cliff**. The direct link from the BS enters a deep null.
    
3. **Phase 3 (RIS Intervention):** The RIS (which has a clear Line-of-Sight to the BS) reflects the main beam upward, "filling" the null.
    
4. **Phase 4 (Near-Field Transition):** As the drone gets within 5–10m of the RIS-equipped building to land, the wave model must switch from **Far-Field (Plane)** to **Near-Field (Spherical)**.
    

### C. Simulation Parameters for Sionna

|**Parameter**|**Value**|**Reason**|
|---|---|---|
|**Frequency**|3.5 GHz (n78)|Standard 5G Mid-band in Europe.|
|**Bandwidth**|100 MHz|High-fidelity CSI estimation.|
|**BS Downtilt**|![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA8AAAAUCAYAAABSx2cSAAABc0lEQVR4AcyTTSuEURiGT4RZsLBRsvAPlGwUWVEWlFBWPjaKDYVIFlYWNj4XFpSSElYiP4CQBdlq8pXssJhpppnVzHVPPXWambOazUz3dZ6P99wz533edypcCZ/yMLdyB6dwBWcwA5UQlB27kR1bsAx9MALdsAmmapJZWIN5iJh5mkK/+E6UMizaMEWsBWmD5RlW4AF2zdxM0Qa+/imqoAYkfeGtEriHhJk/KXTUc2IEpAmWC/gDKanFI23mY5q6OEx8hEUYAh2bkJN+oCOXOddOjJo5StEPMWiBddDRfommPZIUaGiKB2am53pZNPEjoqSB7SvxeCLfhhdwZtYEG2iswjh0whvovnUi0kLJXE97CXbAdEfSA3HQ/REKJXMT7Tp4BV8fFJp28C2T+YtNGkAXMV/64pv8ptUy62hzNA5hDNTTW7VA/gPXUFTaqAt6DJMkg6BHdEL8hlEIyszacMkyABqQJqx/GGVYvjm8K3ClJHMWAAD//3OsyRcAAAAGSURBVAMAsV5CKfVz9MAAAAAASUVORK5CYII=)|Typical European urban deployment.|
|**UAV Speed**|5 m/s (Vertical)|Standard landing speed for a quadcopter.|
|**C2 Payload**|256 bits|Standard control command size.|
|**Target Latency**|< 1ms|URLLC Requirement.|

---

## 3. What to Deliver in the Paper

### The "Logical Link" Results (Your Part):

- **Outage Probability:** Show that without RIS, the "Sidelobe Cliff" causes an outage (![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADgAAAAXCAYAAABefIz9AAADvUlEQVR4AeyXachOaRjHzzvTbM00e9NMzdo0NU2TrWwhUXwg+WDJUrKHxAch2YXIkiWEhCwhkg+SnewfLFHIUrYPkr3sWX6/x7kf5znP8+B9va8tb//ffV33fe5znnOde7vej6L3/O9DgG/JAP/Ce8yC6fAfFNMQLvwLWb2uEfydX/wYCulnGufBVtgH3SCpr6hsh1UwBTZAf7AdE/nchjgroRoch6wqMsBP+ZWqMAIOgD4mRz9S84X3YxtASxgA3oPJqA3lLdgEp2Eu/ACTYQnshu5QC/pAjioyQF9mDL9WB3whTJ4GxS0zY3seOwl6wyegqlNchqCDOFfAoNpja8IOGAsXIEchwKa02qk+trz0Gw9qAhuhmFpw4RgkdYKKH8QRwY0eUJRAkP7DUMH+A23BNYrJVQhwLc1DwamxEPsnVLRce3/wI9chqRtxJXzsw9S/hyCn+tG4YrCz8XvCY8hTCNAL2yhcB+uxy2AC+CUxFaJf46c6QrGbMfczZRT9HdsV2K+hLvwEjSDMii74u+AIFFQywNBhKY7TYw3WICdiw8vglpu+LPKkMP3CGnSEW9F3GEyDdmAfP34nfNc5prAKBRh67sTpDO5UU7GLoBKUl8JIpZ8XpppBhGtuLI2puKOexapRFIPhLqgeFA6KOzHuUz0vwKc9osiHuxmMpsE1uhr7OZRWrpfkPVfjSrrdc81L4bp+mho0OMIuK9zId6uC44i6YbrUqEbRywRox+8ovNl14AK/R/1V5VbvM9If6wsboViABuboDaSP+oaiL7g5es9w/Gyy8KIA/TGzBrOMa9xoGuS0CNOIppdWSaqnZ9tJ2r6FpDz8rXv4a9P0o2E++D6YqDKFWY1rFTc6R2HmhImiYgH6ldx699LLtVAbOx78QpgyqaTAXe6Q/9OevGb9Im1hp8TN6i88p+dybFBYy8lnhLa8AD/jrq6wBzx76mFNie5gy6owBf3K6We4dhzJ5vEFZ4zTy1mTPj7sYpbjdNQPeE4+ouIywkSerZd0JDmC7piHaPSsMXl1+71JvaxawI1nYCSodRQmzb2wQe6Azag49e3vbu3aWkxbWq1pcFMxncPN6jae97mLOooeJ3NoyygE6K5jauVUNKd7lcAyD6boCGZE/qiYfJudhLyTyxk57cfh2d/80l2aao48M807Z+S0Pqv4UcyATtG0GbZARiFANxG/dFiomYt5xZtr8L+JDvy8+wEmT05nE3SzHxOVbIcQYLbhLXYcoVK/3rsUYKmD84YPAfoV3mWeAAAA//85c7v5AAAABklEQVQDAPUjny9g2d7OAAAAAElFTkSuQmCC) packet loss) for 2 seconds during descent. With RIS, the link remains at ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACYAAAAXCAYAAABnGz2mAAACRElEQVR4AeyWu0sdQRTGbxLIm0AgJJAEQkiTIgmkS7RQfBSChf+AWtiIiChqKQgqCOIDOwsLsVIb0UJRsLAQrbSw8NWJjeBbxLf+vuvMcnfvrrq6qIXy/eacM7Mze3Zm7oxPY/f3l8+r/4NvDr6VPHwXKuUlE3AC3fASHN1nYgtkkQZfQbO3j3Xkl9gTWr9DkDTIEI362l7sN7iJtug0DiuQpMTEPtOaByPQAn4qobISCiEFZmEKPkJYvaNDFWgZB7G+S1lGwzBkgaYXk6RP1DRDA6yCVE9xBEoUE0rTPN0KWoFn2ApwZGesnZo/oA2pF+EmKZcafdU81uoUR3Em1kofWUPgRzn1VkpKG1/xHIVWAHMhm9hFdHn51zRvGGvNNk4qKGlMTB9Zh+NHG/WSktDmf60AnsMBOAqT2BfTyzujh9S/BduOe6X2eGIRZNU3Hb8PHIVJ7I3Ty+3Y5dBXu1uCoxmaBqAIlFATtgcchUlMM+N0THDOjH9s7HVNBw92Qg50gUtBiekscz1IYPeWt02/KJpj6yqiIigxv/HXTKXd5CaMvTKOTdyEtzNBiXlnRW/RuSP7XkUCH/B1C+jowI1GYRLTZt3htb/AShv+J4GuJkx08ib2gqFVp1+gd9a0VAW0F4PdVzrxl4m1kTHRSUlotAyKSdgE7SHFS/ijoHMGE1c/ZS00gu6431id+q7/DKi7tWxiY4z0D7SRNVPiB3E27EKidMlXU6E7TtdPpL9Gxo3LJhYPHlLxmFjY1XicsbAzdg4AAP//2Zo2uAAAAAZJREFUAwB4klgvP81lhgAAAABJRU5ErkJggg==) PER.
    
- **Near-Field vs. Far-Field Gap:** Plot the SINR error if you _ignore_ near-field effects. Show that assuming plane waves when the drone is 3m from the RIS building causes a **6dB focusing error**, which kills the URLLC link.
    

### The "RF" Results (Colleague's Part):

- **Beam Heatmaps:** 3D renders from Sionna showing the "focused spot" the RIS creates at the landing pad.
    
- **Angular Power Spectrum:** Showing how the multipath from German stone/glass buildings adds "noise" that the RIS must suppress.
    

**Would you like me to draft the specific "Introduction" text that bridges this German urban scenario to the safety-critical requirements of the LAWN Call for Papers?**

Implementing the simulation in **Sionna** involves creating a pipeline that moves from the electromagnetic physics (Ray Tracing) to information theory (Finite Blocklength).

Since you are targeting the **LAWN** paper in three weeks, you should focus on a **Deterministic Ray Tracing** approach rather than a stochastic one. This proves the "site-specific" nature of your emergency landing scenario.

---

## The Simulation Pipeline: CSI ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAdCAYAAACwuqxLAAAAyElEQVR4AeyRsQkCQRBFRbAAwR60BnNzTUXQTDAxEjGyCXM1MbACQauwAUPBFkzuLexme/u5gctG/vPg/sx8+NfttPzzAFmwV9RaRVN5OQ5Yv8GK/T5IWQNOXF6DlDXgxeUBjKEoa0A4uudvCwfoQVYp4Ir7bMiD+SHsYAFZpYAl7qQhc+Y/MIIzZJUCsmbhZdi74G/gB7UKg7VmwZjh3eALRVkDQuf34uVoWgOO7P9ByhrwlpfjgDUgruuHB8iOvCKvSDYgByoAAAD//zF7xecAAAAGSURBVAMAPPEcO+/lgekAAAAASUVORK5CYII=) SINR ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAdCAYAAACwuqxLAAAAyElEQVR4AeyRsQkCQRBFRbAAwR60BnNzTUXQTDAxEjGyCXM1MbACQauwAUPBFkzuLexme/u5gctG/vPg/sx8+NfttPzzAFmwV9RaRVN5OQ5Yv8GK/T5IWQNOXF6DlDXgxeUBjKEoa0A4uudvCwfoQVYp4Ir7bMiD+SHsYAFZpYAl7qQhc+Y/MIIzZJUCsmbhZdi74G/gB7UKg7VmwZjh3eALRVkDQuf34uVoWgOO7P9ByhrwlpfjgDUgruuHB8iOvCKvSDYgByoAAAD//zF7xecAAAAGSURBVAMAPPEcO+/lgekAAAAASUVORK5CYII=) PER

### Step 1: Generate the Channel (Sionna RT)

Use Sionna’s `Raytracer` to get the Channel Impulse Response (CIR). At 50m, ensure your Base Station (BS) uses a realistic antenna pattern with downward tilt to capture the **Sidelobe Cliff**.

Python

```
import sionna
from sionna.rt import load_scene, Transmitter, Receiver, PlanarArray

# 1. Load your European Urban Scene (e.g., from Mitsuba/Blender)
scene = load_scene("urban_canyon.xml") 

# 2. Configure Antennas (Add downtilt to BS)
scene.tx_array = PlanarArray(num_rows=8, num_cols=8, vertical_spacing=0.5, horizontal_spacing=0.5)
scene.add_transmitter(Transmitter(name="BS", position=[0, 0, 25], orientation=[0, 0.14, 0])) # 8 degree downtilt

# 3. Compute Paths (CIR)
paths = scene.compute_paths(max_depth=5) 
a, tau = paths.cir() # a: complex gains, tau: delays
```

### Step 2: RIS Integration (The "Bridge")

Sionna doesn't have a "native" RIS object that handles near-field focusing out of the box. You must model the RIS as a **Secondary Transmitter** that re-radiates the signal it receives from the BS, modified by your phase-shift matrix ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAYCAYAAADzoH0MAAABSklEQVR4AeyTq0tEQRTGxxeYbKJNsVj8CwyCYjMoWDQoNrX6ApOKFjGLSYsIBoPBYFJRULBoMGkx+EqWbbsLu7/vMmd278A+YOsu3++ec+ZcPmbO7G11Df6aBs7FM+hlpoUq3NBLKTb4pzvqOSOalkm0vkpMKTbI0r3zfBNNryRafyGmFBv00F2AQ5gG0z7JHkxABwSZQTsrR/AJu/AAz2C6JumGK/iAOUhkButUS9AJW3AOX2C6JVmEe+iDYxiCcAsjKjw/Puo2fBrCu890jGHltgM5qxYDekALxOr3CzniI4QdHFCcgrTGYxLawNRFsgnjkAEd940YDPIU8zAGlzALU2DSXAYptkHxhJjIjpAUPDSsFeIMXIBJfyBd7w4LvxAUG4RGvUlsUP4tbJSZPJHrVmp+C3+8qOlXQjPilZLiHZQ6dWZNA+eKAAAA//93eOMyAAAABklEQVQDAN/wOjEJ5m8yAAAAAElFTkSuQmCC).

- **Logic:** ![](data:image/png;base64,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)
    
- **Near-Field vs. Far-Field:** In the Near-Field, your ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAYCAYAAADzoH0MAAABSklEQVR4AeyTq0tEQRTGxxeYbKJNsVj8CwyCYjMoWDQoNrX6ApOKFjGLSYsIBoPBYFJRULBoMGkx+EqWbbsLu7/vMmd278A+YOsu3++ec+ZcPmbO7G11Df6aBs7FM+hlpoUq3NBLKTb4pzvqOSOalkm0vkpMKTbI0r3zfBNNryRafyGmFBv00F2AQ5gG0z7JHkxABwSZQTsrR/AJu/AAz2C6JumGK/iAOUhkButUS9AJW3AOX2C6JVmEe+iDYxiCcAsjKjw/Puo2fBrCu890jGHltgM5qxYDekALxOr3CzniI4QdHFCcgrTGYxLawNRFsgnjkAEd940YDPIU8zAGlzALU2DSXAYptkHxhJjIjpAUPDSsFeIMXIBJfyBd7w4LvxAUG4RGvUlsUP4tbJSZPJHrVmp+C3+8qOlXQjPilZLiHZQ6dWZNA+eKAAAA//93eOMyAAAABklEQVQDAN/wOjEJ5m8yAAAAAElFTkSuQmCC) must account for the **spherical curvature**. Instead of a linear phase gradient, calculate the phase for each element ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAwAAAAYCAYAAADOMhxqAAAA40lEQVR4AezQLw9BURjH8TteAE1QTNJMkggKs6Ewf4oqqZqq2ERFYzZ/mo0xEzDBG1C8Cxoz3+funrMbjyIYez73+Z27++wcx2N9+PsPmFzY926pyXEumMGPFiY4ow8f7JIjRUhh5FDEEQeUUUADVdglAzXSGFFIdXicIPWUh5sMtHkhWyfpd0yhKuuErdMtGVA5QdjhAVUVghzxSrdLDQRYxbCBqhAhgyG8GEHvkJIF1lAVd8KKXsceeiDIYgG9NXmJOQaQa5WuB7q8zMNdNxYlpNHDC3pAshH1p40+lo9+YeANAAD//5A0U0AAAAAGSURBVAMAVwciMRObDOoAAAAASUVORK5CYII=) based on the exact distance to the drone: ![](data:image/png;base64,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).
    

### Step 3: Calculate SINR

To get the SINR, you must scale the path gains by the transmit power and add the noise floor.

![](data:image/png;base64,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)

Python

```
# Scale the channel gain to Received Power
P_tx_dbm = 30 
P_tx = 10**((P_tx_dbm - 30) / 10)
noise_floor = -174 + 10*np.log10(bandwidth) + noise_figure

# Effective channel H after beamforming/RIS optimization
h_eff = np.sum(a * np.exp(-1j * 2 * np.pi * frequency * tau), axis=-1)
snr = (P_tx * np.abs(h_eff)**2) / (10**(noise_floor/10))
```

### Step 4: Map SINR to PER (URLLC Logic)

This is the most critical part for your **Logical Link** role. Standard 5G uses BLER tables, but for a high-impact paper, use the **Polyanskiy Approximation** for Finite Blocklength (FBL). This accounts for the fact that short C2 packets (e.g., 256 bits) cannot achieve Shannon capacity.

Python

```
import tensorflow as tf
from scipy.special import erfc

def calculate_per(snr, k_bits, n_blocklength):
    """
    snr: Linear SINR
    k_bits: Information bits (e.g., 256)
    n_blocklength: Channel uses (Latency * Bandwidth)
    """
    C = np.log2(1 + snr)  # Capacity
    V = (1 - (1 + snr)**-2) * (np.log2(np.e)**2)  # Dispersion
    
    # Q-function argument
    arg = (n_blocklength * C - k_bits) / np.sqrt(n_blocklength * V)
    per = 0.5 * erfc(arg / np.sqrt(2)) # Q(x) = 0.5 * erfc(x/sqrt(2))
    return per
```

---

## How to use this for your Paper

1. **The "Cliff" Plot:** Run the simulation as the drone descends. Plot **SINR vs Altitude**. You will see the SINR drop sharply as the drone hits the antenna null.
    
2. **The RIS Benefit:** Show that without RIS, the `calculate_per` function returns ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABkAAAAXCAYAAAD+4+QTAAABm0lEQVR4AeyUvStFYRzHH295L4NSTJKFMshA3sVksdpsUshusBhMBv4HFmzkLWGSUmxIMRuQDPISn+/T89xOh5tznNxB9/b9PL+X85znd3+/e8/JNRn4/O8iOUywFuKojc1rcAD70AUpBcdVTXYItmEeoqqVjSswB90wC1vQB1a+yCTRJvSDNmIia5Gdq3AM0i6LuprCWvkiC0RNMA6vEFX1bGyBSwhKcQ+JfDC+iPzf0OxuenDWm0eccmiHxEVqdAiEu38hJ9VpSdpJiQ75hneXK5BNWiTcgc4UH1rgDdKOS8+Krv/EndsQ3p/n8veySTvxRYp0WIBi59vr6YqEv5m754s5cZkKZ72pxHmGU4g9rk5uGgavG5xDaISgFK+TsH/tcCeFXFCuFBvuRvEG+SXwzweuGTHG6BWi1xKuaWDpgGmw0oFytOkIR5U1X8VXxDtQBpL+MWr/lkAdYKyuWQdhFJZhAnrhAqx8kT0ivej0g+kbCz1IA+SfwEvjqiKwPyjW6xxnBjTKMewZpOSLpBJ/4WSLxJpqRsb1CQAA//9vtt2WAAAABklEQVQDAL6gOi8cz+yHAAAAAElFTkSuQmCC) (total outage) during the cliff. With RIS, it stays below ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACYAAAAXCAYAAABnGz2mAAACRElEQVR4AeyWu0sdQRTGbxLIm0AgJJAEQkiTIgmkS7RQfBSChf+AWtiIiChqKQgqCOIDOwsLsVIb0UJRsLAQrbSw8NWJjeBbxLf+vuvMcnfvrrq6qIXy/eacM7Mze3Zm7oxPY/f3l8+r/4NvDr6VPHwXKuUlE3AC3fASHN1nYgtkkQZfQbO3j3Xkl9gTWr9DkDTIEI362l7sN7iJtug0DiuQpMTEPtOaByPQAn4qobISCiEFZmEKPkJYvaNDFWgZB7G+S1lGwzBkgaYXk6RP1DRDA6yCVE9xBEoUE0rTPN0KWoFn2ApwZGesnZo/oA2pF+EmKZcafdU81uoUR3Em1kofWUPgRzn1VkpKG1/xHIVWAHMhm9hFdHn51zRvGGvNNk4qKGlMTB9Zh+NHG/WSktDmf60AnsMBOAqT2BfTyzujh9S/BduOe6X2eGIRZNU3Hb8PHIVJ7I3Ty+3Y5dBXu1uCoxmaBqAIlFATtgcchUlMM+N0THDOjH9s7HVNBw92Qg50gUtBiekscz1IYPeWt02/KJpj6yqiIigxv/HXTKXd5CaMvTKOTdyEtzNBiXlnRW/RuSP7XkUCH/B1C+jowI1GYRLTZt3htb/AShv+J4GuJkx08ib2gqFVp1+gd9a0VAW0F4PdVzrxl4m1kTHRSUlotAyKSdgE7SHFS/ijoHMGE1c/ZS00gu6431id+q7/DKi7tWxiY4z0D7SRNVPiB3E27EKidMlXU6E7TtdPpL9Gxo3LJhYPHlLxmFjY1XicsbAzdg4AAP//2Zo2uAAAAAZJREFUAwB4klgvP81lhgAAAABJRU5ErkJggg==).
    
3. **Transition Study:** Run a comparison where you use the **Far-Field** formula even when the drone is near the RIS. Show that the **PER increases** significantly because the beam isn't properly focused (spherical wave mismatch).
    

### 3-Week Project Management

- **Week 1:** Your colleague gets the **SINR traces** from Sionna for the landing path (with and without RIS).
    
- **Week 2:** You process these traces through the `calculate_per` function to generate **Reliability vs. Latency** curves.
    
- **Week 3:** Draft the paper. Focus the "System Model" on the transition from **Sidelobe-dominated Far-Field** to **RIS-dominated Near-Field**.
    

**Would you like me to provide the LaTeX format for the Finite Blocklength (PER) equations to include in your Section III?**

---
### Visualizing the 10 MHz Slice in an Urban Canyon

---

### The "Loop" for your 14-page Paper:

Since you are the "Logical Link" person, your results should show **Spectral Efficiency**.
1. **Plot PER vs. Bandwidth:** Show that increasing from 1 MHz to 10 MHz drastically improves reliability (due to diversity).
    
2. **Plot PER vs. Bandwidth (beyond 10 MHz):** Show that increasing from 10 MHz to 50 MHz provides **diminishing returns** for a small C2 packet.
    

- _This "Saturation Curve" is a great graph to include to prove 10 MHz is the optimal choice._


----


- RF - LOS

- Fresnel Region - First 3 wichtig

- V-polarized wave in 1st Fresnel region

- Same phase of LOS wave and reflected wave → total stronger signal

- Second Fresnel region - opp phase - Weak signal

- V-polarized antenna systems - odd zones stronger signal and weak signals from even zones

- Horizontally polarized antenna system - vice versa

- Position and phase of antenna is important

- RF signal reflect from all kinds of surfaces - lakes, buildings

- Longer the distance - bigger the frensel zone - more reflective elements

- Beamwidth (not coverage) angular width of main lobe -6/-3 db below the antenna gain

- PTP links

- Coverage prediction (Antenna pattern, Gain, Radio Output power)

- Coverage calc incude Geography, map accuracy, down tilt, Tower height

- pseudo color for RF visualization

- Noise floor, Channel width - Plot MCS ISO Surfaces

- MIMO - for deducing fading effects, throughput capacity and coverage, reliability of wireless link

- Rate gain - improve resistance to noise , better coverage , multiple path - successful data transfer

- multiple data streams in same frequency channel - more capacity

- 2 distinct channel links via 2 different polarization (double capacity)

- MU-MIMO - pre and post processing happens at Access point - nothing to do with CPE (Customer premises equipment). Therefore multiple independent CPE

- System requirements - Channel state information (Sounding) - test data and response,

- Client side synchronization (delay) - each signal for each CPE mainlobe

- Array resolution (limit # CPE) - group CPE scheme - which antenna array serve at same time

- MU-MIMO Data transfer CPE served at same time at same frequency

- knowledge of signal Prorogation characteristics

- QAM modulation - encode information into an RF wave

- RF wave 3 main properties that is used to encode infos

- Amplitude, Frequency, Phase

- QAM - uses amplitude and phase

- Data 0s, 1s (symbols) QAM modulator - RF carrier

- Length of the signal - Depth of the QAM modulator

01 - QPSK
0001 - 16 QAM
001011 - 64 QAM

- Symbols → constellation diagram

- Noise based, fluctuation of bit point error

- less symbol distance - less noise tolerance

- High MCS rate needs higher SNR levels

- MCS rate (802.11 std) - QAM modulation, No of spatial channels, coding rate

- Antenna - parameters - front to back (mainlobe) ratio

- Sidelobe level

- Beam efficiency - main lobe energy/total energy

- beam efficiency - side lobe measures

- beam efficiency - over whole antenna - freq specturm with both polarization

![[RF1 1.png]]  

![[RF2.png]]

### RIS
![[ICNS_2025___RIS.pdf]] 


![[CNS summary for Abstract.pdf]]

To do read the followin 8/5
 - resource orchestration for positioning, navigation, and timing systems 
 - https://scholar.google.com.vn/citations?user=-c8vaNEAAAAJ&hl=vi
 - https://dl.acm.org/doi/10.1145/3614454.3623001

---
8/9 
Meeting - presentation by Roshan 
mm-Wave communication for AAM 
- Controllable communication environment 
- energy conserved 
- companies have initial versions of RIS 
- Low hardware, cost
- Active and passive elements 
- passive materials are like mirrors 
- dynamic operation active
- Model EM behavior for active materials for drone operations 
- multi field factors, far field metrics 
- electro magnetic  - micro meter - Heat - meter scale 
- diffraction gratings work similar to active meta materials 
- field - u0, ud - angle of incidence and reflection (known and unknown field )
- all the effects of diffraction grating 
- waves come from different angle - and compressed - shift in wavelength (as example)
- homogenization - 
- thermo electro magnetic coupling 
- effects from thermal 
- passive implementations 
- radar cross-section of aeroplanes 

--
vahana
depriciation - years? 
indirect costs - opex 
slide 9 - monetory costs 
control station ?!?!?

---
Geometric optic tools ray tracing 
any EM waves interaction create Near field and far field
LAWN - far field 
RIS is complicated - always calculate near field before calculate far field 

far field model  - assumes less complexity 

Required signal quality in geographical 
near field to computation heavy
Traditional RIS - antenna and relay devices - electroactive and polymer active materials (used in space application)
computational mechanics to communication 

---



T2 Presentation 13/4

- controllable communication channel 
- Physics based  less and more stochastic 
- large surface area 
- warping 
- Macro Thermo mechnical to micro electro magnetic to macro electromagnetic 
- Theromal boundary conditions - not flux conditions 
- 