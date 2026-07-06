# Lilian Omoike Cybersecurity Portfolio

Welcome to my cybersecurity portfolio! Here I document practical, hands-on projects across **GRC (Governance, Risk & Compliance)**, **Security Operations (SOC)**, and **Vulnerability Management**.

**Email:** lilianomoike@gmail.com
**LinkedIn:** [linkedin.com/in/lilian-omoike](https://www.linkedin.com/in/lilian-omoike/)
 **GitHub:** [github.com/Omoike-lilian](https://github.com/Omoike-lilian)

---

 Featured Project: AWS Integrated GRC Platform (Capstone)

**Governance, Risk & Compliance | Cloud-Native Automation on AWS**

A fully automated, cloud-native GRC platform deployed on AWS using Infrastructure as Code, demonstrating enterprise-grade compliance monitoring, risk management, and audit-ready infrastructure across **6 industry-standard frameworks** with zero manual intervention after deployment.

**The problem:** Manual GRC processes can cost organizations up to $280,000/year, and non-compliant organizations face fines up to 3x higher than compliant ones.
**The solution:** An automated AWS platform that cuts GRC costs by ~93% â€” from ~$280,000/year to ~$500/year.

**Key features:**
- Automated compliance monitoring via Lambda, checked hourly through EventBridge
- Real-time CloudWatch + SNS alerting when compliance drops below 80%
- 6 compliance frameworks mapped across 16 controls: ISO 27001, NIST CSF, PCI DSS, HIPAA, GDPR, SOC 2
- Enterprise security: KMS encryption, VPC isolation, IAM least privilege, CloudTrail + AWS Config audit trail
- 22/22 automated tests passing across 8 test classes

**Stack:** AWS CloudFormation (IaC) · RDS MySQL 8.0.40 · DynamoDB · Lambda (Python 3.11) · S3 · KMS · CloudTrail · AWS Config · EventBridge · CloudWatch · SNS · IAM · VPC

**Repo:** [AWS Integrated GRC Platform’](https://github.com/Omoike-lilian/aws-grc-platform)

---

## Risk & Governance Projects

| Project | Focus | Tools/Frameworks | Summary |
|---|---|---|---|
| **[SecureBank Quantitative Risk Analysis](https://github.com/Omoike-lilian/lilian-omoike-cybersecurity-portfolio/tree/main/SecureBank_Risk_Assessment)** | Quantitative Risk (SLE, ARO, ALE, ROI) | Excel, NIST CSF, CIS Controls | Calculated financial risk exposure and ROI for mitigation controls |
| **[TechStart Risk Assessment](https://github.com/Omoike-lilian/lilian-omoike-cybersecurity-portfolio/tree/main/TechStart)** | GRC Case Study | ISO 31000, NIST CSF | Evaluated 10 risks and proposed mitigations for a fintech organization |
| **[TechFlow Assessment](https://github.com/Omoike-lilian/lilian-omoike-cybersecurity-portfolio/tree/main/TechFlow)** | Business Risk Evaluation | NIST 800-30 | Performed risk rating and mitigation plan for cloud-based systems |

## Vulnerability & Threat Analysis

| Project | Focus | Tools | Summary |
|---|---|---|---|
| **[Metasploitable Assessment](https://github.com/Omoike-lilian/lilian-omoike-cybersecurity-portfolio/tree/main/Metasploitable%20Lab)** | Host Vulnerability Scanning | Nmap, Nuclei, Nikto | Identified critical CVEs, mapped to CIS and NIST, and produced a mitigation plan |
| **[Critical OWASP Top 10 Analysis](https://github.com/Omoike-lilian/lilian-omoike-cybersecurity-portfolio/tree/main/OWASP_Lab)** | Web Application Security | Burp Suite, OWASP | Mapped vulnerabilities to the OWASP Top 10 with remediation recommendations |

## SOC & Incident Response Projects

| Project | Focus | Tools | Summary |
|---|---|---|---|
| **[Log Analysis Report](https://github.com/Omoike-lilian/lilian-omoike-cybersecurity-portfolio/tree/main/Log%20Analysis)** | SIEM & Threat Detection | Splunk | Analyzed system logs and identified anomalies related to CVEs and attack patterns |
| **[Wazuh SIEM Deployment & Analysis](https://github.com/Omoike-lilian/lilian-omoike-cybersecurity-portfolio/blob/main/Wazuh_SIEM_Project.md)** | Security Monitoring, FIM & Compliance | Wazuh, Ubuntu Server, Windows 11, MobaXterm | End-to-end deployment and analysis of a Wazuh SIEM in a simulated enterprise environment, covering file integrity monitoring, vulnerability detection, CIS Benchmark configuration assessment, and compliance mapping |

**Wazuh SIEM Deployment additional detail:**
- Deployed Wazuh 4.12.0 (Ubuntu 22.04 LTS server via VMware Workstation) monitoring a Windows 11 Pro endpoint agent, resolving storage allocation and bridged-networking issues along the way.
- Configured File Integrity Monitoring (FIM) to detect unauthorized changes to sensitive files, and identified critical CVEs on the endpoint and third-party software, mapped to MITRE ATT&CK tactics.
- Ran a CIS Benchmark configuration assessment for Windows 11 Enterprise (26% compliance score, 125/477 controls passed) to pinpoint hardening gaps.
- Mapped SIEM alerts to NIST 800-53, PCI DSS, and HIPAA controls to connect security monitoring findings directly to compliance reporting.

---

## Core Skills Demonstrated

- Cloud GRC automation and Infrastructure as Code (AWS CloudFormation, Lambda, Python)
- Risk identification, scoring, and control evaluation (ISO 31000, ISO 27001, NIST CSF, NIST 800-30)
- Quantitative risk modeling (SLE, ARO, ALE, ROI)
- Vulnerability management and web application security testing (Nmap, Nuclei, Nikto, Burp Suite)
- SIEM log analysis, file integrity monitoring, and threat detection (Splunk, Wazuh)
- Configuration hardening assessments (CIS Benchmarks) and threat mapping (MITRE ATT&CK)
- Policy compliance and risk reporting (NIST 800-53, PCI DSS, HIPAA, ISO 27001)

---

**Contact:** lilianomoike@gmail.com | [LinkedIn](https://www.linkedin.com/in/lilian-omoike/) | [GitHub](https://github.com/Omoike-lilian)
