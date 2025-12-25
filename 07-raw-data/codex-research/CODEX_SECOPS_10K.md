# CODEX SecOps Consulting Guide (10K)

## Scope and intent
- Provide a practical Security Operations (SecOps) consulting guide focused on SOC optimization and SOAR implementation.
- Emphasize actionable rate benchmarks, tool landscape, and market opportunity signals.
- Offer vendor-agnostic delivery models that map to measurable outcomes.
- Support independent consultants, boutique firms, and internal SecOps leaders.
- Align with internal repository research and operating patterns.

## Methodology and limitations
- Synthesized from internal research files in this repository; no live web access used.
- Rate and pricing bands are planning ranges, not real-time market quotes.
- Validate numbers against current regional bids and client procurement constraints.
- Treat tool references as examples rather than endorsements.
- Use this guide as a scoping and proposal framework, not a legal or compliance artifact.

## Executive summary
- SecOps demand continues to rise as alert volume, cloud adoption, and compliance obligations expand.
- SOC optimization engagements frequently begin with a short assessment and expand into phased remediation.
- SIEM consulting remains a core revenue driver, especially for migration and content tuning.
- SOAR implementation delivers high leverage when automation targets low-risk, repeatable tasks first.
- Clients pay premiums for consultants who improve MTTD, MTTR, and signal-to-noise ratios.
- Pricing sensitivity varies by client size; mid-market buyers often favor fixed-price phases.
- Tool sprawl and integration gaps create opportunity for workflow redesign and automation.
- Outcome-focused deliverables outperform generic advisory reports in sales cycles.
- Retainers and managed services provide steady income after initial optimization projects.
- Regulatory pressure and cyber insurance requirements sustain SOC investment.

## Internal sources referenced
- CODEX_SOC_SIEM_10K.md
- CODEX_MSP_INCOME.md
- CODEX_SECURITY_ARCH_10K.md
- CODEX_ZEROTRUST_10K.md
- CODEX_OT_SECURITY_10K.md
- CODEX_THREAT_INTEL_10K.md
- CODEX_DEVSECOPS_10K.md
- ZIPRECRUITER_SECURITY_COMPENSATION_GUIDE_2025.md
- CODEX_RED_TEAM_10K.md

## Definitions and glossary
- SecOps: operational security function focused on detection, response, and continuous improvement.
- SOC: Security Operations Center responsible for monitoring, triage, and incident response.
- SIEM: Security Information and Event Management for log collection, normalization, and correlation.
- SOAR: Security Orchestration, Automation, and Response for workflow automation and playbooks.
- SOCaaS: SOC as a Service delivered by an external provider.
- MDR: Managed Detection and Response combining tooling and analyst response.
- EDR/XDR: endpoint and extended detection with telemetry and response actions.
- NDR: network detection and response for traffic analysis and anomaly detection.
- CSPM: cloud security posture management for configuration and risk baselines.
- ITSM: IT service management systems used for case and change workflows.
- CTI: cyber threat intelligence used to enrich detections and prioritization.
- Use case: a defined detection scenario tied to a threat or risk.
- Detection engineering: lifecycle for building, testing, and tuning detections.
- Playbook: documented response steps for a specific incident type.
- Runbook: repeatable operational procedure for analyst execution.
- MTTD: mean time to detect.
- MTTR: mean time to respond or resolve.
- Normalization: conversion of logs into a consistent schema.
- Data model: standardized field schema such as CIM or ECS.
- Signal-to-noise ratio: proportion of actionable alerts to total alerts.
- Log source: system or application emitting telemetry to the SIEM.
- Ingestion: process of collecting and parsing logs in the SIEM.
- Retention: storage duration for searchable telemetry.
- Case management: system of record for incidents and response actions.
- MITRE ATT&CK: taxonomy of adversary tactics and techniques.
- RACI: responsibility matrix for roles and ownership.

## Market landscape and demand drivers
- Regulatory pressure drives demand for audit-ready logging and response processes.
- Cyber insurance requirements increase scrutiny of detection and response maturity.
- Cloud adoption expands log volume and introduces multi-environment complexity.
- Talent shortages increase reliance on external specialists and project-based consulting.
- Ransomware and high-impact incidents accelerate SOC modernization funding.
- Mergers and acquisitions create urgent needs for monitoring integration.
- Tool sprawl causes operational inefficiency and motivates workflow redesign.
- Board-level risk oversight prioritizes measurable SecOps outcomes.

