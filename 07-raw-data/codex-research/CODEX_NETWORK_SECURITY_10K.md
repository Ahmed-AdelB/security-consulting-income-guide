# CODEX Network Security Consulting Guide — 10K Research Synthesis

## Purpose
- Synthesize network security consulting guidance on segmentation, firewalls, zero trust, wireless, OT/ICS, and network pentesting.
- Extract rate benchmarks, certification signals, and market opportunity cues from in-repo research.
- Provide a structured service catalog, deliverables library, and pricing framework for consulting scoping.
- Keep the guidance grounded in repository sources without external web browsing.

## Source Base (In-Repo Research)
- `CODEX_SECURITY_ARCH_10K.md` — security architecture rate bands, segmentation guidance, and deliverables.
- `CODEX_ZEROTRUST_10K.md` — zero trust rates, specialization premiums, budgets, and segmentation workstreams.
- `CODEX_WIRELESS_10K.md` — wireless security demand drivers, pricing, and segmentation validation steps.
- `CODEX_OT_SECURITY_10K.md` — OT/ICS segmentation, vendor-aligned services, and rate benchmarks.
- `SECURITY_ARCHITECTURE_CONSULTING_GUIDE_2025.md` — architecture rate spectrum and engagement models.
- `PENETRATION_TESTING_CONSULTING_COMPREHENSIVE_GUIDE_2025.md` — network pentest rates and pricing models.
- `docs/PART4_RATE_GUIDE.md` — premium specialization rates and expert network benchmarks.
- `INDEED_CYBERSECURITY_SALARY_COMPILATION_2025.md` — salary benchmarks and certification premiums.

## How to Use This Guide
- Treat rate tables as directional baselines for scoping, not fixed quotes.
- Map segmentation and firewall guidance to your environment and regulatory constraints.
- Use the deliverables library to build SOWs and acceptance criteria.
- Pair market opportunity signals with the specialization rate tables to prioritize offerings.
- Combine architecture, zero trust, wireless, and OT sections for multi-domain programs.

## Executive Summary
- Network security consulting blends architecture, segmentation, identity, and monitoring into repeatable controls.
- Zero trust programs command premium rates because they require cross-domain integration (identity, network, data).
- OT/ICS network security demands zone/conduit design and carries premium rates due to safety constraints.
- Wireless security engagements remain high value as hybrid work and IoT expand the RF attack surface.
- Security architecture rate bands range from $50–$400+/hr depending on seniority and specialization.
- Zero trust global rate bands cluster between $150–$500+ per hour depending on provider type.
- Wireless audits range from $2,500–$150,000+; wireless pentests scale to $400,000+ for global scope.
- OT/ICS hourly rates span $120–$500/hr with fixed-fee assessments from $25k–$350k.
- Network pentest day rates reach $1,500–$2,500/day for enterprise network testing.
- Certifications (CISSP, CCSP, SABSA, TOGAF, GIAC, CCIE Security) materially influence rates.
- Market opportunity is strongest in regulated industries, critical infrastructure, and hybrid cloud transitions.

## Market Landscape and Demand Drivers

### Enterprise and Cloud Drivers
- Enterprises seek architecture leadership that reduces cloud risk and accelerates compliance.
- Architecture consulting is positioned as a high-impact, short-duration engagement that yields a roadmap.
- Mature clients blend advisory architecture work with fractional leadership (vCISO or interim architect).
- Cloud landing zones and guardrails require consistent network segmentation and routing strategy.
- Multi-cloud environments raise demand for consistent network policy enforcement patterns.

### Zero Trust Transformation Drivers
- Zero trust replaces perimeter trust with identity and policy-driven controls.
- Regulatory pressure increases demand for measurable segmentation and access governance.
- Cross-domain integration (identity, network, data) raises the value of specialized consultants.
- Programs require policy enforcement points (PEP) and policy decision points (PDP).
- Legacy systems drive demand for phased segmentation and migration planning.

### Wireless Network Security Drivers
- Hybrid work and BYOD increase wireless reliance and expand attack surface.
- IoT growth increases lateral movement risk in poorly segmented wireless networks.
- Cloud-managed WiFi centralizes configuration but increases blast radius for misconfigurations.
- PCI DSS, HIPAA, ISO 27001, SOC 2, and NIST guidance fuel periodic wireless assessments.
- Ransomware and insider threats make WiFi a critical initial-access vector.

### OT/ICS and Critical Infrastructure Drivers
- IT/OT convergence exposes legacy systems to enterprise threat paths.
- Ransomware targeting industrial operations elevates segmentation urgency.
- Regulatory oversight (NERC CIP, TSA directives, IEC 62443) increases demand.
- Critical infrastructure owners prioritize asset visibility and network segmentation.
- Vendor ecosystems (Claroty, Nozomi, Dragos) anchor service delivery models.

