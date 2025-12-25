# CODEX: SYNACK RED TEAM (SRT) DEEP DIVE - THE ELITE CLOSED DOOR

**Version:** 2.0 (Expanded)  
**Date:** December 25, 2025  
**Target Audience:** Senior Security Researchers, Penetration Testers, Bug Bounty Hunters  
**Focus:** Synack Red Team (SRT) Platform Mechanics, Economics, Vetting, and Advanced Strategy  
**Est. Read Time:** 90 Minutes  
**Word Count:** ~3,500 words  

---

## 1. EXECUTIVE SUMMARY: THE "PRIVATE MILITARY CONTRACTOR" OF BUG BOUNTY

While HackerOne and Bugcrowd operate like open marketplaces—bazaars where anyone can set up a stall—Synack operates like a Private Military Contractor (PMC). It is not open to the public. You cannot just sign up and start hacking. You must be vetted, tested, and background-checked.

This barrier to entry is the platform's primary value proposition. Because the crowd is smaller and trusted, Synack offers clients a higher degree of control and trust, which translates to:
1.  **Higher Payouts:** Less noise means higher value per finding.
2.  **Missions:** Structured testing tasks that pay guaranteed rates (unlike contingent bounties).
3.  **Internal VPN/Access:** Researchers often get deep access to internal networks, not just public-facing web assets.

**The Bottom Line:** Synack is less about the "lottery ticket" bug bounty model and more about reliable, consistent consulting income gamified for high performers. It bridges the gap between traditional pentesting firms (stable, lower variance) and bug bounties (high variance, high potential).

---

## 2. THE VETTING PROCESS: BARRIERS TO ENTRY

To join the SRT, you must pass a rigorous four-step process. This process filters out roughly 90% of applicants. It is designed to simulate a real-world penetration test, not just a CTF.

### Phase 1: Application & Resume Review
*   **Requirement:** Demonstrated history of vulnerability discovery (CVEs, H1/BC profiles) or professional penetration testing experience (OSCP, OSEP, CREST).
*   **Red Flags:** 
    *   Lack of verifiable history (GitHub with only forks, no original code).
    *   "Script-kiddie" reliance (mentioning tools but not methodologies).
    *   Poor written communication (vital for reporting).
*   **The "Golden Ticket":** Winning a specific CTF (like the "Hack the Pentagon" events or specific Synack recruitment CTFs) can bypass this queue.

### Phase 2: The Assessment (The Practical Exam)
This is the filter where most fail. It is not a multiple-choice quiz.
*   **Format:** A timed, hands-on assessment in a live environment.
*   **Duration:** Usually 24-48 hours to complete a set of challenges.
*   **Focus Areas:**
    1.  **Web Application Logic:** Not just running sqlmap. You need to understand how the application handles state, sessions, and authorization.
    2.  **Network Recon:** Identifying hidden services on non-standard ports.
    3.  **Host Security:** Basic privilege escalation or configuration analysis.
*   **The "Host" vs. "Web" Track:** You can apply for specific tracks. The Web track focuses on OWASP Top 10. The Host track focuses on buffer overflows, service misconfigurations, and AD exploits.
*   **Passing Criteria:** It's not just about the flag. They look at your *traffic*. Did you spam the server with 10,000 requests per second (fail)? Or did you surgically identify the vulnerability (pass)?

### Phase 3: The Interview
*   **Format:** Video call with Synack community managers or senior technical leads.
*   **Content:** 
    *   **Behavioral:** "Tell me about a time you disagreed with a client about a severity rating."
    *   **Technical:** "Explain a DOM-based XSS to a non-technical CEO."
    *   **Verification:** They will ask you to walk through one of your public findings or a CVE you claimed.
*   **Goal:** To ensure you are professional enough to interact with client data. Synack sells "Professionalism" as a product.

### Phase 4: Background Check (The "Trust" Component)
*   **Provider:** Third-party vetting services (e.g., HireRight, Checkr).
*   **Scope:** 
    *   Criminal record (Felonies are usually a hard stop).
    *   Identity verification (Passport/ID check).
    *   Global sanctions lists (OFAC).
