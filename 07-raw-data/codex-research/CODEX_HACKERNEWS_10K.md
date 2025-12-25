# CODEX HACKER NEWS 10K RESEARCH
## Ask HN security consulting, freelance pentester, and bug bounty income threads

## Scope, Methodology, and Limitations

This report synthesizes internal Hacker News research already present in this repository. It does **not** include live web browsing or new external verification. All figures and discussion summaries are derived from previously captured HN thread notes and should be validated directly in the linked threads before making business decisions.

**Coverage snapshot**:
- 36+ targeted HN searches, 3,000+ comments (2009–2025), emphasis 2020–2025.
- Focus on Ask HN threads about security consulting, freelance pentesting, and bug bounty income.
- Includes community commentary on rates, client acquisition, platform friction, and career strategy.

**Interpretation rules used here**:
- Rates and payouts are anecdotal signals, not guarantees.
- Income ranges reflect HN community estimates and examples.
- “Consulting rate” refers to billable client pricing, not employee salary.
- Any scenario modeling is illustrative and labeled as such.

## Source Index (Internal Repository)

Primary sources referenced in this report:

- `HACKER_NEWS_COMPREHENSIVE_INSIGHTS_2025.md`
- `HN_SECURITY_CONSULTING_COMPILATION_2025.md`

## Executive Summary

- HN consensus frames a bifurcated market: stable full-time security roles vs. volatile freelance and bug bounty paths.
- Network referrals dominate consulting lead flow; cold outreach rarely wins high-value work.
- Market demand is shifting toward risk management and compliance over “pure pentesting.”
- Reported standard consulting rates cluster around $100–$250/hr; niche expertise commands $300–$500/hr.
- Training/speaking can yield ~$3,000/day, while expert networks cite ~$500/hr for rare expertise.
- Freelance pentesting has a steep learning curve; manual pentests are expensive, slow, and hard to verify for coverage.
- Bug bounty income is power-law distributed: top 1–5% earn most payouts; most participants treat it as a side hustle.
- Platform friction is common (duplicate disputes, NDAs, triage quality, and non-payment complaints).
- Retainers and fractional vCISO models ($3k–$8k/month per client) are recurring stability themes.
- Long sales cycles (3–9 months) and liability concerns demand a cash runway and strong contracts.

---

## Table of Contents

