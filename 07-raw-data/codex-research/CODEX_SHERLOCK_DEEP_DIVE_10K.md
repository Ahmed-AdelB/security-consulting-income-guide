# CODEX: Sherlock Web3 Security Contests Deep Dive
## The Comprehensive Guide to Audit Contests, Judging, and $10K/Week Outcomes

**Version:** 1.0
**Focus:** Sherlock contests, smart contract auditing, income engineering
**Target Audience:** Web3 security researchers, smart contract developers, auditors
**Income Potential:** $2,000 - $40,000+/month (performance-based)
**Goal Range:** $1K - $10K/week for senior auditors
**Positioning:** High-trust, judge-led contest platform with curated sponsors

---

## 1. Executive Summary
Sherlock is a Web3 security contest platform that runs time-boxed audits.
Researchers, called Watsons, review smart contract code for vulnerabilities.
Sponsors fund a prize pool that is split among valid findings.
The platform emphasizes consistent judging and clear reporting standards.
Sherlock contests reward unique, high-impact vulnerabilities.
Income is variable, but senior Watsons can target $1K-$10K per week.
This guide explains the platform mechanics, judging process, and earning math.
It also provides strategies to move from beginner to senior performance.

---

## 2. Platform Overview
### 2.1 What Sherlock Is
Sherlock runs competitive security reviews for Web3 protocols.
Contests are time-boxed and scoped to specific codebases.
Most contests are public and open to all qualified auditors.
Sherlock publishes final reports for community learning.

### 2.2 Mission and Positioning
Provide reliable security coverage to Web3 teams.
Create a consistent, judge-led audit experience.
Reward independent auditors for validated findings.
Improve ecosystem safety with transparent reports.

### 2.3 Key Differentiators
Lead Senior Judge model for consistent severity decisions.
Curated contest intake with clearer scope and specs.
Smaller, focused contest participation relative to larger platforms.
High emphasis on PoCs and impact clarity.

### 2.4 Typical Sponsor Types
DeFi protocols launching new pools or upgrades.
Bridges and cross-chain infrastructure.
DAOs deploying treasury systems and governance modules.
Wallets, staking protocols, and restaking networks.

### 2.5 Typical Codebases
Solidity contracts on EVM chains.
Vyper contracts for select protocols.
Rust or Move contracts for non-EVM chains.
Off-chain automation scripts and keeper bots.

### 2.6 Core Roles and Terms
Sponsor: the protocol team funding the contest.
Watson: the auditor submitting findings.
Judge: auditor validating reports and severity.
Lead Senior Judge: primary decision maker for final results.
Sherlock Team: staff managing contest logistics and payouts.
Escalation Panel: group reviewing appeals and disputes.

### 2.7 Contest Types
Public contests with open participation.
Invite-only contests with curated auditor lists.
Focused contests on single modules or upgrades.
Occasional follow-up contests for patched code.

### 2.8 Contest Artifacts
In-scope contract lists.
Out-of-scope clarifications.
Documentation and protocol specs.
Threat model assumptions and privileged roles.

### 2.9 Strengths
Consistent judging and dedupe criteria.
Clear rules around severity and scope.
Structured contest updates and Q&A.
Quality final reports for reputation building.

### 2.10 Tradeoffs
Competitive environment with many duplicates.
Income variability tied to contest volume.
Requires strong writing and PoC quality.
Escalations can add time before payouts.

---

## 3. Contest Structure and Lifecycle
### 3.1 Contest Sizing and Duration
Small contests: 7 to 10 days.
Medium contests: 10 to 14 days.
Large contests: 14 to 21 days.
Durations depend on scope size and complexity.

### 3.2 Phase 1: Announcement and Scope Review
Contest page goes live with dates and rules.
Repository and documentation become available.
In-scope contracts are listed explicitly.
Out-of-scope areas are clearly stated.
Watsons set up local environments and tooling.

### 3.3 Phase 2: Early Orientation
Review architecture diagrams and dependencies.
Identify critical assets and trust boundaries.
Note upgradeability or admin control features.
Draft a threat model with attacker assumptions.

### 3.4 Phase 3: Active Audit Window
Watsons review code and run tests.
Q&A remains open for clarifications.
Sherlock may publish answers or updates.
Contest time pressure drives focused analysis.

### 3.5 Phase 4: Submission Cutoff
All reports must be submitted before deadline.
Late submissions are rejected without review.
Reports are kept private until judging concludes.

### 3.6 Phase 5: Initial Triage
Judges filter out-of-scope or invalid submissions.
Obvious duplicates are grouped.
High-priority issues are reviewed first.

### 3.7 Phase 6: Deep Judging
Judges validate exploitability and impact.
Reports are grouped by root cause.
Severity is assigned per rubric.
Lead Senior Judge resolves conflicts.

### 3.8 Phase 7: Sponsor Review
Sponsors validate intended behavior.
Sponsors can dispute severity or validity.
Judges incorporate sponsor feedback.

### 3.9 Phase 8: Escalations
Watsons submit appeals for misjudged findings.
Escalation panel reviews evidence.
Final decisions are recorded.

