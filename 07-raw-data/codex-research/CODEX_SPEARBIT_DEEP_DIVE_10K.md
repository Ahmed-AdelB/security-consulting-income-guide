# SPEARBIT Web3 Security Audits: Deep Dive Guide (K-10K/week)

Version: 1.0
Last updated: 2025-02-14
Audience: auditors, security researchers, protocol teams, and security leads
Scope: SPEARBIT audit delivery model, Lead Security Researcher program, and auditor success patterns
Disclaimer: This is an independent guide based on common industry practices and anonymized patterns
Disclaimer: It is not an official SPEARBIT publication and should be verified with current program details

## How to use this guide

- Read the platform overview to understand SPEARBIT’s audit model
- Use the Lead Security Researcher section to map the leadership track
- Review earning potential to understand variability and tradeoffs
- Follow the audit process section as a field guide during engagements
- Study the guild structure section for collaboration and role clarity
- Treat the vetting requirements section as a prep checklist
- Apply the success strategies section for day-to-day execution
- Use the comparisons to choose between SPEARBIT, Code4rena, or Sherlock
- Learn from real auditor experience composites for practical insight
- Use the appendices for templates, checklists, and routines

## Table of contents

- Platform overview
- Operating model and value proposition
- Typical engagement types
- Audit deliverables and artifacts
- Lead Security Researcher (LSR) program
- LSR responsibilities
- LSR growth path
- LSR economics and incentives
- Earning potential (K-10K/week)
- Rate structures and pay mechanics
- Variability and risk factors
- Audit process end-to-end
- Pre-engagement and intake
- Threat modeling and design review
- Manual review and tool-assisted review
- Reporting and remediation
- Post-audit follow-up
- Guild structure and collaboration
- Roles within a guild
- How guilds are staffed
- Vetting requirements and selection
- Application materials
- Technical screening
- Trial audits and writeups
- Success strategies
- Skill development
- Communication and leadership
- Time management and delivery
- Quality bar and QA expectations
- Comparison with Code4rena and Sherlock
- Engagement model comparison
- Pay model comparison
- Workflow and deliverable comparison
- Real auditor experiences (composite)
- Common challenges and solutions
- Frequently asked questions
- Glossary
- Appendices and templates

## Platform overview

SPEARBIT operates as a curated Web3 security collective.
The platform connects protocol teams with vetted auditors and specialized guilds.
Unlike contest platforms, audits are staffed with known contributors.
Engagements are scoped and staffed for depth and accountability.
SPEARBIT emphasizes senior reviewer oversight and consistent reporting.
Clients often use SPEARBIT for high-stakes protocol launches.
The model blends boutique security firm rigor with distributed talent.
Auditors are selected based on fit, availability, and domain expertise.
Guilds provide a structure for scale without sacrificing quality.
The platform focuses on long-term relationships and repeat clients.

### Operating model and value proposition

- Curated talent reduces time-to-start for clients
- Guilds enable specialized coverage and flexible staffing
- Lead Security Researchers coordinate end-to-end quality
- Audits are scoped to deliver deterministic outcomes, not contest lotteries
- Process emphasizes proactive risk discovery and remediation support
- Repeat engagements allow deeper system knowledge and faster turnaround
- Community-level knowledge sharing improves review depth
- Central coordination streamlines contracts and payments
- Brand reputation depends on consistent, high-severity find rate
- Post-audit support is often integrated into engagement planning

### Typical engagement types

- Core protocol audits before mainnet deployment
- Major upgrades or contract migrations
- Cross-chain bridge or messaging subsystem reviews
- Token launch or tokenomics contract checks
- Staking or restaking module assessments
- Oracle integration audits and price feed validation
- Governance module and timelock analysis
- Security design reviews and threat modeling sessions
- Incident response and post-mortem reviews
- Retainer-style security coverage for fast-moving teams

### Audit deliverables and artifacts

- Scoping document with in-scope and out-of-scope components
- Threat model covering trust assumptions and attacker profiles
- Audit plan with milestones and reporting cadence
- Findings report with severity, impact, and exploit narrative
- Proof-of-concept notes or minimal exploit steps
- Remediation guidance and patch verification notes
- Final report with risk summary and status of fixes
- Optional presentation to protocol team or community
- Internal QA checklist and reviewer sign-off
- Optional follow-up verification report

### Stakeholder map

