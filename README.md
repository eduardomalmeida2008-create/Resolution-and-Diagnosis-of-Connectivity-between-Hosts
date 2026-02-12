# Resolution-and-Diagnosis-of-Connectivity-between-Hosts
This is a simulated lab in the Cisco Packet Tracer simulator. In this lab, a diagnosis and resolution of a connectivity problem was performed, with visual information stored in the repository files.
\
\
\
PROBLEM:
\
![Ping ICMP PC1](06-TestPing-PC1.png) ![Ping ICMP PC2](07-TestPing-PC2.png)
\
Problem identified in the connectivity test (ICMP) between the department computer (CLIENTS) and the department computer (SERVERS).
\
\
\
TOPOLOGY AND DIAGRAM:
![TOPOLOGY](01-Topology_Overview.png) ![DIAGRAM](08-Diagram.png)
\
As shown, these images would be the visual part of the network topology and diagram. Where it shows information about:
- Routing List between Devices
- Number of Devices

Device model and brands:
Switch 2960-24TT (CISCO)
Router 2911 (CISCO)
Generic PCs (CISCO)
\
\
\
Where is the error and how can it be fixed?
\
What we see is an ICMP connectivity problem for a basic network that has few hosts and only one switch and router to perform routing and connectivity between hosts and departments. We can analyze some possible errors:
\
- Incorrect host subnet mask
- Incorrect IPV4 address
- Incorrect host gateway
- Incorrect access/trunk ports
- Among other specific errors
\
\
\
Check the switch and router settings:
![SWITCH](05-Configuration-Switch.png) ![ROTEADOR](04-Configuration_Router.png)
\
As we can see:

- Trunking configured correctly
- VLANs created correctly
- Ethernet ports activated correctly
- Encapsulation of the “client” department configured correctly on the router

However, as we can see, the encapsulation of the “servers” department is not configured correctly, as the following are missing:

- Gateway and subnet mask applied


Why add them?
- The subnet mask works to define network limits, so that the host or router can identify: “is this destination on my local network or outside it?”

- The gateway acts as a “gateway” for the network, through which hosts can connect to the internet.

- Encapsulation works as a “traffic identifier.” When there are several departments or more than one, encapsulation is necessary to label the departments so that when traffic travels on the network, it will know where to go and which department to go to by identifying the department's TAG.
