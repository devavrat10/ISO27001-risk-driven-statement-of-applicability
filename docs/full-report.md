# Progress Technologies — Risk-Driven Statement of Applicability (ISO/IEC 27001:2022)

26 October 2026 · Devavrat Yadav (author) · Taimuri Jlal (original author)

Of the 93 Annex A controls, 83 apply to Progress Technologies and 10 are excluded with a defence; at the 26 October 2026 baseline, 33 applicable controls are implemented, 42 partial and 8 planned.

## 1. Document control and authorship

| Field | Value |
| --- | --- |
| Organisation | Progress Technologies |
| Document title | Risk-Driven Statement of Applicability (SoA) and Exclusion Defence Pack |
| Document ID | PT-ISMS-SOA-001 |
| Standard | ISO/IEC 27001:2022 (including Amendment 1:2024), Annex A; guidance from ISO/IEC 27002:2022 |
| Author | Devavrat Yadav |
| Original author | Taimuri Jlal — original project brief, scenario design and SoA template ("Project 02: Justifying a Statement of Applicability in ISO 27001") |
| Version / status | 1.0 — Draft for management approval |
| Date | 26 October 2026 |
| Next review | 26 April 2027, or earlier on any trigger in section 12 |
| Classification | Confidential — internal and external auditors only |
| Distribution | ISMS Steering Group, Risk Owner, certification body (on request) |

**Attribution.** This pack builds on the framework, scenario, risk assessment summary and SoA template created by Taimuri Jlal. Devavrat Yadav has re-authored it for Progress Technologies and extended it with a control-by-control baseline, an evidence index, supplementary risks, auditor Q&A, a gap-closure roadmap and a deviations log (section 21).

## 2. Executive summary

Progress Technologies can defend a proportionate Statement of Applicability: 83 of 93 Annex A controls are applicable, 10 are excluded with documented defences, and every applicable control is tied to an assessed risk or to a legal, contractual or standard requirement. The company is a fully remote, 85-person B2B SaaS analytics provider running 100% on AWS (eu-west-1), so the exclusions fall almost entirely in the physical theme and in outsourced development.

| Headline | Result |
| --- | --- |
| Controls assessed | 93 (37 organizational, 8 people, 14 physical, 34 technological) |
| Applicable / excluded | 83 / 10 |
| Baseline status of the 83 applicable controls | 33 Implemented · 42 Partially implemented · 8 Planned |
| Exclusions defended | 10 controls in 4 defence dossiers (ED-01 to ED-04) |
| Highest-rated risk | R-003 Cloud misconfiguration (Critical) — drives priority on the open gaps in 8.9, 8.16 and 5.26 |
| Target | ISO/IEC 27001:2022 certification within 6 months (by 26 April 2027) |

**Three decisions shape this SoA.**

1. **Physical controls are split, not blanket-excluded.** Nine physical controls (7.1–7.6, 7.8, 7.11, 7.12) are excluded because Progress has no premises or on-premises equipment. Five (7.7, 7.9, 7.10, 7.13, 7.14) stay in scope because every company laptop is permanently off-premises — an auditor would reject excluding them.
2. **Reliance on AWS is not an exclusion of accountability.** Controls 7.4, 7.5 and 7.11 are excluded only because AWS operates the data centres. The defence depends on supplier assurance evidence under 5.19–5.23 (AWS ISO 27001 certificate, SOC reports via AWS Artifact). This is the most contestable exclusion and is the subject of the video walkthrough (section 19).
3. **Status is stated honestly.** Only 33 controls are marked Implemented, each with an evidence reference. Eight controls are Planned and carry dated remediation actions in section 18. No control is marked Implemented without an artefact that can be produced on demand.

**Where the work is.** The largest gaps sit in detection and response maturity (5.26–5.28, 8.16), data protection engineering (8.11, 8.12, 8.33), endpoint web filtering (8.23) and independent assurance (5.35, 5.36). Closing the eight Planned controls and the highest-risk Partial controls before the Stage 1 audit is the critical path.

**What we need from management.** Approve this SoA (section 22), confirm the baseline statuses after the evidence walk-through, ratify the supplementary risks R-007 to R-013, and fund the Wave 1 remediation actions.

## 3. Engagement context and ISMS scope

Progress Technologies is a remote-first B2B SaaS company whose only customer-facing surface is an API running entirely in AWS. That operating model, not the Annex A list, decides what is applicable.

### 3.1 Company profile

| Attribute | Fact | Implication for the SoA |
| --- | --- | --- |
| Business | B2B SaaS data analytics platform | Customer data confidentiality and availability are the core obligations |
| Workforce | 85 employees, fully remote since founding (2021) | Remote working (6.7) and endpoint controls carry the physical-security load |
| Infrastructure | 100% AWS, region eu-west-1; no data centres, server rooms or on-premises equipment | Physical premises controls excluded; AWS shared-responsibility model governs |
| Endpoints | Company-managed laptops only | Endpoint, off-premises and disposal controls remain applicable |
| Customers | 200+ enterprise clients requiring ISO 27001 | Contractual requirements justify inclusion of governance and assurance controls |
| Product | API-only; no end-user application; no mobile app development | Application security (8.26–8.29) applies to the API; no mobile-specific controls needed |
| Cryptography | AWS KMS only; no key generation by Progress | 8.24 still applies — key use, rotation and access rules must be defined |
| Development | In-house; no outsourced development | 8.30 excluded |
| Programme goal | ISO/IEC 27001:2022 certification within 6 months | Stage 1 and Stage 2 audits planned in section 18 |

### 3.2 Proposed ISMS scope statement

> The information security management system covers the design, development, operation, support and delivery of the Progress Technologies data analytics platform (API service), including the supporting AWS production and non-production environments in eu-west-1, the company-managed endpoints and identity services used by all employees, and the corporate functions that govern them. Progress operates from remote locations only; no company-controlled physical premises exist.

| Boundary | In scope | Out of scope (with reason) |
| --- | --- | --- |
| Locations | Employee remote working locations (as an extension of endpoint security) | Company premises — none exist |
| Systems | AWS accounts, CI/CD, source control, IdP, MDM, SaaS tools processing company or customer data | Customer-operated systems and customer-side integrations |
| Services | API platform, support and operations | Marketing website content hosting unless it processes personal data (to be confirmed) |
| Suppliers | AWS and other suppliers listed in the supplier register | Supplier internal controls (covered by assurance, not scope) |

### 3.3 Interested parties and requirements (clause 4.2)

| Interested party | Key requirement | SoA consequence |
| --- | --- | --- |
| Enterprise customers | Certified ISMS, confidentiality of data, availability, breach notification | Governance, supplier, incident and BC controls applicable |
| Regulators and data protection authorities | Lawful processing and breach reporting | 5.5, 5.31, 5.34 applicable |
| AWS and other suppliers | Acceptable use, shared-responsibility compliance | 5.19–5.23 applicable |
| Employees | Clear rules, usable security | 5.10, 6.3, 6.7 applicable |
| Certification body | Defensible SoA, evidence of operation | Honest status, evidence index (section 16) |

Amendment 1:2024 to ISO/IEC 27001:2022 requires the organisation to determine whether climate change is a relevant issue for the ISMS and interested parties. Progress's exposure is indirect (AWS region resilience, remote-worker disruption) and is recorded in the context register (EV-02); it does not add controls.

### 3.4 Regulatory and contractual landscape

The table lists frameworks that commonly apply to an EU-hosted SaaS processor. Applicability must be confirmed by legal counsel; it is recorded here because it justifies inclusion of 5.31 and 5.34.

| Framework | Relevance to Progress | Action |
| --- | --- | --- |
| GDPR | Progress processes customer personal data in the EU as a processor | Maintain RoPA, DPAs, breach procedure (EV-17, EV-18) |
| NIS2 | Depends on Progress's classification and customers' supply-chain requirements | Legal to confirm; align incident reporting timelines in 5.24–5.26 |
| DORA | Applies to financial-sector customers; flows down ICT third-party requirements by contract | Review customer addenda; map to 5.19–5.22 |
| EU AI Act | Relevant only if platform features qualify as AI systems | Legal to confirm; no control change expected now |
| Customer contracts | 200+ security addenda and audit clauses | Track in the legal and contractual register (EV-17) |

## 4. Risk assessment baseline

The SoA is driven by the completed risk assessment (R-001 to R-006) supplemented by seven risks the author proposes for ratification. A control is included only if it treats at least one of these risks, satisfies a legal or contractual requirement, or is a precondition for a control that does.

### 4.1 Source risk register (as assessed by the company)

| Risk ID | Risk description | Likelihood | Impact | Inherent level | Risk owner (proposed) |
| --- | --- | --- | --- | --- | --- |
| R-001 | Unauthorized access to customer data | Medium | High | High | Head of Engineering |
| R-002 | Employee laptop theft or loss | Medium | Medium | Medium | IT Operations Lead |
| R-003 | Cloud misconfiguration | High | High | Critical | Cloud Platform Lead |
| R-004 | Insider threat | Low | High | Medium | Head of People |
| R-005 | Third-party breach (AWS) | Low | Critical | High | Head of Engineering |
| R-006 | Business continuity failure | Low | High | Medium | Head of Operations |

### 4.2 Supplementary risks (author-proposed, pending ratification by the risk owner)

These were identified by applying the scenario facts (remote workforce, API-only SaaS, in-house CI/CD on AWS) to common threat patterns. They are not part of the company's source assessment.

