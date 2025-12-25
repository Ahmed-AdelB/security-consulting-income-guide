# MSP + MSSP Income Research: Managed Security Services & SOC-as-a-Service Pricing

## Scope, methodology, and limitations
This report consolidates practical, vendor-agnostic knowledge about how MSPs (managed service providers) and MSSPs
(managed security service providers) generate income from security services, with a focus on pricing models for
managed security, MDR, and SOC-as-a-Service (SOCaaS). The goal is to provide a structured planning guide for
catalog design, quoting, budgeting, and revenue modeling. It is not a live market survey and does **not** include
real-time vendor quotes, proprietary benchmarks, or contracted pricing. Treat the ranges as indicative planning
estimates and validate with current bids in your geography and segment.

**Important limitation:** the environment used to prepare this report does not allow live web research. The pricing
bands and operating assumptions are synthesized from common industry patterns and should be verified with
competitive quotes, RFP responses, and current reseller licensing terms.

## Executive summary
- Managed security revenue is primarily recurring (MRR/ARR) with high attach rates when bundled with managed IT.
- SOCaaS pricing is commonly driven by endpoints, users, or log ingest volume, with minimum monthly commitments.
- 24x7 coverage, log volume, and response depth are the biggest cost and pricing multipliers.
- Onboarding fees (setup, tuning, onboarding, use case calibration) are often 1–3x monthly recurring fees.
- Gross margins vary widely by scale and automation; mature MSSPs target 45–65% gross margin after tooling costs.
- MDR and SOCaaS services are frequently bundled with EDR/XDR licensing, obscuring pure service costs in quotes.
- Mid-market and regulated buyers prefer clear SLAs, escalation procedures, and quarterly metrics reporting.
- Upsell paths include vCISO, compliance support, security awareness, vulnerability management, and IR retainers.

## Definitions and service taxonomy
### Core acronyms and roles
- **MSP:** Managed Service Provider, typically responsible for IT operations, endpoints, patching, and helpdesk.
- **MSSP:** Managed Security Service Provider, focused on security monitoring, detection, response, and reporting.
- **SOCaaS:** SOC-as-a-Service; outsourced SOC functions (monitoring, triage, and escalation) delivered as a service.
- **MDR:** Managed Detection and Response; combines EDR/XDR tooling with human monitoring and response.
- **SIEM:** Security Information and Event Management; log collection, normalization, correlation, and alerting.
- **SOAR:** Security Orchestration, Automation, and Response; workflow automation and response playbooks.
- **EDR/XDR:** Endpoint/extended detection and response; telemetry and response from endpoints and beyond.
- **NDR:** Network Detection and Response; network-level telemetry and anomaly detection.
- **vCISO:** Virtual CISO service offering governance, risk, and compliance leadership on a retainer.

### Service families
- **Monitoring and alert triage:** continuous alert detection and prioritization.
- **Detection engineering:** rule tuning, content development, and ongoing use case refinement.
- **Incident response orchestration:** containment, response coordination, and post-incident reporting.
- **Managed endpoint security:** deployment and tuning of EDR/XDR, anti-malware, and host firewalls.
- **Managed network security:** firewall, IDS/IPS, VPN, and network segmentation management.
- **Cloud security management:** CSPM, cloud log monitoring, and security policy governance.
- **Vulnerability management:** scanning, prioritization, remediation tracking, and reporting.
- **Compliance support:** evidence collection, audit prep, and policy assistance.

## Market landscape and demand drivers
Security budgets continue to rise due to high ransomware incidence, cyber insurance requirements, regulatory
pressure, and board-level awareness. Buyers increasingly prefer managed services because in-house SOC operations
are expensive to build and difficult to staff. Several forces shape pricing and income models:

- **Regulatory pressure:** SOC 2, ISO 27001, HIPAA, PCI DSS, and GDPR create ongoing demand for monitoring.
- **Insurance mandates:** cyber insurers demand stronger controls, MFA coverage, logging, and incident response.
- **Cloud adoption:** distributed systems increase log volume, asset complexity, and need for continuous monitoring.
- **Talent shortages:** analysts and detection engineers are expensive, raising the cost of 24x7 coverage.
- **Convergence of IT and security:** MSPs move upstream into security to increase ARPU and retention.

## Buyer segments and budget anchors
Pricing expectations change dramatically by client size, complexity, and risk. Typical buyer personas:

| Segment | Typical size | Buying triggers | Budget anchor (security portion of IT) | Common contract shape |
| --- | --- | --- | --- | --- |
| Micro | 1–25 employees | Compliance check, insurer request | 10–20% of IT spend | Bundled per-user plan |
| Small | 25–100 employees | Ransomware fears, IT gaps | 12–25% of IT spend | Per-user or per-endpoint |
| SMB | 100–500 employees | Audit readiness, vendor risk | 15–30% of IT spend | MRR + onboarding |
| Mid-market | 500–2,000 employees | SOC maturity, executive oversight | 20–35% of IT spend | Multi-year MRR |
| Enterprise | 2,000+ employees | Global coverage and SLA | 20–40% of IT spend | Multi-vendor, SLAs |

**Budget anchors (indicative):**
- Small organizations often accept bundled “IT + security” rates of $60–$150 per user/month.
- Mid-market orgs frequently see security-only spend of $10k–$75k/month depending on scope and log volume.
- Enterprise SOCaaS pricing can exceed $100k/month for multi-region, high-ingest monitoring.

## Income streams for MSPs and MSSPs
Managed security income usually combines recurring service revenue with high-margin project add-ons.

**Recurring revenue streams**
- 24x7 monitoring and incident triage.
- MDR/EDR management with response.
- SIEM management and log retention.
- Managed firewall and network security services.
- Managed vulnerability scanning and remediation tracking.
- Cloud security monitoring and configuration management.

**Project and advisory revenue streams**
- Incident response retainers and per-incident surcharges.
- Security assessments, gap analysis, and roadmap services.
- Compliance preparation and policy creation.
- Penetration testing, tabletop exercises, and red teaming.
- Security awareness programs and phishing simulations.
- vCISO/virtual security leadership retainers.

**Resale and platform revenue streams**
- Margin on licenses (EDR, SIEM, email security, backup).
- Professional services for deployment, migration, and configuration.
- Usage-based overages for log ingestion or storage.

## Managed security service catalog (what buyers actually purchase)
The following catalog maps typical security services to deliverables and pricing metrics.

### 1) SOC monitoring and alert triage
**Deliverables:** continuous monitoring of security events, alert triage, escalation of confirmed incidents,
and monthly reporting. **Pricing metrics:** endpoints, log volume, hours of coverage (8x5 vs 24x7).

### 2) Managed detection and response (MDR)
**Deliverables:** EDR deployment, alert tuning, managed response actions (isolation, kill process), and response
coordination. **Pricing metrics:** endpoints, severity of response obligations, EDR license included or not.

### 3) SIEM management and log retention
**Deliverables:** log source onboarding, parsing, correlation rules, retention policies, and data governance.
**Pricing metrics:** GB/day ingest, total retention, number of log sources.

### 4) Threat hunting
**Deliverables:** proactive searches for threats, hypothesis-based hunts, and report-out. **Pricing metrics:**
hours per month or included in higher-tier SOC packages.

### 5) Managed vulnerability management
**Deliverables:** scanning schedules, prioritization, remediation tracking, ticketing integration, and reporting.
**Pricing metrics:** number of assets, scan frequency, vulnerability backlog.

### 6) Managed patch management
**Deliverables:** patch cadence, change windows, rollback testing, and compliance reporting. **Pricing metrics:**
endpoints, servers, maintenance windows.

### 7) Managed firewall and network security
**Deliverables:** rule management, change control, VPN management, and monitoring. **Pricing metrics:** number of
firewalls, sites, rules change rate, bandwidth.

### 8) Managed email security
**Deliverables:** spam/phish filtering, DMARC/DKIM tuning, suspicious email remediation. **Pricing metrics:**
mailboxes or users, inbound message volume.

### 9) Cloud security monitoring (AWS/Azure/GCP)
**Deliverables:** CSPM, cloud log monitoring, IAM posture review, and threat detection. **Pricing metrics:**
cloud accounts, services enabled, log volume.

