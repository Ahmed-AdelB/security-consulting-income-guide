# CODEX: The Ultimate Client Onboarding Guide for Security Consultants (10K Series)

**Version:** 1.0
**Date:** December 2025
**Target Audience:** Independent Security Consultants, vCISOs, Penetration Testers, GRC Experts
**Focus:** Professionalizing the client intake process to minimize friction, maximize trust, and ensure project success.

---

## Table of Contents

1.  [Introduction: The First 72 Hours](#introduction)
2.  [Phase 1: Pre-Engagement & Legal Framework](#phase-1-pre-engagement--legal-framework)
    *   Initial Conflict Check
    *   The Non-Disclosure Agreement (NDA)
    *   Master Services Agreement (MSA) vs. Statement of Work (SOW)
3.  [Phase 2: Scope & Financial Setup](#phase-2-scope--financial-setup)
    *   Defining Success Criteria
    *   Billing, Invoicing, & Retainers
    *   Expense Policies
4.  [Phase 3: Operational Onboarding & Access](#phase-3-operational-onboarding--access)
    *   Communication Protocols
    *   Access Provisioning (Identity & Access Management)
    *   Secure Data Transfer Channels
5.  [Phase 4: The Kickoff Meeting](#phase-4-the-kickoff-meeting)
    *   Agenda & Structure
    *   Stakeholder Alignment
    *   "Rules of Engagement" (RoE)
6.  [Phase 5: Execution & Ongoing Management](#phase-5-execution--ongoing-management)
    *   Reporting Cadence
    *   Escalation Matrix
7.  [Appendix A: Master Onboarding Checklist](#appendix-a-master-onboarding-checklist)
8.  [Appendix B: Templates & Artifacts](#appendix-b-templates--artifacts)
    *   NDA Template Structure
    *   Kickoff Email Template
    *   SOW Component Library

---

## Introduction: The First 72 Hours

The period immediately following a signed contract is the "Zone of Disillusionment" risk area. The sales high has worn off, and the reality of work has set in. If you are silent or disorganized during these first 72 hours, buyer's remorse can set in.

**The Goal of Onboarding:**
1.  **Confidence:** Reassure the client they made the right choice.
2.  **Velocity:** Remove technical and administrative blockers before the clock starts ticking on billable hours.
3.  **Boundaries:** Establish how you work, when you work, and how you communicate.

This guide provides a rigid, repeatable structure to ensure every client feels like your *only* client.

---

## Phase 1: Pre-Engagement & Legal Framework

Before a single packet is captured or a policy reviewed, the legal and ethical foundation must be poured.

### 1.1 Initial Conflict Check
*For independent consultants, especially those working with competitors.*

*   **Action:** Review current active client list against the new prospect.
*   **Considerations:**
    *   Are they direct competitors? (e.g., advising two different endpoint security vendors).
    *   Is there a conflict of interest in auditing? (e.g., auditing a system you previously architected).
*   **Resolution:** If a potential conflict exists, disclose it immediately. Transparency builds more trust than silence.

### 1.2 The Non-Disclosure Agreement (NDA)
Never discuss sensitive architecture or vulnerabilities without a signed NDA.

*   **Mutual vs. One-Way:** Always prefer a Mutual NDA. You have IP (methodologies, custom scripts, templates) that needs protection just as much as their data.
*   **Key Clauses to Watch:**
    *   *Non-Solicit:* Ensure they can't hire you directly without a buyout fee if you are sub-contracting.
    *   *Residual Knowledge:* Ensure you retain the right to use "general knowledge and skills" learned during the engagement.
    *   *Term:* indefinite confidentiality for trade secrets; 2-5 years for general information.

### 1.3 MSA vs. SOW
*   **Master Services Agreement (MSA):** The "Umbrella" contract. Handles liability, payment terms, dispute resolution, and IP ownership. Sign this *once* every 1-3 years.
*   **Statement of Work (SOW):** The specific "Task Order." Handles the *what*, *when*, and *how much* for a specific project. You may have 10 SOWs under one MSA.

**Critical SOW Components:**
1.  **Objective:** One sentence describing the goal.
2.  **Scope Inclusions:** Explicitly what is covered.
3.  **Scope Exclusions:** Explicitly what is NOT covered (Scope Creep Defense).
4.  **Deliverables:** The tangible artifacts (PDF Report, Slide Deck, Code).
5.  **Timeline:** Milestones and deadlines.

---

## Phase 2: Scope & Financial Setup

Security consulting often suffers from "mission creep." Use the financial setup to lock in expectations.

### 2.1 Defining Success Criteria
Ask the client: *"It is 6 months from now, and we are finished. What does the result look like for you to call this a massive success?"*

*   **Technical Success:** "Zero critical vulnerabilities in the external perimeter."
*   **Political Success:** "The Board approves the 2026 security budget."
*   **Operational Success:** "SOC team false positive rate drops by 20%."

*Document this in the SOW.*

### 2.2 Billing, Invoicing, & Retainers

**Setup Steps:**
1.  **Vendor Registration:** Get into their Accounts Payable (AP) system immediately. This often takes 2-4 weeks. Do not wait until the first invoice is due.
    *   *Required Docs:* W-9 (US) or W-8BEN (International), Voided Check / Bank Letter for ACH.
2.  **Invoicing Contact:** Identify the specific human who processes invoices. It is rarely your project point of contact (POC).
3.  **Billing Cycle:**
    *   *Retainer:* Bill on the 1st of the month, Net 15.
    *   *Project:* 50% upfront, 50% on delivery. **Never start work without a deposit.**
    *   *T&M (Time & Materials):* Bi-weekly or monthly invoicing.

**The "Late Payment" Protocol:**
*   Define late fees in the MSA (e.g., 1.5% per month).
*   Automate reminders: 5 days before due, Due Date, 3 days overdue, 7 days overdue.

### 2.3 Expense Policies
If travel or software purchases are required:
*   **Pre-Approval:** Expenses over $X (e.g., $500) require written approval.
*   **Pass-Through:** Expenses are billed at cost (no markup) or cost + 10% admin fee (rare for independents).
*   **Travel Class:** Economy Plus or Business (for international flights >6 hours). Define this *before* booking tickets.

---

## Phase 3: Operational Onboarding & Access

This is where projects usually stall. Drive this process aggressively.

### 3.1 Communication Protocols
Establish the "Rhythm of Business."

*   **Primary Channel:** Email for formal decisions. Slack/Teams for quick coordination?
    *   *Consultant Tip:* If using their Slack, request a "Guest" account restricted to specific channels to limit noise.
*   **Response Time SLAs:**
    *   "I will respond to emails within 24 business hours."
    *   "I will be available for urgent issues via Signal/Phone between 9 AM - 5 PM EST."
*   **Weekly Status Update:** Even if no meeting occurs, send a "Friday Status Email" (3 bullets: Completed, Planned, Blockers).

### 3.2 Access Provisioning (IAM)
**The Golden Rule:** Never use shared accounts. Request a named account (e.g., `consultant-name@client.com` or `ext-name`).

**Checklist for Access:**
*   [ ] **VPN:** Client capability, MFA setup.
*   [ ] **Cloud Provider:** AWS/Azure/GCP specific IAM roles (e.g., `SecurityAudit`, `ViewOnly`, or `Administrator` for remediation).
*   [ ] **Code Repos:** GitHub/GitLab access (Read vs. Write).
*   [ ] **Document Repos:** SharePoint/Confluence/Google Drive.
*   [ ] **Ticketing:** Jira/ServiceNow access for tracking remediation.
*   [ ] **Physical:** Badging if onsite access is required.

**Hardware Requirements:**
*   Will the client provide a laptop? (Common for banking/defense).
*   If BYOD (Bring Your Own Device), do you need MDM (Mobile Device Management) installed?
    *   *Warning:* Be very careful installing client MDM on your personal/business consulting laptop. It may allow them to wipe your machine. Use a VM or a dedicated "Client Laptop" if possible.

### 3.3 Secure Data Transfer
**Never** email sensitive data (P2, vulnerability reports, PII).

*   **Option A:** Client's secure portal (SharePoint, Box).
*   **Option B:** Your secure portal (encryped file share with expiration).
*   **Option C:** Encrypted Archives (7zip/GPG) with out-of-band password transmission (e.g., file via email, password via Signal).

---

## Phase 4: The Kickoff Meeting

The Kickoff is a ceremony. It marks the transition from "Sales" to "Delivery."

**Duration:** 45 - 60 Minutes.
**Attendees:** Project Sponsor, Main POC, Technical Leads, Consultant.

### 4.1 Kickoff Agenda Template

1.  **Introductions (5 min):** Roles and responsibilities. Who is the "Blocker Remover"?
2.  **Project Objectives (10 min):** Reiterate the "Why".
3.  **Scope Review (10 min):** Briefly review SOW Inclusions/Exclusions.
4.  **Timeline & Milestones (10 min):**
    *   "We are here (Start)."
    *   "First draft due X."
    *   "Testing window Y."
5.  **Logistics (10 min):** Access status, meeting cadence.
6.  **Q&A / Next Steps (5 min).**

### 4.2 Rules of Engagement (RoE)
*Critical for Penetration Testing / Red Teaming.*

*   **Testing Windows:** (e.g., "Anytime" vs. "Weeknights only").
*   **Excluded Hosts:** (e.g., "Do not touch the mainframe or the CEO's laptop").
*   **Emergency Contact:** Who to call if a server goes down? (24/7 Phone Number required).
*   **"Get Out of Jail Free" Card:** A signed letter authorizing the testing, to be carried (physically or digitally) in case of law enforcement or physical security intervention.

---

## Phase 5: Execution & Expectations

### 5.1 Reporting Cadence
*   **Weekly Sync:** 15-30 minutes. Optional if the email update is sufficient.
*   **Mid-Point Review:** For longer engagements (>2 months), schedule a check-in to ensure alignment is still true.
*   **Draft Review:** Always schedule a live walkthrough of the draft report. *Never* send a report "cold." Context is lost in PDFs.

### 5.2 Escalation Matrix
Define the path when things go wrong.

*   **Level 1:** Technical Lead (Day-to-day blockers).
*   **Level 2:** Project Manager (Timeline/Resource issues).
*   **Level 3:** Executive Sponsor (Budget/Strategic misalignment).

---

## Appendix A: Master Onboarding Checklist

**Administrative & Legal**
- [ ] Conflict Check performed.
- [ ] NDA signed (Mutual).
- [ ] MSA signed (if applicable).
- [ ] SOW signed and countersigned.
- [ ] Deposit invoice generated and sent.
- [ ] Vendor registration completed in client portal.

**Access & Technical**
- [ ] Identity Verification provided (Passport/DL) if requested.
- [ ] Corporate email account (`@client.com`) requested.
- [ ] Laptop procurement (if applicable) initiated.
- [ ] VPN access requested and tested.
- [ ] Application/Cloud access requested (list specific roles).
- [ ] Source code repository access granted.
- [ ] "Guest" access to Slack/Teams established.

**Knowledge Transfer**
- [ ] Request existing architecture diagrams.
- [ ] Request previous audit reports/pentest findings.
- [ ] Request policy documents relevant to scope.
- [ ] Request list of key stakeholders and interviewees.

**Scheduling**
- [ ] Kickoff meeting scheduled.
- [ ] Recurring weekly status meeting booked.
- [ ] Testing/Interview windows reserved on calendars.
- [ ] Final readout presentation placeholder booked.

---

## Appendix B: Templates & Artifacts

### B.1 Kickoff Email Template

**Subject:** Project Kickoff: [Project Name] - [Your Company] x [Client Company]

**Body:**

Hi [Client Name],

We are thrilled to officially start the [Project Name] engagement!

To ensure a smooth launch, I have attached the countersigned SOW for your records.

**Immediate Next Steps:**
1.  **Kickoff Call:** I have sent a calendar invite for [Date/Time]. Please forward to any technical leads who should be involved.
2.  **Access:** Please initiate the onboarding process for [System A] and [System B]. My technical details are below.
3.  **Invoicing:** I have cc'd [Finance Person] to handle the vendor setup.

**Kickoff Agenda:**
*   Introductions & Roles
*   Scope & Timeline Confirmation
*   Access & Logistics
*   Q&A

Please let me know if you have any questions before we meet.

Best regards,

[Your Name]
[Your Title]

---

### B.2 Information Request List (IRL) - Generic Security Review

*Please provide the following prior to the project start date (or upload to [Secure Link]):*

1.  **Network Diagrams:** High-level topology and data flow diagrams.
2.  **Asset Inventory:** List of in-scope IP addresses, domains, and applications.
3.  **Previous Reports:** The most recent penetration test or audit report for this environment.
4.  **Policy Documents:**
    *   Information Security Policy
    *   Incident Response Plan
    *   Access Control Policy
5.  **Architecture:** Details on cloud environment (AWS/Azure) accounts and structure.

---

### B.3 "Rules of Engagement" (RoE) One-Pager (for Pentesting)

**Authorization:**
I, [Client Executive Name], hereby authorize [Consultant Name] to perform security testing against the assets listed in Schedule A.

**Emergency Stop:**
In the event of system instability, testing will cease immediately upon notification.
*   **Client Contact:** [Name, Phone (24/7)]
*   **Consultant Contact:** [Name, Phone (24/7)]

**Constraints:**
*   No Denial of Service (DoS) attacks.
*   No intentional modification of production data.
*   Social Engineering is [Included / Excluded].
*   Physical Access is [Included / Excluded].

**Signed:**
__________________________ Date: __________
(Client Representative)

---

### B.4 Scope of Work (SOW) - Snippet Examples

**Example: Cloud Security Review**
*   **In Scope:**
    *   AWS Account: `Production-01` (ID: 123456789012).
    *   Review of IAM, S3, EC2, RDS, and VPC configurations against CIS Benchmarks.
    *   One (1) hour remediation workshop with DevOps team.
*   **Out of Scope:**
    *   Operating system level vulnerabilities (patching).
    *   Application code review.
    *   Any AWS accounts not explicitly listed above.

**Example: vCISO Retainer**
*   **In Scope:**
    *   Up to 10 hours of advisory services per month.
    *   Attendance at monthly Risk Committee meeting.
    *   Annual review of policy stack.
*   **Constraints:**
    *   Hours do not rollover month-to-month.
    *   Response time SLA: 1 business day.
    *   Additional hours billed at $X/hr.

---

### B.5 Feedback & Offboarding

The end of the project is the beginning of the next one.

**Offboarding Checklist:**
1.  **Access Revocation:** Remind the client to revoke your accounts (Security hygiene!).
2.  **Data Destruction:** Confirm destruction of sensitive client data from your systems (per NDA).
3.  **Final Invoice:** Sent and confirmed received.
4.  **The "Ask":**
    *   *"If you were happy with this engagement, would you be open to providing a 2-sentence testimonial for my website?"*
    *   *"Is there anyone else in your network tackling similar challenges who might need help?"*

---

*End of Guide*