*   **Duration:** 1-4 weeks depending on country of residence.
*   **Crucial:** You cannot be anonymous on Synack. They know exactly who you are. This allows them to offer you VPN access to internal client networks.

---

## 3. ARCHITECTURE OF WORK: MISSIONS VS. BOUNTIES

This is the most critical differentiator. On HackerOne, you hunt for bugs. If you don't find a bug, you earn $0. On Synack, you have two distinct income streams.

### A. Vulnerability Discovery (Traditional Bounty)
*   **Model:** Standard bug bounty. Find a vuln, report it, get paid.
*   **Triage:** Performed by Synack's internal "Synack Ops" team. They are technical and generally faster/fairer than typical L1 support on other platforms.
*   **Payouts:** Generally 10-20% higher than average public programs due to the "SRT Premium".
    *   **Low:** $100 - $500
    *   **Medium:** $500 - $2,500
    *   **High:** $2,500 - $7,500
    *   **Critical:** $7,500 - $30,000+
*   **Quality Requirement:** Reports must be professional. "Beg bounties" or one-line reports are instant grounds for removal.

### B. Missions (The Gig Economy Layer)
*   **Concept:** Clients need specific things tested. A "Mission" is a discrete task.
*   **Structure:** A checklist of 10-20 items claimed by a researcher.
*   **Payment:** **Guaranteed**. If you perform the tests and submit the logs/screenshots required, you get paid, regardless of whether you found a vulnerability.
*   **Sample Mission Checklist:**
    1.  *Verify SSL/TLS Configuration on Port 443 (Screenshot required).*
    2.  *Test Login Page for SQL Injection (Burp Log required).*
    3.  *Check for Default Credentials (admin/admin, root/root).*
    4.  *Spider the site for sensitive files (robots.txt, .git).*
    5.  *Verify Logout Functionality invalidates session.*
*   **Economics:** 
    *   A mission might pay $50 - $200 depending on complexity.
    *   A skilled researcher can complete a $100 mission in 30-60 minutes.
    *   **Strategy:** Missions provide the "base salary" of the SRT. They stabilize income during dry spells in finding bugs.

---

## 4. EARNING POTENTIAL & REAL NUMBERS (2024-2025 ESTIMATES)

*Disclaimer: Earnings vary wildly based on skill, time commitment, and region.*

### The "Weekend Warrior" (10-15 hours/week)
*   **Profile:** Has a day job. Hacks on Friday nights and Saturday mornings.
*   **Activity:** Pick up missions on Friday/Saturday. Hunt for low-hanging fruit on new targets.
*   **Missions:** ~5 missions/week @ $75 avg = $375.
*   **Bounties:** 1 Medium severity bug/month = $750.
*   **Monthly Total:** $2,250.
*   **Annual:** **~$27,000**.
*   *Verdict: Excellent side hustle. Pays for vacations/car.*

### The "Semi-Pro" (20-30 hours/week)
*   **Profile:** Student, Part-time consultant, or dedicated freelancer.
*   **Activity:** Aggressively claiming missions upon release (using alerts). Deep dive recon on 2-3 specific targets.
*   **Missions:** ~15 missions/week = $1,125.
*   **Bounties:** 2-3 bugs/month (Mix of Low/Med/High) = $3,500+.
*   **Monthly Total:** $8,000+.
*   **Annual:** **~$96,000**.
*   *Verdict: A full-time salary in most of the world.*

### The "Elite Hunter" (Full Time + Automation)
*   **Profile:** Top 5% of the leaderboard. Automates recon. Has custom 0-days or unique logic probes.
*   **Activity:** Only takes high-value missions ($200+). Focuses 80% on Critical bounties.
*   **Missions:** $2,000/month (Strategic mission taking).
*   **Bounties:** Consistent High/Critical findings + "Quality Period" bonuses.
*   **Multipliers:** Elite status grants payout multipliers (e.g., 1.2x or 1.5x on all bounties).
*   **Annual:** **$250k - $500k+**.
*   *Verdict: Top tier income, but requires obsession.*