### 3.10 Phase 9: Final Report
Sherlock publishes a final report.
Payouts are calculated and distributed.
Watsons are credited for accepted findings.

### 3.11 Submission Visibility Model
Reports are private during the contest.
Privacy reduces copycat submissions.
Final reports become educational references.

### 3.12 What Counts as a Valid Finding
Demonstrable exploit or clear security impact.
In-scope code paths with realistic assumptions.
Reproducible logic with clear transaction steps.
Impact aligned with contest rules.

### 3.13 Common Invalid Reasons
Out-of-scope components or dependencies.
Assumptions contradicting sponsor specs.
No realistic attacker or unrealistic permissions.
Missing PoC or incomplete impact statement.
Purely informational or stylistic comments.

### 3.14 Deduplication Logic
Same root cause and impact are deduped.
Different root causes with distinct impact are separate.
Report clarity helps acceptance but does not alter shares.
Dedupes split the reward evenly.

### 3.15 Severity Rubric Snapshot
High: direct loss of funds or critical control.
Medium: significant risk or protocol disruption.
Low: limited impact or unlikely edge case.
QA or Gas: quality improvements or efficiency gains.
Always use the contest-specific rubric.

### 3.16 Example 14-Day Timeline
Day 0: announcement and repository access.
Day 1: environment setup and docs review.
Day 2: architecture mapping and asset flow.
Day 3: access control and role review.
Day 4: initialization and upgradeability review.
Day 5: accounting math and invariants.
Day 6: external calls and reentrancy checks.
Day 7: oracle and price dependency review.
Day 8: permissionless actions and griefing.
Day 9: edge cases and state transitions.
Day 10: fuzzing and invariant testing.
Day 11: PoC drafting and validation.
Day 12: report writing and severity mapping.
Day 13: final proofreading and submission.
Day 14: deadline and submission lock.

---

## 4. Prize Pools and Payout Mechanics
### 4.1 Prize Pool Composition
Sponsors deposit a fixed prize pool.
Pools range from tens of thousands to six figures.
Payout currency is usually a stablecoin.
The pool is split across severity tiers.

### 4.2 Share-Based Allocation
Findings are assigned shares, not fixed bounties.
Each severity tier has a weight.
Deduped findings share the tier allocation.
Unique findings capture larger portions.

### 4.3 Severity Weights (Illustrative)
High severity receives the largest pool share.
Medium severity receives a meaningful share.
Low and QA may receive smaller shares or no payout.
Exact weights are defined per contest.

### 4.4 Duplicate Handling
Duplicates are grouped by root cause.
Each report in a group receives equal share.
Being first does not guarantee more payout.
Clarity and correctness prevent invalidation.

### 4.5 Solo vs Team Submissions
Teams submit under a single Watson handle.
Teams split rewards internally.
Teams can increase coverage but require coordination.

### 4.6 Example Payout Math
Pool: $100,000.
High allocation: 70 percent ($70,000).
Medium allocation: 30 percent ($30,000).
Two High issues, two reports each.
Each High issue receives $35,000.
Each report receives $17,500.

### 4.7 Incentive Summary
Unique Highs are the highest earners.
Multiple Mediums can outpace a single High.
Low and QA are best for learning and recognition.

### 4.8 Sponsor Disputes and Adjustments
Sponsors can argue about expected behavior.
Judges may downgrade or invalidate.
Documentation clarity affects final outcomes.

### 4.9 Impact of Escalations
Successful escalations restore severity.
Unsuccessful escalations do not reduce payout.
Escalations can delay final distribution.

### 4.10 Common Payout Mistakes
Overstating severity without impact evidence.
Submitting speculative or unproven attacks.
Missing critical assumptions in the report.
Failing to align with contest scope.

---

## 5. Earning Potential and Weekly Outcomes
### 5.1 The Income Ladder
Beginner Watsons: $0 to $2,000 per month.
Developing Watsons: $2,000 to $6,000 per month.
Senior Watsons: $4,000 to $40,000 per month.
Top performers: $50,000+ in strong months.

### 5.2 Senior Weekly Range Target
Senior Watsons can target $1K to $10K per week.
The upper end requires unique Highs or multiple Mediums.
The lower end is achievable with consistent Mediums.
Weekly outcomes depend on contest volume and pot size.

### 5.3 Volume Assumptions
One contest per week is aggressive.
Many Watsons focus on one or two per month.
Large codebases reduce contest throughput.

### 5.4 Realistic Weekly Scenarios
Scenario A: Medium in a $50k pool with five duplicates.
Expected payout range: $1K to $3K.
Scenario B: Unique Medium in a $60k pool.
Expected payout range: $4K to $8K.
Scenario C: Unique High in a $100k pool.
Expected payout range: $15K to $35K.

### 5.5 Variance and Volatility
Monthly income can swing dramatically.
One strong finding can cover multiple months.
Plan for gaps and contest dry spells.

### 5.6 Risk Mitigation
Keep a cash buffer of 3 to 6 months.
Track contest calendar and overlap.
Use off-contest weeks for skill upgrades.