### Buyer Personas (Cross-Domain)
- CISO, CIO, and security directors seeking enterprise roadmaps.
- Network engineering managers responsible for segmentation and routing.
- Compliance and risk teams tied to audit deadlines.
- OT engineers and plant managers focused on safety and uptime.
- MSPs and MSSPs needing specialist support for client networks.

## Network Security Consulting Service Catalog

### Strategy and Governance
- Security architecture principles and standards.
- Architecture decision frameworks and exception handling.
- Security capability mapping and maturity assessments.
- Integration of security architecture into enterprise governance.
- Long-term security architecture roadmaps aligned to business strategy.

### Current-State Assessment
- System inventory and criticality ranking.
- Data flow and trust boundary mapping.
- Control coverage assessment and gap analysis.
- Threat modeling for high-risk systems.
- Dependency and integration analysis.

### Target-State Architecture
- Enterprise security reference architecture.
- Standard patterns for identity, network, data, and application security.
- Multi-cloud and hybrid integration patterns.
- Zero trust design patterns and segmentation strategies.
- Resilience and disaster recovery architecture.

### Network and Zero Trust Architecture
- Replace implicit network trust with explicit identity-based access.
- Design segmentation based on sensitivity, workload type, and data flows.
- Treat internal traffic as untrusted; monitor east-west movement.
- Implement secure DNS, proxy, and egress controls.
- Define policy enforcement points and policy decision points.
- Plan for legacy systems that cannot support modern identity protocols.

### Cloud and Infrastructure Architecture
- Cloud account/subscription strategy.
- Baseline policies, guardrails, and logging patterns.
- Secure connectivity between cloud and on-prem environments.
- Key management and secrets architecture.
- Infrastructure-as-code standards and pipeline gates.

### Identity and Access Architecture
- Unified identity strategy across workforce, customers, and partners.
- Privileged access management architecture.
- Role- and attribute-based access control patterns.
- Identity lifecycle, provisioning, and recertification processes.
- Federation and SSO integration patterns.

### Data Security Architecture
- Data classification and handling standards.
- Encryption and key management patterns.
- Data masking and tokenization strategies.
- DLP and data loss risk mitigation.
- Data residency and cross-border transfer considerations.

### Application and DevSecOps Architecture
- Secure SDLC standards and pipeline controls.
- Application security testing strategy and tool integration.
- API security design patterns and gateway architecture.
- Secrets management in CI/CD and runtime.
- Software supply chain security controls.

### Detection and Response Architecture
- Logging and telemetry architecture.
- SIEM/SOAR integration patterns.
- Security event normalization and retention policies.
- Detection engineering guidance aligned to threat models.
- Incident response playbooks and architecture considerations.

### Third-Party and Supply Chain Security
- Vendor onboarding and access architecture.
- Security requirements in procurement and contracts.
- Continuous monitoring of critical vendors.
- Software supply chain risk mitigation patterns.
- Vendor segmentation and risk tiering.

### Specialized Domains
- OT/ICS security architecture and safety integration.
- IoT device security and lifecycle management.
- Wireless security assessment and segmentation validation.
- Zero trust network access (ZTNA) and SASE deployment planning.

## Network Segmentation and Firewall Playbook (Synthesis)
- Trust zone definitions and segmentation maps.
- Application dependency mapping and flow analysis.
- Policy enforcement points for segmentation tools.
- Migration planning from flat networks to segmented architectures.
- Validation and rollback planning for segmentation changes.
- Purdue model alignment and zone/conduit design for OT.
- Firewall rules and policy definition aligned to zones.
- Conduit traffic definitions and firewall rule guidance.
- VLAN tagging enforcement for wireless segmentation.
- NAC policy validation for unknown device isolation.
- Segmentation based on data sensitivity and workload type.
- Vendor segmentation based on operational criticality.
- Secure remote access hardening for segmented environments.
- Logging and telemetry requirements for segmentation controls.

## Zero Trust Consulting Workstreams

### Identity and Access
- Identity inventory and consolidation of identity providers.
- MFA and conditional access policy design.
- Privileged access management architecture and vault integration.
- Role mining and least-privilege access modeling.
- Service account governance and credential rotation.

### Device and Endpoint Security
- Device classification (corporate, BYOD, contractor).
- Compliance posture definitions and device risk scoring.
- EDR and MDM integration with access policies.
- Endpoint configuration baselines and patching requirements.
- Access enforcement for unmanaged or non-compliant devices.

### Network and Infrastructure Segmentation
- Trust zone definitions and segmentation maps.
- Application dependency mapping and flow analysis.
- Policy enforcement points for segmentation tools.
- Migration planning from flat networks to segmented architectures.
- Validation and rollback planning for segmentation changes.

