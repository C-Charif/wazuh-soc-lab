# 🔐 SOC Simulation Lab with Wazuh SIEM

## 📌 Overview

This project demonstrates the design and implementation of a **Security Operations Center (SOC)** in a virtualized environment using **Wazuh SIEM**.

The lab simulates real-world cyberattacks and shows how they are **detected, analyzed, and correlated** in real time.

---

## 🎯 Objectives

* Deploy a complete SOC architecture
* Configure Wazuh SIEM with active agents
* Simulate real-world cyberattacks
* Detect and analyze security incidents
* Map attacks to MITRE ATT&CK framework
* Produce a professional incident report

---

## 🧱 Architecture

| Machine      | Role     | IP            |
| ------------ | -------- | ------------- |
| Kali Linux   | Attacker | 192.168.57.40 |
| Ubuntu 24.04 | Victim   | 192.168.57.20 |
| Wazuh Server | SIEM     | 192.168.57.30 |

* Network: Host-Only (isolated lab)
* Hypervisor: VirtualBox

---

## ⚙️ Technologies Used

* Wazuh 4.12 (SIEM / XDR)
* Kali Linux (Attacker)
* Ubuntu 24.04 (Target)
* VirtualBox
* Nmap (Reconnaissance)
* Hydra (Brute Force)

---

## ⚔️ Simulated Attacks

### 1. Network Scanning (Reconnaissance)

```
nmap -A -sV 192.168.57.20
```

### 2. SSH Brute Force Attack

```
hydra -l user -P passwords.txt ssh://192.168.57.20
```

### 3. Repeated SSH Login Attempts

```
for i in {1..10}; do ssh user@192.168.57.20; done
```

### 4. File Integrity Manipulation (FIM)

```
sudo touch /etc/malware_test
sudo echo "backdoor" >> /etc/crontab
```

---

## 🛡️ Detection Capabilities

* Real-time log analysis
* Brute-force detection (SSH)
* File Integrity Monitoring (FIM)
* Vulnerability detection (CVE)
* Alert correlation

---

## 📊 Key Results

| Metric                   | Value        |
| ------------------------ | ------------ |
| Detection Time           | < 30 seconds |
| Events analyzed          | 571+         |
| Detection rate           | 100%         |
| Critical vulnerabilities | 21           |

---

## 🧠 MITRE ATT&CK Mapping

| Attack      | Technique |
| ----------- | --------- |
| Nmap Scan   | T1046     |
| Brute Force | T1110     |
| Persistence | T1543     |

---

## 🔧 Security Improvements

* SSH Hardening
* Fail2Ban deployment
* Wazuh Active Response (auto-block)
* System patching
* Disable unnecessary services

---

## 📄 Documentation

Full technical report available here:

👉 `docs/rapport.pdf`

---

## 🚀 Skills Demonstrated

* SIEM deployment (Wazuh)
* Incident detection & analysis
* Linux system administration
* Threat detection & correlation
* MITRE ATT&CK mapping
* SOC operations workflow

---

## ⚠️ Disclaimer

All attacks were performed in a **controlled virtual environment** for educational purposes only.

---

## 👤 Author

**Chaima Charif**
Cybersecurity Student | Blue Team | SOC Analyst

---

## ⭐ Future Improvements

* Add Windows machine
* Integrate TheHive
* Create custom Wazuh rules
* Automate incident response
