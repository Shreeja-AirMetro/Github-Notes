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
- Ref: https://techlibrary.doodlelabs.com/mini-oem-mesh-rider-radio-24002482-mhz-wi-fi-band 
- mesh rider radios
- Pin Connections  - https://techlibrary.doodlelabs.com/minioem-mesh-rider-radio-connector-descriptions-2023-update
-|Ports 1/2/3/5/6|Data Connectors|JST|SM4B-GHS-TB|
|Port 4|Power Connector|JST|SM6B-GHS-TB|
|ANT 0/1|MMCX Female Antenna Connectors|Molex|