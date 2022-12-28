<p align="center">
<img src="https://i.imgur.com/pugpymL.jpg" alt="Traffic Examination"/>
</p>

<h1>Implementing OSPF Routing Protocol on Cisco Routers</h1>
In this tutorial, we will configure Cisco routers with the OSPF routing protocol and test network connectivity between different subnets in the network. <br />


<h2>Overview of the Topology</h2>

<img src="https://i.imgur.com/FQPkm1J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<h2>Environments and Technologies Used</h2>

- Cisco Packet Tracer
- Cisco IOS CLI
- IP Addresses
- OSPF Routing Protocol

<h2>Operating Systems Used </h2>

- Cisco Packet Tracer
- Cisco IOS

<h2>High-Level Steps</h2>

- Step 1: Configure R1 with the appropriate IP addressed for each interface. Enable each interface. Repeat for R2, R3, and R4.
- Step 2: Enable the Routing Protocol OSPF on each router.
- Step 3: Configure a default route on R1 and advertise it the other OSPF routers.
- Step 4: 
- Step 5: 
- Step 6: 
- Step 7: 
- Step 8: 

<h2>Actions and Observations</h2>

Step 1
<p>
<img src="https://i.imgur.com/LhpIuHN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
For this tutorial, refer to the Topology Overview image for the IP addresses to assign on each router interface. Left click on R1 and navigate to the CLI tab. This is the router's command line. Enter the "en" (enable), "conf t" (configure terminal), to reach global config mode. Here we can configure the IP addresses for each interface. Enter the "int g3/0" (interface gigabit3/0) to configure the g3/0 interface individually. Enter the "ip address" command followed by 203.0.113.1 (g3/0 ip) 255.255.255.252 (the /30 subnet mask). Next enter "no sh" to turn the interface status up. By default, Router interfaces are "administratively down". Repead these steps for interfaces g0/0 and f1/0. Change the router hostname to R1 with the command "hostname R1". Lastly enter "do sh ip int br" (do show ip interface brief) to confirm the configurations are correct. Repeat these steps for routers 2, 3, and 4.
</p>
<br />

Step 2
<p>
<img src="https://i.imgur.com/mMwGMEe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In step 2, we will enable OSPF on each interface for each router. Enter the command "interface range g0/0, f1/0". This range command allows us to configure multiple interfaces at once. Next activate OSPF on both interfaces with the command "ip ospf 1 area 0". The number "1" is the process id while "0" is the area. To confirm our configurations are correct, enter the command do "sh ip protocol". Repeat this step for routers 2, 3, and 4. After these configurations, you should see messages in the cli of each router detailing OSPF changing from LOADING to FULL.
</p>
<br />

Step 3
<p>
<img src="https://i.imgur.com/Le894ma.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On R1, we will configure a default route to advertise to the other OSPF routers since it is face the internet. Essentially, a default route is ip 0.0.0.0. We will tell all other routers to send traffic that does not match a destination on their routing table to the default route. In most cases, a default route is used to send traffic to the internet. 
</p>
<br />

Step 4
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

Step 5
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

Step 6
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
