# CODEX SECURITY DELIVERABLES GUIDE: THE GOLD STANDARD (10K EDITION)

**Version:** 1.0
**Date:** December 2025
**Author:** Codex Security Operations
**Classification:** INTERNAL USE / CONSULTANT RESOURCE
**Status:** DEFINITIVE GUIDE

---

## 1. EXECUTIVE OVERVIEW & PHILOSOPHY

### 1.1 The Role of Deliverables in Security Consulting
In high-end security consulting, the deliverable **IS** the product. You are not paid for the hours you spend hacking, auditing, or analyzing; you are paid for the report that articulates risk, guides remediation, and provides assurance to stakeholders. A poorly written report devalues technically excellent work. Conversely, a stellar report can elevate average technical findings into a strategic roadmap.

This guide provides the definitive templates, structures, and standards for every major type of security deliverable. Adhering to these standards ensures consistency, professionalism, and maximum impact for clients ranging from startups to Fortune 100 enterprises.

### 1.2 The "Three-Tier" Audience Principle
Every security deliverable must simultaneously satisfy three distinct audiences:
1.  **The Executive (C-Suite/Board):** Needs "Bottom Line Up Front" (BLUF), financial impact, and risk quantification. They read the first 2 pages.
2.  **The Management (Director/VP):** Needs resource requirements, timelines, trends, and systemic issues. They read the summary and conclusion.
3.  **The Technical Team (Engineers/Devs):** Needs reproduction steps, code snippets, configuration fixes, and root cause analysis. They read the findings and appendices.

---

## 2. EXECUTIVE SUMMARIES (THE "C-LEVEL" VIEW)

The Executive Summary is the most critical section. If this fails, the engagement fails.

### 2.1 Standard Executive Summary Structure

**[CLIENT LOGO]**
**Engagement:** [Engagement Name] (e.g., Q4 2025 External Penetration Test)
**Date:** [Date]

#### 2.1.1 Strategic Assessment
[A 1-paragraph narrative describing the overall security posture. Avoid jargon. Use business language.]

*Example:*
"Codex Security performed a controlled assessment of Acme Corp's external infrastructure. While the perimeter defenses are generally robust against automated attacks, our assessment identified a critical gap in the legacy payment portal that allows unauthorized access to customer data. This represents a significant business risk. However, the responsiveness of the internal security team was notably high, indicating a strong operational security culture."

#### 2.1.2 Key Risk Metrics
| Metric | Status | Trend |
| :--- | :--- | :--- |
| **Overall Risk Score** | **HIGH** | 🔴 (Worsening) |
| **Critical Findings** | 3 | 🔼 (+1 vs last year) |
| **High Findings** | 5 | 🔽 (-2 vs last year) |
| **Remediation Effort** | 4 Weeks | 🟢 (On Track) |

#### 2.1.3 The "Top 3" Risks (Business Impact Focused)
1.  **Customer Data Exposure:** Direct path to PII database via legacy API.
    *   *Business Impact:* GDPR fines, reputation loss, customer churn.
2.  **Administrator Account Compromise:** Weak MFA implementation on VPN.
    *   *Business Impact:* Full network takeover, ransomware susceptibility.
3.  **Supply Chain Weakness:** Hardcoded vendor credentials in public GitHub.
    *   *Business Impact:* Third-party breach vector, IP theft.

#### 2.1.4 Strategic Recommendations Roadmap
*   **Immediate (0-7 Days):** Patch legacy API, enforce MFA for all admins.
*   **Short Term (30 Days):** Conduct credential audit, rotate vendor keys.
*   **Long Term (90+ Days):** Implement SSDL (Secure Software Development Lifecycle) training.

---

## 3. PENETRATION TEST REPORT TEMPLATES

### 3.1 Report Structure
1.  **Title Page** (Confidentiality markers, Client Name, Date)
2.  **Document Control** (Version history, Distribution list)
3.  **Executive Summary** (See Section 2)
4.  **Methodology & Scope**
5.  **Attack Narrative** (The "Story" of the hack)
6.  **Detailed Findings**
7.  **Appendices**

### 3.2 Methodology & Scope Template

**Scope of Assessment:**
*   **Targets:** `*.acme.com`, `192.168.1.0/24`
*   **Exclusions:** Denial of Service (DoS), Social Engineering of HR staff.
*   **Testing Window:** Dec 1 - Dec 15, 2025.
*   **Perspective:** Grey Box (Authenticated User + Network Access).

