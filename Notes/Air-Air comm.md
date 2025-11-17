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
- 