# Bugcrowd Deep Dive Guide (10K)

Version: 1.0
Scope: Comprehensive Bugcrowd overview for researchers
Audience: New and experienced security researchers
Goal: Explain platform mechanics, earnings, and strategy

Disclaimer: Educational material only
Disclaimer: Program rules always override this guide
Disclaimer: Earnings examples are self reported and approximate

## Table of Contents
- 1. Executive Summary
- 2. Platform Overview
- 3. Researcher Onboarding and Identity
- 4. Researcher Tiers and Reputation
- 5. Program Types and Access
- 6. Payout Structure
- 7. Private vs Public Programs
- 8. Program Lifecycle and Workflow
- 9. VRT Deep Dive
- 10. Success Strategies
- 11. Report Writing
- 12. Communication and Professionalism
- 13. Common Rejection Reasons
- 14. Tooling and Lab Setup
- 15. Comparison with HackerOne and Synack
- 16. Real Earnings Data
- 17. 30-60-90 Day Plan
- 18. Legal and Ethics
- 19. Quality Checklist
- 20. Glossary
- 21. Appendix A: Sample Report Template
- 22. Appendix B: Triage Checklist
- 23. Appendix C: Resource List

## 1. Executive Summary
Bugcrowd is a crowdsourced security platform connecting organizations with researchers.
It blends public and private programs with a managed triage layer.
The platform uses the Vulnerability Rating Taxonomy (VRT) for consistent severity.
Researchers build reputation through accepted submissions and professionalism.
Strong results come from disciplined scope selection and high quality reporting.
This guide focuses on practical steps to earn, learn, and grow.

## 2. Platform Overview
### 2.1 What Bugcrowd Is
Bugcrowd hosts coordinated vulnerability disclosure and bounty programs.
Organizations list assets and rules under clearly defined scopes.
Researchers submit findings through the Bugcrowd portal.
Bugcrowd triage validates reports and routes them to customers.
Some programs are fully managed, others are customer managed.

### 2.2 Core Components
- Program listings with scope and reward rules
- Submission workflow and ticket tracking
- Vulnerability Rating Taxonomy (VRT)
- Researcher reputation and kudos
- CrowdMatch or similar invite matching
- Bugcrowd University learning modules
- Mediation for disputes and clarifications
- Payment processing and tax compliance

### 2.3 Platform Roles
- Customer: the organization running a program
- Researcher: the independent tester submitting findings
- Triage: Bugcrowd analysts validating and rating reports
- Program team: security staff and engineers fixing issues

### 2.4 Why Companies Use Bugcrowd
- Elastic testing capacity without hiring full time staff
- Diverse skill sets covering web, mobile, and cloud
- Faster discovery of impactful vulnerabilities
- Standardized severity scoring and triage processes
- Coordinated disclosure and safe testing rules

### 2.5 Why Researchers Use Bugcrowd
- Access to real world assets and targets
- Potential cash bounties and recognition
- Structured taxonomy for severity and impact
- Private program invitations with lower competition
- Learning through writeups and community feedback

### 2.6 Typical Program Assets
- Web applications and APIs
- Mobile apps and backend services
- Cloud configurations and storage
- Authentication flows and SSO
- Payment, identity, and user data workflows
- Marketing sites and CMS instances

### 2.7 Submission Lifecycle at a Glance
1. Read scope and rules for a program
2. Enumerate assets and test within scope
3. Submit a clear report with proof
4. Triage validates and assigns severity
5. Customer reviews, fixes, and closes
6. Bounty payment and kudos are issued

### 2.8 Key Terms
- Scope: assets allowed for testing
- Out of scope: assets or actions prohibited
- Duplicate: a report matching an earlier submission
- N/A: submission not applicable to the program rules
- Informational: valid but non exploitable issue
- VRT: Bugcrowd taxonomy for severity
- Triage: Bugcrowd validation and routing layer
- Kudos: non monetary recognition points