| Risk ID | Risk description | Likelihood | Impact | Inherent level | Why it matters here |
| --- | --- | --- | --- | --- | --- |
| R-007 | Phishing or credential theft against remote staff leading to account takeover | High | Medium | High | Fully remote workforce; identity is the perimeter |
| R-008 | Ransomware or destructive attack on cloud workloads and backups | Low | Critical | High | Availability commitments to 200+ customers |
| R-009 | Software supply-chain compromise (open-source dependencies, CI/CD tooling) | Medium | High | High | In-house development with heavy dependency use |
| R-010 | Secrets or credentials exposed in source code or pipelines | Medium | High | High | Direct path to production AWS access |
| R-011 | Non-compliance with GDPR processor duties or customer contract terms | Medium | High | High | Personal data of customers' end users processed in the EU |
| R-012 | Customer data retained beyond contract or not deleted on request | Medium | Medium | Medium | Data lifecycle in analytics datasets and backups |
| R-013 | API abuse: broken authorization, injection or denial of service | Medium | High | High | The API is the only product surface |

### 4.3 Target residual ratings (proposed)

| Risk ID | Inherent | Target residual after full implementation | Treatment |
| --- | --- | --- | --- |
| R-001 | High | Medium | Treat |
| R-002 | Medium | Low | Treat |
| R-003 | Critical | Medium | Treat (priority) |
| R-004 | Medium | Low | Treat |
| R-005 | High | Medium | Treat and share (supplier assurance, contractual) |
| R-006 | Medium | Low | Treat |
| R-007 | High | Medium | Treat |
| R-008 | High | Medium | Treat |
| R-009 | High | Medium | Treat |
| R-010 | High | Low | Treat |
| R-011 | High | Medium | Treat and share (DPAs, customer terms) |
| R-012 | Medium | Low | Treat |
| R-013 | High | Medium | Treat |

**Methodology observation.** The source assessment states qualitative ratings but not the scoring matrix. An auditor will ask how "Medium × Medium" and "Low × Critical" map to levels. The risk methodology (EV-05) should publish the likelihood and impact definitions and the matrix before Stage 1.

## 5. Methodology and decision framework

This SoA responds to clause 6.1.3 c) and d): it records the necessary controls, why they are included, whether they are implemented, and why any Annex A control is excluded. Annex A is a reference list, not a mandate, so each control is tested against Progress's context.

### 5.1 Applicability test

Each of the 93 controls was passed through the same four questions, in order.

1. **Does the control treat an assessed risk (R-001 to R-013)?** If yes, it is applicable, and the justification names the risk IDs.
2. **Is it required by law, regulation or a customer contract?** If yes, it is applicable and the basis is named.
3. **Does the control's subject exist in Progress's environment?** Examples: premises, on-premises equipment, outsourced developers. If the subject does not exist, move to the exclusion test.
4. **Is the risk the control addresses already treated by a different applicable control, or inherited from a supplier?** If so, the control may be excluded only if the replacement or inherited measure is named and evidenced.

### 5.2 Exclusion test (all five must pass)

| # | Test | Evidence of passing |
| --- | --- | --- |
| 1 | The control's subject matter does not exist in the ISMS scope | Non-applicability dossier (EV-43) |
| 2 | No assessed risk depends on the control | Risk register cross-check (section 15) |
| 3 | Any residual risk is treated by a named alternative control or inherited supplier control | Alternative measures mapping (section 14) |
| 4 | Inherited controls are backed by current supplier assurance | AWS Artifact reports, supplier review (EV-12) |
| 5 | A re-evaluation trigger is defined | Exclusion register (section 12) |

### 5.3 Implementation status definitions

| Status | Meaning | Auditor expectation |
| --- | --- | --- |
| Implemented | Fully operational; evidence available on demand | Records of operation, metrics or logs |
| Partial | Some elements operate; gaps documented | Evidence for the parts in place plus a dated remediation plan |
| Planned | Not yet operating; committed | Project plan, owner, resource allocation, target date |
| N/A (Excluded) | Control not applicable | Documented justification and alternative measures |

**Rule: never mark a control Implemented unless its evidence reference can be produced on demand.** The baseline statuses in this pack are the author's assessed starting position derived from the scenario; each must be confirmed in an evidence walk-through with the control owner before the SoA is approved. Any control that fails the walk-through is downgraded to Partial.

### 5.4 Justification categories

Every justification in sections 7 to 10 names its driver using risk IDs. Where a legal or contractual driver applies, it is stated in words (for example GDPR processor duty or customer security addendum).

## 6. Statement of Applicability summary

| Theme | Total | Applicable | Excluded | Implemented | Partial | Planned |
| --- | --- | --- | --- | --- | --- | --- |
| 5. Organizational | 37 | 37 | 0 | 11 | 23 | 3 |
| 6. People | 8 | 8 | 0 | 6 | 2 | 0 |
| 7. Physical | 14 | 5 | 9 | 1 | 4 | 0 |
| 8. Technological | 34 | 33 | 1 | 15 | 13 | 5 |
| **Total** | **93** | **83** | **10** | **33** | **42** | **8** |

Implemented, Partial and Planned sum to the applicable total in every row. Statuses are the baseline at 26 October 2026 and are subject to the evidence walk-through described in section 5.3.

**Key exclusions**

1. **7.1, 7.2, 7.3, 7.6 (4 controls):** premises, entry and secure areas — Progress has no premises (ED-01).
2. **7.4, 7.5, 7.11 (3 controls):** monitoring, environmental threats and utilities — inherited from AWS data centres, backed by supplier assurance (ED-02).
3. **7.8, 7.12 (2 controls):** equipment siting and cabling — no company-owned equipment sited on premises and no company cabling (ED-03).
4. **8.30 (1 control):** outsourced development — all code is written in-house (ED-04).

**Risk coverage.** All thirteen risks (R-001 to R-013) are treated by at least six applicable controls each; the full matrix is in section 15. No risk depends solely on an excluded control.

## 7. Theme 5 — Organizational controls (37)

All 37 organizational controls are applicable: governance, supplier, incident, continuity and legal controls are the backbone of the ISMS for a cloud-only SaaS company. Baseline: 11 Implemented, 23 Partial, 3 Planned. Evidence references (EV-nn) are defined in section 16.

| Ref | Control | Applicable | Status | Justification (risk link) | Evidence Ref |
| --- | --- | --- | --- | --- | --- |
| 5.1 | Policies for information security | Yes | Implemented | Governance anchor of the ISMS (clause 5.2); direction for treating R-001 and R-003; customer contracts require a documented policy set. | EV-01 |
| 5.2 | Information security roles and responsibilities | Yes | Implemented | Names accountable owners for ISMS, risk and cloud security in a fully remote organisation (R-001, R-003, R-004). | EV-03 |
| 5.3 | Segregation of duties | Yes | Partial | Limits single-person misuse of production and admin rights (R-001, R-003, R-004). Peer-approved deployments operate; break-glass and small-team admin overlap need compensating review. | EV-11, EV-27 |
| 5.4 | Management responsibilities | Yes | Implemented | Management directs and enforces compliance across a remote workforce (R-004, R-007). | EV-03, EV-04 |
| 5.5 | Contact with authorities | Yes | Partial | Needed for GDPR breach notification and incident escalation (R-001, R-011). Contact list exists; escalation paths untested. | EV-35 |
| 5.6 | Contact with special interest groups | Yes | Partial | Low-cost source of cloud-threat and vulnerability bulletins (R-003, R-007). Memberships to be formalised. | EV-35 |
| 5.7 | Threat intelligence | Yes | Partial | Feeds R-003, R-007 and R-009 from AWS and vendor advisories. Triage SLA and reporting not yet formal. | EV-34 |
| 5.8 | Information security in project management | Yes | Partial | Security gate for new features and infrastructure changes (R-003, R-013). Gate not yet mandatory for every project type. | EV-40 |
| 5.9 | Inventory of information and other associated assets | Yes | Partial | Unknown assets cannot be protected (R-001, R-002, R-003). Laptops tracked in MDM and AWS resources in AWS Config; information asset owners incomplete. | EV-07, EV-24 |
| 5.10 | Acceptable use of information and other associated assets | Yes | Implemented | Sets endpoint, SaaS and data-handling behaviour for remote staff (R-002, R-004, R-007); acknowledged at onboarding. | EV-08 |
| 5.11 | Return of assets | Yes | Implemented | Prevents leavers retaining laptops or data (R-002, R-004). Courier return and reconciliation process used for remote leavers. | EV-20, EV-24 |
| 5.12 | Classification of information | Yes | Partial | Drives encryption, access and retention for customer data (R-001, R-011, R-012). Scheme approved; tagging of cloud data stores in progress. | EV-09 |
| 5.13 | Labelling of information | Yes | Planned | Proportionate labelling only: document footers and cloud resource tags (R-001, R-011). Automated tagging scheduled in Wave 1. | EV-09 |
| 5.14 | Information transfer | Yes | Partial | Controls transfer of customer and internal data via TLS, approved sharing tools and NDAs (R-001, R-011). Customer data export rules being finalised. | EV-09, EV-30 |
| 5.15 | Access control | Yes | Implemented | Least-privilege, role-based access to AWS and SaaS (R-001, R-004). | EV-10, EV-11 |
| 5.16 | Identity management | Yes | Implemented | Central identity provider with joiner-mover-leaver lifecycle (R-001, R-004). | EV-11, EV-46 |
| 5.17 | Authentication information | Yes | Implemented | Password manager, MFA and secrets manager for machine credentials (R-001, R-007, R-010). | EV-44, EV-46 |
| 5.18 | Access rights | Yes | Partial | Quarterly AWS access reviews operate; extension to all SaaS applications outstanding (R-001, R-004). | EV-11 |
| 5.19 | Information security in supplier relationships | Yes | Partial | AWS and other suppliers hold customer data or underpin the service (R-005, R-009). Supplier tiering in progress. | EV-12 |
| 5.20 | Addressing information security within supplier agreements | Yes | Partial | Security and data-protection terms with AWS and sub-processors (R-005, R-011). Customer flow-down clauses under review. | EV-13 |
| 5.21 | Managing information security in the ICT supply chain | Yes | Partial | Open-source dependencies and CI/CD tooling are the main ICT supply chain (R-009). Dependency scanning live; SBOM and formal standard not yet produced. | EV-12, EV-26 |
| 5.22 | Monitoring, review and change management of supplier services | Yes | Partial | Ongoing assurance over AWS (R-005) and the evidence base for inherited physical controls. Annual review of AWS certificates and reports being scheduled. | EV-12 |
| 5.23 | Information security for use of cloud services | Yes | Implemented | Core control for a 100% AWS company: cloud security standard and shared-responsibility matrix define who secures what (R-003, R-005). | EV-14, EV-31 |
| 5.24 | Information security incident management planning and preparation | Yes | Implemented | Defined incident roles, severity model and reporting channels (R-001, R-006). | EV-15 |
| 5.25 | Assessment and decision on information security events | Yes | Partial | Triage criteria defined; evidence of consistent event classification still thin (R-001, R-003). | EV-15, EV-28 |
| 5.26 | Response to information security incidents | Yes | Partial | Playbooks for cloud credential compromise and data exposure; not yet validated by a tabletop exercise (R-001, R-003, R-006, R-008). | EV-15 |
| 5.27 | Learning from information security incidents | Yes | Partial | Post-incident review template exists; limited operating history to evidence (R-003, R-006). | EV-15 |
| 5.28 | Collection of evidence | Yes | Planned | Forensic readiness (log retention, snapshot and chain-of-custody procedure) needed for customer and regulator enquiries (R-001, R-004). | EV-15, EV-28 |
| 5.29 | Information security during disruption | Yes | Partial | Keeps security controls effective during outage and failover (R-005, R-006, R-008). | EV-16 |
| 5.30 | ICT readiness for business continuity | Yes | Partial | Multi-AZ design in place; cross-region recovery test pending (R-005, R-006, R-008). | EV-16, EV-29 |
| 5.31 | Legal, statutory, regulatory and contractual requirements | Yes | Implemented | 200+ enterprise contracts, GDPR processing in eu-west-1 and customer security addenda tracked in a register (R-011). | EV-17 |
| 5.32 | Intellectual property rights | Yes | Partial | Software and open-source licence compliance for platform code (R-009). Licence register and scanning to be completed. | EV-42 |
| 5.33 | Protection of records | Yes | Partial | Protects audit trails, contracts and security records (R-011, R-012). Retention schedule approved; immutable log storage being rolled out. | EV-41 |
| 5.34 | Privacy and protection of PII | Yes | Partial | Progress acts as processor of customer personal data (R-011, R-012). RoPA, DPAs and DSAR procedure operate; DPIA coverage incomplete. | EV-18 |
| 5.35 | Independent review of information security | Yes | Planned | Independent assurance on ISMS design and operation (clause 9.2). First internal audit scheduled before Stage 1. | EV-19 |
| 5.36 | Compliance with policies, rules and standards for information security | Yes | Partial | Checked through AWS Config and MDM compliance reports (R-003, R-004); manager attestation cycle not yet running. | EV-19, EV-23, EV-31 |
| 5.37 | Documented operating procedures | Yes | Partial | Runbooks for deployment, access, incident and backup held in the wiki (R-003, R-006); ownership and review dates incomplete. | EV-39 |