1. [Thread Index (Ask HN + HN)](#1-thread-index-ask-hn--hn)
2. [Market Landscape & Community Consensus](#2-market-landscape--community-consensus)
3. [Consulting Rates & Income Signals](#3-consulting-rates--income-signals)
4. [Freelance Pentester Pathways](#4-freelance-pentester-pathways)
5. [Bug Bounty Income Reality](#5-bug-bounty-income-reality)
6. [Client Acquisition & Reputation](#6-client-acquisition--reputation)
7. [Engagement & Delivery Standards](#7-engagement--delivery-standards)
8. [Transition & Career Strategies](#8-transition--career-strategies)
9. [Risk, Ethics, and Platform Friction](#9-risk-ethics-and-platform-friction)
10. [Opportunity Map: Services & Niches](#10-opportunity-map-services--niches)
11. [Scenario Models (Illustrative)](#11-scenario-models-illustrative)
12. [Verification Checklist](#12-verification-checklist)
13. [Appendix: Thread Summaries](#13-appendix-thread-summaries)

---

## 1. Thread Index (Ask HN + HN)

### 1.1 Security Consulting & Advisory

- **[Ask HN: How do you become a security consultant?](https://news.ycombinator.com/item?id=7589479)** (Apr 2014) — Entry advice on turning vulnerability expertise into paid consulting.
- **[Tell HN: Information security audit/consulting is largely a scam industry](https://news.ycombinator.com/item?id=32039828)** (Jul 2022) — Insider critique of compliance theater, balanced by practical wins like MFA and privilege reduction.
- **[Cryptography/security consultant - what I do](https://news.ycombinator.com/item?id=16003650)** (Dec 2017) — Consulting is about expertise plus communication and client satisfaction.
- **[Consulting in cryptography and security design](https://news.ycombinator.com/item?id=30188512)** (Feb 2022) — Lean marketing, inbound requests once reputation is established.
- **[Synacktiv Security Consulting](https://news.ycombinator.com/item?id=19632158)** (Apr 2019) — Boutique firm model founded by long-tenured consultants.

### 1.2 Consulting Rates & Pricing

- **[Ask HN: What is the highest consulting rate you've come across, in tech?](https://news.ycombinator.com/item?id=28356047)** (Aug 2021) — High-end pricing examples for specialists and one-person shops.
- **[Ask HN: What do you do and what's your consulting rate?](https://news.ycombinator.com/item?id=30188101)** (Feb 2022) — Wide range of rates tied to system integration and strategy work.
- **[$1000+/day consulting rates](https://news.ycombinator.com/item?id=17015333)** (May 2018) — Training/speaking leading to $3k/day engagements.
- **[Freelancer and consulting rates survey](https://news.ycombinator.com/item?id=2991350)** (Sep 2011) — Low-end hourly vs. high-end weekly rates.
- **[Major consulting firm rates](https://news.ycombinator.com/item?id=2189462)** (Feb 2011) — High client billing rates vs. consultant pay.
- **[Tech consultant hourly rates](https://news.ycombinator.com/item?id=7559468)** (Apr 2014) — Experienced developers should avoid sub-$75/hr work.
- **[Consulting rates vs annual salaries](https://news.ycombinator.com/item?id=20999557)** (Sep 2019) — Sales/marketing skills matter as much as coding.
- **[How much to charge for first freelance consultancy](https://news.ycombinator.com/item?id=25870129)** (Jan 2021) — Recommendations at $300–$500/hr for specialized expertise.

### 1.3 Freelance & Contract Work Sourcing

- **[Ask HN: What's a reasonable rate for contract software engineer?](https://news.ycombinator.com/item?id=9728997)** (Jun 2015) — Contract rate anchoring and the dangers of underpricing.
- **[Ask HN: Where to find contract work as developer?](https://news.ycombinator.com/item?id=27097426)** (May 2021) — Discovery channels, tech stack specialization, and contract pipelines.
- **[Ask HN: How does one get into contract work?](https://news.ycombinator.com/item?id=39482510)** (Feb 2024) — Personal relationships and reputation are decisive.
- **Monthly “Ask HN: Freelancer? Seeking freelancer?” threads** — Recurring, community-policed postings.

### 1.4 Freelance Pentesting & Penetration Testing

- **[Penetration testing and low-cost freelancing](https://news.ycombinator.com/item?id=24869219)** (Oct 2020) — Common vulnerabilities, small-client realities.
- **[Ask HN: Have you performed penetration test for your company?](https://news.ycombinator.com/item?id=40168610)** (Apr 2024) — New tester asking for pricing; building a portfolio via free/discounted tests.
- **[I work as pentester (freelance nowadays)](https://news.ycombinator.com/item?id=37558656)** (Sep 2023) — “Sheer amount of stuff you’re supposed to know.”
- **[Shared thoughts after 6 years in Pentesting](https://news.ycombinator.com/item?id=14631830)** (Jun 2017) — Skepticism about cert obsession; value is in demonstrable skills.
- **[Ask HN: How did you get started in Network Security/Penetration Testing?](https://news.ycombinator.com/item?id=15152957)** (Sep 2017) — Start with current discipline, learn web vulns, pursue certs selectively.
- **[Launch HN: MindFort – AI agents for continuous pentesting](https://news.ycombinator.com/item?id=44117465)** (May 2025) — Manual pentests are slow/expensive; AI tooling emerging.
- **[Show HN: Hackerest – Real-time penetration testing](https://news.ycombinator.com/item?id=46216649)** (2025) — Pentests take days/weeks; productized pentesting.
- **[Show HN: Oneleet – Penetration Testing for SOC 2](https://news.ycombinator.com/item?id=35905927)** (May 2023) — Compliance-focused PTaaS model.
- **[Show HN: Building a Market for Penetration Testing](https://news.ycombinator.com/item?id=10990462)** (Feb 2016) — Coverage uncertainty in pentests.

### 1.5 Bug Bounty Income & Platform Economics

- **[Ask HN: Bug Bounty Dilemma](https://news.ycombinator.com/item?id=44507114)** (Jul 2025) — NDA vs. public disclosure on a €1,000 payout.
- **[Life as a bug bounty hunter](https://news.ycombinator.com/item?id=17829644)** (Sep 2018) — $5,000 Facebook bounty anecdote; impact on early-career finances.
- **[Apple introduces $2M bug bounty](https://news.ycombinator.com/item?id=45557772)** (2025) — High-end payouts for spyware-class issues.
- **[Sei pays out $2M bug bounty](https://news.ycombinator.com/item?id=40710201)** (Jun 2024) — Crypto/DeFi payouts reaching seven figures.
- **[Google paid $10M in bug bounty rewards last year](https://news.ycombinator.com/item?id=39682265)** (Mar 2024) — Annual payout totals.
- **[$100M in bounties paid via HackerOne](https://news.ycombinator.com/item?id=23326511)** (Jun 2020) — Platform-wide cumulative payout headline.
- **[HackerOne appears completely broken](https://news.ycombinator.com/item?id=22404022)** (Mar 2020) — Non-payment/triage dispute complaints.
- **[Bugcrowd quality concerns](https://news.ycombinator.com/item?id=41130304)** (Aug 2024) — Triage quality criticism.
- **[Bugcrowd designed to control narrative](https://news.ycombinator.com/item?id=42795047)** (Jan 2025) — Platform incentives and disclosure control critiques.
- **[XBOW autonomous pentester reaches #1 on HackerOne](https://news.ycombinator.com/item?id=44367548)** (Jun 2025) — “Economic numbers game” framing of platform competition.

### 1.6 Zero-Day Compensation

- **[Ask HN: Best way to get paid for discovering zero day exploits?](https://news.ycombinator.com/item?id=9931551)** (Jul 2015) — Salary + benefits vs. sporadic bounty pay.

---

## 2. Market Landscape & Community Consensus

HN discussions repeatedly frame security consulting as a business discipline as much as a technical one. Market maturity, compliance demand, and automation shape both pricing power and required differentiation.

**Core themes**:
- **Bifurcated market**: Full-time roles provide stable, predictable compensation; freelance and bounty paths are high upside but volatile.
- **Compliance as demand driver**: Clients increasingly pay for risk management and audit readiness rather than “cool hacking.”
- **Specialization beats generalism**: Deep expertise in a niche (cryptography, cloud, AppSec, compliance) commands premium rates.
- **Communication wins deals**: Consultants must translate vulnerabilities into business outcomes and remediation steps.
- **Automated tooling pressure**: Low-effort pentests are commoditized; human insight and reporting remain differentiators.

**Career outcome framing from HN**:

| Path | Income Range (HN estimates) | Stability | Notes |
| --- | --- | --- | --- |
| Full-time security engineer | $120k–$250k+ | High | Benefits, steady comp, clear path. |
| Staff/Principal security (FAANG) | $300k–$600k+ | High | “Golden handcuffs.” High stress, high pay. |
| Freelance consultant | $100k–$400k+ | Low | High upside, requires sales + delivery. |
| Bug bounty hunter | $0–$500k+ | None | Pure power-law; most earn little. |

---

## 3. Consulting Rates & Income Signals

HN threads provide a consistent range of rate signals across general consulting, niche expertise, and training/speaking engagements.

### 3.1 Rate Benchmarks (From HN Threads)

| Rate Type | HN Range/Signal | Notes |
| --- | --- | --- |
| Minimum experienced hourly | $75/hr+ | “Don’t go below this” for skilled consultants. |
| Standard consulting hourly | $100–$250/hr | Common for pentesting/engineering consulting. |
| Specialized consulting hourly | $300–$500/hr | Cryptography, niche systems, high-stakes IR. |
| Expert network consults | ~$500/hr | High-end expert calls. |
| Major firm bill rate | ~$250/hr | Client pays vs. consultant take-home. |
| Training/speaking | ~$3,000/day | Events can lead to consulting deals. |
| Weekly ranges | $8k–$24k/week | From freelancer rate surveys. |
| vCISO retainers | $3k–$8k/month | Fractional CISO advisory (HN synthesis). |

### 3.2 Pricing Heuristics from HN Discussions

- Start with **2–3x** your employee hourly equivalent to cover downtime and overhead.
- Fixed-price projects are increasingly preferred by clients; pad estimates **20–30%** for scope creep.
- Avoid price competition; specialized positioning yields the highest rates.
- Raise rates as soon as demand outpaces capacity.

### 3.3 Income Caveats & Overhead

- Non-billable time (sales, admin, reporting) erodes hourly earnings.
- No benefits: health insurance, retirement, and paid leave must be self-funded.
- Cash flow is irregular; long sales cycles require a savings buffer.

---

## 4. Freelance Pentester Pathways

### 4.1 Entry Skills & Learning Curve

- Most entrants start with web vulnerabilities (XSS, SQLi, auth flaws).
- “Sheer amount of stuff you’re supposed to know” is a recurring theme.
- Build on your current discipline (web dev → web security).

### 4.2 Certification Debate (HN Themes)

- OSCP is respected for hands-on rigor.
- Some commenters warn: employers overly focused on certs can be a red flag.
- Practical demonstrations (write-ups, tooling, talks) often carry more weight.

### 4.3 Portfolio Building & First Clients

- Early-stage testers may offer free/discounted pentests to build a portfolio.
- Public write-ups, CTFs, and open-source tools are favored for credibility.
- HN monthly freelancer threads provide early exposure but require strict posting etiquette.

### 4.4 Delivery Reality in HN Threads

- Manual pentests often run **days to weeks**, not hours.
- Cost per assessment is typically **tens of thousands** for serious engagements.
- Coverage is hard to verify; scope clarity is essential.

### 4.5 Career Progression Signals

- Specialization improves rates and client trust (cloud, crypto, AppSec).
- Many pentesters plan to shift toward security architecture or advisory work over time.

---

## 5. Bug Bounty Income Reality

### 5.1 Power-Law Earnings (HN Consensus)

- Top **1–5%** of hunters earn the majority of payouts.
- Most participants treat bounties as a side hustle or learning tool.
- Income is highly irregular; long dry spells are common.

### 5.2 Reported Income Ranges (HN Synthesis)

| Experience Tier | HN Community Estimates | Notes |
| --- | --- | --- |
| Beginner (0–1 yr) | $0–$500/month | Slow start; duplicates common. |
| Intermediate | $2k–$5k/month | Requires consistent methodology. |
| Elite (Top 1%) | $100k–$500k+/year | Often teams or heavy automation. |

### 5.3 Notable Payout Signals in HN Threads

- **$2,000,000**: Apple bug bounty (spyware-class).
- **$2,000,000**: Sei bug bounty (crypto).
- **$10,000,000**: Google annual bug bounty payout total (2024).
- **$100,000,000**: Cumulative platform payout headline (HackerOne).
- **$5,000**: Facebook bounty (2013 anecdote).
- **€1,000**: High-criticality bounty with NDA (UK company).

### 5.4 Platform Friction & Trust Issues

- Duplicate marking and payment disputes are recurring complaints.
- NDAs can limit disclosure and community learning.
- Platform triage quality varies widely by program.
- Some commenters frame platforms as “economic numbers games.”

### 5.5 Strategy Guidance from HN

- Treat bug bounty as **skill-building or reputation-building** early on.
- Focus on programs with transparent payout and fair triage reputations.
- Automation is increasingly necessary to compete at high tiers.
- Web3/crypto bounties pay more but require specialized knowledge and carry higher risk.

---

## 6. Client Acquisition & Reputation

HN threads consistently stress that client acquisition is the hardest part of consulting.

**Primary acquisition channels**:
- Personal networks and former colleagues (most effective).
- Content marketing: blogs, technical write-ups, and open-source tooling.
- Conference talks (DefCon, BSides) and community recognition.
- Referrals from satisfied clients.
- HN monthly freelancer threads as supplemental visibility.

**Positioning guidance**:
- Niche down (e.g., “Cloud Security for Fintech,” “SOC 2 readiness for SaaS”).
- Sell business outcomes (audit pass, risk reduction), not just fear or vulnerabilities.
- Build reputation before ramping pricing.

---

## 7. Engagement & Delivery Standards

HN commentary emphasizes that delivery quality and clarity drive repeat business.

**Scoping and execution**:
- Define scope precisely to avoid coverage disputes.
- Align on success criteria and testing depth.
- Document findings with reproducible steps and evidence.

**Reporting**:
- Write actionable reports for non-technical stakeholders.
- Prioritize remediation over raw vulnerability lists.
- Follow up to confirm fixes and reduce rework.

**Client satisfaction**:
- Combine technical rigor with strong communication.
- Provide “practical wins” (MFA, least privilege, hardening).
- Offer retest windows or ongoing advisory to build long-term relationships.

---

## 8. Transition & Career Strategies

HN contributors advise against abrupt transitions without runway and pipeline.

**Common transition tactics**:
- Keep a full-time role while building a consulting portfolio.
- Save **3–6 months** of expenses before going independent.
- Start with limited-scope engagements to prove delivery quality.
- Use training/speaking to seed consulting leads.
- Aim for retainers or fractional vCISO work to stabilize income.

**Bug bounty to consulting**:
- Use a strong bounty profile to establish credibility.
- Convert bounty wins into case studies (where disclosure allows).
- Be ready to sell client outcomes, not just findings.

---

## 9. Risk, Ethics, and Platform Friction

HN threads include consistent warnings about legal, ethical, and operational risk.

**Risk signals**:
- Liability exposure requires professional insurance and clear contracts.
- Compliance-driven security work can feel like “checkbox theater.”
- Platforms can mediate disputes in favor of buyers/program owners.
- NDAs reduce transparency and reduce reputation-building benefits.

**Operational stressors**:
- Feast-or-famine revenue cycles.
- Underpricing and overwork lead to burnout.
- Market commoditization pressures low-end pentesting.

---

## 10. Opportunity Map: Services & Niches

HN discussions highlight recurring consulting niches and how they connect to pricing power.

**High-signal niches (HN mentions)**:
- **Cryptography & security design**: Rare expertise, higher rates, strong advisory demand.
- **Compliance readiness (SOC 2, audit prep)**: Predictable budgets, recurring needs.
- **Cloud security & architecture**: High demand as infrastructure shifts to cloud.
- **Application security**: Bread-and-butter for startups; needs clear reporting.
- **Pentesting-as-a-service**: Productized testing with faster cycles.
- **Fractional vCISO**: Retainers for startups needing strategic guidance.

**Service packaging ideas**:
- Fixed-scope assessments with retest windows.
- Ongoing quarterly security reviews to create predictable revenue.
- Advisory “office hours” for engineering teams.

---

## 11. Scenario Models (Illustrative)

These scenarios use HN rate ranges as inputs. They are **not** forecasts; they are simple calculations to visualize pricing impact.

### 11.1 Standard Consulting (Illustrative)

- **Assumption**: $150/hr (within $100–$250/hr range).
- **Billable hours**: 20 hrs/week, 46 weeks/year (illustrative).
- **Gross revenue**: $150 × 20 × 46 = **$138,000/year**.

### 11.2 Specialist Consulting (Illustrative)

- **Assumption**: $350/hr (within $300–$500/hr range).
- **Billable hours**: 15 hrs/week, 46 weeks/year.
- **Gross revenue**: $350 × 15 × 46 = **$241,500/year**.

### 11.3 Fractional vCISO Retainer (Illustrative)

- **Assumption**: $5,000/month per client (within $3k–$8k range).
- **Clients**: 3 retainers.
- **Gross revenue**: $5,000 × 3 × 12 = **$180,000/year**.

### 11.4 Bug Bounty Income Bands (HN Estimates)

- **Beginner**: $0–$500/month.
- **Intermediate**: $2,000–$5,000/month.
- **Elite (Top 1%)**: $100k–$500k+/year.

**Reminder**: These numbers ignore taxes, insurance, tooling, and downtime.

---

## 12. Verification Checklist

Before acting on any insight in this report:

- Read the original HN threads for context and nuance.
- Validate current rates in your local market and specialty.
- Confirm platform payout rules and disclosure requirements.
- Secure professional liability coverage and legal review of contracts.
- Build a clear scope template to reduce coverage disputes.
- Track billable vs. non-billable time to price sustainably.

---

## 13. Appendix: Thread Summaries

Below are condensed summaries of the most relevant HN threads referenced in this report.

### Security Consulting & Advisory

- **Ask HN: How do you become a security consultant?** (2014)
  - Start with existing domain knowledge and expand into security.
  - Charge to identify and fix vulnerabilities.
  - Communicate clearly with non-technical stakeholders.

- **Tell HN: Information security audit/consulting is largely a scam industry** (2022)
  - Critique of compliance theater and misaligned incentives.
  - Practical security wins still matter (MFA, privilege reduction).
  - Reports are often ignored once paid.

- **Cryptography/security consultant - what I do** (2017)
  - Expertise plus client satisfaction is the core value.
  - Clear explanations and trust drive repeat business.

- **Consulting in cryptography and security design** (2022)
  - Lean marketing can work once reputation is strong.
  - Inbound requests replace outbound sales over time.

- **Synacktiv Security Consulting** (2019)
  - Boutique firm model started by senior consultants.
  - Highlights the viability of specialized security shops.

### Consulting Rates & Pricing

- **Ask HN: Highest consulting rate you've seen** (2021)
  - High-end rates for specialists and one-person shops.
  - Pricing power correlates with reputation and scarcity.

- **Ask HN: What do you do and what's your consulting rate?** (2022)
  - Wide variation based on systems integration vs. strategy.
  - Demonstrates how “consulting” spans many categories.

- **$1000+/day consulting rates** (2018)
  - Training/speaking can drive $3k/day engagements.
  - Visibility creates inbound consulting leads.

- **Freelancer and consulting rates survey** (2011)
  - Low-end hourly rates contrast with high-end weekly pricing.
  - Reinforces the importance of positioning and specialization.

- **Major consulting firm rates** (2011)
  - Clients pay premiums for brand and process.
  - Consultants often receive a fraction of billed rates.

- **Tech consultant hourly rates** (2014)
  - Experienced consultants should avoid sub-$75/hr work.
  - Price floors protect long-term earning power.

- **Consulting rates vs annual salaries** (2019)
  - Sales and marketing skills often gate higher rates.
  - Pure hourly work has a ceiling without differentiation.

- **How much to charge for first freelance consultancy** (2021)
  - $300–$500/hr suggested for specialized security expertise.
  - Underpricing can damage perceived value.

### Freelance & Contract Work Sourcing

- **Ask HN: What's a reasonable rate for contract software engineer?** (2015)
  - Underpricing is common for first-time contractors.
  - Quick acceptance is a signal the rate is too low.

- **Ask HN: Where to find contract work as developer?** (2021)
  - Prior experience and specialization open doors.
  - Generalist positioning is less effective.

- **Ask HN: How does one get into contract work?** (2024)
  - Personal relationships are key to initial contracts.
  - Reputation grows through consistent delivery.

- **Monthly “Ask HN: Freelancer? Seeking freelancer?”**
  - Strict rules: only post if actively hiring or seeking work.
  - Useful for visibility but not a primary lead channel.

### Freelance Pentesting & Penetration Testing

- **Penetration testing and low-cost freelancing** (2020)
  - Common findings include weak passwords and header mistakes.
  - Small clients often need practical hygiene improvements.

- **Ask HN: Have you performed penetration test for your company?** (2024)
  - New tester seeking pricing guidance.
  - Portfolio-building via free tests is common early on.

- **I work as pentester (freelance nowadays)** (2023)
  - Skill breadth expectations are overwhelming.
  - Most entrants begin with web vulnerabilities.

- **Shared thoughts after 6 years in Pentesting** (2017)
  - Certificates are not a substitute for real ability.
  - Employer overemphasis on certs can be a warning sign.

- **Ask HN: How did you get started in Network Security/Penetration Testing?** (2017)
  - Start with current discipline; learn web vulns first.
  - Certifications can help, but practical proof matters.

- **Launch HN: MindFort – AI agents for continuous pentesting** (2025)
  - Manual pentests are expensive and slow.
  - AI tools promise continuous testing but still evolving.

- **Show HN: Hackerest – Real-time penetration testing** (2025)
  - Pentests typically run for days/weeks, not hours.
  - Productized pentesting is a growing niche.

- **Show HN: Oneleet – Penetration Testing for SOC 2** (2023)
  - Compliance-focused PTaaS with vetted testers.
  - SOC 2 demand is a recurring revenue driver.

- **Show HN: Building a Market for Penetration Testing** (2016)
  - Coverage uncertainty is a persistent concern.
  - Buyers struggle to measure pentest completeness.

### Bug Bounty Income & Platform Economics

- **Ask HN: Bug Bounty Dilemma** (2025)
  - NDA vs. disclosure tradeoffs at €1,000 payout.
  - Highlights platform/legal pressure on researchers.

- **Life as a bug bounty hunter** (2018)
  - $5,000 Facebook bounty anecdote.
  - Bounties can be meaningful but inconsistent.

- **Apple introduces $2M bug bounty** (2025)
  - Seven-figure payout potential for critical exploits.
  - Sets expectations for top-tier researchers.

- **Sei pays out $2M bug bounty** (2024)
  - Crypto bounties can exceed traditional programs.
  - Highlights smart-contract risk and payout scale.

- **Google paid $10M in bug bounty rewards last year** (2024)
  - Large aggregate payouts do not imply broad distribution.
  - Debates on adequacy of compensation vs. profits.

- **$100M in bounties paid via HackerOne** (2020)
  - Headline figure underscores platform scale.
  - Community debates over distribution fairness.

- **HackerOne appears completely broken** (2020)
  - Complaints about non-payment and communication failures.
  - Reinforces the need to vet program reputations.

- **Bugcrowd quality concerns** (2024)
  - Triage quality criticized.
  - Researchers report dismissed valid findings.

- **Bugcrowd designed to control narrative** (2025)
  - Perception that platforms prioritize company narratives.
  - Disclosure timelines remain contentious.

- **XBOW autonomous pentester reaches #1 on HackerOne** (2025)
  - Competitive automation signals rising bar for earnings.
  - “Economic numbers game” framing of bounty platforms.

### Zero-Day Compensation

- **Ask HN: Best way to get paid for discovering zero day exploits?** (2015)
  - Stable salaries and benefits often beat sporadic payouts.
  - Highlights risk tradeoffs of independent research.

