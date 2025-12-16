# 🚀 Day 13 – Linux Privilege Escalation (Beginner Intro)

**Date:** 16/12/2025 
**Journey:** 100 Days of Cybersecurity  
**Focus:** Understanding Linux privilege escalation basics, enumeration & SUID concepts.

---

## 🎯 Why Privilege Escalation Matters

In real penetration testing:

- Getting access as a normal user is NOT enough  
- The real goal is **root / administrator access**  

Privilege Escalation (PrivEsc) means:
👉 Finding weaknesses to increase privileges.

Think of it like:
> You entered the house, now you want the **master key** 🔑

---

# ✅ TASK 1 — Users, Groups & Root (Linux Basics)

Linux has different privilege levels:

### 👑 Root User
- Full control of the system  
- Can read/write all files  
- Can install software  
- Can modify system configuration  

### 👤 Normal User
- Limited access  
- Restricted permissions  
- Cannot modify critical system files  

### Commands Used:
whoami
id



These commands tell:
- Who you are  
- Your user ID  
- Your group memberships  

Understanding this is the first step in privilege escalation.

---

# ✅ TASK 2 — Basic Enumeration (First Step of PrivEsc)

Once you get a shell, **enumeration is mandatory**.

I ran these commands:

whoami
id
uname -a
hostname
pwd
ls -la


### 🧠 Goal of Enumeration:
- Who am I?  
- Where am I?  
- What system is this?  
- What files & permissions exist?  

Without enumeration, privilege escalation is blind guessing.

---

# ✅ TASK 3 — Understanding SUID (VERY IMPORTANT)

### 🔐 What is SUID?
SUID (Set User ID) allows a program to run with the **permissions of its owner**.

If the owner is **root**, the program runs as root — even if you are a normal user.

### Checking SUID files:
find / -perm -4000 2>/dev/null



### Common SUID binaries:
/usr/bin/passwd
/usr/bin/sudo
/usr/bin/find



### 🧠 Key Learning:
Some SUID binaries can be abused for privilege escalation if misconfigured.

Today I only **identified** SUID files, not exploited them.

---

# ✅ TASK 4 — TryHackMe Beginner PrivEsc Room

I completed beginner sections from ONE of these:

✔ Linux Privilege Escalation (Intro)  
✔ Sudo Security Bypass (Beginner)  
✔ Basic Privilege Escalation  

### Focus Areas:
- Enumeration  
- SUID concept  
- Misconfigurations  
- Why PrivEsc exists  

Skipped advanced exploitation techniques for now.

---

# ✅ TASK 5 — Simple PrivEsc Check (Safe)

If a shell was available, I ran:

sudo -l



This command shows:
- Which commands I can run as root  
- Whether password is required  

### Example Output:
(ALL) NOPASSWD: /usr/bin/find



This indicates a **potential privilege escalation path**.

Today I only noted it — no exploitation attempted.

---

# 📝 TASK 6 — Notes in My Own Words

### 🔹 What is Privilege Escalation?
Privilege escalation is the process of gaining higher access (root/admin) from a limited user account.

---

### 🔹 What is SUID?
A permission that allows programs to run as the file owner, often root.

---

### 🔹 Why is enumeration important?
Because it reveals system information, permissions, binaries, and misconfigurations needed for PrivEsc.

---

### 🔹 What did `sudo -l` show?
It showed which commands can be run as root and if password is required.

---

### 🔹 Which binaries had SUID bit?
Examples:
- passwd  
- sudo  
- find  

---

## 💭 How I Felt Today

- Privilege escalation concepts became clear  
- Enumeration felt like real hacker workflow  
- SUID understanding was a big milestone  
- Feeling confident moving toward deeper Linux exploitation  

---

## 📌 Summary of Day 13

Today I learned:

- Why privilege escalation is critical  
- Difference between normal user & root  
- Importance of enumeration  
- What SUID is and why it’s dangerous  
- How misconfigurations lead to root access  

This day marked my **entry into system-level hacking**.

---

**End of Day 13** 