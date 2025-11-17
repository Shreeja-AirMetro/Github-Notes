**==This page is for Mesh device setup==** 
- UAV mesh node setup 
- Initial idea 
- Pixhawk -- MAV forwarding --- Rasp pi --- Mesh node ........ mesh --- Laptop --- QGC

To do: 
- [ ] Rasp pi - Ubuntu 
- [x] Pixhawk setup -check - using 6C 
- [ ] Pixhawk - Rasp  - MAVlink forwarding (Mav router)
- [ ] Rasp pi Mesh node 
- [ ] Use rasp pi - Mesh note - network configuration to send mavlink packets 


---

Meshmerize Devices 
The devices are used for establishing wifi based comm - C2 communication between UAV (PiXhawk) and GCS

### Notes 

- We have MINI-OEM RM-2450-12M3 ([2023 Update](https://techlibrary.doodlelabs.com/mini-oem-mesh-rider-radio-24002482-mhz-wi-fi-band#Update))
- Frequency range: 2400 – 2482 MHz 
- Data rates up to 87 Mbps 
- 1.6 Watts Transmit Power
- Low power consumption
- MANET radio performance for today’s advanced UAV platforms, the RM 2450-12M3 unites
command & control, telemetry, and video transport in one ultra compact OEM module.
- Ref: https://techlibrary.doodlelabs.com/mini-oem-mesh-rider-radio-24002482-mhz-wi-fi-band 
- Ref: https://doodlelabs.filecloudonline.com/ui/core/index.html?mode=single&path=/SHARED/%2128Nh0Ga6zDeIsEryj68zFoLHlcLbb/chPLqt08InqjdYdi#/
- mesh rider radios
- Pin Connections  - https://techlibrary.doodlelabs.com/minioem-mesh-rider-radio-connector-descriptions-2023-update
- Ports 1/2/3/5/6- Data Connectors - JST
- Port 4 - Power Connector- JST
- ANT 0/1 -MMCX Female Antenna Connectors - Molex
- ![[mini-OEM Mesh Rider Radio - 2400~2482 MHz (Wi-Fi band).pdf]]![[RM-2450-12M3.pdf]]
- Key data 
- 2 freq bands available 2450 Mhz and 2455 Mhz
- The Mesh Rider Radio has been designed to be **plug and play**. Only **USB and a power supply** are required for integration.


https://learn.doodlelabs.com/throughput-estimation-tool  Throughput calculator

1. Operating Modes Mesh, WDS AP, WDS Client
Command & Control channel Ultra-Reliable Low Latency Channel (URLLC). Latency 1.5-10 ms
2. Video Channel Optimized video streaming with Unicast and Multicast transmission

3. Over the Air Data Encryption 128-bit AES (Full throughput)
256-bit AES (12 Mbps max throughput)

4. Advanced Band Filters Dedicated SAW filters for each band for high interference immunity
5. Minimum Sensitivity UDP Throughput -101 dbm @ 3 MHz | 87 mbps@20 MHz
6. Max RF Power at SMA port (Software control) Each radio individually calibrated 1.6W (32 dBm)
7. Channel Sizes (Software Selectable) 3, 5, 10, 20 MHz
8. Radio Data Rate Auto adapting Modulation Coding Scheme (MCS0-15)
9. Antenna Signal Strength -30 to -90 dBm (Recommended), Absolute Maximum= +12 dBm
10. RF Power Control In 1 db steps with ATPC(Automatic Transmit Power Control)
11. Integrated Antenna Port Protection Able to withstand open port, >10 KV (contact) and >15KV (open air discharge) as per IEC-61000-4-2
12. Wireless Error Correction FEC, ARQ
13. Mesh Router Self-Forming/Self-Healing, Peer to Peer
14. Custom Software Package Manager -Image Builder, OPKG, ipk
15. Radio Management Web GUI (HTTPs), SSH and JSON-RPC,Android/Linux/Windows App
16. Mesh tools - https://techlibrary.doodlelabs.com/product-index 
17. Antenna : https://doodlelabs.sharepoint.com/sites/Technical/Shared%20Documents/Forms/AllItems.aspx?id=%2Fsites%2FTechnical%2FShared%20Documents%2F2024%20%2D%2D%20Technical%20Library%2FDatasheets%2FCurrent%20Models%2FAntennas%2FOld%20%2D%2D%20Mini%2DOEM%20and%20Nano%2DOEM%2F2450%2FANT%2D2450%2D3%2DO%20Datasheet%2Epdf&parent=%2Fsites%2FTechnical%2FShared%20Documents%2F2024%20%2D%2D%20Technical%20Library%2FDatasheets%2FCurrent%20Models%2FAntennas%2FOld%20%2D%2D%20Mini%2DOEM%20and%20Nano%2DOEM%2F2450&p=true&ga=1 
18. ![[ANT-2450-3-O Datasheet.pdf]]


Through the links

Guide links : https://techlibrary.doodlelabs.com/mini-oem-mesh-rider-radio-24002482-mhz-wi-fi-band
Pin diagram: https://techlibrary.doodlelabs.com/minioem-mesh-rider-radio-connector-descriptions-2023-update 
Main spec details: https://doodlelabs.filecloudonline.com/ui/core/index.html?mode=single&path=/SHARED/%2128Nh0Ga6zDeIsEryj68zFoLHlcLbb/chPLqt08InqjdYdi#/ 
Mesh tool box : https://techlibrary.doodlelabs.com/mini-oem-mesh-rider-radio-24002482-mhz-wi-fi-band 

Hardware integration :https://techlibrary.doodlelabs.com/mini-oem-mesh-rider-radio-24002482-mhz-wi-fi-band 
Hardware interfaces: https://techlibrary.doodlelabs.com/mesh-rider-radio-hardware-interfaces 
Antenna Configuration: https://techlibrary.doodlelabs.com/can-i-do-x-distance  
RF Link : https://techlibrary.doodlelabs.com/optimizing-the-rf-link 
Networking Modules: https://techlibrary.doodlelabs.com/supported-networking-modes 
video guide : https://techlibrary.doodlelabs.com/self-service/gui-quick-walkthrough-guide-video 

Pin Configuration of Mini OEM and Eval kit 

### Component list 
mini-OEM Mesh Rider Radio

1. mini-OEM Mesh Rider Radio
2.  Side View -- 2x MMCX Connectors
3.  Cables
    A) MMCX-SMA cables
    B) LAN Ethernet cable
    C) USB-A to USB-C cable