## Market opportunities by buyer segment
| Segment | Typical size | Buying triggers | Budget anchor |
| --- | --- | --- | --- |
| Micro | 1 to 25 employees | Compliance request, insurer mandate | 10 to 20 percent of IT spend |
| Small | 25 to 100 employees | Ransomware fear, IT gaps | 12 to 25 percent of IT spend |
| SMB | 100 to 500 employees | Audit readiness, vendor risk | 15 to 30 percent of IT spend |
| Mid-market | 500 to 2,000 employees | SOC maturity, executive oversight | 20 to 35 percent of IT spend |
| Enterprise | 2,000 plus employees | Global coverage and SLA requirements | 20 to 40 percent of IT spend |

## Core SecOps service lines
- SOC maturity assessment and gap analysis.
- SOC process mapping and triage redesign.
- SIEM tool selection and architecture design.
- SIEM implementation and log source onboarding.
- SIEM migration and modernization programs.
- Detection engineering and use case lifecycle management.
- SOAR integration and automation playbook development.
- Threat hunting program design and enablement.
- Incident response playbooks and tabletop exercises.
- Metrics dashboards and KPI reporting frameworks.
- SOC staffing and coverage analysis.
- Managed SOC or SOCaaS transition planning.
- CTI integration into SOC workflows.
- OT SOC integration and specialized monitoring support.

## Engagement delivery model
- Phase 1: Discovery and baseline assessment, typically 2 to 4 weeks.
- Phase 2: Design and process alignment, typically 3 to 6 weeks.
- Phase 3: Implementation and enablement, typically 6 to 12 weeks.
- Phase 4: Continuous improvement, delivered via retainers or quarterly reviews.

## SOC optimization blueprint

### Objectives
- Reduce false positives and alert fatigue.
- Improve MTTD and MTTR with measurable targets.
- Standardize triage, escalation, and documentation.
- Align detection coverage to critical business risks.
- Improve analyst experience and retention.

### Assessment focus areas
- Alert volume and severity distribution.
- Top noise sources and duplicate alerts.
- Triage workflow and escalation paths.
- Staffing ratios and shift coverage.
- Tool integration gaps and data handoffs.
- Use case coverage aligned to MITRE ATT&CK.
- Evidence collection and case management workflows.
- Training coverage and onboarding effectiveness.

### Process improvements
- Standardize incident categories and severity matrix.
- Define entry and exit criteria for cases.
- Establish escalation rules and handoff procedures.
- Map SOC workflows to ITSM ticketing processes.
- Implement follow-the-sun handoffs for global teams.
- Introduce service management reporting cadences.

### People and staffing improvements
- Clarify L1, L2, L3 responsibilities and escalation.
- Define SOC lead and SOC manager ownership.
- Create training plans for detection engineering and tooling.
- Implement mentoring and on-call rotation guidelines.
- Develop analyst performance metrics tied to quality.

### Technology improvements
- Rationalize log sources to reduce noise and cost.
- Tune SIEM correlation rules and thresholds.
- Integrate EDR telemetry with SIEM context.
- Implement SOAR for low-risk automation first.
- Build unified dashboards with case visibility.

### Typical SOC optimization deliverables
- SOC maturity assessment report and gap analysis.
- SOC process maps for triage and escalation.
- Updated severity matrix and decision trees.
- Incident response playbooks and runbooks.
- Metrics dashboard and KPI framework.
- Staffing analysis and coverage recommendations.
- Training plan for analysts and SOC leads.

### Common SOC gaps observed
- Excessive alert noise without tuning ownership.
- Inconsistent severity and response thresholds.
- Missing escalation paths and unclear ownership.
- Poor integration between SIEM and ticketing systems.
- Lack of standardized playbooks and runbooks.
- Minimal measurement of MTTD and MTTR trends.

### Optimization levers
- Data reduction and field filtering for noisy sources.
- Tiered triage workflows with automation for enrichment.
- Use case prioritization based on business impact.
- Continuous review of false positive drivers.
- Analyst feedback loops into detection engineering.

## SOC maturity model
- Level 1: Ad hoc monitoring and reactive response.
- Level 2: Repeatable workflows with inconsistent enforcement.
- Level 3: Defined processes with standardized triage.
- Level 4: Managed operations with metrics and governance.
- Level 5: Optimized SOC with automation and continuous feedback.