### 5.7 Portfolio Strategy
Mix small and medium contests for steady flow.
Reserve time for large, high-profile codebases.
Avoid chasing too many contests simultaneously.

### 5.8 The $10K/Week Plan for Seniors
Target one unique High per month.
Supplement with two to three Mediums per month.
Maintain a pipeline of two contests in progress.
Build specialization to reduce competition overlap.

---

## 6. Judging Process Deep Dive
### 6.1 Judge Responsibilities
Validate correctness of vulnerability claims.
Assess severity using the contest rubric.
Deduplicate similar reports and root causes.
Communicate with sponsors for intent confirmation.
Write clear notes for final report summaries.

### 6.2 Typical Judging Workflow
Initial triage and invalid filtering.
Grouping by root cause and impact.
Deep review for exploitability and severity.
Discussion with Lead Senior Judge for edge cases.
Draft final report and payout calculations.

### 6.3 Severity Determination Criteria
Direct theft or irreversible loss drives High severity.
Protocol disruption or partial loss is Medium.
Low-likelihood or low-impact issues trend Low.
Economic abuse without theft can be Medium.

### 6.4 How Judges Interpret PoCs
Working tests increase acceptance odds.
Clear transaction sequences are required.
Ambiguous PoCs reduce confidence.
Concise reproduction steps matter.

### 6.5 Communication with Sponsors
Judges confirm expected behavior and threat model.
Sponsors clarify admin assumptions and constraints.
Sponsor feedback can change severity.

### 6.6 Escalation Process Overview
Watsons submit a written appeal with evidence.
Escalation panel evaluates the arguments.
Panel may confirm or modify the decision.
Escalations are final once resolved.

### 6.7 Winning Escalations
Reference exact logic and line numbers.
Show a minimal exploit path.
Align the argument with rubric language.
Keep the appeal short and technical.

---

## 7. Lead Senior Judge (LSJ) Role
### 7.1 LSJ Definition
The LSJ is the primary judge for the contest.
They set severity precedent and resolve conflicts.
They are accountable for the final report quality.

### 7.2 LSJ Responsibilities
Coordinate the judging team and timelines.
Ensure consistent severity across findings.
Resolve duplicates and edge-case disputes.
Communicate with the sponsor for context.
Approve the final report and payout breakdown.

### 7.3 Why the LSJ Matters to Watsons
LSJ interpretations define acceptable severity claims.
Clear LSJ guidance reduces uncertainty.
LSJ decisions shape contest precedent.

### 7.4 Required Skills for LSJ
Deep smart contract auditing experience.
Strong judgment on economic and technical impact.
Clear written communication and neutrality.
Ability to manage many reports and deadlines.

### 7.5 LSJ Compensation and Incentives
LSJs are paid fixed fees or retainers.
Compensation is separate from Watson payouts.
The role builds strong reputation for future work.
LSJs often receive repeat engagements.

### 7.6 Path to Becoming an LSJ
Build a strong public contest record.
Submit consistent, high-quality findings.
Engage in community discussions professionally.
Demonstrate mentorship and reliability.

### 7.7 How Watsons Should Engage with the LSJ
Read contest rules and LSJ clarifications.
Ask concise questions during Q&A.
Use professional tone during escalations.
Provide clean evidence with minimal speculation.

### 7.8 LSJ Expectations in Reports
Clearly stated impact and threat model.
Minimal reproduction steps with realistic attacker.
Precise line references and code excerpts.
Practical mitigations that align with protocol intent.

### 7.9 LSJ Red Flags
Overstated severity or vague impact.
Missing PoC or speculative exploitation.
Out-of-scope assumptions.
Confusing writeups or inconsistent terminology.

---

## 8. Success Strategies for Watsons
### 8.1 Preparation Before the Contest
Read rules, scope, and exclusions.
Review past Sherlock reports for similar patterns.
Set up local environment and dependencies.
Map critical assets and trust boundaries.

### 8.2 Threat Modeling First
Identify who can call each function.
Define attacker capabilities and permissions.
List assets that can be stolen or frozen.
Define protocol invariants and safety properties.

### 8.3 Layered Review Strategy
Start with architecture and token flow.
Review external calls and upgradeability.
Check access control and role management.
Inspect accounting and precision math.
Finish with edge cases and state transitions.

### 8.4 Invariant-Driven Thinking
List balances that must always reconcile.
Track minted and burned token totals.
Verify share pricing in vault systems.
Ensure collateralization ratios remain consistent.

### 8.5 Common High-Value Areas
Initialization and upgrade flows.
Cross-contract callbacks and hooks.
Oracle dependencies and price timing.
Fee accounting and reward distribution.
Emergency controls and pausing logic.

### 8.6 PoC-First Mindset
Draft PoCs as soon as a hypothesis forms.
Validate the exploit with minimal assumptions.
Keep tests short and deterministic.
Save failing tests as evidence.

### 8.7 Report Writing Excellence
Use a crisp impact-first title.
Explain root cause and why the code is wrong.
Show exact exploit steps with realistic actors.
Provide a minimal PoC or transaction trace.
Recommend a concrete mitigation.