## 8. Theme 6 — People controls (8)

All eight people controls apply. With no premises to rely on, people and endpoint controls carry the security load for a remote workforce. Baseline: 6 Implemented, 2 Partial.

| Ref | Control | Applicable | Status | Justification (risk link) | Evidence Ref |
| --- | --- | --- | --- | --- | --- |
| 6.1 | Screening | Yes | Implemented | Background checks proportionate to access to customer data (R-004), within local employment law. | EV-20 |
| 6.2 | Terms and conditions of employment | Yes | Implemented | Contracts bind staff to security duties, including remote-working obligations (R-004). | EV-20 |
| 6.3 | Information security awareness, education and training | Yes | Partial | Annual awareness and phishing simulation run (R-004, R-007); role-based secure-coding and cloud-admin training planned. | EV-21 |
| 6.4 | Disciplinary process | Yes | Implemented | Formal sanction process deters policy breaches (R-004). | EV-20 |
| 6.5 | Responsibilities after termination or change of employment | Yes | Implemented | Leaver and mover checklist covers access removal, asset return and continuing confidentiality (R-002, R-004). | EV-20, EV-24 |
| 6.6 | Confidentiality or non-disclosure agreements | Yes | Implemented | NDAs for staff, contractors, customers and suppliers (R-004, R-011). | EV-20, EV-13 |
| 6.7 | Remote working | Yes | Partial | The entire workforce is remote, so this is central to scope (R-001, R-002, R-007). Remote working standard issued; home-network guidance and spot-check programme still maturing. | EV-22, EV-23 |
| 6.8 | Information security event reporting | Yes | Implemented | One channel (security mailbox and chat channel) for loss, phishing and suspicious activity, with reporting statistics (R-002, R-007). | EV-50 |

## 9. Theme 7 — Physical controls (14)

Nine physical controls are excluded and five remain applicable. The source brief anticipated 11 exclusions; this pack keeps 7.7, 7.9, 7.10, 7.13 and 7.14 in scope because every company laptop is a permanently off-premises asset (see section 21, deviation D-01). Baseline of the five applicable controls: 1 Implemented, 4 Partial. Exclusion defences are in section 13 (ED-01 to ED-03).

| Ref | Control | Applicable | Status | Justification (risk link) | Evidence Ref |
| --- | --- | --- | --- | --- | --- |
| 7.1 | Physical security perimeters | No | N/A | **Excluded (ED-01).** Progress controls no premises or secure perimeter; all staff work remotely and production runs in AWS. Residual laptop risk (R-002) treated by 8.1 and 7.9. | EV-43 |
| 7.2 | Physical entry | No | N/A | **Excluded (ED-01).** No facilities with entry points. Access to information is controlled logically through 5.15, 5.18 and 8.5. | EV-43 |
| 7.3 | Securing offices, rooms and facilities | No | N/A | **Excluded (ED-01).** No offices, rooms or facilities. Employee homes are not company facilities; their risk is treated by 6.7, 7.7 and 7.9. | EV-43 |
| 7.4 | Physical security monitoring | No | N/A | **Excluded (ED-02).** No premises to monitor. AWS monitors its data centres; assurance obtained under 5.22; logical monitoring by 8.15 and 8.16. | EV-12, EV-43 |
| 7.5 | Protecting against physical and environmental threats | No | N/A | **Excluded (ED-02).** No company site exposed to fire, flood or power loss. AWS Availability Zone design inherited (R-005); service impact treated by 5.29, 5.30 and 8.14 (R-006). | EV-12, EV-43 |
| 7.6 | Working in secure areas | No | N/A | **Excluded (ED-01).** No secure areas exist. Sensitive work is protected logically through 8.2 and 8.3. | EV-43 |
| 7.7 | Clear desk and clear screen | Yes | Partial | Applies to remote workers in homes, cafés and travel (R-001, R-002, R-007). MDM enforces auto-lock; clear-desk guidance in the remote working standard; no-printing rule. | EV-22, EV-23 |
| 7.8 | Equipment siting and protection | No | N/A | **Excluded (ED-03).** No company equipment is sited in company premises; servers are AWS-operated. Endpoint protection covered by 7.9 and 8.1. | EV-24, EV-43 |
| 7.9 | Security of assets off-premises | Yes | Implemented | Primary physical control for the business: laptops are the only company-owned assets outside AWS and are always off-premises (R-002). Full-disk encryption, remote wipe and travel guidance enforced. | EV-23, EV-24 |
| 7.10 | Storage media | Yes | Partial | Laptops and removable media can carry customer-adjacent data (R-002, R-004). USB mass storage restricted by MDM policy; formal media handling rules being finalised. | EV-22, EV-23 |
| 7.11 | Supporting utilities | No | N/A | **Excluded (ED-02).** No company site with power, cooling or telecoms. AWS provides resilient utilities for the hosting layer (R-005, R-006). | EV-12, EV-43 |
| 7.12 | Cabling security | No | N/A | **Excluded (ED-03).** Progress owns no cabling; networks are home ISPs and AWS. Data in transit protected by 8.24. | EV-43 |
| 7.13 | Equipment maintenance | Yes | Partial | Laptop repair, firmware and warranty servicing must not expose data (R-002). Approved repair route with encrypted disks; firmware patching via MDM. | EV-23, EV-24 |
| 7.14 | Secure disposal or re-use of equipment | Yes | Partial | End-of-life laptops must be wiped and certified (R-002, R-011, R-012). Cloud media sanitisation inherited from AWS; disposal certificates being collected. | EV-24, EV-33 |

## 10. Theme 8 — Technological controls (34)

33 technological controls apply; 8.30 (outsourced development) is excluded. Baseline of the 33: 15 Implemented, 13 Partial, 5 Planned. 8.24 remains applicable even though Progress generates no keys, because using KMS still requires rules for key use, rotation and access. Application controls 8.26 to 8.29 apply to the API even though there is no end-user application.

