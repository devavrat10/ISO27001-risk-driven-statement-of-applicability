> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Theme 5 — Organizational controls (37)

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
