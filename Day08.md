# 🚀 Day 8 – Stored XSS, DOM XSS & Input Reflection

**Date:** 11/12/2025 
**Journey:** 100 Days of Cybersecurity  
**Focus:** Learning Stored XSS, DOM XSS, HTML Injection & reflection points.

---

## 🎯 What I Learned Today

After learning **Reflected XSS** earlier, today I focused on:

1. ⭐ Stored XSS  
2. ⭐ DOM XSS  
3. ⭐ HTML Injection  
4. ⭐ Understanding reflection points  

These attacks are extremely important in web hacking and appear commonly in real-world vulnerability reports.

---

# ✅ TASK 1 — Understanding 3 New Attack Types

### ⭐ 1. Stored XSS  
This is the **most dangerous** type of XSS.

- Your payload gets **saved in the database**  
- Anyone who visits the page gets affected  
- Impacts **all users**, not just you  

Example:

<script>alert('Hacked')</script>
yaml


If every user who opens the comments page sees a popup → **Stored XSS confirmed**.

---

### ⭐ 2. DOM XSS  
Occurs **inside the browser**, not on the server.

- JavaScript reads user input (URL / hash / parameters)
- Writes it into the page without sanitizing
- You inject JavaScript into the DOM, not the server response

Example URL:

http://example.com/page#name=khwahish

css

If the JS contains:

```javascript
document.write(location.hash.substring(1));
Then injecting:

cpp

#name=<script>alert(1)</script>
→ DOM XSS triggers.

⭐ 3. HTML Injection
Not JavaScript injection — just breaking or modifying page layout.

Example payloads:

css

<b>Hello</b>
<h1>Hacked!</h1>
If the website displays these as real HTML, you found HTML Injection.

✅ TASK 2 — TryHackMe Room: XSS Basics (Selected Sections)
I completed these from the “Cross-site Scripting” room:

✔ Introduction
✔ Stored XSS
✔ DOM XSS
✔ HTML Injection

Skipped advanced labs for later.

I compared how each XSS behaves differently and where the payload executes.

✅ TASK 3 — Hands-On: Stored XSS Testing
I used:
✔ DVWA (Security: LOW)
or
✔ TryHackMe XSS Playground
or
✔ Juice Shop comment box

Steps I followed:
Found an input field that stores data

Comment box

Feedback form

Username update field

Profile bio

Tested harmless HTML first:

css

<b>hello</b>
If the text appears in bold → HTML Injection confirmed.

Then tested stored XSS:

php-template

<script>alert('stored')</script>
Refreshed the page
→ If popup appears WITHOUT re-entering input → Stored XSS works

🧠 What I learned:
Stored XSS is persistent and affects ALL users.
Dangerous but easy to understand.

✅ TASK 4 — Hands-On: DOM XSS Testing
I looked for a page where URL data appears on the screen.
Example:

bash

http://target.com/#name=test
Then tested:

php-template

<script>alert(1)</script>
And also:

php-template

"><script>alert(1)</script>
Observations:
DOM XSS does NOT rely on the server

If JavaScript writes user input into the page → DOM XSS possible

Not all pages respond; that's normal

Today was about understanding how DOM XSS works.

✅ TASK 5 — Reflection Points
I tested simple text:

nginx

test123
Then observed where it appears:

In the URL

In the HTML body

In JavaScript on the page

Inside attributes

Inside comment sections

Reflection points help a hacker know where to inject payloads.

I wrote down 3 reflection points I observed.
📝 TASK 6 — Notes in My Own Words
🔹 What is Stored XSS?
When the injected script is stored in the database and executes for every user viewing the page.

🔹 What is DOM XSS?
XSS that happens inside the browser due to unsafe JavaScript code, not because of server-side vulnerabilities.

🔹 What is HTML Injection?
Injecting HTML tags to manipulate the page layout or structure without injecting JavaScript.

🔹 Where did I find reflection?
URL parameters

Comment box

Page title or body section

🔹 Which payloads worked today?
<b>hello</b>

<h1>Hacked</h1>

<script>alert('stored')</script> (in vulnerable environments)

💭 How I Felt Today
XSS concepts became much clearer

DOM XSS felt tricky but interesting

Stored XSS was fun to test

Reflection analysis increased my hacker mindset

📌 Summary of Day 8
Today I learned:

Difference between Stored, Reflected & DOM XSS

HTML Injection basics

How reflection works

How browsers interpret unsafe input

How hackers exploit unsafe input fields

This was one of the most important days of the XSS learning journey.

End of Day 8 🚀