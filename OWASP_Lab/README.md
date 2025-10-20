#  OWASP Top 10 Vulnerability Assessment

##  Project Overview
This lab focuses on identifying, analyzing, and documenting common web application vulnerabilities aligned with the **OWASP Top 10 (2021)**.  
Using intentionally vulnerable applications (**BodgeIt** and **WebGoat**), I performed hands-on testing to demonstrate real-world exploitation and remediation strategies.


##  Objectives
- Identify and classify vulnerabilities using the OWASP Top 10 framework.  
- Assess the **risk and business impact** of each finding.  
- Recommend security controls and mitigation actions.  
- Strengthen understanding of **application security testing** and SDLC integration.



##  Tools Used
| Tool | Purpose |
|------|----------|
| **Burp Suite** | Intercepting and analyzing HTTP requests/responses |
| **OWASP ZAP** | Automated vulnerability scanning |
| **Nmap** | Network reconnaissance and port discovery |
| **Nikto** | Web server vulnerability assessment |
| **Nuclei** | Automated CVE and OWASP-based template scanning |

---

##  Key Findings

| OWASP Category | Vulnerability | Affected App | Risk Level | Description |
|----------------|----------------|---------------|-------------|--------------|
| **A01: Broken Access Control** | Unrestricted Admin Page | BodgeIt | 🔴 High | Admin interface accessible without authentication |
| **A02: Cryptographic Failures** | Unencrypted login credentials | WebGoat | 🔴 High | Credentials transmitted in plaintext (HTTP) |
| **A03: Injection** | SQL Injection | BodgeIt | 🔴 Critical | Malicious SQL queries allow database extraction |
| **A07: Identification & Authentication Failures** | Weak passwords accepted (`12345`) | WebGoat | 🔴 High | No password complexity or lockout policy enforced |
| **A08: Software & Data Integrity Failures** | Outdated PHP & ASP.NET versions | WebGoat | 🔴 High | Deprecated versions with known CVEs |
| **A09: Security Logging & Monitoring Failures** | No brute-force alerting or audit trail | WebGoat | 🟠 Medium | Failed logins not logged or alerted |

---

## 🧾 Executive Summary
An assessment of the **OWASP BWA environment** revealed multiple severe web application vulnerabilities mapped to the **OWASP Top 10 (2021)**.  
The most critical issues relate to **broken access control**, **unencrypted credentials**, and **injection flaws**, which pose a direct threat to data confidentiality and system integrity.  
The findings highlight the need for stronger **secure development practices**, **continuous monitoring**, and **timely patch management**.

---

## 🔧 Recommendations
1. **Enforce Access Control:** Restrict admin pages to authorized users with RBAC.  
2. **Encrypt Data in Transit:** Enforce HTTPS with TLS 1.2+ across all endpoints.  
3. **Input Validation:** Sanitize and validate all input fields to prevent SQL injection.  
4. **Patch Management:** Regularly update vulnerable components (e.g., PHP, ASP.NET).  
5. **Implement Logging & Monitoring:** Integrate SIEM alerts for failed logins and privilege escalation.  
6. **Periodic Testing:** Perform quarterly vulnerability assessments and penetration tests.

---

## 📊 Visual Evidence

### 🧩 Burp Suite Dashboard — Vulnerability Scan Summary
The Burp Suite scan revealed several critical and high-risk issues including SQL injection points, authentication flaws, and insecure HTTP responses.  
The dashboard view below summarizes detected vulnerabilities categorized by severity.

Burp Suite Scan Results

(<img width="1078" height="452" alt="image" src="https://github.com/user-attachments/assets/937de216-e19b-47f2-9af0-dfc1686bf8c5" />)
*Figure 1: Burp Suite vulnerability scan summary highlighting OWASP Top 10 categories.*

---

### 💬 Burp Suite Repeater — Exploitation Proof of Concept (PoC)
This screenshot demonstrates a captured HTTP request being modified and replayed in Burp Suite's **Repeater** tab to validate the presence of a SQL injection vulnerability in the login form.

Burp Suite Repeater

(<img width="1040" height="457" alt="image" src="https://github.com/user-attachments/assets/5e7bec4f-932e-443d-8abc-053d0cd415e0" />)
*Figure 2: SQL injection test executed via Burp Suite Repeater tab.*

---

### 🧭 OWASP Mapping Visualization
Each finding was mapped against the OWASP Top 10 2021 framework to identify key areas of weakness and remediation priorities.

OWASP Mapping Chart

(<img width="577" height="605" alt="image" src="https://github.com/user-attachments/assets/5d149b9e-c027-4512-b827-d5361daf4923" />)
*Figure 3: Visual mapping of detected vulnerabilities to OWASP Top 10 categories.*

---

##  Outcome
- Demonstrated ability to identify, assess, and mitigate OWASP Top 10 vulnerabilities.  
- Strengthened understanding of **application security testing** and secure coding.  
- Reinforced skills in using **industry-standard tools** (Burp Suite, ZAP, Nmap, Nikto, Nuclei).  

---

## 🏁 Next Steps
- Expand testing to include **automated CI/CD scanning** integration.  
- Explore **secure API testing** and DevSecOps alignment.  
- Document and visualize findings using dashboards or risk registers.

---

👩🏽‍💻 *Author:* **Lilian Omoike**  
📅 *Project Date:* 2025  
🏷 *Focus Area:* Application Security | OWASP Top 10 | Vulnerability Assessment  