| Ref | Control | Applicable | Status | Justification (risk link) | Evidence Ref |
| --- | --- | --- | --- | --- | --- |
| 8.1 | User endpoint devices | Yes | Implemented | Laptops are the main access point to customer-adjacent systems (R-001, R-002, R-007). MDM enforces encryption, patching, EDR and screen lock. | EV-23 |
| 8.2 | Privileged access rights | Yes | Partial | Admin rights to AWS accounts concentrated in few roles (R-001, R-003, R-004). Just-in-time elevation and periodic review being completed. | EV-11 |
| 8.3 | Information access restriction | Yes | Implemented | Restricts customer data to authorised roles and service identities through IAM, resource policies and per-account separation (R-001, R-004). | EV-11, EV-37 |
| 8.4 | Access to source code | Yes | Implemented | Source code and infrastructure-as-code are core IP and the path to production (R-004, R-009, R-010). Organisation SSO, branch protection and least-privilege repositories. | EV-26 |
| 8.5 | Secure authentication | Yes | Implemented | SSO with MFA for all users and stronger methods for administrators; conditional access (R-001, R-007, R-013). | EV-46 |
| 8.6 | Capacity management | Yes | Partial | Platform availability under customer load (R-006, R-013). Auto-scaling and dashboards exist; capacity forecasting not formal. | EV-36 |
| 8.7 | Protection against malware | Yes | Implemented | EDR and anti-malware on all laptops; workload protection in AWS (R-007, R-008). | EV-23 |
| 8.8 | Management of technical vulnerabilities | Yes | Partial | Scanning of hosts, containers and dependencies (R-003, R-008, R-009). Remediation SLAs and reporting not yet consistently evidenced. | EV-25 |
| 8.9 | Configuration management | Yes | Partial | Treats R-003 (Critical) and R-010: baselines via infrastructure-as-code and AWS Config rules. Drift remediation, exception process and secrets-in-config checks still maturing. | EV-31 |
| 8.10 | Information deletion | Yes | Partial | Deletion of customer data at contract end and of data on retired laptops (R-011, R-012). Offboarding runbook exists; deletion verification evidence limited. | EV-33 |
| 8.11 | Data masking | Yes | Planned | Analytics datasets need masking in non-production and support access (R-001, R-011). Design approved; implementation scheduled in Wave 1. | EV-38 |
| 8.12 | Data leakage prevention | Yes | Planned | Prevents exfiltration through insiders or misconfiguration (R-001, R-003, R-004). S3 public-access blocks exist; endpoint and egress DLP planned. | EV-49 |
| 8.13 | Information backup | Yes | Partial | AWS Backup policies configured with encryption and retention aligned to contracts (R-006, R-008, R-012). Scheduled restore-test evidence missing. | EV-29 |
| 8.14 | Redundancy of information processing facilities | Yes | Implemented | Multi-AZ architecture for production services (R-005, R-006, R-008). | EV-16, EV-32 |
| 8.15 | Logging | Yes | Implemented | CloudTrail, VPC flow logs, application and identity-provider logs centralised (R-001, R-003, R-004, R-013). | EV-28 |
| 8.16 | Monitoring activities | Yes | Partial | GuardDuty and Security Hub alerts reviewed (R-001, R-003, R-004, R-007). Alert tuning and out-of-hours response still maturing. | EV-28 |
| 8.17 | Clock synchronization | Yes | Implemented | Systems use AWS Time Sync, giving reliable log correlation for investigations (R-001). | EV-47 |
| 8.18 | Use of privileged utility programs | Yes | Partial | Admin tools (session manager, CLI, database consoles) can bypass application controls (R-001, R-004). Use is restricted and logged; formal tool inventory pending. | EV-11, EV-28 |
| 8.19 | Installation of software on operational systems | Yes | Implemented | Production software deployed only through CI/CD from reviewed code (R-003, R-009, R-010); endpoint software governed by MDM. | EV-26, EV-31 |
| 8.20 | Networks security | Yes | Implemented | VPC design, security groups and WAF protect API endpoints (R-001, R-003, R-013). | EV-32 |
| 8.21 | Security of network services | Yes | Partial | Relies on AWS network services and their assurance (R-005, R-013). Service security requirements documented; supplier evidence review ongoing. | EV-32, EV-12 |
| 8.22 | Segregation of networks | Yes | Implemented | Separate AWS accounts and VPC segments for production and non-production (R-001, R-003, R-008). | EV-32, EV-37 |
| 8.23 | Web filtering | Yes | Planned | Reduces phishing and malware exposure on remote laptops (R-007). DNS filtering through MDM scheduled in Wave 1. | EV-45 |
| 8.24 | Use of cryptography | Yes | Implemented | Encryption at rest and in transit using AWS KMS keys (R-001, R-002, R-005). Progress generates no keys but defines key use, rotation and access rules. | EV-30 |
| 8.25 | Secure development life cycle | Yes | Implemented | Defines security activities from design to release (R-003, R-009, R-013). | EV-26 |
| 8.26 | Application security requirements | Yes | Partial | API-only product: authentication, authorisation, rate limiting and input validation requirements (R-001, R-013). Documented requirement set still being completed. | EV-26 |
| 8.27 | Secure system architecture and engineering principles | Yes | Partial | Secure-by-design patterns for AWS (R-003, R-013). Principles exist; threat modelling not yet routine. | EV-14, EV-32 |
| 8.28 | Secure coding | Yes | Partial | Secure coding standard, peer review, SAST and secret scanning (R-009, R-010, R-013). Developer role-based training links to 6.3. | EV-26 |
| 8.29 | Security testing in development and acceptance | Yes | Partial | SAST, SCA and DAST in pipeline plus annual third-party penetration test (R-009, R-010, R-013). Acceptance criteria not formalised. | EV-25, EV-26 |
| 8.30 | Outsourced development | No | N/A | **Excluded (ED-04).** All code is written in-house. Contractors or agencies would trigger re-evaluation; 8.25, 8.28 and 5.19–5.21 are the fall-back controls. | EV-43 |
| 8.31 | Separation of development, test and production environments | Yes | Implemented | Separate AWS accounts keep untested change and customer data out of lower environments (R-001, R-003). | EV-37 |
| 8.32 | Change management | Yes | Implemented | Pull-request approval, CI checks and change records for infrastructure and application (R-003). | EV-27 |
| 8.33 | Test information | Yes | Planned | Test data must not contain real customer data without safeguards (R-001, R-011). Policy approved; synthetic data tooling planned. | EV-38 |
| 8.34 | Protection of information systems during audit testing | Yes | Planned | Audits, scans and penetration tests on production must not disrupt service or expose data (R-001, R-006). Audit-testing protocol to be written. | EV-48 |

## 11. Controls beyond Annex A

Clause 6.1.3 b) requires the organisation to determine all controls necessary, then compare them with Annex A to confirm none was omitted. Three controls specific to a multi-tenant, EU-hosted SaaS provider are added; they are not Annex A controls and do not change the 93-control count.

| Ref | Additional control | Rationale (risk link) | Related Annex A | Status | Evidence Ref |
| --- | --- | --- | --- | --- | --- |
| C-01 | Logical tenant isolation for customer data in the multi-tenant platform | Cross-tenant exposure is the most damaging form of R-001 and R-013; tested in design and penetration testing | 8.3, 8.22, 8.26 | Partial | EV-25, EV-32 |
| C-02 | EU data residency enforcement and sub-processor transparency | Customers and GDPR expect processing in eu-west-1 (R-011); region restrictions applied through AWS organisation policies | 5.20, 5.31, 8.9 | Partial | EV-13, EV-37 |
| C-03 | Customer assurance handling: security questionnaires, audit-rights requests and a shared-responsibility statement | 200+ enterprise customers drive contractual obligations (R-005, R-011) | 5.19, 5.31 | Planned | EV-12, EV-17 |

## 12. Exclusion register

Ten controls are excluded. Each passes the five-part exclusion test in section 5.2. Any re-evaluation trigger below, once met, requires the SoA to be reissued before the change goes live.

| Ref | Control | Dossier | Reason for exclusion | Alternative or inherited measure | Re-evaluation trigger |
| --- | --- | --- | --- | --- | --- |
| 7.1 | Physical security perimeters | ED-01 | No company premises; remote-first since founding | 8.1, 7.9; AWS data-centre perimeters via 5.22 | Lease or ownership of any premises |
| 7.2 | Physical entry | ED-01 | No facilities with entry points | 5.15, 5.18, 8.5 (logical access) | Any premises or shared workspace holding company assets |
| 7.3 | Securing offices, rooms and facilities | ED-01 | No offices, rooms or facilities; home offices are not company facilities | 6.7, 7.7, 7.9, 8.1 | Company-controlled office, storage room or lab |
| 7.4 | Physical security monitoring | ED-02 | No premises to monitor; AWS monitors its data centres | 8.15, 8.16; AWS assurance via 5.22 | Loss of AWS assurance evidence or move to non-AWS hosting |
| 7.5 | Protecting against physical and environmental threats | ED-02 | No company site; hosting threats inherited from AWS AZ design | 5.29, 5.30, 8.14; AWS assurance via 5.22 | Move to single-AZ or non-AWS hosting; AWS assurance gap |
| 7.6 | Working in secure areas | ED-01 | No secure areas exist | 8.2, 8.3 (logical segregation of sensitive work) | Creation of a secure room or lab |
| 7.8 | Equipment siting and protection | ED-03 | No company equipment sited on company premises | 7.9, 8.1; AWS-operated servers | Any on-premises server, network or storage equipment |
| 7.11 | Supporting utilities | ED-02 | No company site with power, cooling or telecoms; AWS provides hosting utilities | 5.30, 8.14; AWS assurance via 5.22 | Any company-operated site or equipment room |
| 7.12 | Cabling security | ED-03 | Progress owns no cabling; networks are home ISPs and AWS | 8.24 (encryption in transit), 8.20 | Any company-owned network infrastructure |
| 8.30 | Outsourced development | ED-04 | All development is performed by employees | 8.25, 8.28, 5.19–5.21 as fall-back | Use of any external developer, agency or offshore team |

**General re-evaluation triggers** apply in addition: new product lines handling different data, new hosting regions or providers, acquisition, a major incident traced to an excluded control, or a customer or regulator requirement that names an excluded control.

## 13. Auditor defence dossiers

Four dossiers defend the ten exclusions. Each follows the same structure: exclusion statement, business context, risk linkage, evidence of non-applicability, anticipated auditor questions and re-evaluation conditions. The consolidated question bank is in section 17.

### ED-01 — Premises cluster: 7.1, 7.2, 7.3, 7.6

**Exclusion statement.** Physical security perimeters, physical entry, securing offices, rooms and facilities, and working in secure areas are not applicable to Progress Technologies.

**Business context.** Progress has been fully remote since founding. It has no office, data centre, server room, equipment store or secure area. Employees work from their own locations on company-managed laptops. The product runs entirely in AWS eu-west-1.

**Risk linkage.** The physical risks these controls would address are treated elsewhere.

