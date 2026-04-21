# Lab 01: Basic Connectivity

## Overview
This lab demonstrates how two devices communicate within the same network using a switch. It covers basic IP configuration and connectivity testing.

---

## Topology
PC0 ─── Switch ─── PC1

![Topology](basic-connectivity.png)

---

## Devices Used
- 2 × PCs (PC0, PC1)  
- 1 × Switch (2960)  

---

## Configuration

### PC0
- IP Address: 192.168.1.1  
- Subnet Mask: 255.255.255.0  

### PC1
- IP Address: 192.168.1.2  
- Subnet Mask: 255.255.255.0  

---

## Connectivity Test

Command used:

```
ping 192.168.1.2
```


Result:
- Successful replies received  
- No packet loss  

---

## How to Run

1. Open the `.pkt` file using Cisco Packet Tracer
2. Click on PC0 → Desktop → Command Prompt
3. Run:
```
ping 192.168.1.2
```
4. Observe successful replies

---

## What Actually Happens

1. PC0 checks if the destination IP (192.168.1.2) is in the same network.  
2. Since both devices share the same subnet, no router is required.  
3. PC0 sends the packet to the switch.  
4. The switch uses its MAC address table to forward the frame to PC1.  
5. PC1 receives the packet and sends a reply.  
6. PC0 receives the reply, confirming connectivity.  

---

## Key Concepts Learned

- Devices in the same network can communicate without a router  
- A switch forwards data using MAC addresses  
- IP addressing enables device identification  
- Ping is used to test connectivity  

---

## Interview Explanation

**Explain your lab:**  
I created a basic network with two PCs and a switch, assigned IP addresses in the same network, and verified connectivity using ping. This demonstrates how devices communicate within a local network.

**What is a switch?**  
A switch connects devices in a local network and forwards data using MAC addresses to the correct device.

**How does ping work?**  
Ping sends a request to another device and waits for a reply to verify connectivity.

---

## Key Takeaway

Devices within the same network can communicate directly through a switch without requiring a router.

## Conclusion
This lab establishes the foundation of networking by demonstrating basic device communication within a LAN environment.