### Application and Workload Security
- Application inventory and criticality classification.
- Service identity and API authentication models.
- Workload segmentation within container or VM environments.
- Service mesh or API gateway integration for policy enforcement.
- Secure access for remote and third-party applications.

### Data Security and Policy
- Data classification scheme and tagging strategy.
- Encryption requirements and key management design.
- Data access control matrix and ABAC models.
- DLP policy design and monitoring workflows.
- Data residency and cross-border compliance mapping.

### Visibility, Analytics, and Continuous Verification
- Logging and telemetry requirements by control point.
- Identity, device, and network telemetry correlation design.
- UEBA and behavior analytics integration guidance.
- Alerting thresholds and escalation workflows.
- KPIs for measuring trust decision effectiveness.

### Automation and Orchestration
- Policy-as-code frameworks and automation pipelines.
- SOAR integration for automated response to policy violations.
- Continuous compliance checks and drift detection.
- API-driven provisioning and access enforcement.

### Governance and Operating Model
- Zero trust governance board structure and cadence.
- RACI definitions across IT, security, and business units.
- Change management and communication plans.
- Budgeting and ongoing KPI reporting model.

## Wireless Network Security Consulting

### Service Taxonomy
- Wireless security audit for configuration and policy review.
- Wireless security assessment with light active testing.
- Wireless penetration test for adversarial RF attack paths.
- Wireless red team/adversary emulation scenarios.
- Continuous monitoring and WIPS tuning for rogue AP detection.

### Engagement Phases
- Pre-engagement scoping with asset inventory and ROE.
- Discovery and passive reconnaissance with RF sweeps.
- Active testing of authentication and encryption controls.
- Client-side attack validation (evil twin, supplicant behavior).
- Segmentation and lateral movement validation (wireless to internal).
- Reporting, risk rating, and remediation guidance.

### Attack Paths and Test Categories
- Authentication and encryption weaknesses (WPA2/WPA3 posture).
- EAP misconfiguration and weak certificate validation.
- Management plane exposure and insecure admin interfaces.
- Rogue AP detection and evil twin susceptibility.
- Captive portal weaknesses and guest isolation gaps.
- VLAN misconfigurations enabling lateral movement.
- IoT/OT WiFi exposure with legacy protocols.

### Staffing and Skills
- Wireless security consultant (senior delivery lead).
- Network security architect for segmentation review.
- Field engineer for RF survey and onsite recon.
- Experience with NAC platforms (ISE/ClearPass).
- Strong reporting and remediation planning capability.

## OT/ICS Network Security Consulting

### Common Entry Points
- Asset discovery and network visibility assessment.
- Risk assessments and segmentation planning.
- OT SOC integration and alert triage workflows.
- Incident response readiness and tabletop exercises.

### Vendor-Aligned Services
- Claroty: asset discovery, risk assessment, secure remote access, segmentation strategy.
- Nozomi Networks: passive monitoring, asset inventory, vulnerability management, ISA/IEC 62443 support.
- Dragos: threat-informed OT monitoring, incident response readiness, OT SOC design.

### OT Deliverables
- Asset inventory with model/firmware and criticality ratings.
- Network diagrams of OT zones, conduits, and trust boundaries.
- Risk register with operational impact and prioritization.
- Segmentation blueprint with phased rollout plan.
- Detection strategy mapped to OT playbooks.
- OT incident response plan and tabletop outputs.

### Controls Roadmap
- Short-term: asset inventory, segmentation design, remote access hardening, basic monitoring.
- Mid-term: segmentation implementation, OT SOC operationalization, patch lifecycle.
- Long-term: full OT security program governance and threat hunting.

## Network Penetration Testing Focus
- Testing types include web apps, APIs, internal networks, and external networks.
- Enterprise network testing often demands expert-level day rates.
- Network protocols in scope include TCP/IP, DNS, and SMB.
- External network assessments typically run 3–7 days.
- Enterprise network pentests often span 10–20 days.

## Engagement Models and Typical Effort

### Security Architecture Engagements
- Advisory retainer: 10–40 hours/month for architecture review boards.
- Architecture assessment and gap analysis: 2–6 weeks, 80–240 hours.
- Target-state architecture and roadmap: 4–12 weeks, 160–480 hours.
- Zero trust program design: 8–26 weeks, 320–1,000 hours.
- Identity and access modernization: 8–20 weeks, 320–800 hours.

### Zero Trust Engagement Types
- Assessment and maturity baseline: 4–8 weeks, $30k–$150k.
- Strategy and roadmap development: 6–12 weeks, $50k–$250k.
- Architecture design and proof of concept: 8–16 weeks, $80k–$400k.
- Implementation oversight and governance: 6–24 months, $250k–$2M+.

### Wireless Engagement Models
- Fixed-price audits for defined RF scope.
- Time-and-materials when environment changes or discovery is incomplete.
- Retainers for quarterly assessments and ongoing rogue AP monitoring.
- Embedded specialist engagements (2–8 weeks) for large programs.

