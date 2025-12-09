Equipment consideration: ![[Equipment-list-consideration.pdf]]
Document approved during 30 sep 2024 - PI - budget meeting 
![[RTG 2947 AirMetro – Hardware Purchase List.pptx]]

Initial HW equipments


![[aux-notes- hardware.pdf]]

### Holybro  X650

- Hardware: https://holybro.com/products/x650-development-kit?srsltid=AfmBOoqCYgb8HaNEsrRwr07xJ9sZ6S8hLMG4xKvN3GN-ZPEL_rELTBnZ 
- Assembly guide:  https://cdn.shopifycdn.net/s/files/1/0604/5905/7341/files/Holybro_X650_Assembly_Guide_V1.1.pdf?v=1718154187 
- Video ref: https://www.youtube.com/watch?v=ZlJs6iSO_dw 
https://www.youtube.com/watch?v=yRhfzMknK7E 
https://www.youtube.com/watch?v=5oEcA4S9I28&t=185s 
- Hangers 
- Rubber to hanger - Fit the handers - rod
- Screw on the counter - base plate  (M2) 
- Bottom plate  - PDB middle  (where to place battery) + power module  - Wiring 
- Bottom plate to (unscrew the motor beam end ) - screw to the plate  - Make sure the order is correct
- Place the side bars 
- Battery plate + foam pads for battery
- Place the legs to bottom plate  + fix to battery
- Final top plate  - See where the X650 logo - place the pixhawk accordingly . Backside of top plate is UBEC for Pixhawk 6X Pro + its lid
- LED power supply 
- Last -GPS and Compass

---


### Hexacopter

