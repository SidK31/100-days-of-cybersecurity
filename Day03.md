# 🚀 Day 3 – Introduction to Scanning & Enumeration (Soft Start)

**Date:** 06/12/2025 
**Journey:** 100 Days of Cybersecurity  
**Focus:** Learning Nmap, scanning basics, and early enumeration.

---

## 🎯 What I Learned Today

Today I started understanding one of the MOST important skills in ethical hacking:

👉 **How hackers gather information before attacking.**  
This phase is called **Scanning & Enumeration** — and it is the backbone of penetration testing.

---

# ✅ TASK 1 — What is Nmap & Why Hackers Use It?

Before running scans, I learned what Nmap actually is:

### 🔥 **Nmap = Network Mapper**
Hackers use it to discover:

- Open ports  
- Running services  
- OS information  
- Network hosts  
- Potential vulnerabilities  

Nmap is basically an **X-ray vision tool for networks**.

I also completed the TryHackMe section:

✔ *Nmap Introduction (Beginner)*

This helped me understand theory + small examples.

---

# ✅ TASK 2 — Basic Nmap Hands-On (Beginner Commands)

I opened Kali Linux and practiced 5 essential Nmap commands on a TryHackMe machine.

### 1️⃣ Ping Scan
nmap -sn <IP>
Checks if the host is alive.

### 2️⃣ Basic Port Scan
nmap <IP>
Shows open ports.

### 3️⃣ Service Version Detection
nmap -sV <IP>
Reveals service versions (e.g., Apache, SSH, FTP).

### 4️⃣ Scan Top Common Ports
nmap -F <IP>

### 5️⃣ OS Detection (If Allowed)
nmap -O <IP>

### 🧠 What I observed:
- Which ports were open  
- What services were running  
- Which services look interesting for pentesting (FTP, SSH, SMB, HTTP etc.)

No advanced enumeration yet — only understanding the output.

---

# ✅ TASK 3 — TryHackMe Room: Nmap Basics

I completed the following beginner-friendly TryHackMe rooms:

✔ *Nmap Live Host Discovery*  
or  
✔ *Nmap Basics*

I focused only on:

- Introduction  
- Basic scans  
- Understanding the output  

This gave me confidence with Nmap.

---

# ✅ TASK 4 — Light Enumeration (Observation Only)

After scanning, I learned how hackers *think*:

### 🔍 Important ports to observe:

| Port | Service | Why It Matters |
|------|---------|----------------|
| 80/8080 | HTTP | Website exists |
| 22 | SSH | Remote login |
| 21 | FTP | Anonymous login possibility |
| 445 | SMB | Common vulnerability target |
| 3306 | MySQL | Database access |

### 🔥 Today's Task:
I identified:
- Open ports  
- Running services  
- Possible entry points  

(No exploitation yet — only enumeration mindset.)

---

# ✅ TASK 5 — Notes in My Own Words

### 🔹 **What is Nmap?**  
A network scanning tool used to discover open ports, services, OS info, and vulnerabilities.

---

### 🔹 **What is a port scan?**  
A technique to check which ports are open on a system and what services are running.

---

### 🔹 **What is service detection?**  
Using flags like `-sV` to identify the exact version of services running on open ports.

---

### 🔹 **Three Most Common Ports I Saw Today:**  
- 22 (SSH)  
- 80 (HTTP)  
- 443 (HTTPS)  

---

## 💭 How I Felt Today

- Nmap felt intimidating at first, but beginner commands are easy  
- Now I understand why scanning is the first step of hacking  
- Feeling excited for deeper enumeration on Day 4 🔥  

---

## 📌 Summary of Day 3

Today I learned:
- What Nmap is  
- How scanning works  
- Basic Nmap scans  
- How to interpret results  
- Early enumeration mindset  

Nmap is the backbone of pentesting — and today was my first step into real hacking workflow.

---

**End of Day 3** 🚀