## 3. Researcher Onboarding and Identity
### 3.1 Account Setup
Create a Bugcrowd account with accurate identity details.
Enable multi factor authentication for account safety.
Fill profile fields so programs can match your expertise.
Use a stable email to avoid missing triage requests.

### 3.2 Profile Hygiene
Maintain a professional handle and profile description.
List technical areas like web, mobile, or cloud.
Add languages and time zone for collaboration.
Keep contact channels current for payout and legal forms.

### 3.3 Bugcrowd University
Bugcrowd offers structured learning modules.
Completion can unlock badges and improve invite matching.
Use it to learn VRT severity mapping and report quality.
New researchers can use it to build a baseline portfolio.

### 3.4 Identity and Compliance
Some private programs require additional verification.
Tax forms and payout methods may require legal details.
Respond quickly to verification requests to avoid payout delays.

### 3.5 Portfolio and Proof of Work
Document accepted findings in a private log.
Track impact, severity, and lessons learned.
Use sanitized notes for future methodology improvements.

## 4. Researcher Tiers and Reputation
### 4.1 Overview
Bugcrowd uses a reputation system to surface skilled researchers.
The exact tier labels can evolve, but a 1 to 5 scale is common.
Higher rank typically increases private program invitations.
Reputation also influences triage trust and faster validations.

### 4.2 Common Tier Model (Example)
- Rank 1: New researcher with limited accepted findings
- Rank 2: Consistent valid reports with low duplicates
- Rank 3: Multiple impactful findings across programs
- Rank 4: High severity submissions and reliable reports
- Rank 5: Elite performance with sustained impact

### 4.3 How Rank Is Earned
- Valid submissions accepted by programs
- Severity and impact of findings
- Quality of reproduction steps
- Low rate of duplicates and out of scope
- Professional communication and responsiveness

### 4.4 Kudos and Non Monetary Signals
Kudos points show contribution volume and quality.
Some programs reward kudos even without payouts.
Kudos can improve visibility in invite matching.

### 4.5 CrowdMatch and Invitations
Bugcrowd often matches researchers to private programs.
Signals include rank, skills, and recent activity.
Consistency is more valuable than one large win.

### 4.6 Sample Progression Timeline
Month 1: learn scope, submit a few low severity issues.
Month 2: improve methodology and reduce duplicates.
Month 3: land a medium severity finding and get Rank 2.
Month 6: focus on a niche and aim for Rank 3 invites.
Month 12: build a steady pipeline and target higher impact.

### 4.7 Tips to Level Up
- Pick a niche and master it
- Focus on programs with clear scope
- Write detailed reports with evidence
- Follow up quickly on triage questions
- Avoid noisy automation that causes duplicates

## 5. Program Types and Access
### 5.1 Public Bug Bounty Programs
Public programs are visible to all researchers.
Competition is higher, so speed matters.
Good for learning platform workflow and VRT.

### 5.2 Private Bug Bounty Programs
Private programs require an invitation.
They usually have fewer researchers and less noise.
Rewards can be higher and triage faster.

### 5.3 Vulnerability Disclosure Programs (VDP)
VDPs focus on disclosure without guaranteed payment.
Some offer swag, recognition, or points.
VDPs are useful for building reputation and practice.

### 5.4 Pentest Engagements
Pentest programs are time bound and scoped.
They may be invite only and heavily rule driven.
Reports often require stricter documentation.

### 5.5 Managed vs Customer Managed
Managed programs rely on Bugcrowd triage.
Customer managed programs may triage directly.
Managed programs usually provide consistent severity mapping.

### 5.6 Target Types
- Web applications and APIs
- Mobile apps with backend APIs
- Cloud services and misconfigurations
- IoT or firmware in rare programs
- Public infrastructure and DNS assets

### 5.7 Access Strategies
Start with public programs to learn the flow.
Build rank and kudos to earn private invites.
Keep a short list of core programs to avoid dilution.

## 6. Payout Structure
### 6.1 How Bounties Are Defined
Programs publish reward ranges by severity.
Rewards can be fixed per severity or variable.
Severity is typically mapped using VRT.

