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