### 10) Identity security and MFA monitoring
**Deliverables:** identity hygiene, MFA enforcement reporting, risky sign-in alerts. **Pricing metrics:** users
and identity providers.

### 11) Data loss prevention and backup/DR
**Deliverables:** DLP policies, data classification, backup monitoring, recovery testing. **Pricing metrics:**
data volume, protected endpoints, retention period.

### 12) Compliance support and reporting
**Deliverables:** control mapping, evidence collection, reporting for audits. **Pricing metrics:** scope size,
number of frameworks, hours per month.

### 13) Incident response retainers
**Deliverables:** guaranteed response hours, playbooks, incident war-room support. **Pricing metrics:** annual
retainer plus hourly response rates.

### 14) Security awareness and training
**Deliverables:** monthly training, phishing simulations, reporting. **Pricing metrics:** per user/month.

## SOC-as-a-Service (SOCaaS) deep dive
SOCaaS is the most visible MSSP product and the core income engine for many providers.

### Core SOC functions
- **Telemetry ingestion:** log collection from endpoints, identity, cloud, network, and SaaS.
- **Detection engineering:** tuning and developing alert use cases and correlation rules.
- **Alert triage:** severity scoring, false-positive reduction, and escalation.
- **Incident response coordination:** containment steps, client communication, and documentation.
- **Threat intelligence integration:** IOC feeds and contextual enrichment.
- **Reporting and governance:** dashboards, KPIs, and executive reporting.

### SOC delivery models
- **8x5 SOC:** business-hours monitoring; lower cost, slower response outside hours.
- **12x5/16x5 SOC:** extended coverage to reduce gap in evenings/weekends.
- **24x7 SOC:** full coverage; highest cost, required for regulated or global clients.
- **Hybrid SOC:** tier-1 coverage with escalation to on-call or client staff.

### Staffing and coverage mathematics
SOC coverage is a major cost driver. A 24x7 seat requires approximately 4.2–5.0 FTEs to cover
vacation, sick leave, training, and shift rotation. Analyst-to-endpoint ratios vary by alert quality
and automation maturity. Typical planning heuristics:

- **Tier 1 analyst:** 1 analyst per 500–1,500 endpoints depending on alert volume.
- **Tier 2 analyst:** 1 analyst per 2,000–5,000 endpoints for escalations and investigations.
- **Detection engineer:** 1 engineer per 20,000–60,000 endpoints or per 50–150 clients.
- **SOC manager:** 1 manager per 8–12 analysts.

These ratios are approximate and improve significantly with automation, better log hygiene, and mature
detection content.

### SOC onboarding stages (typical)
1. **Discovery and scoping:** assets, log sources, risk appetite, and escalation contacts.
2. **Log source onboarding:** endpoint, cloud, identity, network devices, and SaaS integrations.
3. **Parsing and normalization:** ensure logs are normalized and searchable.
4. **Use-case calibration:** enabling baseline detections and tuning false positives.
5. **Escalation workflows:** ticketing integration and response playbooks.
6. **Go-live and stabilization:** 30–90 days of tuning and reporting.

### SOC SLAs and response obligations
- **MTTD (mean time to detect):** target 5–60 minutes depending on tier.
- **MTTA (mean time to acknowledge):** target 15–60 minutes for critical alerts.
- **MTTR (mean time to respond):** target 1–24 hours depending on severity and scope.
- **Critical alert escalation:** 15–30 minutes for 24x7 tiers, 1–4 hours for 8x5 tiers.

### SOC reporting expectations
- Monthly executive summary (top incidents, trends, coverage).
- SLA metrics and response timelines.
- Detections by category and false positive rates.
- Vulnerability and patch posture (if included).
- Improvement plan and tuning backlog.

### Common SOCaaS pricing mechanics
- **Per endpoint per month:** easy to sell; common for MDR + SOC bundles.
- **Per user per month:** common when identity and email monitoring are central.
- **Per GB/day ingest:** common when SIEM licensing is the dominant cost.
- **Tiered packages:** defined by log sources, response depth, and coverage hours.
- **Minimum monthly fee:** protects the provider against low-volume clients.

## Pricing models and rate drivers
### Common pricing constructs
- **MRR/ARR contracts:** typical for SOCaaS and MDR.
- **Onboarding/setup fees:** log source onboarding, detection engineering, playbook development.
- **Overage fees:** when log volume or endpoints exceed contracted limits.
- **Add-on retainers:** vCISO, compliance, IR response hours.
- **Project-based pricing:** incident response, assessments, and migration.

### Primary rate drivers
- **Coverage hours:** 24x7 can cost 2–4x more than 8x5 coverage.
- **Log volume:** SIEM licensing is often driven by GB/day ingest.
- **Endpoint types:** servers and high-value assets cost more than laptops.
- **Response depth:** containment actions raise price compared to pure monitoring.
- **Sector risk:** healthcare, fintech, and critical infrastructure command premium rates.
- **Geography and data residency:** multi-region monitoring increases cost.
- **Integration complexity:** number of log sources and custom parsers.
- **Client maturity:** poor log hygiene and high false positives drive cost.

## Indicative pricing ranges (USD-equivalent)
**Reminder:** These are planning ranges, not live quotes. Confirm with local bids.

### Endpoint/user-based SOC and MDR services
| Service | Metric | Indicative range | Notes |
| --- | --- | --- | --- |
| Basic SOC monitoring (8x5) | per endpoint/month | $8–$20 | Monitoring + alert triage only |
| 24x7 SOC monitoring | per endpoint/month | $20–$60 | Full coverage with escalation |
| MDR (EDR + response) | per endpoint/month | $30–$120 | Often includes EDR licensing |
| Server endpoint premium | multiplier | 1.5x–4x | Higher risk and log volume |
| Per user SOC coverage | per user/month | $10–$35 | Common for identity-heavy scopes |
| Email security management | per mailbox/month | $2–$8 | Often bundled with identity |
| Security awareness training | per user/month | $1–$6 | Often sold as add-on |
| Managed vulnerability scanning | per asset/month | $5–$20 | Depends on scan cadence |
| Managed patching | per endpoint/month | $6–$20 | Often bundled with MSP services |
| vCISO retainer | per month | $3,000–$20,000 | Based on hours and scope |

### Log ingestion and SIEM-driven pricing
| Ingest model | Indicative range | Notes |
| --- | --- | --- |
| SIEM licensing (baseline) | $0.10–$0.50 per GB | Licensing-only component |
| SOCaaS add-on per GB/day | $2–$10 per GB/day | SOC analysis + response |
| High-volume ingest discount | 20–60% lower | Volume-based discounts |
| Retention storage | $0.02–$0.15 per GB/month | Varies by hot vs cold storage |

### Network, cloud, and infrastructure pricing
| Service | Metric | Indicative range | Notes |
| --- | --- | --- | --- |
| Managed firewall | per device/month | $150–$600 | Higher for HA or complex sites |
| IDS/IPS monitoring | per device/month | $150–$500 | Often tied to firewall |
| Cloud account monitoring | per account/month | $300–$1,500 | Depends on log volume |
| Cloud workload monitoring | per workload/month | $15–$60 | For VM/container monitoring |
| Backup monitoring | per endpoint/month | $5–$15 | Often combined with DR |

### Setup, onboarding, and project services
| Service | Indicative range | Notes |
| --- | --- | --- |
| SOCaaS onboarding | $2,000–$25,000 | Scope and log sources drive cost |
| MDR onboarding | $1,000–$10,000 | Includes EDR deployment |
| SIEM integration | $5,000–$50,000 | Parsing and rule tuning |
| Incident response retainer | $5,000–$100,000 per year | Includes pre-paid hours |
| Penetration test | $8,000–$60,000 | Based on scope and complexity |

## SOCaaS package examples (illustrative)
| Package | Coverage | Typical inclusions | Indicative monthly range |
| --- | --- | --- | --- |
| Essential SOC | 8x5 | Monitoring + triage + monthly report | $1,500–$8,000 |
| Growth SOC | 16x5/24x5 | Monitoring + triage + response guidance | $5,000–$20,000 |
| Enterprise SOC | 24x7 | Full monitoring + response + hunt | $15,000–$100,000+ |