- Protocol teams responsible for architecture and implementation
- SPEARBIT operations coordinating logistics and contracts
- Lead Security Researchers managing the audit
- Guild contributors providing deep review coverage
- QA reviewers ensuring consistency and severity correctness
- Client stakeholders consuming risk outputs
- Community or governance stakeholders reviewing public reports

## Lead Security Researcher (LSR) program

The LSR program is SPEARBIT’s leadership track for audit leads.
LSRs drive audit quality, coordination, and client communication.
The role blends technical depth with delivery accountability.
LSRs are expected to model top-tier audit hygiene.
The program emphasizes consistency, mentorship, and stakeholder trust.

### LSR responsibilities

- Lead scoping and confirm audit objectives with clients
- Build and staff the audit guild with the right skill mix
- Define the audit plan, milestones, and review cadence
- Set expectations for issue submission and evidence quality
- Ensure coverage across critical contracts and integrations
- Coordinate daily standups or asynchronous updates
- Review and triage findings from contributors
- Write or approve the final report
- Manage communication during remediation and re-review
- Protect the client timeline by minimizing coordination friction

### LSR growth path

- Start as a contributor on a guild audit
- Demonstrate strong finding quality and documentation
- Support an audit lead as a shadow or deputy
- Lead a smaller scoped audit with oversight
- Lead complex audits with multi-guild coordination
- Mentor newer auditors and maintain consistent delivery quality

### LSR economics and incentives

- LSRs typically receive a lead premium for management overhead
- Lead roles may include revenue share based on project value
- Long-term relationships can lead to retainer-based engagements
- Some audits include bonuses for fast turnaround or low churn
- Reputation compounds, leading to higher utilization and priority staffing

### LSR success metrics

- Severity accuracy and lack of reclassification disputes
- Client satisfaction and repeat engagement rate
- On-time delivery against a scoped schedule
- Coverage completeness and clean QA outcomes
- Low rate of missed critical issues in production

## Earning potential (K-10K/week)

SPEARBIT auditor earnings are highly variable and performance-driven.
Top contributors and LSRs can reach K-10K per week in strong periods.
Entry contributors may earn less while building proof of capability.
Rates depend on experience, availability, and specialization.
Work volume can fluctuate with market conditions and protocol demand.
Earnings may be tied to project fees or hourly equivalents.
Some auditors operate part-time with proportionally reduced earnings.

### Rate structures and pay mechanics

- Fixed-fee engagements split among guild contributors
- Lead premiums for coordination and report ownership
- Retainer agreements for ongoing protocol coverage
- Optional bonus structures tied to delivery speed
- Payment schedules aligned to milestones or final delivery
- Some work may be paid in fiat, stablecoins, or token-based incentives

### Variability and risk factors

- Seasonal market cycles affect audit demand
- New protocol launches create spikes in workload
- Team availability and overlapping audits impact utilization
- Specialization in niche domains can command higher rates
- Time spent on research and mentorship is often unpaid
- Reputation and referral pipeline significantly affect stability

### Earnings scenarios (illustrative, not guarantees)

- Scenario A: part-time contributor, 10-15 hours per week, low-mid 4 figures
- Scenario B: full-time senior auditor, 35-45 hours, mid 4 to low 5 figures
- Scenario C: LSR on complex audit, 50+ hours, high 4 to low 5 figures
- Scenario D: multiple retainer clients, mixed weeks, high variability

## Audit process end-to-end

SPEARBIT audits are structured, collaborative, and documentation-heavy.
The process prioritizes upfront clarity to avoid surprises mid-audit.
Each phase is designed to reduce false negatives and improve prioritization.

### Pre-engagement and intake

- Client submits scope, architecture docs, and code repositories
- LSR clarifies objectives, timeline, and constraints
- In-scope contracts and dependencies are enumerated
- External services and oracles are identified early
- Prior audits or known issues are collected for context
- Threat assumptions and trust boundaries are defined
- Budget and staffing range is confirmed with ops

### Scoping and staffing

- LSR maps domain expertise to required audit coverage
- Guild members are selected based on experience and availability
- Roles are assigned for core contracts, tooling, and QA
- Audit timeline is finalized with kickoff milestone
- Communication channels and reporting tools are established

### Kickoff and environment setup

