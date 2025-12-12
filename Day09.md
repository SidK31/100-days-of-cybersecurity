# 🚀 Day 9 – Reconnaissance & Information Gathering

**Date:** 12/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Subdomain enumeration, robots.txt recon, header analysis, directory fuzzing.

---

## 🎯 What I Learned Today

Reconnaissance (recon) is the **first and MOST important step** of penetration testing.

Pentesting steps:

1️⃣ Recon  
2️⃣ Scanning  
3️⃣ Enumeration  
4️⃣ Exploitation  
5️⃣ Privilege Escalation  
6️⃣ Reporting  

Today I focused on mastering Step 1.

Recon = detective work that makes exploitation easier.

---

# ✅ TASK 1 — What is Recon?

Recon is the process of gathering public and technical information about a target.

I learned that recon reveals:

- Subdomains  
- Hidden directories  
- Server details  
- Technologies used  
- Publicly exposed data  
- robots.txt secrets  
- Headers  
- Internal endpoints  
- Backup files  
- Web server info  

### 🔥 Important Lesson:
👉 **More recon = easier exploitation.**

---

# ✅ TASK 2 — Subdomain Enumeration

Tools used: **Gobuster (DNS mode)**  
TryHackMe Rooms:  
✔ Demystifying Subdomains  
✔ Reconnaissance Basics  

### Command Used:
gobuster dns -d <domain>
-w /usr/share/wordlists/seclists/Discovery/DNS/subdomains-top1million-110000.txt



If wordlist missing:
sudo apt install seclists



### 🧠 Goal:
Find subdomains like:

- admin.example.com  
- dev.example.com  
- test.example.com  
- backup.example.com  

### ✍️ I wrote down all valid subdomains discovered.

---

# ✅ TASK 3 — robots.txt Recon

robots.txt often hides valuable paths.

Visited:
http://<target>/robots.txt


Looked for sensitive directories like:

- /admin  
- /backup  
- /test  
- /hidden  
- /.git  
- /private  

robots.txt recon is one of the easiest and most powerful early recon tricks.

### ✍️ I noted all interesting directories found.

---

# ✅ TASK 4 — Using curl & wget for Recon

Used **curl** to inspect headers:

### 🔹 Get headers only:
curl -I http://<IP>




### 🔹 View full request + response:
curl -v http://<IP>

css


### 🔹 Download a page:
wget http://<IP>

markdown


### 👀 What I looked for:

- **Server:** Apache, nginx  
- **X-Powered-By:** PHP, Node.js, Express  
- **Set-Cookie:** session values  
- **Content-Type:** text/html, json  

These details help identify the stack and potential weaknesses.

### ✍️ I wrote down:
- Server type  
- Cookies  
- Framework used  

---

# ✅ TASK 5 — Directory Fuzzing (Level Up)

Used Gobuster for directory enumeration:

gobuster dir -u http://<IP>
-w /usr/share/wordlists/dirb/common.txt



### Goal:
Find directories like:

- /admin  
- /uploads  
- /backup  
- /config  
- /includes  
- /images  
- /private  

### ✍️ Noted the most interesting and attackable ones.

---

# ✅ TASK 6 — TryHackMe Recon Rooms

Completed:

✔ Reconnaissance Basics  
or  
✔ Intro to Offensive Security (Recon section)  
or  
✔ Information Gathering  

Focused on beginner-friendly recon exercises.

---

# 📝 TASK 7 — Notes in My Own Words

### 🔹 **What is recon?**  
The first step of hacking where we gather information about the target to make later exploitation easier.

---

### 🔹 **Which subdomains did I find?**  
(Write the actual ones you saw)

Example:
- admin.example.com  
- dev.example.com  
- staging.example.com  

---

### 🔹 **What did robots.txt contain?**  
(Write findings)

Example:
- /admin  
- /beta  
- /private  

---

### 🔹 **What server type did curl show?**  
Example:
- Server: Apache/2.4.41  
- X-Powered-By: PHP/7.4.3  

---

## 💭 How I Felt Today

- Recon felt like real hacker detective work 🔍  
- Subdomain enumeration was fun  
- curl gave me deeper insights into server behavior  
- Feeling more confident about mapping targets before attacking  

---

## 📌 Summary of Day 9

Today I learned:

- Recon fundamentals  
- Subdomain enumeration  
- robots.txt discovery  
- Header analysis with curl  
- Directory fuzzing  
- How reconnaissance makes exploitation easier  

Recon is the heart of pentesting — the more you find, the more you can exploit.

---

**End of Day 9** 🚀