### 8.8 Preventing Duplicates
Read Q&A for known clarifications.
Track your findings in a personal log.
Prioritize unusual edge cases and novel logic.
Validate unique impacts, not just unique functions.

### 8.9 Managing Time and Focus
Choose fewer contests with higher preparation.
Front-load analysis in the first half.
Reserve final days for PoCs and report polish.
Avoid context switching across too many codebases.

### 8.10 Team Strategies
Divide modules across team members.
Share notes and threat models daily.
Use a single report writer for consistent voice.
Avoid internal duplicates with clear responsibilities.

### 8.11 Escalation Strategy
Escalate only when impact is clear.
Reference the rubric and scope explicitly.
Provide a deterministic reproduction path.
Keep the appeal short and technical.

### 8.12 Reputation Building
Publish high-quality reports.
Contribute to community discussions.
Maintain a clean and professional profile.
Help others with clarifications and tooling tips.

### 8.13 Mental Health and Sustainability
Schedule breaks during long contests.
Avoid all-night marathons for multiple days.
Track productivity without burnout.
Use post-contest time for rest and learning.

### 8.14 Economic Attack Modeling
Map how value moves between pools and vaults.
Simulate extreme price movements.
Check for oracle manipulation paths.
Look for incentive misalignment between roles.

### 8.15 Competition Strategy
Select contests with less overlapping researcher focus.
Prioritize novel protocols rather than forks.
Review the sponsor's previous audits to avoid duplicates.
Balance speed with depth to capture unique findings.

---

## 9. Watson Workflow and Tooling
### 9.1 Environment Setup
Clone the repo and verify commit hashes.
Install dependencies with locked versions.
Run the baseline test suite.
Document any failing tests or required configs.

### 9.2 Workspace Organization
Create a notes folder with dated files.
Track findings with severity hypotheses.
Store PoC scripts in a dedicated folder.
Use consistent naming for tests and scripts.

### 9.3 Review Passes
Pass 1: architecture and module mapping.
Pass 2: access control and roles.
Pass 3: asset flow and accounting.
Pass 4: edge cases and state transitions.
Pass 5: external calls and oracle dependencies.

### 9.4 Static Analysis Workflow
Run Slither for obvious issues.
Scan for uninitialized variables and reentrancy.
Review warnings and map to actual flows.
Document false positives for future speed.

### 9.5 Dynamic Analysis Workflow
Write Foundry tests for invariants.
Use fuzzing to explore boundary inputs.
Simulate attacker flows with `vm.prank`.
Use forked chains when external integrations matter.

### 9.6 Manual Review Techniques
Trace storage mutations across functions.
Verify role checks for all privileged calls.
Audit custom math for rounding risk.
Map dependency graphs for cross-contract calls.

### 9.7 Tooling Cheat Sheet
Foundry: tests, fuzzing, and quick PoCs.
Hardhat: scripting and deployment emulation.
Slither: fast static analysis.
Aderyn: additional static checks.
Mythril: symbolic execution for complex paths.
Echidna: property-based fuzzing.
Tenderly: trace debugging and transaction inspection.

### 9.8 Evidence Collection
Keep screenshots of failing tests.
Log transaction traces with clear inputs.
Capture call graphs for complex sequences.
Save reproduction steps in a simple markdown file.

### 9.9 Report Drafting Workflow
Draft summary first, then root cause.
Write PoC steps before mitigation.
Add line references after final edits.
Run a final clarity pass for length and precision.

### 9.10 Quality Assurance for Reports
Check for scope alignment.
Confirm attacker assumptions are valid.
Remove speculative language.
Ensure mitigation matches the root cause.

---

## 10. Communication and Q&A Playbook
### 10.1 Why Q&A Matters
Sponsor clarifications reduce invalid submissions.
Q&A can reveal intended invariants and constraints.
Questions can shape severity interpretation.

### 10.2 When to Ask Questions
When intent is unclear or contradictory.
When privileged roles are ambiguous.
When external dependencies are undefined.
When documentation conflicts with code.

### 10.3 How to Ask Effective Questions
Be concise and reference specific functions.
State the assumption you need validated.
Avoid leading questions that imply a bug.
Ask one question per message.

### 10.4 Q&A Do and Do Not
Do ask about role permissions and invariants.
Do ask about upgradeable deployment assumptions.
Do not ask for hints about vulnerabilities.
Do not flood the channel with multiple posts.

### 10.5 Logging Q&A Answers
Record answers in your notes.
Update your threat model with clarifications.
Cite responses in your reports if needed.

---

## 11. Comparison: Sherlock vs Code4rena vs Spearbit
### 11.1 Quick Comparison Table
| Dimension | Sherlock | Code4rena | Spearbit |
| --- | --- | --- | --- |
| Model | Contest-based audits | Contest-based audits | Curated audit collective |
| Primary Audience | Watson researchers | Wardens | Senior auditors |
| Access | Public contests | Public contests | Invite or referral |
| Judging | Lead Senior Judge and panel | Lead judge and lookouts | Internal QA and peer review |
| Payout Basis | Prize pool shares | Prize pool shares | Fixed fees or retainers |
| Income Volatility | High | High | Moderate |
| Typical Timeline | Weeks | Weeks | Weeks to months |
| Best For | Structured contest learning | High volume contesting | Stable premium work |
| Competition | Medium to high | High | Low (curated) |
| Output | Public final report | Public final report | Private client report |
| Repeatability | Moderate | High | High with retainers |
| Skill Growth | High | High | High but specialized |
| Reputation Signal | Strong public track record | Strong public track record | Private references |

