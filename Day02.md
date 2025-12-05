# 🚀 Day 2 – Linux for Hackers + Basic Commands Mastery

**Date:** 05/12/2025  
**Journey:** 100 Days of Cybersecurity  
**Focus:** Becoming comfortable with Linux & building hacker muscle memory.

---

## 🎯 Goal of Day 2
- Learn the Linux environment  
- Practice essential commands used by every hacker  
- Build confidence using the terminal  
- Complete Linux Fundamentals Part 1 on TryHackMe  

---

## ✅ TASK 1 — Kali Linux Setup / Usage

Today I worked with Kali Linux.

Options explored:  
- Kali Linux VM (VirtualBox)  
- Kali WSL (Windows Subsystem for Linux)  

If Kali was already installed → I continued with it.  
If not → installation options were reviewed.

---

## ✅ TASK 2 — Essential Linux Commands I Practiced

I opened the terminal in Kali Linux and practiced these commands:

### 🔥 **File & Directory Commands**
| Command | What It Does |
|--------|---------------|
| `pwd` | Shows current directory path |
| `ls -l` | Lists files with detailed info |
| `cd` | Change directory |
| `mkdir test` | Create folder |
| `rmdir test` | Delete empty folder |
| `touch file.txt` | Create empty file |
| `cat file.txt` | View file content |
| `rm file.txt` | Delete file |

---

### 🔥 **System Commands**
| Command | Meaning |
|--------|---------|
| `whoami` | Shows current logged-in user |
| `id` | Shows user ID & group info |
| `uname -a` | Shows OS & kernel version |
| `hostname` | Shows machine name |

---

### 🔥 **Permissions Commands**
| Command | Meaning |
|--------|---------|
| `chmod 755 file.txt` | Changes permission of a file |
| `chown user:user file.txt` | Changes ownership of a file |

---

### 🔥 **Process & Network Commands**
| Command | Meaning |
|--------|---------|
| `ps aux` | Shows all running processes |
| `top` | Shows real-time process usage |
| `ifconfig` | Shows network interfaces |
| `ip a` | Shows IP address details |
| `who` | Shows logged-in users |

---

### 🎯 My Objective
Understand what each command does, when it is used, and why hackers rely on it.

---

## ✅ TASK 3 — TryHackMe: Linux Fundamentals Part 1

I completed the **Linux Fundamentals Part 1** room on TryHackMe.

Topics learned:
- Linux file system structure  
- Commands & syntax  
- File permissions  
- Navigation using terminal  
- Basic command-line operations  

This room is extremely important because Linux is the foundation of hacking.

---

## 📝 TASK 4 — Notes in My Own Words

### 🔹 **What is the Linux file system?**  
A structured way in which Linux organizes files & folders.  
Everything starts from `/` (root directory).  
Key directories:  
- `/home` → user files  
- `/etc` → configuration files  
- `/var` → logs  
- `/bin` → essential commands  

---

### 🔹 **Difference between absolute & relative paths**
- **Absolute path:** Starts from `/` (root), e.g., `/home/user/Desktop`  
- **Relative path:** Starts from current directory, e.g., `../Documents`

---

### 🔹 **What does `chmod` do?**  
Changes permissions (read, write, execute) for users, groups, and others.

Example:  
`chmod 755 file` = owner full permission, others read + execute.

---

### 🔹 **What does `ps aux` show?**  
Shows *all* running processes on the system with details like:  
- Process ID  
- User  
- CPU/Memory usage  
- Process command  

Very useful for monitoring, debugging, and finding suspicious activity.

---

## 💭 How I Felt Today
- Linux commands are getting easier  
- Terminal feels more comfortable now  
- TryHackMe Linux Room gave me strong fundamentals  
- Feeling more confident for Day 3 💪  

---

## 📌 Summary of Day 2
Today was all about Linux — the operating system hackers live in.  
I learned commands, understood permissions, explored the file system, and practiced on TryHackMe.

---

**End of Day 2** 🚀
