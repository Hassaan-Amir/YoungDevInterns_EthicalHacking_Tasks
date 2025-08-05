# Hands-On Task – Vulnerable VM Exploitation (Mr. Robot)

As part of Week 4 of the **YoungDevInterns Ethical Hacking Program**, I completed a hands-on challenge by exploiting Mr robot from VulnHub.

## Target Machine
- **VM:** Mr. Robot (VulnHub)
- **Goal:** Achieve root access

## Overview of Approach

### 1. Initial Reconnaissance
- Scanned target using `nmap` to identify open ports and services
- Detected Apache server running a WordPress site
- Used `gobuster` to enumerate hidden directories

### 2. Exploitation
- Found credentials through exposed WordPress files and pages
- Accessed the WordPress admin dashboard

### 3. Shell Access
- Listened for incoming connection with `netcat`
- Received a reverse shell and obtained limited user access

### 4. Privilege Escalation
- Inspected system for misconfigured SUID binaries and cron jobs
- Exploited a vulnerable script to escalate privileges
- Successfully gained root access

## Tools Utilized
- Nmap
- Gobuster
- Netcat
- WordPress Admin Panel
- Linux privilege escalation techniques

## Outcome
- Full root access obtained on the target machine
- Demonstrated the complete attack chain from enumeration to privilege escalation

## Screenshots
<img width="173" height="43" alt="robot1" src="https://github.com/user-attachments/assets/a26aa6c6-5860-4c26-a503-ddf6cc8fc569" />

<img width="289" height="326" alt="robot2" src="https://github.com/user-attachments/assets/b7e426ad-24de-41c3-8d09-c3b634478c4d" />

<img width="374" height="70" alt="robot3" src="https://github.com/user-attachments/assets/4fb5e8df-db0b-4118-8ae4-77fd23d5d25d" />


## Lessons Learned
- Thorough enumeration is critical for successful exploitation
- Applied real-world privilege escalation techniques to gain full control