### 11.2 Sherlock vs Code4rena
Sherlock tends to run fewer contests with tighter scopes.
Code4rena runs more frequent contests with larger crowds.
Sherlock LSJ model can provide clearer severity alignment.
Code4rena offers larger community scale and history.
Both reward unique High and Medium findings.

### 11.3 Sherlock vs Spearbit
Spearbit operates like a boutique audit firm.
Compensation is fixed and negotiated, not prize-based.
Spearbit emphasizes long-term relationships and code ownership.
Sherlock is better for competitive skill growth and public reputation.
Spearbit is better for stable, predictable income.

### 11.4 Choosing the Right Platform
Choose Sherlock for structured contest learning.
Choose Code4rena for high contest volume.
Choose Spearbit for premium, stable audit work.
A hybrid strategy can combine contests with private work.

### 11.5 Hybrid Strategy Example
Use Sherlock for competitive learning and visibility.
Use Code4rena for volume and diverse exposure.
Use Spearbit or private audits for stability.
Rotate focus to avoid burnout and maintain income.

---

## 12. Payout Timelines and Logistics
### 12.1 Typical Timeline
Contest ends and submissions lock.
Judging and deduping begin within days.
Sponsor review follows initial judging.
Escalations are processed after sponsor feedback.
Final report is published once decisions are final.
Payments are issued after report approval.

### 12.2 Typical Payout Window
Fast contests can pay within 3 to 4 weeks.
Complex contests can take 6 to 8 weeks.
Escalations or disputes can extend timelines.

### 12.3 Common Delay Drivers
Large volume of submissions.
Complex or disputed findings.
Slow sponsor feedback.
Additional clarification requests.

### 12.4 Payment Methods
Stablecoin transfers are common.
Some sponsors pay in token or fiat.
Ensure wallet addresses are correct and verified.

### 12.5 Operational Best Practices
Track contest dates and payout status.
Maintain a log of findings and report IDs.
Store payout confirmations for accounting.
Keep copies of final reports and credits.

### 12.6 Tax Considerations
Treat payouts as income under local law.
Track token values at time of receipt.
Consult professionals for compliance guidance.

---

## 13. Real Auditor Earnings (Modeled + Public Patterns)
### 13.1 Why This Section Uses Ranges
Payouts vary by contest size and competition.
Sherlock final reports show pool sizes and payouts.
Exact earnings are public only when auditors share them.
Ranges below are based on pool math and typical splits.

### 13.2 Contest Pot Ranges (Common Observations)
Small contests: $20k to $40k pools.
Medium contests: $40k to $80k pools.
Large contests: $80k to $150k+ pools.
Special audits can exceed these ranges.

### 13.3 Modeled Payout Scenarios
Scenario 1: Medium in a $40k pool with four duplicates.
Estimated payout range: $1k to $3k.
Scenario 2: Unique Medium in a $60k pool.
Estimated payout range: $4k to $8k.
Scenario 3: Two Mediums in a $60k pool, two duplicates each.
Estimated payout range: $3k to $6k.
Scenario 4: Unique High in a $100k pool.
Estimated payout range: $15k to $30k.
Scenario 5: High in a $120k pool with two duplicates.
Estimated payout range: $10k to $20k.
Scenario 6: Multiple low-impact or QA items.
Estimated payout range: $0 to $1k.
Scenario 7: Unique High plus Medium in a $120k pool.
Estimated payout range: $20k to $40k.

### 13.4 Monthly Earnings Patterns
One strong find can cover an entire month.
Two to three Mediums per month can yield $5k to $15k.
A single unique High can exceed $20k in a month.
Top Watsons often mix contests and private audits.

### 13.5 The Senior $1K-$10K/Week Reality
At $1K/week, a Watson needs occasional Mediums.
At $5K/week, a Watson needs consistent unique Mediums.
At $10K/week, a Watson needs a mix of Highs and Mediums.
The biggest lever is unique impact, not submission volume.

### 13.6 Factors That Increase Earnings
Targeting codebases with novel logic.
Submitting clean PoCs that avoid invalidation.
Choosing contests with manageable competition.
Building speed with reusable tooling.

### 13.7 Factors That Suppress Earnings
Crowded contests with duplicate findings.
Overreliance on automated tools.
Weak impact statements that lead to downgrades.
Failure to align with sponsor assumptions.

### 13.8 Where to Validate Earnings Yourself
Read Sherlock final reports for payout math.
Track contest pools and duplicates to model shares.
Follow public Watson profiles and disclosure threads.
Maintain a spreadsheet to estimate ROI per contest.

---