**Methodology:**
This assessment followed the **PTES (Penetration Testing Execution Standard)** guidelines:
1.  **Intelligence Gathering:** OSINT, DNS recon, port scanning.
2.  **Threat Modeling:** Identifying high-value targets.
3.  **Vulnerability Analysis:** Automated scanning + Manual verification.
4.  **Exploitation:** Safe execution of payloads to prove risk.
5.  **Post-Exploitation:** Lateral movement and persistence (simulated).
6.  **Reporting:** Documentation of findings.

### 3.3 The Attack Narrative (The "Story")
*This section is crucial for showing the "chain" of an attack.*

"Our consultants began by enumerating subdomains and discovered `dev-api.acme.com`. Although this endpoint was not advertised, it accepted authentication tokens. By analyzing the JavaScript on the main login page, we extracted a hardcoded API key. Using this key against `dev-api`, we were able to enumerate user IDs. One ID belonged to an administrator. We then attempted a password spray attack using common passwords and successfully gained access to the administrator account. From there, we uploaded a web shell..."

---

## 4. VULNERABILITY ASSESSMENT FORMATS

Unlike a pen test, a VA report is broad but shallow. It focuses on coverage and inventory.

### 4.1 Asset Inventory Table
| IP Address | Hostname | OS / Version | Role | Detected Services |
| :--- | :--- | :--- | :--- | :--- |
| 10.0.1.5 | `web-prod-01` | Ubuntu 22.04 | Web Server | Nginx 1.18, SSH |
| 10.0.1.6 | `db-prod-01` | Windows 2019 | Database | MSSQL 2019 |

### 4.2 Automated Scan Summary
*   **Scanner Used:** Nessus Professional / Qualys
*   **Scan Policy:** Full Safe Scan (No DoS)
*   **Total Hosts Scanned:** 150
*   **Total Vulnerabilities:** 450 (23 Critical, 50 High)

### 4.3 False Positive Removal Log
*Always include this to show value add over raw output.*

| Plugin ID | Vulnerability Name | Target | Action | Justification |
| :--- | :--- | :--- | :--- | :--- |
| 12345 | SSL Self-Signed Cert | 10.0.1.5 | **Removed** | Internal dev server, not facing public. |
| 67890 | Apache Version Disclosure | 10.0.1.6 | **Downgraded** | Banner is faked by security config (ServerTokens Prod). |

---

## 5. SECURITY AUDIT REPORTS (GRC FOCUS)

Used for SOC2, ISO 27001, HIPAA, or NIST assessments.

### 5.1 Control Framework Mapping (NIST CSF Example)

| Function | Category | Subcategory | Control Description | Status | Evidence Ref |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **IDENTIFY** | Asset Mgmt | ID.AM-1 | Physical devices are inventoried | **Partial** | MDM lists laptops, but no server inventory. |
| **PROTECT** | Access Control | PR.AC-1 | Identities are managed (IAM) | **Compliant** | Okta fully implemented with MFA. |
| **DETECT** | Anomalies | DE.AE-1 | Baseline of network ops established | **Non-Compliant** | No NetFlow analysis or SIEM baseline. |

### 5.2 Gap Analysis Visualization
*Create a "Spider Chart" or "Heat Map" description.*

*   **Policy Maturity:** 3/5
*   **Technical Implementation:** 4/5
*   **Monitoring & Response:** 1/5 (Major Gap)

### 5.3 Audit Opinion
"Based on the evidence reviewed, Acme Corp is **MATERIALLY COMPLIANT** with the access control requirements of SOC2 Type 1, but significant gaps exist in the Monitoring and Logging criteria."

---

## 6. COMPLIANCE DOCUMENTATION TEMPLATES

### 6.1 System Security Plan (SSP) - NIST 800-171 / CMMC
**1. System Identification**
*   System Name: Enterprise ERP
*   System Owner: CIO
*   Security Category: Moderate/Moderate/Moderate (CIA)

**2. System Environment**
*   **General Description:** The ERP hosts financial and HR data.
*   **Network Diagram:** [Reference to Appendix A]
*   **Hardware Inventory:** [Reference to Asset List]