| Physical risk | Treating control | Reference |
| --- | --- | --- |
| Theft or loss of equipment | 8.1 User endpoint devices; 7.9 Security of assets off-premises | Disk encryption, remote wipe, MDM (EV-23) |
| Unauthorised access to information | 5.15, 5.18, 8.5 | IAM, access reviews, SSO and MFA (EV-11, EV-46) |
| Exposure of documents or screens | 7.7, 5.10 | Auto-lock, clear-desk guidance, no-printing rule (EV-08, EV-22) |

**Evidence of non-applicability (EV-43).** Company registration showing a registered-agent address only; absence of leases or serviced-office contracts in the finance ledger; AWS billing showing 100% cloud infrastructure; HR policy confirming remote-first status; asset register and MDM roster showing laptops as the only physical assets.

**Anticipated questions.**

- *What about employees' home offices?* Home offices are not company facilities. Security of devices used there is addressed by 6.7, 7.7, 7.9 and 8.1.
- *What about rented meeting spaces or co-working desks?* Temporary use does not store company equipment or data; data remains in AWS and on encrypted laptops. Any recurring or contracted space triggers re-evaluation.
- *What about physical mail at the registered address?* The registered agent forwards scanned mail; no sensitive information is sent by post. To be confirmed by the Head of Operations.
- *How do you protect sensitive work without secure areas (7.6)?* Sensitive access is logical, restricted by 8.2 and 8.3 and logged by 8.15.

**Re-evaluation conditions.** Lease or ownership of premises; any shared workspace holding company equipment; creation of a secure room or lab.

### ED-02 — Hosting environment cluster: 7.4, 7.5, 7.11

**Exclusion statement.** Physical security monitoring, protection against physical and environmental threats, and supporting utilities are not applicable as controls operated by Progress. They are operated by AWS for the data centres hosting the service, and Progress relies on that through documented supplier assurance.

**Business context.** Progress owns no data centre or equipment room. AWS operates power, cooling, fire suppression, surveillance and physical access for the Availability Zones in eu-west-1. Progress remains accountable for choosing a resilient architecture (multi-AZ), backups and recovery.

**Risk linkage.**

| Physical risk | Treating control | Reference |
| --- | --- | --- |
| Physical compromise of a data centre (R-005) | 5.19–5.23 supplier assurance | AWS ISO 27001 certificate and SOC reports via AWS Artifact (EV-12) |
| Fire, flood or power loss at a hosting site (R-005, R-006) | 5.29, 5.30, 8.14 | Multi-AZ design, DR plan, restore tests (EV-16, EV-29) |
| Undetected physical intrusion | 8.15, 8.16 | Logical monitoring; AWS physical monitoring evidenced through its audit reports (EV-28, EV-12) |

**Evidence of non-applicability and inheritance (EV-43, EV-12).** AWS billing and architecture diagrams showing no non-AWS hosting; current AWS certificates and SOC reports reviewed within the last 12 months with reviewer sign-off; shared-responsibility matrix (EV-14).

**Anticipated questions.**

- *Is excluding these controls the same as ignoring the risk?* No. R-005 stays in the risk register and is treated by 5.19–5.23, 5.29, 5.30 and 8.14. The exclusion removes only controls Progress itself would operate.
- *How do you know AWS's physical controls work?* Through AWS's independent certifications and audit reports, reviewed annually under 5.22 and recorded with reviewer name, date and any exceptions.
- *What if an AWS report contains an exception or the certificate lapses?* The supplier review escalates to the risk owner; the exclusion is re-evaluated and the SoA reissued if the exception affects physical or environmental controls.
- *Where does AWS's responsibility end and yours begin?* The shared-responsibility matrix in the cloud security standard (EV-14) assigns region and AZ selection, backups and recovery to Progress.
- *What if a staff member's home loses power?* Cloud-hosted work continues from another location; staff availability is handled in the business continuity plan (EV-16).

**Re-evaluation conditions.** Move to non-AWS or single-AZ hosting; loss or qualification of AWS assurance evidence; operation of any company-controlled site or equipment room.

### ED-03 — Equipment cluster: 7.8, 7.12

**Exclusion statement.** Equipment siting and protection, and cabling security, are not applicable because Progress owns no equipment sited on premises and no cabling.

**Business context.** The only company-owned equipment is laptops and standard peripherals, which are always off-premises and are covered by 7.9, 7.13 and 8.1. Servers and network equipment are AWS-operated. Progress does not own, install or maintain cabling.

**Risk linkage.**

| Physical risk | Treating control | Reference |
| --- | --- | --- |
| Damage or interference with laptops | 7.9, 7.13 | MDM compliance and approved repair route (EV-23, EV-24) |
| Interception of data in transit | 8.24, 8.20 | TLS everywhere, WAF and network controls (EV-30, EV-32) |
| Overlooking of screens in public | 7.7 | Remote working standard (EV-22) |

**Evidence of non-applicability (EV-43).** Asset register with no servers, network equipment or cabling; MDM roster; AWS billing; finance ledger with no hardware purchases other than laptops and peripherals.

**Anticipated questions.**

- *Laptops are equipment — why exclude 7.8?* 7.8 addresses siting equipment in controlled locations. For laptops used off-premises the specific control is 7.9, which is applicable and implemented.
- *What about the home router and cabling?* They belong to the employee or ISP, not to Progress. The remote working standard sets wireless security expectations and data is protected by encryption in transit.
- *What about docking stations and peripherals?* They are tracked as laptop accessories in the asset register and covered by 5.9 and 5.11.

**Re-evaluation conditions.** Any on-premises server, network or storage equipment; any company-owned network infrastructure.

### ED-04 — Outsourced development: 8.30

**Exclusion statement.** Outsourced development is not applicable because all software for the platform is written by Progress employees.

**Business context.** The company has no external developer, agency, offshore team or commissioned development contract. Contractors and freelancers are not used for development.

**Risk linkage.**

| Risk if the control were needed | Treating control | Reference |
| --- | --- | --- |
| Malicious or insecure code from an external party (R-009, R-010) | 8.25, 8.28, 8.29 | Secure SDLC, review and testing (EV-26) |
| Supplier handling of source code (R-009) | 5.19–5.21, 8.4 | Supplier due diligence and repository access control (EV-12, EV-26) |

**Evidence of non-applicability (EV-43).** Source repository contributor list reconciled quarterly to the HR employee roster; supplier register with no development suppliers; contractor register showing none engaged in engineering.

**Anticipated questions.**

- *Do you use contractors or freelancers?* No. The contributor-to-roster reconciliation proves it each quarter.
- *Are open-source libraries or AI coding assistants outsourced development?* No. Open-source components are managed under 5.21, 8.8 and 8.28. AI coding tools are treated as suppliers under 5.19 and 5.23 with review requirements under 8.28. This is the stated position and should be confirmed with the certification body.
- *What happens if you engage a contractor next quarter?* The engagement is a re-evaluation trigger: the SoA is updated, 8.30 becomes applicable and contract, access and code-review requirements are applied before access is granted.

**Re-evaluation conditions.** Any external developer, agency or offshore team; use of commissioned custom development for any component.

## 14. Alternative measures mapping

Every physical-theme control has a named treatment: an applicable control that Progress operates, an AWS-inherited control backed by assurance, or a documented statement that the subject does not exist. The source brief's mapping is retained where sound and corrected where an alternative control would not satisfy an auditor (7.7, 7.9, 7.10, 7.13, 7.14 are applicable, not substituted).

| Physical control | Disposition | How the risk is still addressed | Reference |
| --- | --- | --- | --- |
| 7.1 Physical security perimeters | Excluded | Endpoint security for laptops; AWS data-centre perimeters through supplier assurance | 8.1, 5.22 |
| 7.2 Physical entry | Excluded | Logical access control replaces physical entry control | 5.15, 5.18, 8.5 |
| 7.3 Securing offices, rooms and facilities | Excluded | Remote working standard, screen-lock and off-premises asset controls | 6.7, 7.7, 7.9 |
| 7.4 Physical security monitoring | Excluded | Logical monitoring in AWS; AWS physical monitoring evidenced in audit reports | 8.15, 8.16, 5.22 |
| 7.5 Protecting against physical and environmental threats | Excluded | AWS AZ design inherited; Progress multi-AZ, DR and continuity controls | 5.22, 5.29, 5.30, 8.14 |
| 7.6 Working in secure areas | Excluded | No secure areas; logical segregation of sensitive access | 8.2, 8.3 |
| 7.7 Clear desk and clear screen | **Applicable** | MDM auto-lock plus clear-desk guidance for homes and public places | 7.7, 8.1, 6.7 |
| 7.8 Equipment siting and protection | Excluded | No on-premises equipment; laptops covered by off-premises control | 7.9, 8.1 |
| 7.9 Security of assets off-premises | **Applicable** | Encrypted, MDM-managed laptops with remote wipe | 7.9, 8.1, 8.24 |
| 7.10 Storage media | **Applicable** | Restricted removable media; deletion and encryption controls | 7.10, 8.10, 8.24 |
| 7.11 Supporting utilities | Excluded | AWS provides hosting utilities; Progress designs for resilience | 5.22, 5.30, 8.14 |
| 7.12 Cabling security | Excluded | No company cabling; encryption in transit protects data on third-party networks | 8.24, 8.20 |
| 7.13 Equipment maintenance | **Applicable** | Approved repair route, firmware patching and laptop refresh policy | 7.13, 8.1 |
| 7.14 Secure disposal or re-use of equipment | **Applicable** | Certified wipe at end of life; cloud sanitisation inherited from AWS | 7.14, 8.10, 5.11 |

**Compensating-control caution.** An alternative control is accepted by an auditor only if it is itself implemented and evidenced. Where the alternative is still Partial (for example 8.10), the exclusion defence relies on the remediation plan in section 18.

## 15. Risk-to-control traceability matrix

Every risk is treated by at least six applicable controls, and every applicable control cites at least one risk or a legal, contractual or standard requirement. The only control with no risk ID is 5.35, which is driven by ISO/IEC 27001 clause 9.2 and by customers' expectation of an audited ISMS.