## 14. Common Pitfalls
### 14.1 Technical Pitfalls
Missing protocol invariants.
Ignoring upgradeable proxy initialization.
Assuming price feeds are trustworthy without checks.
Overlooking cross-chain or bridge assumptions.

### 14.2 Process Pitfalls
Starting too late in the contest window.
Skipping documentation and threat model review.
Submitting rushed reports without PoCs.
Failing to dedupe internally on teams.

### 14.3 Reporting Pitfalls
Using vague titles like bug in function.
Omitting clear impact or attacker assumptions.
Not linking to relevant lines of code.
Providing mitigation that changes protocol intent.

### 14.4 Communication Pitfalls
Combative escalation language.
Unclear questions in Q&A.
Overconfidence in severity without evidence.

---

## 15. Sample Weekly Operating System
### 15.1 Monday (Contest Kickoff)
Read docs and architecture.
List critical assets and trust boundaries.
Set up repository and run baseline tests.
Create initial threat model notes.

### 15.2 Tuesday (Deep Dive)
Map state transitions and invariants.
Review access control and privileged operations.
Start tests for critical paths.
Document any suspicious logic.

### 15.3 Wednesday (Exploit Exploration)
Focus on edge cases and error handling.
Add fuzzing for value ranges.
Draft initial findings.
Prioritize unique impact opportunities.

### 15.4 Thursday (PoC and Reporting)
Finalize PoCs with reproducible steps.
Write reports with clear impact analysis.
Cross-check severity with rubric.
Peer review within a team if possible.

### 15.5 Friday (Finalization)
Re-review reports for clarity.
Check scope and out-of-scope exclusions.
Submit before the deadline.
Archive notes for post-contest review.

### 15.6 Off-Contest Week
Review final reports from previous contests.
Document lessons and new patterns.
Improve tooling and templates.
Network with other Watsons.

---

## 16. Report Template (Sherlock-Optimized)
### 16.1 Title
Short, impact-first title.
Example: Unauthorized withdraw drains escrowed funds.

### 16.2 Summary
Two to three sentences explaining the issue.
Include attacker requirements and high-level impact.

### 16.3 Root Cause
Explain the exact logic error.
Point to specific conditions or missing checks.
Reference the relevant code lines.

### 16.4 Proof of Concept
Minimal steps to reproduce.
Include test code or transaction sequence.
Show expected versus actual behavior.

### 16.5 Exploit Steps
Step 1: attacker preconditions.
Step 2: triggering transaction sequence.
Step 3: resulting fund loss or state corruption.

### 16.6 Impact Analysis
Describe loss, freeze, or protocol failure.
Quantify if possible.
Explain why the impact is credible.

### 16.7 Mitigation
Provide a minimal code change.
Avoid redesign unless necessary.
Explain how the fix addresses the root cause.

### 16.8 Severity Justification
Map to contest rubric.
Explain why the impact is High or Medium.
Avoid severity inflation.

### 16.9 Assumptions
List attacker permissions and required state.
Call out any external dependency requirements.
Ensure assumptions align with scope.

### 16.10 References
Link to related functions and documentation.
Include relevant tests or traces.
Cite any sponsor clarifications if used.

---

## 17. Checklists
### 17.1 Pre-Contest Checklist
Read rules and scope list.
Clone repo and install dependencies.
Run baseline test suite.
Identify critical assets and roles.
List external integrations and oracles.
Create a threat model document.
Set a personal schedule for the contest.
Review previous audits or reports.

### 17.2 Day 1 Audit Checklist
Map contract architecture.
Identify entry points and access modifiers.
Trace token flows for mint and burn.
Mark privileged admin functions.
List upgradeable components.
Document contract ownership chains.

### 17.3 Day 2 Audit Checklist
Validate state transitions.
Review initialization and upgrade flows.
Check for reentrancy and external calls.
Scan for rounding and precision loss.
Start writing tests for invariants.
Review event emissions for logging gaps.

### 17.4 Day 3 Audit Checklist
Assess oracle usage and time dependencies.
Review permissions and role changes.
Inspect cross-contract interactions.
Test boundary values and overflows.
Draft preliminary report outlines.
Validate error handling and revert reasons.

### 17.5 Day 4 Audit Checklist
Review economic incentives and rewards.
Inspect fee calculations.
Check for griefing and denial-of-service paths.
Test emergency pause and recovery flows.
Validate input sanitization and restrictions.

### 17.6 Pre-Submission Checklist
Validate exploit steps are reproducible.
Confirm issue is in-scope.
Double-check severity and impact.
Ensure no internal duplicates.
Proofread report for clarity and brevity.
Verify line references and function names.

### 17.7 Escalation Checklist
Reference the specific rule or rubric clause.
Provide minimal reproduction steps.
Clarify why original judgment is incorrect.
Avoid emotional language.
Submit within the escalation window.
Include any new evidence succinctly.

### 17.8 Post-Contest Checklist
Read final report and compare to your findings.
Document what worked and what did not.
Update your personal playbook.
Reach out to peers for feedback.
Record payouts and time spent for ROI.

---