### 6.2 Typical Severity Mapping
- P1 Critical: remote code execution, auth bypass, full account takeover
- P2 High: significant data exposure, high impact privilege escalation
- P3 Medium: stored XSS, limited data access, weak authorization
- P4 Low: reflected XSS, minor information disclosure
- P5 Informational: best practice or low risk issues

### 6.3 Typical Payout Ranges (Approximate)
These ranges are common across many programs but vary widely.
Use them as rough expectations, not guarantees.
Severity | Typical range in USD | Notes
P1 Critical | 2000 to 20000+ | Highest variability
P2 High | 800 to 7000 | Common for serious issues
P3 Medium | 200 to 1500 | Most frequent paid tier
P4 Low | 0 to 300 | Often small or unpaid
P5 Info | 0 to 100 | Sometimes kudos only

### 6.4 Bonuses and Multipliers
First valid report on a new program can earn a bonus.
Exceptional clarity or impact can earn discretionary rewards.
Some programs pay extra for novel attack chains.

### 6.5 Payment Timing
Payment timing depends on the program and validation speed.
Many programs pay within one to four weeks after resolution.
Delays can occur when engineering teams need to confirm impact.

### 6.6 Payout Methods
Bugcrowd supports common payout options by region.
Typical options include PayPal and bank transfer providers.
Always verify your payment method before submitting high volume.

### 6.7 Taxes and Compliance
Researchers are responsible for local tax obligations.
Bugcrowd may request W 9 or W 8 forms as applicable.
Maintain records of payouts and dates for reporting.

### 6.8 Disputes and Mediation
Dispute channels exist when severity is contested.
Provide clear technical evidence to support impact.
Be professional and specific in severity discussions.

## 7. Private vs Public Programs
### 7.1 Public Program Advantages
- Immediate access and no invitation required
- Broad variety of targets for learning
- Faster exposure to triage feedback

### 7.2 Public Program Challenges
- High duplicate rate and competition
- Lower signal to noise for new assets
- Some programs may have narrow scope

### 7.3 Private Program Advantages
- Fewer researchers and fewer duplicates
- Often clearer scope and direct communication
- Higher likelihood of sustained earnings

### 7.4 Private Program Challenges
- Access requires rank or matching
- Some programs require stronger NDA terms
- Lower visibility into program rules until invited

### 7.5 How to Earn Private Invites
- Maintain consistent valid reports on public programs
- Complete Bugcrowd University modules
- Specialize in program relevant tech stacks
- Keep response times high during triage

### 7.6 Strategy for Balanced Portfolio
Keep one or two public programs for steady practice.
Focus most time on a small set of private programs.
Review scope changes weekly to catch new assets.

## 8. Program Lifecycle and Workflow
### 8.1 Submission Stages
Drafting: gather evidence and reproduction steps.
Submission: file the report with impact summary.
Triage: Bugcrowd validates and rates severity.
Customer review: program team confirms and fixes.
Resolution: report is closed and paid if eligible.

### 8.2 Communication Flow
Triage may ask for additional proof or clarifications.
Respond promptly to avoid delays or closure.
Use clear, structured updates for retest requests.

### 8.3 Retesting and Follow Up
Some programs request retest confirmation.
Retest should follow the original steps with updated proof.
Avoid testing outside scope during retest.

### 8.4 Safe Harbor and Rules
Programs typically include safe harbor language.
Always follow rules around rate limiting and data handling.
Stop testing immediately if you may impact production stability.

### 8.5 SLA and Timeboxing
Programs may define expected response windows.
Respect these timelines to build reputation.
If you need more time, ask triage early.

## 9. VRT Deep Dive
### 9.1 Purpose of the VRT
The VRT standardizes vulnerability categories and severity.
It aligns researchers, triage, and customers on impact.
Using VRT language in reports speeds up review.

### 9.2 Common VRT Categories
- Authentication and session management
- Authorization and access control
- Injection and code execution
- Cross site scripting and HTML injection
- Server side request forgery
- Insecure direct object references
- Sensitive data exposure
- Cryptographic weaknesses
- Misconfigurations and security headers
- Business logic and workflow abuse

