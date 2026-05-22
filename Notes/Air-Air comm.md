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
 - specialized tools to measure signal strength, frequency, and quality, and then adjust equipment to improve performance.
 - 
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


---

To read 

- [x] https://techlibrary.doodlelabs.com/mesh-rider-radio-hardware-interfaces
- [x] https://techlibrary.doodlelabs.com/hardware-integration-guidelines
- [x] https://techlibrary.doodlelabs.com/mini-oem-and-helix-mesh-rider-radio-eval-kit-connector-descriptions
- [x] https://techlibrary.doodlelabs.com/optimizing-the-rf-link
- [x] https://techlibrary.doodlelabs.com/self-service/gui-quick-walkthrough-guide-video


---

2/12

- ETH1 is configured by default as a configuration interface which is not remotely accessible, but it can be re-configured if necessary. Please note that the -H variant of the Embedded Mesh Rider Radio is a legacy model. We recommend new designs to use the -J models. For the -H it comes with either a UART or a USB Host port.
- ETH0 and ETH1 are standard Ethernet interfaces and are bridged to the Mesh Rider Interface. USB Device Port The USB Device port is an Ethernet over USB interface and can be connected to USB host ports like those found on PCs, or USB OTG ports like those on Smart Devices. It is bridged to the Mesh Rider interface.
- Ethernet over a USB interface
- The default SSID is DoodleLabsWiFi and the password is DoodleSmartRadio. By default the WiFi Radio is in AP mode, but it can be configured as a client to connect to a standard Wi-Fi access point.
- UART interface. This interface can be bridged to the Mesh Rider network.
- Embedded/Wearable/OEM: Up to 1 Mbps baud rate, 3.3-V TTL.
- External: Up to 1 Mbps baud rate, RS232.
- mini/nano OEM: Up to 115200 baud rate, 3.3-V TTL.
![[Hardware Integration Guidelines.pdf]]![[mini-OEM and Helix Mesh Rider Radio – Eval Kit Connector Descriptions.pdf]]![[Optimizing the RF Link.pdf]]

```
RF Link Range=f(TX Power, RX Sensitivity and Channel Bandwidth, Operating Frequency and Antenna Gain, Path Loss, Noise and Interference)
```

 Having two antennas allows the radio to use either spatial-multiplexing to improve the data rate or spatial-diversity to improve the reliability of the link.

In spatial-diversity, the same stream of data is sent redundantly over both antennas and combined at the receiver in an intelligent way to optimize the link quality and SNR. Depending on the application, it may be beneficial to mount one antenna horizontally and the other vertically to get the most diversity in the polarization, or to mount both antennas horizontally (for example) to get the most power if the polarization is known.

In spatial-multiplexing, two different streams of data are sent to the two antennas resulting in double the throughput. In order not to interfere with each other in a line-of-sight (LoS) link, the antennas should be oppositely polarized and spaced a half-wavelength apart. In a non-LoS link, it is not necessary for the antennas to be oppositely polarized as the radios make use of multipath propagation to combine the data streams.

For mobile applications, where the orientation of the nodes constantly changes, it is beneficial to mount the antennas in a cross-polarized orientation to get the most diversity in the polarization.

> Doodle Labs recommends using two antennas. Mesh Rider Radios automatically switch between spatial-diversity to spatial-multiplexing modulations in order to optimize link quality.

// **Antenna part is difficult but worth another read** 

Lower frequency results in larger Fresnel zone and vice versa.
The MCS rate determines the link speed at which data is sent over the wireless medium. For the same 1500 byte packet, a low MCS rate such as MCS0 will result in better sensitivity (and hence longer range), and better immunity to continuous noise. However, a low MCS rate also results in a longer frame duration in the air, which makes the packet more susceptible to being corrupted by bursts of interference.

● MCS0-7 are spatial diversity rates with modulation rates between 1/2-coded BPSK and 5/6-coded 64-QAM. The same packet is transmitted redundantly over both antennas. The radios use a technique called cyclic-shift-diversity to prevent unintentional beamforming.  
● MCS8-15 are spatial multiplexing rates with the same modulation rates as MCS0-7. In this case, different packets are transmitted over each antenna allowing for double the link speed.