## 18. Glossary
Access Control: who can call privileged functions.
Accounting Bug: math error that misallocates assets.
Attack Surface: all external entry points.
Deduplication: grouping similar findings.
Escalation: appeal of a judgment decision.
Impact: the consequence of the exploit.
Invariant: property that should always hold.
LSJ: Lead Senior Judge.
Medium: severity class for substantial risk.
High: severity class for critical risk.
Watson: Sherlock auditor.
Sponsor: protocol team funding the contest.
PoC: proof of concept demonstrating exploit.
Scope: list of in-scope and out-of-scope targets.
Severity: classification of issue impact.
Triage: initial sorting and filtering.
Threat Model: attacker capabilities and assumptions.
Upgradeable Proxy: contract pattern allowing logic changes.
Reentrancy: external call that re-enters a function.
Oracle: external data source used by the protocol.
Slippage: price movement affecting trades.
Front-running: transaction ordering attack.
MEV: miner or validator extractable value.
Gas Optimization: change that reduces execution cost.
QA: quality assurance issues.
Sandbox: isolated testing environment.
Forked Chain: local copy of chain state for tests.
Time Lock: delay before privileged actions execute.
Timelock Bypass: exploit that skips delays.

---

## 19. Resource Map
Sherlock contest pages and rules.
Past Sherlock final reports.
Foundry and Hardhat documentation.
Slither and Aderyn static analysis tools.
Solidity security best practices.
OpenZeppelin contract standards.
Protocol docs and whitepapers.
Community writeups and postmortems.

---

## 20. Final Action Plan for New Watsons
Step 1: Choose a single upcoming contest.
Step 2: Read the rules, scope, and docs on day one.
Step 3: Build a threat model with assets and roles.
Step 4: Run static analysis and map the contract graph.
Step 5: Review critical asset flows and invariants.
Step 6: Draft PoCs for suspicious logic.
Step 7: Write concise reports with evidence and mitigations.
Step 8: Submit early enough to review for errors.
Step 9: Track judging outcomes and learn from the final report.
Step 10: Iterate on your playbook for the next contest.

---

## 21. Advanced Growth Path to $10K/Week
### 21.1 Skill Deepening
Specialize in a niche protocol domain.
Practice formal verification concepts.
Learn L2 and bridge security patterns.
Master economic attack modeling.

### 21.2 Process Optimization
Create reusable test harnesses.
Maintain a library of invariant tests.
Build checklists for common vulnerabilities.
Track contest stats and ROI per hour.

### 21.3 Reputation Compounding
Contribute thoughtful escalations.
Share writeups and learning notes.
Collaborate with high-quality teams.
Offer mentorship to newer Watsons.

### 21.4 Income Stack Strategy
Combine Sherlock contests with private audits.
Offer pre-contest review to protocol teams.
Maintain a recurring advisory client.
Use contest wins as marketing leverage.

### 21.5 Specialization Examples
Restaking and slashing mechanics.
Automated market makers and LP accounting.
Bridges and cross-chain message verification.
Governance and tokenomics.

---

## 22. Reality Check and Ethics
Contest hacking is competitive and demanding.
Always disclose responsibly and follow the rules.
Do not exploit vulnerabilities beyond PoC.
Protect your reputation and the ecosystem.
Ethical conduct increases long-term opportunity.

---

## 23. Quick Reference Summary
Sherlock is a judge-led Web3 audit contest platform.
Watsons submit vulnerabilities for prize pool shares.
Unique, high-impact findings drive earnings.
Senior Watsons can target $1K-$10K per week.
Judging quality and report clarity determine outcomes.
Use structured methodology and repeatable tooling.
Read final reports to accelerate your learning.

---

## 24. Appendix: Vulnerability Pattern Library
### 24.1 Access Control Patterns
Missing role checks on admin functions.
Upgradeable proxy initialized twice.
Privilege escalation via role transfer.
Admin-controlled oracle manipulation.
Owner-only function missing in upgrade path.
Role renounce leads to permanent lock.

### 24.2 Token Accounting Patterns
Incorrect share calculations in vaults.
Rounding errors on deposits and withdrawals.
Inflation of reward tokens via timing attack.
Fee miscalculation due to precision loss.
Balance updates after external call.
Incorrect fee-on-transfer token handling.

### 24.3 State Machine Patterns
State transition skipping in lockup systems.
Premature withdrawal before cooldown expiry.
Re-entrancy during state transitions.
Incorrect cancellation logic in auctions.
Double-claiming in reward states.
State reset without cleanup.

### 24.4 External Call Patterns
Unchecked return values from token transfers.
Reentrancy via ERC777 hooks.
Callback functions that can be abused.
Delegatecall to untrusted targets.
Call to zero address tokens.
Unsafe `call` with uncontrolled gas.

### 24.5 Oracle Patterns
Stale price usage.
Missing heartbeat checks.
Manipulable DEX spot prices.
Single-source oracle dependency.
Price scaling errors across decimals.
TWAP window too short for manipulation resistance.

### 24.6 Governance Patterns
Flash-loan voting manipulation.
Timelock bypass via delegatecall.
Emergency pause abuse.
Proposal execution order bugs.
Vote snapshot block mismatch.
Governance parameter change without delay.

