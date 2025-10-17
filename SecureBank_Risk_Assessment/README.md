# SecureBank Quantitative Risk Assessment

## Project Overview
This project focuses on performing a quantitative risk assessment for the SecureBank mobile banking application.  
The assessment identifies, analyzes, and quantifies potential financial impacts of key security vulnerabilities aligned with the OWASP Top 10 and NIST Risk Management Framework.

---

##  System Context
- Platform: SecureMobile Banking Application  
- User Base: 500,000 active customers  
- Average Transaction: $2,500  
- Daily Transactions: 50,000  
- Objective: Protect customer data, ensure transaction integrity, and minimize operational risk.

---

##  Key Vulnerabilities Identified
Vulnerability	Description	SLE	ARO	ALE	Risk Level
API Authentication Bypass	Unauthorized fund transfers 	$5,000,000 	0.15	$750,000 	High
Database Injection	Exposure of 500,000 customer records	$125,000,000 	0.25	$31,250,000 	Critical
Session Hijacking	Account takeover from active sessions 	$7,500,000 	0.4	$3,000,000 	High

---

## Controls & Mitigation
| Control Option | Cost | Annual Maintenance | Effectiveness | Risk Reduction | ROI | Payback Period |
Advanced API Security Gateway | $350,000 | $50,000 | 90% | $675,000 | 193% | <1 year |
Web Application Firewall (WAF) | $150,000 | $25,000 | 75% | $23,437,500 | 156% | <1 year |
Multi-Factor Authentication (MFA) | $200,000 | $30,000 | 95% | $2,850,000 | 900% | <1 year |

## Visualizations
The following visualizations were created to communicate the findings effectively:
1. **Risk Exposure (Before vs. After Controls)** – Double bar chart
2. <img width="975" height="604" alt="image" src="https://github.com/user-attachments/assets/7a105256-e818-4edb-8e1b-117ea3755496" />

3. Control Investment Breakdown – Stacked bar chart  
4. ROI Comparison– Horizontal bar chart  
5. Risk Reduction Over Time – Line graph  
6. Risk Heat Map – Probability vs. Impact visualization  

---

## Key Insights
- The Database Injection vulnerability poses the greatest financial exposure.
- Implementation of WAF and API Gateway provides significant ROI within the first year.
- Quantitative analysis highlights how proactive investment in security controls leads to measurable financial protection.

##  Executive Summary
An assessment of the SecureBank system revealed multiple high-impact vulnerabilities aligning with the **OWASP Top 10**.  
Applying quantitative analysis (SLE, ARO, ALE) enabled data-driven decision-making on control investments.  
Recommendations include deploying WAF, MFA, and API security gateways, expected to reduce financial exposure by over **90%**, improving overall cyber resilience.

---

##  Tools & Frameworks Used
- **Tools:** Burp Suite, Excel (for risk modeling), NIST SP 800-30
- **Frameworks:** OWASP Top 10, NIST RMF
- **Skills Demonstrated:** Quantitative Risk Analysis, Risk Mitigation Planning, Financial ROI Assessment, Reporting

---

> **Author:** Lilian Omoike  
> **Role:** Cybersecurity Analyst | Risk Management & GRC  
> **Date:** October 2025  
> **Repository:** [Back to Portfolio](../..)
