# COIT12206 TCP/IP Principles and Protocols  
## Week 2 Portfolio – Static IP Configuration and Ping  

### Student Details  
Name: Elish Niraula  
Student ID: 12313870  
Unit: COIT12206 TCP/IP Principles and Protocols  
Term: 2026 T1  

---

## 1. Introduction  
This task focuses on configuring static IP addresses using different methods and testing network connectivity using the ping command. It demonstrates how devices communicate within a local network and how delays and errors can be observed.

---

## 2. Methodology  
A network consisting of four Linux hosts and one Ethernet switch was created in GNS3. Static IP addresses were assigned using three different approaches: via the GNS3 configuration menu, by editing the `/etc/network/interfaces` file, and by using the `ip address add` command in the terminal.  

After configuring the IP addresses, connectivity between hosts was tested using the ping command with different options.

---

## 3. Commands Used  
ip address show
ip address add <ip>/<mask> dev eth0
ifdown eth0
ifup eth0
ping <destination-ip>
ping -c 5 <destination-ip>
ping -s 100 <destination-ip>

---

## 4. Results  
All four hosts were successfully assigned IP addresses using different configuration methods. The `ip address show` command confirmed correct IP assignment on each host.  

Ping tests between hosts were successful, demonstrating proper network connectivity. When pinging an invalid IP address, packet loss was observed, confirming expected network behaviour.

---

## 5. Screenshots  
The following evidence is included to support the results:

![IP Configuration](./Screenshot%202026-03-23%20173356%20(1).png)

![IP Configuration Method](./Screenshot%202026-03-23%20175004%20(1).png)

![Console Output](./Screenshot%202026-03-23%20181351%20(1).png)

![Console Output 2](./Screenshot%202026-03-23%20181356%20(1).png)

![Ping Success](./Screenshot%202026-03-23%20181406%20(1).png)

![Ping Error](./Screenshot%202026-03-23%20181414%20(1).png)

![Ping Options](./Screenshot%202026-03-23%20183249%20(1).png)

![Additional Result](./Screenshot%202026-03-23%20183431%20(1).png)

---

## 6. Discussion  
This task highlights the importance of correctly assigning IP addresses for communication within a network. It also demonstrates how different configuration methods can be used depending on the situation.  

The ping command proved useful in verifying connectivity and measuring network performance, including delay and packet loss.

---

## 7. Conclusion  
The activity successfully demonstrated how to configure static IP addresses and test communication between network devices. The results confirmed that the network was functioning as expected.

---

## 8. Reflection  
Through this task, I developed a deeper understanding of IP addressing and network testing tools. The experience improved my ability to configure and troubleshoot network connectivity issues.