---


 ### PX4
 -  [https://www.youtube.com/watch?v=pQ4UJ2asciQ](https://www.youtube.com/watch?v=pQ4UJ2asciQ)
- [https://de.mathworks.com/help/uav/px4-spkg.html](https://de.mathworks.com/help/uav/px4-spkg.html)

--- 

### QGC



---

###  **Battery and Power** 
Battery and Power calculation : basics 
**Thumb rule :** 
-  Increased weight -> higher throttle (Takeoff) -> more power draw -> faster battery depletion 
- Consumption of gimbals 
Power -V -I requirements of the purchased hardware - ![[Power-V-I.xlsx]]
To read:![[Intro-batteryandpower.pdf]]
- [https://forum.digikey.com/t/xt30-xt60-xt90-deans-connector-comparison/34551](https://forum.digikey.com/t/xt30-xt60-xt90-deans-connector-comparison/34551)
- https://www.reddit.com/r/Multicopter/comments/8aaqad/everything_you_need_to_know_about_the_xt90/
- [https://www.youtube.com/watch?v=qEdysiZAYZ4](https://www.youtube.com/watch?v=qEdysiZAYZ4)
- PX4 battery -  https://docs.px4.io/main/en/config/battery.html

- Why is a LiPo battery important for drones?
LiPo (Lithium Polymer) batteries are essential for drones because they offer:
<span style="color:rgb(0, 176, 80)">High Energy Density:</span> They provide a lot of power in a compact and lightweight form, crucial for drones that need to stay airborne for longer durations.
<span style="color:rgb(0, 176, 80)">High Discharge Rates: </span>Drones require rapid bursts of power, and LiPo batteries can deliver high currents efficiently.
<span style="color:rgb(0, 176, 80)">Rechargeability & Longevity:</span> They can handle multiple charge cycles while maintaining performance.
<span style="color:rgb(0, 176, 80)">Customizable Cell Configurations: </span>LiPo batteries come in different cell counts (e.g., 3S, 4S, 6S) to match the voltage requirements of various drones.

-  What LiPo battery is suitable for the Holybro X650?
The Holybro X650 is a professional drone frame designed for heavy payloads and high-performance applications. Suitable LiPo battery specifications include:
<span style="color:rgb(0, 176, 80)">Voltage: </span>6S (22.2V) for optimal power output
<span style="color:rgb(0, 176, 80)">Capacity:</span> 5000mAh to 16000mAh, depending on flight duration requirements
<span style="color:rgb(0, 176, 80)">Discharge Rate (C-Rating):</span> At least 25C or higher, ensuring sufficient current supply
<span style="color:rgb(0, 176, 80)">Connector Type:</span> XT60 or XT90 (check compatibility with the power distribution board)
A recommended battery would be a 6S 10000mAh 25C LiPo for a balance between endurance and weight.

-  Why do most drones use Tattu batteries?
Tattu batteries are widely used for drones because they offer:
<span style="color:rgb(0, 176, 80)">High Reliability & Consistency:</span> They provide stable voltage and current output under heavy loads.
<span style="color:rgb(0, 176, 80)">Durability: </span>Longer lifespan with efficient heat dissipation.
<span style="color:rgb(0, 176, 80)">Low Internal Resistance:</span> Ensures better performance and efficiency.
<span style="color:rgb(0, 176, 80)">High C-Rating: </span>Essential for high-power applications like racing drones, commercial UAVs, and cinematography drones.

- Calculate Power requirement and distribution    
     - Identify power requirements of ESC , Flight controller, Telemetry, GPS
     - Camera and Gimbals
 - Calculate battery run time 
 - Consider min and max discharge rate 
 - Consider flight mode , external environmental uncertainties

- What is ESC ? 
    - An Electronic Speed Controller (ESC) is a crucial component in a drone that regulates the speed, direction, and braking of the brushless motors. It takes signals from the flight controller (Pixhawk, Betaflight, etc.) and adjusts power delivery from the LiPo battery to the motors.
    - Convert battery power to motors (DC voltage to AC signal for brushless motors) 
    - Control speed of motor and direction based on signal 
        - PWM
        - Dshot 
    - Optimize power delivery - prevent overheating and cooling , 
    - Contain short-circuit and overheat protection features
    - <span style="color:rgb(112, 48, 160)">Match Amp rating (A) with the motors requirement while choosing ESCs</span>
    - Types of ESCs: Individual ESCs and 4-in-1 ESC (all-in-one board)
    - 4S ESC won't work for 6S - check battery compatibility 
    

1. [https://holybro.com/products/microhard-radio](https://holybro.com/products/microhard-radio)
2. [https://holybro.com/products/pixhawk-6x](https://holybro.com/products/pixhawk-6x)
3. [https://www.mybotshop.de/Holybro-X650-Development-Kit_1](https://www.mybotshop.de/Holybro-X650-Development-Kit_1)
4. [https://www.flyingtech.co.uk/product/holybro-x650-quadcopter-frame-kit/](https://www.flyingtech.co.uk/product/holybro-x650-quadcopter-frame-kit/)
5. [https://docs.holybro.com/radio/microhard-radio/specification](https://docs.holybro.com/radio/microhard-radio/specification)
6. [https://docs.holybro.com/autopilot/pixhawk-6c/technical-specification](https://docs.holybro.com/autopilot/pixhawk-6c/technical-specification)
7. [https://holybro.com/products/atlatl-3w-vtx](https://holybro.com/products/atlatl-3w-vtx)
8. [https://holybro.com/products/m10-gps](https://holybro.com/products/m10-gps)
    
 ---
 
### **RC**
- Protocol RC -  [https://www.engelmt.de/access-von-frsky.html](https://www.engelmt.de/access-von-frsky.html "https://www.engelmt.de/access-von-frsky.html")
- RC- Sender Emfanger [https://www.planet-rc.ch/images/pdf/Futaba%20Sender%20Empfaenger%20Kompatibilitaet.pdf](https://www.planet-rc.ch/images/pdf/Futaba%20Sender%20Empfaenger%20Kompatibilitaet.pdf "https://www.planet-rc.ch/images/pdf/futaba%20sender%20empfaenger%20kompatibilitaet.pdf")
- Channel and Spread spectrum [https://www.rc-modellbau-portal.de/index.php?threads/sfhss-und-fhss.5248/](https://www.rc-modellbau-portal.de/index.php?threads/sfhss-und-fhss.5248/)
- PX 4 Guide - [https://docs.px4.io/main/en/getting_started/rc_transmitter_receiver.html](https://docs.px4.io/main/en/getting_started/rc_transmitter_receiver.html)
- FrSky [https://inavfixedwinggroup.com/guides/getting-started/frsky-protocols-made-simple/#22-point-of-confusion-3-frsky-protocols](https://inavfixedwinggroup.com/guides/getting-started/frsky-protocols-made-simple/#22-point-of-confusion-3-frsky-protocols)
-  [https://diydrones.com/forum/topics/need-step-by-step-guide-for-storm32-sbus-connection-to-px4](https://diydrones.com/forum/topics/need-step-by-step-guide-for-storm32-sbus-connection-to-px4)
-  [https://discuss.ardupilot.org/t/pixhawk-2-4-8-channel-issue/54111](https://discuss.ardupilot.org/t/pixhawk-2-4-8-channel-issue/54111)
- [https://docs.holybro.com/autopilot/pixhawk-6c/pixhawk-6c-ports](https://docs.holybro.com/autopilot/pixhawk-6c/pixhawk-6c-ports)
-  [https://docs.cubepilot.org/user-guides/herelink/herelink-user-guides/one-time-setup](https://docs.cubepilot.org/user-guides/herelink/herelink-user-guides/one-time-setup)
-  [https://docs.px4.io/main/en/assembly/quick_start_pixhawk4.html](https://docs.px4.io/main/en/assembly/quick_start_pixhawk4.html)
-  [https://ardupilot.org/copter/docs/common-pixhawk-wiring-and-quick-start.html](https://ardupilot.org/copter/docs/common-pixhawk-wiring-and-quick-start.html)
-  [https://docs.px4.io/main/en/assembly/quick_start_pixhawk5x.html](https://docs.px4.io/main/en/assembly/quick_start_pixhawk5x.html)
-  [https://www.youtube.com/watch?v=UGSRWx_JWUg](https://www.youtube.com/watch?v=UGSRWx_JWUg)

- To bind roll, pitch, throttle, and yaw SBUS channels in Pixhawk, follow these steps:
- Connect your SBUS receiver to the RCIN port on the Pixhawk flight controller[1](https://diydrones.com/forum/topics/need-step-by-step-guide-for-storm32-sbus-connection-to-px4)[5](https://docs.px4.io/main/en/assembly/quick_start_pixhawk4.html).
- In your ground control software (e.g., Mission Planner or QGroundControl), navigate to the Radio Calibration section.
- Move your transmitter sticks through their full range of motion, ensuring that the software detects all channels correctly.
- Map the channels as follows:

<span style="color:rgb(0, 176, 80)">Channel 1: Roll
Channel 2: Pitch
Channel 3: Throttle
Channel 4: Yaw</span>

- Save the calibration settings.
- In the flight controller parameters, ensure that the RC protocol is set to SBUS.
- For a detailed guide, you can refer to the official PX4 documentation on Pixhawk wiring and setup[5](https://docs.px4.io/main/en/assembly/quick_start_pixhawk4.html)[7](https://docs.px4.io/main/en/assembly/quick_start_pixhawk5x.html). These guides provide comprehensive information on connecting various peripherals, including SBUS receivers, to Pixhawk flight controllers.
- Additionally, the ArduPilot documentation offers a Pixhawk Wiring Quick Start guide that can be helpful for setting up SBUS and other connections[6](https://ardupilot.org/copter/docs/common-pixhawk-wiring-and-quick-start.html).

- <span style="color:rgb(0, 0, 0)"><span style="color:rgb(0, 0, 0)">Remember to check your specific Pixhawk model's documentation, as pin layouts and connection methods may vary slightly between versions.</span></span>
### FRSKY
- To set up the SBUS protocol with the FrSky Archer Plus R6 receiver and the FrSky Twin X14 transmitter, follow these steps:

   - Bind the receiver to the transmitter:
   - Power on the Twin X14 transmitter.
   - Enter the binding mode on the transmitter using the ETHOS operating system.
   - Power on the Archer Plus R6 receiver while holding the bind button.
   - The receiver will automatically detect and match the appropriate protocol (ACCESS or ACCST D16)[1](https://www.tekrc.eu/shop/receivers/frsky/frsky-archer-plus-r6/)[3](https://www.premium-modellbau.de/frsky-archer-plus-r6-access-accst-d16-2-4-ghz-empfaenger).
   - Connect the receiver to your flight controller:
   - Connect the SBUS OUT port from the Archer Plus R6 to the SBUS IN port on your flight controller.
   - Ensure proper ground connection between the receiver and flight controller.
   - Power the receiver using a 3.5V-10V power source (e.g., BEC)[1](https://www.tekrc.eu/shop/receivers/frsky/frsky-archer-plus-r6/)[3](https://www.premium-modellbau.de/frsky-archer-plus-r6-access-accst-d16-2-4-ghz-empfaenger).
   - Configure the Twin X14 transmitter:
   - Use the ETHOS operating system to set up your model and assign channels.
   - Configure the 4 customizable buttons on the transmitter front for quick access to functions like trims[4](https://www.scm-modellbau.com/FrSky-TWIN-X14-FrSky-Sender-24Ghz-Schwarz-ohne-Akku-ohne-Staenderhalter-ohne-EVA-Bag).
   - Set up the flight controller:
   - Use your ground control software (e.g., QGroundControl for Pixhawk) to calibrate the RC input.
   - Ensure the SBUS protocol is selected in the flight controller settings.
   - Map the channels correctly for roll, pitch, yaw, and throttle.
   - Test the connection:
   - Move the sticks on the Twin X14 transmitter and verify that the inputs are recognized by the flight controller.
   - Check that all channels are working correctly, including any auxiliary switches or sliders.
1. [https://www.tekrc.eu/shop/receivers/frsky/frsky-archer-plus-r6/](https://www.tekrc.eu/shop/receivers/frsky/frsky-archer-plus-r6/)
2. [https://discuss.px4.io/t/help-needed-rc-sbus-signal-from-frsky-archer-gr8-receiver-not-recognized-by-pixhawk-6x/42606](https://discuss.px4.io/t/help-needed-rc-sbus-signal-from-frsky-archer-gr8-receiver-not-recognized-by-pixhawk-6x/42606)
3. [https://www.premium-modellbau.de/frsky-archer-plus-r6-access-accst-d16-2-4-ghz-empfaenger](https://www.premium-modellbau.de/frsky-archer-plus-r6-access-accst-d16-2-4-ghz-empfaenger)
4. [https://www.scm-modellbau.com/FrSky-TWIN-X14-FrSky-Sender-24Ghz-Schwarz-ohne-Akku-ohne-Staenderhalter-ohne-EVA-Bag](https://www.scm-modellbau.com/FrSky-TWIN-X14-FrSky-Sender-24Ghz-Schwarz-ohne-Akku-ohne-Staenderhalter-ohne-EVA-Bag)
5. [https://www.frsky-rc.com/product/archer-plus-r6/](https://www.frsky-rc.com/product/archer-plus-r6/)
6. [https://www.premium-modellbau.de/frsky-twin-x14s-schwarz-fernsteuerung-dual-2.4-ghz-accst-access](https://www.premium-modellbau.de/frsky-twin-x14s-schwarz-fernsteuerung-dual-2.4-ghz-accst-access)
7. [https://www.frsky-rc.com/wp-content/uploads/Downloads/Amanual/ARCHER PLUS R6 GR6 Manual.pdf](https://www.frsky-rc.com/wp-content/uploads/Downloads/Amanual/ARCHER%20PLUS%20R6%20GR6%20Manual.pdf)
8. [https://www.flyingtech.co.uk/product/frsky-archer-plus-r6-2-4g-8ch-access-accst-receiver/](https://www.flyingtech.co.uk/product/frsky-archer-plus-r6-2-4g-8ch-access-accst-receiver/)
9. [https://discuss.px4.io/t/r9sx-sbus-no-radio-channels/19426](https://discuss.px4.io/t/r9sx-sbus-no-radio-channels/19426)
10. [https://www.engelmt.de/mtfrsky-fernsteuerungen-und-zubehoer/fernsteuerungen/ethos-mehrsprachig/twin-x14-serie/1](https://www.engelmt.de/mtfrsky-fernsteuerungen-und-zubehoer/fernsteuerungen/ethos-mehrsprachig/twin-x14-serie/1)
### FRSky Setup 
- **SBUS**: A digital protocol that transmits up to 16 or 24 channels over a single wire. It's widely supported and commonly used for connecting receivers to flight controllers.
- **F.Port**: A newer FrSky protocol that combines SBUS and SmartPort telemetry into a single bi-directional signal line. This simplifies wiring and enables telemetry feedback from the flight controller to the transmitter.
<span style="color:rgb(0, 176, 80)">We go with Sbus protocol </span>
- Sbus out  to RC In Pixhawk 6X
- Use a 5V and GND connection from the Pixhawk to the receiver
- 
-  For Sbus Protocol -  RC_PROTOCOL = 1 (SBUS) 
- SERIAL2_PROTOCOL = 10 (FrSky Telemetry)
SERIAL2_BAUD = 57600
- Register receiver - Internal transmission mode -bind and set https://www.youtube.com/watch?v=BGn9RvFaZN8&t=1847s - registration ok 
- Bind the receiver 
- 4 Trims 
### PX4 RC issues
1.  [https://docs.px4.io/main/en/getting_started/rc_transmitter_receiver.html](https://docs.px4.io/main/en/getting_started/rc_transmitter_receiver.html)
2. [https://www.mybotshop.de/Datasheet/Radiolink_Pixhawk_Manual.pdf](https://www.mybotshop.de/Datasheet/Radiolink_Pixhawk_Manual.pdf)
3. [https://github.com/ArduPilot/ardupilot_wiki_copy/blob/master/common/source/docs/common-pixhawk-and-px4-compatible-rc-transmitter-and-receiver-systems.rst](https://github.com/ArduPilot/ardupilot_wiki_copy/blob/master/common/source/docs/common-pixhawk-and-px4-compatible-rc-transmitter-and-receiver-systems.rst)
4. [https://docs.qgroundcontrol.com/master/en/qgc-user-guide/setup_view/radio.html](https://docs.qgroundcontrol.com/master/en/qgc-user-guide/setup_view/radio.html)
5. [https://docs.px4.io/main/en/flight_controller/pixhawk4.html](https://docs.px4.io/main/en/flight_controller/pixhawk4.html)
6. [https://docs.px4.io/main/en/config/radio.html](https://docs.px4.io/main/en/config/radio.html)
7. [https://docs.px4.io/main/en/getting_started/px4_basic_concepts.html](https://docs.px4.io/main/en/getting_started/px4_basic_concepts.html)
8. [https://github.com/PX4/PX4-Autopilot/issues/21674](https://github.com/PX4/PX4-Autopilot/issues/21674)

### SIYI MK 15

- [https://www.premium-modellbau.de/media/pdf/fb/a1/00/MK15_User_Manual_en_v1-2.pdf](https://www.premium-modellbau.de/media/pdf/fb/a1/00/MK15_User_Manual_en_v1-2.pdf)
- [https://www.siyi.biz/](https://www.siyi.biz/)
- MK15 supports 4G network, like a smartphone. You can put in an SIM card into the transmitter to activate the function. Before putting in an SIM card into MK15 transmitter, please check if it is compatible with your local cellular network.
- LTE FDD: B1/B3/B5/B7/B8 LTE TDD: B34/B38/B39/B40/B41 EVDO/CDMA: BC0
- 1080p video simultaneously, latency low to *180ms
- The 180ms latency is an average result measured by using SIYI standard IP camera under the following conditions: H.265 format, 720p @ 30 fps, displayed in QGC v4.1 (low-latency mode): end-to-end latency is between 130 and 180ms. H.265 format, 1080p @ 30 fps, displayed in QGC v4.1 (low-latency mode): end-to-end latency is between 180 and 250ms.

SIYI Report


- page 39 Android RC settings

![[siyi1 1.png]]
![[siyi2.png]]
- Antenna, Antenna Setup and link quality

1. 0 to 10 Kilometers Range Two standard omni antennas on ground unit. Wireless mode: 5 km or 8 km low latency. 2. 10 to 15 Kilometers Range Two standard omni antennas or two standard long-range antennasongroundunit.Wireless mode: 15 km GCS. 3. 15 to 30 Kilometers GCS Flight Two standard long-range antennas or higher gain patch antennasongroundunit. Wireless mode: 24 km GCS.
2. The signal at the top of the standard omnidirectional antennaisweak. Whenflying directly above the ground, the flying height of the aircraft shouldbeaslowas 100 meters. 5. When the ground unit is working with long range antennas or patchantennas,the aircraft should always be in front of the antenna panel insteadof beingvertical of the antenna or on opposite. 6. Only the standard omni antennas are suggested for the air unit. If your aircraftis too small to mount the omni antennas, or you worry about theweaksignalofthe top part, then you can consider using SIYI lollipop antennas. Lollipopantennas performs shorter range than the standard omni antennas.

- page 42 - 45 Antenna
- 2.2.4 How to Place the Long-Range Patch Antennas on GroundUnit

1. The SMA connectors should be screwed tightly. 2. Long-range patch antennas are directional, which should alwaysbepointingtothe aircraft during flight. 3. When you are using SIYI standard long-range antennas, pleasemakeitsshortside be parallel with horizon and its long side be vertical of thecontrol paneltoget the best signal quality. 2.2.5 How to Place Air Unit Antennas
2. The SMA connectors should be screwed tightly. 2. On multirotor, the standard omni antennas should be hanging verticallyfromthedrone arms with the antenna heads pointing to ground, andtheantennaflatside should always point to the ground unit during flight. Onplane,thestandard omni antenna can stand vertically above the wings, andtheantennaflat side should always point to the ground unit during flight. 3. The air unit antenna feeder wire should be placed away fromE.S.Candmotors, and any other equipment with heavy current or interference. Donot crossoroverlap the antenna feeder wires. 4. The antenna body, feeder wire, and the SMA connectors shouldnot touchthemetal / carbon-fiber structure parts directly. Please reserveat least 10mmdistance between these parts and the structure parts. 5. The two air unit antennas should be placed away fromeach other for at least50mm distance. And try your best to avoid any kinds of obstructionbetweentheground unit and the aircraft during flight. 6. Please be very careful with the antenna wire’s SMA connectorsanditssolderconnectors. Do not drag them or bend them in case of any damage. Toadjustthe position of the antenna, please always try to bend the middlepart oftheantenna feeder wires

- Page 63 - binding
- Page 81 -
- Page 92 - QGC
- Page 107 - UDP Wifi hotspot
- Page 125 - FPV app
- Page 148 - IP addresses


---

### **5G and Satcom terminals**
![[Shreeja- research-Comm-HW.pdf]]

The integration of 5G and satellite communications (Satcom) is pivotal in advancing Unmanned Aerial Systems (UAS) operations, particularly for Beyond Visual Line of Sight (BVLOS) missions. Several industry players are at the forefront of developing these communication enablers:

**1. Honeywell Aerospace**
- **VersaWave System:** Honeywell has introduced VersaWave, a compact Satcom system that combines satellite, 5G, 4G, Wi-Fi, and Bluetooth connectivity. Designed for Advanced Air Mobility (AAM) and UAS applications, VersaWave facilitates BVLOS communication in a lightweight package.
    [aerospace.honeywell.com](https://aerospace.honeywell.com/us/en/about-us/press-release/2023/05/honeywell-introduces-new-small-satcom-system-versawave-with-5g-for-advanced-air-mobility-market?utm_source=chatgpt.com
**2. Videosoft Global and ATMOSPHERE**
- **5G/Iridium Certus Terminal:** In collaboration, these companies have developed the world's first Iridium-certified terminal for UAVs, integrating 5G capabilities with real-time low-bandwidth video streaming. This innovation enhances surveillance and communication for UAV operations.
    [videosoftglobal.com](https://www.videosoftglobal.com/news/worlds-first-5g-iridium-certus-uav-for-surveillance-realtime-video/?utm_source=chatgpt.com)
**3. JOUAV**
- **5G-Connected UAVs:** JOUAV offers UAV systems equipped with 5G connectivity, providing advantages in emergency communications, remote sensing, power line inspection, urban security, and environmental monitoring. The integration of 5G reduces costs and increases operational efficiency.
    [jouav.com](https://www.jouav.com/industry/5g?utm_source=chatgpt.com)
**4. Vodafone and AST SpaceMobile**
- **Satellite-Enabled 5G Connectivity:** Vodafone, in partnership with AST SpaceMobile, has successfully conducted the world's first satellite video call using a standard smartphone. This technology aims to eliminate mobile coverage gaps, enabling users in remote areas to access 4G and 5G services without special devices.
    [thetimes.co.uk](https://www.thetimes.co.uk/article/vodafone-satellite-video-call-ordinary-smartphone-r8nkrctlx?utm_source=chatgpt.com)

https://www.skydrone.aero/collections/frontpage/products/sky-drone-link-3

Elsight BVLOS terminal 
https://sky-drones.com/sets/airlink-5g-enterprise-set.html 
https://sky-drones.com/telemetry

### **Protocols** 
RSTP

---

### 1. **What is Auto-Tuning of Drones?**

**Auto-tuning** is a **process where the drone adjusts its own control system parameters** (usually PID gains) automatically, during a flight, to optimize how it responds to control inputs.

- **PID** stands for **Proportional, Integral, Derivative** — these parameters determine how aggressively or smoothly the drone reacts to things like stick movements or disturbances (like wind).
- Manual tuning would involve a human trial-and-error approach (test flying, adjusting, testing again).
- Auto-tuning automates this process to find **ideal controller settings** for the drone’s weight, motor thrust, frame stiffness, and aerodynamic behavior

 2. **Why is Auto-Tuning Done While Flying?**
- The drone's behavior depends heavily on **how it moves** — inertia, drag, motor dynamics, and sensor feedback only become meaningful **while it's actually flying**.
- During flight, the drone can **excite** (intentionally wiggle or shake slightly) the airframe in controlled ways to observe its dynamic response.
- It measures the **real-world data**: how quickly it accelerates, decelerates, overshoots, etc.
- From these responses, it calculates the best PID parameters.

If it was tuned on the ground, the data would be completely wrong because real aerodynamic forces are not acting on it.

3. **Why is Auto-Tuning Important?**
- **Performance**: Proper tuning makes the drone fly **more precisely and smoothly**, which is critical for tasks like mapping, inspection, delivery, etc.
- **Efficiency**: A poorly tuned drone wastes battery by overcorrecting or fighting itself.
- **Safety**: An improperly tuned drone might oscillate, crash, or behave unpredictably, especially in wind or during aggressive maneuvers.
- **Adaptability**: Changes like new payloads, damaged propellers, or aging motors change flight dynamics — auto-tuning helps re-optimize without deep manual work.

 3. **How PX4 Parameters Help in Safe Tuning?**
PX4 is a very mature open-source flight control software, and it has **several layers of safety** during tuning:

- **Pre-set Limits**: PX4 uses **parameter constraints** (like maximum allowed PID values, acceptable oscillation thresholds) to avoid going into unsafe ranges.
- **Supervised Excitation**: The auto-tune uses controlled and small movements — it does not perform dangerous or extreme maneuvers during tuning.
- **Failsafe Behavior**: If oscillations exceed certain thresholds (e.g., indicating instability), the tuning is **aborted automatically** to prevent crashes.
- **Data Filtering**: PX4 uses **low-pass filters** on sensor data to prevent noise from confusing the tuning algorithm.
- **Progressive Updates**: PX4 doesn't apply the new tuning all at once — it can save intermediate results and validate them before finalizing.
- **Flight Mode Control**: Auto-tuning is usually engaged in a **specific safe flight mode** (like Position mode or Altitude mode) so the pilot retains override control.

Some specific PX4 parameters that are critical during auto-tuning include:

- `ATC_RAT_PIT_*`, `ATC_RAT_RLL_*`, `ATC_RAT_YAW_*` (rate controller tuning)
- `MC_TUNE_ENABLE` (to enable/disable auto-tuning)
- `MC_TUNE_PID_*` (specifies how aggressive the auto-tuning is)
- `IMU_INTEG_RATE`, `IMU_GYRO_CUTOFF` (sensor filtering, important for clean data during tuning)

Auto-tuning while flying is crucial because real-world aerodynamic forces can only be measured mid-flight. PX4 provides a smart, layered safety system to ensure tuning improves performance without risking a crash.
 **Safety Notes During Auto-Tune**:

- Always do it in **good GPS conditions**, **no wind** if possible.
- Make sure you are **high enough** (5–10 meters minimum).
- Stay ready to **take manual control** if oscillations start.
- Monitor **logs after flight** (`.ulg` files) to confirm stability
- 
 ➔ What are **P values** in Auto-Tuning?

In **control systems** (especially in drone flight), the **P value** refers to the **Proportional Gain** of the **PID controller**.
Specifically in auto-tuning:
- **P** determines **how strongly** the drone reacts to an error — for example, how fast it corrects a tilt or heading mistake.
- When the error (e.g., angle off-target) is large, the **P** gain multiplies that error to produce a corrective action.

Mathematically:
Control Output=P×(Error)\text{Control Output} = P \times (\text{Error})
Where:
- **Error** = desired value – current value (e.g., desired pitch angle – actual pitch angle)
- **P** = proportional gain (how aggressively the drone corrects)

 **In Auto-Tuning Specifically:**
During auto-tuning, PX4 automatically adjusts the **P** values based on how the drone **responds to small disturbances**:
- If the drone is **too sluggish** (slow to correct), auto-tune **increases** P.
- If the drone **overshoots** (moves too much past the target) or **oscillates**, auto-tune **reduces** P.

**Auto-tune finds a "sweet spot"** where:
- The drone responds **quickly** but **without overshooting** or **oscillating**.

 **Where P Gains are Applied in PX4:**
There are **two important levels** of P gains:

|**Controller Level**|**PX4 Parameter Example**|**Meaning**|
|:--|:--|:--|
|**Rate Controller P**|`ATC_RAT_RLL_P`, `ATC_RAT_PIT_P`, `ATC_RAT_YAW_P`|How hard the drone corrects its angular rate (deg/sec).|
|**Angle Controller P**|`ATC_ANG_RLL_P`, `ATC_ANG_PIT_P`|How hard the drone corrects its tilt angle (degrees).|

Usually **rate P** is tuned **first**, because the **rate loop** is _inside_ the angle loop.

 **Visual Example:**

Imagine if you push your drone slightly sideways:

- **Low P value**:  
    It slowly drifts back to level — _laggy_ and _unresponsive_.
- **Perfect P value**:  
    It quickly and cleanly comes back to level — _snappy but smooth_.
- **Too High P value**:  
    It _overcorrects_, _vibrates_, or _wobbles_ — unstable.

Auto-tuning automatically **measures** these reactions and **sets the right P**.

 ➔ **Simple analogy**:

P value is like how **tight** the steering wheel feels in a car.

- If it's **too loose** → Sluggish reaction → Hard to stay in lane.
- If it's **too tight** → Overreacts to small movements → Jerky ride.
- **Perfectly tuned** → Smooth, precise, easy driving.

 Typical P values (for Multicopters) after Auto-Tune**

|**Axis**|**Rate P Gain Typical Range**|
|:--|:--|
|Roll|0.05 – 0.2|
|Pitch|0.05 – 0.2|
|Yaw|0.1 – 0.5|

(Note: These are rough! Your frame size, weight, and motor power heavily affect the final numbers.)

 **In Short:**

- P value = Proportional gain = "how strong is the correction for a given error"
- Auto-tuning adjusts P (and I, D) so the drone flies **sharp but safe**.
- In PX4, **Rate P** (`ATC_RAT_*_P`) and **Angle P** (`ATC_ANG_*_P`) are the main targets.


--- 

### **Remote ID and e-ID**
- Being registered as UAS operator / pilot with A1/A3 license - unique identification number 
- e-ID is the identifizierungsnummber in A1/A3 certificate
- https://www.dipul.de/homepage/en/information/general/registration-and-qualification/
- e-ID is often referred as operator ID

Remote ID https://www.drohnen.de/48027/fernidentifikation_remote-id/
- Often referred as digital license plate
 - Remote identification of drone classes C1-C3 and C4-C6 
 - How DJI does it ? 
     - register and get e-ID 
     - DJI fly app - sicherheit tab - include this e-ID  - here drone identification is by Operator ID
     - This is constantly emitted by inbuilt WIFI /bluetooth module within range of 100 m to 1.5 km
     - Drone scanner app from Drone tag can be used to check this 
- The following data must be permanently sent by law (COMMISSION DELEGATED REGULATION (EU) 2019/945) using the Remote ID system for remote identification from the drone:

- The physical serial number of the drone (according to ANSI/CTA-2063 standard)
- The pilot’s e-ID / UAS operator number
- Position data (geographical position) of the drone (coordinates including height above ground or above the take-off point)
- Direction of the drone and the speed
- Position (geographical position) of the pilot (of the remote control / smartphone / app) or, if not available, the starting point of the drone (home point)
- If the pilot's position is unknown, the drone's starting point (home point)

Optionally, additional data may be sent – ​​for example:
- GPS time / timestamp of the current data record
- Type / model of drone / designation

- **Drones >250g without C-labels**  (CE marking complainace) operated in the **Open Category** must be flown under the **A3 subcategory**, **away from people**, and **require remote ID if flying after Jan 1, 2024** in non-exempted areas.

Possible solutions 
- Cube pilot  - proprietary solution https://docs.cubepilot.org/user-guides/cube-id/cube-id#updating 
- Ardupilot Remote ID - https://github.com/ArduPilot/ArduRemoteID
- Px4  https://docs.px4.io/main/en/peripherals/remote_id.html supports (beta phase) remote id equipment - by holybro are available - https://holybro.com/products/remote-id - But
-  **Warning** 
<span style="color:rgb(255, 0, 0)">This product is designed for the [Standard Remote ID Solution](https://www.faa.gov/uas/getting_started/remote_id), primarily targeting drone manufacturers and system integrators, NOT for DIY users, as you need to do your own approval process at the FAA (DoC submission) if you are in the USA. This product does not include serial number. For the most accurate and latest information related to this topic, please refer to the official governance website of your country.</span> 
If in public airspace dronetag , droniq remote ID module (CE compliance)
- https://dronetag.com/products/beacon/ (200€)
- https://droniq.de/en/produkte/dronetag-rider/ (1000 €) - specification sheet https://help.dronetag.com/dronetag-rider/
- https://www.aerobits.pl/product/idme-plus/ (89 €) Specification - https://www.aerobits.pl/wp-content/uploads/ci_uploads_software/idme/technical_documentation_idme_plus/IDME_RemoteID_Datasheet_v1_29_1.pdf 

---

<span style="color:rgb(0, 176, 80)">Remote ide Aerobits IdME Pro purchased </span>
Step - Setup
Details and Specs 
- Drone remote identification and localization  - Ble broadcast and WiFi Nan and Beacon Frames 
- Equipped with Multi-GNSS receiver and Barometric sensors 
- Firmware Version - v1.29.1
- Power budget: 5V , <130 mA Power connector - JST 6pin or micro usb Type B
- Power and Data  JST GH SM
B- GHS-TB_ LF-SN- Connection to Pixhawk 
- Interface USB and UART 
- How to power: 
- Use free android Application - OpenDroneID OSM 
-  First Band BLE 2400 MHz | Second Band Wi-Fi 2400 MHz| Third Band GNSS 1575 MHz| Max. output (BLE) Maximum output power +18 dBm| Max. output (Wi-Fi) Maximum output power +20 dBm| Sensitivity (GNSS) -167 dBm
- UART AT commands   - 57600 Baudrate 921600 bps , Stop bit 1 , No flow or parity bit 
- USB AT commands
Different States : 
Bootloader: This is an initial state of after restart. Firmware update is possible here. Typically module transitions automatically to RUN state. It is possible to lock module in this state (prevent transition to RUN state) using one of BOOTLOADER triggers.

Run : In this state module is broadcasting drone identification data. In this state module is working and receiving the data from aircrafts.

Configuration state: Change of stored settings is possible 
 Transition between states are possible. Only possible state is RUN state 
 
Q: Diff between Bluetooth 3, 4 ?

// Commands
AT+DRONE_ID_ADVERTISING_ENABLE=1       [Advertising enable]
 AT+DRONE_ID_BASIC_BROADCAST_PERIOD=1500 [Basic frame broadcast period in [ms]]
 AT+DRONE_ID_BROADCAST_BLUETOOTH_4=1    [Enable Bluetooth 4.0 broadcast]
 AT+DRONE_ID_BROADCAST_BLUETOOTH_5=1    [Enable Bluetooth 5.0 broadcast]
 AT+DRONE_ID_BROADCAST_WIFI_BEACON=1    [Enable Wifi Standard Beacon broadcast]
 AT+DRONE_ID_BROADCAST_WIFI_NAN_BEACON=0 [Enable WiFi NaN Beacon broadcast]
 AT+DRONE_ID_LOCALIZATION_BROADCAST_PERIOD=500 [Localization frame broadcast period in [ms]]
 AT+DRONE_ID_SCAN_ENABLE_BT=0           [Scan enable Bluetooth]
 AT+DRONE_ID_SCAN_ENABLE_WIFI=0         [Scan enable Wifi]
 AT+FIRMWARE_VERSION=1.25.6.0 (Dec 13 2024) [Device's firmware version]
 AT+USER_PIN_1=0                        [Set user pin 1]
SYSTEM:
 AT+BAUDRATE=0                          [Baudrate of serial interface (0:115200, 1:921600, 2:3000000, 3:57600)]
 AT+BOOT=0                              [Is firmware in bootloader mode]
 AT+CONFIG=1                            [CONFIG mode (0:disable, 1:baudrate 115200, 2:baudrate as set)]
 AT+DEVICE=IDME-PRO                     [Device type's name]
 AT+LOCK=0                              [Device in CONFIG mode (0:no lock, 1:lock)]
 AT+SERIAL_NUMBER=18099300000528        [Device's serial number]
 AT+SYSTEM_LOG=0                        [System logs (0:disable, 1:enable)]
 AT+SYSTEM_STATISTICS=CSV               [None, CSV]
GNSS:
 AT+GNSS_RX_PROTOCOL_RAW=NMEA           [None, NMEA]
SENSORS:
 AT+SENSORS_RX_PROTOCOL_RAW=NONE        [None, CSV, JSON]
RID:
 AT+DRONE_ID_DRONE_CATEGORY_CLASS=0     [Drone category class.]
 AT+DRONE_ID_HEIGHT_TYPE=0              [Height type]
 AT+DRONE_ID_MAVLINK_CONNECTION_TIMEOUT=5 [Mavlink timeout in [s]]
 AT+DRONE_ID_MODE=1                     [Force standalone mode]
 AT+DRONE_ID_OPERATIONAL_STATUS=0       [Operational Status]
 AT+DRONE_ID_OPERATION_CATEGORY=0       [Operation category. Open, Specific or Certified]
 AT+DRONE_ID_OPERATOR_ID=               [Operator message payload]
 AT+DRONE_ID_OPERATOR_ID_TYPE=0         [Operator ID type]
 AT+DRONE_ID_SELF_ID=                   [Self message payload]
 AT+DRONE_ID_SELF_ID_TYPE=0             [Self message type]
 AT+DRONE_ID_TYPE=1                     [UAS ID type]
 AT+DRONE_ID_UAS_ID=                    [UAS ID]
 AT+DRONE_ID_UAS_TYPE=0                 [UAS type]
COMMANDS:
 AT+3RD_PARTY_LICENSES                   [Displays licenses of third party software]
 AT+BLUETOOTH_MAC                        [Bluetooth device mac address]
 AT+DRONE_ID_OPERATOR_ID                 [Operator message payload]
 AT+HELP                                 [Show this help]
 AT+INFO                                 [Display device information]
 AT+REBOOT                               [Reboot system]
 AT+REBOOT_BOOTLOADER                    [Reboot to bootloader]
 AT+SETTINGS_DEFAULT                     [Loads default settings]
 AT+TEST                                 [Responds "AT+OK"]
 AT+WIFI_MAC                             [WiFI device mac address]
AT






### **Network Remote ID**

- **What it is**: Sends your drone's flight data (ID, location, etc.) over the **internet** to a central database or service provider via a **mobile network or Wi-Fi**.
- **Who receives it**: Authorities or authorized users who access the service online.
- **Purpose**: Useful for **centralized monitoring** in urban air traffic management systems (U-Space).

**Not required** yet in the EU but is **used in some other countries** (like the U.S. for future UTM/U-Space integration).
Ground station for ADS-B/ FLARM and Uspace-UTM surveillance
- https://www.aerobits.pl/wp-content/uploads/ci_uploads_software/gs2l/technical_documentation/GS2L_Datasheet_v1_16_0.pdf
- https://www.aerobits.pl/product/ground-station-with-linux/
- https://www.aerobits.pl/wp-content/uploads/ci_uploads_software/gs2l/gs2l_software_documentation/gs2l_software_latest.pdf

### EASA links 
- https://www.easa.europa.eu/en/domains/drones-air-mobility/operating-drone/open-category-low-risk-civil-drones
- https://www.uas-operations.de/homepage/en/information/general/legal-bases/
- https://dipul.de/homepage/en/information/general/first-steps/

---
### Companion Computer 
### Rasp pi - pixhawk connection 
https://docs.px4.io/main/en/companion_computer/pixhawk_rpi.html
https://px4.io/get-the-pixhawk-raspberry-pi-cm4-baseboard-by-holybro-talking-with-px4/
https://www.youtube.com/watch?v=nIuoCYauW3s
https://docs.px4.io/main/en/companion_computer/pixhawk_rpi.html#ubuntu-setup-on-rpi
https://docs.px4.io/main/en/advanced_config/ethernet_setup.html#supported-flight-controllers
https://docs.px4.io/main/en/companion_computer/pixhawk_companion.html#serial-port-setup
https://docs.px4.io/main/en/companion_computer/

Procedure
- Serial hardware enable - Rasppi config 
- Interface options - enable serial port enable 
- Bluetooth occupy the uart ports - so disable 
- Make sure all UART ports are available for Pixhawk
- https://www.youtube.com/watch?v=nIuoCYauW3s&t=188s 
- Pip , pyyaml mavproxy
- https://dojofordrones.com/what-is-mavproxy/
- 

### Jetson Orin NX - Wifi Card



![Wireless Card Dual band intel Wireless AC 7265 7265NGW ...](https://d2u1z1lopyfwlx.cloudfront.net/thumbnails/bf875915-f934-598b-8dda-b47dff777e8e/67deb6c3-b137-50e2-95c8-31f1b8543917.jpg)





## Intel AC 7265 Dual Band WiFi: Components Overview

The **Intel Dual Band Wireless-AC 7265** is a compact wireless module offering both WiFi and Bluetooth connectivity. Here are its key components and features:

- **WiFi:**
    
    - Supports 802.11ac (dual band, 2x2 MIMO)
    - Maximum speed up to 867 Mbps
    - Operates on both 2.4 GHz and 5 GHz bands
    - M.2 2230 and M.2 1216 form factors
    - PCIe and USB interfaces
    - Advanced features: improved channel reliability, better coverage, and energy efficiency[4](https://www.intel.com/content/dam/www/public/us/en/documents/product-briefs/dual-band-wireless-ac-7265-brief.pdf)[6](http://www.bplus.com.tw/Accessory/INTEL-7265.html)

- **Bluetooth:**
    
    - Version 4.2 (dual mode, including Low Energy)
    - Connects to a wide range of Bluetooth peripherals[4](https://www.intel.com/content/dam/www/public/us/en/documents/product-briefs/dual-band-wireless-ac-7265-brief.pdf)[6](http://www.bplus.com.tw/Accessory/INTEL-7265.html)

- **Other Features:**
    
    - Microsoft InstantGo support (low-power connectivity)
    - Worldwide regulatory support
    - Operating temperature: 0°C to +80°C
    - Designed for thin-and-light devices (very compact)[4](https://www.intel.com/content/dam/www/public/us/en/documents/product-briefs/dual-band-wireless-ac-7265-brief.pdf)[6](http://www.bplus.com.tw/Accessory/INTEL-7265.html)


## Setting Up Intel AC 7265 with Jetson Orin NX

**1. Hardware Installation:**

- Insert the Intel AC 7265 module into the M.2 Key E slot on your Jetson Orin NX carrier board.
- Attach the external antennas if included

**2. Driver and Firmware Support:**

- The Intel 7265 relies on the `iwlwifi` Linux driver.
- On NVIDIA Jetson platforms, especially with recent JetPack releases, the 7265 is often **not fully supported out-of-the-box**.
- Users have reported that while Bluetooth may work, WiFi functionality is frequently missing or unreliable[3](https://forums.developer.nvidia.com/t/intel-7265-wifi-missing-bluetooth-functional/73934).
- The last Linux driver version with solid support for the 7265 was "Core14." If your kernel is newer, you may need to **downgrade the driver** or manually build the backported iwlwifi driver from the Core14 branch[3](https://forums.developer.nvidia.com/t/intel-7265-wifi-missing-bluetooth-functional/73934).


**3. Steps to Attempt WiFi Setup:**

- Check if the card is recognized:
    
    bash
    
    `lspci | grep -i wireless`
    
- Check driver status:
    
    bash
    
    `dmesg | grep iwlwifi`
    
- If WiFi is not working, try building and installing the backport driver (Core14 branch)[3](https://forums.developer.nvidia.com/t/intel-7265-wifi-missing-bluetooth-functional/73934):
    
    - Clone the backport repository:
        
        text
        
        `git clone -b release/LinuxCore14 https://git.kernel.org/pub/scm/linux/kernel/git/iwlwifi/backport-iwlwifi.git`
    
    - Build and install according to the repository's instructions.


**4. Alternative Recommendation:**

- The **Intel 8265** WiFi card is widely recommended for Jetson platforms, as it works with the preinstalled drivers and provides a more reliable experience[3](https://forums.developer.nvidia.com/t/intel-7265-wifi-missing-bluetooth-functional/73934)5.

## Summary Table

|Feature|Intel AC 7265 Details|
|---|---|
|WiFi Standard|802.11ac, dual band, 2x2 MIMO|
|Max Speed|867 Mbps|
|Bluetooth|4.2 (dual mode)|
|Interface|M.2 2230/1216, PCIe, USB|
|Jetson Support|Partial (WiFi often problematic, Bluetooth may work)[3](https://forums.developer.nvidia.com/t/intel-7265-wifi-missing-bluetooth-functional/73934)|
|Recommended Card|Intel 8265 for full compatibility[3](https://forums.developer.nvidia.com/t/intel-7265-wifi-missing-bluetooth-functional/73934)5|

If you need step-by-step guidance on building drivers or want alternative WiFi card suggestions for Jetson Orin NX, just ask!

- [ ] https://www.ardusub.com/reference/troubleshooting.html

<span style="color:rgb(0, 176, 80)">Research </span>
Typically your router (or the mobile network) has a public IP address, and your GCS computer/vehicle are on a _local_ network. The router uses network address translation (NAT) to map _outgoing_ requests from your local network to the Internet, and can use the map to route the _responses_ back to requesting system. However NAT has no way to know where to direct the traffic from an arbitrary external system, so there is no way to _initiate_ a connection to a GCS or vehicle running in the local network. 
https://docs.px4.io/main/en/companion_computer/companion_computer_peripherals.html#ftdi-devices


### Citations:

1. [https://www.intel.com/content/www/us/en/products/sku/83635/intel-dual-band-wirelessac-7265/specifications.html](https://www.intel.com/content/www/us/en/products/sku/83635/intel-dual-band-wirelessac-7265/specifications.html)
2. [https://jetsonhacks.com/2019/04/08/jetson-nano-intel-wifi-and-bluetooth/](https://jetsonhacks.com/2019/04/08/jetson-nano-intel-wifi-and-bluetooth/)
3. [https://forums.developer.nvidia.com/t/intel-7265-wifi-missing-bluetooth-functional/73934](https://forums.developer.nvidia.com/t/intel-7265-wifi-missing-bluetooth-functional/73934)
4. [https://www.intel.com/content/dam/www/public/us/en/documents/product-briefs/dual-band-wireless-ac-7265-brief.pdf](https://www.intel.com/content/dam/www/public/us/en/documents/product-briefs/dual-band-wireless-ac-7265-brief.pdf)
5. [https://www.youtube.com/watch?v=6CiNyQ__PSY](https://www.youtube.com/watch?v=6CiNyQ__PSY)
6. [http://www.bplus.com.tw/Accessory/INTEL-7265.html](http://www.bplus.com.tw/Accessory/INTEL-7265.html)
7. [https://fcc.report/FCC-ID/2AVBM-TK11-B0/5728605.pdf](https://fcc.report/FCC-ID/2AVBM-TK11-B0/5728605.pdf)
8. [https://fcc.report/FCC-ID/2AVBM-AK1/5727983.pdf](https://fcc.report/FCC-ID/2AVBM-AK1/5727983.pdf)
9. [https://www.ebay.de/itm/271813383837](https://www.ebay.de/itm/271813383837)
10. [https://techinfodepot.shoutwiki.com/wiki/Intel_Dual_Band_Wireless-AC_7265_(7265NGW)](https://techinfodepot.shoutwiki.com/wiki/Intel_Dual_Band_Wireless-AC_7265_\(7265NGW\))
11. [https://www.shi.com/product/34065311/Intel-Dual-Band-Wireless-AC-7265](https://www.shi.com/product/34065311/Intel-Dual-Band-Wireless-AC-7265)
12. [https://nvidia-jetson.piveral.com/jetson-orin-nano/setting-up-wifi-and-ethernet-sharing-on-nvidia-jetson-orin-nano-dev-board/](https://nvidia-jetson.piveral.com/jetson-orin-nano/setting-up-wifi-and-ethernet-sharing-on-nvidia-jetson-orin-nano-dev-board/)
13. [https://community.intel.com/t5/Wireless/BE200-support-on-Jetson-Orin-NX/td-p/1666212](https://community.intel.com/t5/Wireless/BE200-support-on-Jetson-Orin-NX/td-p/1666212)
14. [https://www.youtube.com/watch?v=v_neNpfQ38Q](https://www.youtube.com/watch?v=v_neNpfQ38Q)
15. [https://forum.seeedstudio.com/t/trouble-installing-wifi-drivers-for-jetson-orin-nx-j4012/280971](https://forum.seeedstudio.com/t/trouble-installing-wifi-drivers-for-jetson-orin-nx-j4012/280971)
16. [https://ubuntuforums.org/archive/index.php/t-2346021.html](https://ubuntuforums.org/archive/index.php/t-2346021.html)
17. [https://community.intel.com/t5/Wireless/BE200-support-on-Jetson-Orin-NX/m-p/1668145](https://community.intel.com/t5/Wireless/BE200-support-on-Jetson-Orin-NX/m-p/1668145)
18. [https://askubuntu.com/questions/1390071/is-there-any-permanent-fix-for-no-wifi-with-iwlwifi-other-than-removing-the-pnv](https://askubuntu.com/questions/1390071/is-there-any-permanent-fix-for-no-wifi-with-iwlwifi-other-than-removing-the-pnv)
19. [https://forums.linuxmint.com/viewtopic.php?t=414216](https://forums.linuxmint.com/viewtopic.php?t=414216)
20. [https://askubuntu.com/questions/1477620/wifi-adapter-not-found-on-nvidia-jetson-orin-nx-running-ubuntu-20-04](https://askubuntu.com/questions/1477620/wifi-adapter-not-found-on-nvidia-jetson-orin-nx-running-ubuntu-20-04)
21. [https://community.intel.com/t5/Wireless/Intel-AC-7265-NGW-support-for-Linux/m-p/488787](https://community.intel.com/t5/Wireless/Intel-AC-7265-NGW-support-for-Linux/m-p/488787)
22. [https://www.mini-box.com/Intel-Dual-Band-Wireless-AC-7265-M-2](https://www.mini-box.com/Intel-Dual-Band-Wireless-AC-7265-M-2)
23. [https://it-mixx.de/Intel-Dual-Band-Wireless-AC-7265-WLAN-Karte-7265NGW-P-N-0K57GX](https://it-mixx.de/Intel-Dual-Band-Wireless-AC-7265-WLAN-Karte-7265NGW-P-N-0K57GX)
24. [https://www.verical.com/datasheet/intel-802.11-modules-7265.ngwg.w-939155-4357719.pdf](https://www.verical.com/datasheet/intel-802.11-modules-7265.ngwg.w-939155-4357719.pdf)
25. [https://www.parts-people.com/index.php?action=item&id=27889](https://www.parts-people.com/index.php?action=item&id=27889)
26. [http://static6.arrow.com/aropdfconversion/513a862ac5f68df7aa2f74216ac36aa37d0fbbf3/pgurl_intel-dual-band-wireless-ac-7265.pdf](http://static6.arrow.com/aropdfconversion/513a862ac5f68df7aa2f74216ac36aa37d0fbbf3/pgurl_intel-dual-band-wireless-ac-7265.pdf)
27. [https://forums.developer.nvidia.com/t/jetson-tx2-nx-and-intel-wifi-ac-8265-unable-to-connect/202454](https://forums.developer.nvidia.com/t/jetson-tx2-nx-and-intel-wifi-ac-8265-unable-to-connect/202454)
28. [https://www.intel.com/content/www/us/en/products/sku/83635/intel-dual-band-wirelessac-7265/downloads.html](https://www.intel.com/content/www/us/en/products/sku/83635/intel-dual-band-wirelessac-7265/downloads.html)
29. [https://www.aliexpress.com/item/1005007180288792.html](https://www.aliexpress.com/item/1005007180288792.html)
30. [https://forum.seeedstudio.com/t/compatible-wifi-module-for-jetson-orin-nx-16gb/274792](https://forum.seeedstudio.com/t/compatible-wifi-module-for-jetson-orin-nx-16gb/274792)
31. [https://jetsonhacks.com/2014/10/12/installing-wireless-intel-7260-adapter-nvidia-jetson-tk1/](https://jetsonhacks.com/2014/10/12/installing-wireless-intel-7260-adapter-nvidia-jetson-tk1/)
32. https://techinfodepot.shoutwiki.com/wiki/Main_Page
33. https://www.youtube.com/watch?v=-dy5SgDQqKU - imp to know mounting the cable , antenna
34. https://fcc.report/FCC-ID/2AVBM-GK5/5728379.pdf - main fcc report on the Intel 7265 unit
35. https://www.intel.com/content/dam/www/public/us/en/documents/product-briefs/dual-band-wireless-ac-7265-brief.pdf
36. https://techinfodepot.shoutwiki.com/wiki/Intel_Dual_Band_Wireless-AC_7265_%287265NGW%29 - important wiki 



The Intel Dual Band Wireless-AC 7265 (Wi-Fi 5 + Bluetooth) is a compact wireless module commonly used in embedded and laptop applications. To connect it to the Boson 22 Carrier Board for Jetson Orin NX, you’ll need to consider both physical form factor and electrical interfaces.
 1. Intel AC 7265 Overview
	- Form Factor: M.2 2230 E-Key (or sometimes NGFF)
	- Interfaces: Wi-Fi: PCIe  Bluetooth: USB
	- Connectors:
		- Two antenna u.FL connectors (for 2.4 GHz and 5 GHz bands)
 2. Components Needed to Connect AC7265 to Boson 22
 - Since Jetson Orin NX itself doesn’t have an integrated Wi-Fi/Bluetooth module, and the Boson 22 carrier board may not have a native M.2 E-Key slot, here’s how to approach it:
	- Required Components:
		- Intel AC7265 Wi-Fi card (M.2 2230)
		- M.2 E-Key to PCIe + USB adapter (if the Boson board lacks a native E-Key slot)
		- PCIe slot or M.2 slot (provided on the Boson 22)
		- USB connection for Bluetooth (usually from carrier board's USB header)

**u.FL Antennas (2x antennas with u.FL connectors)**

**Linux firmware (needed in Jetson OS for proper driver support)**
 
  ### **Connection Steps**

A. Physical Installation
Insert the Intel AC7265 into an M.2 E-Key slot on the Boson 22 board (if available).
If not available, use an M.2 E-Key to mini PCIe or USB/PCIe adapter that can connect to:
PCIe lines for Wi-Fi
USB lines for Bluetooth

B. Connect Antennas
Attach 2x u.FL antennas to the Wi-Fi card for optimal wireless signal.

C. Power & USB Routing
Make sure the USB signal lines from the AC7265 are connected to a USB host port on the carrier board.

Most adapters handle this by routing the USB connection via a separate cable.

Software Setup (Jetson Orin NX)
A. Drivers
The AC7265 is supported under the iwlwifi driver in Linux.
Ensure your Jetson Linux BSP (L4T) includes the relevant firmware:

`bash`
`Copy`
`Edit`
`sudo apt install linux-firmware`
`or manually install:`

`/lib/firmware/iwlwifi-7265D-xx.ucode`

`B. Bluetooth Support`
`Ensure the USB interface is working:`

`bash`
`Copy`
`Edit`
`lsusb | grep -i intel`

Use bluetoothctl and rfkill to manage and test.


[![Connect Tech MSG093 | WDL Systems](https://images.openai.com/thumbnails/5eafcd9d9118fed03bbfadf4cf57fb56.png)](https://www.wdlsystems.com/Connect-Tech-North-America-WIFI-Bluetooth-Antenna)

Certainly! Here's an overview of the components involved in connecting the **Intel AC 7265 wireless module** with the **Connect Tech PAR502 antenna accessory**, including images and descriptions of each component:

---
 1. **Intel AC 7265 Wireless Module**

* **Description**: A dual-band Wi-Fi 5 (802.11ac) and Bluetooth 4.0 M.2 2230 module.
* **Connectors**: Two **U.FL (IPEX MHF4)** antenna connectors labeled **MAIN** and **AUX**.
* 
. **U.FL to RP-SMA Cables**

* **Description**: These pigtail cables connect the U.FL connectors on the wireless module to external RP-SMA antennas.
* **Features**:

  * **U.FL (IPEX MHF4)** connector on one end.
  * **RP-SMA female** bulkhead connector on the other end for panel mounting.
  * Typically available in lengths ranging from 10cm to 50cm.
* **Image**:([Walmart.com][2], [eBay][3])

 3. **Dual-Band Wi-Fi Antennas**

* **Description**: External antennas that support both 2.4 GHz and 5 GHz frequencies, enhancing wireless signal strength and stability.
* **Connection**: Screw onto the RP-SMA connectors mounted on the enclosure.

Mounting Hardware

* **Description**: Hardware used to secure the RP-SMA connectors to the device enclosure, ensuring a stable and durable connection.
* **Components**:
  * Bulkhead nuts and washers for securing the RP-SMA connectors.
  * Optional O-rings for waterproofing and dust protection.

**Assembly Overview**

 **Install the Intel AC 7265 Module**: Insert the module into the M.2 Key E slot on your carrier board (e.g., Boson 22).

**Connect U.FL to RP-SMA Cables**: Attach the U.FL connectors to the MAIN and AUX ports on the wireless module. Route the cables to the desired mounting location on your device enclosure.

**Mount RP-SMA Connectors**: * Drill holes in the enclosure to accommodate the RP-SMA bulkhead connectors. Secure the connectors using the provided nuts and washers.([Data Alliance][4])

 **Attach Antennas** : Screw the dual-band antennas onto the externally mounted RP-SMA connectors.
- **One end**: tiny **U.FL/MHF4** connector for Intel card
- **Other end**: larger **RP-SMA female bulkhead** with nut & washer for mounting

By following this setup, you can effectively integrate the Intel AC 7265 wireless module with external antennas using the Connect Tech PAR502 accessory, enhancing your device's wireless connectivity.

[1]: https://www.newegg.com/youhua-b08g57dd33-bluetootadapter/p/1GK-021R-00269?srsltid=AfmBOoqnlo1H1V-0ifHyanq6dzIFSlUoCgUay-456CvzfXHKsornnLMk&utm_source=chatgpt.com "Bingfu U.FL IPX IPEX MHF4 to RP-SMA Female Bulkhead ... - Newegg"
[2]: https://www.walmart.com/c/kp/m-2-wifi-antenna?utm_source=chatgpt.com "M 2 Wifi Antenna - Walmart"
[3]: https://www.ebay.com/itm/166004283015?utm_source=chatgpt.com "WiFi Antenna Cable U.FL MHF4 to RP-SMA 0.81mm for Intel ... - eBay"
[4]: https://www.data-alliance.net/u-fl-to-rp-sma-female-cable-1-inch-2-3-4-5-6-7-8-9-10-inch-adapter/?utm_source=chatgpt.com "U.FL to RP-SMA-female Cable: 1-inch 2\" 3\" 4\" 5\" 6\" 7\" 8\" 9\" 10-inch ..."

**MHF (Micro High Frequency)** refers to a series of miniature RF (radio frequency) coaxial connectors used to connect internal wireless modules (like Wi-Fi/Bluetooth cards) to external antennas. They’re made by I-PEX (also known as Hirose or IPEX Connectors), and are commonly found on laptop Wi-Fi cards, embedded systems, and modules like the Intel 7265NGW.

|Connector|Typical Use|Size|Common Devices|
|---|---|---|---|
|**MHF (MHF1)**|Older Wi-Fi cards|~2.5 mm|Legacy mini PCIe cards|
|**MHF2**|Less common variant|~2.0 mm|IoT modules|
|**MHF3**|Rare|~1.9 mm|Compact modules|
|**MHF4**|Modern standard|~1.2 mm|M.2 Wi-Fi cards like Intel AC 7265NGW|
|**MHF4L**|Slightly enhanced MHF4|Same|Some newer modules (backward compatible)|
- These terms are often used interchangeably in product listings, but here's the reality:
- U.FL is a brand name from Hirose (the original standard).
- MHF is the I-PEX equivalent.
- IPX / IPEX are commonly used in the industry to describe similar micro-coaxial connectors.
- So when you see U.FL / IPX / IPEX / MHF4, they often refer to the same type of connector, particularly when talking about modern Wi-Fi modules like the Intel 7265NGW.

The **Intel® Dual Band Wireless-AC 7265** (model **7265NGW**) utilizes **MHF4** connectors for its antenna interfaces. This is explicitly stated in Intel's External Product Specification (EPS) for the device:[mini-box.com+3WikiDevi.Wi-Cat.RU+3mfactors.com+3](https://wikidevi.wi-cat.ru/Intel_Dual_Band_Wireless-AC_7265_%287265NGW%29?utm_source=chatgpt.com)[FCC Report](https://fcc.report/FCC-ID/2AVBM-GK5/5728379.pdf?utm_source=chatgpt.com)

> “An M.2 compatible RF micro coax type connector (like I-PEX MHF4 connector) is used on the Stone Peak hardware.” [FCC Report](https://fcc.report/FCC-ID/2AVBM-GK5/5728379.pdf?utm_source=chatgpt.com)

These MHF4 connectors are designed for high-frequency applications and are commonly used in compact wireless modules due to their small size.

For detailed specifications and mechanical drawings, you can refer to the full EPS document available through the FCC's database:

- [Intel® Dual Band Wireless-AC 7265 - FCC Report (PDF)](https://fcc.report/FCC-ID/2AVBM-GK5/5728379.pdf)

Additionally, community discussions and technical wikis corroborate this information:
- [Intel Community Forum Discussion on Antenna Connector Type](https://community.intel.com/t5/Wireless/Intel-Dual-Band-Wireless-AC-7265-antenna-connector-type/td-p/506128)
- [TechInfoDepot Wiki on Intel 7265NGW](https://techinfodepot.shoutwiki.com/wiki/Intel_Dual_Band_Wireless-AC_7265_%287265NGW%29)

When sourcing antenna cables or adapters for the 7265NGW module, ensure they are compatible with **MHF4** connectors to guarantee proper fit and performance.


---

### MAVLink Router and MAVproxy
### **MAVLink Router**

Primarily used to **route MAVLink messages** between multiple endpoints (e.g., from a drone to ground station, companion computer, etc.)

- **Efficient message forwarding** with low overhead
- Routes messages between multiple interfaces (e.g., serial, UDP, TCP)
- Supports filtering (e.g., only forward specific messages)
- Lightweight and fast – ideal for onboard companion computers
- Often used with **PX4** and **ArduPilot**

 A drone's flight controller sends telemetry via serial to a Raspberry Pi running MAVLink Router, which forwards it to multiple ground stations over Wi-Fi (UDP).
### **MAVProxy**


A **command-line ground control station** and development tool for ArduPilot systems. Also routes messages but with **interactive control and scripting**.

- Modular, with plugins for many functions
- Allows command/control of vehicle via CLI
- Supports routing to multiple endpoints
- Python-based and scriptable
- Good for debugging and testing

A developer uses MAVProxy on a laptop to connect to a drone over telemetry radio, sends commands via CLI, and logs telemetry data.

**Pros:**

- Powerful CLI interface
- Highly customizable with Python plugins
- Useful for development, debugging, and automation

**Cons:**

- Heavier than MAVLink Router
- More complex, less suited to production unless scripted carefully



Raspbi pi - always have separate power from rest of the computer  
Depending on the load of companion computer  - it consumes power 
-https://discuss.ardupilot.org/t/power-raspberry-pi-5-and-drone-from-lipo-battery/127236

https://discuss.ardupilot.org/t/stable-power-supply-5v-5a-for-raspberry-pi-on-your-drone/44277/3

![[Pasted image 20250509082329.png]] 

-https://discuss.px4.io/t/best-way-to-power-my-companion-computer/27131

Logic level Shifter - https://www.instructables.com/A-Quick-Guide-on-Logic-Level-Shifting/ 
Normally if you have a 3.3V device sending signals to a 5V device you will not have any problems, so even though the 3.3V device will only measure at 3.3V when set to HIGH, this is normally over the threshold of what a 5V device considered HIGH.

Pixhawk - wiring standards: https://github.com/pixhawk/Pixhawk-Standards/blob/master/DS-009%20Pixhawk%20Connector%20Standard.pdf 

6C - Rasp pi - problems 
- https://discuss.px4.io/t/problems-connecting-a-pixhawk-6c-to-a-raspberry-pi/32318
- https://discuss.px4.io/t/controlling-pixhawk-6c-with-raspberry-pi-4b/30712/2
- https://discuss.px4.io/t/control-pixhawk4-using-telemetry-and-raspberry-pi/25421/5 - MAVSDK
- https://discuss.px4.io/t/telemetry-configuration-for-companion-computer/33027 - Telem Config 
- https://ardupilot.org/dev/docs/raspberry-pi-via-mavlink.html
- https://discuss.ardupilot.org/t/pixhawk-6c-to-rpi-4-connection/104768/15
- https://pure.tue.nl/ws/portalfiles/portal/342361930/1426591_BEP_Controlling_a_drone_with_Pixhawk_6c_in_Simulink.pdf
- https://diydrones.com/forum/topics/pixhawk-raspberry-pi
 - https://www.3dxr.co.uk/downloads/1612816175UBEC3A2-6S.pdf
 - https://www.reddit.com/r/Traxxas/comments/149jctl/wiring_a_2battery_vehicle_with_a_hobbywing_bec/
 - Rasp pi - ethernet cable  - https://www.circuitbasics.com/how-to-connect-to-a-raspberry-pi-directly-with-an-ethernet-cable/ 

Pi connect lite - https://www.docs.rpanion.com/products/pi-connect-lite

IMP link - wires - https://trampaboards.com/cable-kits-c-1040.html

Check - https://viflydrone.com/
https://diysolarforum.com/threads/which-goes-first-fuse-or-switch.27070/ .- read

RAsp pi - Evaluate setup 
 - Pixhawk and Rasp pi have Tx/Rx logic level compatibility
 - Enable / reboot Raspi pi  and install mavproxy 
 - Pixhawk is connected to **`/dev/serial0`** (UART on Pi):
 - Connect Mavproxy   --> `sudo mavproxy.py --master=/dev/serial0 --baudrate 57600 --aircraft MyCopter`
 - Note -->Different command for USB 
```
  ls /dev/serial*
```
 - Then  Mavproxy should start showing the details  
 - <span style="color:rgb(0, 176, 80)">MavProxy can output a mavlink stream to remote network addresses using UDP Broadcast. </span>
 - To ensure recieveing MAVlink messages - `watch -n1 "grep -i heartbeat ~/.mavproxy/MyCopter/logs/*"` 
 - Commands
 `mode GUIDED` 
 `arm throttle` 
 `status`
 `param show`

Only communication via Rasp pi - USB 4G stick 
https://ardupilot.org/mavproxy/docs/getting_started/quickstart.html 
**While MAVProxy also has the capability of forwarding using TCP, it is not recommended, since network delays can cause long lags if joystick control is being used.** 
https://ardupilot.org/mavproxy/docs/getting_started/starting.html
 Companion Computer Peripherals 
https://docs.px4.io/main/en/companion_computer/companion_computer_peripherals.html#ftdi-devices
Check - https://www.youtube.com/watch?v=5OIjKTgwNe0 

https://docs.px4.io/main/en/peripherals/mavlink_peripherals.html#telem2
---



### 5g summer school test  - Analysis and Questions - Potential direction within AirMetro 

**Initial Points**
 - Evaluate 5G Campus network performance - Comparison to Public 5G 
 - Compare DronC2om project 
 -  Diff Public/Private/campus network 
 - Null Hypothesis - What's based on 
 - Setup - Rand S Scanners  | Multiple SIMs - Can Barometric GPS tools - correlate signal strength 
 - Data Evaluation Plan - Statistical analysis, Confidence interval, Variance modeling 
 - SINR  , throughput (What'S threshold - follow regulations)
 - Weather , environment - network reliability - to be explored
 - Campus Network take over - hard /soft - If hard - Link loss triggered? 
-  What's ground verification truth - geo tagging 
- IP changes , session resilience, Cell IDs - timestamping
- R and D scanners  (Non intrusive measurements) -  https://www.rohde-schwarz.com/de/produkte/messtechnik/netzwerkdatenerfassung/rs-tsmx-scanner-fuer-drive-und-walk-tests_63493-526400.html 
	-  network scanners passively collect data over the air, providing unbiased and accurate insights into RF performance and MIB/SIB/Layer 3 messages for the most common technologies without requiring subscription to network services.
	- **Carrier-Grade NAT (CGNAT)** or dynamic IP pools.
	- Protocols used -  (Advanced - **QUIC**, **Multipath TCP**, or **SD-WAN**)
---

CNS cluster presentation 
- 5 slide 
- CNS - Intro 
	- technological corridor 
	- AAM - CNS - 3 challenges - 
	- Topics 

- C
	- AAM - reliable resilient communication 
	- T2 , T9 - logical and physical aspects of the communication technology 
	- ICAO = Availability, Integrity, Continuity and Transaction Time 
	- Multi-link (Wi-Fi, 5g, Satellite)
	- Availability and Continuity - physical 
- N
	- Absolute and Relative Nav 
	- GNSS vulnerabilities 
	- Multi-Modal Navigation:  enhancing  the availability with redundant systems ( additional tools )
	- quick reactive system - on-board system  - fusing data from different sensors
	- dependent on Ground infrastructure - impractical 
	- communication - region aware map dependencies 
- S
	- Software - Modeling 
	- digital twin 
	- UAV - monitor /behavior , position 
	- Support Simulation before flight 
- Outcome / deliverable / hardware 


----


Todos: 
- [ ] Setup MAVlink router - UDP connection 
- [ ] Configure - Huawei LTE with Rasp 
- [ ] Test with Mavproxy - Log files 
- [ ] Then move to ROS 
- [ ] Learn Barometer , magnetometer, EKF2 ,
- [ ] PWM power 


---
Qgc - VM Windows 



---

### Rasp pi  - LTE connection 

Steps 
- USB dongle functioning in Rasp pi 
- Now we do Pixhawk talk MAVLink via LTE with QGC
- https://www.technotrade.com.ua/userfiles/files/Huawei-E3372-user-guide.pdf?srsltid=AfmBOop2DTFBaNL7vCwPg1s31YJ5N_MTZmdKJaWTCRJ5GAuG7_WWbleN
- https://www.usermanuals.au/huawei/e3372/manual?p=3
- https://bellergy.com/3-installing-4g-usb-modem-to-raspberry-pi/
- Check Data plans
 Configure Pixhawk Serial Port for MAVLink - - `SERIAL2_PROTOCOL = 2` (MAVLink 2)
- `SERIAL2_BAUD = 921` (921600 baud, or set to 57600 for PX4 if needed)
- - - Go to “Interfacing Options” → “Serial”.
    - Disable shell over serial, enable serial hardware.
- Reboot the Pi.
- The UART will be available at `/dev/serial0` or `/dev/ttyAMA0`


- Most LTE dongles work as USB network devices or modems.
    
- Install required packages:
    
    text
    
    `sudo apt-get update sudo apt-get install usb-modeswitch wvdial`
    
- Configure `wvdial` or use `NetworkManager` to connect to the internet via LTE.  
    Confirm connection with:
    
    text
    
    `ifconfig ping -c 4 8.8.8.8`
    
    The LTE modem will usually show up as `wwan0` or similar[5](https://forums.raspberrypi.com/viewtopic.php?t=302262)[6](https://www.wevolver.com/article/add-cellular-connectivity-to-your-raspberry-pi)[4](https://developers.soracom.io/en/start/connect/raspberry-pi).
    

## 5. Install MAVLink Routing Software

- Install MAVProxy (or use `mavlink-router` for more advanced routing):
    
    text
    
    `sudo apt-get install python3-pip sudo pip3 install mavproxy`
    
- Start MAVProxy to connect to Pixhawk:
    
    text
    
    `sudo mavproxy.py --master=/dev/serial0 --baudrate=921600 --out=udp:QGC_IP:14550`
    
    Replace `QGC_IP` with the public IP of your QGroundControl computer, or use a VPN/port forwarding if behind NAT[7](https://docs.px4.io/main/en/companion_computer/pixhawk_rpi.html)[2](https://hagerstefan.de/raspi/raspipixhawk/index.php).
    

## 6. Configure QGroundControl

- On your ground station, set QGroundControl to listen for UDP packets on port 14550 (default).
- If using a VPN or port forwarding, ensure the port is open and forwarded to your ground station.

- https://www.jeffgeerling.com/blog/2022/using-4g-lte-wireless-modems-on-raspberry-pi
- https://forums.raspberrypi.com/viewtopic.php?t=159344
- https://www.thefanclub.co.za/how-to/how-setup-usb-3g-modem-raspberry-pi-using-usbmodeswitch-and-wvdial
- https://forums.raspberrypi.com/viewtopic.php?t=101582
## **LTE Dongle Configuration (Huawei E3372)**

- The E3372 in _HiLink (router) mode_ is plug-and-play on Raspberry Pi OS; it presents itself as a USB Ethernet adapter (e.g., `eth1`), providing a local IP (usually 192.168.8.x)[3](https://bellergy.com/3-installing-4g-usb-modem-to-raspberry-pi/)[4](https://forums.raspberrypi.com/viewtopic.php?t=313520)[2](https://forums.raspberrypi.com/viewtopic.php?t=159344).
    
- No need for `wvdial` or PPP; just plug it in and check with:
    
    text
    
    `lsusb | grep Huawei ifconfig`
    
    You should see a new interface (often `eth1`), and you’ll have internet access if the SIM is active[3](https://bellergy.com/3-installing-4g-usb-modem-to-raspberry-pi/)[4](https://forums.raspberrypi.com/viewtopic.php?t=313520).
    
- If you don’t see the interface, install:
    
    text
    
    `sudo apt-get install usb-modeswitch usb-modeswitch-data`
    
    and reboot
https://unix.stackexchange.com/questions/159086/difference-between-ppp0-vs-wwan0
https://unix.stackexchange.com/questions/213663/huawei-e3372s-linux-rasbian-incoming-connections-problem

https://github.com/alireza787b/mavlink-anywhere 
https://www.youtube.com/watch?v=WoRce4Re3Wg

https://www.youtube.com/watch?v=5OIjKTgwNe0
https://ardupilot.org/mavproxy/docs/getting_started/quickstart.html#over-network
https://www.youtube.com/watch?v=DGAB34fJQFc
https://www.docs.rpanion.com/software/rpanion-server
https://discuss.ardupilot.org/t/unlimited-range-hd-streaming-with-lte/48670/15
https://discuss.px4.io/t/4g-telemetry-for-pixhawk/1548/16
https://stackoverflow.com/questions/42557913/connecting-with-huawei-e3372-on-raspberrypi
---

- https://www.jeffgeerling.com/blog/2022/network-interface-routing-priority-on-raspberry-pi
- https://developers.soracom.io/en/start/connect/raspberry-pi/
- https://discuss.ardupilot.org/t/connect-pixhawk-to-raspberry-and-control-it-with-4g-lte/42366/8
- https://docs.uavmatrix.com/docs/5.x/quick-start/
- https://discuss.ardupilot.org/t/mavlink-routing-with-a-router-software/82138
- https://ardupilot.org/dev/docs/raspberry-pi-via-mavlink.html
---
## **Not Identifying the Correct Network Interface**

- The E3372 can appear as different interfaces depending on its mode (HiLink, Stick, or PPP). It may show up as `wwan0`, `usb0`, `eth1`, or `ppp0`[1](https://www.jeffgeerling.com/blog/2022/using-4g-lte-wireless-modems-on-raspberry-pi)[2](https://forums.raspberrypi.com/viewtopic.php?t=205540)[3](https://forums.raspberrypi.com/viewtopic.php?t=231239)[4](https://stackoverflow.com/questions/58660837/no-connection-with-huawei-e3372-on-raspberry-pi-4).
- Always use `ifconfig` or `ip a` to confirm which interface is created by the dongle. Using the wrong interface will prevent internet access or routing[1](https://www.jeffgeerling.com/blog/2022/using-4g-lte-wireless-modems-on-raspberry-pi)[2](https://forums.raspberrypi.com/viewtopic.php?t=205540).
    

## **2. Missing or Incorrect Default Gateway**

- If the Pi does not set the LTE dongle’s interface as the default gateway, traffic will not route through the LTE connection[5](https://raspberrypi.stackexchange.com/questions/50050/4g-dongle-internet-connection-problem)[6](https://dietpi.com/forum/t/no-internet-connection/6263).

- For HiLink mode, the gateway is usually `192.168.8.1`. Failing to set this as the default gateway (e.g., using `sudo route add default gw 192.168.8.1`) results in “no route to host” errors[5](https://raspberrypi.stackexchange.com/questions/50050/4g-dongle-internet-connection-problem)[6](https://dietpi.com/forum/t/no-internet-connection/6263).
    

## **3. Overlapping or Conflicting Routes**

- If multiple interfaces (e.g., `eth0`, `wlan0`, `wwan0`) are active, the Pi may route traffic through the wrong interface.
- Check the routing table (`route -n` or `ip route`) and ensure the LTE interface has the default route if it should handle all outbound traffic[5](https://raspberrypi.stackexchange.com/questions/50050/4g-dongle-internet-connection-problem).
    

## **4. Power Supply Issues**

- The E3372 can draw significant current, especially during connection bursts. Underpowered Pi or unpowered USB hubs can cause the modem to disconnect or hang[5](https://raspberrypi.stackexchange.com/questions/50050/4g-dongle-internet-connection-problem).
- Use a reliable 2A+ power supply and, if needed, a powered USB hub[5](https://raspberrypi.stackexchange.com/questions/50050/4g-dongle-internet-connection-problem).
    

## **5. Driver and Mode Mismatch**

- The E3372 can operate in different modes (HiLink/CDC_Ether, Stick/QMI, PPP). Not switching to the correct mode or missing drivers can leave the device unusable[1](https://www.jeffgeerling.com/blog/2022/using-4g-lte-wireless-modems-on-raspberry-pi)[4](https://stackoverflow.com/questions/58660837/no-connection-with-huawei-e3372-on-raspberry-pi-4)[7](https://raspberrypi.stackexchange.com/questions/79272/problems-with-huawei-e3372-usb-modem-with-raspberry-pi-3).
- Use `usb-modeswitch` to ensure the dongle is in the desired mode and confirm with `lsusb`[7](https://raspberrypi.stackexchange.com/questions/79272/problems-with-huawei-e3372-usb-modem-with-raspberry-pi-3).
    

## **6. Incorrect or Missing DNS Configuration**

- If DNS is not set up, you may have an IP connection but be unable to resolve domain names. Ensure your Pi receives DNS settings from the dongle or set them manually in `/etc/resolv.conf`[4](https://stackoverflow.com/questions/58660837/no-connection-with-huawei-e3372-on-raspberry-pi-4).
    

## **7. Overriding `/etc/network/interfaces` or Network Manager Conflicts**

- Auto-generated or manual entries in `/etc/network/interfaces` can override or conflict with DHCP or Network Manager, leading to wrong gateway or DNS settings[6](https://dietpi.com/forum/t/no-internet-connection/6263).
- Avoid manual edits unless necessary, and prefer using Network Manager for broadband connections[4](https://stackoverflow.com/questions/58660837/no-connection-with-huawei-e3372-on-raspberry-pi-4).
    

## **8. Not Checking Dongle Status or Connection**

- The E3372’s web interface (usually at 192.168.8.1) can show connection status. Not checking this can lead to troubleshooting the Pi when the issue is with the SIM, network, or dongle[5](https://raspberrypi.stackexchange.com/questions/50050/4g-dongle-internet-connection-problem).
    

## **Summary Table**
|                               |                                                  |
| ----------------------------- | ------------------------------------------------ |
| Mistake                       | Consequence                                      |
| Wrong interface selected      | No internet or routing failures                  |
| Missing default gateway       | â€œNo route to hostâ€, no outbound connectivity |
| Routing conflicts             | Unpredictable internet routing                   |
| Underpowered USB/dongle       | Dongle disconnects, hangs, or is not detected    |
| Wrong dongle mode             | Dongle not usable or not recognized              |
| No/incorrect DNS              | Canâ€™t resolve domain names                     |
| Manual/etc/network/interfaces | Gateway/DNS conflicts, loss of connectivity      |
| Ignoring dongle status        | Troubleshooting wrong layer of the stack         |
https://www.youtube.com/watch?v=MKKB79H1tzQ
https://www.youtube.com/watch?v=z0XgOtg_0ic


---
Points for Panel 
- Opening slides + statement 
- How the talks before inspire the points of discussion 

Panel 1
- Safety from different domain perspectives 
- Sky highways feasibility - economy vs safety
- Priorities and levels of safety
- How safety concerns are linked to each other 
(keep discussions brisk)

Panel 2
- On Site experiments
- Regulations, certification 
- BVLOS

Panel 3
- Interdependence of drone aerodynamics and drone fleets
- What else can influence energy efficiency other than aerodynamics 
- What factors affect energy efficiency and economics of drone fleets
- When to use fleets ? What criteria to be used for deciding ? (Tech, money)


---
### Student Computer 

General specification 
- 16Gb RAM 
- 1Tb SSD
- i7 | Ryzen 5 
- Suitable Linux OS 
- GPU - Check Gazebo requirements 


---

### Connectors 

# Harrisen GH 1.25 mm to Dupont 2.54 mm JST Connector Kit, 2/3/4/5/6/7/8/9/10/12 GH 1.25 mm to 2.54 mm Dupont 28AWG Cable for Pixhawk 6C 6X 
https://www.mattmillman.com/info/crimpconnectors/common-jst-connector-types/
 **Yes — but only for low-current signal connections (UART/TELEM, I²C, GPS, etc.).** It’s commonly used to adapt Pixhawk’s JST-GH (1.25 mm) ports to standard 0.1″ (2.54 mm) Dupont pins that you can plug into a Raspberry Pi header — but you must verify pinout, voltage and current requirements first. ([docs.holybro.com](https://docs.holybro.com/autopilot/pixhawk-6c-mini/pixhawk-6c-mini-ports?utm_source=chatgpt.com "Pixhawk 6C Mini Ports"))

Why that is:

- **Connector pitch matches the kit purpose.** Recent Pixhawk/Cube family boards expose many ports as **JST-GH 1.25 mm** (I²C, TELEM, GPS, CAN, etc.), and Raspberry Pi GPIO/headers use **2.54 mm (0.1")** pitch — the adapter cable you described exactly converts between those. ([docs.holybro.com](https://docs.holybro.com/autopilot/pixhawk-6c-mini/pixhawk-6c-mini-ports?utm_source=chatgpt.com "Pixhawk 6C Mini Ports"))
- **Signal voltage:** Pixhawk I/O and Raspberry Pi GPIO are typically **3.3 V logic**, so direct connections for data lines (UART, I²C, GPIO) are usually safe. **Still confirm the specific Pixhawk port’s voltage** (some power pins provide 5 V or regulated power outputs). The Cube/Pixhawk docs list port voltages (VCC_5V, 3.3 V, GND) for each JST port — check the port you intend to use. ([docs.cubepilot.org](https://docs.cubepilot.org/user-guides/carrier-boards/cube-red-standard-carrier-board-pinout?utm_source=chatgpt.com "Cube Red Standard Carrier Board Pinout"))
- **Wire gauge / current:** The kit’s **28 AWG** is fine for signals and short low-current sensor power (small sensors, GPS, serial modules). **It is not suitable for high currents** (motors, ESC power, servos under heavy load). Typical safe continuous current for 28 AWG in hobby wiring is on the order of a few hundred milliamps to ~1 A depending on insulation/conditions — don’t use it to carry sustained high current. ([Wikipedia](https://en.wikipedia.org/wiki/American_wire_gauge?utm_source=chatgpt.com "American wire gauge"))

Practical checklist before you connect:

1. **Identify the exact Pixhawk port** (e.g., TELEM1, I2C, GPS) and read that port’s pinout/voltages in the Pixhawk/Cube documentation. ([docs.cubepilot.org](https://docs.cubepilot.org/user-guides/carrier-boards/cube-red-standard-carrier-board-pinout?utm_source=chatgpt.com "Cube Red Standard Carrier Board Pinout"))
2. **Match pins** — confirm order (VCC, TX, RX, GND or SDA, SCL, VCC, GND). Don’t assume the adapter’s wire order is the same as the port order. Use a multimeter or continuity tester if unsure.
3. **Never connect 5 V to a Pi GPIO pin.** If the Pixhawk port supplies 5 V on VCC, either do not connect VCC to the Pi or ensure the Pi pin you’re connecting to is a 5 V input (rare) — otherwise power only GND and data lines, or use proper power routing. ([docs.cubepilot.org](https://docs.cubepilot.org/user-guides/carrier-boards/cube-red-standard-carrier-board-pinout?utm_source=chatgpt.com "Cube Red Standard Carrier Board Pinout"))
4. **Use level shifting if voltages differ.** For any port that runs at a higher voltage than 3.3 V, use a level shifter or opto/isolation as appropriate.
5. **Avoid powering the Pi or Pixhawk through thin 28 AWG wires** for anything other than tiny current draws — use the board’s recommended power connections for supply lines to avoid voltage drop/overheating. ([smartechcables.com](https://www.smartechcables.com/blog/24awg-vs-26awg-vs-28awg/?srsltid=AfmBOopct4X3jg_NGmO-hxOuB5HlH4AjYQ60d3t8oLXcx29ck7Iep5gi&utm_source=chatgpt.com "Ethernet Cable Gauge: 24 vs 26 vs 28 AWG"))
6. **Test with small steps** — connect GND first, then signal lines, check communication, then only connect power if safe.

If you tell me which **exact Pixhawk model/port** (e.g., Pixhawk 6C TELEM2, Cube Orange I2C) and **what you want to connect to the Pi** (I²C sensor, GPS, serial telemetry, etc.), I can give a precise wiring map and highlight any power/level-shifter precautions.

---
The antenna is always a male 
Wifi antenna we have a indentation so its RP-SMA
female to male MHF4 - RP-SMA cable 

LTE has protruding antenna - SMA male 
