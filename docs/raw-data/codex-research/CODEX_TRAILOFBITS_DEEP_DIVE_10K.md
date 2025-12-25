# Trail of Bits Web3 Audit Deep Dive

Version: 1.0
Audience: founders, protocol leads, engineering managers, auditors
Scope: comprehensive overview of a Web3 audit program
Perspective: Trail of Bits style, research-driven, adversarial
Length target: 400+ lines

## Table of Contents

- Executive summary
- Core audit methodology
- Engagement lifecycle
- Threat modeling and assumptions
- Architecture and dependency review
- Code review practices
- Dynamic analysis and fuzzing
- Formal verification and specifications
- Economic and game-theoretic review
- Cryptography and key management
- Infrastructure and operational security
- Reporting standards and deliverables
- Remediation and retest workflow
- Quality assurance and metrics
- Team structure and staffing model
- Role definitions and responsibilities
- Research focus and knowledge areas
- Client types and engagement patterns
- Career paths and progression ladders
- Training, mentorship, and culture
- Communication templates and rituals
- Sample audit timelines
- Artifact catalog
- Glossary
- Appendix: checklist compendium

## Executive Summary

Trail of Bits applies a research-first, adversarial security mindset to Web3 audits.
Audits are structured as phased engagements with measurable milestones.
The methodology blends static analysis, dynamic testing, and formal methods.
The team focuses on smart contracts, protocol design, and off-chain components.
Audit results emphasize actionable risk reduction and long-term resilience.
Client education and collaborative remediation are core to the process.
Deep ecosystem expertise drives higher coverage and better threat modeling.

## Core Audit Methodology

### Guiding Principles

- Assume active, intelligent adversaries.
- Validate security properties against explicit specifications.
- Prefer root-cause fixes over mitigations.
- Combine automated and manual analysis for depth and breadth.
- Treat economic exploits as first-class security issues.
- Track risk to user funds, system liveness, and governance integrity.
- Communicate findings with clear reproduction and impact analysis.
- Avoid false confidence; highlight uncertainty and unknowns.
- Encourage secure-by-design architecture rather than patching.
- Build reusable knowledge across audits through research.

### Phase Overview

- Phase 0: Intake and scoping
- Phase 1: Architecture understanding
- Phase 2: Threat modeling
- Phase 3: Code review and static analysis
- Phase 4: Dynamic analysis and fuzzing
- Phase 5: Formal verification and specification checks
- Phase 6: Economic analysis and simulation
- Phase 7: Report drafting and review
- Phase 8: Remediation support
- Phase 9: Retest and closure

### Audit Questions

- What can go wrong given adversarial incentives?
- What invariants must always hold?
- Which modules are most security-critical?
- Where is trust placed, and is it justified?
- What dependencies can fail or be upgraded maliciously?
- How does governance affect safety guarantees?
- What assumptions are implicit and must be documented?
- Are mitigations robust across chain conditions?
- How do off-chain systems influence on-chain risk?

## Engagement Lifecycle

### Intake and Scoping

- Collect high-level protocol description and goals.
- Identify supported chains and deployment environments.
- Enumerate repositories, commit hashes, and branches.
- Confirm feature freeze and review window.
- Define in-scope and out-of-scope components.
- Confirm expected deliverables and timelines.
- Establish communication channels and escalation paths.
- Gather previous audits and open issues.
- Identify operational constraints for testing.
- Align on severity taxonomy and reporting style.

### Kickoff and Access

- Schedule kickoff call with engineering and product leads.
- Provide access to private repos and CI pipelines.
- Gather deployment configuration and environment variables.
- Obtain architecture diagrams and system specs.
- Identify core team contacts for rapid questions.
- Confirm tooling requirements and test networks.
- Establish a shared issue tracker for findings.

### Discovery and Context Building

- Build a protocol map of contracts and dependencies.
- Enumerate on-chain state flows and permissions.
- Review upgradeability patterns and admin roles.
- Identify token economics and stakeholder incentives.
- Trace privileged actions and pause mechanisms.
- Capture deployment boundaries across chains.
- Document integration points and oracles.
- Validate assumptions with the engineering team.

