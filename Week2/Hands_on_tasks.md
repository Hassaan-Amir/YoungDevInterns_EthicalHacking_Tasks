#  Hands On Task ... Week 2

This week includes two practical exercises: cracking a password-protected zip file using a dictionary attack, and performing thorough enumeration on a vulnerable Linux system and web environment.

---

## Task 1: Crack a Password-Protected ZIP

###  Objective  
Use a dictionary attack to obtain the password of a protected ZIP using the `rockyou.txt` wordlist.

###  Tools Used  
- `zip2john` – Converts ZIP file hash into a John-readable format  
- `John the Ripper` – Performs dictionary attack  
- Wordlist: /usr/share/wordlists/rockyou.txt

![Password Cracking Screenshot]<img width="1164" height="348" alt="9" src="https://github.com/user-attachments/assets/57a7dc2a-9083-4350-bd0c-2437bc43c92d" />


---

##  Task 2: Perform Enumeration on a Vulnerable Linux System

###  Objective

Gather imporant information about a target system to uncover weak points, user details, and services that could be exploited.

---

### 1. Network & OS Enumeration (Using Nmap)

```bash
nmap -sV -O <target_ip>           # Version + OS detection
nmap --script vuln <target_ip>  # Run NSE script
```

![Nmap Screenshot]<img width="984" height="491" alt="nmap" src="https://github.com/user-attachments/assets/8a0bb242-e624-4863-91d5-b0e149eb8ed9" />


![Nmap Screenshot]<img width="717" height="217" alt="nmap2" src="https://github.com/user-attachments/assets/d856a6ca-e4a1-4f73-a958-3880036d5598" />


---

###  2. Web Enumeration (Nikto, Dirb, Gobuster)

Made a http server of my target machine and used tools

```bash
nikto -h http://192.168.87.129
dirb http://192.168.87.129
gobuster dir -u http://192.168.87.129 -w /usr/share/wordlists/dirb/common.txt
```
![nikto Screenshot]<img width="1299" height="456" alt="nikto" src="https://github.com/user-attachments/assets/83d31e02-6ff8-4f1c-afdd-97e4773afea4" />


![dirb Screenshot]<img width="499" height="417" alt="dirb" src="https://github.com/user-attachments/assets/fc792a05-63a4-4c0c-b5c3-6452e58ef163" />


![gobuster Screenshot]
<img width="686" height="404" alt="gobuster" src="https://github.com/user-attachments/assets/5af61c9b-1234-48c4-a5d1-f504999b66e7" />

---

## Learnings

Gained hands-on experience with dictionary attacks to uncover passwords from encrypted ZIP files.

Conducted in-depth system enumeration by identifying active services, operating system information, and hidden web directories.

Enhanced proficiency in command-line operations and reconnaissance techniques using industry-standard tools in a simulated vulnerable environment.

---
