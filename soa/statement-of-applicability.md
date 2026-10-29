# ISO 27001:2022 Statement of Applicability

## Document Information
| Field | Value |
|-------|-------|
| Organization | Progress Technologies |
| ISMS Scope | Design, development, operation, support and delivery of the Progress Technologies data analytics platform (API service) on AWS eu-west-1, company-managed endpoints, identity services and supporting corporate functions. Remote locations only; no company premises. |
| Version | 1.0 (Draft for management approval) |
| Last Updated | 26 October 2026 |
| Author | Devavrat Yadav |
| Original author | Taimuri Jlal (original SoA template and project brief) |
| Approved By | [Name/Role] - pending |
| Next Review | 26 April 2027 |

---

## Control Summary

| Theme | Total | Applicable | Excluded | Implemented | Partial | Planned |
|-------|-------|------------|----------|-------------|---------|---------|
| 5. Organizational | 37 | 37 | 0 | 11 | 23 | 3 |
| 6. People | 8 | 8 | 0 | 6 | 2 | 0 |
| 7. Physical | 14 | 5 | 9 | 1 | 4 | 0 |
| 8. Technological | 34 | 33 | 1 | 15 | 13 | 5 |
| **TOTAL** | **93** | **83** | **10** | **33** | **42** | **8** |

---

## Theme 5: Organizational Controls

| Ref | Control | Applicable | Status | Justification | Evidence Ref |
|-----|---------|------------|--------|---------------|--------------|
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

---

## Theme 6: People Controls

| Ref | Control | Applicable | Status | Justification | Evidence Ref |
|-----|---------|------------|--------|---------------|--------------|
| 6.1 | Screening | Yes | Implemented | Background checks proportionate to access to customer data (R-004), within local employment law. | EV-20 |
| 6.2 | Terms and conditions of employment | Yes | Implemented | Contracts bind staff to security duties, including remote-working obligations (R-004). | EV-20 |
| 6.3 | Information security awareness, education and training | Yes | Partial | Annual awareness and phishing simulation run (R-004, R-007); role-based secure-coding and cloud-admin training planned. | EV-21 |
| 6.4 | Disciplinary process | Yes | Implemented | Formal sanction process deters policy breaches (R-004). | EV-20 |
| 6.5 | Responsibilities after termination or change of employment | Yes | Implemented | Leaver and mover checklist covers access removal, asset return and continuing confidentiality (R-002, R-004). | EV-20, EV-24 |
| 6.6 | Confidentiality or non-disclosure agreements | Yes | Implemented | NDAs for staff, contractors, customers and suppliers (R-004, R-011). | EV-20, EV-13 |
| 6.7 | Remote working | Yes | Partial | The entire workforce is remote, so this is central to scope (R-001, R-002, R-007). Remote working standard issued; home-network guidance and spot-check programme still maturing. | EV-22, EV-23 |
| 6.8 | Information security event reporting | Yes | Implemented | One channel (security mailbox and chat channel) for loss, phishing and suspicious activity, with reporting statistics (R-002, R-007). | EV-50 |

---

## Theme 7: Physical Controls

