#  Metasploitable Vulnerability Assessment

##  Project Overview
This project involved conducting a comprehensive vulnerability assessment on a **Metasploitable 2** server — a deliberately vulnerable Linux machine used for penetration testing and security training.  
The goal was to identify and document **critical security flaws** mapped to frameworks such as **CIS Controls**, **NIST Cybersecurity Framework (CSF)**, and **OWASP Top 10**.

The assessment simulated a real-world enterprise audit workflow — from reconnaissance and vulnerability discovery to reporting and remediation planning.


##  Objectives
- Identify critical and high-risk vulnerabilities across network and web layers.  
- Map each finding to applicable controls (CIS, NIST CSF).  
- Recommend prioritized remediation and risk mitigation strategies.  
- Strengthen practical experience in vulnerability assessment, reporting, and risk communication.


##  Tools & Methodology
| Phase | Tools Used | Purpose |
|-------|-------------|----------|
| Discovery & Enumeration | **Nmap** | Port scanning, service detection, OS identification |
| Web Assessment | **Nikto** | Detect misconfigurations, outdated components, missing headers |
| Vulnerability Mapping | **Nuclei** | Automated CVE template scanning, confirmation of known exploits |
| Reporting | **Excel / Markdown / Word** | Consolidated results, risk matrix, and executive summary |


##  Key Findings (Summary)
| Category | Example Vulnerability | CVE / Reference | Severity | Framework Mapping |
|-----------|----------------------|------------------|-----------|-------------------|
| **Remote Code Execution** | vsFTPd 2.3.4 Backdoor | CVE-2011-2523 | 🔴 Critical | CIS 7.1, NIST PR.IP-1 |
| **Data Exposure** | Cleartext Transmission (Telnet/FTP) | - | 🔴 High | NIST PR.DS-2 |
| **Weak Authentication** | Default Credentials (SSH, MySQL) | - | 🔴 High | CIS 5.2 |
| **Outdated Components** | Apache 2.2.x, Samba 3.x | Multiple CVEs | 🟠 High | CIS 7.1 |
| **Information Disclosure** | phpinfo.php, Directory Listing | - | 🟡 Medium | CIS 9.2, OWASP A5 |


##  Risk Summary
| Metric | Description |
|--------|--------------|
| **Total Findings** | 14 vulnerabilities identified |
| **Critical / High** | 8 vulnerabilities requiring immediate remediation |
| **Frameworks Referenced** | CIS Controls v8, NIST CSF, OWASP Top 10 |
| **Business Impact** | Risk of system compromise, data theft, or lateral network intrusion |


##  Recommended Actions
1. **Immediate Isolation** – Disconnect the vulnerable host from the network until remediated.  
2. **Patch Management** – Upgrade vsFTPd, Apache, Samba, MySQL, and related dependencies.  
3. **System Hardening** – Disable Telnet, enforce SSH-only remote access, use encrypted protocols.  
4. **Access Controls** – Enforce strong authentication and rotate default credentials.  
5. **Continuous Monitoring** – Implement a SIEM (e.g., Wazuh, Splunk) to detect unauthorized access attempts.  
6. **Verification Scan** – Conduct follow-up assessment after remediation to validate closure.  


## Visuals & Supporting Files
| File | Description |
|------|--------------|
| `metasploitable_executive_summary.pdf` | Executive summary report for management |

| `nmap_scan.txt` | Nmap service and version detection output |

<img width="978" height="438" alt="image" src="https://github.com/user-attachments/assets/1294707f-d718-49f8-a358-df0df41a32bb" />


| `nikto_scan.txt` | Web server vulnerability results |

<img width="1044" height="404" alt="image" src="https://github.com/user-attachments/assets/fbe45c73-5273-4a4a-a8d8-49f0ec80a048" />


| `nuclei_report.txt` | Template-based CVE detection output |

<img width="1027" height="415" alt="image" src="https://github.com/user-attachments/assets/bed5aa05-4abf-4361-8a7b-1da79dae8755" />


| `visual_risk_matrix.png` | Risk severity and priority visualization |

<img width="507" height="619" alt="image" src="https://github.com/user-attachments/assets/0450ec38-8af6-4990-af57-017ecff06ab7" />


##  Learning Outcomes
- Strengthened understanding of **vulnerability management lifecycle** — discovery, prioritization, remediation, and validation.  
- Hands-on application of **offensive and defensive security principles**.  
- Improved ability to translate technical findings into **business risk language**.  
- Reinforced **reporting and documentation** skills for audit-ready deliverables.


##  References
- [CIS Controls v8](https://www.cisecurity.org/controls/)
- [NIST Cybersecurity Framework (CSF)](https://www.nist.gov/cyberframework)
- [ProjectDiscovery Nuclei Templates](https://github.com/projectdiscovery/nuclei-templates)


###  Author
**Lilian Omoike**  
Cybersecurity Analyst | GRC & Vulnerability Management  
 Lagos, Nigeria  


> *“Security isn’t just about tools — it’s about awareness, discipline, and continuous improvement.”*
