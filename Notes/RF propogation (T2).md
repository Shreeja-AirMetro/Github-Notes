
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