- Kickoff call aligns on goals and key risks
- Repository access and tooling permissions are verified
- Build instructions and test harnesses are validated
- Deployments or forks are prepared for testing
- A shared notes repository is created
- Severity rubric and reporting format are confirmed

### Threat modeling and design review

- Document system invariants and critical value flows
- Identify privileged roles and admin boundaries
- Define attacker capabilities and realistic threat actors
- Identify trusted off-chain components and their assumptions
- Enumerate integration risks with third-party protocols
- Produce a high-level risk map to guide review

### Manual review and tool-assisted review

- Review core contracts and high-value functions first
- Trace privilege paths and role transitions
- Review initialization, upgradeability, and storage layout
- Analyze math operations, rounding, and precision loss
- Review access control modifiers and role assignment flows
- Inspect external calls and reentrancy patterns
- Model state transitions and edge cases
- Validate event emission against external dependencies
- Use static analyzers for basic issue discovery
- Use custom scripts to model invariants
- Use fuzzing for key entry points where feasible

### Internal review cadence

- Daily notes sync to share findings and hypotheses
- Mid-audit checkpoint with client for early feedback
- Review of preliminary issues by LSR or QA
- Consolidate duplicates and confirm exploitability

### Reporting and remediation

- Draft report includes severity, impact, and remediation steps
- Issues are categorized as critical, high, medium, low, or informational
- LSR confirms severity and evidence quality
- Client receives interim report for remediation iteration
- Fixes are reviewed and verified by auditors
- Final report includes resolved and unresolved findings

### Post-audit follow-up

- Optional verification report for patched issues
- Post-mortem to refine audit approach and tooling
- Lessons learned shared with guild members
- Client feedback captured for process improvement

## Guild structure and collaboration

Guilds are curated groups of auditors aligned by skill and availability.
They provide a modular staffing approach for audits of varying complexity.
Guilds can be persistent or assembled for a specific engagement.

### Roles within a guild

- Lead Security Researcher
- Deputy lead or shadow lead
- Senior auditor for core logic
- Specialist for cryptography or math-heavy modules
- Tooling lead for fuzzing or formal methods
- QA reviewer for severity alignment
- Documentation coordinator for report editing

### How guilds are staffed

- LSR requests contributors through SPEARBIT operations
- Availability is matched to audit timeline
- Expertise is matched to domain and language
- Past collaboration quality is considered
- Balance is maintained between senior and mid-level auditors

### Collaboration practices

- Shared notes with consistent structure and naming
- Daily async updates with findings and progress
- Short sync calls at critical checkpoints
- Internal review of each finding before client submission
- Clear ownership of modules to avoid coverage gaps

### Communication norms

- Use structured templates for issue reports
- Maintain a single source of truth for findings
- Separate speculation from confirmed vulnerabilities
- Escalate critical findings immediately
- Keep client informed of high-level progress

## Vetting requirements and selection

SPEARBIT emphasizes a high bar for technical competency and clarity.
Selection prioritizes proven audit capability and professional communication.
Applicants are expected to show strong fundamentals and reliable execution.

### Application materials

- Security-focused resume or profile
- Prior audit reports or public findings
- GitHub repositories demonstrating Solidity or Rust expertise
- Writeups demonstrating clear reasoning and remediation guidance
- References from known auditors or clients when available

### Technical screening

- Deep knowledge of Solidity and EVM semantics
- Understanding of common DeFi and Web3 architectures
- Ability to reason about invariant preservation
- Familiarity with upgradeability and proxy patterns
- Knowledge of access control and role-based design
- Evidence of secure coding and review experience

### Trial audits and writeups

- Candidates may be asked to review a sample codebase
- Findings must include impact and exploit narrative
- Deductions for duplicated or low-signal findings
- Strong emphasis on reproduction and evidence quality
- Clear remediation guidance is required

### Soft skills expectations

- Respectful and precise communication
- Reliable delivery within agreed deadlines
- Ability to collaborate across time zones
- Openness to feedback and severity re-evaluation
- Consistent documentation habits

## Success strategies

Success at SPEARBIT combines technical depth and delivery discipline.
Auditors who develop repeatable routines outperform those who improvise.
The following strategies have proven effective across many audits.

### Skill development strategies

- Master Solidity memory, storage, and calldata behavior
- Build mental models for common DeFi primitives
- Study bridge architectures and cross-chain messaging patterns
- Learn typical oracle designs and data freshness risks
- Practice writing attack flows and PoCs
- Read prior audit reports to learn issue framing
- Keep a personal library of exploit patterns
- Track ecosystem incidents and post-mortems

