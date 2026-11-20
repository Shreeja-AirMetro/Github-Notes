### UAV G Paper

Abstract: ![[UAV_G_2025-Abstract.pdf]]
Meeting 3/4

- Plan for Paper - 6-8 pages
- 1-2 pages - extended abstract
- Goal of paper: BVLOS flight with multi-modal navigation (comm is the backbone supporting aspect)
- We focus on integration in one UAV - can be spanned to larger number by communication -
- Q: what| How the messaging looks like

Multi-modal Navigation
1- traditional GNSS is not “accurate enough” for BVLOS Low altitude flights
2- contradictory thema - Use LiDAR and Camera (Day and night) BVLOS
3- Methods - how to chase Hardware?
4- How to setup for better results
5- How to setup (statically) and anticipate/ handle dynamic drift while flying (calibration - Spatial , temporal with IMU sensors) - create same datastructure for all the sensor , not as overlap (as kitty, schamurrza team ) but
6- build map - visualize (octomap)
7- augmentation and visualization algorithm - top layer
8- conclusion and future works

- How to Choose and calibrate Hw
- Use octo map as base for Augmentation and visualization
- How backbone comm can support single UAV - multiple UAV is a zone
---
 ### **LiDAR - Point Clouds**
- Objects comes in cubes . then traverse through the cubes (occupying cube) with information
- Pointcloud - octtree behind (class - float , info (integer) or so
- Use data set - with semantic information like color - computing intensive

- what is ROS Noetic - to generate OctoMap?

Lear the basics:

Whats octomap
- OctoMap is a probabilistic 3D mapping framework that uses an **octree data structure** to represent occupied, free, and unknown space in volumetric environments. It recursively subdivides 3D space into octants, enabling memory-efficient storage and multi-resolution queries while dynamically expanding or pruning nodes as needed
- [https://github.com/balloon61/Drone-Navigation-with-Octomap](https://github.com/balloon61/Drone-Navigation-with-Octomap) | [https://www.youtube.com/watch?v=W1sos9TLVeg](https://www.youtube.com/watch?v=W1sos9TLVeg)
- the sensors - probabilistic occupancy updates - considering sensor noise and dynamic changes
- we use ROS - integrated navigation protocol stacks
- Semantic mapping - having labelled map (building, trees) - enable complex 3D environment

UAV Navigation - Octomap and 5G
- Octomap updates to ground station/edge server in real time - need data compression?
- RTK over 5G (Ref 3GPP correction data - document)
- Observed time difference of arrival - use 5G BS signals with IMU sensors to resolve NLOS - reduce LiDAR drifts
- Network slicing for prioritized connectivity
- future - Edge computing | Regression based Data compression techniques



- Where Octomap created? Companion computer?

Validation metrics- (bandwidth- latency - packet loss)

Time sensitivity of the map?`

- Network slicing - traffic

### To Learn: 

- USRDC - ROS DDS, Gazebo
- XRCE- DDS
- octo map - octo tree
- FEM - adaptive /dynamic discretization

1- [https://www.mdpi.com/2504-446X/9/3/194](https://www.mdpi.com/2504-446X/9/3/194
2- [https://www.mdpi.com/2504-446X/7/4/278](https://www.mdpi.com/2504-446X/7/4/278)
3- [https://www.thedroningcompany.com/blog/5g-connectivity-and-drones](https://www.thedroningcompany.com/blog/5g-connectivity-and-drones)
4- [https://bettstetter.com/edge-drones/](https://bettstetter.com/edge-drones/)
5- [https://www.gsma.com/get-involved/gsma-foundry/wp-content/uploads/2024/07/Updated-Foundry-Case-Study-The-role-of-5G-networks-and-UAVs.pdf](https://www.gsma.com/get-involved/gsma-foundry/wp-content/uploads/2024/07/Updated-Foundry-Case-Study-The-role-of-5G-networks-and-UAVs.pdf)
6- [https://docs.px4.io/v1.15/en/flight_controller/airlink.html](https://docs.px4.io/v1.15/en/flight_controller/airlink.html)
7 - [https://5gdrones.eu/wp-content/uploads/2020/06/D1_5_Description-of-the-5G-trial-facilities-and-use-case-mapping-v2.pdf](https://5gdrones.eu/wp-content/uploads/2020/06/D1_5_Description-of-the-5G-trial-facilities-and-use-case-mapping-v2.pdf) | [https://5gdrones.eu/wp-content/uploads/2022/01/D4.2-Integration-status-and-updated-integration-plan.pdf](https://5gdrones.eu/wp-content/uploads/2022/01/D4.2-Integration-status-and-updated-integration-plan.pdf) | [https://5gdrones.eu/](https://5gdrones.eu/)
8- [https://arxiv.org/pdf/2503.19613](https://arxiv.org/pdf/2503.19613)
9- [https://github.com/ctu-mrs/mrs_octomap_planner](https://github.com/ctu-mrs/mrs_octomap_planner)
10 - [https://advexure.com/blogs/news/the-role-of-5g-in-expanding-drone-capabilities](https://advexure.com/blogs/news/the-role-of-5g-in-expanding-drone-capabilities)
11- [https://dspace.lib.cranfield.ac.uk/server/api/core/bitstreams/98c7647e-228b-4d9e-913b-243abd5401ed/content](https://dspace.lib.cranfield.ac.uk/server/api/core/bitstreams/98c7647e-228b-4d9e-913b-243abd5401ed/content)
12- [https://pmc.ncbi.nlm.nih.gov/articles/PMC6777497/pdf/ROB-36-734.pdf](https://pmc.ncbi.nlm.nih.gov/articles/PMC6777497/pdf/ROB-36-734.pdf)
13- [https://www.gsma.com/solutions-and-impact/industries/smart-mobility/wp-content/uploads/2023/01/Foundry-Case-Study-Commercial-Drone-Scale-v7-1.pdf](https://www.gsma.com/solutions-and-impact/industries/smart-mobility/wp-content/uploads/2023/01/Foundry-Case-Study-Commercial-Drone-Scale-v7-1.pdf) (Ericson - 5G technology as the Backbone for Commercial Drone Usage)
14 - [https://www.ericsson.com/en/cases/2021/long-distant-flights-for-autonomous-drones](https://www.ericsson.com/en/cases/2021/long-distant-flights-for-autonomous-drones)
15 - [https://www.ericsson.com/en/blog/2020/11/unmanned-drones-beyond-line-of-sight-challenges](https://www.ericsson.com/en/blog/2020/11/unmanned-drones-beyond-line-of-sight-challenges)
16 -[https://www.ericsson.com/en/blog/2020/6/network-exposure-and-the-case-for-connected-drones](https://www.ericsson.com/en/blog/2020/6/network-exposure-and-the-case-for-connected-drones)
17 - [https://www.vodafone.com/news/services/vodafone-ericsson-safe-passage-drones](https://www.vodafone.com/news/services/vodafone-ericsson-safe-passage-drones)
18 - [https://5g-ppp.eu/](https://5g-ppp.eu/)</span></span>
 - GOF 2.0
- ROS - Octomap _server

Align point clouds - using TF transforms for accurate map creations

- Volume and dynamic updates

[https://5gdrones.eu/wp-content/uploads/2020/06/D1_5_Description-of-the-5G-trial-facilities-and-use-case-mapping-v2.pdf](https://5gdrones.eu/wp-content/uploads/2020/06/D1_5_Description-of-the-5G-trial-facilities-and-use-case-mapping-v2.pdf)

[https://github.com/Taeyoung96/OctoMap-ROS2?tab=readme-ov-file](https://github.com/Taeyoung96/OctoMap-ROS2?tab=readme-ov-file)

[https://github.com/5G-ERA/signalQualityNetworkApplicationRos2](https://github.com/5G-ERA/signalQualityNetworkApplicationRos2)

OctoMap in ROS 2 enables drones to build and update **3D occupancy maps** in real time using LiDAR/camera data, while 5G/WiFi communication ensures low-latency data transfer for dynamic mapping and control. Here’s how they work together:

---

### **1. OctoMap in ROS 2: Core Functions**

- **Real-Time 3D Mapping**
    - Processes `sensor_msgs/PointCloud2` data from LiDAR or depth cameras into probabilistic 3D voxel maps using an octree structure[1][3].
    - Integrates with ROS 2 nodes like `octomap_server` to publish maps for path planning and collision avoidance[3].
- **Multi-Resolution Flexibility**
    - Adjusts voxel resolution dynamically (e.g., 0.1 m near obstacles, 1 m for distant regions) to balance detail and computational load[6].
- **2D/3D Map Conversion**
    - Tools like `Map-Conversion-3D-Voxel-Map-to-2D-Occupancy-Map` project OctoMap data into 2D grids for ground robots or hybrid UAV/UGV teams[2].

**2. 5G/WiFi Communication Roles**

**5G Contributions**

- **Low-Latency Sensor Streaming**
    - 5G’s <10 ms latency enables real-time transmission of LiDAR point clouds (∼50 MB/s) to edge servers for OctoMap updates[4][5].
    - Network slicing prioritizes OctoMap traffic over non-critical data (e.g., video feeds)[4].
- **Edge Offloading**
    - Offloads GPU-intensive tasks like raycasting to 5G-connected edge nodes, reducing onboard compute by 40%[5][6].
- **High-Precision Positioning**
    - 5G NR OTDOA enhances SLAM accuracy (<1 m error), critical for aligning OctoMap with the drone’s pose[6].

**WiFi Fallback**

- Provides local connectivity in environments without 5G coverage, though with higher latency (∼50–100 ms)[7].

**3. Integrated Workflow Example**

1. **Data Acquisition**: Drone captures LiDAR scans and depth images.
2. **ROS 2 Processing**: `octomap_server` fuses sensor data into a 3D OctoMap[3].
3. **5G Transmission**: Map updates sent to an edge server for trajectory planning via `mrs_octomap_planner`[1][5].
4. **Action Execution**: Optimized paths are relayed back to the drone over 5G/WiFi.


**4. Use Cases**

- **Search and Rescue**: 5G-enabled OctoMap sharing across drones improves collaborative mapping in GPS-denied areas[5].
- **Infrastructure Inspection**: Live 3D maps streamed via 5G allow remote operators to validate structural integrity[6].

**Key Research**

- The **5G!Drones EU project** validated OctoMap’s integration with 5G for industrial inspections, achieving 100 Mbps throughput and <30 ms latency[5].
- **Network Digital Twin (NDT)** frameworks use 5G to synchronize OctoMap with real-time network conditions, improving energy efficiency in robotic navigation[6].

By combining ROS 2’s modular mapping with 5G/WiFi’s speed and reliability, drones achieve robust autonomy in complex environments.

Citations: 
[1] [https://robotics.stackexchange.com/questions/70435/octomap-slam-path-planning-how-does-it-all-fit-together](https://robotics.stackexchange.com/questions/70435/octomap-slam-path-planning-how-does-it-all-fit-together) 
[2] [https://github.com/LTU-RAI/Map-Conversion-3D-Voxel-Map-to-2D-Occupancy-Map](https://github.com/LTU-RAI/Map-Conversion-3D-Voxel-Map-to-2D-Occupancy-Map) 
[3] [https://robotics.stackexchange.com/questions/103089/octomap-ros-on-ros-2-humble](https://robotics.stackexchange.com/questions/103089/octomap-ros-on-ros-2-humble) 
[4] [https://discourse.ros.org/t/ros-2-native-5g-support-from-ericsson-and-eprosima/17705](https://discourse.ros.org/t/ros-2-native-5g-support-from-ericsson-and-eprosima/17705) 
[5] [https://5gdrones.eu/wp-content/uploads/2020/06/D1_5_Description-of-the-5G-trial-facilities-and-use-case-mapping-v2.pdf](https://5gdrones.eu/wp-content/uploads/2020/06/D1_5_Description-of-the-5G-trial-facilities-and-use-case-mapping-v2.pdf) 
[6] [https://arxiv.org/html/2502.02253v1](https://arxiv.org/html/2502.02253v1) 
[7] [https://github.com/5G-ERA/signalQualityNetworkApplicationRos2](https://github.com/5G-ERA/signalQualityNetworkApplicationRos2) 
[8] [https://docs.px4.io/v1.15/en/flight_controller/airlink.html](https://docs.px4.io/v1.15/en/flight_controller/airlink.html) 
[9] [https://arxiv.org/html/2407.01792v1](https://arxiv.org/html/2407.01792v1) 
[10] [https://docs.px4.io/main/en/flight_controller/airlink.html](https://docs.px4.io/main/en/flight_controller/airlink.html) 
[11] [http://wiki.ros.org/octomap](http://wiki.ros.org/octomap) 
[12] [https://docs.px4.io/v1.12/en/simulation/gazebo_octomap.html](https://docs.px4.io/v1.12/en/simulation/gazebo_octomap.html) 
[13] [https://gaas.gitbook.io/guide/software-realization-build-your-own-autonomous-drone/build-your-own-autonomous-drone-part-4-stereo-depth-estimation-octomap-and-path-planning](https://gaas.gitbook.io/guide/software-realization-build-your-own-autonomous-drone/build-your-own-autonomous-drone-part-4-stereo-depth-estimation-octomap-and-path-planning) 
[14] [https://pypi.org/project/octomap-ros/](https://pypi.org/project/octomap-ros/) 
[15] [https://apps.dtic.mil/sti/trecms/pdf/AD1203873.pdf](https://apps.dtic.mil/sti/trecms/pdf/AD1203873.pdf) 
[16] [https://groups.google.com/g/octomap/c/xz2A9U6emfA](https://groups.google.com/g/octomap/c/xz2A9U6emfA)
[17] [https://answers.ros.org/question/350822](https://answers.ros.org/question/350822) 
[18] [https://discourse.ros.org/t/outdoor-navigation-in-ros-current-state-future-direction/33599](https://discourse.ros.org/t/outdoor-navigation-in-ros-current-state-future-direction/33599) 
[19] [https://www.youtube.com/watch?v=TtUblDNscnA](https://www.youtube.com/watch?v=TtUblDNscnA) 
[20] [](https://octomap.github.io/)[https://octomap.github.io](https://octomap.github.io) 
[21] [https://www.reddit.com/r/ROS/comments/bllq2u/tutorial_build_autonomous_drone_depth_estimation/](https://www.reddit.com/r/ROS/comments/bllq2u/tutorial_build_autonomous_drone_depth_estimation/) 
[22] [https://moveit.picknik.ai/humble/doc/examples/perception_pipeline/perception_pipeline_tutorial.html](https://moveit.picknik.ai/humble/doc/examples/perception_pipeline/perception_pipeline_tutorial.html) 
[23] [https://github.com/Taeyoung96/OctoMap-ROS2](https://github.com/Taeyoung96/OctoMap-ROS2)
[24] [https://www.mdpi.com/2504-446X/7/6/337](https://www.mdpi.com/2504-446X/7/6/337) 
[25] [https://mdpi-res.com/bookfiles/book/8621/MultiUAV_Networks.pdf?v=1742263700](https://mdpi-res.com/bookfiles/book/8621/MultiUAV_Networks.pdf?v=1742263700) 
[26] [https://docs.px4.io/main/en/flight_controller/modalai_voxl_2.html](https://docs.px4.io/main/en/flight_controller/modalai_voxl_2.html) 
[27] [https://onlinelibrary.wiley.com/doi/10.1002/rob.22384](https://onlinelibrary.wiley.com/doi/10.1002/rob.22384) 
[28] [https://www.sciencedirect.com/science/article/pii/S0924271621003282](https://www.sciencedirect.com/science/article/pii/S0924271621003282) 
[29] [https://github.com/fkromer/awesome-ros2](https://github.com/fkromer/awesome-ros2) 
[30] [https://www.sciencedirect.com/science/article/abs/pii/S1574119225000069](https://www.sciencedirect.com/science/article/abs/pii/S1574119225000069) 
[31] [https://discourse.ros.org/t/ros2-default-behavior-wifi/13460](https://discourse.ros.org/t/ros2-default-behavior-wifi/13460) 
[32] [https://www.mdpi.com/2504-446X/5/2/41](https://www.mdpi.com/2504-446X/5/2/41) 
[33] [https://www.ros.org/news/2011/09/3d-collision-avoidance.html](https://www.ros.org/news/2011/09/3d-collision-avoidance.html) 
[34] [https://github.com/slaghuis/nav_drone](https://github.com/slaghuis/nav_drone) 
[35] [https://github.com/iKrishneel/octomap_server2](https://github.com/iKrishneel/octomap_server2) 
[36] [https://docs.px4.io/main/en/ros2/px4_ros2_navigation_interface.html](https://docs.px4.io/main/en/ros2/px4_ros2_navigation_interface.html)
37- [https://arxiv.org/html/2502.02253v1](https://arxiv.org/html/2502.02253v1)
38-[https://discourse.ros.org/t/ros-2-native-5g-support-from-ericsson-and-eprosima/17705/3](https://discourse.ros.org/t/ros-2-native-5g-support-from-ericsson-and-eprosima/17705/3)


---


### Lecture KD Tree | Octree - 30.04
- 3d points - use tree structure 
- binary  search - 1D tree 
- Root - leaf nodes - how tree builds
- vergleich - search on tree ?!
- 2D - categories  - by sign - proceed direction of positive - left works, proceed to next left leaf node  - x , y (sub-space axis)
- 3D - x, y,z
- Motiv: search nearest neighbor
- d_xl < d_0
- when y is less - next x go less -direction 
- d_xlyl who close last point (d_y)
- d_x > d_xlyr
- Data spatial discretization 
- Recursive functions- kd tree for organizing /building the point clouds
- Tree - depth parameter 
- Octree - recursive partition based - occupancy grid /space
      - Quadtree 
      - the entire quantity as one node then as a quad tree its 4 group of nodes - 
      - Difference of white/black pixels - like 0 and eg - if 1 traverse further - is it like region of interest? - Intensity of colors
      - The mix black/white quad unit is further classified - further and further based on mix level
      - color /pixel levels vary then the tree structure helps capture - how intensity is understood?  
      - Octree is a cube - one node is cube then divided - when 8 cubes - then when points /pixels available traverse  there 
      - <span style="color:rgb(255, 0, 0)">umfolge  - entourage 
      - abfolge is sequence</span> 
      - cloud compare octree
      - voxel 3d counterpart of Pixel - determine volume of the element- octree as wave form analysis 
      - Waveform full ALS - reflection - ray dampening  - multiple returns 
      - UWB- Two way ranging
  - <span style="color:rgb(255, 0, 0)">Does ROS node does compression?</span> 
  - ROS point cloud pre-processing in Companion computer ?

---
6/10 
Presentation Felix - T8 

UAV positioning and Navigation 
multi-sensor navigation framework - Map based navigation (absolute), GNSS positioning (absolute), IMU(relative) - semantic SLAM (relative- Tushar's topic)
PnP - Perspective-n-Point - match point clouds to match the image - define the pose 
Similar approach with gaussian splat mapping - start with 2d gaussian disks 
rendering of synthetic image from 2D Gaussian based on initial camera pose 
interior and exterior information of camera
true value an rendered tile - covariance matrix - check the shape
rural town based data set - UAVScenes: A multi-modal dataset for UAVs
- camera pose and movement positions - 6 Degree of freedom 
- signed distance fields 
- store gaussian information for large environments 
- Semantic level segmentation - semantic  gaussian splats enable the rendering images 
- data augmentation to enhance semantic segmentation of 3D point clouds
- Probabilistic prediction called - calibration- don't predict with high confidence 