> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Risk-to-control traceability matrix

Every risk is treated by at least six applicable controls, and every applicable control cites at least one risk or a legal, contractual or standard requirement. The only control with no risk ID is 5.35, which is driven by ISO/IEC 27001 clause 9.2 and by customers' expectation of an audited ISMS.

| Risk ID | Risk | Inherent level | Applicable treating controls | Inherited or excluded measures relied on |
| --- | --- | --- | --- | --- |
| R-001 | Unauthorized access to customer data | High | 5.1, 5.3, 5.12, 5.14, 5.15, 5.16, 5.17, 5.18, 6.7, 7.7, 8.1, 8.2, 8.3, 8.5, 8.11, 8.12, 8.15, 8.16, 8.17, 8.18, 8.20, 8.22, 8.24, 8.26, 8.31, 8.33, C-01 | — |
| R-002 | Employee laptop theft or loss | Medium | 5.9, 5.10, 5.11, 6.5, 6.7, 6.8, 7.7, 7.9, 7.10, 7.13, 7.14, 8.1, 8.24 | 7.1, 7.3, 7.8 excluded; treated by 7.9 and 8.1 |
| R-003 | Cloud misconfiguration | Critical | 5.1, 5.2, 5.3, 5.7, 5.8, 5.23, 5.25, 5.26, 5.36, 5.37, 8.2, 8.8, 8.9, 8.12, 8.15, 8.16, 8.19, 8.20, 8.22, 8.25, 8.27, 8.31, 8.32 | — |
| R-004 | Insider threat | Medium | 5.2, 5.3, 5.4, 5.10, 5.11, 5.15, 5.16, 5.18, 5.28, 5.36, 6.1, 6.2, 6.3, 6.4, 6.5, 6.6, 7.10, 8.2, 8.3, 8.4, 8.12, 8.15, 8.16, 8.18 | 7.2, 7.6 excluded; treated by logical access controls |
| R-005 | Third-party breach (AWS) | High | 5.19, 5.20, 5.21, 5.22, 5.23, 5.29, 5.30, 8.14, 8.21, 8.24, C-03 | 7.4, 7.5, 7.11 excluded; inherited from AWS under 5.22 |
| R-006 | Business continuity failure | Medium | 5.24, 5.26, 5.27, 5.29, 5.30, 5.37, 8.6, 8.13, 8.14, 8.34 | 7.5, 7.11 excluded; AWS resilience plus Progress multi-AZ |
| R-007 | Phishing or credential theft of remote staff | High | 5.4, 5.6, 5.7, 5.10, 5.17, 6.3, 6.7, 6.8, 7.7, 8.1, 8.5, 8.7, 8.16, 8.23 | — |
| R-008 | Ransomware or destructive attack | High | 5.26, 5.29, 5.30, 8.7, 8.8, 8.13, 8.14, 8.22 | — |
| R-009 | Software supply-chain compromise | High | 5.7, 5.19, 5.21, 5.32, 8.4, 8.8, 8.19, 8.25, 8.28, 8.29 | 8.30 excluded; fall-back if development is outsourced |
| R-010 | Secrets or credentials exposed in code or pipelines | High | 5.17, 8.4, 8.9, 8.19, 8.28, 8.29 | — |
| R-011 | Non-compliance with GDPR or customer contracts | High | 5.5, 5.12, 5.13, 5.14, 5.20, 5.31, 5.33, 5.34, 6.6, 7.14, 8.10, 8.11, 8.33, C-02, C-03 | — |
| R-012 | Data retained beyond contract or not deleted | Medium | 5.12, 5.33, 5.34, 7.14, 8.10, 8.13 | — |
| R-013 | API abuse: broken authorization, injection or denial of service | High | 5.8, 8.5, 8.6, 8.15, 8.20, 8.21, 8.25, 8.26, 8.27, 8.28, 8.29, C-01 | — |

**Reading the matrix.** R-003, the only Critical risk, is treated by 23 applicable controls, but 8.9, 8.16 and 5.26 are Partial; closing those three is the highest-value remediation in section 18.