### 9.3 Severity Considerations
Severity is based on impact, likelihood, and exploitability.
Context matters, such as user roles and data sensitivity.
Chainable bugs can elevate severity.

### 9.4 Evidence Needed for Severity
Provide a working proof of concept where possible.
Include affected endpoints and user roles.
State preconditions and required permissions.

### 9.5 Avoiding Overstatement
Do not claim full takeover without demonstrating it.
Separate potential impact from confirmed impact.
Use cautious language for hypothetical escalations.

### 9.6 When to Include VRT References
Add the most relevant VRT category in the summary.
Reference VRT severity to justify impact.
It helps triage map your report faster.

## 10. Success Strategies
### 10.1 Program Selection
Choose programs with clear scope and reward tables.
Look for assets recently added to reduce duplicates.
Prefer programs that match your experience level.

### 10.2 Scoping Discipline
Read in scope and out of scope lists carefully.
Note prohibited testing methods like brute forcing.
Document testing boundaries in your notes.

### 10.3 Recon and Asset Mapping
Enumerate subdomains and identify tech stacks.
Map API endpoints and authentication flows.
Validate ownership to avoid testing out of scope assets.

### 10.4 Prioritize High Impact Paths
Focus on authentication, authorization, and data access paths.
Test password reset and account recovery flows.
Look for logic bugs that bypass checks.

### 10.5 Methodology for Web Apps
- Identify user roles and permission boundaries
- Test IDORs and access control on every object
- Review file upload handlers and content validation
- Validate CSRF protections on state changing actions
- Assess server side validation vs client side only

### 10.6 Methodology for APIs
- Enumerate endpoints and parameter types
- Test for broken object level authorization
- Validate rate limits and token reuse
- Check error handling for sensitive data leaks
- Evaluate CORS and authentication flows

### 10.7 Methodology for Mobile
- Decompile and review local storage
- Check for hardcoded secrets and tokens
- Validate certificate pinning and TLS configuration
- Analyze API calls from the mobile client
- Test deep links and intent handling

### 10.8 Cloud and Infrastructure
- Check for misconfigured buckets and storage
- Review IAM role misuse if in scope
- Test for SSRF that reaches metadata endpoints
- Validate DNS and subdomain takeover risks

### 10.9 Duplicate Avoidance Tactics
Read recent program announcements and change logs.
Focus on newly added endpoints or features.
Reproduce findings on the latest version and capture proof.
Avoid submitting low impact issues that are often duplicates.

### 10.10 Quality Over Quantity
One high quality report can beat ten weak ones.
Spend time on clear reproduction steps.
Attach screenshots or videos with concise annotations.

### 10.11 Time Management
Plan focused sessions for a single program.
Track hours to understand your ROI.
Rotate programs only after a clear methodology pass.

### 10.12 Collaboration and Teaming
Some programs allow team submissions.
Agree on roles and split recon tasks.
Keep communications clear to avoid duplicate internal work.

## 11. Report Writing
### 11.1 Report Structure
- Title with vulnerability and asset
- Summary describing impact and scope
- Steps to reproduce in numbered order
- Proof of concept or payloads
- Impact analysis and severity reasoning
- Suggested remediation

### 11.2 Writing Clear Steps
Use exact URLs, parameters, and accounts.
Explain prerequisites such as roles or permissions.
Number each step and avoid extra commentary.

### 11.3 Evidence and Attachments
Provide screenshots, logs, or video captures.
Redact sensitive data not necessary for proof.
Include response headers or raw HTTP when needed.

### 11.4 Impact Language
Describe impact in terms of confidentiality, integrity, availability.
Avoid speculative statements without evidence.
If impact is potential, state assumptions explicitly.

### 11.5 Severity Justification
Map your finding to VRT category and severity.
Explain why exploitability is practical.
Show how an attacker can repeat the steps.

