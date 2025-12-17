# 🚀 Day 14 – Linux Privilege Escalation (Beginner Techniques)

**Date:** 17/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Abusing misconfigurations, sudo misuse & understanding GTFOBins.

---

## 🎯 Why Day 14 Matters

Yesterday I learned:
- What privilege escalation is  
- What SUID means  
- How enumeration works  

Today I learned:
👉 **How attackers abuse misconfigurations to become root**

Privilege escalation is not magic — it’s about **misconfigured permissions**.

This is a **core pentesting skill**.

---

# ✅ TASK 1 — Understanding GTFOBins

### 🔹 What is GTFOBins?

GTFOBins is a curated list of Linux binaries that can be abused to:

- Get a shell  
- Read files  
- Escalate privileges  

If these binaries run as **root** (via sudo or SUID) → attacker wins.

### Common GTFOBins examples:
find
vim
less
nano
python
bash


### 🧠 Key Learning:
I don’t need to memorize GTFOBins —  
I just need to recognize **dangerous binaries running as root**.

---

# ✅ TASK 2 — Checking Misconfigured sudo (Hands-On)

I ran:

sudo -l


This command lists:
- Which commands I can run as root  
- Whether a password is required  

### Dangerous example output:
(ALL) NOPASSWD: /usr/bin/find


### Meaning:
- I can run `find` as root  
- No password needed  
- This is a **privilege escalation opportunity**

Today I only **identified** the issue.

---

# ✅ TASK 3 — Simple PrivEsc Using `find` (Safe Demo)

If `find` had sudo permission, I tested:

sudo find . -exec /bin/bash ;


Then checked:

whoami


### Expected output (if successful):
root


### 🧠 Learning:
- Some binaries allow command execution  
- If they run as root → shell becomes root  

If it didn’t work, that’s fine — understanding is the goal.

---

# ✅ TASK 4 — SUID Binary Abuse (Beginner Understanding)

I searched for SUID binaries again:

find / -perm -4000 2>/dev/null


Common SUID binaries I observed:

find
vim
less


### 🧠 Key Concept:
If a binary:
- Has SUID bit  
- Runs as root  
- Allows command execution  

→ It can be abused for privilege escalation.

Today I focused on **identification**, not exploitation.

---

# ✅ TASK 5 — TryHackMe Beginner PrivEsc Room

I completed beginner sections from ONE of these:

✔ Linux PrivEsc (Beginner)  
✔ Sudo Security Bypass  
✔ RootMe (Linux part only)  

### Focus Areas:
- sudo abuse  
- SUID abuse  
- Understanding *why* privilege escalation works  

Skipped advanced exploitation techniques.

---

# 📝 TASK 6 — Notes in My Own Words

### 🔹 What is GTFOBins?
A list of Linux binaries that can be abused for privilege escalation if misconfigured.

---

### 🔹 What does `sudo -l` show?
It shows which commands I can run as root and whether a password is required.

---

### 🔹 Which binary could be abused?
Examples:
- find  
- vim  
- less  

---

### 🔹 Why is misconfigured sudo dangerous?
Because it allows normal users to run powerful commands as root.

---

### 🔹 How did I become root (if I did)?
By abusing a binary that was allowed to run as root without a password.

---

## 💭 How I Felt Today

- Privilege escalation started feeling real  
- GTFOBins concept clicked clearly  
- Misconfigurations now feel “visible”  
- Confidence increased in Linux exploitation  

---

## 📌 Summary of Day 14

Today I learned:

- What GTFOBins is  
- How sudo misconfigurations occur  
- How attackers abuse allowed binaries  
- How SUID & sudo lead to root access  
- Why privilege escalation is mostly about configuration mistakes  

This day strengthened my **Linux PrivEsc foundation**.

---

**End of Day 14** 