> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Engagement context and ISMS scope

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