| Risk ID | Risk | Inherent level | Applicable treating controls | Inherited or excluded measures relied on |
| --- | --- | --- | --- | --- |
| R-001 | Unauthorized access to customer data | High | 5.1, 5.3, 5.12, 5.14, 5.15, 5.16, 5.17, 5.18, 6.7, 7.7, 8.1, 8.2, 8.3, 8.5, 8.11, 8.12, 8.15, 8.16, 8.17, 8.18, 8.20, 8.22, 8.24, 8.26, 8.31, 8.33, C-01 | — |
| R-002 | Employee laptop theft or loss | Medium | 5.9, 5.10, 5.11, 6.5, 6.7, 6.8, 7.7, 7.9, 7.10, 7.13, 7.14, 8.1, 8.24 | 7.1, 7.3, 7.8 excluded; treated by 7.9 and 8.1 |
| R-003 | Cloud misconfiguration | Critical | 5.1, 5.2, 5.3, 5.7, 5.8, 5.23, 5.25, 5.26, 5.36, 5.37, 8.2, 8.8, 8.9, 8.12, 8.15, 8.16, 8.19, 8.20, 8.22, 8.25, 8.27, 8.31, 8.32 | — |
| R-004 | Insider threat | Medium | 5.2, 5.3, 5.4, 5.10, 5.11, 5.15, 5.16, 5.18, 5.28, 5.36, 6.1, 6.2, 6.3, 6.4, 6.5, 6.6, 7.10, 8.2, 8.3, 8.4, 8.12, 8.15, 8.16, 8.18 | 7.2, 7.6 excluded; treated by logical access controls |
| R-005 | Third-party breach (AWS) | High | 5.19, 5.20, 5.21, 5.22, 5.23, 5.29, 5.30, 8.14, 8.21, 8.24, C-03 | 7.4, 7.5, 7.11 excluded; inherited from AWS under 5.22 |
| R-006 | Business continuity failure | Medium | 5.24, 5.26, 5.27, 5.29, 5.30, 5.37, 8.6, 8.13, 8.14, 8.34 | 7.5, 7.11 excluded; AWS resilience plus Progress multi-AZ |
| R-007 | Phishing or credential theft of remote staff | High | 5.4, 5.6, 5.7, 5.10, 5.17, 6.3, 6.7, 6.8, 7.7, 8.1, 8.5, 8.7, 8.16, 8.23 | — |
| R-008 | Ransomware or destructive attack | High | 5.26, 5.29, 5.30, 8.7, 8.8, 8.13, 8.14, 8.22 | — |
| R-009 | Software supply-chain compromise | High | 5.7, 5.19, 5.21, 5.32, 8.4, 8.8, 8.19, 8.25, 8.28, 8.29 | 8.30 excluded; fall-back if development is outsourced |
| R-010 | Secrets or credentials exposed in code or pipelines | High | 5.17, 8.4, 8.9, 8.19, 8.28, 8.29 | — |
| R-011 | Non-compliance with GDPR or customer contracts | High | 5.5, 5.12, 5.13, 5.14, 5.20, 5.31, 5.33, 5.34, 6.6, 7.14, 8.10, 8.11, 8.33, C-02, C-03 | — |
| R-012 | Data retained beyond contract or not deleted | Medium | 5.12, 5.33, 5.34, 7.14, 8.10, 8.13 | — |
| R-013 | API abuse: broken authorization, injection or denial of service | High | 5.8, 8.5, 8.6, 8.15, 8.20, 8.21, 8.25, 8.26, 8.27, 8.28, 8.29, C-01 | — |

**Reading the matrix.** R-003, the only Critical risk, is treated by 23 applicable controls, but 8.9, 8.16 and 5.26 are Partial; closing those three is the highest-value remediation in section 18.

## 16. Evidence reference index

Each evidence reference (EV-nn) identifies an artefact that must be producible on demand before the related control is shown as Implemented. Owners are proposed roles; systems of record are indicative and should be replaced with the tools in use.

**Evidence handling rules.** Exports are timestamped and read-only; operating evidence is retained for at least the certification cycle (three years) or the contractual minimum if longer; configuration evidence is sampled across the audit period, not only taken on the audit date; evidence for excluded controls (EV-43) is refreshed at each management review.

| ID | Evidence artefact | Proposed owner | System of record (indicative) | Cadence | Primary controls |
| --- | --- | --- | --- | --- | --- |
| EV-01 | Information security policy, approved by management | ISMS Manager | Policy repository | Annual | 5.1 |
| EV-02 | ISMS scope statement and context register (incl. climate-change consideration) | ISMS Manager | Policy repository | Annual | Clauses 4.1–4.3 |
| EV-03 | Roles and responsibilities matrix, appointment records | ISMS Manager | Policy repository | On change | 5.2, 5.4 |
| EV-04 | Management review minutes and ISMS KPI pack | Executive sponsor | Document store | Quarterly | 5.4, clause 9.3 |
| EV-05 | Risk assessment methodology (criteria, matrix) and risk register | Risk Owner | Risk register | Semi-annual | Clause 6.1.2 |
| EV-06 | Risk treatment plan | Risk Owner | Risk register | Semi-annual | Clause 6.1.3 |
| EV-07 | Information asset register with owners and classification | IT Operations Lead | Asset inventory | Quarterly | 5.9 |
| EV-08 | Acceptable use policy and signed acknowledgements | Head of People | HR system | Onboarding and annual | 5.10 |
| EV-09 | Classification and handling standard; labelling and transfer rules | ISMS Manager | Policy repository | Annual | 5.12, 5.13, 5.14 |
| EV-10 | Access control policy | Head of Engineering | Policy repository | Annual | 5.15 |
| EV-11 | Identity and access configuration exports and quarterly access review records | Cloud Platform Lead | Identity provider, AWS IAM | Quarterly | 5.3, 5.15, 5.16, 5.18, 8.2, 8.3, 8.18 |
| EV-12 | Supplier register, due-diligence files and AWS assurance reviews (certificates, SOC reports) | Procurement and ISMS Manager | Supplier register, AWS Artifact | Annual per supplier | 5.19, 5.21, 5.22, 7.4, 7.5, 7.11, 8.21 |
| EV-13 | Supplier contracts, DPAs, NDAs and security addenda | Legal | Contract repository | On signature and renewal | 5.20, 5.14, 6.6 |
| EV-14 | Cloud security standard and shared-responsibility matrix | Cloud Platform Lead | Policy repository | Annual | 5.23, 8.27 |
| EV-15 | Incident response plan, playbooks, incident log, post-incident reviews, tabletop reports | Security Lead | Ticketing system | Per incident; tabletop annually | 5.24, 5.25, 5.26, 5.27, 5.28 |
| EV-16 | Business impact analysis, continuity and DR plans, DR test reports | Head of Operations | Document store | Annual test | 5.29, 5.30, 8.14 |
| EV-17 | Legal and contractual requirements register | Legal | Document store | Semi-annual | 5.31 |
| EV-18 | Record of processing, DPIAs, DSAR procedure and log | Data Protection Lead | Privacy register | Semi-annual | 5.34 |
| EV-19 | Internal audit programme, reports and corrective actions | ISMS Manager | Audit tracker | Annual | 5.35, 5.36 |
| EV-20 | Screening records, contracts, disciplinary policy, leaver and mover checklists | Head of People | HR system | Per event | 5.11, 6.1, 6.2, 6.4, 6.5, 6.6 |
| EV-21 | Awareness training completion reports and phishing simulation results | Head of People | Training platform | Annual; simulations quarterly | 6.3 |
| EV-22 | Remote working and endpoint standard | IT Operations Lead | Policy repository | Annual | 6.7, 7.7, 7.10 |
| EV-23 | MDM compliance exports: encryption, patching, EDR, screen lock, removable media | IT Operations Lead | MDM console | Continuous; monthly snapshot | 8.1, 8.7, 7.7, 7.9, 7.10, 7.13, 5.36 |
| EV-24 | Laptop asset register, issue and return logs, disposal certificates | IT Operations Lead | Asset register | Per event; quarterly reconciliation | 5.9, 5.11, 6.5, 7.9, 7.13, 7.14 |
| EV-25 | Vulnerability scan reports, remediation SLA tracker, penetration test reports | Security Lead | Scanner, ticketing | Continuous; pen test annually | 8.8, 8.29 |
| EV-26 | Secure SDLC policy, pipeline configuration, SAST, SCA, DAST outputs, code review records | Head of Engineering | Source control, CI/CD | Continuous | 8.4, 8.19, 8.25, 8.26, 8.28, 8.29, 5.21 |
| EV-27 | Change records and pull-request approvals | Head of Engineering | Source control, ticketing | Continuous | 8.32, 5.3 |
| EV-28 | Logging and monitoring configuration, alert runbooks, alert review records | Security Lead | AWS logging and security services | Continuous | 8.15, 8.16, 5.25, 5.28, 8.18 |
| EV-29 | Backup configuration and restore test records | Cloud Platform Lead | AWS Backup | Quarterly test | 8.13, 5.30 |
| EV-30 | Cryptography policy, KMS key policies and rotation settings, TLS scan results | Cloud Platform Lead | AWS KMS, scanner | Quarterly | 8.24, 5.14 |
| EV-31 | Configuration baselines (infrastructure-as-code), AWS Config and conformance results | Cloud Platform Lead | Code repository, AWS Config | Continuous | 8.9, 5.23, 8.19, 5.36 |
| EV-32 | Network architecture diagrams, VPC and security group configuration, WAF rules | Cloud Platform Lead | Architecture repository, AWS | Semi-annual | 8.14, 8.20, 8.21, 8.22, 8.27 |
| EV-33 | Retention schedule, deletion logs, customer offboarding runbook | Data Protection Lead | Runbook wiki, AWS logs | Per event | 8.10, 7.14 |
| EV-34 | Threat intelligence subscriptions and triage log | Security Lead | Ticketing system | Weekly | 5.7 |
| EV-35 | Contact list for authorities and special interest groups | Security Lead | Document store | Semi-annual | 5.5, 5.6 |
| EV-36 | Capacity dashboards and auto-scaling configuration | Cloud Platform Lead | AWS monitoring | Continuous | 8.6 |
| EV-37 | AWS organisation structure, account separation, service control policies | Cloud Platform Lead | AWS Organizations | Semi-annual | 8.3, 8.22, 8.31 |
| EV-38 | Test data policy and masking or synthetic data scripts | Head of Engineering | Code repository | Annual | 8.11, 8.33 |
| EV-39 | Operating procedures and runbooks with owners and review dates | Process owners | Runbook wiki | Annual | 5.37 |
| EV-40 | Project security gate checklist and completed gates | Project office | Project tracker | Per project | 5.8 |
| EV-41 | Records retention policy and immutable log storage configuration | Legal and Cloud Platform Lead | Policy repository, AWS | Annual | 5.33 |
| EV-42 | Software licence register and open-source licence scan results | Head of Engineering | CI/CD, register | Per release | 5.32 |
| EV-43 | Non-applicability dossier: registration, billing, HR policy, asset register, contributor roster | ISMS Manager | Document store | At each management review | 7.1–7.6, 7.8, 7.11, 7.12, 8.30 |
| EV-44 | Secrets management configuration and secret-scanning results | Cloud Platform Lead | AWS, CI/CD | Continuous | 5.17 |
| EV-45 | DNS and web filtering policy and endpoint configuration | IT Operations Lead | MDM console | Continuous | 8.23 |
| EV-46 | SSO and MFA enforcement and conditional access configuration | IT Operations Lead | Identity provider | Quarterly | 5.16, 5.17, 8.5 |
| EV-47 | Time synchronisation configuration | Cloud Platform Lead | AWS, infrastructure-as-code | Annual | 8.17 |
| EV-48 | Audit and penetration test rules of engagement and read-only access procedure | Security Lead | Document store | Per engagement | 8.34 |
| EV-49 | Data leakage controls: public-access blocks, egress rules, DLP configuration | Cloud Platform Lead | AWS, MDM | Continuous | 8.12 |
| EV-50 | Event reporting channel and reporting statistics | Security Lead | Ticketing, chat | Monthly | 6.8 |