- Spatial diversity rates are more robust to changes in the RF path, while spatial multiplexing rates offer higher link-speed. The radio automatically selects the best MCS rate through an iterative trial and error process.

> For mobile applications with real-time streaming requirements, we recommend enabling "Diversity Rates Only".

● Intermittent high-level spikes of noise caused by a nearby transmitter.

● Mesh Rider radios use techniques including OFDM and spatial diversity allow them to operate in harsh RF environments.

There is a checkbox in the Traffic Prioritization settings labelled `Optimize for Latency over Throughput`. Enabling it results in improved latency, but the maximum achievable throughput is reduced by approximately half for high MCS rates.

Our overall recommendation is to design the RF link with about 10-15 dB fade margin to account for changes in the environmental and operational conditions. Changes in orientation of mobile nodes can affect the link margin. Use the highest gain antenna possible within the physical constraints of the system. The objective is to operate the link with the highest SNR (RSSI) possible (the sweet spot for Mesh Rider Radio is around -40 dBm to -70 dBm RSSI). A higher RSSI level will allow the link to operate at the highest modulation, and provide the best throughput, interference resistance and reliability.

https://techlibrary.doodlelabs.com/can-i-do-x-distance
![[Supported Networking Modes.pdf]]
Start by selecting a profile under Profile Selection, such as General, UAV/UGV/Robot, or Ground Control System (GCS). This will auto-fill recommended configuration values relevant to your application. You can then modify the basic settings based on your specific network design.

- - UAV Configuration appears only if the selected profile is UAV/UGV/Robot. It includes fields like GCS IP address, port number, and baud rate. The GCS Finder utility is enabled by default.
    
- - Active Frequency Band allows you to choose the frequency band used by the radio (e.g., 915v4 MHz).
    
- - Under Mesh Rider Radio Configuration, select the scenario (e.g., Mesh), Mesh ID, password, channel, bandwidth, operating distance, and number of devices. There's also an option to optimize for latency.
    
- - WiFi Radio Configuration enables configuration of SSID, password, and WiFi scenario (e.g., Access Point).
    
- - The Network Configuration section allows you to set additional static IPv4 addresses and netmask for BR-WAN interface if needed.
    

Once all necessary settings are applied, click Save Configuration to apply the changes.

---

### Evaluation kit 