### OT/ICS Engagement Models
- Discovery and baseline assessment with fixed-fee pricing.
- Segmentation design plus rollout planning.
- OT SOC integration and runbook development.
- IR readiness and tabletop exercises.

## Deliverables Library

### Assessment and Mapping
- System inventory and criticality ranking.
- Data flow and trust boundary mapping.
- Threat model summaries for high-risk systems.
- Control coverage assessment and gap analysis.
- Dependency and integration analysis.

### Architecture and Roadmaps
- Enterprise security reference architecture.
- Target-state architecture diagrams.
- Segmentation strategy and phased migration roadmap.
- Cloud landing zone blueprint and guardrails.
- IAM target-state blueprint with PAM integration.

### Policy and Controls
- Firewall policy and rule base guidance.
- Zero trust policy framework and enforcement mapping.
- Data classification standards and handling policies.
- Vendor onboarding and access architecture policies.
- Secure remote access standards for OT and third parties.

### Monitoring and Response
- Logging and telemetry architecture.
- SIEM/SOAR integration patterns.
- Detection engineering guidance aligned to threat models.
- Incident response playbooks and escalation paths.
- OT SOC runbooks and tabletop exercise results.

### Wireless Deliverables
- RF discovery and rogue AP inventory.
- Wireless audit findings with encryption and policy gaps.
- Wireless-to-internal segmentation validation results.
- Pentest findings with attack paths and remediation steps.

## Rate Benchmarks and Pricing

### Security Architecture Rate Snapshot (USD/hr)
| Rate Band | Typical Profile | Common Use Cases | Notes |
| --- | --- | --- | --- |
| $50–$100/hr | Junior-to-mid or offshore architect | Documentation support, diagramming, control mapping | Lower cost, narrower scope |
| $100–$150/hr | Experienced independent architect | Standard reference architectures, design reviews | Common for mid-level consultants |
| $150–$250/hr | Senior/principal architect | Enterprise programs, regulated industries | Lead architect or boutique firm |
| $250–$400+/hr | Strategic advisor or specialist | Breach-driven redesigns, OT/ICS, urgent programs | Premium scarcity rates |

### Security Architecture Role Ladder
| Role Level | Typical Experience | Responsibilities | Typical Range |
| --- | --- | --- | --- |
| Associate Architect | 3–5 years | Diagrams, control mapping, documentation | $50–$90/hr |
| Architect | 5–8 years | System-level designs, threat modeling | $80–$140/hr |
| Senior/Lead Architect | 8–12 years | Cross-system designs, program ownership | $120–$220/hr |
| Principal Architect | 12+ years | Enterprise patterns, governance | $160–$300/hr |
| Strategic Advisor | 15+ years | Executive advisory, transformation | $250–$400+/hr |

### Security Architecture Regional Multipliers
- North America: 1.0x baseline.
- Western Europe: 0.8–1.0x.
- Eastern Europe: 0.4–0.7x.
- LATAM: 0.3–0.6x.
- India / South Asia: 0.2–0.5x.
- Australia / NZ: 0.9–1.1x.
- Middle East (specialist): 0.8–1.2x.

### Day, Week, and Month Conversions
- Day rate (8 hours): $400–$3,200+.
- Week rate (40 hours): $2,000–$16,000+.
- Monthly retainer (20–40 hours): $1,000–$16,000+.

### Security Architecture Sample Budgets
1. Security architecture assessment: 160–240 hours, $120–$180/hr, $19k–$43k.
2. Cloud landing zone architecture: 240–360 hours, $150–$220/hr, $36k–$79k.
3. Zero trust architecture program: 600–900 hours, $180–$300/hr, $108k–$270k.
4. IAM/PAM modernization: 320–600 hours, $150–$250/hr, $48k–$150k.
5. M&A integration architecture: 120–300 hours, $160–$260/hr, $19k–$78k.
6. Compliance remediation architecture: 200–400 hours, $150–$240/hr, $30k–$96k.
7. Application security architecture program: 300–700 hours, $140–$230/hr, $42k–$161k.

### Security Architecture Guide Rate Spectrum
| Band | Typical Engagement | Benchmark Range | Notes |
| --- | --- | --- | --- |
| Baseline contractor | General consulting support | $50–$75/hr | Entry contractor equivalents |
| Standard consulting | Broad security consulting | $100–$300/hr | Baseline consulting range |
| Security architecture | Cloud/security architect | $175–$300/hr | Architecture-heavy work |
| Senior leadership | Fractional/vCISO lead | $250–$500+/hr | Executive advisory |
| Expert networks | 1-hour expert calls | $200–$1,000+/hr | Premium advisory |
| Premium outliers | High-sensitivity engagements | $500–$625+/hr | Scarcity cases |