**3. Security Controls Implementation**
*   **AC-1 (Access Control Policy):**
    *   *Implementation:* Access is governed by the Corporate IAM Policy v2.0.
    *   *Mechanism:* Active Directory Groups mapped to ERP Roles.
*   **AC-2 (Account Management):**
    *   *Implementation:* Automated provisioning via Workday integration. Access revoked within 24 hours of termination.

### 6.2 Policy Template Header
**Policy Name:** Remote Access Policy
**Policy ID:** POL-SEC-04
**Effective Date:** 2025-01-01
**Owner:** CISO
**Applies To:** All Employees, Contractors, Vendors

**1. Purpose**
To define standards for connecting to the corporate network from external hosts.

**2. Scope**
All remote access technologies (VPN, RDP, SSH, Cloud Portals).

**3. Policy Statements**
*   3.1 All remote access must use Multi-Factor Authentication (MFA).
*   3.2 Split-tunneling is prohibited for corporate managed devices.
*   3.3 Remote sessions generally time out after 15 minutes of inactivity.

---

## 7. TECHNICAL FINDINGS FORMAT (THE CORE)

This is the template for every single finding in a pentest or audit report.

### 7.1 The Finding Block

**Finding ID:** VULN-01
**Title:** SQL Injection in Search Field
**Severity:** **CRITICAL**
**CVSS Score:** 9.8 (CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H)
**Status:** Open / Verified

**Description:**
The application's search function (`/search?q=`) does not properly sanitize user input. By injecting SQL syntax, an attacker can manipulate the backend database query.

**Technical Detail / Proof of Concept (PoC):**
*   **URL:** `https://acme.com/search`
*   **Payload:** `' OR 1=1 --`
*   **Request:**
    ```http
    GET /search?q='%20OR%201=1%20-- HTTP/1.1
    Host: acme.com
    ```
*   **Response:**
    The server returned a list of all users, including hashed passwords, confirming the injection.

**Impact:**
*   **Confidentiality:** Attacker can dump the entire database (Usernames, Passwords, PII).
*   **Integrity:** Attacker could modify data or drop tables (depending on DB user permissions).
*   **Availability:** Attacker could delete data, causing a denial of service.

**Remediation:**
1.  **Primary Fix:** Use Parameterized Queries (Prepared Statements) for all database interaction. Do not concatenate strings.
    *   *Code Example (Python/Flask):*
        ```python
        # BAD
        cursor.execute("SELECT * FROM users WHERE name = '" + user_input + "'")
        
        # GOOD
        cursor.execute("SELECT * FROM users WHERE name = %s", (user_input,))
        ```
2.  **Secondary Defense:** Implement input validation (allow-listing) for search terms.
3.  **Tertiary Defense:** Ensure the database user has least-privilege permissions.

**References:**
*   OWASP Top 10 - A03:2021 (Injection)
*   CWE-89: Improper Neutralization of Special Elements used in an SQL Command.

---

## 8. REMEDIATION TRACKING & POAM

### 8.1 Plan of Action and Milestones (POAM) Template

| ID | Finding | Severity | Root Cause | Planned Action | Owner | Resources Required | Sched. Completion | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| V-01 | SQL Injection | Critical | Legacy Code | Rewrite search module using ORM | Dev Team A | 40 Hours Dev Time | 2026-01-15 | **In Progress** |
| V-02 | Weak SSL Cipher | Medium | Config Error | Update Nginx Config | Ops Team | Change Window | 2025-12-30 | **Scheduled** |
| V-03 | Missing SOPs | Low | Process Gap | Draft Incident Response Plan | GRC Team | Consultant Hire | 2026-03-01 | **Delayed** |

### 8.2 Retest Report (The "Clean" Bill of Health)

**Finding ID:** VULN-01 (SQL Injection)
**Original Status:** Open
**Retest Date:** 2026-01-20
**Retester:** Codex Security
**Result:** **CLOSED / REMEDIATED**

**Verification:**
The consultant attempted the original payload `' OR 1=1 --` against the updated endpoint. The application now returns a "0 results found" standard page and does not execute the SQL. Code review confirmed the use of `SQLAlchemy` parameterized queries.

---

## 9. CLIENT PRESENTATION TEMPLATES