## Metrics and reporting framework
- Alerts per day by source and severity.
- False positive rate by rule and log source.
- MTTD trendlines by incident category.
- MTTR trendlines by incident category.
- Analyst workload distribution and backlog metrics.
- Incident volume by business impact.
- Coverage map for top MITRE ATT&CK techniques.
- Automation success rate and exception volume.

## SIEM program playbook

### SIEM selection and architecture design
- Document functional and non-functional requirements.
- Define log volume and retention needs.
- Score vendors against integration and cost constraints.
- Run proof of concept with high-value log sources.
- Deliver a tool selection matrix and roadmap.

### SIEM implementation and onboarding
- Prioritize high-value log sources first.
- Normalize fields to the chosen data model.
- Establish data quality checks and parsing validation.
- Create initial detection content and alert routing.
- Document integrations and knowledge transfer.

### SIEM migration and modernization
- Inventory current detection content and dependencies.
- Map field transformations between platforms.
- Re-implement alerts and validate output.
- Run parallel operation phases before cutover.
- Plan migration waves by source category or business unit.

### SIEM health check focus areas
- Log source inventory and gap analysis.
- Detection rule efficacy and false positive review.
- Data ingestion cost and storage optimization.
- Dashboard performance and query efficiency.
- Incident workflow alignment with SIEM alerts.

## Detection engineering and QA
- Treat detection engineering as a product practice.
- Maintain a detection backlog with owners and priorities.
- Use version control for detection-as-code artifacts.
- Align detections to MITRE ATT&CK coverage.
- Create staging environments for new content.
- Validate against simulated logs or historical replays.
- Track false positive rates and tuning outcomes.
- Document detection logic and business rationale.
- Establish review gates for production deployment.

## SOAR implementation playbook

### SOAR readiness criteria
- Clear incident categories and response thresholds.
- Defined system of record for cases and evidence.
- Stable SIEM alert taxonomy with ownership.
- Stakeholder approval for automated actions.
- Logging and audit trails for automated workflows.

### Use case selection
- Start with low-risk enrichment and notification tasks.
- Prioritize high-volume repetitive analyst actions.
- Target use cases with strong data quality.
- Avoid automation of high-impact actions early.

### Playbook design steps
- Map manual steps and decision points.
- Identify integration points for data enrichment.
- Define success criteria and exception handling.
- Include escalation paths and manual overrides.
- Document rollback procedures for automated actions.

### Automation guardrails
- Require approvals for destructive actions.
- Log every automated action and outcome.
- Implement timeouts and kill-switch procedures.
- Track automation errors and manual rework rates.

### Testing and validation
- Use simulated incidents for playbook testing.
- Validate data mappings and field normalization.
- Test edge cases and partial data scenarios.
- Monitor post-deployment performance metrics.

### SOAR outcome metrics
- Reduction in manual triage time.
- Mean time saved per playbook execution.
- Automation success rate and failure rate.
- Analyst satisfaction with automated workflows.

## Toolchain integration map
- Telemetry sources include endpoints, identity, cloud, network, and SaaS logs.
- SIEM aggregates logs and normalizes fields for correlation.
- SOAR automates enrichment and response workflows.
- EDR provides host context and response actions.
- CSPM feeds cloud misconfiguration findings into SOC.
- ITSM handles case management and change workflows.
- Dashboards provide executive and analyst reporting views.

## Tool landscape

### SIEM platforms referenced in internal research
- Splunk
- Microsoft Sentinel
- IBM QRadar
- Elastic Stack
- LogRhythm
- Sumo Logic
- Devo
- Exabeam

### SOAR platforms referenced in internal research
- Cortex XSOAR
- SOAR platforms integrated via playbooks and API workflows

### Adjacent tooling commonly integrated with SOC
- EDR and XDR platforms for endpoint telemetry and response.
- Identity providers for authentication and session context.
- CSPM for cloud configuration and risk findings.
- Ticketing and ITSM tools for case workflows.
- Threat intelligence platforms for IOC enrichment.

## Rate benchmarks and pricing bands

