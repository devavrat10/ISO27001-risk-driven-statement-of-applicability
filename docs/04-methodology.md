> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Methodology and decision framework

This SoA responds to clause 6.1.3 c) and d): it records the necessary controls, why they are included, whether they are implemented, and why any Annex A control is excluded. Annex A is a reference list, not a mandate, so each control is tested against Progress's context.

### 5.1 Applicability test

Each of the 93 controls was passed through the same four questions, in order.

1. **Does the control treat an assessed risk (R-001 to R-013)?** If yes, it is applicable, and the justification names the risk IDs.
2. **Is it required by law, regulation or a customer contract?** If yes, it is applicable and the basis is named.
3. **Does the control's subject exist in Progress's environment?** Examples: premises, on-premises equipment, outsourced developers. If the subject does not exist, move to the exclusion test.
4. **Is the risk the control addresses already treated by a different applicable control, or inherited from a supplier?** If so, the control may be excluded only if the replacement or inherited measure is named and evidenced.

### 5.2 Exclusion test (all five must pass)

| # | Test | Evidence of passing |
| --- | --- | --- |
| 1 | The control's subject matter does not exist in the ISMS scope | Non-applicability dossier (EV-43) |
| 2 | No assessed risk depends on the control | Risk register cross-check (section 15) |
| 3 | Any residual risk is treated by a named alternative control or inherited supplier control | Alternative measures mapping (section 14) |
| 4 | Inherited controls are backed by current supplier assurance | AWS Artifact reports, supplier review (EV-12) |
| 5 | A re-evaluation trigger is defined | Exclusion register (section 12) |

### 5.3 Implementation status definitions

| Status | Meaning | Auditor expectation |
| --- | --- | --- |
| Implemented | Fully operational; evidence available on demand | Records of operation, metrics or logs |
| Partial | Some elements operate; gaps documented | Evidence for the parts in place plus a dated remediation plan |
| Planned | Not yet operating; committed | Project plan, owner, resource allocation, target date |
| N/A (Excluded) | Control not applicable | Documented justification and alternative measures |

**Rule: never mark a control Implemented unless its evidence reference can be produced on demand.** The baseline statuses in this pack are the author's assessed starting position derived from the scenario; each must be confirmed in an evidence walk-through with the control owner before the SoA is approved. Any control that fails the walk-through is downgraded to Partial.

### 5.4 Justification categories

Every justification in sections 7 to 10 names its driver using risk IDs. Where a legal or contractual driver applies, it is stated in words (for example GDPR processor duty or customer security addendum).
