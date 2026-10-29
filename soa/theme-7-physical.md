> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Theme 7 — Physical controls (14)

Nine physical controls are excluded and five remain applicable. The source brief anticipated 11 exclusions; this pack keeps 7.7, 7.9, 7.10, 7.13 and 7.14 in scope because every company laptop is a permanently off-premises asset (see section 21, deviation D-01). Baseline of the five applicable controls: 1 Implemented, 4 Partial. Exclusion defences are in section 13 (ED-01 to ED-03).

| Ref | Control | Applicable | Status | Justification (risk link) | Evidence Ref |
| --- | --- | --- | --- | --- | --- |
| 7.1 | Physical security perimeters | No | N/A | **Excluded (ED-01).** Progress controls no premises or secure perimeter; all staff work remotely and production runs in AWS. Residual laptop risk (R-002) treated by 8.1 and 7.9. | EV-43 |
| 7.2 | Physical entry | No | N/A | **Excluded (ED-01).** No facilities with entry points. Access to information is controlled logically through 5.15, 5.18 and 8.5. | EV-43 |
| 7.3 | Securing offices, rooms and facilities | No | N/A | **Excluded (ED-01).** No offices, rooms or facilities. Employee homes are not company facilities; their risk is treated by 6.7, 7.7 and 7.9. | EV-43 |
| 7.4 | Physical security monitoring | No | N/A | **Excluded (ED-02).** No premises to monitor. AWS monitors its data centres; assurance obtained under 5.22; logical monitoring by 8.15 and 8.16. | EV-12, EV-43 |
| 7.5 | Protecting against physical and environmental threats | No | N/A | **Excluded (ED-02).** No company site exposed to fire, flood or power loss. AWS Availability Zone design inherited (R-005); service impact treated by 5.29, 5.30 and 8.14 (R-006). | EV-12, EV-43 |
| 7.6 | Working in secure areas | No | N/A | **Excluded (ED-01).** No secure areas exist. Sensitive work is protected logically through 8.2 and 8.3. | EV-43 |
| 7.7 | Clear desk and clear screen | Yes | Partial | Applies to remote workers in homes, cafés and travel (R-001, R-002, R-007). MDM enforces auto-lock; clear-desk guidance in the remote working standard; no-printing rule. | EV-22, EV-23 |
| 7.8 | Equipment siting and protection | No | N/A | **Excluded (ED-03).** No company equipment is sited in company premises; servers are AWS-operated. Endpoint protection covered by 7.9 and 8.1. | EV-24, EV-43 |
| 7.9 | Security of assets off-premises | Yes | Implemented | Primary physical control for the business: laptops are the only company-owned assets outside AWS and are always off-premises (R-002). Full-disk encryption, remote wipe and travel guidance enforced. | EV-23, EV-24 |
| 7.10 | Storage media | Yes | Partial | Laptops and removable media can carry customer-adjacent data (R-002, R-004). USB mass storage restricted by MDM policy; formal media handling rules being finalised. | EV-22, EV-23 |
| 7.11 | Supporting utilities | No | N/A | **Excluded (ED-02).** No company site with power, cooling or telecoms. AWS provides resilient utilities for the hosting layer (R-005, R-006). | EV-12, EV-43 |
| 7.12 | Cabling security | No | N/A | **Excluded (ED-03).** Progress owns no cabling; networks are home ISPs and AWS. Data in transit protected by 8.24. | EV-43 |
| 7.13 | Equipment maintenance | Yes | Partial | Laptop repair, firmware and warranty servicing must not expose data (R-002). Approved repair route with encrypted disks; firmware patching via MDM. | EV-23, EV-24 |
| 7.14 | Secure disposal or re-use of equipment | Yes | Partial | End-of-life laptops must be wiped and certified (R-002, R-011, R-012). Cloud media sanitisation inherited from AWS; disposal certificates being collected. | EV-24, EV-33 |