### United States (USD)
- SIEM Analyst or SOC Analyst L1 or L2: 90 to 160 per hour; day rate 700 to 1,200.
- Senior SIEM Analyst or Detection Engineer: 140 to 230 per hour; day rate 1,100 to 1,800.
- SIEM Engineer or Content Engineer: 150 to 260 per hour; day rate 1,200 to 2,000.
- SIEM Architect or Security Data Architect: 200 to 350 per hour; day rate 1,600 to 2,800.
- SOC Manager or SOC Lead Consultant: 180 to 320 per hour; day rate 1,400 to 2,500.
- Threat Hunter or Detection Strategy Consultant: 180 to 340 per hour; day rate 1,500 to 2,600.
- Incident Response Consultant with SIEM focus: 200 to 400 per hour; day rate 1,600 to 3,200.

### Canada (CAD)
- SIEM Analyst or SOC Analyst: 95 to 170 per hour; day rate 750 to 1,300.
- Senior SIEM Analyst or Detection Engineer: 140 to 230 per hour; day rate 1,100 to 1,800.
- SIEM Architect or SOC Lead: 200 to 320 per hour; day rate 1,600 to 2,500.

### United Kingdom (GBP)
- SIEM Analyst or SOC Analyst: 55 to 95 per hour; day rate 450 to 750.
- Senior SIEM Analyst or Detection Engineer: 85 to 140 per hour; day rate 650 to 1,100.
- SIEM Architect or SOC Lead: 120 to 200 per hour; day rate 900 to 1,600.

### Western Europe (EUR)
- SIEM Analyst or SOC Analyst: 60 to 100 per hour; day rate 480 to 800.
- Senior SIEM Analyst or Detection Engineer: 90 to 150 per hour; day rate 700 to 1,200.
- SIEM Architect or SOC Lead: 130 to 220 per hour; day rate 1,000 to 1,700.

### Eastern Europe (EUR)
- SIEM Analyst or SOC Analyst: 35 to 70 per hour; day rate 280 to 560.
- Senior SIEM Analyst or Detection Engineer: 60 to 120 per hour; day rate 480 to 900.
- SIEM Architect or SOC Lead: 90 to 160 per hour; day rate 720 to 1,200.

### Australia and New Zealand (AUD or NZD)
- SIEM Analyst or SOC Analyst: 110 to 190 per hour; day rate 900 to 1,500.
- Senior SIEM Analyst or Detection Engineer: 160 to 260 per hour; day rate 1,300 to 2,100.
- SIEM Architect or SOC Lead: 220 to 340 per hour; day rate 1,800 to 2,700.

### Middle East (USD equivalent)
- SIEM Analyst or SOC Analyst: 80 to 140 per hour; day rate 650 to 1,100.
- Senior SIEM Analyst or Detection Engineer: 120 to 210 per hour; day rate 950 to 1,650.
- SIEM Architect or SOC Lead: 180 to 300 per hour; day rate 1,400 to 2,400.

### Latin America (USD equivalent)
- SIEM Analyst or SOC Analyst: 35 to 80 per hour; day rate 280 to 650.
- Senior SIEM Analyst or Detection Engineer: 70 to 130 per hour; day rate 560 to 1,050.
- SIEM Architect or SOC Lead: 110 to 200 per hour; day rate 850 to 1,600.

### South and Southeast Asia (USD equivalent)
- SIEM Analyst or SOC Analyst: 25 to 70 per hour; day rate 200 to 560.
- Senior SIEM Analyst or Detection Engineer: 60 to 120 per hour; day rate 480 to 950.
- SIEM Architect or SOC Lead: 100 to 180 per hour; day rate 800 to 1,450.

### SOC optimization pricing bands
- Mid-sized SOC assessment: 20,000 to 60,000 USD.
- Full SOC optimization program: 80,000 to 250,000 USD.
- Large global SOC transformation: 500,000 USD or more.

### SIEM implementation pricing bands
- Small implementation with 10 to 20 log sources: 30,000 to 100,000 USD.
- Mid-sized implementation with 20 to 50 log sources: 100,000 to 250,000 USD.
- Large enterprise implementation or migration: 500,000 USD or more.

### Enterprise SecOps program budgets
- Multi-region SOC or SIEM programs often exceed 250,000 USD.
- Complex migration and SOAR integration programs can reach 1,000,000 USD or more.

