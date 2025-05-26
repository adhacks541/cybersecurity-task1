# 🚨 Cyber Security Internship – Task 1

## 🔍 Task: Local Network Port Scanning

### 🧠 Objective:
To perform a TCP SYN scan on the local network using **Nmap** and identify open ports to understand the network exposure and potential security risks.

---

### 🛠 Tools Used:
- **Nmap** v7.94SVN
- Operating System: Kali Linux

---

### 🖥️ Scan Details:
- **Command Used:**
nmap -sS -oN scan_results.txt 10.0.2.15/24
- **Scan Time:** May 26, 2025
- **IP Range Scanned:** 10.0.2.0/24

---

### 📋 Results Summary:

#### ✅ Host: 10.0.2.2
- **Open Ports:**
- 135/tcp - msrpc
- 445/tcp - microsoft-ds
- 1042/tcp - afrog
- 1043/tcp - boinc
- 2000/tcp - cisco-sccp

#### ✅ Host: 10.0.2.3
- **Open Port:**
- 53/tcp - domain (DNS)

#### ✅ Host: 10.0.2.15
- **Open Port:**
- 80/tcp - http

---

### ⚠️ Potential Security Risks:

- **Port 135 & 445** – Often targeted in Windows-based attacks (e.g., EternalBlue, WannaCry).
- **Port 80 (HTTP)** – Unencrypted traffic; susceptible to sniffing or MITM attacks.
- **Port 53 (DNS)** – Can be abused for DNS tunneling or amplification attacks.
- **Port 2000 (Cisco SCCP)** – May expose vulnerabilities in VoIP systems.
- **Custom Ports (1042, 1043)** – Unknown services; may pose unmonitored risks.

---

### 📘 Learnings:
- Understood how to identify live hosts and scan for open TCP ports.
- Learned to analyze port functions and their possible threats.
- Gained practical experience using `nmap` for reconnaissance.

---

### 📁 Files Included:
- `scan_results.txt` – Raw output of the Nmap TCP SYN scan
- `Screenshot` – Screenshot of scan
- `README.md` – Description and analysis of the task

---
### ✅ Task Outcome:
Basic network reconnaissance and understanding of how exposed services can introduce vulnerabilities in a network.
