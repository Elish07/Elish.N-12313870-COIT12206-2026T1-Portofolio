# COIT12206 TCP/IP Principles and Protocols  
## Week 4 Portfolio – Routing Tables and OSPF  

### Student Details  
Name: Elish Niraula  
Student ID: 12313870  
Unit: COIT12206 TCP/IP Principles and Protocols  
Term: 2026 T1  

---

## Task 1: Viewing Routing Tables  

### Objective  
To understand how routing tables work and how routers forward packets between different subnets.

### Methodology  
A network was created in GNS3 with multiple Linux hosts and a router connected via a switch. Static IP addresses were assigned to all devices. IP forwarding was enabled on the router and disabled on the hosts.  

Routing tables were viewed using appropriate commands, and connectivity between hosts in different subnets was tested using ping.

### Commands Used  
ip route show
sysctl net.ipv4.ip_forward


### Results  
The routing tables displayed the correct network paths. Communication between hosts across different subnets was successful, confirming that routing was functioning correctly.

### Screenshots  

![Network Topology](./week04-1.png)

![Routing Table](./week04-2.png)

![Ping Result](./week04-3.png)

---

## Task 2: Dynamic Routing with OSPF  

### Objective  
To observe how OSPF dynamically manages routing and adapts to network changes.

### Methodology  
The provided OSPF template was used, where routers were pre-configured. Routing information was analysed using FRR commands. The traceroute command was used to observe packet paths between hosts.  

A link was then disabled to observe how OSPF recalculates routes and selects an alternative path.

### Commands Used  
show ip ospf neighbor
show ip ospf route
show ip route
traceroute <destination-ip>


### Results  
OSPF successfully identified neighbouring routers and maintained routing tables dynamically. After disconnecting a link, the routing path changed automatically, demonstrating OSPF’s adaptability.

### Screenshots  

![OSPF Neighbors](./week04-4.png)

![OSPF Routes](./week04-5.png)

![Traceroute Before](./week04-6.png)

![Traceroute After](./week04-7.png)

---

## Conclusion  
The tasks demonstrated both static and dynamic routing. Static routing provides controlled communication, while OSPF improves network reliability by automatically adapting to changes.

---

## Reflection  
This week enhanced my understanding of routing mechanisms and dynamic protocols. The practical experience with OSPF provided valuable insight into real-world network behaviour and fault tolerance.