### 11.6 Example Report Snippet
Title: IDOR allows viewing other user invoices
Summary: User A can access invoices for User B by changing invoice id
Steps: Authenticate as User A, request invoice endpoint, replace id, observe data
Impact: Exposure of billing data for other accounts

## 12. Communication and Professionalism
### 12.1 Triage Responsiveness
Respond within 24 to 48 hours when possible.
Provide additional evidence quickly when asked.
If unavailable, communicate expected response time.

### 12.2 Tone and Clarity
Use factual and neutral language.
Avoid blame or sarcasm.
Thank triage for their time and feedback.

### 12.3 Handling Disagreements
Point to evidence and VRT references calmly.
Ask for clarification rather than making demands.
Accept that some programs may rate lower than expected.

### 12.4 Confidentiality
Do not disclose findings without permission.
Respect NDAs for private programs.
Use private notes for learning and anonymized summaries.

## 13. Common Rejection Reasons
- Duplicate submission already reported
- Out of scope asset or endpoint
- Missing proof of exploitability
- Best practice or low risk issue
- Vulnerability requires unrealistic conditions
- Self XSS or clickjacking not in scope
- Missing authentication or role context
- No security impact beyond functional behavior
- Incomplete report or missing reproduction steps
- Spam or automated low quality submissions

## 14. Tooling and Lab Setup
### 14.1 Core Tools
- Intercepting proxy like Burp Suite or OWASP ZAP
- Browser with multi profile support
- HTTP client like Postman or curl
- Note taking tool for reports and evidence

### 14.2 Recon Tools
- Subdomain enumeration tools
- DNS and certificate transparency queries
- Port scanning within scope and allowed rates
- Technology fingerprinting tools

### 14.3 Web Testing Tools
- Parameter discovery and fuzzers
- Session and cookie analysis tools
- Static analysis for client side code

### 14.4 Mobile Testing Tools
- Android emulator and iOS simulator
- APK or IPA analysis tools
- Proxy configuration for mobile devices

### 14.5 Cloud and Infrastructure Tools
- Cloud resource enumeration tools
- IAM policy analyzers where permitted
- SSRF detection helpers and safe payloads

### 14.6 Safe Testing Practices
Honor rate limits and avoid denial of service.
Keep attack traffic targeted and low volume.
Log your tests to reproduce issues precisely.

## 15. Comparison with HackerOne and Synack
### 15.1 High Level Comparison
Platform | Access model | Triage model | Researcher vetting | Typical program mix | Culture
Bugcrowd | Public and private | Managed triage common | Open signup | Bounty, VDP, pentest | Structured VRT
HackerOne | Public and private | Program managed or H1 triage | Open signup | Bounty and VDP | Broad community
Synack | Private only | Synack managed | Application and vetting | Time bound assessments | High formality

### 15.2 Bugcrowd vs HackerOne
Bugcrowd emphasizes VRT consistency across programs.
HackerOne offers a large public directory and fast start.
Both platforms support public and private programs.
Bugcrowd managed triage can reduce back and forth.
HackerOne offers a strong disclosure and writeup ecosystem.

### 15.3 Bugcrowd vs Synack
Synack is invite only and requires vetting.
Synack engagements are often time boxed and assigned.
Bugcrowd provides more open access and self selection.
Synack researchers may have fewer programs but lower competition.
Bugcrowd offers broader skill diversity and self paced work.

### 15.4 Choosing a Platform
Use Bugcrowd if you want structured VRT and managed triage.
Use HackerOne if you want maximum program variety.
Use Synack if you prefer vetted, scheduled engagements.
Many researchers use multiple platforms to diversify.

## 16. Real Earnings Data
### 16.1 Data Caveats
There is no official public earnings dataset from Bugcrowd.
Most data comes from self reported blogs or conference talks.
Figures below are approximate and can vary significantly.
Treat these as directional signals, not guarantees.

### 16.2 Self Reported Annual Ranges
- Casual researchers often report 0 to 1000 USD per year
- Part time consistent researchers report 1000 to 10000 USD
- Advanced researchers report 10000 to 100000 USD
- Top performers occasionally report 100000+ USD in strong years