### Communication and documentation

- Write issues as if the developer is under time pressure
- Use short titles that capture impact and vector
- Provide steps to reproduce or a minimal exploit narrative
- Separate facts from assumptions
- Keep internal notes tidy to ease report compilation
- Ask precise questions when design intent is unclear

### Time management and delivery

- Start with threat modeling to avoid blind spots
- Block time for deep review without distractions
- Schedule a mid-audit refresh to revisit initial assumptions
- Review critical modules twice with different lenses
- Reserve time for report polishing and QA responses
- Avoid overcommitting to parallel audits

### Quality bar and QA expectations

- Confirm each issue has a clear impact statement
- Verify that issues are distinct and not duplicates
- Ensure that severity aligns with risk and likelihood
- Provide remediation that is feasible within context
- Validate that findings reference the correct functions and lines
- Track unresolved questions before report finalization

### Personal execution playbook

- Create a per-audit notebook with sections for each module
- Track open hypotheses and verify them before reporting
- Use version control diff tools to monitor changes
- Keep a list of invariants to revisit during review
- Record assumptions for external dependencies
- Maintain a buffer day for re-checking fixes

## Comparison with Code4rena and Sherlock

This section compares SPEARBIT with contest-based audit platforms.
The comparison focuses on process, economics, and deliverable quality.
Actual terms vary by engagement and should be verified with each platform.

### Engagement model comparison

| Dimension | SPEARBIT | Code4rena | Sherlock |
| --- | --- | --- | --- |
| Staffing | Curated guild | Open contest | Open contest with judges |
| Accountability | Lead-driven | Competitive | Competitive |
| Timeline control | High | Medium | Medium |
| Client involvement | High-touch | Limited | Limited |
| Repeat context | High | Low | Low |
| Report ownership | Lead team | Platform | Platform |

### Pay model comparison

| Dimension | SPEARBIT | Code4rena | Sherlock |
| --- | --- | --- | --- |
| Pay basis | Fixed fee | Prize pool | Prize pool |
| Predictability | Higher | Lower | Lower |
| Lead premium | Yes | No | No |
| Retainers | Common | Rare | Rare |
| Risk of zero pay | Low | Medium | Medium |

### Workflow and deliverable comparison

- SPEARBIT provides a single, consolidated report per engagement
- Contest platforms generate a ranked set of findings after judging
- SPEARBIT emphasizes proactive communication with the client
- Contest platforms emphasize competitive discovery and judge arbitration
- SPEARBIT provides clearer ownership for remediation and verification
- Contest platforms provide broader eyeballs but less coordination

### When SPEARBIT is a better fit

- The protocol needs high-touch collaboration and confidentiality
- The system is complex and requires domain specialists
- The client wants a consistent, single-source report
- There is a need for retainer-based follow-up
- Launch schedules require reliable delivery dates

### When a contest platform can be a better fit

- The protocol benefits from many independent reviewers
- The team wants cost flexibility via prize pools
- The scope is large but can be parallelized
- The team can tolerate variability in timelines

## Real auditor experiences (composite)

The following experiences are composites drawn from common patterns.
They are anonymized and represent typical journeys and challenges.
They are not endorsements or statements from specific individuals.

### Composite experience A: junior auditor to reliable contributor

- Joined after two public contest wins and a strong portfolio
- First audit focused on a small staking module
- Received feedback on report clarity and severity calibration
- Built a habit of writing detailed exploit narratives
- After four audits, invited to take on more complex modules
- Earnings stabilized after consistent participation

### Composite experience B: part-time specialist

- Maintains a full-time engineering role outside Web3
- Participates in short audits focused on oracle integrations
- Chooses projects with short timelines and clear scope
- Uses a dedicated checklist to stay efficient
- Earns supplemental income with limited weekly hours

### Composite experience C: niche cryptography specialist

- Focuses on protocols with cryptographic primitives
- Often reviews zero-knowledge proof integrations
- Work is sporadic but high-impact
- Maintains close collaboration with LSRs for scope planning
- Receives higher rates for specialized coverage

### Composite experience D: Lead Security Researcher

