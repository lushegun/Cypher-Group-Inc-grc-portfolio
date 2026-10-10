[← Portfolio home](../README.md) · [All templates](README.md)

# [ORGANISATION] — SOC 2 Trust Services Criteria to control-set crosswalk — TEMPLATE

> [!TIP]
> **How to use this template.** Blank reusable template from the CGI-SOC-001 portfolio project (fictional). Replace every
> `[BRACKETED]` field. The criterion IDs, categories and groups are pre-filled for Security (CC1–CC9), Availability (A1)
> and Confidentiality (C1). **Criterion wording is deliberately left blank: the AICPA Trust Services Criteria are
> copyrighted, so paraphrase them from your own licensed copy.** Add the Processing Integrity (PI1) and Privacy (P1–P8)
> rows if those categories are in scope for you.

| Field | Value |
|---|---|
| Document ID | [ORG-SOC-001] |
| Version | [1.0] |
| Criteria version | [AICPA 2017 Trust Services Criteria with the 2022 revised points of focus] |
| Control set crosswalked | [e.g. ISO/IEC 27001:2022 Annex A, your own control library] |
| Assessor | [Name, role] |
| Date | [DD Mon YYYY] |

## The scoring method — publish it before you score anything

1. **Score the controls, not the criterion.** Give every control in your own control set an evidence-based maturity (0–4).
   A criterion inherits the mean of the controls mapped to it.
2. **Criterion Readiness Level (CRL), 0–3, is that mean, banded:** below 0.5 → 0 · 0.5–1.49 → 1 · 1.5–2.49 → 2 · 2.5 and above → 3.
3. **Clause-style requirements scored 0–2 convert** 0 → 0 · 1 → 2 · 2 → 3 before they enter the mean.
4. **The design-hole rule.** Design is *Adequate* only when **CRL ≥ 2 AND no mapped control sits at maturity 0**.
   One control at zero is a hole in the design, however good the average looks.
5. **Operating effectiveness is *Evidenced* only at CRL 3.** Design and operation are separate columns and separate questions.
6. **Gates beat percentages.** Name the criteria whose failure stops the engagement before you score, and apply the
   override first: any gate failure is a NO-GO whatever the percentage.
7. **Readiness, two numbers:** Type I = Σ(CRL capped at 2) ÷ (2 × criteria). Type II = Σ(CRL) ÷ (3 × criteria).

> Worked example row: CC7.4 below shows the level of specificity expected. Delete it before issue.

| Criterion | TSC category | Criteria group | Criterion (paraphrase from your licensed copy) | Mapped control IDs | Mapped clause or policy requirements | Items scored | Mean mapped maturity | Zero-maturity items | CRL (0-3) | Design verdict | Operating verdict | Design holes (items at maturity 0) | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| CC7.4 | Security | CC7 System Operations | [Responds to identified security incidents] | A.5.24; A.5.25; A.5.26; A.5.27; A.6.8 | 5.5 of the incident policy | 6 | 1.83 | 1 | 2 | Adequate | Not evidenced | A.5.29 | [EXAMPLE ROW - replace] Plan approved and owned; never exercised, so no operating evidence |
| CC1.1 | Security | CC1 Control Environment | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC1.2 | Security | CC1 Control Environment | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC1.3 | Security | CC1 Control Environment | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC1.4 | Security | CC1 Control Environment | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC1.5 | Security | CC1 Control Environment | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC2.1 | Security | CC2 Communication and Information | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC2.2 | Security | CC2 Communication and Information | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC2.3 | Security | CC2 Communication and Information | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC3.1 | Security | CC3 Risk Assessment | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC3.2 | Security | CC3 Risk Assessment | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC3.3 | Security | CC3 Risk Assessment | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC3.4 | Security | CC3 Risk Assessment | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC4.1 | Security | CC4 Monitoring Activities | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC4.2 | Security | CC4 Monitoring Activities | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC5.1 | Security | CC5 Control Activities | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC5.2 | Security | CC5 Control Activities | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC5.3 | Security | CC5 Control Activities | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC6.1 | Security | CC6 Logical and Physical Access Controls | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC6.2 | Security | CC6 Logical and Physical Access Controls | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC6.3 | Security | CC6 Logical and Physical Access Controls | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC6.4 | Security | CC6 Logical and Physical Access Controls | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC6.5 | Security | CC6 Logical and Physical Access Controls | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC6.6 | Security | CC6 Logical and Physical Access Controls | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC6.7 | Security | CC6 Logical and Physical Access Controls | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC6.8 | Security | CC6 Logical and Physical Access Controls | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC7.1 | Security | CC7 System Operations | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC7.2 | Security | CC7 System Operations | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC7.3 | Security | CC7 System Operations | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC7.4 | Security | CC7 System Operations | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC7.5 | Security | CC7 System Operations | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC8.1 | Security | CC8 Change Management | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC9.1 | Security | CC9 Risk Mitigation | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| CC9.2 | Security | CC9 Risk Mitigation | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| A1.1 | Availability | A1 Availability | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| A1.2 | Availability | A1 Availability | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| A1.3 | Availability | A1 Availability | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| C1.1 | Confidentiality | C1 Confidentiality | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |
| C1.2 | Confidentiality | C1 Confidentiality | [Paraphrase the criterion] | [Control IDs, semicolon separated] | [Clause or policy references] | [n] | [0.00] | [n] | [0-3] | [Adequate / Deficient] | [Evidenced / Not evidenced] | [IDs at maturity 0, or -] | [Evidence to obtain] |

## Fill-in checklist

- [ ] Every criterion in every category you selected has a row, and the selection itself is justified in writing.
- [ ] Every criterion maps to at least one control or requirement. A criterion with no mapping is a gap, not a blank.
- [ ] Every mapped control carries an evidence-based maturity from a source you can show an examiner.
- [ ] The design verdict applies the design-hole rule, not just the average.
- [ ] No criterion claims operating evidence that your control records say does not exist.
- [ ] Gates are listed, scored and applied before the percentage is quoted.
- [ ] Criteria with no counterpart in your control set are listed separately — they are what a single-framework plan cannot see.
