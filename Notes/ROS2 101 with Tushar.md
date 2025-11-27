27/11

connections
Pixhawk with agx
lidar and camera ethernet to agx 

ROS in a docker 
ROS is always connected to specific ubuntu version 
git clone and build - make sure ROS and ubuntu version is compatible 

RoS
Topics - One to many - publish to subscribe - broadcast 

Action - server 

Topics have direcories like event camera then image vector (namespaces)
Topic have specific message type 
standard and sensor type message 
geometry message sand custom message 

Nodes - multiple nodes can publish on one topic 

Ros packages is clustering into one lib. Node is final executable - interact with nodes through topics 

processing can be segregated and parallelized among nodes 
nodes can exists anywhere in the network 
Node can be communicated across anywhere in the network
stick to directory structure 
 node 
src is workspace

symlink - like in linux


eg: camera has a image topic from a node. Then In the package node 1 - Tushar can create/model and add data to the topic- processed image and that can be subscribed by RViz 

Rviz can subscribe to any topic


what is action-server 
more like TCP  - get a feedback

message - header : spatial and temporal data and then actual payload

xrcedds bus between pixhawk and jetson (cable uart or ethernet)

check gitlab
create publishers and subscribers

read ros commands 
ros packages used 

srx px4 have message definitions - then that have access to nodes, launch files etc.

main cmtd after build  - source install/setup.bash 
ctrl +r  - for finding cmds

in and out 
explore action server for in and out 

launch file orchestrate all the nodes together 
work with callback 
ros2 