### Reporting and Wrap-up

- Draft findings with reproduction steps.
- Validate exploit scenarios with stakeholders.
- Assign severity and impact categories.
- Provide remediation recommendations.
- Conduct a close-out meeting with the client.
- Capture lessons learned for future engagements.
- Offer follow-up support or retest window.

## Threat Modeling and Assumptions

### Threat Modeling Inputs

- Publicly accessible contracts and APIs.
- Governance and admin key custody models.
- Economic incentives for arbitrage and MEV.
- Cross-chain dependencies and bridging mechanisms.
- Off-chain data feeds and oracle providers.
- Integration with third-party protocols.

### Threat Modeling Outputs

- Attack surface map for critical flows.
- List of high-value assets and invariants.
- Trust boundaries and privilege hierarchy.
- Known limitations and residual risks.
- Candidate abuse cases for testing.

### Assumption Catalog

- Admin keys are held in secure multisigs.
- Oracles deliver timely and accurate data.
- L2 sequencers follow expected behavior.
- Validators maintain honest majority.
- Upgrades are governed by time locks.
- Off-chain keepers remain online.
- Users transact with recommended frontends.
- Chain reorgs remain within expected limits.
- Dependencies follow semantic versioning.

## Architecture and Dependency Review

### Architecture Checklist

- Identify module boundaries and responsibilities.
- Track data flow between contracts and off-chain services.
- Confirm initialization order and ownership assignment.
- Review upgradeability mechanism and storage layout.
- Validate access control patterns and modifiers.
- Inspect role management and permission delegation.
- Confirm pause and emergency controls are reachable.
- Map governance execution paths and delays.
- Evaluate upgrade admin threat exposure.
- Document dependency tree and version constraints.
- Review external calls and reentrancy boundaries.
- Analyze internal accounting models.
- Check inter-contract message passing.
- Assess configuration at deployment time.
- Review hidden backdoors and privileged hooks.

### Dependency Checklist

- Review ERC standards and custom extensions.
- Confirm safe usage of libraries and math utilities.
- Audit third-party contracts for known issues.
- Validate oracle contracts and fallback logic.
- Check bridging libraries and message verification.
- Inspect token wrappers and adapter patterns.
- Evaluate proxy implementations and admin separation.
- Confirm safety of low-level calls.
- Assess upgrade governance for dependencies.
- Identify transitive dependencies and risk aggregation.

## Code Review Practices

### Static Review Approach

- Begin with most critical contracts.
- Trace value flows and state transitions.
- Identify privileged methods and external calls.
- Evaluate reentrancy guards and checks-effects.
- Review precision, rounding, and overflow handling.
- Confirm correct handling of ERC-20 return values.
- Inspect event emissions for auditability.
- Verify on-chain accounting invariants.
- Check custom errors and revert paths.
- Evaluate fail-open versus fail-closed behavior.

### Manual Review Heuristics

- Compare intended design with actual code.
- Search for implicit assumptions and TODOs.
- Check for duplicated logic and divergence.
- Validate time-dependent logic for edge cases.
- Inspect trust assumptions around admin roles.
- Analyze batching and multi-call semantics.
- Review upgrade migration functions.
- Validate emission schedules and rate limits.
- Check pausing logic for system recovery.
- Ensure correct token decimal conversions.

### Static Analysis Tools

- Slither for linting and detectors.
- Semgrep rules tuned to Web3 patterns.
- Mythril for symbolic execution.
- Custom scripts for invariant checking.
- EVM disassembly for low-level patterns.
- Foundry static tools for coverage hints.

## Dynamic Analysis and Fuzzing

### Dynamic Testing Goals

- Exercise state transitions under adversarial inputs.
- Validate invariants under random sequences.
- Discover state corruption and accounting drift.
- Identify denial-of-service conditions.
- Evaluate gas exhaustion and block limits.
- Simulate oracle anomalies and stale data.
- Test reentrancy under complex call graphs.

### Fuzzing Workflow

