# 🚀 Day 6 – Parameters, Burp Manipulation & Intro to XSS

**Date:** 09/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Understanding parameters, modifying requests in Burp, and learning beginner-level XSS concepts.

---

## 🎯 What I Learned Today

Today was my first real introduction to manipulating web requests and understanding how data flows inside a website.

I practiced:

- Identifying URL parameters  
- Capturing parameters in Burp  
- Modifying values using Repeater  
- Observing server responses  
- Testing harmless XSS payloads  

These concepts are the base of **XSS, SQL Injection, authentication bypass, and web hacking**.

---

# ✅ TASK 1 — What Are URL Parameters?

Every website receives data through:

### ✔ URL Parameters (Query Strings)

Example:

http://example.com/search.php?query=apple

- `query` → parameter  
- `apple` → user input value  

### ✔ Form Fields  
(username, password, comments, search boxes)

### ✔ Cookies  
(session tokens, tracking data)

### ❗ Important  
Hackers manipulate these values to trigger vulnerabilities.

Today I learned how to identify these values clearly.

---

# ✅ TASK 2 — Captured Parameters in Burp Suite

I started a TryHackMe machine:

✔ Web Fundamentals  
✔ Juice Shop (Beginner Mode)  
✔ OWASP Top 10 (XSS tasks only)

Steps I followed:

1. Turned **Intercept ON**  
2. Visited a page with a search/login form  
3. Entered input like `test`  
4. Burp captured requests such as:

### Example GET Request:
GET /search?query=test HTTP/1.1

### Example POST Request:
POST /login HTTP/1.1
username=test&password=123


### 🔍 My Goal Today:
- Observe parameter **names**  
- Observe parameter **values**  
- Understand how my data travels from browser → server  

No exploitation yet — only understanding.

---

# ✅ TASK 3 — Manipulated a Request Using Burp Repeater

Steps I followed:

1. Captured a request  
2. Right-click → **Send to Repeater**  
3. Modified the parameter

Example:

query=test123

Changed to:
query=hello


4. Clicked **Send**  
5. Observed how the server responded

### 🧠 What I learned:
Changing parameters = changing how websites behave.

This is the core of:

- XSS  
- SQL Injection  
- Authentication bypass  
- Business logic hacking  

---

# ⭐ NOW THE FUN PART  
# ✅ TASK 4 — My First Intro to XSS (Safe Testing)

XSS = Cross-Site Scripting  
It happens when a website displays user input without cleaning or escaping it.

### Step 1 — Harmless Input Test
Typed:

<test> ```

If the website shows:
<test>
➡ Possible XSS vulnerability.

Step 2 — Harmless XSS payload

Typed:
<script>alert(1)</script>
✅ TASK 5 — TryHackMe XSS Room (Beginner)

I completed:

✔ What is XSS?
✔ Reflected XSS
✔ Basic exploitation

Skipped advanced ones for later:

❌ Stored XSS
❌ DOM XSS

This gave me a beginner-friendly introduction to real-world XSS attacks.

📝 TASK 6 — Notes in My Own Words
🔹 What is a URL parameter?

A value in the URL that sends data to the server.
Example: /search?query=apple → query is the parameter.

🔹 GET vs POST

GET sends data in the URL

POST sends data in the body (not visible in URL)

🔹 What is XSS (simple definition)?

A vulnerability where a website displays user input without cleaning it, allowing attackers to run JavaScript inside the victim’s browser.

🔹 What happened when I changed the request in Repeater?

The website responded differently because the parameter value changed.
This showed me how input manipulation affects website behavior — the foundation of web hacking.

💭 How I Felt Today

Manipulating requests felt powerful 🔥

Understood how hackers test parameters

XSS concepts were clear and exciting

Feeling more confident using Burp Suite

📌 Summary of Day 6

Today I learned:

What URL parameters are

How GET & POST data works

How to capture & modify requests

Basics of XSS

How Burp Repeater helps in vulnerability testing

One of the most important days in my web hacking journey.

End of Day 6 🚀