### Project and Retainer Benchmarks
| Model | Typical Range | Notes |
| --- | --- | --- |
| Project-based assessments | $4,000–$12,000 | Short, defined architecture projects |
| vCISO-style project fees | $5k–$15k entry, $15k–$40k mid, $40k–$100k+ senior | Proxy for architecture-heavy advisory |
| Monthly retainers | $2,000–$25,000+ | Fractional architect or vCISO |

### Zero Trust Global Rate Bands (USD)
| Provider Type | Typical Hourly Rate | Typical Daily Rate | Notes |
| --- | --- | --- | --- |
| Independent consultant | 150–350 | 1,200–2,800 | Wide variation by region |
| Boutique security firm | 200–400 | 1,600–3,200 | Methodology + small teams |
| Global consulting firm | 250–500+ | 2,000–4,000+ | Premium for scale |
| Niche zero trust specialist | 220–450 | 1,750–3,600 | Deep implementation expertise |

### Zero Trust Regional Rates (USD/hr)
| Region | Mid-level | Senior | Principal |
| --- | --- | --- | --- |
| North America | 130–220 | 180–300 | 250–400+ |
| UK & Ireland | 110–200 | 160–260 | 220–350 |
| Western Europe | 100–190 | 150–240 | 210–320 |
| Southern Europe | 80–160 | 120–200 | 170–270 |
| Middle East | 110–200 | 160–280 | 220–350 |
| APAC | 80–160 | 120–230 | 180–320 |
| Latin America | 60–120 | 90–170 | 130–220 |
| Africa | 60–120 | 90–160 | 120–220 |

### Zero Trust Specialization Premiums
- IAM/PAM: 10–25% premium over base rate.
- Network microsegmentation: 10–20% premium.
- ZTNA/SASE: 10–20% premium.
- Cloud zero trust (multi-cloud): 15–30% premium.
- OT/IoT zero trust: 20–40% premium.
- Data-centric zero trust (DLP/ABAC): 15–25% premium.
- DevSecOps and application security: 10–20% premium.

### Zero Trust Engagement Budgets
- Assessment and maturity baseline: $30k–$150k.
- Strategy and roadmap development: $50k–$250k.
- Architecture design and proof of concept: $80k–$400k.
- Implementation oversight and governance: $250k–$2M+.

### Zero Trust Industry Multipliers and Budgets
| Industry | Typical Rate Multiplier | Typical Budget Range |
| --- | --- | --- |
| Financial services | 1.2–1.5x | $150k–$1.5M |
| Healthcare | 1.1–1.4x | $120k–$1.2M |
| Government/public sector | 1.2–1.6x | $200k–$2M |
| Critical infrastructure | 1.3–1.7x | $250k–$3M |
| Technology/SaaS | 1.0–1.3x | $80k–$900k |
| Manufacturing/logistics | 1.0–1.3x | $100k–$1M |
| Retail/e-commerce | 0.9–1.2x | $70k–$800k |
| Professional services | 0.9–1.2x | $60k–$700k |

### Zero Trust Client Size Budgets
| Client Size | Typical Scope | Engagement Budget Range |
| --- | --- | --- |
| Small (250–1,000 employees) | Targeted assessment or pilot | $25k–$150k |
| Midmarket (1,000–5,000) | Assessment + roadmap | $60k–$300k |
| Enterprise (5,000–20,000) | Full roadmap + pilot | $150k–$800k |
| Global enterprise (20,000+) | Multi-year transformation | $500k–$5M+ |

### Wireless Consulting Rates
| Role | Hourly (USD) | Day Rate (USD) | Notes |
| --- | --- | --- | --- |
| Wireless Analyst | $100–$160 | $800–$1,280 | RF survey support |
| Senior Wireless Consultant | $170–$275 | $1,360–$2,200 | Primary delivery |
| Lead/Principal | $250–$400 | $2,000–$3,200 | Architecture and complex pentests |
| Specialist/Red Team | $350–$550 | $2,800–$4,400 | Advanced adversary simulation |

### WiFi Security Audit Price Ranges
| Audit Type | Scope | Typical Price Range |
| --- | --- | --- |
| Lightweight WiFi audit | 1 site, ≤10 APs, 1–2 SSIDs | $2,500–$7,000 |
| Standard WiFi audit | 1–3 sites, 10–50 APs | $7,500–$18,000 |
| Multi-site audit | 3–10 sites, 50–200 APs | $20,000–$55,000 |
| Enterprise audit | 10+ sites or 200+ APs | $60,000–$150,000+ |

### Wireless Penetration Testing Price Ranges
| Pentest Type | Scope | Typical Price Range |
| --- | --- | --- |
| Small wireless pentest | 1 site, ≤20 APs | $8,000–$20,000 |
| Mid-size wireless pentest | 2–5 sites, 20–100 APs | $20,000–$60,000 |
| Large enterprise pentest | 5–20 sites, 100–500 APs | $60,000–$150,000 |
| Global/very large | 20+ sites or 500+ APs | $150,000–$400,000+ |

