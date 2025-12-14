# 🚀 Day 11 – File Upload Vulnerabilities (Beginner-Friendly)

**Date:** 14/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Understanding file upload logic, validation checks & safe testing techniques.

---

## 🎯 Why File Upload Vulnerabilities Are Important

Many real-world websites allow users to upload files such as:

- Profile photos  
- Resumes  
- Assignments  
- Documents  

If upload validation is weak, attackers may upload **malicious files**.

Today was about learning **how hackers analyze upload functionality**, not blindly exploiting it.

---

# ✅ TASK 1 — How File Upload Works

When a file is uploaded, the server may check:

- **File extension** (`.jpg`, `.png`, `.pdf`)  
- **MIME type** (`image/jpeg`)  
- **File content**  
- **File name**  
- **File size**  

### 🔥 Key Point  
If any of these checks are weak or missing → **file upload vulnerability exists**.

Understanding these checks is critical before exploitation.

---

# ✅ TASK 2 — Common File Upload Bypass Techniques (Theory)

I studied common beginner-level bypass concepts (theory only).

### 🔹 Extension Tricks
shell.php.jpg
shell.php.png
shell.jpg.php


### 🔹 Case Sensitivity
shell.PHP
shell.pHp



### 🔹 Null Byte (Concept Only)
shell.php%00.jpg



### 🔹 MIME Type Manipulation
Changing request header:

Content-Type: image/jpeg



Even when the file extension is not an image.

⚠️ Today I did NOT upload real shells — only learned how detection works.

---

# ✅ TASK 3 — TryHackMe File Upload Room

I completed beginner-level sections from one of these:

✔ Upload Vulnerabilities  
✔ File Upload Vulnerability  
✔ Vulnversity (Upload section only)  

### Focused on:
- Understanding server-side validation  
- Observing allowed extensions  
- Seeing how the server reacts to invalid uploads  

Skipped advanced exploitation.

---

# ✅ TASK 4 — Inspecting Upload Requests in Burp Suite

Steps followed:

1. Opened **Burp Suite**  
2. Proxy → **Intercept ON**  
3. Uploaded a normal file (`test.jpg`)  
4. Captured the request  

### Observed request structure:

Content-Disposition: form-data
filename="test.jpg"
Content-Type: image/jpeg



### 🔍 What I analyzed:
- Filename  
- Content-Type  
- Request structure  
- Server response  

This is how pentesters understand **upload logic internally**.

---

# ✅ TASK 5 — Safe Testing (No Exploitation)

I performed safe validation tests using **Burp Repeater**.

### Tests performed:

#### 🔹 Filename change
test.jpg → test.jpg.php



#### 🔹 MIME type change
image/jpeg → application/php



### 🔍 Observations:
- Upload rejected?  
- Error message shown?  
- Upload accepted?  

This helped me understand how strict the server validation is.

No exploitation attempted — only behavior analysis.

---

# 📝 TASK 6 — Notes in My Own Words

### 🔹 **What checks do servers use for file upload?**
File extension, MIME type, file content, filename, and file size.

---

### 🔹 **What is MIME type?**
A header that tells the server what type of file is being uploaded (e.g., image/jpeg).

---

### 🔹 **What happened when I changed the filename?**
The server response changed (rejection or error), showing extension-based validation.

---

### 🔹 **What happened when I changed the Content-Type?**
The server behavior showed whether MIME type validation was enforced.

---

## 💭 How I Felt Today

- File upload logic became very clear  
- Burp Suite helped me see how uploads actually work  
- Learned how hackers think before exploiting uploads  
- Feeling more confident with web vulnerability analysis  

---

## 📌 Summary of Day 11

Today I learned:

- How file upload systems work  
- Common upload bypass techniques (theory)  
- How to analyze uploads using Burp  
- How servers validate files  
- Why upload vulnerabilities are dangerous  

This knowledge is essential for **web exploitation and bug bounty hunting**.

---

**End of Day 11** 🚀