**Notes:** package pricing typically scales with endpoints or log volume. Contracts usually include minimums
and overage thresholds (e.g., included 100 GB/day, overage billed per GB/day).

## MSP + MSSP income stacking strategies
MSPs often increase security revenue by bundling, tiering, and upselling security capabilities:

- **Bundle security into per-user managed IT plans** (easier buying decision, higher retention).
- **Offer tiered packages** (Essential, Professional, Elite) with clear incremental outcomes.
- **Create response-based upgrades** (monitoring-only vs managed response).
- **Leverage compliance-driven upsells** (SOC 2 readiness, HIPAA, PCI, or ISO).

### Example bundled pricing ladder (per user/month, indicative)
| Tier | Managed IT | Security inclusions | Indicative range |
| --- | --- | --- | --- |
| IT Core | Helpdesk, patching, backup | Basic AV, MFA policy | $60–$110 |
| IT + Security | IT Core + SOC monitoring | EDR, email security, security reports | $120–$220 |
| IT + Advanced Security | IT + Security | MDR + threat hunting + vCISO hours | $200–$350 |

## Revenue modeling framework
Use a consistent model to estimate income and margin. Core formulas:

- **MRR** = (Endpoints × Endpoint Rate) + (Users × User Rate) + Add-on retainers + Overage fees
- **ARR** = MRR × 12
- **Gross margin** = (Revenue − COGS) ÷ Revenue
- **COGS per endpoint** = (Analyst labor + tooling + infrastructure) ÷ monitored endpoints
- **Break-even endpoints** = Fixed costs ÷ (Price per endpoint − Variable cost per endpoint)

### Scenario A: Small MSP launching SOCaaS
**Assumptions (illustrative):**
- 20 clients, average 40 endpoints each = 800 endpoints
- SOC monitoring price: $28 per endpoint/month
- Add-ons: $4,000 monthly (vulnerability management and training)
- Onboarding: $1,500 per client average

**Revenue estimate:**
- Endpoint MRR = 800 × $28 = $22,400
- Add-on MRR = $4,000
- Total MRR = $26,400 (ARR = $316,800)
- Onboarding revenue = 20 × $1,500 = $30,000 one-time

### Scenario B: Growth-stage MSSP
**Assumptions (illustrative):**
- 75 clients, average 150 endpoints each = 11,250 endpoints
- SOC/MDR blended price: $45 per endpoint/month
- Log volume overage: $12,000 monthly
- vCISO retainers: 10 clients × $6,000 = $60,000 monthly

**Revenue estimate:**
- Endpoint MRR = 11,250 × $45 = $506,250
- Overage MRR = $12,000
- vCISO MRR = $60,000
- Total MRR = $578,250 (ARR = $6.94M)

### Scenario C: Mature MSSP with enterprise clients
**Assumptions (illustrative):**
- 12 enterprise clients averaging 8,000 endpoints each = 96,000 endpoints
- Weighted rate: $35 per endpoint/month (volume discount)
- Dedicated IR retainers: $300,000/year
- Cloud monitoring add-ons: $40,000/month

**Revenue estimate:**
- Endpoint MRR = 96,000 × $35 = $3.36M
- Cloud add-ons = $40,000
- Total MRR = $3.4M (ARR = $40.8M)
- IR retainer adds $300,000 annual

## Cost structure and margin expectations
MSSP cost structures are dominated by labor and tooling. Indicative cost distribution (varies by scale):

- **SOC labor:** 35–55% of revenue (analysts, managers, detection engineers)
- **Tooling and licenses:** 15–30% (SIEM, EDR, SOAR, TI feeds)
- **Cloud and storage:** 5–15% (log storage, compute)
- **Sales and marketing:** 6–15% (CAC, channel fees)
- **G&A and compliance:** 4–10% (insurance, legal, audits)

**Margin expectations (indicative):**
- Early-stage MSSP: 20–40% gross margin (heavy onboarding and tooling costs)
- Mature MSSP: 45–65% gross margin with automation and scale
- Best-in-class: 60–70% gross margin with optimized detection and low alert volume

## Sales motion and contracting
Typical sales lifecycle:
1. **Discovery and scoping:** identify assets, log sources, response expectations, and compliance drivers.
2. **Technical assessment:** log inventory, architecture review, and data ingestion estimate.
3. **Proposal:** package options, SLA, onboarding timeline, and pricing.
4. **Pilot or limited rollout:** 30–90 day pilot to validate data quality.
5. **Full rollout:** SOC go-live and ongoing reporting.

Key contract elements:
- Scope of monitoring and response actions (monitoring-only vs containment).
- Data retention requirements and log ingestion limits.
- SLA terms for alert acknowledgement and escalation.
- Liability limitations and customer responsibilities.
- Change control and new log source onboarding terms.

## KPI dashboard for MSSP income management
- **MRR / ARR:** recurring revenue growth and churn.
- **ARPA (average revenue per account):** indicator of upsell effectiveness.
- **Gross margin %:** core profitability indicator.
- **Endpoint coverage:** total endpoints under management.
- **Alert volume per endpoint:** drives analyst efficiency.
- **MTTD / MTTA / MTTR:** operational effectiveness.
- **False positive rate:** detection quality metric.
- **Retention and churn:** service stickiness and renewal health.
- **Onboarding cycle time:** speed to revenue realization.

## SOCaaS delivery stack (reference architecture)
Most SOCaaS offerings require a minimum technical stack. Common components:

- **Log collection:** agents, syslog, cloud API collectors.
- **SIEM:** correlation, alerting, search, and storage.
- **EDR/XDR:** endpoint telemetry and response actions.
- **SOAR:** workflow automation and response playbooks.
- **Ticketing:** incident tracking and escalation.
- **Threat intelligence:** feeds, reputational scoring, enrichment.
- **Reporting:** dashboards, KPIs, compliance reporting.

## Pricing workbook: quote construction checklist
Use a consistent quoting checklist to avoid margin erosion:

1. Asset inventory: endpoints, servers, cloud accounts, and critical apps.
2. Log source estimate: GB/day by source (endpoint, identity, network, cloud).
3. Coverage requirement: 8x5, 16x5, or 24x7.
4. Response expectations: monitoring-only vs containment actions.
5. Compliance requirements: audit evidence, report cadence, or data residency.
6. Tooling coverage: customer-owned tools vs MSSP-provided tools.
7. Onboarding effort: integration complexity and custom parsers.
8. Reporting cadence: monthly or quarterly reporting and QBRs.
9. SLA requirements: response times and escalation paths.
10. Contract term: 12, 24, 36 months and discounts.

## Use case library (starter set for SOC detection)
This library is a reference list of common detection use cases often bundled into SOCaaS offerings. Providers
should tailor based on client environment and risk profile.

**Identity and access**
- Multiple failed logins followed by success.
- Impossible travel / anomalous sign-in locations.
- MFA bypass or MFA fatigue patterns.
- Privileged role assignments outside change windows.
- New admin accounts created and used immediately.

**Endpoint and host**
- Suspicious PowerShell or script execution.
- Known ransomware file activity or encryption behavior.
- Malware quarantine events and re-infection attempts.
- Registry and persistence changes (Run keys, services).
- Unauthorized local admin creation.

**Network and perimeter**
- Port scans or lateral movement attempts.
- New external connections to unusual geographies.
- DNS tunneling indicators.
- Unusual VPN logins or high-volume data exfil.
- Command and control beaconing patterns.

**Email and collaboration**
- OAuth consent to suspicious third-party apps.
- Mass forwarding rules or mailbox rule changes.
- Phishing email click-through confirmation.
- Login from non-compliant device.

**Cloud and SaaS**
- Public exposure of storage buckets.
- Unusual API calls or privilege escalation.
- Security group changes allowing 0.0.0.0/0 access.
- Creation of new access keys without rotation.
- Excessive data downloads or egress spikes.