### 24.7 Upgradeability Patterns
Unprotected upgrade functions.
Storage collision between implementations.
Initialization function callable post-deployment.
Beacon proxies pointing to malicious implementation.
Admin role stored in proxy storage incorrectly.

### 24.8 Economic Design Patterns
Incentives allow risk-free yield extraction.
Reward emission miscalculations.
Liquidity withdrawal breaks invariant ratios.
Slippage checks absent in swaps.
Fee distribution favors attacker accounts.

### 24.9 Cross-Chain Patterns
Message replay across chains.
Improper domain separation.
Bridge relayer trust assumptions.
Mismatch between token decimals on chains.
Nonce or sequence mismanagement.

---

## 25. Appendix: Example Finding Outline
Title: Oracle price can be manipulated to drain vault.
Impact: attacker can withdraw more assets than deposited.
Root Cause: price feed lacks TWAP or heartbeat check.
Exploit Steps:
1. Manipulate the DEX pool with a flash loan.
2. Call vault deposit or withdraw in the same block.
3. Capture inflated share calculation.
Mitigation: add a TWAP oracle and minimum delay.

---

## 26. Appendix: Escalation Template
Subject: Escalation for Report ID and Severity Review.
Summary: brief statement of why the severity is incorrect.
Evidence: line references and proof steps.
Impact: quantified loss or protocol disruption.
Rule Reference: quote the contest rubric.
Conclusion: request reconsideration.

---

## 27. Appendix: Q&A Question Bank
Is the admin allowed to pause withdrawals at any time?
Are privileged roles expected to be multisig-controlled?
Is the oracle assumed to be trusted or adversarial?
Can the owner change fee parameters without delay?
Are flash loans within the threat model?
Is the protocol expected to handle fee-on-transfer tokens?
Are there any off-chain keepers with special permissions?
Is the upgrade path expected to be immutable after launch?
Are tokens with non-standard decimals in scope?
Does the protocol rely on chain reorg assumptions?
Is the vault expected to support rebase tokens?
Are emergency withdrawals allowed to bypass cooldowns?
Is the protocol expected to run on a forked chain?
Are there planned integrations not in the repo?
Are any contracts intentionally immutable or locked?
Is the staking reward schedule subject to governance changes?
Are there constraints on block timestamp manipulation?
Is the sponsor assuming validators are honest?

---

## 28. Appendix: Metrics Tracker
Contests joined per quarter.
Hours spent per contest.
Findings submitted per contest.
Accepted findings per contest.
Duplicate rate percentage.
Invalid rate percentage.
Average payout per contest.
Median payout per contest.
Average payout per hour.
Severity mix across findings.
Escalation success rate.
Time from contest end to payout.
Skill gaps identified.
Tooling improvements shipped.

---

## 29. Appendix: 90-Day Ramp Plan
### Weeks 1-2: Fundamentals
Read Sherlock rules and past final reports.
Set up Foundry and a sample audit repo.
Learn standard vulnerability categories.
Practice writing two mock reports.

### Weeks 3-4: First Contest Exposure
Join a small contest with low pressure.
Focus on one module or contract set.
Submit at least one QA or low finding.
Review the final report and compare.

### Weeks 5-6: Medium Depth
Join a medium contest.
Build a full threat model before reading code.
Write at least two invariant tests.
Aim for one Medium-quality finding.

### Weeks 7-8: Process Refinement
Create a personal checklist.
Automate static analysis workflows.
Improve report templates for clarity.
Join a second contest with similar patterns.

### Weeks 9-10: Specialized Focus
Pick a niche such as AMMs or staking.
Study prior exploits in the niche.
Develop reusable PoC templates.
Target unique logic in the next contest.

### Weeks 11-12: Senior Readiness
Join a larger contest with stronger competition.
Allocate time for deep PoCs and mitigations.
Attempt at least one High-impact path.
Review outcomes and plan next quarter.

---

## 30. FAQ
Q: Do I need to be a Solidity expert to start?
A: You need core proficiency, but contests accelerate learning.

Q: Can I join contests as a beginner?
A: Yes, but start with smaller scopes and focus on QA findings.

Q: How many contests should I do per month?
A: One to two is common; more requires high stamina.

Q: Are teams allowed?
A: Yes, teams submit under a single Watson handle.

Q: Do I have to submit a PoC?
A: A PoC is strongly recommended and often required for acceptance.

Q: How do duplicates affect payout?
A: Duplicates split the reward equally within the group.

Q: Can I escalate a severity decision?
A: Yes, within the escalation window and with evidence.

Q: Are payouts always in stablecoins?
A: Usually, but check contest rules for specifics.

Q: What if I find something out of scope?
A: It will be invalid, so confirm scope before reporting.

Q: How do I track my performance?
A: Keep a spreadsheet of time spent, payouts, and outcomes.

---

## 31. Closing Note
Sherlock rewards depth, clarity, and disciplined execution.
Build a repeatable audit system and iterate every contest.
Focus on unique bugs, clean PoCs, and professional reports.
Consistency and learning compound toward $10K/week outcomes.