### 9.1 The "Kick-Off" Deck
*   **Slide 1: Title & Team** (Who we are, contact info)
*   **Slide 2: Objectives** (What are we testing? Why?)
*   **Slide 3: Scope & Rules of Engagement** (IPs, Times, "Stop Testing" Triggers)
*   **Slide 4: Timeline** (Start, Milestones, Draft Report, Final Report)
*   **Slide 5: Communication Plan** (Escalation paths for critical findings)
*   **Slide 6: Q&A**

### 9.2 The "Close-Out" / Findings Deck
*   **Slide 1: Executive Summary** (The BLUF - see Section 2)
*   **Slide 2: The Good** (What is working well? Praise the internal team)
*   **Slide 3: The Bad (Theme 1)** (e.g., "Input Validation Issues")
*   **Slide 4: The Bad (Theme 2)** (e.g., "Patch Management Lags")
*   **Slide 5: Critical Walkthrough** (Deep dive into the 1-2 most scary findings with screenshots)
*   **Slide 6: Roadmap** (30/60/90 day plan)
*   **Slide 7: Q&A**

---

## 10. TECHNICAL WRITING STANDARDS

### 10.1 Tone and Voice
*   **Objective:** Never use emotional language ("terrible security," "shocking gap"). Use factual language ("insufficient controls," "critical exposure").
*   **Active Voice:** "The consultant identified a vulnerability" (Better than "A vulnerability was identified").
*   **Precise:** "The server responded in 45ms" (Better than "The server was fast").

### 10.2 Formatting
*   **Code Blocks:** Always use fixed-width font (Courier/Consolas) for paths, commands, payloads, and code.
*   **Screenshots:**
    *   Must be readable.
    *   Must have a caption (Figure 1: Admin Dashboard access).
    *   Sensitive data (unrelated user PII) must be redacted/blurred.
*   **Emphasis:** Use **Bold** for emphasis, not CAPS.

---

## 11. APPENDICES

### 11.1 Standard Disclaimer
"This report is a snapshot in time. Security is dynamic; new vulnerabilities are discovered daily. This assessment represents a best-effort analysis based on the scope and time allotted. It does not guarantee that the system is free from all vulnerabilities or immune to all attacks."

### 11.2 Severity Rating Scale (The Codex Standard)

| Severity | Description | Remediation SLA |
| :--- | :--- | :--- |
| **CRITICAL** | Immediate root access, data loss, or total system compromise. Easy to exploit. | **24-48 Hours** |
| **HIGH** | Significant data loss, privilege escalation, or lateral movement. Moderate difficulty. | **7-14 Days** |
| **MEDIUM** | Partial disclosure, limited access, or requires unlikely user interaction (uncommon phishing). | **30-60 Days** |
| **LOW** | Information leakage (headers), best practice violations. | **90+ Days / Backlog** |
| **INFO** | Debug data, architectural notes, no direct risk. | **N/A** |

### 11.3 Common Acronyms
*   **XSS:** Cross-Site Scripting
*   **SQLi:** SQL Injection
*   **RCE:** Remote Code Execution
*   **LPE:** Local Privilege Escalation
*   **PII:** Personally Identifiable Information
*   **MFA:** Multi-Factor Authentication

---

## 12. SPECIALIZED REPORT ADD-ONS

### 12.1 Cloud Security Review (AWS/Azure/GCP)
*   **Identity (IAM):** Check for over-permissive roles, lack of MFA on root, unused keys.
*   **Storage (S3/Blobs):** Check for public buckets, lack of encryption at rest.
*   **Compute (EC2/VMs):** Check for open Security Groups (0.0.0.0/0 on SSH/RDP).
*   **Logging:** Check if CloudTrail/VPC Flow Logs are enabled and stored centrally.

### 12.2 Mobile Application Security (iOS/Android)
*   **Data Storage:** Checking `plist` files, SQLite DBs, and LogCat for unencrypted PII.
*   **Network:** Checking for Certificate Pinning and proper TLS implementation.
*   **Binary Analysis:** Checking for hardcoded API keys, debug symbols, and jailbreak detection.

### 12.3 Social Engineering Report (Phishing)
*   **Campaign Setup:** Domain spoofing, email template used.
*   **Metrics:**
    *   Emails Sent: 100
    *   Emails Opened: 45 (45%)
    *   Links Clicked: 20 (20%)
    *   Credentials Submitted: 12 (12%)
    *   Reported to Security: 2 (2%)
*   **User Training Gaps:** Identification of departments with high click rates.

---
**END OF DELIVERABLES GUIDE**
