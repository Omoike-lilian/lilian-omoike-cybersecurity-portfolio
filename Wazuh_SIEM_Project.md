# 🧠 Wazuh SIEM Deployment & Analysis Project

## 📘 Overview
This project documents the **setup, configuration, and analysis** of a Wazuh Security Information and Event Management (SIEM) system within a simulated enterprise environment.  

The deployment focused on:
- Centralized monitoring  
- File integrity tracking  
- Vulnerability assessment  
- Compliance mapping  

This project showcases both **technical** and **analytical** skills across cybersecurity and GRC domains.  

**Role:** Deployed, configured, and analyzed Wazuh SIEM end-to-end in a virtual enterprise setup to strengthen SOC and governance integration skills.

---

## ⚙️ Environment Setup
**Wazuh Server:** Ubuntu 22.04 LTS (VMware Workstation)  
**Wazuh Agent:** Windows 11 Pro (Monitored endpoint)  
**Network Configuration:** Switched from NAT ➜ Bridged Adapter for inter-VM communication  
**Remote Access:** Secure SSH and dashboard management via *MobaXterm*

### 🧩 Challenges Overcome
- Resolved LVM/VG storage allocation errors (“No space left on device”)  
- Fixed network reachability and bridged networking issues  
- Recovered dashboard access and performed password reset after interrupted installation  

---

## 🔍 Key Features Configured

### 🧾 File Integrity Monitoring (FIM)
- Tracked unauthorized modifications to sensitive files such as financial reports.  
- Generated alerts for file creation, deletion, and checksum changes.  
- **Example:** Detected deletion and modification of `Q4_Financial_Forecast.docx`.  

---

### ⚠️ Vulnerability Detection
- Identified critical vulnerabilities (CVEs) affecting Windows 11 and third-party software (e.g., VirtualBox).  
- Highlighted risks by severity (Critical, High, Medium, Low).  
- Mapped findings to **MITRE ATT&CK** tactics: Defense Evasion, Persistence, Privilege Escalation.  

---

### 🧮 Configuration Assessment
- Performed **CIS Benchmark scan** for Windows 11 Enterprise v3.0.0.  
- Reported 26% compliance score (125 controls passed, 352 failed).  
- Pinpointed control gaps for hardening and configuration improvements.  

---

### 📊 Compliance Mapping
Mapped Wazuh alerts to major frameworks:  

| Framework | Controls Referenced | Focus Area |
|------------|--------------------|-------------|
| **NIST 800-53** | CM.1, SI.7, AU.6 | Configuration & Integrity |
| **PCI DSS** | 2.2, 11.5, 10.6.1 | File monitoring & log review |
| **HIPAA** | 164.312(a)(2)(iv), 164.312(e)(2)(ii) | Access control & data integrity |

---

## 🔒 Risk & Control Insights
| Category | Description |
|-----------|-------------|
| **Risk Identified** | Unauthorized modification of financial documents |
| **Potential Impact** | Financial loss, reputational damage, compliance violation |
| **Detective Control** | FIM alerts on file modification/deletion |
| **Preventive Control** | Access restriction and file encryption |
| **Corrective Control** | Incident response — recovery of deleted or tampered files |

---

## 📈 Metrics for Reporting
1. Number of integrity alerts triggered per time frame  
2. Count of critical vulnerabilities by severity and host  
3. Compliance score trend (pre- vs post-hardening)

**Why Centralized Monitoring Matters:**  
Wazuh centralizes log collection, enabling easier audit, visibility, and reporting — strengthening governance and incident response maturity.

---

## 🧠 Lessons Learned
- SIEM deployment demands patience, troubleshooting, and structured configuration.  
- Disk space allocation and volume management directly impact system stability.  
- Bridged networking is crucial for effective inter-VM log communication.  
- Tools like **MobaXterm** streamline remote administration and monitoring.  

---

## 🧰 Tools & Technologies
**Wazuh 4.12.0** · **VMware Workstation** · **Ubuntu Server** · **Windows 11 Pro** · **MobaXterm** · **OpenSSH** · **CIS Benchmark** · **NIST 800-53** · **PCI DSS** · **HIPAA**

---

## 📸 Optional Enhancements
If allowed, add screenshots such as:
- Dashboard Overview  
- File Integrity Alert Example  
- Vulnerability Scan Summary  
- Compliance Report Excerpt  

---

> 💬 *“Security monitoring is effective only when visibility, governance, and response work together — this project demonstrates that synergy.”*