## SOCaaS and managed services pricing signals
- SOCaaS pricing often scales by endpoints, users, or log volume.
- Small organizations often accept bundled rates of 60 to 150 USD per user per month.
- Mid-market security-only spend can range from 10,000 to 75,000 USD per month.
- Enterprise SOCaaS pricing can exceed 100,000 USD per month.
- Onboarding fees commonly run 1 to 3 times the monthly recurring charge.
- Mature MSSPs target gross margins around 45 to 65 percent after tooling costs.

## OT SOC integration considerations
- OT monitoring often requires custom runbooks and vendor coordination.
- SIEM and SOAR integration adds scope and pricing complexity.
- OT SOC integration should prioritize safety impacts and operational continuity.

### Indicative OT consulting rate bands (USD)
- Claroty junior or analyst: 125 to 175 per hour.
- Claroty senior consultant: 200 to 300 per hour.
- Claroty principal or lead: 300 to 425 per hour.
- Nozomi junior or analyst: 120 to 170 per hour.
- Nozomi senior consultant: 190 to 290 per hour.
- Nozomi principal or lead: 290 to 410 per hour.
- Dragos junior or analyst: 150 to 210 per hour.
- Dragos senior consultant: 250 to 350 per hour.
- Dragos principal or lead: 350 to 500 per hour.

### Indicative OT assessment fee bands
- Single-site visibility assessment: 25,000 to 75,000 USD.
- Multi-site baseline program with 3 to 5 sites: 125,000 to 350,000 USD.
- Segmentation design and rollout planning: 75,000 to 250,000 USD.
- Incident response readiness and tabletop: 30,000 to 120,000 USD.

## Rate drivers and premium multipliers
- Platform certification premium for SIEM specialists: 10 to 25 percent.
- Cloud-native SIEM expertise premium: 15 to 35 percent.
- SOAR integration experience premium: 10 to 30 percent.
- Threat hunting and detection content premium: 15 to 40 percent.
- Security clearance premium: 25 to 80 percent.
- SIEM and SOAR platform skill premium: 8 to 12 percent.
- Cloud security skill premium: 15 to 25 percent.
- Incident response skill premium: 10 to 12 percent.
- CISSP certification premium: 10 to 15 percent.
- CISM certification premium: 10 to 12 percent.
- CEH certification premium: 8 to 10 percent.

## Market opportunities and positioning
- SOC optimization for organizations with high alert fatigue and analyst burnout.
- SIEM migration services for cloud adoption or licensing change.
- SOAR automation pilots tied to specific high-volume workflows.
- SOCaaS transition planning for mid-market clients with limited staffing.
- Detection engineering sprints aligned to top threat scenarios.
- CTI integration to improve SOC prioritization and response.
- OT SOC integration for critical infrastructure and safety-driven environments.
- Log cost optimization and retention strategy projects.
- Executive dashboards that link detection outcomes to business risk.

## Business case framing
- Quantify current inefficiency costs such as analyst overtime or incident backlog.
- Model reductions in false positives as reclaimed analyst hours.
- Tie MTTD and MTTR improvements to reduced breach impact.
- Use a simple ROI formula: ROI equals benefit minus cost divided by cost.
- Emphasize compliance readiness and audit evidence production.

## Proposal and SOW structure
- Section 1: Objectives and outcomes with measurable targets.
- Section 2: Scope covering log sources, tooling, and workflows.
- Section 3: Deliverables list and acceptance criteria.
- Section 4: Assumptions and client responsibilities.
- Section 5: Timeline with milestones and review gates.
- Section 6: Pricing model and change control.

## Risk, governance, and change management
- Define ownership for detection rule changes and playbook updates.
- Require approvals for high-impact automation actions.
- Maintain audit trails for automation and response steps.
- Build stakeholder governance and reporting cadence early.
- Plan for training and change management to reduce resistance.

## Appendix A: Sample 12-week SOC optimization roadmap
- Weeks 1 to 2: Baseline metrics, interviews, and process mapping.
- Weeks 3 to 4: Alert triage redesign and severity matrix updates.
- Weeks 5 to 6: Detection tuning for top 20 use cases.
- Weeks 7 to 8: Playbook development and ticketing integration.
- Weeks 9 to 10: Automation pilot using SOAR or scripting.
- Weeks 11 to 12: Training, handoff, and metrics review.

## Appendix B: Sample 6-week SIEM health check plan
- Week 1: Inventory log sources and map critical data flows.
- Week 2: Review detection content and rule efficacy.
- Week 3: Tune top noise-producing rules and adjust severity.
- Week 4: Identify data gaps and ingestion cost drivers.
- Week 5: Implement quick-win detections and dashboards.
- Week 6: Final report with roadmap and recommended next steps.

