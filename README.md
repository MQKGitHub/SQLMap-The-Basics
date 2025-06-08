### 🛡️ SQLMap: The Basics

**Room:** [SQLMap: The Basics — TryHackMe](https://tryhackme.com/room/sqlmapthebasics)  
**Status:** ✅ Completed  
**Date:** *07 June 2025* 

### 🎯 Objective
Understand SQL injection and learn how to exploit it using the SQLMap tool. This includes identifying SQLi vulnerabilities, extracting database contents, and automating the exploitation process through command-line techniques.

---

### 🗝️ Key Concepts  
- **SQL Injection (SQLi)** — Exploiting a vulnerability in a web app by injecting malicious SQL into database queries.  
- **GET vs POST Requests** — SQLi can be found in both; GET shows parameters in the URL, POST hides them in the body.  
- **Boolean-Based SQLi** — Uses logical conditions like `OR 1=1` to manipulate query results.  
- **Error-Based SQLi** — Forces errors in SQL queries to leak database info.  
- **Time-Based SQLi** — Uses delays (e.g., `SLEEP(5)`) to confirm injection through response timing.  
- **Union-Based SQLi** — Uses `UNION SELECT` to merge data from multiple queries into one response.  
- **SQLMap** — An automated tool that simplifies SQLi exploitation with powerful flag-based commands.

---

### 🛠️ Tools Used
- **SQLMap** — Main tool used to detect and exploit SQLi vulnerabilities through automated queries.  
- **Browser Dev Tools (Network Tab)** — Used to inspect GET/POST requests and identify injectable parameters.  
- **TryHackMe AttackBox** — Used as the testing environment for practical exploitation.

---

### ⚠️ Challenges Faced
- The login page didn’t display parameters in the URL, so I had to inspect browser traffic to extract the correct GET request.
- Initial scans didn’t return much, but using `--level=5` enabled deeper testing and successful exploitation.
- Needed to understand and respond to SQLMap’s interactive prompts during testing.

---

### 🧠 What I Learned
- Learned how SQLi works by injecting malicious input into an unsanitised SQL query.
- Gained hands-on experience using SQLMap flags like `--dbs`, `--tables`, and `--dump` to extract database contents.
- Understood how to test both GET and POST requests using SQLMap.
- Realised how dangerous a simple login form can be when it doesn't validate input properly.

---

### 🌐 Real-World Application:
> SQL injection is one of the most common and dangerous web vulnerabilities. Tools like SQLMap help penetration testers identify and exploit these flaws, but defenders also use this knowledge to patch vulnerabilities and monitor for suspicious behaviour (e.g., strange SQL queries or login attempts).

---

### 💭 Reflections:
- This room showed just how much damage can be done with a single vulnerable input field.
- SQLMap was much more powerful and user-friendly than I expected — especially with the `--wizard` mode for beginners. 
