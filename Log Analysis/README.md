#  Security Log Analysis & Threat Investigation  

**Date:** September 2025  


##  Objective  
This project involved analyzing simulated enterprise log data to identify recurring security incidents, correlate events across systems, and recommend mitigation strategies aligned with industry frameworks such as **NIST CSF** and **CIS Controls**.


##  Tools & Techniques  
| Category | Tools / Methods Used |
|-----------|----------------------|
| Log Review | Manual log parsing, pattern recognition, timestamp correlation |
| Threat Analysis | CVE mapping, incident severity classification |
| Frameworks | NIST CSF (DE, PR, RS), CIS Controls, MITRE ATT&CK |
| Visualization | Excel & Power BI (incident trend and severity mapping) |



##  Key Findings  

###  Webserver-01: Repeated Attack Target  
- **Incidents Detected:**  
  - Phishing (Sept 5 & 7)  
  - Malware infections (Sept 3 & 7)  
  - Data exfiltration (Sept 5 & 7)  
- **Observation:** The variety and recurrence of attacks suggest weak patch management, misconfiguration, or that the server is a high-value target.  
- **Risk:** High — recurring multi-vector attacks indicate compromised defense layers.  

###  Firewall-01: Unauthorized Access & Exploitable Vulnerabilities  
- **Incidents Detected:**  
  - Unauthorized access attempts on Sept 2.  
  - Vulnerabilities identified:  
    - CVE-2023-1234 – SQL Injection (High)  
    - CVE-2023-5678 – Cross-Site Scripting (Medium)  
  - Repeated data exfiltration attempts within 48 hours.  
- **Risk:** High — unpatched vulnerabilities and weak access controls expose the perimeter defense.  

###  DB-Server-02: Critical Remote Code Execution Vulnerability  
- **Detected:** CVE-2023-9012 (Critical) — Remote Code Execution.  
- **Impact:** Full compromise potential, including exposure of sensitive data.  



##  Root Cause Analysis  
| Category | Issue | Systems Impacted |
|-----------|--------|------------------|
| Patch Management | Unpatched CVEs (SQLi, XSS, RCE) | Firewall-01, DB-Server-02 |
| Access Control | Weak authentication & unauthorized access | Webserver-01, Firewall-01 |
| Incident Response | Delayed closure of critical incidents | All systems |
| Configuration | Unhardened and misconfigured assets | Webserver-01 |



##  Recommendations  
| Priority | Action | Description |
|-----------|---------|-------------|
| 🔴 Critical | Patch and Harden Vulnerable Systems | Apply OS and application updates; disable unused services |
| 🔴 Critical | Strengthen Access Controls | Enforce MFA, audit user accounts, and limit admin privileges |
| 🟠 High | Improve Incident Response Timelines | Define SLA to ensure critical incidents are resolved within 24 hours |
| 🟡 Medium | Deploy WAF & DLP Controls | Reduce attack surface and prevent data exfiltration |
| 🟢 Ongoing | Conduct Awareness Training | Educate users on phishing and password hygiene |


##  Summary Insights  
**Incidents by System**  
- Webserver-01 — 6 incidents  
- Firewall-01 — 5 incidents  
- DB-Server-02 — 2 incidents  

**Top CVEs Identified**  
- CVE-2023-9012 — Critical (RCE)  
- CVE-2023-1234 — High (SQL Injection)  
- CVE-2023-5678 — Medium (Cross-Site Scripting)



##  Learning Outcomes  
- Conducted end-to-end security log analysis.  
- Correlated attack patterns across systems to identify persistent threats.  
- Applied CVE mapping to contextualize real-world vulnerabilities.  
- Enhanced SOC analytical and incident reporting skills.  


##  Framework Alignment  
- **NIST CSF:** Identify, Protect, Detect, Respond  
- **CIS Controls:** 5.2 (Access Control), 7.1 (Patch Management), 9.2 (Monitoring)  
- **MITRE ATT&CK Techniques:**  
  - T1078 – Valid Accounts  
  - T1048 – Exfiltration Over Alternative Protocol  
  - T1190 – Exploit Public-Facing Application  

---
