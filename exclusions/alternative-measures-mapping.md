> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Alternative measures mapping

Every physical-theme control has a named treatment: an applicable control that Progress operates, an AWS-inherited control backed by assurance, or a documented statement that the subject does not exist. The source brief's mapping is retained where sound and corrected where an alternative control would not satisfy an auditor (7.7, 7.9, 7.10, 7.13, 7.14 are applicable, not substituted).

| Physical control | Disposition | How the risk is still addressed | Reference |
| --- | --- | --- | --- |
| 7.1 Physical security perimeters | Excluded | Endpoint security for laptops; AWS data-centre perimeters through supplier assurance | 8.1, 5.22 |
| 7.2 Physical entry | Excluded | Logical access control replaces physical entry control | 5.15, 5.18, 8.5 |
| 7.3 Securing offices, rooms and facilities | Excluded | Remote working standard, screen-lock and off-premises asset controls | 6.7, 7.7, 7.9 |
| 7.4 Physical security monitoring | Excluded | Logical monitoring in AWS; AWS physical monitoring evidenced in audit reports | 8.15, 8.16, 5.22 |
| 7.5 Protecting against physical and environmental threats | Excluded | AWS AZ design inherited; Progress multi-AZ, DR and continuity controls | 5.22, 5.29, 5.30, 8.14 |
| 7.6 Working in secure areas | Excluded | No secure areas; logical segregation of sensitive access | 8.2, 8.3 |
| 7.7 Clear desk and clear screen | **Applicable** | MDM auto-lock plus clear-desk guidance for homes and public places | 7.7, 8.1, 6.7 |
| 7.8 Equipment siting and protection | Excluded | No on-premises equipment; laptops covered by off-premises control | 7.9, 8.1 |
| 7.9 Security of assets off-premises | **Applicable** | Encrypted, MDM-managed laptops with remote wipe | 7.9, 8.1, 8.24 |
| 7.10 Storage media | **Applicable** | Restricted removable media; deletion and encryption controls | 7.10, 8.10, 8.24 |
| 7.11 Supporting utilities | Excluded | AWS provides hosting utilities; Progress designs for resilience | 5.22, 5.30, 8.14 |
| 7.12 Cabling security | Excluded | No company cabling; encryption in transit protects data on third-party networks | 8.24, 8.20 |
| 7.13 Equipment maintenance | **Applicable** | Approved repair route, firmware patching and laptop refresh policy | 7.13, 8.1 |
| 7.14 Secure disposal or re-use of equipment | **Applicable** | Certified wipe at end of life; cloud sanitisation inherited from AWS | 7.14, 8.10, 5.11 |

**Compensating-control caution.** An alternative control is accepted by an auditor only if it is itself implemented and evidenced. Where the alternative is still Partial (for example 8.10), the exclusion defence relies on the remediation plan in section 18.
