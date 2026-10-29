> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Auditor challenge preparation

These are the questions a certification-body auditor is most likely to ask about the SoA, beyond those in the dossiers. Answers are written for the control owner to speak to, with the evidence to have open.

| # | Likely question | Model answer | Evidence to show |
| --- | --- | --- | --- |
| 1 | You have no premises. Why are five physical controls applicable? | The subject of 7.7, 7.9, 7.10, 7.13 and 7.14 exists: every company laptop is off-premises. Excluding them would leave the main physical risk (R-002) untreated. | SoA section 9; MDM export (EV-23); asset register (EV-24) |
| 2 | Why is 7.8 excluded but 7.9 included? | 7.8 concerns equipment sited in controlled locations; Progress has none. Laptops outside such locations fall under 7.9. | ED-03; EV-43 |
| 3 | Your SoA shows only 33 controls as implemented. Is that acceptable? | Yes. Status reflects evidence. Partial and Planned controls have owners, dates and remediation actions; marking them Implemented without evidence would be the nonconformity. | Section 18 roadmap; EV-06 |
| 4 | Show me the evidence for one Implemented control chosen by me. | Provide the evidence reference from the SoA and open the artefact, with dates across the audit period. | Any EV-nn in section 16 |
| 5 | You excluded 7.4, 7.5 and 7.11 because of AWS. Show me AWS's assurance. | Open the AWS certificates and SOC reports from AWS Artifact, the dated review, reviewer name and any exceptions noted. | EV-12; shared-responsibility matrix (EV-14) |
| 6 | Does Progress use cryptography? You say you generate no keys. | Yes. 8.24 covers use of cryptography, including KMS key policies, rotation and TLS. Progress does not generate its own key material, which reduces but does not remove the requirement. | EV-30 |
| 7 | You have no mobile app. Why is application security applicable? | The API is the product. 8.26 to 8.29 apply to it; mobile development would add nothing because none exists. | EV-26, EV-25 |
| 8 | Do staff use personal phones for work email, chat or MFA? | To be confirmed by IT. If personal phones access company data, a mobile device rule must be added under 8.1 and 6.7; if used only as authenticators, 5.17 and 8.5 cover it. | EV-22, EV-46 |
| 9 | How is the SoA kept current? | Reviewed at management review and on any trigger in section 12, with version history and approval recorded. | Section 22; EV-04 |
| 10 | Why is 5.13 labelling applicable for a cloud-only company? | Labelling is proportionate: document footers and cloud resource tags. It supports classification-based handling of customer data (R-001, R-011). | EV-09 |
| 11 | How do you know the remaining residual risks are acceptable? | Target residual ratings are Medium or Low and approved by the risk owner; Medium residuals on R-001, R-003, R-005 and others are accepted formally. | EV-05, EV-06 |
| 12 | What happens to the SoA if you open an office? | 7.1 to 7.6 and 7.8, 7.11, 7.12 are re-evaluated before occupation and the SoA is reissued; the scope statement is amended. | Section 12; EV-43 |
| 13 | Who approved this SoA and when? | The approval table in section 22 records name, role and date. | Section 22 |
