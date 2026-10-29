> **Progress Technologies** · ISO/IEC 27001:2022 · Document ID PT-ISMS-SOA-001 · v1.0 · Author: Devavrat Yadav · Original author: Taimuri Jlal

# Reflection questions

**1. Which exclusion was hardest to justify?** 7.5 (with 7.4 and 7.11). The other exclusions rest on facts about Progress — no premises, no cabling, no outsourced developers. These three rest on AWS, so the defence is only as strong as the supplier assurance evidence under 5.22. That is why A-04 (the AWS assurance review) is an early action.

**2. Which inclusion was a surprise?** The five physical controls that remain applicable (7.7, 7.9, 7.10, 7.13, 7.14). A company with no premises appears to have no physical controls, but every laptop is a permanently off-premises asset. Other surprises: 8.24 applies although Progress generates no keys; 8.26 to 8.29 apply to an API with no end-user application; and 5.13 labelling applies in a light form.

**3. How would the SoA change if the company opened one physical office?** Most of the nine excluded physical controls would be re-evaluated before occupation. 7.1 to 7.5 and 7.7 would become fully applicable and new evidence would be needed: visitor and access records, office network controls under 8.20, monitoring with privacy review, and a continuity plan for loss of the office. 7.6, 7.11 and 7.12 might stay excluded if the landlord provides utilities and cabling and no secure area exists, but each would need a documented decision. The scope statement, asset register and risk register would change, and the SoA would be reissued.

**4. Where did the risk assessment drive a different decision than instinct?** Instinct says a cloud-only company excludes physical controls wholesale; R-002 (laptop loss) kept five of them. R-003 (Critical) shifted attention from policy documents to 8.9, 8.16 and 5.26, where the gaps are. Instinct also suggests dropping 8.18 (privileged utilities) and 8.34 (audit testing) as marginal in the cloud; R-001, R-004 and R-006 keep both applicable.

**5. What is the cost of over-including controls?** Every applicable control needs an owner, an evidence artefact, periodic review and exposure to audit sampling. Including 7.2 would demand visitor logs for visitors who never arrive, and the only ways to satisfy it are to invent evidence or to accept a nonconformity. Over-inclusion also dilutes attention from the controls that treat R-003, and marking aspirational controls Implemented creates credibility damage with the certification body that outlasts the audit.
