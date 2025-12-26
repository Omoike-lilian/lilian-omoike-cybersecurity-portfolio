# Wazuh SIEM – Incident Detection, Monitoring, and Compliance Visibility

## Project Overview
This project involved deploying and configuring *Wazuh* as a Security Information and Event Management (SIEM) platform to monitor endpoints, detect security incidents, and provide visibility into vulnerabilities, file integrity events, and compliance posture.

The goal was to simulate a real-world SOC environment where security events are centralized, analyzed, and acted upon, while also supporting governance and compliance requirements.

---

## Objectives
- Deploy a functional SIEM environment for endpoint monitoring
- Detect and analyze security events in real time
- Monitor file integrity changes on sensitive files
- Identify system vulnerabilities and assess risk severity
- Map security findings to compliance frameworks
- Practice incident investigation and response workflows

---

## Environment Setup
- *SIEM Platform:* Wazuh Manager & Dashboard  
- *Agent:* Windows 11 endpoint (GRC-AGENT)
- *Access Method:* SSH (via MobaXterm) and web dashboard
- *Network Configuration:* Bridged networking for inter-VM communication
- *Monitoring Scope:* Host-based logs, file system activity, vulnerabilities, and compliance checks

---

## Key Implementations

### 1. Log Collection & Centralized Monitoring
- Collected security, system, and application logs from the Windows agent
- Centralized all events in the Wazuh dashboard for visibility and correlation
- Verified agent heartbeat and event ingestion status

*Outcome:* Enabled SOC-style centralized monitoring instead of isolated endpoint logs.

---

### 2. File Integrity Monitoring (FIM)
- Monitored sensitive directories containing financial documents
- Detected file creation, modification, and deletion events
- Captured hash changes and timestamps for each event

- 
<img width="1039" height="406" alt="image" src="https://github.com/user-attachments/assets/73517006-94cc-401c-8198-e4c778eb88ac" />



<img width="1034" height="376" alt="image" src="https://github.com/user-attachments/assets/9a3b853f-d8e4-4cfa-a475-37af550e9331" />

<img width="975" height="348" alt="image" src="https://github.com/user-attachments/assets/3a4b50b6-199d-427d-bae4-d0ce690727dd" />




*Example Events Detected:*
- Modification of financial forecast documents
- Temporary file creation during document editing
- Deletion of sensitive files

*Outcome:* Demonstrated detective controls for unauthorized data changes and insider risk detection.

---

### 3. Vulnerability Detection & Risk Visibility
- Enabled vulnerability detection on the Windows endpoint
- Identified critical, high, medium, and low severity CVEs
- Observed vulnerability trends by OS, package, and CVSS score

- <img width="1039" height="406" alt="image" src="https://github.com/user-attachments/assets/70ecfb60-5b56-4d40-8270-59e341f5855e" />

<img width="975" height="421" alt="image" src="https://github.com/user-attachments/assets/bb8007ff-72af-4878-b6aa-371bb93423f4" />


*Findings:*
- High concentration of vulnerabilities tied to OS version
- Presence of critical vulnerabilities with CVSS scores above 9.0
- Ability to prioritize remediation based on risk severity

*Outcome:* Practiced vulnerability triage and risk-based prioritization.

---

### 4. MITRE ATT&CK Mapping
- Observed alerts mapped to MITRE ATT&CK tactics such as:
  - Defense Evasion
  - Initial Access
  - Persistence
  - Privilege Escalation
- Used MITRE mapping to understand attacker behavior patterns

*Outcome:* Improved threat context beyond raw alerts.

---

### 5. Compliance & Control Mapping
Mapped security findings to compliance frameworks including:
- *NIST 800-53*
- *HIPAA*
- *PCI DSS*

- GDPR Dashboard <img width="975" height="384" alt="image" src="https://github.com/user-attachments/assets/2b59bc5a-79be-407f-9472-01d1daf51b66" />


HIPAA Dashboard <img width="975" height="384" alt="image" src="https://github.com/user-attachments/assets/bdf850f8-8b4b-45b6-bce9-1ba9f1e4a366" />



Reviewed control gaps across areas such as:
- Configuration Management
- Audit & Accountability
- System Integrity
- Access Control

*Outcome:* Connected technical findings to governance and regulatory requirements.

---

## Incident Response Simulation
- Investigated FIM alerts involving sensitive document deletion
- Validated event timelines and affected assets
- Assessed potential business impact (data integrity and confidentiality)
- Identified response actions such as access review and policy enforcement

*Outcome:* Practiced end-to-end alert triage and response thinking.

---

## Challenges Encountered
- Disk space and LVM constraints impacting SIEM stability
- High resource usage from running multiple VMs on a single host
- Network reconfiguration issues (NAT vs Bridged)
- SSH and connectivity interruptions due to IP changes

*Resolution:*  
Improved system troubleshooting skills, optimized VM usage, and adopted MobaXterm for stable remote access.

---

## Skills Demonstrated
- SIEM deployment and configuration
- Endpoint security monitoring
- Incident detection and analysis
- File Integrity Monitoring (FIM)
- Vulnerability assessment and prioritization
- Compliance mapping and control evaluation
- Troubleshooting Linux, networking, and resource constraints

---

## Key Takeaway
This project reinforced that effective security operations go beyond tool deployment. Visibility, persistence, and the ability to interpret alerts in a business and compliance context are critical to SOC and GRC success.

---

## Next Improvements
- Automate alert escalation workflows
- Integrate ticketing for incident tracking
- Expand monitoring to additional endpoints
- Implement preventive controls to complement detective alerts
