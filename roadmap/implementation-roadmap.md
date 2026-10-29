> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Implementation roadmap and gap-closure plan

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
