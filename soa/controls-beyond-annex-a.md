> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Controls beyond Annex A

Clause 6.1.3 b) requires the organisation to determine all controls necessary, then compare them with Annex A to confirm none was omitted. Three controls specific to a multi-tenant, EU-hosted SaaS provider are added; they are not Annex A controls and do not change the 93-control count.

| Ref | Additional control | Rationale (risk link) | Related Annex A | Status | Evidence Ref |
| --- | --- | --- | --- | --- | --- |
| C-01 | Logical tenant isolation for customer data in the multi-tenant platform | Cross-tenant exposure is the most damaging form of R-001 and R-013; tested in design and penetration testing | 8.3, 8.22, 8.26 | Partial | EV-25, EV-32 |
| C-02 | EU data residency enforcement and sub-processor transparency | Customers and GDPR expect processing in eu-west-1 (R-011); region restrictions applied through AWS organisation policies | 5.20, 5.31, 8.9 | Partial | EV-13, EV-37 |
| C-03 | Customer assurance handling: security questionnaires, audit-rights requests and a shared-responsibility statement | 200+ enterprise customers drive contractual obligations (R-005, R-011) | 5.19, 5.31 | Planned | EV-12, EV-17 |