- Define invariants in property-based frameworks.
- Build stateful fuzzers with protocol actions.
- Seed with known edge cases.
- Use differential testing against reference models.
- Track minimal counterexamples for reproduction.
- Validate invariant coverage metrics.
- Triage and prioritize failing cases.

### Dynamic Tooling

- Foundry for invariant and fuzz tests.
- Echidna for property-based fuzzing.
- Hardhat and Tenderly for traces.
- Anvil or Ganache for local chains.
- Custom harnesses for cross-chain testing.

## Formal Verification and Specifications

### Specification Strategy

- Define critical invariants for each module.
- Formalize assumptions about external systems.
- Convert business rules into assertions.
- Use state machine models for complex flows.
- Prioritize safety-critical paths for proofs.

### Verification Techniques

- SMT-based checks for arithmetic safety.
- Model checking for state transitions.
- Symbolic execution for path exploration.
- Proof scripts for cryptographic protocols.
- Manual proof review for critical invariants.

### Formal Methods Tooling

- Certora Prover for contract properties.
- Scribble annotations for runtime checks.
- K framework for EVM semantics.
- Coq or Isabelle for advanced proofs.
- Securify for pattern analysis.

## Economic and Game-Theoretic Review

### Economic Risk Areas

- MEV extraction and sandwich risk.
- Oracle manipulation and price impact.
- Liquidity assumptions and slippage.
- Governance attack incentives.
- Flash loan amplification.
- Reward farming and incentive abuse.
- Fee model manipulation.
- Liquidation and collateral volatility.
- Cross-chain arbitrage and sync gaps.

### Analysis Techniques

- Simulate market conditions with stress scenarios.
- Evaluate incentive compatibility of roles.
- Model profit functions for adversaries.
- Assess griefing vectors and denial incentives.
- Estimate economic security budgets.
- Review liquidation parameters and stability fees.
- Test keeper incentives for liveness.

## Cryptography and Key Management

### Cryptographic Review Checklist

- Verify signature schemes and domain separation.
- Confirm nonce handling and replay protection.
- Review hash usage for collisions and preimages.
- Check randomness sources and entropy.
- Validate threshold and multi-sig logic.
- Ensure secure key rotation patterns.
- Review key storage and access control.
- Validate time locks and timelock controls.

### Key Management Considerations

- Multisig quorum requirements.
- Hardware security module integration.
- Emergency key revocation.
- Audit logging for key use.
- Backup and recovery procedures.
- Separation of duties across teams.

## Infrastructure and Operational Security

### Off-Chain Components

- Backend services and API endpoints.
- Indexers and data pipelines.
- Keeper bots and automation scripts.
- Frontend interactions and signing flows.
- Monitoring and alerting systems.

### Operational Checklist

- Review deployment pipelines and approvals.
- Validate environment variable handling.
- Inspect secrets management and vault usage.
- Confirm rate limiting and abuse controls.
- Analyze logging for sensitive data leakage.
- Check for supply chain risks in dependencies.
- Ensure rollback and disaster recovery plans.

## Reporting Standards and Deliverables

### Report Structure

- Executive summary and high-level risks.
- Methodology and scope documentation.
- System overview with architecture diagrams.
- Findings with impact and likelihood.
- Reproduction steps and proof-of-concept.
- Recommended remediation actions.
- Appendix with assumptions and test coverage.

### Severity Taxonomy

- Critical: direct loss of funds or control.
- High: significant loss or privilege escalation.
- Medium: notable impact with constraints.
- Low: minor impact or edge-case exposure.
- Informational: best practices and hygiene.

### Finding Metadata

- Unique identifier and title.
- Affected components and versions.
- Root cause analysis.
- Exploit prerequisites.
- Estimated economic impact.
- Proof-of-concept links or code.
- Remediation guidance and references.

## Remediation and Retest Workflow

### Remediation Support

- Provide patch guidance and secure alternatives.
- Validate fixes against original exploit.
- Confirm no new regressions introduced.
- Re-run targeted static checks.
- Update findings status and documentation.

### Retest Process

- Establish retest window and scope.
- Validate applied fixes in new commit.
- Reproduce original issue to confirm closure.
- Review any related code changes.
- Issue retest summary in final report.

