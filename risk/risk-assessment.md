> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Risk assessment baseline

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