An _evaluation kit_ for Doodle Labs Mesh Rider Evaluation Kit (used together with a Doodle Labs Mesh Rider radio) serves several important purposes. In short: it gives you all the extra hardware and interfaces you need to **test, prototype, integrate and configure** the radio — before committing to a final design. [techlibrary.doodlelabs.com+2techlibrary.doodlelabs.com+2](https://techlibrary.doodlelabs.com/quick-start-guide-ch1?utm_source=chatgpt.com)

Here are the main uses and benefits:

### ✅ What the evaluation kit provides

- It includes **antennas, cables, breakout boards and connectors** (power, USB, Ethernet, etc.) so you don’t have to design a custom PCB or wiring harness just to get started. [techlibrary.doodlelabs.com+1](https://techlibrary.doodlelabs.com/quick-start-guide-ch1?utm_source=chatgpt.com)
- For embedded-form radios, the kit provides an **evaluation test board** (or breakout / evaluation board), which lets you mount and power the radio module, connect interface ports, and test functionality on a bench. [techlibrary.doodlelabs.com+2techlibrary.doodlelabs.com+2](https://techlibrary.doodlelabs.com/quick-start-guide-ch1?utm_source=chatgpt.com)
- It often includes additional components like **heatsinks / thermal pads**, especially for smaller (“mini” / “nano”) modules, which helps with thermal management during testing. [techlibrary.doodlelabs.com+1](https://techlibrary.doodlelabs.com/quick-start-guide-ch1?utm_source=chatgpt.com)

### 🎯 Why these are useful

- **Faster prototyping & testing**: Instead of building custom hardware around the radio module, you can quickly put it on the evaluation board, hook up power, antenna, USB/ethernet and start testing networking, firmware, antenna performance, data throughput, latency, etc. — a big time-saver.
- **Integration validation**: If your end product will integrate the radio (e.g. in a UAV, robot, embedded system), the evaluation kit lets you test how the radio will behave in your system before committing to full-scale build or PCB design.
- **Configuration and software setup**: Because the evaluation kit gives you standard interfaces (USB, Ethernet, power, etc.), you can connect the radio to a host (PC / controller) and configure firmware, network settings, test mesh networking, encryption, data links, before deploying. [Doodle Labs+1](https://doodlelabs.com/mesh-rider-overview/?utm_source=chatgpt.com)
- **Thermal and mechanical test**: Using the included heatsink / thermal pad, you can test the radio under load to see how it handles heat — important for reliability in real-world deployment. [techlibrary.doodlelabs.com+1](https://techlibrary.doodlelabs.com/quick-start-guide-ch1?utm_source=chatgpt.com)

### 🛠 When you _should_ use an evaluation kit

- When you just got a Mesh Rider radio module and want to **verify basic functionality, test links, antennas, or mesh networking**.
- When you are **developing a custom system (robot, drone, embedded device)** and need to test how the radio behaves in that system before designing final electronics/PCBs.
- When you need to **evaluate performance characteristics** (range, throughput, latency, interference robustness) before committing to purchase or full integration.
- When you want to **experiment, prototype, or test new firmware / configuration** without risking a final, production-grade build.

---

First time Simple configuration mesh network 

**TRY PIXHAWK SETUP ON THURSDAY**

https://techlibrary.doodlelabs.com/integration-flight-controller

###  Summary of the mesh hardware and ideas of what to do

Summary of mesh hardware: 
1. The mesh radio comes as a AP (memory, wifi and storage) . Its multi banc in 2Ghz spectrum with MIMO antenna
2. we have evaluation kit for performance test 
3. MESH Mini OEM with 6 ports and 2 antenna 
	-  Port 4 is power 5V and 3A max 
	- Port 1 us USB  (Device)
	- Port 2 is Eth 1
	- Port 3 is UART Reset 
	- Port 5 USB (Host)
	- ==<span style="color:rgb(0, 176, 80)"> <span style="color:rgb(0, 0, 0)"><b>Note: A 5V barrel jack (5.5mm x 2.5mm with positive center) rated for 3A is required to power on the Mini/Nano OEM.</b> </span></span>
	- Static Ip is set? - check because Mesh software is installed
	- 
4. We will evaluate two setup A2A and A2G 

Setup 1

Setup 2

---
Welcome to working with Doodle Labs hardware! The **Doodle Labs Mini OEM (such as the RM-2450-12M3)** and its Evaluation (EVK) kit can seem a bit daunting because they use industrial-grade, defense-heritage Mobile Ad-hoc Network (MANET) technology rather than consumer Wi-Fi plug-and-play standards.

Here is a comprehensive, step-by-step implementation guide tailored for a beginner to get your kits physically connected, booted up, and configured for the first time.

### Step 1: Unbox and Identify Your Components

Your Doodle Labs Evaluation Kit typically contains two nodes (as you need at least two to build a mesh network). For each node, locate:

1. **The RM-2450-12M3 Mini OEM Radio Module** (the small metal-shielded board).
    
2. **The Ethernet Test Board / Evaluation Board (EVK)** (the carrier board that the radio snaps onto or is wired to).
    
3. **2x Antennas** (Matching 2.4 GHz frequency).
    
4. **2x MMCX-to-SMA or MMCX-to-RP-SMA RF cables** (pigtails).
    
5. **Power Cable / Wall Adapter** (usually a 2.5mm barrel jack power supply or a screw terminal block).
    
6. **Ethernet Data Cable (RJ45)**.
    

### Step 2: Physical Hardware Connection (Crucial Step)

- **CRITICAL WARNING:** **NEVER power on a radio without the antennas securely attached.** Powering on an RF amplifier without a load (antenna) will reflect the energy back into the chip and permanently fry your $1,400+ radio module.
    

1. **Attach the Antennas:** Take the small MMCX connectors on the pigtail cables and press them firmly onto the `ANT0` and `ANT1` tiny round gold ports on the radio module until they click. Screw the large rubber ducky antennas onto the other end of those cables.
    
2. **Mount the Radio:** If it isn't already, secure the Mini OEM radio to the Evaluation Board.
    
3. **Connect to Your PC:** Plug one end of an Ethernet cable into the RJ45 jack on the EVK board, and the other end directly into your computer's Ethernet port.
    
4. **Plug in the Power:** Insert the power supply into the EVK board's barrel jack (or terminal block), but **do not switch on the wall socket yet** until you read the networking step below.
    

### Step 3: Configure Your PC’s Static Network Settings

Doodle Labs radios do not have a built-in DHCP server running on their setup ports by default. They use a unique static IP tracking system based on their MAC addresses, falling into the `10.223.0.0/16` subnet.

To communicate with the radio, you must manually give your PC a static IP address in that exact range:

1. Look at the sticker on your **RM-2450** radio. It will state its default IP address (usually something like `10.223.XX.YY`, where XX and YY correspond to parts of its MAC address or serial ID).
    
2. **On your Windows PC:** Go to _Settings > Network & Internet > Ethernet > Change Adapter Options_. Right-click your Ethernet adapter and choose _Properties_. Double-click _Internet Protocol Version 4 (TCP/IPv4)_.
    
3. **On your Mac:** Go to _System Settings > Network > Ethernet > Details > TCP/IP_ and set "Configure IPv4" to _Manually_.
    
4. Change the settings to the following:
    
    - **IP Address:** `10.223.0.100` _(Choose any variation, just ensure it does not conflict with the radio’s exact IP sticker)._
        
    - **Subnet Mask:** `255.255.0.0` _(This allows your PC to look across the whole 10.223.x.x network)._
        
    - **Default Gateway:** Leave blank.
        

### Step 4: First Boot and Initial To-Do

Now that your network environment is ready, you can access the radio's built-in operating system (Mesh Rider OS / OpenWrt).

1. **Power up the unit:** Turn on the power supply. You should see the LEDs on the EVK board begin to blink, indicating the radio is booting up. Wait about 60 to 90 seconds for it to fully initialize.
    
2. **Open a Web Browser:** Open Chrome or Firefox and type the radio's sticker IP address into the URL bar (e.g., `http://10.223.XX.YY`).
    
3. **Bypass the Security Warning:** Because the radio uses a self-signed local certificate, your browser will say "Your connection is not private". Click **Advanced** and then click **Proceed / Accept the Risk and Continue**.
    
4. **The Login Screen:** The login page will appear.
    
    - **Username:** `root`
        
    - **Password:** _Leave blank_ (There is no default password). Click **Login**.
        

### Step 5: Essential Initial Configuration Tasks

Once inside the Mesh Rider GUI, complete these four "Initial To-Dos" to establish your first functional mesh link:

1. **Set a Secure Password:**
    
    - Go to **System > Administration**.
        
    - Enter a strong router password and click **Save & Apply**. Do this immediately so your device is protected.
        
2. **Verify/Match Mesh Frequency & Bandwidth:**
    
    - Navigate to the **Network > Mesh Rider** (or Wireless) tab.
        
    - To get two radios talking to each other, they **must** have identical settings here. Ensure both radios are configured to the same channel frequency (e.g., 2450 MHz) and Channel Bandwidth (usually start with a conservative `5 MHz` or `10 MHz` for initial testing, though it supports up to 20 MHz).
        
3. **Configure the Mesh ID and Encryption Key:**
    
    - On the same Mesh Rider settings page, look for the **Mesh ID** (ESSID) and **Key** (Encryption string).
        
    - Make sure both nodes share the exact same Mesh ID and Password so they recognize each other's encrypted handshakes.
        
4. **Boot up Node 2 and Test the Mesh:**
    
    - Perform Steps 2, 3, and 4 on your second RM-2450 radio node (remembering its unique sticker IP).
        
    - Once both units are powered on and configured with matching Mesh parameters, look at the **Mesh Rider Interface / Status Dashboard** in the web GUI. You should see Node 2 appear under the "Associated Stations" or "Mesh Peers" list, showing a live signal bar (RSSI) measured in dBm (aim for between -30 and -60 dBm on a test bench).
        

_Quick Troubleshooting Tip:_ If they are sitting right next to each other on your desk, the signal might be too strong and "deafen" the receivers. Move them at least 2–3 meters apart or turn down the **Transmit (Tx) Power** in the software settings to around `10 dBm` for bench testing.

Perfect! Knowing you have the exact model **RM-2450-12M3-A100-D3325** simplifies things immensely.

This model is the **Mini OEM (Smart Radio)** form factor using **JST wire harness connectors** rather than header pins. This means it relies on **Method A** for physical mounting and uses miniature wire bundles to pass data and power between the radio module and your Evaluation Board (EVK).

Here is your exact step-by-step instruction for mechanical mounting, wiring, and initial checks for this specific model.

### Step 1: Secure the Radio Mechanically (Mounting)

Because this module is incredibly light but gets warm during extended transmission, it needs to be securely fastened to the EVK for stability and a bit of passive grounding.

1. **Locate your hardware:** Inside your kit box, you should find a tiny plastic bag containing **4x short threaded standoffs** (usually brass or nylon M2 or M2.5 size) and **8x matching tiny screws**.
    
2. **Install the standoffs on the EVK:** Take 4 screws, insert them from the _bottom_ of the larger Evaluation carrier board upward through the corner mounting holes, and screw the 4 hex standoffs onto them from the top. Tighten until finger-tight.
    
3. **Place the RM-2450:** Align the 4 corner holes of the RM-2450 radio shield over the top of those 4 standoffs.
    
4. **Fasten down:** Drop the remaining 4 screws through the top of the radio corners into the standoffs. Gently tighten them down using a precision cross-pattern (top-left, then bottom-right, etc.) so the radio sits completely level.
    

### Step 2: Plug in the JST Cable Harnesses (Wiring)

Your **RM-2450-12M3** utilizes miniature white JST locking sockets on the side of the board to route power and Ethernet signals.

1. **Locate the Main Cable Assembly:** In your kit, find the custom wire harness. One side features small, multi-pin white JST plastic housings, and the other side splits into plugs that match the sockets on your Evaluation board.
    
2. **Connect to the Radio:** Look closely at the white sockets on the side of your RM-2450 module. The plastic JST plugs on your cable have tiny "fins" or keys on one side—**they will only glide into the radio socket smoothly in one direction.**
    
3. **Firmly Click Them In:** Push the wire harness plug into the radio socket until you feel or hear a micro-click. _Do not pull on the raw colored wires; always push using the white plastic housing._
    
4. **Connect to the EVK:** Plug the other end of that cable assembly into the designated expansion header or socket on your Evaluation Board.
    

### Step 3: Fasten RF Pigtails & Confirm Setup

Now that the module is clamped down and wired for data, finish the critical RF paths:

1. **The MMCX Snaps:** Press your two MMCX pigtail cables directly down onto the gold ANT0 and ANT1 round micro-ports on the module until they click into place. They should be able to spin freely but shouldn't wobble or come off with a light tug.
    
2. **Mount to Chassis / Desk:** Ensure your antennas are screwed tight to the other side of those cables and are propped upright.
    

> 🚀 **Ready for Boot-up:** With the JST wire harness plugged in and the radio screwed down, you can now safely apply power to the EVK board via its barrel jack, connect your PC to the EVK's RJ45 Ethernet port, and log in using the static IP method outlined earlier (10.223.XX.YY).