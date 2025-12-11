# 🚀 Day 7 – Introduction to SQL Injection (Beginner-Friendly)

**Date:** 10/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Understanding SQL Injection basics, beginner payloads & safe testing.

---

## 🎯 What I Learned Today

Today I entered one of the MOST important vulnerabilities in web hacking:

👉 **SQL Injection (SQLi)**  
This vulnerability allows hackers to change how a website communicates with its database.

After learning parameters, Burp Suite, GET/POST, and request manipulation, SQLi is the natural next step.

---

# ✅ TASK 1 — SQL Injection Explained in SIMPLE Words

SQL Injection happens when:

1. A website takes your input  
2. Puts it inside a database query  
3. BUT does **not** filter or sanitize it  
4. So your input becomes **SQL code**  

### 🔥 Example

Normal query:



SELECT * FROM users WHERE username='khwahish' AND password='1234';


Hacker input:



password: ' OR 1=1 --


Database becomes:



SELECT * FROM users WHERE username='khwahish'
AND password='' OR 1=1 --';


`OR 1=1` is ALWAYS true → login bypass.

This is the core idea behind SQL Injection.

---

# ✅ TASK 2 — Beginner SQLi Payloads I Learned Today

I memorized these 5 basic payloads:

### 1️⃣ Test for breaking the query


'


### 2️⃣ Double quote test


"


### 3️⃣ Universal login bypass


' OR 1=1 --


### 4️⃣ Comment variations


' --
' #


### 5️⃣ Check if site reacts logically


' AND '1'='1


These are enough for beginner labs on TryHackMe and DVWA.

---

# ✅ TASK 3 — Captured & Modified Login Request in Burp

I used:

✔ TryHackMe SQL Injection Beginner Room  
OR  
✔ DVWA (Low Security Mode)

Steps:

1. Turned **Intercept ON**  
2. Entered:



username = test
password = test


3. Burp captured:



POST /login HTTP/1.1
username=test&password=test


4. Sent to **Repeater**  
5. Modified:



username=admin&password=' OR 1=1 --


6. Clicked **Send** and observed:

### 🔍 What I looked for:
- Did login succeed?  
- Did page behavior change?  
- Did server return SQL errors?  
- Did it redirect to a dashboard?  

Even if nothing happened, the learning was understanding the mechanics.

---

# ✅ TASK 4 — TryHackMe SQL Injection (Beginner Room)

I completed sections:

✔ What is SQL?  
✔ What is SQL Injection?  
✔ Why SQLi occurs  
✔ Testing SQLi  
✔ Simple login bypass  
✔ Basic payload usage  

Skipped advanced topics for later:

❌ Blind SQLi  
❌ Time-based SQLi  
❌ UNION-based enumeration  

Today was purely foundational.

---

# ✅ TASK 5 — Beginner Manual SQLi Test

On a search box or login form, I tested:



'


If I saw:

- SQL error  
- MySQL error  
- Broken page  
- Unexpected output  

→ It indicates potential SQL injection.

I also noted where errors appeared and how the site responded.

---

# 📝 TASK 6 — Notes in My Own Words

### 🔹 **What is SQL Injection (simple definition)?**  
SQL Injection happens when the website puts user input into a database query without filtering it, allowing attackers to run unwanted SQL commands.

---

### 🔹 **What payloads did I try today?**
- `'`  
- `"`  
- `' OR 1=1 --`  
- `' --`  
- `' AND '1'='1`  

---

### 🔹 **What happened when I used `' OR 1=1 --`?**  
The server response changed, indicating the logic of the query was altered.  
Sometimes it bypasses login, sometimes shows errors — both are signs of SQLi.

---

### 🔹 **What TryHackMe tasks did I complete?**  
- SQL Injection beginner room  
- Basic login bypass  
- Understanding SQL queries  
- Identifying vulnerable parameters  

---

## 💭 How I Felt Today

- SQLi felt powerful and logical  
- Learning payloads was fun  
- Burp + SQLi combination started making sense  
- Feeling motivated for deeper SQLi challenges ahead  

---

## 📌 Summary of Day 7

Today I learned:

- What SQL Injection is  
- Why it happens  
- Basic SQLi payloads  
- How to intercept and manipulate login data  
- How SQL queries break with wrong input  
- How to test SQLi in beginner labs  

A very important step in becoming a real web pentester.

---

**End of Day 7** 🚀