> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Evidence reference index

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
