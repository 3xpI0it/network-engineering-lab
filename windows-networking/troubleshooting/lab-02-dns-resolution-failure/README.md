# Lab 02: DNS Resolution Failure

## Overview
This lab demonstrates a scenario where internet connectivity is available, but domain names cannot be resolved due to incorrect DNS configuration.

---

## Scenario
A system is able to access the internet using IP addresses, but fails to access websites using domain names. The issue is caused by incorrect DNS server configuration.

---

## Initial State

System has full internet connectivity.

- Ping to IP address works  
- Ping to domain name works  

![Initial Connectivity](01-initial-connectivity.png)

---

## Misconfiguration

DNS is manually configured with invalid DNS server addresses:

- Preferred DNS: 192.168.50.1  
- Alternate DNS: 192.168.50.2  

These DNS servers do not exist.

![DNS Misconfiguration](02-dns-misconfiguration.png)

---

## Issue Observed

After applying incorrect DNS settings:

- Ping to IP address (8.8.8.8) works  
- Ping to domain name (google.com) fails  

This indicates that internet connectivity exists, but domain resolution is not working.

![Domain Failure](03-domain-failure.png)

---

## Troubleshooting

1. Verified connectivity using ping to a public IP address  
2. Observed that IP-based communication is working  
3. Tested domain name resolution and identified failure  
4. Concluded DNS configuration issue as root cause  

---

## Resolution

DNS configuration is corrected by switching to automatic DNS assignment.

![DNS Fix](04-dns-fix.png)

---

## Verification

After fixing DNS configuration:

- Domain resolution works  
- Ping to domain name is successful  
- nslookup confirms proper DNS response  

![Domain Restored](05-domain-restored.png)

---

## Key Takeaway

- Internet connectivity and DNS resolution are separate  
- If ping to IP works but domain fails, it indicates a DNS issue  
- DNS configuration is critical for accessing websites  
- Troubleshooting should isolate IP vs domain-level problems  

---

## Interview Explanation

If a system can access the internet using an IP address but cannot access websites using domain names, it indicates a DNS issue. I verify this by testing connectivity using ping. If IP works and domain fails, I check and correct the DNS configuration.
