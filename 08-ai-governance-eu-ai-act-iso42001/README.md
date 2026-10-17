[← Portfolio home](../README.md) · [← 07 Cloud Configuration Compliance Review](../07-aws-cloud-compliance/)

# 08 · AI Governance Assessment (EU AI Act + ISO/IEC 42001)

**Cypher Group Inc. · CGI-AIG-001 · Version 1.0 · 17 Oct 2026 · 4 AI systems · 38 Annex A controls · 13 findings · 2 new risks**

![AI Act](https://img.shields.io/badge/EU%20AI%20Act-no%20high--risk%20system-0B2545?style=flat-square)
![42001](https://img.shields.io/badge/ISO%2FIEC%2042001%20readiness-30.3%25%20·%20NO--GO-C0392B?style=flat-square)
![Findings](https://img.shields.io/badge/findings-1%20critical%20·%204%20high%20·%207%20medium%20·%201%20low-13315C?style=flat-square)
![Register](https://img.shields.io/badge/risk%20register-v1.3%20·%2016%20risks-1B4965?style=flat-square)

> [!IMPORTANT]
> **Simulated case study.** Laws, standards, article and clause numbers are real and current to 17 October 2026; ISO/IEC 42001 wording is paraphrased.

## The question this answers

Every earlier project left an AI thread hanging: an AI-use rule in the policy pack (§4.5), two AI tools found on expense claims, an AI tiering trigger, a chat tool whose AI read customer posts. The CEO's question: **"Are we using AI safely, and does the new EU AI law catch us?"**

This assessment governs what a machine **says and decides**, where Projects 01 to 07 protected what Cypher **stores**.

## What's in this folder

| Document | What it is | Read online | Download |
|---|---|---|---|
| **AI governance assessment** (CGI-AIG-001) | AI register, EU AI Act applicability (today and later), ISO/IEC 42001 clauses and all 38 Annex A controls, two AI impact assessments, seven-framework mapping, findings, register v1.3, roadmap, CEO one-pager | [View](08-ai-governance-assessment.md) | [PDF](08-ai-governance-assessment.pdf) · [Excel](08-ai-governance-assessment.xlsx) |
| **ISO/IEC 42001 Statement of Applicability** | 38 controls × 16 columns, one value per cell | [View as table](08-ai-governance-assessment.csv) | CSV |
| **Data sets** | Register, AI Act tests and timeline, clauses, readiness, impact assessments, harm scores, DPIA screening, findings, mapping, drawer-2 test, new risks, register delta, roadmap, conflicts, maturity, assumptions | [Browse](data/) | 21 CSVs |

## At a glance

| Measure | Result |
|---|---|
| AI systems | **3 in use** (ScribeCo meeting assistant, ChatCo AI features, WriteCo writing assistant) + **1 scenario** (AI-A01 product assistant, to test the provider role) |
| Cypher's role | **Deployer** of all three; **provider** of AI-A01 at launch |
| EU AI Act tier | **No high-risk system, no prohibited practice.** Duties today: Art. 4 (AI literacy) and Art. 5. AI-A01 adds Art. 50 at launch |
| AI Act dates (verified 17 Oct 2026) | Art. 5 and Art. 4 since 2 Feb 2025 · GPAI since 2 Aug 2025 · Art. 50 since 2 Aug 2026 · Annex III 2 Dec 2027 · Annex I 2 Aug 2028 (Digital Omnibus, Reg. (EU) 2026/1744) |
| ISO/IEC 42001 | Clauses **18/60 (30.0%)** · **26 of 38** Annex A controls applicable, **0 implemented** · readiness **30.3%** · **9 of 9 gates fail → NO-GO** |
| Impact assessments | ScribeCo and ChatCo AI: worst harm **16 → 6** with the measures. DPIA required for **all three** tools |
| Findings | **13: 1 Critical · 4 High · 7 Medium · 1 Low** |
| Risk register | **v1.3: 16 risks**, inherent 213 → **233**, residual 130 → **147**. New: AR-001, AR-002 |
| NIST CSF 2.0 maturity | **1.32, unchanged** |

## The finding I would lead with

The AI Act turned out to be the small problem. None of Cypher's AI is high-risk, so the law asks two things today: support staff's AI literacy, and never use the banned practices.

The big problem is **how the AI arrived**:

- **A meeting assistant joins customer calls under no contract of any kind.** Its decision date passed two days before this assessment.
- **The chat tool's AI reads customer posts** with nothing stopping the supplier training on them, and the action to switch it off has no evidence it happened.
- **The approved AI tools list the policy points to does not exist**, so staff could not comply even if they wanted to.

> **The AI Act asks "how dangerous is the model?" The honest answer for a 50-person SaaS company is "not very". The question that matters is "did anyone sign anything before the AI started listening?"**

## Five design decisions

1. **Inventory only from the record.** Every AI system comes from something Projects 01 to 07 recorded. Where the record runs out, an assumption is declared (AI-A01 to AI-A04) and a verification action scheduled.
2. **The tier belongs to the system; every duty belongs to a role.** Article 50 may apply to ScribeCo's product without placing any duty on Cypher. Cypher's duty to tell people on calls comes from GDPR Articles 13 and 14.
3. **One scenario to test the provider side.** Cypher builds no AI, so AI-A01 (a planned product assistant) shows what changes when it does, and is kept out of every earlier number.
4. **Twelve controls excluded, each with a re-entry trigger.** Development controls (A.6, A.7) wait for the AI-A01 design gate. Four life-cycle controls stay in, because testing, deploying, monitoring and logging apply to anyone who puts AI into use.
5. **"None" when nothing fits.** Output accuracy has no home in ISO/IEC 27001, SOC 2 or CSF 2.0. The mapping says so instead of forcing a match. That gap is the best one-line answer to "why does AI need its own governance?"

## Reuse this work

- [AI register template](../templates/ai-register-template.md) · [CSV](../templates/ai-register-template.csv): inventory with role, tier, deciding article, data, training terms and oversight
- [EU AI Act applicability checklist](../templates/eu-ai-act-applicability-template.md) · [CSV](../templates/eu-ai-act-applicability-template.csv): the eight tests in order, each with its article, and the post-Omnibus dates
- [ISO/IEC 42001 Statement of Applicability](../templates/iso42001-soa-template.md) · [CSV](../templates/iso42001-soa-template.csv): all 38 controls pre-filled, with the maturity-to-status rule and the clause 4-10 checklist
- [AI impact assessment template](../templates/ai-impact-assessment-template.md) · [CSV](../templates/ai-impact-assessment-template.csv): combined AI and DPIA screening, harm scoring and oversight