### 16.3 Time to First Bounty
Many researchers report weeks to months before a first payout.
Learning curve and duplicates are common early obstacles.
Focusing on fewer programs improves early success.

### 16.4 Sample Self Reported Snapshots
Case A: New researcher reports 2 low severity bounties totaling 300 USD.
Case B: Intermediate researcher reports 12 bounties totaling 8000 USD in a year.
Case C: Specialist reports 25 bounties totaling 45000 USD focused on one niche.
Case D: Elite researcher reports 6 figure earnings across multiple platforms.

### 16.5 Per Bounty Distribution (Anecdotal)
- Many accepted reports pay between 200 and 1000 USD.
- High severity payouts are less frequent but dominate totals.
- A single P1 payout can exceed ten P4 payouts.

### 16.6 Earnings Volatility
Earnings are lumpy and unpredictable.
Program scope changes can reduce opportunities overnight.
Seasonal cycles and release schedules affect bug discovery.

### 16.7 Building Predictable Income
Diversify across multiple programs.
Track which assets yield consistent findings.
Invest in deeper testing rather than broad scanning.

### 16.8 ROI Calculation Example
If you spend 10 hours and earn a 500 USD bounty, the rate is 50 USD per hour.
If you spend 40 hours and earn a 2000 USD bounty, the rate is 50 USD per hour.
Track time spent to understand your effective rate.

### 16.9 Expenses to Consider
Proxy licenses, cloud labs, and hardware costs add up.
Learning time and opportunity cost should be included.
Budget for taxes and payment fees.

## 17. 30-60-90 Day Plan
### 17.1 First 30 Days
Complete Bugcrowd University basics.
Join two public programs and read rules carefully.
Practice report writing with lab targets.

### 17.2 Days 31 to 60
Focus on one program and build a methodology checklist.
Submit at least one well documented report.
Track duplicate causes and refine recon.

### 17.3 Days 61 to 90
Aim for medium severity findings and private invites.
Build a personal playbook for repeatable tests.
Review payouts and adjust program selection.

## 18. Legal and Ethics
Always operate within scope and safe harbor rules.
Do not access data beyond what is needed for proof.
Never use found data for personal gain.
Stop testing if you risk service disruption.
Report privacy issues with minimal data exposure.
Keep sensitive information encrypted in your notes.

## 19. Quality Checklist
- Read program rules and scope before testing
- Confirm target ownership and asset scope
- Reproduce the issue from a clean state
- Capture evidence and timestamps
- Provide clear reproduction steps
- Map to a VRT category and severity
- Explain impact with realistic attack scenarios
- Remove sensitive data not needed for proof
- Respond quickly to triage questions
- Retest only within scope

## 20. Glossary
- Asset: a target system or domain in scope
- Attack surface: all reachable components and endpoints
- Bounty: monetary reward for accepted reports
- CrowdMatch: invite matching based on profile signals
- Duplicate: previously reported vulnerability
- Informational: valid issue with minimal security impact
- NDA: non disclosure agreement for private programs
- P1 to P5: common severity tiers used by VRT
- Proof of concept: evidence demonstrating the issue
- Retest: verification after a fix
- Scope: allowed targets and actions
- Triage: validation and routing stage

## 21. Appendix A: Sample Report Template
Title:
Summary:
Program:
Asset:
VRT Category:
Severity:
Impact:
Steps to Reproduce:
1.
2.
3.
Expected Result:
Actual Result:
Proof of Concept:
Attachments:
Remediation Guidance:
Additional Notes:

## 22. Appendix B: Triage Checklist
- Verify program scope and rules
- Confirm reproduction steps are complete
- Validate impact against VRT
- Check for duplicates and prior reports
- Request additional evidence if needed
- Communicate severity reasoning clearly
- Close report with resolution summary

## 23. Appendix C: Resource List
- Bugcrowd University courses
- Bugcrowd VRT documentation
- OWASP Testing Guide
- OWASP Top 10
- Web Security Academy labs
- Common bounty report templates
- Community writeups and conference talks