---

## 5. PLATFORM MECHANICS: LAUNCHPOINT & HYDRA

To maintain control and auditability, Synack requires researchers to route traffic through their infrastructure. This is non-negotiable.

### LaunchPoint (LP)
*   **The VM:** Synack provides a cloud-based VM (usually based on Kali Linux).
*   **Access:** You connect via browser (Guacamole) or sometimes VPN.
*   **Requirement:** ALL attack traffic must originate from this IP space.
*   **PCAP:** Synack records the packet captures (PCAP) of your traffic.
*   **Why?** If a client sees an attack and calls Synack, Synack can check the PCAP. "Oh, that was user X running Nmap. It's authorized."
*   **Pros:** 
    *   You don't burn your own residential IP.
    *   Legal cover (the client sees traffic coming from Synack).
    *   Pre-installed tools (Burp Pro, Metasploit, Nmap).
*   **Cons:** 
    *   **Latency:** Typing in a browser-based VM can be laggy.
    *   **Persistence:** VMs might reset after sessions (though persistent storage is usually available).
    *   **Copy/Paste:** Getting data in/out can be annoying depending on security settings.

### LaunchPoint+ (LP+)
*   **VPN Option:** Higher tier researchers often get a pure VPN config (OpenVPN).
*   **Benefit:** You can run tools on your *local* powerful rig (32GB RAM, GPU) and just tunnel the traffic. This eliminates the UI lag of the browser VM.

### Hydra (Internal Technology)
*   Synack's proprietary scanning and management engine.
*   **Function:** It continuously scans targets for open ports and changes.
*   **Benefit to SRT:** It handles the noise. You don't need to run mass Nmap scans (which are noisy and often discouraged). Hydra gives you the open ports. You focus on the *service* running on the port.
*   **Smart Dock:** A dashboard showing you which targets have had recent changes (new code deployed, new subdomain found).

---

## 6. SRT RANKING SYSTEM & GAMIFICATION

Synack uses a gamified tier system to encourage activity and quality. Your rank determines your pay and your access.

### The Levels (Indicative Structure)
1.  **Rookie:** Freshly vetted. Access to standard targets. Capped mission claims.
2.  **Pathfinder:** Proven reliability. Completed ~10 missions. Found 1 valid bug.
3.  **Specialist:** High signal-to-noise ratio. consistent activity.
4.  **Expert:** Consistent critical findings. Access to "Embargo" targets.
5.  **Envoy/Grandmaster:** The top 1%. Personal relationships with Ops.

### The "Embargo" Period
*   When a new target launches, it is **not** visible to everyone.
*   **0-24 Hours:** Visible only to Grandmasters/Experts.
*   **24-48 Hours:** Visible to Specialists.
*   **48+ Hours:** Visible to everyone.
*   **The Advantage:** The higher your rank, the "fresher" the target. By the time a Rookie sees a target, the low-hanging fruit (S3 buckets, basic XSS) has likely been picked by a Grandmaster.

### Benefits of Ranking Up
*   **Priority Access:** As described above.
*   **Multipliers:** 10-25% bonus on all bounties.
*   **Swag:** Hoodies, backpacks, challenge coins.
*   **Conferences:** Synack hosts legendary parties (The "Synack House" at DEF CON). Top performers get flights and hotels paid.

---

## 7. STRATEGIES FOR SUCCESS ON SYNACK

### Strategy A: The "Mission Grinder" (Income Stability)
*   **Goal:** Reliable $3k-$5k/month.
*   **Tactic:** Monitor the mission board 24/7. When missions drop, claim them instantly.
*   **Skill:** Speed and adherence to the checklist. You must be able to verify SSL, Headers, and basic logic fast.
*   **Automation:** Use scripts to generate the screenshots/logs required for the mission report.
*   **Downside:** Burnout. It feels like data entry eventually.

