# Space & Satellite Security Consulting: 10K Resource Research
*Focus: space security, satellite systems, defense aerospace consulting, rates, and clearance*

Version: 2025-01
Prepared for: consultation-platforms repository

## Scope & Source Note
- This report synthesizes space/satellite/defense aerospace material found in this repository.
- It does not use live web lookups or external scraping.
- The "10K" label follows repository naming conventions and is not a verified external source count.
- Numeric rate and clearance data are extracted from local files listed in Appendix F.

## How to Use This Document
- Use the rate benchmarks as directional guidance for proposals and staffing.
- Use the threat and control sections to scope security assessments.
- Use the checklists to drive discovery and pre-launch reviews.
- Use the SOW and deliverables sections to assemble packages.

## Table of Contents
- [Executive Summary](#executive-summary)
- [Market Landscape & Demand Drivers](#market-landscape--demand-drivers)
- [Mission Types & Use Cases](#mission-types--use-cases)
- [Space System Architecture Overview](#space-system-architecture-overview)
- [Segment Threat Model](#segment-threat-model)
- [Threat Taxonomy](#threat-taxonomy)
- [Mission Assurance Principles](#mission-assurance-principles)
- [Space Segment Security Controls](#space-segment-security-controls)
- [Ground Segment Security Controls](#ground-segment-security-controls)
- [User Segment Security Controls](#user-segment-security-controls)
- [Satcom Security Deep Dive](#satcom-security-deep-dive)
- [PNT/GNSS Security](#pntgnss-security)
- [Onboard Software Assurance](#onboard-software-assurance)
- [Payload & Data Handling](#payload--data-handling)
- [Key Management](#key-management)
- [Supply Chain & Manufacturing Security](#supply-chain--manufacturing-security)
- [Launch & Mission Ops](#launch--mission-ops)
- [Incident Response & Recovery](#incident-response--recovery)
- [Monitoring & SOC](#monitoring--soc)
- [Testing & Verification](#testing--verification)
- [Governance & Compliance](#governance--compliance)
- [Clearance Requirements](#clearance-requirements)
- [Rate Benchmarks & Compensation](#rate-benchmarks--compensation)
- [Pricing Models & Multipliers](#pricing-models--multipliers)
- [Engagement Types & Service Menu](#engagement-types--service-menu)
- [Scoping Questionnaire](#scoping-questionnaire)
- [Deliverables & Artifacts](#deliverables--artifacts)
- [Sample SOW Packages](#sample-sow-packages)
- [Program Timeline](#program-timeline)
- [Stakeholder Map](#stakeholder-map)
- [Risk Register Template](#risk-register-template)
- [Metrics, KPIs, and ROI](#metrics-kpis-and-roi)
- [Tools & Platforms Landscape](#tools--platforms-landscape)
- [Talent & Staffing](#talent--staffing)
- [Business Development](#business-development)
- [Appendix A: Space Segment Checklist](#appendix-a-space-segment-checklist)
- [Appendix B: Ground Segment Checklist](#appendix-b-ground-segment-checklist)
- [Appendix C: Satcom Security Review Checklist](#appendix-c-satcom-security-review-checklist)
- [Appendix D: Clearance & Compliance Checklist](#appendix-d-clearance--compliance-checklist)
- [Appendix E: Rate Calculator Worksheet](#appendix-e-rate-calculator-worksheet)
- [Appendix F: Source Extracts from Repository](#appendix-f-source-extracts-from-repository)
- [Appendix G: Glossary](#appendix-g-glossary)
- [Appendix H: Mission Assurance Validation Checklist](#appendix-h-mission-assurance-validation-checklist)

## Executive Summary
- Space and satellite security is a high-stakes niche blending cyber, RF, and mission assurance.
- Threats include jamming, interception, spoofing, and ground segment intrusion.
- Mission impact centers on availability, integrity, and continuity of operations.
- Defense aerospace buyers frequently require security clearances and on-site access.
- Satcom usage for remote assets creates demand for specialized security reviews.
- Supply chain and manufacturing risk is elevated due to export controls and DIB concerns.
- Ground segment compromise is often the fastest path to mission disruption.
- Satellite fleets need resilient, redundant comms and recovery playbooks.
- Security programs must align with mission timelines and launch windows.
- Pricing reflects scarcity, clearance gating, and operational risk exposure.

## Market Landscape & Demand Drivers
- Government and defense budgets prioritize assured access to space and resilient comms.
- Commercial constellations expand the attack surface and create new exposure.
- Remote industries rely on satcom for safety-critical operations and telemetry.
- High-profile disruptions increase executive attention to mission assurance.
- Regulatory and contractual requirements push security earlier in design cycles.
- Supply chain risks drive demand for component provenance and SBOMs.
- Ground segment modernization introduces cloud and DevSecOps controls.
- Dual-use systems must satisfy both commercial and classified requirements.
- Scarcity of cleared talent sustains premium rates and longer onboarding.
- Incident response expectations include cross-domain coordination and disclosure.
- Multi-constellation strategies create demand for interoperability security.
- Insurance and risk transfer are expanding in aerospace portfolios.

## Mission Types & Use Cases
- Earth observation and geospatial intelligence.
- SATCOM for maritime, aviation, and remote industrial sites.
- Positioning, navigation, and timing (PNT/GNSS).
- Weather, climate, and environmental sensing.
- Military ISR and tactical communications.
- Space domain awareness (SSA) and tracking.
- Launch vehicle telemetry and range safety.
- On-orbit servicing and rendezvous operations.
- Hosted payloads and payload-as-a-service models.
- CubeSat and smallsat research missions.
- Emergency response communications and public safety.
- Commercial broadband constellations.

## Space System Architecture Overview

### 4.1 Space Segment
- Satellite bus, payload, and onboard compute.
- TT&C links for command and telemetry.
- Onboard data storage and processing.
- Attitude control and propulsion subsystems.
- Power management and battery systems.
- Crosslinks between satellites (inter-satellite links).
- Firmware and flight software update mechanisms.
- Physical tamper constraints and anti-tamper design.

### 4.2 Ground Segment
- Mission operations center and control systems.
- Ground stations and antenna networks.
- Scheduling, uplink, and downlink services.
- Telemetry processing and alerting pipelines.
- Data ingestion, storage, and distribution services.
- Operator workstations and privileged access systems.
- Integration with cloud analytics platforms.
- External partner and vendor connectivity.

### 4.3 User Segment
- User terminals and edge receivers.
- Customer networks and integration points.
- Mobile and maritime terminals with constrained power.
- Distribution networks for data products.
- APIs for customer-facing access.
- Reseller and integrator connections.

### 4.4 Data Processing & Cloud Segment
- Cloud data lakes for payload data.
- AI/ML pipelines for imagery analytics.
- Customer portals and delivery services.
- Billing and mission planning systems.
- Monitoring, logging, and SIEM platforms.
- DevSecOps pipelines for ground software.

## Segment Threat Model
- Adversaries target ground systems due to accessibility and impact.
- RF interference can deny service without touching IT systems.
- Insider risk is elevated on cleared and on-site programs.
- Supply chain compromise can introduce persistent weaknesses.
- Compromised user terminals can become pivot points.
- Misconfigured cloud services expose payload data.
- TT&C compromise can lead to loss of control or mission abort.
- Data integrity attacks can degrade downstream decisioning.
- Satellite software updates can be abused if not authenticated.
- Physical sabotage targets ground stations and power systems.

## Threat Taxonomy
- RF jamming of uplink and downlink channels.
- Spoofing of GNSS/PNT signals.
- Replay of telemetry or command streams.
- Unauthorized command injection into TT&C.
- Compromise of ground station network perimeter.
- Credential theft from mission operations staff.
- Supply chain malware in embedded components.
- Rogue firmware updates or counterfeit parts.
- Data exfiltration from imagery processing pipelines.
- Lateral movement from IT to mission networks.
- Cloud control plane compromise.
- Dependency compromise in ground software CI/CD.
- API abuse of customer data services.
- Insider manipulation of scheduling or mission plans.
- Denial of service against customer delivery portals.
- Social engineering against operations teams.
- Physical intrusion at ground sites.
- GPS time manipulation affecting system sync.
- Spectrum abuse or unauthorized transmission.
- Crosslink compromise affecting constellation coordination.

## Mission Assurance Principles
- Assume contested environments and design for degraded operations.
- Prioritize availability and integrity over confidentiality alone.
- Enforce least privilege across mission operations roles.
- Separate mission-critical networks from corporate IT.
- Require cryptographic authentication for all commands.
- Build in redundancy for comms and data paths.
- Validate updates with signed packages and rollback plans.
- Use fault containment to prevent cascading failures.
- Monitor for RF anomalies and unexpected link behavior.
- Document mission impact thresholds and decision criteria.

## Space Segment Security Controls
- Secure boot with hardware root of trust where feasible.
- Authenticated and encrypted command channels.
- Command authorization with dual-control or quorum rules.
- Telemetry integrity checks and sequence validation.
- Flight software signing and update chain-of-custody.
- Onboard logging with tamper-evident storage.
- Partitioning between payload and bus systems.
- Redundant comms paths or fallback command modes.
- Fault detection, isolation, and recovery (FDIR) protections.
- Rate limiting and safe mode triggers for anomalies.
- Key rotation and credential lifecycle management.
- Crosslink authentication and link-layer security.
- Baseline configuration and secure parameter storage.
- Jamming detection thresholds tied to autonomy rules.
- Secure time sources and clock integrity validation.

## Ground Segment Security Controls
- Segmented networks for mission, engineering, and corporate IT.
- Multi-factor authentication for privileged consoles.
- Dedicated jump hosts and hardened admin workstations.
- Strict change management for mission-critical systems.
- Continuous monitoring and centralized logging.
- Zero trust principles for remote operator access.
- Secure APIs with least privilege and scoped tokens.
- Patch management aligned to mission windows.
- Backups and recovery plans tested for mission systems.
- Asset inventory for antennas, servers, and radios.
- Secure remote access with audited sessions.
- Encrypt telemetry at rest and in transit.
- Vulnerability management with mission impact triage.
- Physical security controls for ground stations.
- Third-party access governed by contracts and monitoring.

## User Segment Security Controls
- Hardened user terminals and firmware integrity checks.
- Secure enrollment and provisioning for terminals.
- Customer network segmentation to isolate satcom paths.
- Tokenized API access for data delivery.
- Rate limiting and abuse prevention on public endpoints.
- Tamper detection for portable terminals.
- Secure configuration defaults for shipped devices.
- Clear incident escalation paths for customers.
- Monitoring of anomalous terminal behavior.
- Guidance for customer key management and access roles.

## Satcom Security Deep Dive
- Satcom links are vulnerable to jamming and interception.
- Remote assets rely on Starlink/Satcom for continuity in harsh environments.
- Compromised terminals can expose telemetry and control channels.
- Link-layer encryption should be enforced where possible.
- Authentication must be required for uplink commands.
- Spectrum monitoring helps detect interference patterns.
- Redundant comms paths mitigate single-channel denial.
- Ground station diversity reduces localized outages.
- Secure scheduling prevents unauthorized uplink windows.
- Satellite beamforming policies should be access-controlled.
- Terminal provisioning must include identity validation.
- Satellite & space niche work includes "Satcom Security Reviews".
- Jamming response playbooks should be pre-approved.
- Test comms failover during planned outages.
- Coordinate with regulators for spectrum incident reporting.

## PNT/GNSS Security
- Treat GNSS as an untrusted input without verification.
- Use multi-constellation receivers where feasible.
- Cross-check PNT with inertial navigation systems.
- Detect spoofing via signal strength and timing anomalies.
- Apply holdover clocks for timing continuity.
- Log PNT anomalies and reconcile with ground truth.
- Segment PNT processing from mission planning systems.
- Validate time synchronization for distributed systems.
- Apply anti-jam antennas for critical nodes.
- Test PNT degradation scenarios in mission rehearsals.

## Onboard Software Assurance
- Threat model onboard software interfaces and APIs.
- Use secure coding standards for flight software.
- Verify compiler provenance and build environment integrity.
- Maintain reproducible builds and signed artifacts.
- Enforce code review and mission-critical change controls.
- Minimize attack surface by disabling unused services.
- Implement watchdogs and safe-mode recovery flows.
- Protect configuration data with integrity checks.
- Validate external command schemas and bounds.
- Maintain a vulnerability disclosure and patch path.

## Payload & Data Handling
- Classify payload data sensitivity and handling requirements.
- Encrypt payload data at rest in ground processing systems.
- Enforce least-privilege access to imagery repositories.
- Use immutable logging for data access events.
- Validate integrity from downlink to final delivery.
- Control export restrictions and data residency constraints.
- Apply watermarking or fingerprinting for sensitive imagery.
- Rate-limit bulk exports to prevent data scraping.
- Monitor for unusual customer access patterns.
- Document data retention and deletion policies.

## Key Management
- Use hardware-backed key storage where feasible.
- Establish key hierarchy for mission, payload, and ops.
- Rotate keys on a defined cadence and after incidents.
- Separate test keys from production mission keys.
- Store key material in secured, audited environments.
- Maintain multi-party control for high-impact keys.
- Document key recovery and escrow procedures.
- Validate key usage policies against mission profiles.
- Track key distribution with cryptographic attestations.
- Test key revocation and re-key procedures pre-launch.

## Supply Chain & Manufacturing Security
- Track component provenance and authorized suppliers.
- Apply SBOM requirements to ground and onboard software.
- Perform counterfeit part detection and validation.
- Enforce secure manufacturing and assembly processes.
- Monitor for hardware trojans and unexpected behavior.
- Vet third-party firmware and embedded libraries.
- Apply export control screening for suppliers.
- Implement secure transport and storage for components.
- Require background checks for sensitive build roles.
- Clearance premiums apply to cleared federal/defense manufacturing work.
- DIB supply chain work commands a clearance premium.
- Maintain tamper-evident packaging and chain-of-custody.
- Align C-SCRM controls with mission risk tolerance.
- Validate lab environments for secure test data handling.
- Document component end-of-life and replacement plans.

## Launch & Mission Ops
- Align security milestones with launch readiness reviews.
- Freeze configurations prior to launch window.
- Establish change control boards for mission software.
- Validate fallback procedures for launch anomalies.
- Protect range safety telemetry and command links.
- Conduct pre-launch red team exercises on ground segment.
- Validate physical security for launch facilities.
- Establish emergency comms for launch interruptions.
- Test go/no-go criteria for security-related risks.
- Maintain incident war room readiness during launch.

## Incident Response & Recovery
- Define mission-critical incident severity levels.
- Pre-stage comms plans for internal and external parties.
- Establish evidence collection procedures for ground systems.
- Define authority for safe mode or decommission actions.
- Maintain forensic-ready logging for mission systems.
- Align IR procedures with contractual reporting timelines.
- Test recovery of mission control applications.
- Document satellite command recovery and key rotation steps.
- Include RF interference response playbooks.
- Coordinate with legal and compliance for classified contexts.

## Monitoring & SOC
- Centralize logs from mission and ground systems.
- Monitor telemetry anomalies and command usage patterns.
- Apply detection rules for unauthorized uplink attempts.
- Include RF monitoring telemetry in SIEM workflows.
- Track integrity checks for payload data pipelines.
- Use UEBA for operator and admin activity.
- Build alert runbooks for satellite anomalies.
- Ensure after-hours coverage for critical windows.
- Integrate incident response automation where safe.
- Report metrics to mission leadership regularly.

## Testing & Verification
- Perform threat modeling early in design phases.
- Execute secure code reviews for flight software.
- Fuzz test command parsing and telemetry handlers.
- Validate cryptographic protocols under failure conditions.
- Run tabletop exercises for jamming and spoofing events.
- Test key rotation and recovery procedures.
- Conduct red team assessments of ground segment networks.
- Verify backup restoration for mission control systems.
- Pen test customer portals and APIs.
- Validate least privilege for operator roles.
- Simulate compromised terminal scenarios.
- Assess supply chain risk for third-party components.
- Verify security monitoring coverage and log retention.
- Conduct launch-readiness security checkpoints.
- Document residual risk and mission acceptance.

## Governance & Compliance
- Map controls to NIST 800-53 or equivalent baselines.
- Use NIST 800-171 and CMMC for defense supply chain alignment.
- Apply RMF process for federal or classified systems.
- Align cloud services with FedRAMP where required.
- Maintain export control (ITAR/EAR) compliance for data and components.
- Document data residency constraints for payload data.
- Maintain policy frameworks for dual-use missions.
- Establish authority-to-operate (ATO) workflows when applicable.
- Align security requirements with contract clauses and SOWs.
- Track audit evidence and control ownership.
- Maintain vendor risk assessments for mission-critical suppliers.
- Establish exception processes for mission schedule conflicts.
- Ensure governance for key management and crypto changes.
- Document incident reporting timelines and thresholds.
- Align security metrics to mission assurance objectives.

## Clearance Requirements
- Clearance gating is common for defense aerospace projects.
- Typical clearance levels: Secret, TS, TS/SCI, TS/SCI + Poly.
- TS/SCI is common for defense and intelligence programs.
- TS/SCI + Poly appears in highly restricted missions.
- SETA roles often require TS/SCI and on-site presence.
- Clearance sponsorship may require prime contractor relationships.
- Clearance tracking reduces risk of lapsed credentials.
- On-site or SCIF access is common in classified contexts.
- Clearance level impacts staffing timelines and pricing.
- Background investigations may be required for subcontractors.
- Classified data handling drives stricter tool requirements.
- Clearance requirements should be confirmed in RFPs early.
- Clearance expectations affect resource availability forecasts.
- Document clearance verification for audit readiness.
- Clearance scarcity is a major premium driver.

## Rate Benchmarks & Compensation

### 23.1 Platform Rate Signals (Space/Defense)
| Platform | Category | Rate Range | Notes |
| --- | --- | --- | --- |
| Booz Allen Space Cyber | Space/Satellite Security | $275-$550/hr | EXTREME relevance |
| LinQuest Space Systems | Space/Satellite Security | $250-$500/hr | EXTREME relevance |
| Decent Cybersecurity | Space/Satellite Security | €200-€450/hr | HIGH relevance |
| Honeywell Aerospace Cyber | Aviation Security | $250-$500/hr | EXTREME relevance |
| Thales Aviation Cyber | Aviation Security | $275-$550/hr | EXTREME relevance |
| CACI Cyber Consulting | Defense Consulting | $275-$550/hr | EXTREME relevance |
| Peraton Cyber Mission | Defense Consulting | $250-$500/hr | EXTREME relevance |
| ClearanceJobs | Defense Consulting | $150k-$300k/year | EXTREME relevance |

### 23.2 Cleared Bill Rate Benchmarks (Internal)
| Target Role | W-2 Equivalent | Recommended Bill Rate |
| --- | --- | --- |
| Mid-Level Analyst | ~$110k | $90-$115/hour |
| Senior ISSE / Engineer | ~$160k | $135-$165/hour |
| SME / Cloud Architect | ~$200k | $175-$225/hour |
| Crisis IR Lead | $250k+ | $250-$400+/hour |

### 23.3 Clearance Premium Signals
- Top Secret clearance adds ~$20k-$30k to base compensation.
- Clearance premium for defense manufacturing: +15-25%.
- DIB supply chain clearance premium: +25%.
- Security clearance premium (general consulting): 15-30%.
- Security clearance premium (SOC/SIEM): 25-80%.
- Security clearance premium (zero trust): 15-35%.
- Defense/government sector premium: +30-60%.

### 23.4 Aerospace & Defense Salary Signals
- Aerospace & Defense median (DevSecOps): $133,931.
- Aerospace & Defense median (Threat Intel): $117,371.
- Aerospace & Defense median (SOC Analyst): $101,846.
- Aerospace & Defense median (top-paying industry signal): $121,697.
- Aerospace & Defense top-paying industry signal (training roles): $85,316.

### 23.5 Cleared Salary Benchmarks (Internal)
| Role Category | Experience | Clearance | Average Salary | Top Percentile |
| --- | --- | --- | --- | --- |
| Security Ops / Analyst | Mid (3-5 yrs) | Secret | ~$95k | ~$127k |
| Cyber Engineer / Architect | Senior (8+ yrs) | TS/SCI | ~$133,554 | ~$177k+ |
| IT/Cyber Leadership | Mgmt (10+ yrs) | TS/SCI | ~$167k | ~$240k+ |
| DevSecOps Engineer | Senior | TS/SCI + Poly | ~$155k | ~$210k |

### 23.6 Additional Rate References
- General security consultant range: $100-$250/hour.
- Senior pentester range: $150-$300/hour.
- vCISO advisory range: $200-$500/hour.
- TS clearance roles: $135,000-$216,000 salary range.
- Threat intel consulting premium: +15% over employed roles.
- Currency note: Euro-denominated rates require FX normalization.

## Pricing Models & Multipliers
- Time and materials is common for mission systems with uncertainty.
- Fixed-fee works best for bounded deliverables and clear scope.
- Retainers align with ongoing monitoring and mission support.
- Emergency response can command 1.5x-2.0x rates.
- On-site and SCIF work typically adds a premium.
- Clearance gating reduces supply and increases rates.
- Short delivery windows raise pricing due to opportunity cost.
- Multi-constellation scope increases integration effort.
- High-liability missions justify additional risk premiums.
- Long-term embedded roles may lower hourly rates.

## Engagement Types & Service Menu
- Space system threat modeling and risk assessment.
- TT&C security review and command channel validation.
- Satcom security review for remote operations.
- Ground segment network segmentation and hardening.
- Mission operations access control redesign.
- Secure update pipeline and software assurance.
- Supply chain and SBOM validation for flight software.
- Key management strategy and HSM deployment.
- Incident response readiness and tabletop exercises.
- RF interference detection and response planning.
- GNSS/PNT spoofing resilience assessment.
- Cloud data pipeline security review for payload data.
- Security monitoring integration and SIEM tuning.
- Red team assessment of ground stations.
- Compliance mapping for RMF/CMMC/FedRAMP.
- Export control and data residency analysis.
- Security architecture for inter-satellite links.
- Resilience engineering and redundancy planning.
- Mission assurance metrics and KPI design.
- Post-incident remediation and lessons learned reviews.

## Scoping Questionnaire
- Q: What mission types and orbits are in scope?
- Q: Which payloads are classified or export-controlled?
- Q: What TT&C protocols and vendors are used?
- Q: Are there crosslinks or inter-satellite links?
- Q: What ground stations and network providers are involved?
- Q: Which components are owned vs. third-party managed?
- Q: What cloud services host mission or payload data?
- Q: Are there existing SBOMs and component inventories?
- Q: What clearance levels are required for staff?
- Q: Are SCIFs or on-site requirements in scope?
- Q: What is the operational tempo and contact schedule?
- Q: What is the incident reporting requirement timeline?
- Q: What encryption standards are currently applied?
- Q: How are keys generated, stored, and rotated?
- Q: Are there known jamming or spoofing incidents?
- Q: What redundancy or failover exists for comms?
- Q: How are software updates delivered to flight systems?
- Q: What monitoring and logging is currently in place?
- Q: What SLAs exist for data delivery?
- Q: Who approves command uplinks and schedule windows?
- Q: What vendor risk processes exist for suppliers?
- Q: What is the risk appetite for mission degradation?
- Q: What budget and timeline constraints exist?
- Q: What compliance frameworks are contractually required?
- Q: What evidence is needed for audits and reporting?

## Deliverables & Artifacts
- Mission threat model and risk register.
- System architecture diagrams with trust boundaries.
- TT&C security assessment report.
- Satcom security review findings and recommendations.
- Ground segment hardening plan.
- Key management architecture and procedures.
- Supply chain risk assessment and SBOM review.
- Logging and monitoring coverage matrix.
- Incident response playbooks and escalation paths.
- Compliance mapping matrix (RMF/CMMC/FedRAMP).
- Security test plan and validation checklist.
- Operator access control matrix.
- Recovery and continuity plan.
- Residual risk acceptance documentation.
- Executive summary and mission impact analysis.
- Training plan for operators and admins.
- Secure update pipeline design.
- Metrics and KPI dashboard design.
- Vendor risk assessment templates.
- Final remediation roadmap with priorities.

## Sample SOW Packages
- Package 1: Space System Security Assessment (6-10 weeks).
- Package 2: Ground Segment Hardening + Monitoring (8-12 weeks).
- Package 3: Satcom Security Review + Jamming Playbook (4-6 weeks).
- Package 4: Cleared Mission Assurance Program (12-24 weeks).
- Package 5: Continuous Security Retainer (monthly).
- Package 6: Incident Response Standby (on-call).

## Program Timeline
- Phase 0: Discovery and access onboarding.
- Phase 1: Threat modeling and architecture review.
- Phase 2: Control assessment and gap analysis.
- Phase 3: Remediation planning and quick wins.
- Phase 4: Implementation support and validation.
- Phase 5: Monitoring and operational handoff.
- Phase 6: Post-launch review and continuous improvement.
- Phase 7: Decommissioning and data retention review.
- Phase 8: Lessons learned and KPI refinement.
- Phase 9: Annual re-assessment cycle.

## Stakeholder Map
- Mission operations leadership.
- Satellite engineering and flight software teams.
- Ground station and network operations teams.
- Security operations and incident response teams.
- Compliance and export control officers.
- Legal, contracts, and procurement stakeholders.
- Program management and PMO.
- External partners and integrators.
- Customer success and data delivery teams.
- Executive sponsor and risk owners.

## Risk Register Template
- Risk ID and description.
- Mission impact (availability, integrity, confidentiality).
- Likelihood and severity scoring.
- Attack vector and threat actor profile.
- Affected segment (space, ground, user, supply chain).
- Existing controls and coverage gaps.
- Recommended remediation actions.
- Owner and due date.
- Residual risk after remediation.
- Acceptance or escalation decision.

## Metrics, KPIs, and ROI
- Mean time to detect (MTTD) for mission anomalies.
- Mean time to respond (MTTR) for ground incidents.
- Percentage of authenticated command uplinks.
- Key rotation compliance rate.
- Patch latency for ground segment systems.
- Incident response exercise completion rate.
- Telemetry integrity verification coverage.
- RF interference detection time.
- Unauthorized access attempts blocked per period.
- Mission downtime attributable to security events.
- Data delivery SLA adherence.
- Percentage of suppliers with SBOMs.
- Clearance coverage ratio for staffing needs.
- Reduction in critical findings over time.
- Cost avoidance from prevented incidents.

## Tools & Platforms Landscape
- Mission ops platforms and scheduling systems.
- Ground station management suites.
- RF monitoring and spectrum analytics.
- SIEM and log aggregation tools.
- HSMs and key management services.
- Vulnerability scanners for ground systems.
- SBOM generation and dependency scanners.
- CI/CD security tooling for ground software.
- Endpoint detection for operator workstations.
- Secure remote access and PAM tools.
- Incident response case management systems.
- Configuration management and IaC tooling.

## Talent & Staffing
- Mission assurance lead with aerospace experience.
- Satellite systems security architect.
- Ground segment security engineer.
- RF/Satcom specialist for interference analysis.
- DevSecOps engineer for ground software pipelines.
- Security operations analysts with OT/ICS exposure.
- Clearance-eligible staff for classified programs.
- Supply chain security and C-SCRM specialist.
- Incident response lead with crisis communications.
- Compliance lead for RMF/CMMC alignment.
- Operator training and readiness coordinator.
- Data protection and privacy specialist.
- Export control compliance advisor.
- Program manager for security delivery.
- QA and verification specialist for test plans.

## Business Development
- Target primes and integrators with active space contracts.
- Position satcom security reviews as a niche entry offer.
- Build partnerships with ground station operators.
- Maintain a bench of cleared staff and proof of clearance.
- Offer pre-launch readiness assessments as fixed packages.
- Emphasize mission assurance outcomes over tooling.
- Document past performance and mission impact metrics.
- Align proposals with RFP compliance language.
- Highlight export control and supply chain expertise.
- Build case studies around resilience and uptime.

## Appendix A: Space Segment Checklist
- Secure boot implemented and verified.
- Flight software signing enforced.
- Command uplink authentication required.
- Telemetry integrity checks enabled.
- Safe mode triggers documented.
- Fault detection and recovery tested.
- Crosslink encryption configured.
- TT&C key rotation tested.
- Onboard logs protected against tampering.
- Partitioning between payload and bus validated.
- Unused services disabled.
- Firmware update rollback plan documented.
- Jamming detection thresholds configured.
- Onboard time source integrity validated.
- Rate limiting for commands defined.
- Emergency command pathway documented.
- Watchdog timers configured and tested.
- Payload data confidentiality controls set.
- Data integrity verification for downlink.
- Telemetry sequence validation in place.
- Secure storage for keys validated.
- Hardware root of trust availability assessed.
- Autonomy rules reviewed for safety impact.
- Attitude control safety constraints documented.
- Onboard audit events configured.
- Telemetry loss handling procedures documented.
- Command approval workflow documented.
- RF link policy configuration reviewed.
- Satellite ID and identity claims verified.
- Constellation synchronization safeguards validated.
- End-of-life decommission procedures documented.
- Anti-tamper physical controls verified.
- Configuration baselines stored securely.
- Firmware provenance validated.
- Key escrow policy approved.

## Appendix B: Ground Segment Checklist
- Mission network segmented from corporate IT.
- MFA enforced for mission operations.
- Privileged access management in place.
- Operator workstations hardened.
- Patch cadence aligned to mission windows.
- Backups tested for mission control systems.
- Centralized logging for mission systems.
- SIEM coverage for ground station networks.
- Secure remote access with session recording.
- Configuration management baselines enforced.
- Network time synchronization validated.
- Vulnerability scanning schedule defined.
- Third-party access approvals documented.
- Incident response runbooks accessible.
- Physical security controls in place at ground sites.
- Asset inventory for ground equipment maintained.
- API keys rotated and scoped.
- Data storage encryption enforced.
- Least privilege for operator roles.
- Change control board for mission systems.
- Out-of-band comms tested.
- Network segmentation rules validated.
- Ground station firmware updates signed.
- Log retention meets contract requirements.
- Security monitoring alert thresholds tuned.
- Data delivery integrity checks implemented.
- Customer portal security testing completed.
- External dependencies documented.
- Backup comms path identified.
- Uplink scheduling approvals enforced.
- Manual override procedures documented.
- Admin account review cadence set.
- Incident escalation contacts updated.
- Disaster recovery site readiness validated.
- Operator training completed.
- Access logs reviewed regularly.

## Appendix C: Satcom Security Review Checklist
- Identify all satcom providers and SLAs.
- Confirm encryption for uplink and downlink.
- Validate authentication for terminal provisioning.
- Review terminal firmware update process.
- Assess jamming detection and response playbooks.
- Validate spectrum monitoring capabilities.
- Confirm redundancy across comms paths.
- Review ground station diversity plans.
- Assess terminal physical security controls.
- Test failover to alternate channels.
- Review RF interference incident reporting path.
- Validate key management for satcom links.
- Confirm least privilege for comms scheduling.
- Review customer terminal access policies.
- Validate data integrity checks for downlink.
- Assess risk of compromised terminals.
- Verify logging for uplink commands.
- Confirm revocation process for stolen terminals.
- Review contract clauses for security obligations.
- Test continuity during planned outages.
- Verify incident escalation contacts.
- Assess crosslink security where applicable.
- Review third-party monitoring coverage.
- Verify anti-jam antenna deployment.
- Confirm access control for beam management.

## Appendix D: Clearance & Compliance Checklist
- Confirm required clearance levels for each role.
- Document clearance sponsorship plans.
- Validate clearance verification and tracking process.
- Identify SCIF or on-site access requirements.
- Confirm data handling rules for classified material.
- Document export control classification (ITAR/EAR).
- Map contract requirements to RMF/CMMC controls.
- Confirm FedRAMP requirements for cloud services.
- Validate subcontractor clearance requirements.
- Document audit evidence collection plan.
- Identify compliance reporting timelines.
- Confirm policies for classified tooling and devices.
- Validate staff background checks and training.
- Confirm secure storage for cleared project data.
- Document incident reporting contacts for government.
- Validate supply chain screening procedures.
- Confirm NIST 800-171 alignment if required.
- Document acceptable use policies for mission systems.
- Confirm data residency commitments.
- Record waiver and exception approval process.

## Appendix E: Rate Calculator Worksheet
- Step 1: Identify W-2 equivalent salary.
- Step 2: Convert to hourly base (salary / 2,080).
- Step 3: Apply burden multiplier (1.6x-1.8x).
- Step 4: Add clearance premium where applicable.
- Step 5: Add urgency or on-site premium if required.
- Step 6: Validate against market benchmarks.
- Example: $160,000 salary / 2,080 = ~$76.92/hr.
- Example: $76.92/hr * 1.7 = ~$130.76/hr.
- Example: Add clearance premium to reach $135-$165/hr.
- Example: Crisis IR lead may reach $250-$400+/hr.
- Example: vCISO advisory can reach $200-$500/hr.
- Example: Euro-denominated rates require FX normalization.
- Example: Long-term embedded roles may use lower multipliers.
- Example: Short delivery windows may add 10-25% premium.
- Example: Document all assumptions in proposals.

## Appendix F: Source Extracts from Repository

### ALL_PLATFORMS_LIST.txt
- Booz Allen Space Cyber — Space/Satellite Security — $275-$550/hr — EXTREME relevance.
- LinQuest Space Systems — Space/Satellite Security — $250-$500/hr — EXTREME relevance.
- Decent Cybersecurity — Space/Satellite Security — €200-€450/hr — HIGH relevance.
- Honeywell Aerospace Cyber — Aviation Security — $250-$500/hr — EXTREME relevance.
- Thales Aviation Cyber — Aviation Security — $275-$550/hr — EXTREME relevance.
- CACI Cyber Consulting — Defense Consulting — $275-$550/hr — EXTREME relevance.
- Peraton Cyber Mission — Defense Consulting — $250-$500/hr — EXTREME relevance.
- ClearanceJobs — Defense Consulting — $150k-$300k/year — EXTREME relevance.

### CODEX_MANUFACTURING_ICS_5K.md
- Satellite & Space context: remote assets connect via Starlink/Satcom.
- Risks cited: jamming, interception, compromised terminals.
- Consulting opportunity: "Satcom Security Reviews" for logistics and energy.
- Clearance premium: +15-25% for cleared federal/defense manufacturing work.

### CODEX_LOGISTICS_SUPPLY_CHAIN_5K.md
- Clearance premium: +25% for Defense Industrial Base (DIB) supply chain work.

### CODEX_FEDERAL_10K.md
- Clearance levels: Secret, Top Secret, TS/SCI, TS/SCI + Poly.
- Top Secret premium: ~$20k-$30k to base compensation.
- Cleared bill rates: $90-$115/hr (mid analyst), $135-$165/hr (senior ISSE).
- Cleared bill rates: $175-$225/hr (SME/Cloud), $250-$400+/hr (IR lead).
- Internal rate signals: $100-$250/hr (security consultant).
- Internal rate signals: $150-$300/hr (senior pentester).
- Internal rate signals: $200-$500/hr (vCISO advisory).
- Cleared salary benchmarks listed for Secret and TS/SCI roles.

### FEDERAL_SECURITY_CONSULTING_GUIDE_2025.md
- SETA roles: TS/SCI almost universally required.
- Cleared salary benchmarks aligned to ClearanceJobs report.
- Bill rate conversion guidance: 1.6x-1.8x multiplier.

### COMPREHENSIVE_SECURITY_SALARY_REPORT_2025.md
- Top Secret clearance premium: ~$20,000-$30,000.
- Contracting ranges: Security Consultant $100-$250/hr.
- Contracting ranges: Senior Pentester $150-$300/hr.
- Contracting ranges: vCISO $200-$500/hr.

### CODEX_SECURITY_FIRMS_10K.md
- Security clearance premium: 15-30%.

### CODEX_SOC_SIEM_10K.md
- Security clearance premium: 25-80%.

### CODEX_ZEROTRUST_10K.md
- Security clearance premium: 15-35%.

### CODEX_THREAT_INTEL_10K.md
- Defense and government premium: +30-60%.

### CODEX_DEVSECOPS_10K.md
- Aerospace & Defense median pay: $133,931.

### COMPREHENSIVE_SECURITY_CONSULTING_INCOME_REPORT_2025.md
- Aerospace & Defense median (DevSecOps): $133,931.
- Aerospace & Defense median (Threat Intel): $117,371.
- Aerospace & Defense median (SOC Analyst): $101,846.
- TS clearance roles: $135,000-$216,000.

### CYBERSECURITY_CONSULTING_INCOME_COMPREHENSIVE_REPORT_2025.md
- Aerospace & Defense median (Threat Intel): $117,371.

### GLASSDOOR_SALARY_COMPILATION_2025.md
- Aerospace & Defense median (top-paying industry signal): $121,697.

### MEDIUM_SECURITY_CONSULTING_COMPREHENSIVE_REPORT_2025.md
- Aerospace & Defense top-paying industry signal: $85,316.

### CODEX_NETWORKING_REFERRALS_5K.md
- Federal/Defense contracting: clearance required or ability to get clearance.

## Appendix G: Glossary
- ATO: Authority to Operate for government systems.
- C-SCRM: Cyber Supply Chain Risk Management.
- CMMC: Cybersecurity Maturity Model Certification.
- DIB: Defense Industrial Base.
- FDIR: Fault Detection, Isolation, and Recovery.
- GNSS: Global Navigation Satellite System.
- ISR: Intelligence, Surveillance, and Reconnaissance.
- ITAR: International Traffic in Arms Regulations.
- RMF: Risk Management Framework.
- SBOM: Software Bill of Materials.
- SCIF: Sensitive Compartmented Information Facility.
- SETA: Systems Engineering and Technical Assistance.
- SSA: Space Situational Awareness.
- TT&C: Telemetry, Tracking, and Command.
- W2: Employee payroll classification for compensation.
- C2C: Corp-to-corp consulting arrangement.
- PAM: Privileged Access Management.
- PNT: Positioning, Navigation, and Timing.
- RF: Radio Frequency.
- SLA: Service Level Agreement.
- SOC: Security Operations Center.
- TARA: Threat Analysis and Risk Assessment.
- T&M: Time and Materials.
- UEBA: User and Entity Behavior Analytics.
- UEI: Unique Entity ID for federal contracting.

## Appendix H: Mission Assurance Validation Checklist
- Mission objectives documented and validated.
- Critical mission assets identified and ranked.
- Threat model completed and reviewed.
- Attack surface inventory validated.
- Data flow diagrams verified with engineering.
- Command paths validated and secured.
- Telemetry integrity checks in place.
- Onboard logging policies defined.
- Ground station access controls verified.
- Operator roles mapped to permissions.
- Redundant comms paths tested.
- Jamming detection thresholds tuned.
- Spoofing detection controls validated.
- Key rotation procedures tested.
- Backup and recovery exercises completed.
- Safe mode recovery procedures verified.
- Incident response plan approved.
- Incident communications plan validated.
- Security monitoring coverage confirmed.
- False positive reduction plan implemented.
- Vulnerability remediation SLAs defined.
- Supply chain risk assessment completed.
- Component provenance documented.
- SBOMs collected for software components.
- Export control checks completed.
- Clearance coverage validated for staff.
- SCIF access requirements met.
- Mission change control board active.
- Configuration baselines documented.
- Secure update pipeline validated.
- Ground segment patch cadence approved.
- Ground segment backups tested.
- Telemetry storage integrity validated.
- Payload data encryption verified.
- API access controls tested.
- Customer portal security tested.
- Rate limiting configured on data services.
- Insider risk controls reviewed.
- Physical security controls verified.
- RF spectrum monitoring operational.
- Crosslink security assessed.
- Inter-satellite link access verified.
- Emergency uplink path documented.
- Command approval workflow tested.
- Staff training completed.
- Red team findings remediated.
- Residual risk documented and accepted.
- Compliance evidence collected.
- Audit readiness checklist completed.
- Mission readiness review includes security sign-off.
- Launch window security freeze executed.
- Post-launch monitoring watch established.
- Incident lessons learned captured.
- KPI dashboard baseline set.
- Continuous improvement cadence defined.
- Annual reassessment scheduled.
- Third-party risk reviews completed.
- Vendor access reviewed and approved.
- Data retention policies validated.
- Decommissioning plan documented.
- End-of-life procedures tested.
- Insurance and risk transfer reviewed.
- Executive risk briefing completed.