## Quality Assurance and Metrics

### Quality Gates

- Minimum reviewer coverage per critical module.
- Independent verification of high severity findings.
- Cross-check findings against threat model.
- Peer review of report narrative and clarity.
- Consistent severity calibration across engagements.

### Metrics and KPIs

- Findings per 1,000 LOC by category.
- Average time to first issue.
- Retest success rate.
- Regressions introduced post-fix.
- Time from kickoff to report delivery.
- Coverage of critical flows.
- Client satisfaction and feedback scores.

## Team Structure and Staffing Model

### Org Structure

- Security engineering lead for each engagement.
- Domain specialists for cryptography and DeFi.
- Research engineers dedicated to tooling.
- Project manager for scheduling and coordination.
- QA reviewer for report consistency.

### Staffing Patterns

- Small audits: 2 to 3 engineers.
- Medium audits: 3 to 5 engineers.
- Large audits: 5+ engineers with specialists.
- Parallel review streams for critical subsystems.
- Rotating on-call support during remediation.

### Engagement Roles

- Engagement lead: owns scope, timeline, and quality.
- Primary reviewer: deep dive into core logic.
- Secondary reviewer: independent verification.
- Tooling specialist: fuzzing and automation.
- Research liaison: ecosystem knowledge and advisories.

## Role Definitions and Responsibilities

### Engagement Lead

- Define scope and schedule.
- Coordinate with client stakeholders.
- Review findings for clarity and accuracy.
- Ensure final report aligns with methodology.
- Facilitate remediation and retest.

### Security Engineer

- Perform manual code review.
- Write fuzzing and invariant tests.
- Validate threat model assumptions.
- Draft findings with evidence.
- Collaborate on remediation.

### Research Engineer

- Develop tools and detection rules.
- Track ecosystem vulnerabilities.
- Provide domain expertise on primitives.
- Contribute to formal methods and analysis.
- Maintain internal knowledge base.

### Project Manager

- Maintain timeline and milestones.
- Coordinate meetings and deliverables.
- Track issue status and feedback.
- Ensure documentation completeness.

## Research Focus and Knowledge Areas

### Smart Contract Security

- Reentrancy and cross-function calls.
- Integer precision and rounding.
- Access control and role misconfiguration.
- Upgradeability storage collisions.
- Token standard deviations and edge cases.
- Flash loan amplification vectors.

### Protocol Design

- Incentive alignment and staking security.
- Governance attack surfaces.
- Oracle selection and failure modes.
- Liquidation and margin parameters.
- Cross-chain messaging and finality.

### Cryptography Research

- Threshold signatures and MPC.
- ZK proof systems and circuits.
- SNARK/STARK parameter security.
- Signature malleability and EIP-712.
- Randomness beacons and VRFs.

### Infrastructure Research

- RPC reliability and endpoint security.
- MEV relays and builder markets.
- Data indexing and integrity.
- Key custody and multisig tooling.

## Client Types and Engagement Patterns

### Client Segments

- DeFi protocols and AMMs.
- Lending platforms and money markets.
- NFT marketplaces and gaming systems.
- L2 rollups and appchains.
- Bridges and cross-chain protocols.
- Wallets and key management providers.
- Governance tooling and DAO frameworks.
- Infrastructure and node operators.

### Engagement Drivers

- Pre-launch security assurance.
- Post-incident analysis and recovery.
- Regulatory or investor due diligence.
- Major protocol upgrades.
- New chain deployment or bridge.
- Mergers and ecosystem partnerships.

### Client Expectations

- Clear, prioritized findings.
- Practical remediation guidance.
- Collaboration during fixes.
- Evidence-backed severity ratings.
- Suggestions for long-term security posture.

## Career Paths and Progression Ladders

### Entry-Level Roles

- Security analyst.
- Junior smart contract auditor.
- Research assistant.
- QA reviewer for reports.

### Mid-Level Roles

- Security engineer.
- Protocol analyst.
- Fuzzing and tooling specialist.
- Formal methods contributor.

### Senior Roles