## Sample SOC report outline (monthly)
1. Executive summary and risk posture.
2. Notable incidents and response timeline.
3. Alert trends by category and severity.
4. Top threat sources and affected assets.
5. SLA adherence and response metrics.
6. Vulnerability and patch status (if included).
7. Recommended improvements and next steps.

## Common pitfalls and mitigation strategies
- **Underestimating log volume:** perform a 2–4 week log sampling to size ingest.
- **Ignoring onboarding costs:** charge a setup fee to cover detection engineering.
- **Overpromising response:** clearly define the scope of containment actions.
- **Misaligned SLAs:** match response commitments to staffing and coverage.
- **Poor alert hygiene:** tune detection rules to control analyst workload.
- **Tool sprawl:** consolidate security tooling to reduce license overlap.

## Suggested validation sources (for further research)
Use the following to validate and refine price assumptions:

- Competitive bids and RFP responses from regional MSSPs.
- SIEM and MDR vendor pricing calculators (through reseller or partner portals).
- Industry peer groups and MSP associations.
- Salary surveys for SOC analysts and detection engineers.
- Cyber insurance underwriting requirements and security control checklists.
- Cloud provider pricing for log storage and data egress.

## Pricing by organization size and complexity (indicative)
While endpoint and log-volume pricing are standard, many buyers still anchor to a monthly budget range based on
organization size and risk. The table below shows indicative ranges that combine monitoring, response, and
reporting, assuming a mix of endpoint and log-volume pricing. These should be validated with a log sampling
exercise and confirmed RFP bids.

| Segment | Typical endpoints | Typical log ingest | Coverage | Indicative monthly range | Notes |
| --- | --- | --- | --- | --- | --- |
| Micro | 10–50 | 1–5 GB/day | 8x5 | $750–$2,500 | Minimal log sources, limited response |
| Small | 50–150 | 5–15 GB/day | 8x5–16x5 | $2,000–$8,000 | Some identity + email monitoring |
| SMB | 150–500 | 15–40 GB/day | 16x5–24x5 | $8,000–$25,000 | Basic response coverage |
| Mid-market | 500–2,000 | 40–150 GB/day | 24x7 | $25,000–$80,000 | Formal SLA expectations |
| Enterprise | 2,000+ | 150–1,000+ GB/day | 24x7 | $80,000–$250,000+ | Multi-region, tailored SOC |

**How to use this table:** replace the log ingest column with your actual sampling, then adjust upward for higher
risk sectors (finance, healthcare) and downward for lower-criticality use cases (monitoring-only). Many MSSPs
structure pricing as a hybrid: minimum monthly fee + per-GB/day overage.

## Service tier matrix (sample)
Service tiers are a practical way to align pricing and service outcomes.

| Capability | Essential | Advanced | Elite |
| --- | --- | --- | --- |
| Coverage hours | 8x5 | 16x5 or 24x5 | 24x7 |
| Log sources | Endpoint + identity | + network + cloud | + SaaS + OT + custom |
| Response actions | Notify + ticket | Guided containment | Managed containment |
| Threat hunting | Not included | Monthly hunts | Weekly hunts |
| Reporting | Monthly | Monthly + QBR | Monthly + QBR + compliance |
| vCISO hours | Optional add-on | 2–4 hrs/month | 4–10 hrs/month |
| IR retainer | Optional | Included (limited) | Included (priority) |

## SOCaaS cost model and staffing examples
SOCaaS profitability depends on balancing analyst labor and tooling costs against consistent, recurring revenue.
Below is a simplified cost model to help estimate floor pricing:

**Cost per endpoint (simplified):**
1. Estimate total monthly SOC labor cost (analyst + manager + detection engineering).
2. Add monthly tooling cost (SIEM, EDR, SOAR, threat intel, ticketing).
3. Add cloud/storage cost based on ingest.
4. Divide by monitored endpoints to get a baseline COGS per endpoint.
5. Apply target gross margin (e.g., 50%) to set price.

### Example staffing budget (illustrative)
Assume 24x7 coverage for 5,000 endpoints:

| Role | FTEs | Loaded annual cost | Monthly cost |
| --- | --- | --- | --- |
| Tier 1 analysts | 6 | $90,000 | $45,000 |
| Tier 2 analysts | 2 | $115,000 | $19,167 |
| Detection engineer | 1 | $140,000 | $11,667 |
| SOC manager | 1 | $150,000 | $12,500 |
| Total labor | 10 | — | $88,334 |

If tooling and cloud cost adds $30,000/month, total COGS ≈ $118,334/month.
COGS per endpoint ≈ $23.67. With a 50% target margin, price ≈ $47 per endpoint/month.

## Analyst productivity and capacity planning
Analyst capacity is the most important operational variable. Track these metrics to protect margin:

- **Alerts per analyst per shift:** healthy range 10–40, depending on automation.
- **Mean handle time:** typical 20–60 minutes per incident.
- **Escalation ratio:** 5–20% of alerts should become high-severity incidents.
- **False positive rate:** aim for <20% for mature detections.
- **Automation coverage:** 30–70% of alert actions automated in mature SOCs.

### Capacity benchmarks (indicative)
| Metric | Early SOC | Mature SOC | Notes |
| --- | --- | --- | --- |
| Alerts per analyst/day | 40–80 | 15–40 | Lower is better quality |
| Incidents per analyst/day | 4–10 | 2–6 | Depends on severity |
| Ticket closure time | 2–8 hours | 1–4 hours | Influences SLA compliance |
| Automation rate | 10–30% | 40–70% | Reduces staffing needs |

## Log source inventory and ingest estimation checklist
Accurate ingest estimation is essential for pricing and margin. Below is a typical log source inventory to
use during discovery. Not all sources are needed for every client.

**Identity and directory services**
- Active Directory (domain controllers, authentication logs)
- Entra ID/Azure AD sign-in and audit logs
- Okta or other identity provider logs
- MFA provider logs (Duo, Okta Verify, etc.)

**Endpoint and operating system**
- Windows event logs (Security, System, PowerShell)
- Linux syslog and auth logs
- EDR telemetry (process, file, network)
- Host firewall logs

**Network and perimeter**
- Firewalls (Palo Alto, Fortinet, Cisco, etc.)
- IDS/IPS alerts
- VPN gateways and remote access logs
- DNS logs and resolver telemetry
- Web proxy or secure web gateway logs

**Cloud infrastructure**
- AWS CloudTrail, GuardDuty, VPC Flow Logs
- Azure Activity Logs, Defender for Cloud
- GCP Cloud Audit Logs, VPC Flow Logs
- Kubernetes audit logs and container runtime telemetry

**Email and collaboration**
- Microsoft 365 audit logs
- Google Workspace audit logs
- Email gateway logs (Proofpoint, Mimecast, etc.)
- Collaboration platform logs (Teams, Slack, Zoom)

**SaaS and business applications**
- CRM logs (Salesforce, HubSpot)
- ERP logs (NetSuite, SAP)
- HR systems (Workday, BambooHR)
- DevOps tooling (GitHub, GitLab, CI/CD)

**Security tooling**
- Vulnerability scanner logs
- DLP alerts
- Endpoint privilege management logs
- CASB/SSPM alerts

**Data and database sources**
- Database audit logs (SQL Server, PostgreSQL, MySQL)
- Data warehouse access logs
- Storage access logs (S3, Blob, GCS)

### Ingest estimation rules of thumb (rough guidance)
- Identity logs: 0.1–0.5 GB/day per 100 users, depending on sign-in frequency.
- Endpoint logs: 0.2–1.0 GB/day per 100 endpoints with EDR telemetry enabled.
- Firewall logs: 0.5–3 GB/day per firewall, depends on traffic volume.
- Cloud audit logs: 1–10 GB/day per account, heavily dependent on workload.

## Vertical and risk-based pricing modifiers
Risk exposure affects required coverage, SLAs, and compliance reporting. Many MSSPs use multipliers:

| Vertical | Typical pricing modifier | Rationale |
| --- | --- | --- |
| Healthcare | 1.2x–1.5x | PHI exposure, compliance reporting |
| Financial services | 1.3x–1.7x | Regulatory scrutiny and fraud risk |
| Government/critical infra | 1.2x–1.6x | High availability and SLA demands |
| SaaS B2B | 1.0x–1.3x | SOC 2 and vendor risk drivers |
| Retail/e-commerce | 1.0x–1.2x | PCI and fraud exposure |
| Manufacturing/OT | 1.1x–1.4x | OT logs and availability risks |

## Add-on modules and upsell pricing bands (indicative)
| Add-on module | Typical pricing | Notes |
| --- | --- | --- |
| Threat hunting | $1,000–$12,000/month | Based on frequency and scope |
| IR retainer | $5,000–$100,000/year | Includes reserved response hours |
| vCISO | $3,000–$20,000/month | Strategic leadership and compliance |
| Compliance reporting | $1,000–$10,000/month | SOC 2, ISO, HIPAA, PCI |
| Security awareness | $1–$6 per user/month | Includes phishing simulations |
| Penetration testing | $8,000–$60,000/project | Scope drives cost |
| Purple team exercise | $15,000–$120,000 | Combined red/blue exercises |
| Tabletop exercise | $3,000–$25,000 | Incident response readiness |

## Channel, reseller, and wholesale pricing considerations
Many MSSPs rely on channel partners and MSPs to deliver services to SMB clients. This introduces a wholesale
price band and reseller margin requirement. Common patterns include:

- **Wholesale SOCaaS:** MSSP sells to MSP at 20–40% discount from retail.
- **Co-managed SOC:** MSP retains tier-1 support, MSSP handles escalation.
- **White-label pricing:** MSSP provides SOCaaS under MSP branding, often with minimums.
- **Margin preservation:** MSP aims for 25–50% gross margin on top of MSSP wholesale.

## Sample Statement of Work (SOW) outline
1. Scope of monitoring and response services.
2. Assets and log sources in scope.
3. Coverage hours and shift definitions.
4. SLA targets (MTTD, MTTA, MTTR).
5. Alert classification and severity matrix.
6. Escalation paths and escalation contacts.
7. Response actions permitted (containment, isolation).
8. Tooling responsibilities (client vs MSSP).
9. Data retention and storage commitments.
10. Reporting cadence and deliverables.
11. Change control and onboarding of new log sources.
12. Incident response retainer terms (if applicable).
13. Customer responsibilities and required controls.
14. Service exclusions and liability limitations.
15. Contract term, renewals, and termination clauses.

## SLA and escalation definitions (template)
- **Severity 1:** confirmed active compromise; response within 15–30 minutes.
- **Severity 2:** probable compromise; response within 1–2 hours.
- **Severity 3:** suspicious activity; response within 4–8 hours.
- **Severity 4:** low-risk alerts; response within 1–3 business days.
- **Escalation channels:** phone, secure chat, and ticketing escalation.

## RFP question bank (selection)
- Describe your SOC coverage model and analyst staffing ratios.
- Which log sources are included in the base package?
- How do you handle log source onboarding and parsing?
- Provide sample SLAs and escalation timelines.
- Explain your false positive tuning process.
- Describe your response actions and containment authority.
- Provide a list of supported EDR and SIEM platforms.
- How do you handle data residency and retention requirements?
- What is your typical onboarding timeline and milestones?
- Do you provide threat hunting, and how often?
- What reports are delivered monthly and quarterly?
- Explain how you manage incident response retainers.
- Describe how you support compliance reporting (SOC 2, ISO, PCI).
- Provide references for organizations of similar size and sector.
- How do you price overages for log ingest or endpoint growth?
- What is your process for rule tuning and detection engineering?
- How do you manage shift handoffs and follow-the-sun operations?
- Describe your escalation path if a client is unreachable.
- What is your average MTTD and MTTR for critical incidents?
- Provide your analyst-to-endpoint coverage ratios.
- How do you support ransomware response?
- What is your approach to insider threat detection?
- Do you integrate with our ticketing system (ServiceNow, Jira)?
- How are alerts prioritized and classified?
- How do you provide forensic evidence preservation?
- Explain your incident post-mortem process.
- What is your onboarding fee and what does it include?
- How do you handle customer-managed tools vs MSSP tools?
- What is your process for vulnerability management integration?
- Do you provide 24x7 phone escalation for critical incidents?
- How do you measure SOC performance and quality?
- What compliance certifications do you hold (SOC 2, ISO)?
- Can you provide a list of standard detection use cases?
- How do you handle alert noise from legacy systems?
- What is your policy for subcontractors and third-party access?
- Describe your data security and privacy controls.
- What happens if log volume exceeds contracted limits?
- How do you support cloud environments (AWS/Azure/GCP)?
- Provide sample QBR materials and dashboards.
- What is your disaster recovery plan for SOC operations?
- Describe your SLA credits and remedies for missed targets.

## Implementation roadmap (detailed)
**Phase 0: Strategy and packaging (2–4 weeks)**
- Define target client segment, service tiers, and pricing model.
- Select baseline tooling and evaluate reseller licensing.
- Build margin model and capacity plan.

**Phase 1: SOC build-out (4–8 weeks)**
- Hire or contract SOC analysts and detection engineers.
- Implement SIEM/SOAR stack and ticketing integration.
- Develop initial detection content and playbooks.

**Phase 2: Pilot onboarding (4–12 weeks)**
- Onboard 2–5 pilot clients with limited scope.
- Tune alerts and establish operational baselines.
- Finalize reporting format and SLA definitions.

**Phase 3: Scale and optimize (ongoing)**
- Automate recurring tasks and reduce false positives.
- Expand log sources and detection coverage.
- Add threat hunting and compliance reporting.

## Cash flow and revenue recognition notes
SOCaaS typically recognizes revenue monthly, while onboarding fees are recognized upon completion of integration
milestones. Providers should model cash flow impact of upfront tooling purchases and staffing ramp-up, especially
when contracts are annual but billed monthly. Build a reserve for incident response spikes and cloud ingest costs.

## Competitive positioning levers
- **Faster response SLAs** for critical incidents.
- **Industry-specific detection content** (healthcare, fintech, OT).
- **Co-managed models** to reduce client cost and improve collaboration.
- **Compliance-ready reporting** aligned to SOC 2 or ISO controls.
- **Transparent pricing** with predictable overage thresholds.

## Detailed service catalog and pricing worksheet
Use the table below as a pricing worksheet to ensure every service has a defined metric, deliverable, and contract
shape. This also helps prevent scope creep by making inclusions explicit.

| Service | Key deliverables | Common pricing metric | Typical contract shape |
| --- | --- | --- | --- |
| SOC monitoring | Alert triage, escalation, reporting | per endpoint or per GB/day | MRR + setup |
| MDR | EDR management, containment | per endpoint | MRR + setup |
| SIEM management | Log onboarding, correlation rules | per GB/day | MRR + overage |
| Threat hunting | Hypothesis-based investigations | hours/month | Add-on retainer |
| Vulnerability management | Scans, prioritization, reporting | per asset | MRR |
| Patch management | Patch scheduling, compliance | per endpoint | MRR |
| Firewall management | Rule changes, monitoring | per device | MRR |
| IDS/IPS monitoring | Tuning, alert triage | per device | MRR |
| Email security | Filtering, incident response | per mailbox | MRR |
| Cloud security monitoring | CSPM, log review | per account | MRR |
| DLP | Policy tuning, incident response | per user | MRR |
| Security awareness | Training + phishing | per user | MRR |
| IR retainer | Reserved response hours | annual retainer | Annual contract |
| Compliance support | Evidence mapping, reporting | hours/month | Retainer |
| vCISO | Governance and roadmap | hours/month | Retainer |

## Incident response and DFIR pricing deep dive
Incident response is often a mix of retainer and on-demand fees. Retainers create predictable income and improve
client readiness, while on-demand pricing covers unexpected incidents. Common patterns include:

- **Annual retainer with reserved hours:** 20–200 hours pre-paid; unused hours roll into tabletop or training.
- **On-demand hourly rates:** $200–$600/hour for analyst/forensic roles; premium for after-hours response.
- **Emergency premium:** 25–100% surcharge for immediate mobilization.
- **Minimum block:** 8–40 hours minimum for ransomware or major incident.

