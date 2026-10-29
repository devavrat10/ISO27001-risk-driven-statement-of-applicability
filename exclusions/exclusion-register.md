> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Exclusion register

Ten controls are excluded. Each passes the five-part exclusion test in section 5.2. Any re-evaluation trigger below, once met, requires the SoA to be reissued before the change goes live.

| Ref | Control | Dossier | Reason for exclusion | Alternative or inherited measure | Re-evaluation trigger |
| --- | --- | --- | --- | --- | --- |
| 7.1 | Physical security perimeters | ED-01 | No company premises; remote-first since founding | 8.1, 7.9; AWS data-centre perimeters via 5.22 | Lease or ownership of any premises |
| 7.2 | Physical entry | ED-01 | No facilities with entry points | 5.15, 5.18, 8.5 (logical access) | Any premises or shared workspace holding company assets |
| 7.3 | Securing offices, rooms and facilities | ED-01 | No offices, rooms or facilities; home offices are not company facilities | 6.7, 7.7, 7.9, 8.1 | Company-controlled office, storage room or lab |
| 7.4 | Physical security monitoring | ED-02 | No premises to monitor; AWS monitors its data centres | 8.15, 8.16; AWS assurance via 5.22 | Loss of AWS assurance evidence or move to non-AWS hosting |
| 7.5 | Protecting against physical and environmental threats | ED-02 | No company site; hosting threats inherited from AWS AZ design | 5.29, 5.30, 8.14; AWS assurance via 5.22 | Move to single-AZ or non-AWS hosting; AWS assurance gap |
| 7.6 | Working in secure areas | ED-01 | No secure areas exist | 8.2, 8.3 (logical segregation of sensitive work) | Creation of a secure room or lab |
| 7.8 | Equipment siting and protection | ED-03 | No company equipment sited on company premises | 7.9, 8.1; AWS-operated servers | Any on-premises server, network or storage equipment |
| 7.11 | Supporting utilities | ED-02 | No company site with power, cooling or telecoms; AWS provides hosting utilities | 5.30, 8.14; AWS assurance via 5.22 | Any company-operated site or equipment room |
| 7.12 | Cabling security | ED-03 | Progress owns no cabling; networks are home ISPs and AWS | 8.24 (encryption in transit), 8.20 | Any company-owned network infrastructure |
| 8.30 | Outsourced development | ED-04 | All development is performed by employees | 8.25, 8.28, 5.19–5.21 as fall-back | Use of any external developer, agency or offshore team |

**General re-evaluation triggers** apply in addition: new product lines handling different data, new hosting regions or providers, acquisition, a major incident traced to an excluded control, or a customer or regulator requirement that names an excluded control.
