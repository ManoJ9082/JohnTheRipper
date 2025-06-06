# 🔐 Password Cracking & Hash Analysis with JohnTheRipper  

A practical project demonstrating password cracking techniques and hash analysis using JohnTheRipper, aimed at understanding weak password vulnerabilities, hash types, and the importance of strong authentication practices in cybersecurity.

---

## 📖 Table of Contents

- [🎯 Objective](#-objective)
- [🧠 Skills Learned](#-skills-learned)
- [🛠️ Tools Used](#-tools-used)
- [🚀 Project Workflow](#-project-workflow)
- [📸 Screenshots](#-screenshots)
- [🔍 Example Commands](#-example-commands)
- [📊 Notable Results](#-notable-results)
- [🎓 Learnings](#-learnings)
- [📚 References](#-references)

---

## 🎯 Objective  

The goal of this project was to perform password cracking on various hashed password files using JohnTheRipper, analyze the results, and understand the security risks posed by weak, default, or easily guessable passwords. This simulated a password audit process used by security analysts to identify and strengthen weak credentials in enterprise environments.

---

## 🧠 Skills Learned  

- Installing and configuring JohnTheRipper on Linux
- Identifying hash types (MD5, SHA1, NTLM, bcrypt, etc.)
- Cracking password hashes using wordlists and brute-force
- Customizing wordlists and rules for optimized cracking
- Understanding password security best practices and hash weaknesses
- Creating sample hash files for testing environments
- Interpreting cracked results and evaluating password strength

---

## 🛠️ Tools Used  

- **JohnTheRipper (Community Edition)**
- **Kali Linux / Parrot OS**
- **RockYou.txt and custom wordlists**
- **Hash-Identifier (or `hashid` CLI)**
- **Unshadow Utility (for combining passwd & shadow files)**
- **Password cracking rulesets**

---

## 🚀 Project Workflow  

1. Installed and configured JohnTheRipper.
2. Created test hash files (MD5, SHA1, NTLM, bcrypt).
3. Used hash identification tools to verify hash types.
4. Ran password cracking operations with default and custom wordlists.
5. Applied cracking rules to improve success rates.
6. Analyzed cracked password results and identified weak patterns.
7. Documented findings and password policy recommendations.

---

## 📸 Screenshots  

> 📌 **Running JohnTheRipper against a hash file**
![hash](https://github.com/user-attachments/assets/7dc887b9-6503-49f9-a1ce-00ec831a7e81)

> 📌 **zip2john**
![zipjohn](https://github.com/user-attachments/assets/70a6b7bf-d0f7-40ee-bbda-d550e7431b43)

> 📌 **Cracked password results**
![rockyou](https://github.com/user-attachments/assets/7c3e98d4-7a45-465f-8922-d4429bb2dec8)



## 🔍 Example Commands  

- Basic cracking:-
  john hashes.txt --wordlist=/usr/share/wordlists/rockyou.txt

- Show cracked passwords:-
  john --show hashes.txt

- Run with custom rules:-
  john --rules --wordlist=customlist.txt hashes.txt

- Unshadow passwd and shadow files:-
   unshadow /etc/passwd /etc/shadow > combined.txt
  
## 📊 Notable Results

- Successfully cracked 85% of MD5 hashes within 5 minutes using rockyou.txt.
- Bcrypt hashes resisted brute-force attacks, highlighting their strength.
- Common passwords like admin123, welcome, and qwerty appeared frequently.
- Rule-based cracking improved success rate by 12%.


## 🎓 Learnings

- Weak passwords remain a massive security risk.
- MD5 and SHA1 hashes can be cracked quickly with standard wordlists.
- Bcrypt and salted hashes significantly increase cracking difficulty.
- Custom wordlists and cracking rules enhance cracking efficiency.
- Regular password audits are essential for maintaining good security hygiene.


## 📚 References

- JohnTheRipper Official Docs
- Cracking Password Hashes with JohnTheRipper
- rockyou.txt Wordlist


🚀 Author: Manoj Mothukuru