4.  2x Antennas + 2x Attenuators 
5.  Eval Kit
    A) Evaluation test board
    B) Heatsink & thermal pad

![[Pasted image 20251117100139.png]] 


### What is doodle labs doing 

Doodle labs work with Wi-Fi on file level. The go beyond IEEE specification and how wireless done over long range 
They use their own on-board processor with wrts routing protocol  

---

What is RF and optimizing the RF link 

1. Include around 10-15 dB of fade margin to account for changing environmental and operating conditions

2. Use the highest gain antenna that your application allows, and if possible, separate the antennas by a half-wavelength in an orthogonal arrangement.

3. The objective is to operate the link with the highest SNR possible (the sweet spot for Mesh Rider Radio is around -40 dB to -70 dB RSSI).

Fundamental RF link laws 
```
RF Link Range=f(TX Power, RX Sensitivity and Channel Bandwidth, Operating Frequency and Antenna Gain, Path Loss, Noise and Interference)
```

TX Power 
- Higher RF transmit power makes signals go farther.
- In [radio transmission](https://en.wikipedia.org/wiki/Radio "Radio"), **transmitter power output** (**TPO**) is the actual amount of [power](https://en.wikipedia.org/wiki/Power_\(physics\) "Power (physics)") (in [watts](https://en.wikipedia.org/wiki/Watt "Watt")) of [radio frequency](https://en.wikipedia.org/wiki/Radio_frequency "Radio frequency") (RF) energy that a [transmitter](https://en.wikipedia.org/wiki/Transmitter "Transmitter") produces at its output.
- The difference becomes significant when you consider that your RF power is likely modulated. That means that your average power will be around 1W, but the instantaneous power will vary. In some modulation schemes, like AM, it's common to refer to the power of the carrier as the transmitter power, but what the antenna will actually see is the power of the carrier and sidebands. For antennas intended to be used with systems like this, the power rating might also refer to just the carrier power. For AM, the instantaneous transmit power (called peak envelope power) is roughly 3x the carrier power. The difference between carrier power, total transmitted power and instantaneous power greatly depends on the modulation scheme used
 - https://www.reddit.com/r/AskEngineers/comments/qgvx7m/communications_power_vs_rf_power/
 -  signals are transmitted and received clearly and efficiently, while minimizing interference from other devices. They work with antennas, transmitters, receivers, and other electronic components to ensure that wireless communication is reliable and strong.
The output power of the radio is not constant. It is controlled by four factors:

1. The user setting :This is the number that you control in the Network Configuration -> Wireless menu.

2. The MCS rate

a. All power amplifiers exhibit non-linear gain as they approach their output power limits.

b. This non-linearity distorts the RF signal and prevents the transmitter from operating at it's power limit when transmitting at high modulation rates.

c. There is usually a power backoff of 6-7 dB when transmitting at the highest modulation rate.

d. The actual backoff is detailed in your product's datasheet.

3. TPC (Transmit Power Control).

a. When the radios are close to one another, they will attempt to reduce their output power so that the received power stays below -30 dBm.

b. This can be disabled if desired.

4. The regulatory limit.

a. A power limit is applied based on the regulatory domain.