## 17. Auditor challenge preparation

These are the questions a certification-body auditor is most likely to ask about the SoA, beyond those in the dossiers. Answers are written for the control owner to speak to, with the evidence to have open.

| # | Likely question | Model answer | Evidence to show |
| --- | --- | --- | --- |
| 1 | You have no premises. Why are five physical controls applicable? | The subject of 7.7, 7.9, 7.10, 7.13 and 7.14 exists: every company laptop is off-premises. Excluding them would leave the main physical risk (R-002) untreated. | SoA section 9; MDM export (EV-23); asset register (EV-24) |
| 2 | Why is 7.8 excluded but 7.9 included? | 7.8 concerns equipment sited in controlled locations; Progress has none. Laptops outside such locations fall under 7.9. | ED-03; EV-43 |
| 3 | Your SoA shows only 33 controls as implemented. Is that acceptable? | Yes. Status reflects evidence. Partial and Planned controls have owners, dates and remediation actions; marking them Implemented without evidence would be the nonconformity. | Section 18 roadmap; EV-06 |
| 4 | Show me the evidence for one Implemented control chosen by me. | Provide the evidence reference from the SoA and open the artefact, with dates across the audit period. | Any EV-nn in section 16 |
| 5 | You excluded 7.4, 7.5 and 7.11 because of AWS. Show me AWS's assurance. | Open the AWS certificates and SOC reports from AWS Artifact, the dated review, reviewer name and any exceptions noted. | EV-12; shared-responsibility matrix (EV-14) |
| 6 | Does Progress use cryptography? You say you generate no keys. | Yes. 8.24 covers use of cryptography, including KMS key policies, rotation and TLS. Progress does not generate its own key material, which reduces but does not remove the requirement. | EV-30 |
| 7 | You have no mobile app. Why is application security applicable? | The API is the product. 8.26 to 8.29 apply to it; mobile development would add nothing because none exists. | EV-26, EV-25 |
| 8 | Do staff use personal phones for work email, chat or MFA? | To be confirmed by IT. If personal phones access company data, a mobile device rule must be added under 8.1 and 6.7; if used only as authenticators, 5.17 and 8.5 cover it. | EV-22, EV-46 |
| 9 | How is the SoA kept current? | Reviewed at management review and on any trigger in section 12, with version history and approval recorded. | Section 22; EV-04 |
| 10 | Why is 5.13 labelling applicable for a cloud-only company? | Labelling is proportionate: document footers and cloud resource tags. It supports classification-based handling of customer data (R-001, R-011). | EV-09 |
| 11 | How do you know the remaining residual risks are acceptable? | Target residual ratings are Medium or Low and approved by the risk owner; Medium residuals on R-001, R-003, R-005 and others are accepted formally. | EV-05, EV-06 |
| 12 | What happens to the SoA if you open an office? | 7.1 to 7.6 and 7.8, 7.11, 7.12 are re-evaluated before occupation and the SoA is reissued; the scope statement is amended. | Section 12; EV-43 |
| 13 | Who approved this SoA and when? | The approval table in section 22 records name, role and date. | Section 22 |

## 18. Implementation roadmap and gap-closure plan

Certification by 26 April 2027 is achievable if the eight Planned controls and the highest-risk Partial controls are closed before the internal audit, leaving at least three months of operating records for Stage 2. Audit dates are targets; the certification body has not been confirmed and must schedule both stages.

### 18.1 Phases and gates

| Phase | Dates | Objective | Exit gate |
| --- | --- | --- | --- |
| 0. Baseline and approval | 26 Oct – 20 Nov 2026 | Evidence walk-through of all 33 Implemented controls; ratify R-007 to R-013; publish risk scoring matrix; assemble EV-43 dossier; approve SoA v1.0 | G1: SoA approved by management |
| 1. Wave 1 remediation | 23 Nov 2026 – 29 Jan 2027 | Close the 8 Planned controls and priority Partial controls in section 18.2 | G2: Wave 1 actions closed or risk-accepted |
| 2. Internal audit and management review | 1 – 19 Feb 2027 | First internal audit of ISMS and SoA; management review; corrective actions | G3: Stage 1 readiness confirmed |
| 3. Stage 1 audit | Week of 1 Mar 2027 | Documentation and readiness review by certification body | G4: Stage 1 findings issued |
| 4. Wave 2 remediation | 8 Mar – 9 Apr 2027 | Close Stage 1 findings and remaining Partial controls; refresh evidence | G5: Stage 2 readiness |
| 5. Stage 2 audit and decision | Week of 12 Apr 2027; decision by 26 Apr 2027 | Operating effectiveness audit; certification decision | Certificate issued |

### 18.2 Priority remediation actions

Owners are proposed roles; dates are proposals for management approval.

| ID | Control | Action | Owner | Due | Risk addressed |
| --- | --- | --- | --- | --- | --- |
| A-01 | Baseline | Confirm whether any staff access company data from personal phones; if so add mobile rule to 8.1 and 6.7 | IT Operations Lead | 20 Nov 2026 | R-002, R-007 |
| A-02 | Method | Publish risk scoring matrix and likelihood and impact criteria | Risk Owner | 20 Nov 2026 | All |
| A-03 | ED-01 to ED-04 | Assemble non-applicability dossier (EV-43) including contributor-to-roster reconciliation | ISMS Manager | 20 Nov 2026 | All exclusions |
| A-04 | 5.22 | Complete and sign off the annual AWS assurance review; schedule reviews for other suppliers | ISMS Manager | 4 Dec 2026 | R-005 |
| A-05 | 8.34 (Planned) | Write audit and penetration test protocol with read-only access rules | Security Lead | 4 Dec 2026 | R-001, R-006 |
| A-06 | 8.23 (Planned) | Deploy DNS and web filtering to all laptops through MDM | IT Operations Lead | 11 Dec 2026 | R-007 |
| A-07 | 5.13 (Planned) | Apply classification tags to cloud data stores and standard document footers | ISMS Manager | 18 Dec 2026 | R-001, R-011 |
| A-08 | 5.28 (Planned) | Approve evidence-collection and forensic-readiness procedure; confirm log retention | Security Lead | 18 Dec 2026 | R-001, R-004 |
| A-09 | 5.18 | Extend quarterly access reviews to all SaaS applications | Cloud Platform Lead | 18 Dec 2026 | R-001, R-004 |
| A-10 | 8.9 | Enable configuration drift detection and exception process for infrastructure-as-code | Cloud Platform Lead | 15 Jan 2027 | R-003, R-010 |
| A-11 | 8.16 | Tune alerts and define out-of-hours escalation | Security Lead | 15 Jan 2027 | R-003, R-007 |
| A-12 | 8.8 | Set remediation SLAs and monthly vulnerability reporting | Security Lead | 15 Jan 2027 | R-003, R-008, R-009 |
| A-13 | 8.11 (Planned) | Implement data masking for non-production and support access | Head of Engineering | 15 Jan 2027 | R-001, R-011 |
| A-14 | 8.33 (Planned) | Deploy synthetic test data and prohibit production data in lower environments | Head of Engineering | 15 Jan 2027 | R-001, R-011 |
| A-15 | 5.26 | Run a tabletop exercise on cloud credential compromise and record lessons | Security Lead | 22 Jan 2027 | R-001, R-003, R-006 |
| A-16 | 8.2 | Implement just-in-time privileged access for AWS administrators | Cloud Platform Lead | 22 Jan 2027 | R-001, R-003, R-004 |
| A-17 | 8.12 (Planned) | Implement egress controls and endpoint DLP rules | Cloud Platform Lead | 29 Jan 2027 | R-001, R-003, R-004 |
| A-18 | 8.13, 5.30 | Perform and record a restore test and a cross-region recovery test | Cloud Platform Lead | 29 Jan 2027 | R-006, R-008 |
| A-19 | 6.3 | Launch role-based secure-coding and cloud-admin training | Head of People | 29 Jan 2027 | R-004, R-007, R-013 |
| A-20 | 5.35 (Planned) | Complete first independent internal audit of the ISMS | ISMS Manager | 12 Feb 2027 | Clause 9.2 |