**Typical DFIR deliverables:** containment guidance, forensic imaging, timeline reconstruction, malware analysis,
eradication guidance, recovery validation, and executive post-incident report. Scope should define data retention,
forensic chain of custody, and legal counsel coordination.

## Unit economics example P&L (illustrative, annual)
This example assumes a mid-market MSSP with 15,000 endpoints under management.

| Line item | Annual amount | Notes |
| --- | --- | --- |
| SOC/MDR revenue | $7.2M | $40/endpoint/month average |
| Add-ons (vCISO, training) | $1.1M | Retainers + per-user fees |
| Project services | $0.8M | IR + assessments |
| Total revenue | $9.1M | — |
| SOC labor | $3.6M | Analysts, engineers, managers |
| Tooling and licenses | $1.8M | SIEM, EDR, SOAR |
| Cloud/storage | $0.7M | Ingest, retention |
| Sales and marketing | $0.8M | CAC and channel |
| G&A and compliance | $0.6M | Insurance, legal |
| Total COGS + Opex | $7.5M | — |
| Operating profit | $1.6M | ~18% operating margin |

## Capacity planning example (case-volume based)
Assume 1,200 alerts per week. If 20% escalate to incidents and average investigation time is 45 minutes:

- Incidents per week: 1,200 × 20% = 240
- Analyst hours per week: 240 × 0.75 hours = 180 hours
- Analysts required (40-hour week): 180 ÷ 40 = 4.5 analysts for incident handling

Add capacity for alert triage (non-escalated alerts), shift coverage, and PTO. Most SOCs add a 20–30% buffer
to prevent SLA breaches during spikes.

## Expanded detection use case library
Use this expanded list when building a detection catalog or communicating coverage to clients.

**Authentication and identity**
- Excessive failed logins across multiple accounts (credential stuffing).
- Password spray attempts across a tenant.
- Authentication from known malicious IP ranges.
- Impossible travel sign-in followed by new token issuance.
- MFA push fatigue sequences with eventual approval.
- Privileged account login outside approved hours.
- Dormant account reactivation and immediate data access.
- New OAuth app approvals with high-risk permissions.

**Privileged access and admin activity**
- Creation of new global admin accounts.
- Privilege escalation via role assignment changes.
- Removal of MFA on privileged accounts.
- Privileged password change without ticket.
- Direct login to domain controllers or critical servers.
- Audit log tampering or deletion attempts.
- Creation of API keys without rotation policies.
- Disablement of security tooling or audit policies.

**Endpoint and malware behaviors**
- Suspicious parent-child process chains (Office → PowerShell).
- LSASS memory access attempts.
- Credential dumping tools detected (Mimikatz variants).
- Mass file modification or encryption behaviors.
- Signed binary proxy execution (LOLbins).
- New persistence mechanisms (scheduled tasks, services).
- Suspicious driver installation events.
- Unusual remote service creation.

**Lateral movement and network**
- SMB or RDP lateral movement spikes.
- Network scanning from a workstation subnet.
- Abnormal internal DNS queries for admin shares.
- Remote service creation across multiple hosts.
- Use of administrative tools from non-admin hosts.
- Multiple failed authentication attempts across hosts.
- Suspicious WinRM or WMI usage.

**Data exfiltration**
- Large outbound transfers to unmanaged cloud storage.
- Unusual compression or archive creation prior to upload.
- Spike in outbound bandwidth to uncommon destinations.
- Sensitive file access outside business hours.
- Mass downloads from SaaS or document repositories.
- FTP/SFTP usage by non-technical accounts.
- Newly created sharing links with external domains.

**Email and collaboration abuse**
- New mailbox forwarding rules to external domains.
- Creation of inbox rules that hide security alerts.
- Mass deletion of email following suspicious login.
- Suspicious OAuth grants to email apps.
- Unusual meeting invite spamming (BEC precursor).

**Cloud and SaaS misconfigurations**
- Publicly accessible storage buckets or blobs.
- Security group changes allowing 0.0.0.0/0 ingress.
- Privileged cloud role creation without approval.
- Removal or disabling of cloud logging services.
- Unusual API calls from new regions or IPs.
- Creation of long-lived access keys.

**CI/CD and development environments**
- Exfiltration of secrets from pipeline variables.
- Unauthorized repo access or cloning.
- Changes to CI/CD workflows that add external scripts.
- New secrets created without rotation tags.
- Unexpected package changes or dependency tampering.

**Web application and API attacks**
- WAF alerts indicating SQL injection patterns.
- API abuse with high-rate requests and token reuse.
- Credential stuffing against public login endpoints.
- Enumeration of users or resources via API.

**OT/IoT and specialized environments**
- Unusual traffic between OT network segments.
- Firmware changes on critical devices.
- Legacy protocol usage spikes (SMBv1, Telnet).
- New device discovery in restricted VLANs.

## Security reporting and QBR artifact checklist
Well-structured reporting improves retention and upsell. Common report artifacts include:

- Executive dashboard with key KPIs.
- Severity-based incident summary.
- Top threat sources and geographies.
- Coverage gaps and recommended log sources.
- MTTA/MTTR trends and SLA adherence.
- Vulnerability and patch posture summary.
- Security awareness outcomes (phishing rates).
- Compliance evidence mapping (if in scope).

## Pricing negotiation, discounting, and term strategy
Discounting should be tied to contract term, scope commitments, or operational efficiencies. Best practices:

- Offer tiered discounts for 24–36 month commitments.
- Provide volume discounts only when log volume is predictable.
- Use phased onboarding pricing (lower during pilot, full rate after).
- Tie discounts to payment terms (annual prepay).
- Avoid discounts that undermine minimum monthly margins.

## Frequently asked questions (FAQ)
**Q: Is SOCaaS the same as MDR?**
A: SOCaaS is the broader SOC function; MDR usually includes EDR tooling and managed response. SOCaaS may use
SIEM-driven monitoring without endpoint containment unless specified.

**Q: Why do SOCaaS prices vary so widely?**
A: Coverage hours, log volume, response scope, and industry risk are the biggest drivers. Two environments with
identical endpoint counts can have 5–10x different log volumes.

**Q: What is a typical onboarding timeline?**
A: 30–90 days is common. Larger clients with many log sources may require 90–180 days to stabilize detections.

**Q: How should we handle log overages?**
A: Use clear overage pricing per GB/day and provide monthly usage reports so clients can adjust log sources.

**Q: What is the minimum contract term?**
A: Many MSSPs require 12–24 month terms to amortize onboarding costs and detection engineering effort.

**Q: What response actions are typically included?**
A: Monitoring-only tiers generally alert and advise. Managed response tiers can isolate endpoints or block users
with pre-approved authority.

**Q: How do MSSPs handle client-owned tools?**
A: Some offer BYO-SIEM/EDR discounts but charge for integration and support. Ensure ownership boundaries are clear.

**Q: Should vCISO services be bundled?**
A: Bundling a small number of vCISO hours can improve retention and create a path to larger strategic projects.

**Q: How do we estimate SIEM licensing cost?**
A: Start with a log sampling period and multiply by pricing per GB, then add retention storage and search costs.

**Q: What happens during incident spikes?**
A: Contracts should define surge capacity and additional billing for large-scale incidents or forensics work.

## Case study scenarios (illustrative)
These fictional scenarios demonstrate how typical MSP/MSSP pricing mechanisms are assembled. They are not real
quotes; use them as templates for your own modeling.

### Scenario 1: Small healthcare clinic (HIPAA-focused)
**Profile:** 2 locations, 65 employees, 55 endpoints, cloud-based EHR, limited on-site IT staff. Primary drivers are
HIPAA compliance, ransomware prevention, and cyber insurance requirements.

**Service design:**
- 8x5 SOC monitoring with after-hours on-call escalation.
- MDR with EDR deployed to endpoints and servers.
- Email security and phishing simulation for staff training.
- Vulnerability scanning monthly with remediation tracking.

