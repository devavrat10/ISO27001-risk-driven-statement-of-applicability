> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Theme 8 — Technological controls (34)

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
