# Incident Response & SOC L1 Case Studies

This repository contains sanitized case studies of real-world incidents handled during my experience as an IT Support Analyst (N2), focusing on Blue Team, DFIR (Digital Forensics and Incident Response), and Email Security.

---

## Case Study 1: Mass Phishing Campaign & Account Takeover (ATO)

* **Scenario:** A corporate email account was compromised, and an attacker sent phishing emails (containing a malicious PDF link) to over 350 recipients.
* **Investigation & Analysis:**
  * Analyzed the email headers and confirmed the emails were sent from the legitimate M365 infrastructure (`X-MS-Exchange-Organization-AuthAs: Internal`), indicating compromised credentials or session tokens (ATO).
  * Extracted and analyzed the malicious PDF, uncovering a redirect link pointing to a fake Microsoft login page.
* **Containment & Remediation:**
  * Blocked the compromised account and revoked all active OAuth/session tokens.
  * Forced a password reset and re-enforced MFA.
  * Audited and removed malicious email forwarding rules created by the attacker.
* **Skills Demonstrated:** Incident Response, Email Security, IOC Extraction, M365 Security Administration.

---

## Case Study 2: Email Forensics & Spoofing Analysis

* **Scenario:** A user reported a suspicious email requesting a change in bank details (wire transfer).
* **Investigation & Analysis:**
  * Extracted and analyzed the email headers (`Message-ID`, `X-MS-Exchange-CrossTenant-id`, `Return-Path`).
  * Verified SPF (Pass), DKIM (Pass), and DMARC (None) results.
  * Concluded the email originated from a legitimate tenant and mailbox, indicating a high probability of Account Takeover or a compromised internal device, rather than external spoofing.
* **Skills Demonstrated:** Email Header Analysis, SPF/DKIM/DMARC Validation, Threat Hunting.

---

## Case Study 3: Network Hardening & Endpoint Security

* **Scenario:** Client required network infrastructure deployment and endpoint protection.
* **Actions Taken:**
  * Deployed and configured a MikroTik edge router (NAT, basic firewall rules, and network segmentation).
  * Deployed enterprise Endpoint Protection (Antivirus) agents across all mapped workstations.
  * Audited network access and verified the security agent health.
* **Skills Demonstrated:** Network Security, Endpoint Protection, Security Hardening.
