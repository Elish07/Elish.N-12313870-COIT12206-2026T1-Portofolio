# COIT12206 TCP/IP Principles and Protocols  
## Week 6 Portfolio – ARP and Default Gateway  

### Student Details  
Name: Elish Niraula  
Student ID: 12313870  
Unit: COIT12206 TCP/IP Principles and Protocols  
Term: 2026 T1  

---

## Task 1: ARP (Address Resolution Protocol)  

### Objective  
To understand how ARP maps IP addresses to MAC addresses and how ARP tables change during communication.

---

### Methodology  
A network consisting of four Linux hosts connected via an Ethernet switch was used. Each host was assigned an IP address.  

The ARP table of a host was viewed using the `ip neigh show` command. Ping tests were performed between hosts, and the ARP table was observed before and after communication to analyse changes.

---

### Commands Used  
ip neigh show
ping <destination-ip>


---

### Results  
Initially, the ARP table contained minimal or no entries. After communication between hosts, new entries appeared showing mappings between IP and MAC addresses.  

The ARP table dynamically updated as different hosts communicated, demonstrating how devices learn and store address mappings.

---

### Screenshots  

![ARP Table Initial](./week06-1.png)

![ARP After Ping](./week06-2.png)

![ARP Updated](./week06-3.png)

---

### Discussion  
This task demonstrates that ARP operates dynamically within a network. Devices automatically update their ARP tables when communication occurs. This process is essential for correct data delivery at the data link layer.

---

## Task 2: Default Gateway and Routing  

### Objective  
To understand how default gateways enable communication between different subnets.

---

### Methodology  
A network was created consisting of four hosts, two routers, and two switches forming three subnets. IP addresses and default gateways were configured using the `/etc/network/interfaces` file.  

IP forwarding was enabled on routers and disabled on hosts. Routing tables were examined, and connectivity between different subnets was tested using ping.

---

### Commands Used  
ip route show
ping <destination-ip>


---

### Results  
Hosts within the same subnet communicated directly. After configuring default gateways, hosts in different subnets were able to communicate successfully.  

Routing tables confirmed that packets were correctly forwarded through routers.

---

### Screenshots  

![Network Topology](./week06-4.png)

![Routing Table](./week06-5.png)

![Ping Across Subnets](./week06-6.png)

---

### Discussion  
Default gateways act as an entry point for communication between networks. Without proper gateway configuration, devices cannot communicate outside their local subnet.  

Routers play a critical role in forwarding packets between networks.

---

## Conclusion  
The tasks demonstrated how ARP resolves IP addresses to MAC addresses and how default gateways enable communication across networks. These concepts are fundamental to network communication.

---

## Reflection  
This week improved my understanding of how devices communicate within and across networks. The practical tasks provided valuable insight into ARP behaviour and routing mechanisms, which are essential for real-world networking.