### Wireless Pricing Add-ons
- Red-team scenario: +20–50% to base scope.
- IoT/OT wireless focus: +10–40% depending on device complexity.

### Wireless Regional Multipliers
- US/Canada: 1.0 baseline.
- UK & Western Europe: 0.9–1.2.
- Nordics: 1.0–1.2.
- Australia/NZ: 1.0–1.3.
- Eastern Europe: 0.6–0.9.
- LatAm: 0.5–0.8.
- India/SEA: 0.3–0.6.
- Middle East: 0.7–1.1.

### OT/ICS Consulting Hourly Rates
| Provider | Junior/Analyst | Senior Consultant | Principal/Lead |
| --- | --- | --- | --- |
| Claroty (PS or partner) | $125–$175/hr | $200–$300/hr | $300–$425/hr |
| Nozomi Networks | $120–$170/hr | $190–$290/hr | $290–$410/hr |
| Dragos (PS/IR focus) | $150–$210/hr | $250–$350/hr | $350–$500/hr |

### OT/ICS Fixed-Fee Benchmarks
- Single-site visibility assessment: $25k–$75k.
- Multi-site baseline program (3–5 sites): $125k–$350k.
- Segmentation design + rollout planning: $75k–$250k.
- IR readiness + tabletop: $30k–$120k.

### OT/ICS Regional Adjustments
- Western Europe: -10% to -20% vs North America.
- APAC: -15% to -30% depending on market maturity.
- Middle East: +10% to +30% for specialized expertise.

### Penetration Testing Consulting Rates (USD/hr)
| Experience Level | Hourly Rate Range | Notes |
| --- | --- | --- |
| Entry/Junior | $75–$100 | New consultants building reputation |
| Mid-Level | $100–$150 | 3–5 years, OSCP preferred |
| Senior | $150–$250 | 5–10 years, multiple certs |
| Expert/Specialist | $250–$300+ | 10+ years, niche expertise |
| Red Team Lead | $250–$500 | Advanced roles, OSCE3 skills |

### Penetration Testing Day Rates
| Complexity | Seniority | Day Rate | Engagement Length |
| --- | --- | --- | --- |
| Small web app | Junior | $1,000 | 3 days = $3,000 |
| Large complex web app | Senior | $1,500 | 15 days = $22,500 |
| Enterprise network | Expert | $1,500–$2,500 | 10–20 days = $15k–$50k |

### Pentest Project Pricing
| Scope | Typical Range | Notes |
| --- | --- | --- |
| Small companies | $5,000–$10,000 | Project-based |
| Mid-size organizations | $10,000–$30,000 | Project-based |
| Large enterprises | $30,000–$100,000 | Project-based |
| Traditional pentest | $20,000–$50,000 | PTaaS discounts possible |
| High-end specialized | $100,000+ | FedRAMP or red team focus |

### Specialization Rate Potential (Selected)
| Specialization | Rate Potential | Market Demand |
| --- | --- | --- |
| 5G Security | $400–$700+/hr | Growing rapidly |
| Telecom Security | $350–$700+/hr | Steady high demand |
| GRC (ISO 27001, PCI DSS, GDPR) | $300–$500/hr | Always in demand |
| AI/ML Security | $400–$700+/hr | Emerging premium |
| Cloud Security (AWS/Azure) | $400–$700+/hr | Very high demand |
| Penetration Testing | $250–$400/hr | Steady demand |
| Zero Trust Architecture | $350–$600/hr | Growing trend |
| SIEM (Splunk, QRadar) | $200–$350/hr | Steady demand |
| DevSecOps/Secure SDLC | $300–$600/hr | Growing demand |
| OT/ICS Security | $500–$800+/hr | Niche, very high rates |

### Experience-Based Rate Comparison
| Experience Level | Typical Rate |
| --- | --- |
| Entry-level (0–3 years) | $100–$200/hr |
| Mid-level (3–7 years) | $200–$400/hr |
| Senior (7–15 years) | $400–$700/hr |
| Executive/C-Suite | $700–$1,500+/hr |

### Platform Rate Bands
| Platform Type | Typical Rate Range | Best For |
| --- | --- | --- |
| Ultra-premium expert networks | $400–$1,000+/hr | PE due diligence, M&A |
| Cybersecurity-focused networks | $300–$600/hr | CISO advisory |
| High-tier expert networks | $250–$500/hr | General consulting |
| Standard expert networks | $150–$300/hr | Volume and reputation |
| Freelance platforms | $100–$300/hr | Project-based work |