| Ref | Control | Applicable | Status | Justification | Evidence Ref |
|-----|---------|------------|--------|---------------|--------------|
| 7.1 | Physical security perimeters | No | N/A | EXCLUDED. Progress controls no premises or secure perimeter; all staff work remotely and production runs in AWS. Residual laptop risk (R-002) treated by 8.1 and 7.9. | EV-43 |
| 7.2 | Physical entry | No | N/A | EXCLUDED. No facilities with entry points. Access to information is controlled logically through 5.15, 5.18 and 8.5. | EV-43 |
| 7.3 | Securing offices, rooms and facilities | No | N/A | EXCLUDED. No offices, rooms or facilities. Employee homes are not company facilities; their risk is treated by 6.7, 7.7 and 7.9. | EV-43 |
| 7.4 | Physical security monitoring | No | N/A | EXCLUDED. No premises to monitor. AWS monitors its data centres; assurance obtained under 5.22; logical monitoring by 8.15 and 8.16. | EV-12, EV-43 |
| 7.5 | Protecting against physical and environmental threats | No | N/A | EXCLUDED. No company site exposed to fire, flood or power loss. AWS Availability Zone design inherited (R-005); service impact treated by 5.29, 5.30 and 8.14 (R-006). | EV-12, EV-43 |
| 7.6 | Working in secure areas | No | N/A | EXCLUDED. No secure areas exist. Sensitive work is protected logically through 8.2 and 8.3. | EV-43 |
| 7.7 | Clear desk and clear screen | Yes | Partial | Applies to remote workers in homes, cafes and travel (R-001, R-002, R-007). MDM enforces auto-lock; clear-desk guidance in the remote working standard; no-printing rule. | EV-22, EV-23 |
| 7.8 | Equipment siting and protection | No | N/A | EXCLUDED. No company equipment is sited in company premises; servers are AWS-operated. Endpoint protection covered by 7.9 and 8.1. | EV-24, EV-43 |
| 7.9 | Security of assets off-premises | Yes | Implemented | Primary physical control for the business: laptops are the only company-owned assets outside AWS and are always off-premises (R-002). Full-disk encryption, remote wipe and travel guidance enforced. | EV-23, EV-24 |
| 7.10 | Storage media | Yes | Partial | Laptops and removable media can carry customer-adjacent data (R-002, R-004). USB mass storage restricted by MDM policy; formal media handling rules being finalised. | EV-22, EV-23 |
| 7.11 | Supporting utilities | No | N/A | EXCLUDED. No company site with power, cooling or telecoms. AWS provides resilient utilities for the hosting layer (R-005, R-006). | EV-12, EV-43 |
| 7.12 | Cabling security | No | N/A | EXCLUDED. Progress owns no cabling; networks are home ISPs and AWS. Data in transit protected by 8.24. | EV-43 |
| 7.13 | Equipment maintenance | Yes | Partial | Laptop repair, firmware and warranty servicing must not expose data (R-002). Approved repair route with encrypted disks; firmware patching via MDM. | EV-23, EV-24 |
| 7.14 | Secure disposal or re-use of equipment | Yes | Partial | End-of-life laptops must be wiped and certified (R-002, R-011, R-012). Cloud media sanitisation inherited from AWS; disposal certificates being collected. | EV-24, EV-33 |

---

## Theme 8: Technological Controls

| Ref | Control | Applicable | Status | Justification | Evidence Ref |
|-----|---------|------------|--------|---------------|--------------|
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
| 8.30 | Outsourced development | No | N/A | EXCLUDED. All code is written in-house. Contractors or agencies would trigger re-evaluation; 8.25, 8.28 and 5.19-5.21 are the fall-back controls. | EV-43 |
| 8.31 | Separation of development, test and production environments | Yes | Implemented | Separate AWS accounts keep untested change and customer data out of lower environments (R-001, R-003). | EV-37 |
| 8.32 | Change management | Yes | Implemented | Pull-request approval, CI checks and change records for infrastructure and application (R-003). | EV-27 |
| 8.33 | Test information | Yes | Planned | Test data must not contain real customer data without safeguards (R-001, R-011). Policy approved; synthetic data tooling planned. | EV-38 |
| 8.34 | Protection of information systems during audit testing | Yes | Planned | Audits, scans and penetration tests on production must not disrupt service or expose data (R-001, R-006). Audit-testing protocol to be written. | EV-48 |

---

## Exclusions Summary

| Control Ref | Control Name | Reason for Exclusion | Alternative Measure |
|-------------|--------------|---------------------|---------------------|
| 7.1 | Physical security perimeters | No company premises; remote-first since founding | 8.1, 7.9; AWS data-centre perimeters via 5.22 |
| 7.2 | Physical entry | No facilities with entry points | 5.15, 5.18, 8.5 (logical access) |
| 7.3 | Securing offices, rooms and facilities | No offices, rooms or facilities; home offices are not company facilities | 6.7, 7.7, 7.9, 8.1 |
| 7.4 | Physical security monitoring | No premises to monitor; AWS monitors its data centres | 8.15, 8.16; AWS assurance via 5.22 |
| 7.5 | Protecting against physical and environmental threats | No company site; hosting threats inherited from AWS AZ design | 5.29, 5.30, 8.14; AWS assurance via 5.22 |
| 7.6 | Working in secure areas | No secure areas exist | 8.2, 8.3 (logical segregation of sensitive work) |
| 7.8 | Equipment siting and protection | No company equipment sited on company premises | 7.9, 8.1; AWS-operated servers |
| 7.11 | Supporting utilities | No company site with power, cooling or telecoms; AWS provides hosting utilities | 5.30, 8.14; AWS assurance via 5.22 |
| 7.12 | Cabling security | Progress owns no cabling; networks are home ISPs and AWS | 8.24 (encryption in transit), 8.20 |
| 8.30 | Outsourced development | All development is performed by employees | 8.25, 8.28, 5.19-5.21 as fall-back |

