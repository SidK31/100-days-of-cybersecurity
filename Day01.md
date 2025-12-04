# Day 1 – Networking Basics & Essential Commands

**Date:** 04/12/2025  
**Journey:** 100 Days of Cybersecurity Learning  
**Goal:** Build strong fundamentals in networking before moving into ethical hacking.

---

## ✅ TASK 1 — Networking Fundamentals I Learned

Today I studied the four core networking concepts every cybersecurity engineer must know:

### 🔹 1. TCP/IP  
A set of communication rules that define how data travels from one device to another on a network.

### 🔹 2. Ports & Protocols  
Ports = numbered "doors" used by services (e.g., 80 = HTTP, 443 = HTTPS).  
Protocols = rules for communication (TCP, UDP, HTTP, DNS, etc.).

### 🔹 3. DNS  
DNS converts human-readable website names like `google.com` into machine-readable IP addresses.

### 🔹 4. DHCP  
Automatically assigns IP addresses and network configuration to devices.

---

## ✅ TASK 2 — Hands-On Networking Practice

I ran these commands to understand how networking works practically:

| Command | Used For |
|--------|----------|
| `ipconfig /all` | Shows full network details (Windows) |
| `/sbin/ifconfig` | Shows interface details (Linux) |
| `ping google.com` | Tests connectivity |
| `tracert google.com` | Shows route to destination (Windows) |
| `traceroute google.com` | Linux route tracing |
| `nslookup google.com` | Finds domain → IP |
| `netstat -ano` | Shows active connections + ports + PID |

---

## Short Notes in My Own Words

### 🔹 **What is IP?**  
The unique address of a device on a network. Without an IP, devices can't communicate.

### 🔹 **What is a port?**  
A virtual door used by applications/services to send or receive data. Example:  
- 80 = HTTP  
- 443 = HTTPS  
- 22 = SSH

### 🔹 What is DNS?  
A service that changes domain names into IP addresses (like phone contacts → phone numbers).

### 🔹 What is DHCP? 
A service that automatically gives IP, subnet mask, gateway, and DNS to devices.

### 🔹 **What is traceroute?**  
A command that shows every router (hop) your data passes through on the way to a destination.

---

## ✅ TASK 3 — Important Ports (Memorized Today)

21 - FTP
22 - SSH
23 - Telnet
25 - SMTP
53 - DNS
67/68 - DHCP
69 - TFTP
80 - HTTP
110 - POP3
123 - NTP
135 - RPC
139 - NetBIOS
143 - IMAP
161/162 - SNMP
389 - LDAP
443 - HTTPS
445 - SMB
587 - Secure SMTP
1433 - MSSQL
3306 - MySQL


---

## 💭 How I Felt Today

- Started my cybersecurity journey 🔥  
- Learnt important networking basics  
- Ran real commands for the first time  
- Feeling motivated for Day 2 💪  

---

## 📌 Summary

Day 1 was all about building the foundation:  
**Networking + Ports + DNS + Practical Commands.**  
This base will help me a lot when I start scanning, enumeration, and exploitation in the future.

---

**End of Day 1** 🚀
