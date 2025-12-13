# 🚀 Day 10 – Cookies, Sessions & Parameter Testing

**Date:** 13/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Understanding cookies, sessions, parameter manipulation & authorization logic.

---

## 🎯 Why Day 10 Is Important

Most real-world web vulnerabilities are found NOT by brute force, but by:

- Manipulating cookies  
- Understanding session handling  
- Modifying parameters  
- Testing authorization & access control logic  

Today was about **thinking like a hacker**, not attacking blindly.

---

# ✅ TASK 1 — Understanding Cookies & Sessions

### 🍪 Cookies
Cookies are small pieces of data stored in the browser.

Examples:
sessionid=abc123
role=user

Cookies are used for:
- Login tracking  
- User roles  
- Preferences  
- Session identification  

---

### 🔐 Sessions
Sessions are stored on the **server side** and mapped to a cookie.

Basic rule:
👉 If you can manipulate a cookie, you may be able to hijack or alter a session.

Understanding sessions is critical for:
- Authentication bypass  
- Session hijacking  
- Privilege escalation  

---

# ✅ TASK 2 — Observing Cookies in Burp Suite

Steps followed:

1. Opened **Burp Suite**  
2. Proxy → **Intercept ON**  
3. Visited a TryHackMe web app (Juice Shop recommended)  
4. Captured a request  

Observed headers like:

Cookie: session=eyJ1c2VyIjoidXNlciJ9


### 🔍 My observations:
- Cookie name  
- Cookie value  
- Value type:
  - Plain text  
  - Base64 encoded  
  - Random string  

❗ No modification yet — only observation.

---

# ✅ TASK 3 — Modifying Cookie (Safe Test)

Steps:

1. Sent the captured request to **Repeater**  
2. Modified cookie value slightly:

session=abcd1234


3. Clicked **Send**

### 🔍 Observed:
- Was I logged out?  
- Did the page change?  
- Did the server reject the request?  
- Did an error message appear?  

This helped me understand how well the application validates sessions.

---

# ✅ TASK 4 — Parameter Testing (Logic Testing)

I identified parameters like:

id=1
user=khwahish
role=user

Then tested logical changes:

- `id=1` → `id=2`  
- `role=user` → `role=admin`  

Requests were sent using **Burp Repeater**.

### 🧠 What I was testing:
- IDOR (Insecure Direct Object Reference)  
- Authorization flaws  
- Broken access control  

Even if no vulnerability appeared, the **testing mindset** was the key learning.

---

# ✅ TASK 5 — TryHackMe Beginner Room

I completed beginner-level sections from one of these:

✔ Authentication Bypass  
✔ IDOR  
✔ Session Management  
✔ Broken Authentication  

Focused only on understanding logic, not exploitation depth.

---

# 📝 TASK 6 — Notes in My Own Words

### 🔹 **Difference between Cookies & Sessions**
- Cookies are stored in the browser  
- Sessions are stored on the server  
- Cookies often contain session identifiers  

---

### 🔹 **What happened when I modified the cookie?**
The server behavior changed (logout / error / denial), showing how session validation works.

---

### 🔹 **What parameters did I test?**
- User IDs  
- Roles  
- Object references  

---

### 🔹 **What is IDOR (simple words)?**
IDOR happens when an application lets you access or modify someone else’s data just by changing an ID value.

Example:
id=1 → id=2


---

## 💭 How I Felt Today

- Understood how real vulnerabilities are discovered  
- Cookie manipulation felt powerful  
- Authorization testing changed my hacking mindset  
- Feeling more confident in web pentesting logic  

---

## 📌 Summary of Day 10

Today I learned:

- How cookies & sessions work  
- How to observe cookies using Burp  
- How session validation works  
- How to test parameters logically  
- What IDOR and authorization issues look like  

This day strengthened my **real-world web hacking thinking**.

---

**End of Day 10** 🚀