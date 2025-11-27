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