### Highest-Paying Expert Platforms
- GLG: up to $2,000+/hr.
- AlphaSights: up to $1,000/hr.
- Maven: up to $1,000/hr.
- Coleman Research: up to $850/hr.
- CleverX: up to $800/hr.
- Third Bridge: up to $800/hr.
- Capvision: up to $700/hr.
- IANS Research: up to $600/hr.

### Salary Benchmarks (Security Consultant)
| Experience | Annual Salary Range | Hourly Equivalent |
| --- | --- | --- |
| Entry (<1 year) | $59,348–$75,000 | $35–$45/hr |
| Junior (1–3 years) | $75,000–$95,000 | $45–$55/hr |
| Mid-Level (3–7 years) | $95,000–$130,000 | $55–$75/hr |
| Senior (7–12 years) | $130,000–$165,000 | $75–$95/hr |
| Principal (12+ years) | $165,000–$233,000+ | $95–$125/hr |

### Salary Benchmarks (Penetration Tester)
| Experience | Annual Salary | Hourly Equivalent |
| --- | --- | --- |
| Entry (<1 year) | $72,823 | $35–$40/hr |
| Early Career (1–4 years) | $95,326 | $45–$55/hr |
| Mid-Career (4–8 years) | $124,144 | $60–$75/hr |
| Senior (8+ years) | $153,206+ | $75–$95/hr |

### Certification Premiums (Salary Impact)
- CISSP: +15–20% premium.
- CISM: +10–15% premium.
- OSCP: +20–25% premium.
- GIAC (GPEN, GWAPT): +15–20% premium.
- CCIE Security: +25–30% premium.
- AWS/Azure Security: +10–15% premium.
- CEH: +5–10% premium.
- CISSP ROI: +$10k–$15k annual salary.
- OSCP ROI: +$15k–$20k annual salary.
- Multiple certifications: 30–40% cumulative premium.

### Job Market Signals
- Independent contractor cybersecurity roles: 1,126 openings.
- 1099 contractor cyber security roles: 500+ openings.
- Contract 1099 cybersecurity roles: 300+ openings.
- Remote work availability: 60–70% of contractor positions.
- Hybrid availability: 20–25% of contractor positions.
- On-site requirement: 10–15% (government, critical infrastructure).

## Certifications and Frameworks

### Core Security Certifications
- CISSP and CCSP for architecture credibility.
- CISM for security management alignment.
- GIAC certifications (GSEC, GCIH, GCIA, GCED).
- GIAC GPEN and GWAPT for pentest specialization.
- OSCP and OSCE3 for offensive depth.
- CCIE Security for network security architecture.
- Cloud security certifications (AWS, Azure, GCP).

### Architecture and Governance Credentials
- SABSA Foundation/Practitioner.
- TOGAF certification.
- CSA Cloud Controls Matrix familiarity.

### Standards and Frameworks
- NIST Cybersecurity Framework.
- NIST SP 800-53, 800-30 (risk), 800-63 (identity).
- NIST SP 800-207 (Zero Trust Architecture).
- NIST SP 800-82 (ICS security guidance).
- ISO/IEC 27001 and 27002.
- CIS Controls v8.
- OWASP ASVS and SAMM.
- MITRE ATT&CK.
- SABSA and TOGAF.

### Sector-Specific Compliance Signals
- IEC 62443 for industrial security maturity.
- NERC CIP for bulk electric systems.
- TSA Security Directives for pipeline and rail.
- HIPAA, PCI DSS, GDPR for regulated data environments.

## Market Opportunities and Industry Focus

### Zero Trust Industry Opportunities
- Financial services: 1.2–1.5x rate multipliers and $150k–$1.5M budgets.
- Healthcare: 1.1–1.4x multipliers and $120k–$1.2M budgets.
- Government/public sector: 1.2–1.6x multipliers and $200k–$2M budgets.
- Critical infrastructure: 1.3–1.7x multipliers and $250k–$3M budgets.
- Manufacturing/logistics: 1.0–1.3x multipliers and $100k–$1M budgets.

### OT/ICS Opportunity Areas
- Asset discovery and network visibility programs.
- Segmentation planning and zone/conduit design.
- OT SOC integration and alert tuning.
- Incident response readiness and tabletop programs.

### Wireless Opportunity Areas
- WiFi audits for multi-site and enterprise estates.
- Wireless pentests with segmentation validation.
- Rogue AP monitoring and WIPS tuning retainers.
- IoT/OT wireless assessments in industrial facilities.

### Network Segmentation and Firewall Opportunities
- Microsegmentation planning for legacy environments.
- Firewall rule rationalization and policy enforcement mapping.
- Secure remote access for third-party vendors.
- Network segmentation for M&A integration or divestiture.

### Expert Network and Advisory Opportunities
- Expert network consults priced $200–$1,000+/hr.
- Telecom/5G security and zero trust advisory positioned as premium.
- Architecture and vCISO-style retainers for ongoing governance.

## Go-to-Market and Service Packaging

