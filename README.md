# Progress Technologies - Risk-Driven Statement of Applicability (ISO/IEC 27001:2022)

**Document ID:** PT-ISMS-SOA-001 | **Version:** 1.0 (Draft for management approval) | **Date:** 26 October 2026
**Classification:** Confidential

| | |
|---|---|
| **Author** | Devavrat Yadav |
| **Original author** | Taimuri Jlal - original project brief, scenario and SoA template |
| **Organisation** | Progress Technologies |
| **Standard** | ISO/IEC 27001:2022 (incl. Amendment 1:2024), Annex A |

---

## Overview

A Statement of Applicability (SoA) is one of the most misunderstood artefacts in ISO 27001. This project delivers a **risk-driven SoA that explicitly excludes controls and defends those exclusions**, for a fully remote, AWS-hosted B2B SaaS company pursuing ISO/IEC 27001:2022 certification within six months.

```
JUNIOR APPROACH                          EXPERIENCED APPROACH
Include everything "to be safe"          Include only what is justified
Mark controls as implemented             Honest implementation status
even when aspirational
Avoid exclusions                         Defend exclusions confidently
Generic justifications                   Risk-driven justifications
Result: audit debt, weak credibility     Result: proportionate, defensible
```

## Headline results

| Measure | Result |
|---|---|
| Annex A controls assessed | 93 (37 organizational, 8 people, 14 physical, 34 technological) |
| Applicable / excluded | **83 / 10** |
| Baseline status of applicable controls | 33 Implemented, 42 Partial, 8 Planned |
| Exclusions defended | 10 controls in 4 dossiers (ED-01 to ED-04) |
| Risks | 13 (R-001 to R-006 from the source brief, R-007 to R-013 author-proposed) |
| Evidence references | 50 (EV-01 to EV-50) |
| Remediation actions | 20 (A-01 to A-20) |
| Certification target | 26 April 2027 |

## Scenario

| Attribute | Fact |
|---|---|
| Company | Progress Technologies |
| Industry | B2B SaaS - data analytics platform |
| Employees | 85, fully remote since founding (2021) |
| Infrastructure | 100% AWS (eu-west-1); no physical data centres |
| Customers | 200+ enterprise clients requiring ISO 27001 |
| Context | No offices; company-managed laptops; API-only product; no mobile app; no key generation (AWS KMS); no outsourced development |

## Repository structure

```
.
├── README.md                          This file
├── AUTHORS.md  CHANGELOG.md
├── docs/
│   ├── 01-document-control.md
│   ├── 02-executive-summary.md
│   ├── 03-scope-and-context.md        Scope statement, interested parties, regulatory landscape
│   ├── 04-methodology.md              Applicability and exclusion tests, status definitions
│   ├── 05-appendix-deviations-assumptions.md
│   ├── 06-approval-and-version-history.md
│   ├── full-report.md                 Whole report in one file
│   └── Progress-Technologies-SoA-Report.docx
├── soa/
│   ├── statement-of-applicability.md  Completed SoA in the original template format
│   ├── 00-summary.md
│   ├── theme-5-organizational.md ... theme-8-technological.md
│   └── controls-beyond-annex-a.md
├── risk/
│   ├── risk-assessment.md             Source and supplementary risks, residual targets
│   └── traceability-matrix.md
├── exclusions/
│   ├── exclusion-register.md
│   ├── ed-01.md ... ed-04.md          Auditor defence dossiers
│   └── alternative-measures-mapping.md
├── evidence/evidence-index.md
├── audit/
│   ├── auditor-challenge-qa.md
│   └── video-walkthrough-script.md
├── roadmap/implementation-roadmap.md
├── reflection/reflection-questions.md
├── workbook/Progress_Technologies_SoA_Workbook.xlsx
├── templates/                         Blank SoA template
└── source-material/                   Original files by Taimuri Jlal (unmodified)
```

## Deliverables checklist

| Original deliverable | Status | Location |
|---|---|---|
| Complete SoA, all 93 controls | Done | [soa/](soa/statement-of-applicability.md) |
| Minimum 5 detailed exclusion justifications | Done (10 controls, 4 dossiers) | [exclusions/](exclusions/) |
| Alternative measures mapping | Done | [exclusions/alternative-measures-mapping.md](exclusions/alternative-measures-mapping.md) |
| Risk-to-control traceability matrix | Done | [risk/traceability-matrix.md](risk/traceability-matrix.md) |
| Evidence reference index | Done | [evidence/evidence-index.md](evidence/evidence-index.md) |
| Auditor challenge preparation | Done | [audit/auditor-challenge-qa.md](audit/auditor-challenge-qa.md) |
| 5-minute video walkthrough | Script done; recording to be produced by the author | [audit/video-walkthrough-script.md](audit/video-walkthrough-script.md) |
| Reflection questions | Done | [reflection/](reflection/reflection-questions.md) |

## Key decisions

1. **Physical controls are split, not blanket-excluded.** Nine (7.1-7.6, 7.8, 7.11, 7.12) are excluded; five (7.7, 7.9, 7.10, 7.13, 7.14) stay because every laptop is off-premises.
2. **Reliance on AWS is not an exclusion of accountability.** 7.4, 7.5 and 7.11 are excluded only because AWS operates the data centres, backed by supplier assurance under 5.19-5.23.
3. **Status is stated honestly.** No control is Implemented without an artefact that can be produced on demand.

## Important notes

- Statuses, owners and evidence artefacts are an **assessed baseline derived from the scenario**, not confirmed records. Run an evidence walk-through before approval.
- Risks R-007 to R-013 are author-proposed and pending ratification by the risk owner.
- Regulatory applicability (NIS2, DORA, EU AI Act) must be confirmed by legal counsel.
- The document does not reproduce the text of ISO/IEC 27001 or 27002 and is not legal advice.

## Attribution

Built on the framework, scenario, risk assessment summary and SoA template by **Taimuri Jlal**. Re-authored and extended for Progress Technologies by **Devavrat Yadav**. See [AUTHORS.md](AUTHORS.md).

*ISO 27001 is not about maximal compliance. It is about proportionate, defensible security aligned to business reality.*