- Began as a high-signal contributor in DeFi audits
- Developed a consistent report format and clear communication style
- Transitioned to shadow lead on a mid-sized audit
- Led a multi-guild audit with heavy protocol complexity
- Earns leadership premium and priority staffing

### Common challenges and solutions

- Challenge: unclear design intent
- Solution: schedule an early design review call
- Challenge: duplicate findings across auditors
- Solution: centralize notes and assign modules clearly
- Challenge: severity disputes
- Solution: document impact, likelihood, and assumptions explicitly
- Challenge: scope creep late in the audit
- Solution: require explicit scope change approval
- Challenge: remediation delays
- Solution: create a prioritized fix list and follow-up cadence

## Frequently asked questions

### What makes SPEARBIT different from a traditional audit firm

SPEARBIT uses a guild model with curated independent auditors.
This allows rapid assembly of experts while maintaining consistency.

### Is the LSR role purely managerial

No, LSRs are expected to contribute technically and lead by example.
They review core modules and handle report quality control.

### How long do audits typically last

Timelines vary with scope, but many audits run one to four weeks.
High-complexity protocols can require longer timelines.

### Can auditors work remotely from any region

Yes, participation is typically remote and globally distributed.
Time zone overlap helps but is not always required.

### What languages are most common

Solidity dominates, but Rust and Move are increasingly relevant.
Some audits involve JavaScript, Go, or backend components.

### Are results public

Many clients publish reports, but publication is optional.
Confidential audits are common for pre-launch systems.

## Glossary

- Audit: structured review of code and architecture for vulnerabilities
- Guild: curated group of auditors assigned to an engagement
- LSR: Lead Security Researcher responsible for audit delivery
- Severity: classification of risk impact and likelihood
- Invariant: property of a system that should always hold
- Threat model: attacker assumptions and system boundaries
- PoC: proof of concept demonstrating exploitability
- Retainer: ongoing agreement for periodic security reviews
- Scope: defined set of contracts and components to review
- QA: quality assurance review of findings and reporting
- Triage: process of validating and categorizing findings
- Upgradeability: ability to modify contract logic via proxies
- Oracle: external data source for on-chain pricing or signals
- MEV: maximal extractable value considerations
- Governance: contract-based decision-making system
- Timelock: delay mechanism for privileged actions
- Multisig: multi-signature authorization control
- Lens: conceptual perspective used in review (auth, math, integration)

## Appendix A: Example weekly plan for auditors

- Monday: scope review and threat modeling
- Tuesday: core contract review and function tracing
- Wednesday: secondary modules and integration analysis
- Thursday: tooling pass, invariant checks, and fuzzing
- Friday: compile findings, severity alignment, and report draft
- Saturday: fix verification and QA responses
- Sunday: rest or buffer for unplanned changes

## Appendix B: Audit note template

- Contract name:
- Module purpose:
- External dependencies:
- Privileged roles:
- Critical invariants:
- Entry points:
- External calls:
- Potential attack paths:
- Notes and questions:
- Findings draft:

## Appendix C: Client kickoff checklist

- Confirm repository access
- Confirm build and test instructions
- Identify deployment configuration
- Clarify scope boundaries
- Confirm threat assumptions
- Share prior audit reports
- Identify third-party dependencies
- Establish communication channels
- Confirm reporting format
- Schedule midpoint sync

## Appendix D: Severity calibration checklist

- Does the issue enable loss of funds or protocol insolvency
- Is there a realistic attacker with required permissions
- Can the issue be exploited with a single transaction
- Does the issue require admin compromise
- Is the impact limited to a subset of users
- Is the exploit contingent on market manipulation
- Does the issue violate a core invariant
- Is there an on-chain mitigation or circuit breaker
- Is the exploit detectable and reversible
- What is the likely time-to-exploit

## Appendix E: 100-point audit checklist

