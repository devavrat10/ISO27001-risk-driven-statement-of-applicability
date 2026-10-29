> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Executive summary

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