## Appendix C: Sample deliverables checklist
- SOC maturity assessment report with prioritized recommendations.
- Detection use case catalog mapped to MITRE ATT&CK.
- Data source onboarding plan and inventory.
- Alert tuning log with before and after metrics.
- Incident response playbooks and escalation matrices.
- SOC metrics dashboard template.
- Training materials for analysts and SOC leads.
- SIEM architecture diagram and data flow map.
- SOAR integration design and playbook catalog.

## Appendix D: Sample metrics dashboard items
- Alerts per day by source and severity.
- False positive rate by detection rule.
- MTTD and MTTR trendlines.
- Analyst workload distribution and backlog metrics.
- Incident volume by category and business impact.
- Automation success and exception rates.
- Coverage by top ATT&CK techniques.
- Time to close by incident type.

## Appendix E: Sample SOC assessment questions
- What are the top five log sources by alert volume?
- Which alerts consistently lack response actions?
- How is severity assigned and who owns changes?
- What is the current MTTD and MTTR by incident class?
- How are analyst shifts staffed and covered for PTO?
- Which tools are the system of record for cases?
- How are playbooks stored and updated?
- What proportion of alerts are false positives?
- Which detections map to critical business risks?
- How is threat intelligence integrated into triage?
- What automation exists and where does it fail?
- What data sources are missing or delayed?
- How often are detection rules reviewed?
- What training is provided for new analysts?
- How are incident post-mortems performed?
- What is the escalation path for high-impact incidents?
- How are changes in the environment communicated to SOC?
- What reporting is shared with leadership and how often?
- What SLAs are required by the business or clients?
- What tooling constraints limit response actions?

## Appendix F: Sample SOAR playbook checklist
- Define trigger conditions for the playbook.
- Validate required input fields and data sources.
- Identify enrichment steps and external integrations.
- Determine decision points and human approvals.
- Document automated actions and rollback steps.
- Configure notifications and escalation routing.
- Log outcomes and errors for audit purposes.
- Test playbook with simulated incidents.
- Review results and tune thresholds.
- Establish ownership for ongoing maintenance.

## Appendix G: Detection engineering lifecycle
- Intake detection request and define objective.
- Map required telemetry and data fields.
- Draft detection logic and hypothesis.
- Validate against MITRE ATT&CK mapping.
- Test with sample logs or simulated data.
- Tune thresholds to reduce false positives.
- Deploy to staging and collect feedback.
- Promote to production with change approval.
- Track performance and update documentation.

## Appendix H: Data onboarding checklist
- Confirm log source owner and access rights.
- Document log format and field mapping.
- Validate parsing rules and normalization.
- Define retention and storage class.
- Establish alerting use cases for the source.
- Create dashboards for visibility and QA.
- Monitor ingestion health and parsing errors.

## Appendix I: Stakeholder roles and RACI
- CISO or security executive: sponsor and outcome accountability.
- SOC manager: operational ownership and staffing.
- Detection engineering lead: use case lifecycle ownership.
- SIEM engineer: ingestion and data model management.
- SOAR engineer: automation development and testing.
- ITSM lead: case workflow integration and SLAs.
- Incident response lead: escalation and containment authority.
- Risk or compliance lead: audit requirements and evidence.
- Infrastructure or cloud lead: log source enablement.

## Appendix J: Continuous improvement cadence
- Weekly: rule tuning review and high-noise source analysis.
- Monthly: metrics review and backlog assessment.
- Quarterly: use case coverage refresh and playbook updates.
- Semiannual: tooling roadmap and budget planning.
- Annual: maturity assessment and strategic roadmap refresh.

## Appendix K: Example engagement artifacts
- Current-state SOC process map.
- Target-state SOC operating model diagram.
- Use case coverage heat map.
- Alert tuning tracker with before and after metrics.
- Training plan and enablement schedule.
- Implementation runbook for workflow changes.

## Appendix L: Success criteria examples
- Reduce false positive rate by 30 percent within 60 days.
- Improve MTTD by 25 percent within one quarter.
- Achieve 90 percent playbook adoption for top incidents.
- Decrease analyst backlog by 40 percent within 90 days.
- Increase automation coverage for enrichment tasks to 60 percent.