- Senior security engineer.
- Engagement lead.
- Research lead.
- Principal auditor.

### Leadership Roles

- Director of security research.
- Head of audits.
- Chief security officer.

### Skill Progression Themes

- Deeper protocol design understanding.
- Stronger formal methods proficiency.
- Ability to mentor and lead teams.
- Advanced exploit development and triage.
- Strategic risk communication.

## Training, Mentorship, and Culture

### Training Pillars

- Secure coding principles for Solidity and Rust.
- Adversarial mindset and exploit development.
- Economic modeling for DeFi systems.
- Formal verification fundamentals.
- Secure infrastructure and DevOps practices.

### Mentorship Practices

- Pair reviews on complex modules.
- Structured feedback on findings.
- Internal write-ups and knowledge sharing.
- Rotations across protocol types.

### Culture Guidelines

- Encourage curiosity and continuous learning.
- Promote clear, kind, and direct feedback.
- Prioritize user safety and transparency.
- Maintain a bias for action and thoroughness.

## Communication Templates and Rituals

### Client Communication

- Daily or twice-weekly status updates.
- Mid-audit sync for clarifications.
- Findings preview before final report.
- Retest schedule confirmation.

### Internal Rituals

- Daily standup during active audits.
- Finding triage sessions for severity alignment.
- Peer review of proof-of-concept scripts.
- Retrospective after closing an engagement.

## Sample Audit Timelines

### Two-Week Audit (Small Scope)

- Day 1: kickoff, access, scoping.
- Day 2: architecture and threat modeling.
- Day 3: primary code review begins.
- Day 4: static analysis and quick wins.
- Day 5: fuzzing harness setup.
- Day 6: invariant testing and triage.
- Day 7: deeper protocol logic review.
- Day 8: report drafting begins.
- Day 9: findings validation with client.
- Day 10: remediation guidance and closeout.

### Four-Week Audit (Large Scope)

- Week 1: architecture mapping and threat model.
- Week 1: initial static analysis sweep.
- Week 2: deep manual review of core contracts.
- Week 2: dynamic testing and fuzzing.
- Week 3: formal verification on critical paths.
- Week 3: economic analysis and simulation.
- Week 4: report drafting and QA review.
- Week 4: remediation support and retest.

## Artifact Catalog

### Core Artifacts

- Scope document and assumptions.
- Architecture map and data flow diagram.
- Threat model and abuse case list.
- Test harnesses and fuzzing results.
- Formal verification specifications.
- Final report with findings.

### Optional Artifacts

- Proof-of-concept scripts.
- Economic simulations and notebooks.
- Custom static analysis rules.
- Postmortem notes and lessons learned.

## Glossary

- ABI: application binary interface for contracts.
- AMM: automated market maker.
- Bridge: cross-chain messaging and asset transfer.
- DAO: decentralized autonomous organization.
- Fuzzing: random input testing for bugs.
- Invariant: property that must always hold.
- L2: layer-2 scaling network.
- MEV: maximal extractable value.
- Oracle: external data feed for blockchain.
- Proxy: upgradeable contract indirection.
- Reentrancy: re-calling contract before completion.
- Timelock: delay mechanism for governance.
- ZK: zero-knowledge proof systems.

## Appendix: Checklist Compendium

### Access Control Checklist

- Validate owner initialization.
- Confirm role admin hierarchy.
- Check for missing onlyOwner guards.
- Ensure modifiers cover all state changes.
- Validate role revocation logic.
- Review delegatecall usage.
- Confirm correct use of msg.sender and tx.origin.

### Upgradeability Checklist

- Verify storage gap alignment.
- Confirm initializer protection.
- Inspect UUPS and transparent patterns.
- Validate upgrade authorization checks.
- Ensure immutable variables are safe.
- Review proxy admin access controls.

### ERC-20 Checklist

- Handle non-standard return values.
- Avoid assumption about decimals.
- Validate allowance and approve flows.
- Handle fee-on-transfer tokens.
- Ensure safe transfer wrappers.
- Prevent double-spend via callbacks.

### Oracle Checklist