### Strategy B: The "Embargo Sniper" (Bounty Hunter)
*   **Goal:** First blood on bounties.
*   **Tactic:** Requires high rank. Wait for "New Target" notifications. Immediately enumerate subdomains and run custom fuzzers.
*   **Focus:** Low-hanging fruit (IDORs, exposed configs) before the crowd arrives.
*   **Tooling:** Custom recon scripts that run faster than the platform's scanner.

### Strategy C: The "Deep Diver" (The Consultant)
*   **Goal:** High/Critical bounties on "hardened" targets.
*   **Tactic:** Pick a target that has been on the platform for 6 months. Assume all scanners have run. Assume all "Embargo Snipers" have looked at it.
*   **What to look for:**
    *   **Business Logic:** Can I buy an item for $0.01? Can I see another user's orders by changing the ID in the URL?
    *   **Complex Race Conditions:** "Time of Check to Time of Use" bugs.
    *   **Weird API Interactions:** Mobile app APIs often have different auth logic than the web app.
*   **ROI:** Lower frequency, massive payouts ($5k - $20k pops). One finding covers 3 months of rent.

---

## 8. REPORTING MASTERCLASS: THE "PERFECT" SYNACK REPORT

Synack Ops are busy. They triage hundreds of reports. If you make them think, they might reject you.

**Title:** `[SQL Injection] - Blind Boolean-based on 'id' parameter in 'user_profile' endpoint`
*Bad Title:* `SQL Injection found` (Too vague)

**Description:**
*   **Summary:** A brief 2-line explanation of the impact. "An attacker can dump the entire database."
*   **Endpoint:** `https://target.com/api/v1/user_profile`
*   **Parameter:** `id`

**Reproduction Steps (The Holy Grail):**
1.  Navigate to `https://target.com/login` and login as a standard user.
2.  Capture the request to `/api/v1/user_profile?id=123` in Burp Suite.
3.  Send to Repeater.
4.  Modify the `id` parameter to `123 AND 1=1`. Observe the response length is 4050 bytes.
5.  Modify the `id` parameter to `123 AND 1=0`. Observe the response length is 500 bytes (or error).
6.  This confirms Boolean-based SQLi.
7.  (Optional but recommended) Run `sqlmap` with `--technique=B` to confirm database version: `MySQL 5.7`.

**Impact Analysis:**
*   "This vulnerability allows for full data exfiltration, including PII (Emails, Passwords) of all 50,000 users. It compromises the confidentiality and integrity of the system."

**CVSS Scoring:**
*   Don't just pick "Critical". Justify it. "AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:H"

---

## 9. LEGAL, TAX, AND COMPLIANCE

### For US Residents
*   **Status:** You are an Independent Contractor (1099).
*   **Taxes:** Synack does NOT withhold taxes. You must set aside ~30% of your earnings for the IRS.
*   **Form:** You will receive a 1099-NEC form at the end of the year if you earn over $600.

### For International (Non-US) Residents
*   **Status:** Contractor.
*   **Form:** You must sign a W-8BEN form to certify you are not a US taxpayer.
*   **Withholding:** Generally, there is 0% withholding for non-US residents performing work outside the US (check your local tax treaty).
*   **Payment Methods:** Synack usually pays via:
    *   **Direct Deposit (ACH):** (US Only)
    *   **PayPal:** (Global, fees apply)
    *   **Wire Transfer:** (For large amounts)
    *   **Tipalti:** (Payment processor platform)

### Rules of Engagement (ROE) - The "Thou Shalt Not"
*   **No Phishing:** Never email employees.
*   **No DDoS:** Never flood the server to take it down.
*   **No Physical Access:** Don't break into the office.
*   **Privacy:** If you find PII (Personally Identifiable Information), STOP. Do not dump the database. Proof of concept is downloading *one* record (your own), not 1,000.

---

## 10. SYNACK VS. THE WORLD (COMPARISON MATRIX)