1. Map all entry points and public functions
2. Identify privileged roles and admin keys
3. Validate initialization and constructor logic
4. Confirm upgradeability patterns and storage layout
5. Check for unprotected upgrade functions
6. Verify access control modifiers on critical functions
7. Ensure role changes emit events
8. Inspect external calls for reentrancy risk
9. Verify reentrancy guards are correctly placed
10. Check for reentrancy on callbacks and hooks
11. Review math operations for overflow and underflow
12. Review rounding and precision in accounting
13. Inspect fee calculations for precision loss
14. Validate token decimal assumptions
15. Inspect price oracle feeds for staleness
16. Confirm price sanity checks and fallback logic
17. Inspect liquidation logic for edge cases
18. Validate collateralization thresholds
19. Review interest accrual and time-based logic
20. Confirm timestamp usage is safe and bounded
21. Review block number usage for predictability
22. Validate signature verification and replay protection
23. Check EIP-712 domain separator usage
24. Confirm nonces are incremented consistently
25. Verify permit usage and allowance revocation
26. Inspect token transfer return value handling
27. Confirm ERC20 compatibility assumptions
28. Inspect ERC721 or ERC1155 transfers for hooks
29. Check for approval race conditions
30. Validate treasury or fee recipient addresses
31. Review governance proposal execution flow
32. Validate timelock parameters and delays
33. Confirm emergency pause mechanisms
34. Verify pause controls are properly authorized
35. Check for denial-of-service via unbounded loops
36. Inspect iteration over dynamic arrays
37. Validate array length assumptions
38. Confirm storage packing does not break upgrades
39. Check for storage collision in proxy contracts
40. Validate fallback and receive functions
41. Review event emission for key state changes
42. Confirm critical events are not missing
43. Inspect error handling and revert reasons
44. Verify require statements cover all invariants
45. Test boundary values for inputs
46. Check for off-by-one errors in ranges
47. Inspect use of unchecked blocks
48. Validate internal accounting invariants
49. Verify accounting symmetry for deposits and withdrawals
50. Inspect fee-on-transfer token handling
51. Check for assumptions about token balance changes
52. Review external protocol integrations
53. Validate slippage parameters and bounds
54. Inspect rate limits and cooldowns
55. Confirm external call return value handling
56. Inspect try-catch usage for external calls
57. Validate access control on admin setters
58. Confirm immutable variables are safe and correct
59. Review use of delegatecall and low-level calls
60. Inspect for arbitrary call execution risks
61. Validate signature malleability protections
62. Inspect for misuse of tx.origin
63. Review use of block.timestamp for critical logic
64. Confirm randomness is not derived from block data
65. Validate that mint and burn are controlled
66. Check supply caps and emission constraints
67. Inspect staking reward calculations
68. Confirm reward distribution fairness
69. Review vesting schedules for correctness
70. Inspect cliff and linear release logic
71. Validate rounding behavior on reward claims
72. Confirm accounting of unclaimed rewards
73. Inspect withdrawal queue mechanics
74. Validate order matching or auction logic
75. Check for front-running vulnerabilities
76. Review sandwich attack resistance
77. Confirm slippage protection can not be bypassed
78. Inspect cross-chain message verification
79. Validate message ordering assumptions
80. Check replay protection across chains
81. Review guardian or relayer permissions
82. Validate configuration changes are logged
83. Check upgrade delay enforcement
84. Confirm admin role rotation mechanisms
85. Review gas griefing vectors
86. Inspect refund or rebate mechanisms
87. Validate fee distribution correctness
88. Review handling of zero addresses
89. Check for non-standard ERC20 behavior
90. Validate allowance reductions for safety
91. Inspect for unintended self-destruct or suicide
92. Review ownership transfer flows
93. Validate that critical setters are bounded
94. Inspect arithmetic in rate or index updates
95. Check for oracle price manipulation resilience
96. Review use of chainlink or TWAP sources
97. Inspect state cleanup and pruning logic
98. Validate migration scripts and upgrade steps
99. Review contract-level invariants post-upgrade
100. Confirm test coverage for highest-risk paths

## Appendix F: Report structure template

- Executive summary
- Scope and methodology
- System overview
- Key risks and threat assumptions
- Findings summary table
- Detailed findings
- Remediation status
- Appendix with tools and references

## Appendix G: Daily audit checklist

- Review open questions and unresolved hypotheses
- Update shared notes with new findings
- Sync with LSR or QA on severity alignment
- Verify any fixes delivered by the client
- Re-check high-risk modules for missed paths
- Record new assumptions or integration risks

## Appendix H: Sample issue writeup template

- Title
- Severity
- Impact
- Likelihood
- Description
- Steps to reproduce
- Proof of concept
- Remediation guidance
- References

## Appendix I: Success metrics tracker

- Number of confirmed findings per audit
- Ratio of unique to duplicate findings
- Report acceptance time by client
- Average time to verify fixes
- Client satisfaction feedback