**Pricing model (indicative):**
- 55 endpoints × $40/endpoint/month = $2,200
- 65 mailboxes × $4/mailbox/month = $260
- Vulnerability scanning (70 assets) × $10/asset/month = $700
- Training: 65 users × $2/user/month = $130
- Total MRR ≈ $3,290
- Onboarding (EDR + log integration): $3,000 one-time

**Notes:** Low log volume keeps SIEM costs minimal. A 12-month contract with annual prepay can justify a 5–10%
discount if margins remain above target.

### Scenario 2: High-growth SaaS company (SOC 2 readiness)
**Profile:** 300 employees, 450 endpoints, cloud-native infrastructure with 60–80 GB/day log ingest. Key drivers
include SOC 2 readiness, vendor due diligence, and rapid incident response.

**Service design:**
- 24x5 SOC monitoring with on-call weekend coverage.
- SIEM management with cloud log ingestion and correlation rules.
- MDR with managed containment capabilities.
- vCISO retainer for audit support and policy alignment.

**Pricing model (indicative):**
- 450 endpoints × $45/endpoint/month = $20,250
- SIEM ingest: 70 GB/day × $5/GB/day = $10,500
- vCISO retainer: $7,500/month
- Total MRR ≈ $38,250
- Onboarding and tuning: $20,000 one-time

**Notes:** The log ingest component is a major cost driver. The vCISO retainer supports SOC 2 control alignment and
reduces project-based consulting needs.

### Scenario 3: Regional retail chain (PCI compliance)
**Profile:** 25 stores, 400 POS endpoints, 300 back-office endpoints, multiple firewalls per site, PCI requirements.
The environment is log-heavy due to POS and network devices.

**Service design:**
- 24x7 SOC monitoring with PCI-specific detections.
- Managed firewall and IDS/IPS across all sites.
- Vulnerability scanning monthly with PCI reporting.
- Incident response retainer with 40 reserved hours.

**Pricing model (indicative):**
- 700 endpoints × $32/endpoint/month = $22,400
- Firewall management: 30 devices × $300/device/month = $9,000
- SIEM ingest: 120 GB/day × $4/GB/day = $14,400
- PCI reporting retainer: $3,000/month
- Total MRR ≈ $48,800
- IR retainer: $30,000 annually

**Notes:** Multi-site firewall management and log ingest drive cost. PCI reporting is positioned as a compliance
add-on to protect margins.

### Scenario 4: Manufacturing firm with OT/IoT footprint
**Profile:** 1,200 endpoints, 150 OT/IoT devices, segmented network, critical availability needs. Drivers include
risk of plant shutdowns and IP theft.

**Service design:**
- 24x7 SOC monitoring with OT-aware detections.
- NDR deployment for industrial segments.
- Managed vulnerability scanning with quarterly OT assessments.
- IR retainer focused on operational continuity.

**Pricing model (indicative):**
- 1,200 endpoints × $30/endpoint/month = $36,000
- NDR (150 devices) × $20/device/month = $3,000
- SIEM ingest: 90 GB/day × $4.50/GB/day = $12,150
- OT assessment retainer: $5,000/month
- Total MRR ≈ $56,150
- Onboarding: $25,000 one-time

**Notes:** OT monitoring increases detection engineering complexity, so pricing should reflect higher tuning effort.

### Scenario 5: Regional bank or credit union
**Profile:** 2,500 endpoints, 300 servers, high regulatory scrutiny, strict SLA requirements. Drivers include fraud
detection, high confidentiality, and regulatory reporting.

**Service design:**
- 24x7 SOC monitoring with strict SLAs.
- MDR with managed containment and privileged access monitoring.
- SIEM ingest with 200 GB/day retention and 12-month storage.
- Quarterly compliance reporting and executive briefings.

**Pricing model (indicative):**
- 2,800 endpoints (including servers) × $55/endpoint/month = $154,000
- SIEM ingest: 200 GB/day × $6/GB/day = $36,000
- Compliance reporting retainer: $12,000/month
- Total MRR ≈ $202,000
- Onboarding: $50,000 one-time

**Notes:** Server-heavy environments justify higher endpoint rates. High SLA expectations often require dedicated
analysts or a premium support tier.

### Scenario 6: Professional services / law firm
**Profile:** 500 users, 450 endpoints, highly sensitive data, strict confidentiality requirements. Drivers include
client trust, regulatory obligations, and insurance requirements.

**Service design:**
- 16x5 SOC monitoring with after-hours escalation.
- MDR with endpoint isolation capabilities.
- Email security, DLP, and encryption policy monitoring.
- Security awareness training quarterly.

**Pricing model (indicative):**
- 450 endpoints × $38/endpoint/month = $17,100
- Email/DLP add-on: 500 users × $6/user/month = $3,000
- Training: 500 users × $2/user/month = $1,000
- SIEM ingest: 40 GB/day × $4/GB/day = $4,800
- Total MRR ≈ $25,900
- Onboarding: $12,000 one-time

**Notes:** DLP increases monitoring scope but creates a strong compliance narrative for legal and professional
services buyers.

## SOCaaS control mapping (framework alignment)
Many buyers want to understand how SOCaaS aligns with recognized frameworks. The table below offers a simple
mapping between SOCaaS functions and NIST CSF categories. This alignment helps MSSPs communicate compliance value
without overstating audit outcomes.

| SOCaaS function | NIST CSF category | Example evidence |
| --- | --- | --- |
| Asset inventory and log source discovery | Identify | Asset and data flow inventory |
| Log collection and normalization | Detect | Centralized SIEM logs |
| Alert triage and escalation | Detect/Respond | Incident tickets, escalations |
| Containment actions | Respond | Playbook execution records |
| Post-incident reporting | Respond/Recover | Incident reports, lessons learned |
| Backup monitoring and validation | Recover | Recovery test results |

**Practical guidance:** position SOCaaS as a “detect and respond” control layer that complements client-side
policies and governance controls. SOCaaS improves audit readiness but does not replace required policies or risk
ownership.

## Data retention, privacy, and residency considerations
Data governance can materially affect pricing and tooling. Clients in regulated sectors may require longer
retention, specific storage locations, or encryption controls, increasing costs.

- **Retention duration:** 90 days to 1 year is common; regulated sectors may require 2–7 years.
- **Hot vs cold storage:** hot storage for rapid search is more expensive than archival storage.
- **Data residency:** regional storage mandates can require multiple SIEM instances.
- **Encryption requirements:** client-managed keys or HSM integration add cost.
- **Privacy filtering:** PII redaction or tokenization can be required for certain logs.
- **Access controls:** strict RBAC and audit logging for SOC analysts may be contractually required.
- **Third-party access:** subcontractor rules must be explicitly documented.

## Tooling selection and integration checklist
Selecting tools with integration readiness reduces onboarding costs and accelerates revenue recognition.

- SIEM supports required log sources with minimal custom parsing.
- EDR/XDR integrates with SIEM for alert correlation.
- SOAR can trigger containment actions with auditable logs.
- Ticketing integrates with client systems for escalation.
- Threat intel feeds are curated and reduce false positives.
- Reporting supports executive dashboards and compliance mapping.
- Multi-tenant architecture supports separation of client data.
- API access supports automation and custom reporting.

## SOC roles and responsibilities (RACI summary)
Clear responsibility assignment reduces disputes during incidents.

| Role | Primary responsibilities |
| --- | --- |
| Client IT owner | Asset inventory, access approvals, remediation actions |
| Client security lead | Policy ownership, risk decisions, escalation authority |
| SOC Tier 1 | Alert triage, initial investigation, ticket creation |
| SOC Tier 2 | Deep investigation, response guidance, playbook execution |
| SOC manager | SLA adherence, quality control, client communication |
| Detection engineer | Rule tuning, use case development |
| IR lead | Incident coordination, containment guidance |

## Step-by-step pricing calculator (worked example)
**Scenario:** 1,000 endpoints, 50 GB/day ingest, 24x5 coverage, MDR with EDR included.

1. Endpoint base price: 1,000 × $38 = $38,000/month
2. SIEM ingest: 50 GB/day × $4/GB/day = $6,000/month
3. Coverage premium (24x5 vs 8x5): +20% = $8,800/month
4. Add-ons: training (1,000 users × $2) = $2,000/month
5. Total MRR ≈ $54,800/month