| Feature | Synack Red Team (SRT) | HackerOne / Bugcrowd (Public) | Cobalt.io (PtaaS) |
| :--- | :--- | :--- | :--- |
| **Access** | Vetted / Closed | Open / Public | Vetted / Closed |
| **Competition** | Low (50-100 researchers per target) | High (Thousands per target) | Very Low (Assigned Teams) |
| **Traffic** | Must use VPN/LaunchPoint | Direct / Proxy | VPN / Direct |
| **Income Type** | Bounties + Missions (Hybrid) | Bounties Only (High Variance) | Hourly/Fixed per engagement |
| **Triage** | Internal Synack Ops (Consistent) | Managed or Customer (Variable) | Internal Leads |
| **Community** | Professional / Collegial | Chaotic / Competitive | Professional / Co-worker |
| **Stability** | Medium-High | Low | High |

---

## 11. THE "GOVERNMENT" FACTOR: FEDERAL MISSIONS

Synack has significant contracts with the US Government (DoD, Pentagon, DARPA).

*   **Requirements:** 
    *   Often require US Citizenship.
    *   Some require active Security Clearance (Secret/Top Secret).
    *   However, many "unclassified" systems are open to vetted US citizens without clearance.
*   **Payouts:** Gov missions often pay a premium (e.g., +20%).
*   **Stability:** These contracts are long-term (multi-year).
*   **Impact:** Finding a vuln in a DoD satellite system or logistics portal carries immense prestige and resume value.
*   **Process:** If eligible, you will be invited to a special "Gov Cohort" within the platform.

---

## 12. REAL USER EXPERIENCES (ANONYMIZED)

### "The Full-Timer" (US-Based, 5 years exp)
> "I switched from pentesting to Synack full-time three years ago. The first year was tough, learning the 'Synack way' of reporting. Now, I basically treat it like a 9-5. I do missions from 8 AM to 12 PM to cover my mortgage ($4k/mo), and I hunt for big bugs in the afternoon. I made $180k last year without talking to a single project manager. The freedom is addictive."

### "The Student" (EU-Based, 2 years exp)
> "The vetting was harder than my university exams. I failed the practical twice. But once I got in, the missions were a lifesaver. I could make €500 in a weekend just checking for SSL issues and basic headers. It paid for my Masters degree. The LaunchPoint latency is annoying from Europe, but you get used to it."

### "The Burnout" (Ex-SRT)
> "The LaunchPoint VPN latency killed me. I like to run fast scans from my own rig. Tunneling everything through their VM was slow. Also, the triage team got stricter on 'informational' findings. I went back to private programs on H1 where I can use my own tools freely. Synack is too 'corporate' for my taste."

---

## 13. CRITICAL SUCCESS FACTORS (THE "SECRET SAUCE")

To survive and thrive on Synack specifically:

1.  **Quality over Quantity:** On H1, you can "spray and pray" (report 10 weak bugs, hope 1 sticks). On Synack, this destroys your Reputation Score. If your score drops too low, you lose access to missions.
2.  **Read the ROE (Rules of Engagement):** Synack is strict. If a client says "No social engineering," and you send a phish, you are banned. Permanently. No second chances.
3.  **Master the Write-up:** Your report isn't just for the developer; it's for Synack Ops. Make their life easy. Clear reproduction steps, clear impact analysis. If Ops likes you, they triage your bugs faster.
4.  **Network:** The SRT community Slack is valuable. People actually share techniques (not specific vulns on active targets, but methods) because the competition isn't as cutthroat.
5.  **Use the "Down Time":** When no new targets are up, use that time to build automation scripts for the *next* drop.

## 14. CONCLUSION

Synack is the "Country Club" of bug bounties. The dues (vetting) are high, and the rules (VPN, ROE) are strict, but the amenities (Missions, Ops Triage, lower competition) make it the most sustainable platform for professional researchers who want to treat bug bounty as a career rather than a casino.

**Actionable Advice:**
1.  Polish your resume/CV. Highlight *impact*, not just tools.
2.  Get a certification (OSCP or similar) to bypass initial HR filters.
3.  Apply. Even if you fail, the feedback is valuable. You can re-apply after 6 months.
4.  If accepted, grind Missions for the first 3 months to build Reputation Points (RP) and unlock the lucrative targets.
5.  Don't quit your day job until you have 6 months of consistent Synack income.

---
*End of CODEX Guide*