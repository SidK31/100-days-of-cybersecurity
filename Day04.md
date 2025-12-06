\# 🚀 Day 4 – Web Enumeration (Beginner-Friendly Start)



\*\*Date:\*\* 07/12/2025  

\*\*Journey:\*\* 100 Days of Cybersecurity  

\*\*Focus:\*\* Learning real-world web enumeration using Gobuster  



---



\## 🎯 What I Learned Today



Web Enumeration is the process of discovering \*\*hidden pages, folders, files, and weaknesses\*\* in a website.



Before a hacker can attack a website, they must know \*\*what exists\*\* on the web server.



Today, I learned how to identify:



\- Hidden directories  

\- Admin/login pages  

\- Upload sections  

\- Backup files  

\- Config files  



This is the first real step toward \*\*web hacking\*\*.



---



\# ✅ TASK 1 — Understanding Web Enumeration



Web Enumeration means mapping out a website by discovering:



\- `/admin`

\- `/login`

\- `/uploads`

\- `/images`

\- `/backup.zip`

\- `/config`



Think of it as \*\*finding all doors and windows of a building before entering it.\*\*



I read the TryHackMe introduction for:

✔ “What is Web Enumeration?” (or similar room)



---



\# ✅ TASK 2 — Installed Gobuster



Gobuster is a fast directory-bruteforcing tool used by pentesters to find hidden content on websites.



Checked if installed:



gobuster --help



If not installed:



sudo apt install gobuster





Installation completed successfully.



---



\# ✅ TASK 3 — My FIRST Gobuster Scan



I started a TryHackMe web machine:



✔ Vulnversity  

or  

✔ Basic Pentesting  



Then ran the directory enumeration command:



gobuster dir -u http://<IP> -w /usr/share/wordlists/dirb/common.txt





\### 🔍 What this command does:

\- `dir` → directory enumeration  

\- `-u` → target website URL  

\- `-w` → wordlist used for discovery  



\### 🧠 What I observed:



Directories discovered (examples):



\- `/admin`

\- `/images`

\- `/uploads`

\- `/css`

\- `/js`

\- `/config`

\- `/backup`



Each one of these can be a potential \*\*entry point\*\* for a hacker.



This gave me my \*\*first hacker’s map\*\* of a website.



---



\# ✅ TASK 4 — Learned Basic HTTP Response Codes



Understanding HTTP response codes is extremely important for web enumeration.



| Code | Meaning | Importance |

|------|---------|------------|

| \*\*200\*\* | OK | Page exists → explore |

| \*\*301/302\*\* | Redirect | Could lead to login/admin |

| \*\*403\*\* | Forbidden | 🔥 A \*very\* interesting page (restricted area) |

| \*\*404\*\* | Not Found | Nothing useful |

| \*\*500\*\* | Server Error | Misconfigured → potential exploit |



While running Gobuster, I identified and noted which responses appeared beside each directory.



---



\# ✅ TASK 5 — TryHackMe Room: Web Enumeration (Beginner)



I completed beginner sections of:



✔ \*\*Web Fundamentals\*\*



Completed:



\- What is a web server  

\- Basic web enumeration  

\- Directory busting  



Skipped exploitation (for now).



This gave me a solid base for real web pentesting.



---



\# 📝 TASK 6 — Notes (In My Own Words)



\### 🔹 \*\*What is directory enumeration?\*\*

It is the technique to discover hidden directories \& files on a web server using tools like Gobuster or Dirb.



---



\### 🔹 \*\*What does `gobuster dir` do?\*\*

It brute-forces directory names using a wordlist and checks which ones exist.



---



\### 🔹 \*\*Common hidden folders I found today\*\*

\- `/admin`

\- `/uploads`

\- `/images`

\- `/backup`

\- `/config`

\- `/private`

\- `/css`

\- `/js`



These folders often contain sensitive data such as credentials, config files, or upload features.



---



\## 💭 How I Felt Today



\- Web enumeration was exciting and felt like real hacking  

\- Gobuster was easy to use  

\- Learned how to identify hidden entry points  

\- Feeling confident for deeper enumeration on Day 5 🔥  



---



\## 📌 Summary of Day 4



Today I learned:

\- What web enumeration is  

\- How hackers discover hidden folders  

\- How to install \& use Gobuster  

\- How to interpret HTTP responses  

\- Beginner-level web enumeration through TryHackMe  



This is the foundation of \*\*web hacking and website analysis\*\*.



---



\*\*End of Day 4\*\* 🚀