### Zero Trust Packages
- Zero Trust QuickStart Assessment: 4–6 weeks, maturity score and executive briefing.
- Target State Architecture Blueprint: 6–10 weeks, diagrams and policy framework.
- Pilot Implementation Support: 8–16 weeks, vendor setup and onboarding.
- Program Governance Retainer: ongoing KPI reporting and policy tuning.

### Architecture Sprint Packages
- Architecture Assessment Sprint (2–4 weeks) with gap analysis.
- Target Architecture & Reference Patterns (4–8 weeks).
- Zero Trust / Network Segmentation Program (6–12 weeks).
- Fractional Security Architect / vCISO Hybrid engagement.

### Wireless Packages
- Fixed-price WiFi audit by site or AP count.
- Wireless pentest with optional red-team add-on.
- Quarterly monitoring retainer for rogue AP tracking.

### OT/ICS Packages
- Single-site visibility assessment.
- Multi-site baseline program with asset inventory.
- Segmentation design plus rollout planning.
- OT incident response readiness and tabletop exercises.

## Delivery Methodology and Checklists

### Scoping Checklist (Architecture)
- Confirm business objectives and risk appetite.
- Inventory systems, data classifications, and critical dependencies.
- Identify regulatory obligations and audit timelines.
- Determine cloud platforms, identity providers, and key vendors.
- Define decision-making governance and approval paths.
- Agree on deliverables, cadence, and acceptance criteria.
- Validate availability of subject matter experts for discovery.

### Zero Trust Estimation Heuristics
- Each major application domain may require 1–3 weeks of analysis.
- Each network trust zone can require 1–2 weeks of dependency mapping.
- Identity governance and role mining can require 4–8 weeks.
- Add 10–20% project time for stakeholder alignment and governance.

### Wireless Engagement Checklist
- Confirm asset inventory (sites, SSIDs, AP count, controllers).
- Define scope boundaries and rules of engagement.
- Set testing windows and downtime constraints.
- Capture RF survey requirements and onsite access needs.
- Validate segmentation testing requirements (wireless to internal).

### OT/ICS Project Phases
- Scoping and access with stakeholder interviews.
- Visibility and baseline via passive monitoring deployment.
- Risk and gap analysis with IEC 62443 or NIST 800-82 mapping.
- Architecture and controls with zone/conduit segmentation design.
- Monitoring and response with SOC integration and playbooks.

### Risk Register Fields (OT)
- Risk description and impacted asset.
- Impact assessment (safety, uptime, regulatory).
- Likelihood and severity rating.
- Recommended mitigation and owner.

## Metrics and Outcomes
- Risk reduction mapped to threat models.
- Percentage of critical systems aligned to target architecture.
- Reduction in high-severity audit findings.
- Time to approve architecture decisions.
- Adoption rate of standard patterns and templates.
- Reduction in security-related rework in delivery teams.
- Improved incident detection and response times.
- Reduction in privileged accounts (zero trust KPI).
- Decrease in network segments with implicit trust.
- Improvement in MFA coverage and device compliance rates.
- Reduced time to grant or revoke access.

## Tooling and Platforms

### Architecture and Governance Tooling
- Architecture modeling and repository tools.
- Threat modeling and diagramming tools.
- GRC and control mapping platforms.
- Cloud security posture management tools.
- Asset inventory and CMDB tools.
- Secrets management and key management systems.

### Wireless Tooling
- Kismet and Wireshark for wireless reconnaissance.
- Airodump-ng and Aircrack-ng for handshake capture.
- hcxtools for credential capture and validation.
- Nmap and netcat for network mapping.
- WiFi adapters with monitor mode support.
- Directional antennas for targeted RF capture.
- Spectrum analyzer for RF audits.

### OT/ICS Platforms
- Claroty for asset visibility and remote access.
- Nozomi Networks for monitoring and asset inventory.
- Dragos for threat-informed detection and incident readiness.

## Risks, Pitfalls, and Rate Protection

### Common Pricing Pitfalls
- Underestimating stakeholder alignment time.
- Ignoring dependencies on client teams or vendor timelines.
- Failing to include documentation or knowledge transfer.
- Over-scoping deliverables without clear acceptance criteria.
- Assuming immediate access to required system inventories.

### Rate Protection Tactics
- Anchor rates based on specialization and outcomes.
- Reduce scope or phase delivery instead of cutting rates.
- Use blended rate cards to preserve senior advisory time.
- Include change control to protect against scope creep.
- Benchmark against internal hiring costs when justifying premiums.

## Closing Notes
- Align segmentation programs with business-critical workflows to avoid disruption.
- Use fixed-fee packages for defined assessments and T&M for evolving scope.
- Pair certifications with measurable outcomes to defend premium pricing.
- Combine zero trust, wireless, and OT offerings for multi-year transformation value.