**Apply margin check:** If COGS is $28,000/month, gross margin ≈ 49%. Adjust price if below target.

## Pricing sensitivity analysis (drivers and impact)
Understanding how key variables affect margin helps avoid underpricing. The most sensitive levers are log volume,
coverage hours, and alert quality. A small increase in log ingest can materially increase SIEM costs without a
matching revenue increase if overage pricing is not structured correctly.

| Change driver | Revenue impact | Margin impact | Mitigation |
| --- | --- | --- | --- |
| +20% log ingest | +0–5% (if flat price) | −5–15% | Use GB/day overages |
| +20% endpoints | +20% | Neutral to positive | Ensure onboarding capacity |
| Move 8x5 → 24x7 | +40–120% | Neutral to negative | Add coverage premium |
| Alert noise spike | 0% | −10–25% | Tune detections, SOAR automation |

**Practical checklist:**
- Recalculate log volume quarterly and compare against contract limits.
- Bake in annual price escalators (3–7%) to cover wage inflation.
- Define a high-volume ingest discount only after consistent usage history.
- Model surge capacity costs for incidents and define billing terms.

## Revenue operations and retention playbook
Retention drives income stability. Mature MSSPs treat customer success as a formal revenue function.

**Onboarding and stabilization**
- 30-day onboarding plan with weekly check-ins.
- Log source validation and alert tuning milestones.
- Early wins report to demonstrate immediate value.

**Ongoing operations**
- Monthly operational report with actionable insights.
- Quarterly business review (QBR) that links detections to business risk.
- Annual security roadmap aligned to client priorities.

**Expansion paths**
- Introduce vCISO hours after 90 days to align policies.
- Offer vulnerability management once log hygiene is stable.
- Use phishing simulation results to sell training expansions.

**Renewal and churn prevention**
- Track sentiment and response-time satisfaction monthly.
- Implement SLA performance dashboards shared with client leadership.
- Offer compliance reporting upgrades ahead of audit cycles.
- Ensure executive stakeholder visibility on improvements.

## Service quality audit checklist
Use this checklist quarterly to prevent service erosion:

- Coverage hours meet SLA commitments.
- Alert response time within agreed thresholds.
- False positive rates tracked and reduced.
- Detection content updated for new threats.
- Client log sources still active and complete.
- Incident runbooks reviewed and updated.
- Analyst training on client environment completed.
- QBRs delivered on schedule.

## Security service maturity model (provider view)
This maturity model helps MSSPs articulate their capability level and align pricing with delivery depth.

**Level 1: Monitoring-only SOC**
Focuses on alert ingestion, triage, and escalation. The provider relies heavily on out-of-the-box detection rules
and has limited response authority. Pricing is typically lower and more sensitive to log volume, since service
value is concentrated in fast alert notification rather than managed containment. This tier is common for smaller
clients or those with internal security teams.

**Level 2: Managed detection**
Adds detection engineering, rule tuning, and contextual enrichment. The SOC begins to provide guided response and
playbooks but still requires client approval for containment actions. This tier improves retention by reducing
false positives and enhancing reporting. Pricing is moderately higher, with a stronger emphasis on SLA adherence.

**Level 3: Managed response and hunting**
Includes containment actions, active threat hunting, and dedicated incident coordination. Tooling is integrated
with SOAR to automate standard actions. Providers at this level typically require longer contract terms and
charge premium rates for 24x7 coverage. This tier is a core income driver for mature MSSPs.

**Level 4: Intelligence-driven SOC**
Adds intelligence-led detection, advanced analytics, and strategic risk reporting. Clients receive continuous
improvement plans, compliance alignment, and quarterly executive briefings. This tier often includes vCISO
services and deep integration with client processes. Pricing is highest but yields strong margins due to high
retention and strategic upsell opportunities.

## Client discovery questionnaire (security services)
Use this intake questionnaire to inform pricing, scope, and detection strategy. It also helps uncover hidden
log sources and compliance constraints.

- How many endpoints, servers, and cloud workloads are in scope?
- Which identity provider(s) are used for authentication?
- What are the primary business systems and critical applications?
- Which compliance frameworks apply (SOC 2, HIPAA, PCI, ISO)?
- What is the current incident response plan and escalation path?
- Are any security tools already deployed (SIEM, EDR, DLP)?
- How many log sources can be enabled immediately?
- What is the acceptable response window for critical incidents?
- Is after-hours response required, and at what severity?
- Do you require data residency or regional storage constraints?
- What is the expected log retention duration?
- Are there OT/IoT or legacy systems with limited logging?
- How frequently do you need executive or compliance reporting?
- Is co-managed response preferred or full managed response?
- Are there contractual penalties for downtime or data loss?
- What ticketing system and communication channels are required?
- Who is authorized to approve containment actions?
- Are there third-party vendors or MSSPs already involved?
- What historical incidents or near-misses have occurred?
- What is your budget range and target contract term?

## Onboarding deliverables checklist
This checklist ensures SOCaaS onboarding is complete and measurable:

- Asset inventory and in-scope systems list.
- Log source onboarding plan with owners.
- Data normalization and parsing validation.
- Initial detection rule set enabled and tuned.
- Escalation matrix and contact list finalized.
- Ticketing system integration tested.
- Response playbooks reviewed and approved.
- Coverage hours and SLA targets documented.
- Reporting templates agreed and scheduled.
- Acceptance criteria for go-live sign-off.

## Log volume optimization and cost control tactics
SIEM and SOCaaS economics are highly sensitive to ingest volume. Reducing unnecessary logs or routing low-value
events to cheaper storage can materially improve margin without reducing detection coverage. Use these tactics
to manage cost while maintaining visibility:

- Enable verbose logging only on high-risk systems.
- Use selective forwarding for low-value application logs.
- Filter out known benign events (e.g., health checks).
- Deduplicate repetitive alerts at the source or in the SIEM.
- Separate security-relevant logs from operational telemetry.
- Move older logs to cold storage with slower query needs.
- Implement alert suppression for known maintenance windows.
- Use event sampling for high-volume, low-risk sources.
- Review ingestion monthly and adjust based on incident learnings.

Applying these measures typically reduces ingest by 15–40% in early-stage deployments, which can free budget for
additional detection content or expanded response coverage.

## Quick pricing cheat sheet (planning ranges)
Use this quick-reference list when drafting early-stage budgets before a full log analysis:

- Basic 8x5 monitoring: $8–$20 per endpoint/month.
- 24x7 SOC monitoring: $20–$60 per endpoint/month.
- MDR with EDR included: $30–$120 per endpoint/month.
- SIEM ingest add-on: $2–$10 per GB/day for SOC analysis.
- Managed firewall: $150–$600 per device/month.
- vCISO retainer: $3k–$20k per month.
- Onboarding fees: 1–3x monthly recurring fees.

These figures are intentionally broad and assume a mid-market environment. Use them to sanity-check proposals,
then refine with actual log sampling and client-specific complexity factors.

## Regional adjustment note
Pricing ranges should be adjusted for local wage levels, regulatory requirements, and data residency costs.
North America and Western Europe often command higher rates for senior analysts and 24x7 coverage, while nearshore
and offshore delivery models can reduce labor costs but may increase management overhead. Always validate local
market expectations and ensure that regional compliance requirements (GDPR, data localization) are covered in the
SOW and pricing model.
Account for currency risk in multi-year contracts and confirm whether local taxes, VAT, or cross-border billing
requirements affect final pricing and payment terms.
    
## Glossary
- **ARPA:** Average revenue per account.
- **ARR:** Annual recurring revenue.
- **MRR:** Monthly recurring revenue.
- **COGS:** Cost of goods sold; direct cost to deliver service.
- **MTTD/MTTR:** Mean time to detect/respond; key SOC performance metrics.
- **RFP:** Request for proposal used to compare MSSP offerings.

## Final note
This document is a large-format planning reference. The numbers are intentionally broad to accommodate regional
variance and service differentiation. For production use, validate with competitive quotes, test pilot programs,
and internal cost modeling before finalizing pricing or revenue projections.