---

## Risk-to-Control Traceability

| Risk ID | Risk Description | Addressing Controls |
|---------|------------------|---------------------|
| R-001 | Unauthorized access to customer data | 5.1, 5.3, 5.12, 5.14, 5.15, 5.16, 5.17, 5.18, 6.7, 7.7, 8.1, 8.2, 8.3, 8.5, 8.11, 8.12, 8.15, 8.16, 8.17, 8.18, 8.20, 8.22, 8.24, 8.26, 8.31, 8.33, C-01 |
| R-002 | Employee laptop theft or loss | 5.9, 5.10, 5.11, 6.5, 6.7, 6.8, 7.7, 7.9, 7.10, 7.13, 7.14, 8.1, 8.24 |
| R-003 | Cloud misconfiguration | 5.1, 5.2, 5.3, 5.7, 5.8, 5.23, 5.25, 5.26, 5.36, 5.37, 8.2, 8.8, 8.9, 8.12, 8.15, 8.16, 8.19, 8.20, 8.22, 8.25, 8.27, 8.31, 8.32 |
| R-004 | Insider threat | 5.2, 5.3, 5.4, 5.10, 5.11, 5.15, 5.16, 5.18, 5.28, 5.36, 6.1, 6.2, 6.3, 6.4, 6.5, 6.6, 7.10, 8.2, 8.3, 8.4, 8.12, 8.15, 8.16, 8.18 |
| R-005 | Third-party breach (AWS) | 5.19, 5.20, 5.21, 5.22, 5.23, 5.29, 5.30, 8.14, 8.21, 8.24, C-03 |
| R-006 | Business continuity failure | 5.24, 5.26, 5.27, 5.29, 5.30, 5.37, 8.6, 8.13, 8.14, 8.34 |
| R-007 | Phishing or credential theft against remote staff | 5.4, 5.6, 5.7, 5.10, 5.17, 6.3, 6.7, 6.8, 7.7, 8.1, 8.5, 8.7, 8.16, 8.23 |
| R-008 | Ransomware or destructive attack on cloud workloads and backups | 5.26, 5.29, 5.30, 8.7, 8.8, 8.13, 8.14, 8.22 |
| R-009 | Software supply-chain compromise | 5.7, 5.19, 5.21, 5.32, 8.4, 8.8, 8.19, 8.25, 8.28, 8.29 |
| R-010 | Secrets or credentials exposed in code or pipelines | 5.17, 8.4, 8.9, 8.19, 8.28, 8.29 |
| R-011 | Non-compliance with GDPR processor duties or customer contract terms | 5.5, 5.12, 5.13, 5.14, 5.20, 5.31, 5.33, 5.34, 6.6, 7.14, 8.10, 8.11, 8.33, C-02, C-03 |
| R-012 | Customer data retained beyond contract or not deleted | 5.12, 5.33, 5.34, 7.14, 8.10, 8.13 |
| R-013 | API abuse: broken authorization, injection or denial of service | 5.8, 8.5, 8.6, 8.15, 8.20, 8.21, 8.25, 8.26, 8.27, 8.28, 8.29, C-01 |

---

## Version History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| Source | - | Taimuri Jlal | Original project brief and SoA template |
| 1.0 | 26 Oct 2026 | Devavrat Yadav | Re-authored for Progress Technologies with full control baseline, dossiers and evidence index |

---

## Approval Signatures

| Role | Name | Date | Signature |
|------|------|------|-----------|
| Information Security Manager | | | |
| Risk Owner | | | |
| Management Representative | | | |
