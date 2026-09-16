[← Portfolio home](../README.md) · [← 03 CSF Gap Assessment](../03-nist-csf-gap-assessment/)

# 04 · Third-Party / Vendor Risk Management Programme

**Cypher Group Inc. · CGI-TPR-001 · Version 1.0 · 15 Sep 2026 · commissioned by CGI-GAP-001 REC-15**

![Vendors](https://img.shields.io/badge/vendors-17%20tiered-0B2545?style=flat-square)
![Questionnaire](https://img.shields.io/badge/questionnaire-74%20questions%20·%2016%20domains-13315C?style=flat-square)
![GV.SC](https://img.shields.io/badge/GV.SC-0%20→%202%20(target%20met)-2BAE66?style=flat-square)
![AI](https://img.shields.io/badge/AI%20vendor%20governance-built%20in-5FA8D3?style=flat-square)

> [!IMPORTANT]
> **Fictional case study.** Cypher Group Inc. does not exist. Real product names are used only as realistic stand-ins. **Every assurance status, DPA status, report period, hosting region and finding attributed to them is invented** and says nothing about those companies.

## Why this project exists

[Project 03](../03-nist-csf-gap-assessment/) scored supply chain risk management (**GV.SC**) at **0 out of 4**, the only zero that is also a hard commercial blocker, and recommended this programme (REC-15). The risk register in [Project 02](../02-risk-register/) also had no supplier risk at all.

## What's in this folder

| Document | What it is | Read online | Download |
|---|---|---|---|
| **Vendor Risk Programme** (CGI-TPR-001) | Inventory, tiering model, questionnaire, three assessments, nine new risks, onboarding/offboarding workflow, contract clause checklist, executive summary | [View](04-vendor-risk-programme.md) | [PDF](04-vendor-risk-programme.pdf) · [Excel](04-vendor-risk-programme.xlsx) |
| **Data sets** | Inventory, tiering, 74-question questionnaire, assessments, risk addendum, KRIs, clause checklist | [Browse](data/) | CSV |

## Headline findings

- **17 vendors found, not 5.** I used four discovery sources: the known architecture, 12 months of card and bank transactions, the apps connected through Google Workspace sign-in, and one conversation with each department.
- **6 of 17 vendors (35%) have no signed Data Processing Agreement (DPA)**, and 4 of those six already hold Confidential data.
- **2 AI tools were bought on expenses and are processing customer calls and typed text under no contract at all.** That is shadow IT and an AI governance gap in one finding.
- **The best-certified vendor passed only with conditions, and all four conditions were ours.** AWS's SOC 2 report assumes customers run four controls themselves, and Cypher Group was running none of them.
- **5 vendors share a cloud provider with the platform**, so a single regional outage takes down the product *and* the tools used to detect it and tell customers about it.

## The estate at a glance

| Tier | Vendors | Assessment depth | Review cycle | Approver |
|:-:|:-:|---|---|---|
| **1** Critical | 7 | Full 74-question questionnaire, assurance report, DPA and data-flow review | 12 months | CEO |
| **2** Important | 6 | The 24 highest-weight questions, assurance report, DPA | 18 months | CTO |
| **3** Limited | 4 | 6-question attestation and DPA confirmation | 24 months | Business owner |

| Assessment | Vendor | Score | Decision |
|---|---|:-:|---|
| VRA-2026-002 | Slack (Tier 1) | 65% | **Fail**: 9 findings; ~USD 3,600/yr to fix, and 6 of the 8 actions are free |
| VRA-2026-001 | AWS (Tier 1) | 89% | **Pass with conditions**: every condition sits on Cypher Group's side |
| VRA-2026-003 | Calendly (Tier 3) | 92% | **Accepted**: documented justification, expires Sep 2028 |

## AI governance, built into the method

- **Tiering trigger T2-f:** any vendor whose AI may keep, review or train on company content is at least Tier 2, whatever its other scores. Grammarly scores only 3 on the four factors, which would put it in Tier 3; T2-f lifts it to Tier 2.
- **Questionnaire domain 15** asks about AI processing, model training, human review and the chain of AI sub-processors. All four questions carry the maximum weight.
- **Contract clause 7:** no training on company data and no human review without consent, applied to every tier.

## Risk and maturity impact

| | |
|---|---|
| New risks for the register | **9** (VR-001 to VR-009): 8 new, 1 a new route to R-003 |
| Addendum exposure | 121 → 78 (**−36%**, deliberately lower than Project 02's 52%, because these controls are not yet running) |
| Register v1.1 after merge | 14 risks · 213 → 122 (**−43%**) · mean residual 8.80 → 8.71 · **3** residual High |
| Supply chain maturity | **GV.SC 0 → 2**, which meets the declared target |
| Overall CSF maturity | **1.23 → 1.32**. Only GV.SC is claimed to move, because a prerequisite for another Category is not a score for it. |

## Three things I would say in an interview

1. **"AWS passed with conditions, and every condition was ours. The report was fine; how we used it was the finding."**
2. **Tier before you assess.** The tier depends on how exposed *you* are, never on how good the vendor is, and the rule was published before any vendor was scored.
3. **New risk or new route?** Ask one question: *would the existing risk's controls have prevented this?* A four-hour leaver revocation does nothing against a vendor's API sync, so that is a new risk.

## Reuse this work

- [Vendor inventory template](../templates/vendor-risk-inventory-template.md) · [CSV](../templates/vendor-risk-inventory-template.csv)
- [Vendor security questionnaire with automatic scoring](../templates/vendor-risk-questionnaire-template.xlsx) (Excel) · [CSV](../templates/vendor-risk-questionnaire-template.csv) · [Markdown](../templates/vendor-risk-questionnaire-template.md)
- [Vendor assessment report template](../templates/vendor-risk-assessment-report-template.docx) (Word) · [Markdown](../templates/vendor-risk-assessment-report-template.md) · [Findings CSV](../templates/vendor-risk-assessment-findings-template.csv)

---

[← 03 CSF Gap Assessment](../03-nist-csf-gap-assessment/) · [Portfolio home](../README.md)