- Confirm price freshness checks.
- Validate fallback sources.
- Review price aggregation and median logic.
- Check for manipulation via low liquidity.
- Ensure proper decimal normalization.
- Verify circuit breaker logic.

### Governance Checklist

- Validate proposal thresholds.
- Review voting power snapshots.
- Check timelock configuration.
- Ensure emergency actions are limited.
- Verify pause mechanisms cannot be abused.

### Economic Checklist

- Validate collateral ratios and liquidation.
- Review fee logic and distribution.
- Check for subsidy abuse.
- Analyze withdrawal and redemption flows.
- Evaluate token emission caps.
- Model adverse market moves.

### Bridge Checklist

- Validate message verification logic.
- Ensure replay protection on chains.
- Review relayer incentives.
- Check for finality assumptions.
- Inspect canonical token handling.
- Validate emergency shutdown paths.

### ZK Checklist

- Validate circuit constraints and ranges.
- Ensure trusted setup parameters.
- Review verifier contract correctness.
- Check for proof replay protection.
- Confirm data availability assumptions.

### Operational Checklist

- Validate deployment scripts and configs.
- Inspect admin key handling.
- Verify monitoring alert thresholds.
- Review backup and recovery plans.
- Ensure proper incident response docs.

## Extended Methodology Notes

### Adversary Modeling

- Passive observer with MEV access.
- Active attacker with flash loan liquidity.
- Malicious governance coalition.
- Insider with privileged key access.
- Cross-chain adversary exploiting finality gaps.

### Attack Surface Mapping

- External functions callable by anyone.
- Admin-only functions with high impact.
- Upgrade hooks and initialization.
- Cross-contract calls and external adapters.
- Off-chain keeper automation triggers.

### Invariant Examples

- Total supply equals sum of balances.
- Collateral never below required ratio.
- Interest accrual monotonicity.
- Governance voting power never negative.
- No unauthorized mint or burn.
- External calls cannot change ownership.

### Report Clarity Checklist

- Include diagrams for critical flows.
- Provide minimal reproduction steps.
- Highlight exploit preconditions.
- Map findings to threat model.
- Offer concrete mitigation steps.
- Provide severity rationale.

## Additional Research Themes

### Cross-Chain Security

- Light client validation tradeoffs.
- Optimistic versus zk bridging.
- Relayer collusion and bribery.
- Reorg-aware message delivery.

### MEV and Transaction Ordering

- Private mempools and relays.
- Builder-based auction mechanisms.
- Sandwich and backrun simulation.
- Order flow dependency risks.

### Tokenomics and Governance

- Lockups and vesting schedules.
- Delegation and snapshot integrity.
- Governance bribery markets.
- Multisig versus DAO tradeoffs.

### Wallet and UX Security

- Transaction simulation support.
- Phishing-resistant signing flows.
- Hardware wallet integration.
- Safe address book management.

## Example Finding Template

- Title: concise and descriptive.
- Severity: critical/high/medium/low/info.
- Impact: describe funds and control impact.
- Description: explain the root cause.
- Proof: reproduction steps and code.
- Recommendation: clear fix steps.
- References: relevant links and advisories.

## Example Remediation Checklist

- Implement patch and add tests.
- Run targeted fuzzing for regression.
- Update documentation and assumptions.
- Review interactions with adjacent modules.
- Re-run static analysis.
- Prepare summary for retest.

## Example Retest Summary Template

- Date of retest.
- Commit hash reviewed.
- Finding status: fixed/partial/not fixed.
- Notes on residual risk.
- Additional recommendations if needed.

## Notes on Ecosystem Trends

- Rapid innovation increases design risk.
- Multi-chain deployments expand attack surface.
- Token incentives can distort governance.
- Security budgets often lag TVL growth.
- Formal methods adoption is increasing.
- Infrastructure centralization remains a key risk.

## Closing Thoughts

This deep dive outlines a rigorous, research-first audit methodology.
Comprehensive audits combine architecture review, code analysis, and economics.
Team structure and clear roles improve coverage and accountability.
Continuous research drives higher quality and better threat modeling.
Client collaboration and clear communication are essential for safe launches.