## 19. Video walkthrough script — the most controversial exclusion

The most contestable exclusion is the AWS-inherited cluster 7.4, 7.5 and 7.11 (ED-02), because it depends on a supplier rather than on a fact about Progress. The script runs about five minutes at a steady speaking pace.

| Time | On screen | Narration |
| --- | --- | --- |
| 0:00–0:30 | Title slide, then SoA row for 7.5 | "I'm Devavrat Yadav. In Progress Technologies' Statement of Applicability, controls 7.4, 7.5 and 7.11 are marked not applicable because AWS runs the data centres. That is the exclusion an auditor is most likely to challenge, so I'll defend it in five minutes." |
| 0:30–1:15 | Architecture diagram: remote laptops, AWS eu-west-1 | "Progress has 85 remote staff, no offices and no servers. The platform runs entirely on AWS in eu-west-1. Physical security monitoring, fire and flood protection, and power and cooling are things AWS builds, runs and is audited on. Progress has no site where it could operate these controls." |
| 1:15–2:15 | Exclusion test table (section 5.2) | "Excluding a control is not the same as ignoring a risk. The risk, third-party breach of AWS, is R-005, and it stays in our register. What I removed is only the controls Progress itself would operate. The risk is treated by supplier controls 5.19 to 5.23, and by our own resilience controls 5.29, 5.30 and 8.14: multi-AZ design, recovery plans and restore tests. The exclusion passes only if five tests pass, including that the inherited control is backed by current evidence." |
| 2:15–3:15 | AWS Artifact reports, review record, shared-responsibility matrix | "Here is the evidence. These are AWS's current ISO 27001 certificate and SOC reports, downloaded from AWS Artifact. This is our annual review: who reviewed, when, what scope, and what exceptions were noted. And this is our shared-responsibility matrix, which says that region and availability-zone choice, backups and recovery belong to Progress, not AWS." |
| 3:15–4:15 | ED-02 question list | "Three challenges to expect. First: how do you know AWS's controls work? Answer: independent audit reports, reviewed annually. Second: what if a report shows an exception? Answer: it goes to the risk owner, the exclusion is re-evaluated and the SoA is reissued if physical or environmental controls are affected. Third: isn't this just trusting a supplier? Answer: it is relying on a supplier with evidence, which is what 5.22 requires." |
| 4:15–5:00 | Re-evaluation triggers; closing slide | "The exclusion stays valid only while three things hold: we host only on AWS, we use multiple availability zones, and our AWS assurance evidence is current. If any changes, we re-evaluate. And if the auditor prefers, the fallback is simple: mark these three controls applicable, implemented by inheritance from AWS, with the same evidence. Either way the risk is treated and the position is defensible. Thank you." |

**Recording checklist.** Have the three evidence artefacts open and dated before recording; do not show customer data; keep the on-screen SoA version number visible; state the date of the AWS review aloud.

## 20. Reflection questions

**1. Which exclusion was hardest to justify?** 7.5 (with 7.4 and 7.11). The other exclusions rest on facts about Progress — no premises, no cabling, no outsourced developers. These three rest on AWS, so the defence is only as strong as the supplier assurance evidence under 5.22. That is why A-04 (the AWS assurance review) is an early action.

**2. Which inclusion was a surprise?** The five physical controls that remain applicable (7.7, 7.9, 7.10, 7.13, 7.14). A company with no premises appears to have no physical controls, but every laptop is a permanently off-premises asset. Other surprises: 8.24 applies although Progress generates no keys; 8.26 to 8.29 apply to an API with no end-user application; and 5.13 labelling applies in a light form.

**3. How would the SoA change if the company opened one physical office?** Most of the nine excluded physical controls would be re-evaluated before occupation. 7.1 to 7.5 and 7.7 would become fully applicable and new evidence would be needed: visitor and access records, office network controls under 8.20, monitoring with privacy review, and a continuity plan for loss of the office. 7.6, 7.11 and 7.12 might stay excluded if the landlord provides utilities and cabling and no secure area exists, but each would need a documented decision. The scope statement, asset register and risk register would change, and the SoA would be reissued.

**4. Where did the risk assessment drive a different decision than instinct?** Instinct says a cloud-only company excludes physical controls wholesale; R-002 (laptop loss) kept five of them. R-003 (Critical) shifted attention from policy documents to 8.9, 8.16 and 5.26, where the gaps are. Instinct also suggests dropping 8.18 (privileged utilities) and 8.34 (audit testing) as marginal in the cloud; R-001, R-004 and R-006 keep both applicable.

**5. What is the cost of over-including controls?** Every applicable control needs an owner, an evidence artefact, periodic review and exposure to audit sampling. Including 7.2 would demand visitor logs for visitors who never arrive, and the only ways to satisfy it are to invent evidence or to accept a nonconformity. Over-inclusion also dilutes attention from the controls that treat R-003, and marking aspirational controls Implemented creates credibility damage with the certification body that outlasts the audit.

## 21. Appendix — deliverables cross-reference, deviations, assumptions and limitations

### 21.1 Cross-reference to the original project brief

| Original deliverable (Taimuri Jlal brief) | Where delivered | Note |
| --- | --- | --- |
| Complete SoA, all 93 controls addressed | Sections 7–10 | 93 of 93 addressed |
| Minimum 5 detailed exclusion justifications | Sections 12 and 13 | 10 controls excluded in 4 dossiers |
| Alternative measures mapping | Section 14 | All 14 physical controls mapped |
| Risk-to-control traceability matrix | Section 15 | 13 risks |
| Evidence reference index | Section 16 | 50 evidence references |
| Auditor challenge preparation | Sections 13 and 17 | Dossier questions plus consolidated bank |
| 5-minute video walkthrough | Section 19 | Script delivered; the recording is for the author to produce |
| Reflection questions | Section 20 | All five answered |

The brief's success criteria are met: risk-driven inclusions, defended exclusions, honest status, documented alternative measures, anticipated pushback and clear business context. None of the brief's red flags applies: not all 93 controls are applicable, justifications are risk-specific, and not all controls are marked Implemented.

### 21.2 Deviations from the source brief

| ID | Source brief | This pack | Reason |
| --- | --- | --- | --- |
| D-01 | Physical theme: 3 applicable, 11 excluded; alternative-measures table treats 7.7, 7.9, 7.10, 7.13 and 7.14 as covered by 8.x controls | 5 applicable, 9 excluded | An auditor will not accept excluding the control for off-premises assets when every laptop is off-premises; 8.x controls support but do not replace them |
| D-02 | Illustrative summary: 78 applicable, 15 excluded, 62 Implemented, 12 Partial, 4 Planned; exclusions in themes 5 and 8 | 83 applicable, 10 excluded, 33 Implemented, 42 Partial, 8 Planned; no theme 5 exclusions; only 8.30 excluded in theme 8 | Source figures were a template example. No organizational control is excludable for this scenario, and statuses are set conservatively against evidence |
| D-03 | 7.4 alternatively addressed by 8.16 monitoring; 7.5 by AWS SOC 2 | 7.4, 7.5 and 7.11 treated as AWS-inherited, backed by ISO 27001 and SOC evidence reviewed under 5.22 | Logical monitoring does not replace physical monitoring; inheritance needs documented review to be defensible |
| D-04 | Risk register R-001 to R-006 | Extended with R-007 to R-013, flagged as pending ratification | Remote-workforce, supply-chain, ransomware, secrets, privacy and API risks were otherwise unrepresented |
| D-05 | Company named as in the original brief | Company is Progress Technologies; all scenario facts retained as given | Requested by the author; facts to be confirmed against Progress's actual records |
| D-06 | ISO/IEC 27001:2022 | Also references Amendment 1:2024 (climate-change consideration in clauses 4.1 and 4.2) | Current edition of the standard |

### 21.3 Assumptions to be validated

- Baseline statuses, owners and evidence artefacts are assessed from the scenario and are not confirmed records. Each Implemented control needs an evidence walk-through before approval.
- Proposed owner roles and indicative systems of record must be replaced with Progress's actual roles and tools.
- The founding year (2021), headcount (85), customer count (200+) and the AWS region (eu-west-1) are taken from the original brief.
- No personal mobile devices access company data (open question, action A-01).
- Registered-agent mail contains no sensitive information (to be confirmed by the Head of Operations).
- No certification body has been selected; audit dates in section 18 are targets.
- Regulatory applicability (NIS2, DORA, EU AI Act) requires confirmation by legal counsel.

### 21.4 Limitations

This document is a consulting-style work product for a case-study engagement. It does not reproduce the text of ISO/IEC 27001 or 27002, is not legal advice, and does not replace the judgement of the certification body. Control titles follow the Annex A titles in the source template.

## 22. Approval and version history

### 22.1 Version history

| Version | Date | Author | Changes |
| --- | --- | --- | --- |
| Source | — | Taimuri Jlal | Original project brief, scenario, risk summary and SoA template |
| 1.0 | 26 October 2026 | Devavrat Yadav | Re-authored for Progress Technologies: control-by-control baseline, exclusion dossiers, evidence index, supplementary risks R-007 to R-013, auditor Q&A, roadmap, video script |

### 22.2 Approval

This SoA takes effect once all three approvers have signed. Names, dates and signatures are left blank for completion by Progress Technologies.

| Role | Name | Date | Signature |
| --- | --- | --- | --- |
| Prepared by (Author) | Devavrat Yadav | 26 October 2026 |  |
| Information Security Manager |  |  |  |
| Risk Owner |  |  |  |
| Management Representative |  |  |  |
