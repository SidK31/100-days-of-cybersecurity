# 🚀 Day 5 – Burp Suite Basics + Intercepting Web Traffic

**Date:** 08/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Understanding Burp Suite, intercepting requests, and learning basic manual testing.

---

## 🎯 What I Learned Today

Burp Suite is one of the MOST important tools in web hacking.  
Today I learned how to:

- Intercept HTTP requests  
- Modify & replay requests  
- Use Burp as a proxy  
- Explore Repeater  
- See how browsers talk to websites  

This is the foundation of **web application hacking**.

---

# ✅ TASK 1 — What Burp Suite Does

Before using Burp Suite, I understood the concept:

### 🔥 **Burp Suite = The Middleman**  
It sits between:

Browser → Burp → Website  
Website → Burp → Browser  

This allows hackers to:

- View all traffic  
- Edit requests  
- Replay requests  
- Brute-force parameters  
- Detect vulnerabilities  

Today was conceptual only — no exploitation.

---

# ✅ TASK 2 — Started Burp Suite & Setup Browser Proxy

### Step 1 — Opened Burp Suite
In Kali:
burpsuite

Selected:

- Temporary Project  
- Start Burp  

---

### Step 2 — Enabled Proxy Intercept

Burp tab:

    Proxy → Intercept → Intercept ON
    
---

### Step 3 — Configured Browser to Use Burp

In Firefox (inside Kali):

Settings → Network Settings → Manual Proxy Configuration

HTTP Proxy: 127.0.0.1
Port: 8080
Use this proxy for all protocols ☑️

Now Burp successfully started capturing traffic from the browser.

---

# ✅ TASK 3 — My First Intercepted Request

I opened:

✔ TryHackMe “Web Fundamentals”  
OR  
✔ Juice Shop (beginner mode)  
OR even example.com  

Then:

- Went to a webpage  
- Burp intercepted the request  
- Turned Intercept OFF → request forwarded  
- Turned Intercept ON again  
- Refreshed the page  

### 🔍 What I observed:

A typical request looked like this:

GET / HTTP/1.1
Host: <IP>
User-Agent: Mozilla/5.0
Accept: text/html
Connection: keep-alive

This was my **first real hacker moment** — seeing raw HTTP traffic.

No exploitation yet.  
Only understanding structure.

---

# ✅ TASK 4 — Sent a Request to Repeater

Repeater = Manual testing tool for hacking.

Steps I followed:

1. Turned Intercept ON  
2. Captured a request  
3. Right click → **Send to Repeater**  
4. Opened the **Repeater tab**  
5. Clicked **Send**  
6. Observed server responses  

### 🔍 What I learned:

Hackers use Repeater to:

- Test login forms  
- Test SQL Injection  
- Test XSS  
- Test parameter manipulation  
- Replay requests repeatedly  

Today I only explored the response structure.

---

# ✅ TASK 5 — TryHackMe Burp Basics Room

Completed beginner sections of:

✔ **"Burp Suite: The Basics"**  
or  
✔ **"Burp Introduction"**

I learned:

- What Burp does  
- Proxy usage  
- Intercept  
- Repeater  
- Basic analysis  

Skipped advanced tools:

❌ Intruder  
❌ Decoder  
❌ Comparer  
❌ Extensions  

Those will come later.

---

# 📝 TASK 6 — Notes in My Own Words

### 🔹 **What is a proxy?**  
A server/tool that sits between the browser and website to inspect, modify, or block traffic.

---

### 🔹 **What is Repeater used for?**  
Repeater allows me to manually edit and resend HTTP requests to test how the server responds — useful for testing vulnerabilities.

---

### 🔹 **What did my first request look like?**  
It was a GET request with headers like:

- Host  
- User-Agent  
- Accept  
- Connection  

---

### 🔹 **Headers I observed:**  
- **Host** – website IP or domain  
- **User-Agent** – browser info  
- **Cookies** – session data  
- **Accept** – types of content the browser accepts  
- **Connection** – keep-alive/close  

---

## 💭 How I Felt Today

- Burp Suite felt powerful  
- Seeing raw traffic was exciting 🔥  
- Understood how hackers intercept & test websites  
- Feeling ready for future advanced Burp usage  

---

## 📌 Summary of Day 5

Today I learned:

- What Burp Suite is  
- How proxy interception works  
- How to capture & modify HTTP requests  
- Basic usage of Repeater  
- How to observe request structure  

Burp Suite is the **heart of web pentesting**, and this was a very important foundational day.

---

**End of Day 5** 🚀

