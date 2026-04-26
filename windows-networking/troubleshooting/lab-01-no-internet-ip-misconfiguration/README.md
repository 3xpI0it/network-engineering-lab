# Lab 01: No Internet – IP Misconfiguration

## Overview
This lab demonstrates how incorrect IP configuration can lead to complete network failure and how to diagnose and resolve the issue using Windows networking tools.

---

## Scenario
A system is unable to access the internet. The issue is caused by incorrect IP configuration where the default gateway does not exist in the network.

---

## Initial State

System is connected to the network and internet is working.

![Initial Connectivity](01-initial-connectivity.png)

---

## Misconfiguration

The system is manually configured with incorrect network settings:

- IP Address: 192.168.50.10  
- Subnet Mask: 255.255.255.0  
- Default Gateway: 192.168.50.1 (invalid)

![IP Misconfiguration](02-ip-misconfiguration.png)

---

## Issue Observed

After applying incorrect settings:

- Internet connectivity is lost  
- Ping to external IP fails  

![Connectivity Failure](03-connectivity-failure.png)

---

## Troubleshooting

1. Checked IP configuration using `ipconfig`  
2. Identified mismatch between valid network and gateway  
3. Observed that the gateway is unreachable  
4. Concluded incorrect IP configuration is the root cause  

---

## Resolution

Restored network configuration to automatic IP assignment (DHCP).

![Fix - Automatic IP](04-fix-ip-automatic.png)

---

## Verification

After fixing the configuration:

- Valid IP assigned  
- Internet connectivity restored  
- Ping successful  

![Connectivity Restored](05-connectivity-restored.png)

---

## Key Takeaway

- Incorrect IP configuration can break connectivity  
- Default gateway must be valid and reachable  
- Troubleshooting should follow a logical step-by-step approach  
- Always verify IP, subnet, and gateway alignment  

---

## Interview Explanation

If a system has no internet connectivity, first check the IP configuration using ipconfig. Verify that the IP address, subnet mask, and default gateway are correctly configured and belong to the same network. If misconfigured, correct the settings or switch to automatic IP assignment.
