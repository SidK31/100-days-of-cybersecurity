# 🚀 Day 12 – Path Traversal & Local File Inclusion (LFI)

**Date:** 15/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Understanding Path Traversal, Local File Inclusion (LFI) & safe manual testing.

---

## 🎯 Why Day 12 Is Important

Many websites dynamically load files using parameters such as:

- `?file=report.pdf`
- `?page=about`
- `?view=profile`

If these inputs are not validated properly, attackers can read **sensitive server files**.

Today was about learning:
- How path traversal works  
- How LFI occurs  
- How pentesters test it safely  

---

# ✅ TASK 1 — Understanding Path Traversal

📁 **Path Traversal** means accessing files outside the intended directory.

### Example vulnerable URL:
http://site.com/view.php?file=report.pdf



### Attacker test:
file=../../../../etc/passwd



### 🔹 Explanation:
- `../` → go one directory back  
- Repeating it allows access to root-level files  

If successful, the server may expose sensitive files.

---

# ✅ TASK 2 — Important Files to Know (Read-Only)

These are common files attackers test for **information disclosure**.

### 🐧 Linux
/etc/passwd
/etc/hosts
/etc/issue
/var/log/auth.log



### 🪟 Windows
C:\Windows\System32\drivers\etc\hosts
C:\Windows\win.ini



⚠️ Today I only learned **reading**, not exploiting or modifying files.

---

# ✅ TASK 3 — TryHackMe Beginner LFI Room

I completed beginner sections from ONE of these:

✔ File Inclusion  
✔ LFI Basics  
✔ OWASP Top 10 → File Inclusion section  

### Focus areas:
- What is LFI  
- Path traversal basics  
- Reading files using parameters  

Skipped advanced **RFI** for now.

---

# ✅ TASK 4 — Hands-On: Path Traversal Testing (Safe)

Using a TryHackMe vulnerable lab, I looked for parameters like:

?file=home
?page=about
?view=profile



Then tested traversal payloads:

../../../../etc/passwd
../etc/passwd
../../../etc/passwd



### 🔍 Observed responses:
- File contents displayed  
- Error messages  
- Blank pages  

Even error messages helped me understand server behavior.

---

# ✅ TASK 5 — Encoded Traversal Testing (Beginner)

When `../` was blocked, I tested encoded payloads:

..%2f..%2f..%2fetc%2fpasswd


and

%2e%2e%2f


### 🧠 Learning:
Some filters block raw traversal but fail against encoded input.

Today was about **observation**, not bypassing security.

---

# ✅ TASK 6 — Inspecting LFI Requests in Burp Suite

Steps followed:

1. Captured request in **Burp Proxy**  
2. Sent it to **Repeater**  
3. Modified the file parameter  
4. Sent multiple traversal variations  

This helped me practice **manual testing** and understand request-response behavior.

---

# 📝 TASK 7 — Notes in My Own Words

### 🔹 **What is Path Traversal?**  
A vulnerability that allows attackers to access files outside the intended directory by manipulating file paths.

---

### 🔹 **What is LFI (Local File Inclusion)?**  
A vulnerability where a website includes local files based on user input, allowing attackers to read sensitive files.

---

### 🔹 **Which files did I try to access?**  
Examples:
- `/etc/passwd`
- `/etc/hosts`
- `C:\Windows\win.ini`

---

### 🔹 **What response did I get?**  
File contents, errors, or blank pages — all useful for understanding vulnerability behavior.

---

### 🔹 **Why is LFI dangerous?**  
It can expose sensitive data, configuration files, credentials, and sometimes lead to remote code execution.

---

## 💭 How I Felt Today

- Path traversal logic became very clear  
- LFI felt powerful but dangerous  
- Burp Repeater helped with controlled testing  
- Gained confidence in manual vulnerability testing  

---

## 📌 Summary of Day 12

Today I learned:

- What Path Traversal is  
- How Local File Inclusion works  
- Important files attackers target  
- How to test traversal safely  
- How to analyze LFI using Burp  

This is a **critical vulnerability class** in web security.

---

**End of Day 12** 🚀