Metasploitable Lab — Recon, Scanning & Remediation

Purpose: Documented hands-on vulnerability discovery, validation, and remediation exercises against an isolated Metasploitable lab host using nmap, nuclei, and nikto. This project is for learning, reporting, and demonstrating defensive recommendations — no exploit payloads are included.

⚠️ Safety & Ethics (Read first)

Only run these VMs on an isolated lab network (host-only or air-gapped).

Do not target systems you do not own or lack explicit written permission to test.

This repo contains sanitized outputs and remediation guidance; raw or sensitive outputs should be stored in a private repository only.

All exploitation steps in the lab were performed in a controlled environment for learning — no weaponized code is published here.

Project Overview

This project documents an initial full-port discovery and focused web/service scanning of a Metasploitable host at 192.168.15.133. The goal is to demonstrate the full reconnaissance → vulnerability identification → remediation validation workflow using common open-source tools.

Tools used

nmap — network discovery, service/version detection, OS fingerprinting

nuclei — fast templated vulnerability checks (CVEs, misconfigs, exposures)

nikto — web server misconfigurations and information disclosure checks

Target

Lab host: 192.168.15.133 (private range — sanitized for public repo)

What’s included (key highlights)

Full-scan outputs (sanitized): nmap_scan_results.md, nikto_scan_results.md, nuclei_scan_results.md.

Executive summaries for quick stakeholder reading: *_findings_summary.md.

Actionable remediation checklists with example commands/configs: *_remediation_checklist.md.

Techniques-only exploit summary (no raw exploit code) for learning purposes.

Defenses & hardening guidance and verification steps for each high-risk finding.

Top Combined Findings (short)

Legacy & cleartext services — Telnet, rsh, rlogin present → credentials exposed in transit.

Outdated software stack — Apache 2.2.8, PHP 5.2.4, MySQL 5.0, PostgreSQL 8.3 — many known CVEs.

Exposed management interfaces — phpMyAdmin, Tomcat (AJP 8009) — Ghostcat (CVE-2020-1938) detected.

Default/weak credentials on DBs — PostgreSQL postgres:postgres found → full DB compromise.

Information disclosure — phpinfo.php, directory indexing, server headers, backup files (e.g., #wp-config.php#).

Service-specific critical CVEs — PHP CGI RCE (CVE-2012-1823), distccd CVE-2004-2687, multiple others.

Missing HTTP security headers & unsafe HTTP methods — TRACE enabled, no X-Frame-Options, CSP, HSTS, etc.

Recommended Priority Remediation (summary)

P1 (Immediate)

Isolate host; remove test/backdoor services (bindshell).

Disable Telnet, rsh, rlogin; disable anonymous FTP.

Remove phpinfo and other debug files; restrict phpMyAdmin to admin IPs/VPN.

Change default DB credentials; restrict DB access via pg_hba.conf.

Disable/secure AJP connector or patch Tomcat (Ghostcat).

P2 (Short term)

Upgrade Apache & PHP to supported versions; patch services.

Disable TRACE; add security headers (X-Frame-Options, X-Content-Type-Options, CSP, HSTS).

Disable SMBv1; restrict or remove NFS exports.

P3 (Ongoing)

Implement monitoring (logs, WAF/IDS), scheduled vulnerability scans (nuclei/OS scanners), and a patch management process.

Rebuild hardened VM images (no test/backdoors), maintain baseline images.

For exact commands and configs, see the remediation checklists:

Lab_01_Reconnaissance/nuclei_remediation_checklist.md

Lab_01_Reconnaissance/nikto_remediation_checklist.md

How to reproduce the scans (lab-only)

Example commands used (run from an isolated attacker VM on the same host-only network)

Nmap (full-port, service/version, default scripts, OS)

sudo nmap --privileged -sV -sC -O -p- -oA initial_scan 192.168.15.133

<img width="978" height="438" alt="image" src="https://github.com/user-attachments/assets/8a019ddb-7556-4add-b3ad-22fb44dda701" />

Nuclei (HTTP CVEs & templates)

nuclei -u http://192.168.15.133 -t cves/ -o nuclei_scan_results.txt
# or full template scan
nuclei -target http://192.168.15.133 -t /path/to/nuclei-templates/ -o nuclei_full.txt

<img width="1027" height="415" alt="image" src="https://github.com/user-attachments/assets/9c34f128-ef1b-4202-9665-73639dc44833" />




Nikto (web server test)

nikto -h http://192.168.15.133 -output nikto_results.txt

<img width="1044" height="404" alt="image" src="https://github.com/user-attachments/assets/443f0124-27d0-4f0c-84ba-6125a245b0a2" />


Validation & Retest

After applying remediations:

Re-run nmap focused checks on remediated ports: nmap -sV --script vuln -p <ports> <target>.

Re-run nuclei with the same templates to confirm CVEs are no longer detected.

Re-run nikto and perform web app scans (OWASP ZAP/Burp) if applicable.

Record evidence (screenshots, logs) and commit sanitized retest files under Defenses_and_Remediation/.
