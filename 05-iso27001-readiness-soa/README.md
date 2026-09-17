[← Portfolio home](../README.md) · [← 04 Vendor Risk](../04-vendor-risk-management/)

# 05 · ISO/IEC 27001:2022 Readiness Assessment & Statement of Applicability

**Cypher Group Inc. · CGI-ISO-001 · Version 1.0 · 16 Sep 2026 · all 93 Annex A controls · clauses 4–10**

![ISO](https://img.shields.io/badge/ISO%2FIEC%2027001-2022%20%2B%20Amd%201%3A2024-0B2545?style=flat-square)
![SoA](https://img.shields.io/badge/SoA-88%20applicable%20·%205%20excluded-13315C?style=flat-square)
![Readiness](https://img.shields.io/badge/readiness-30.6%25%20·%20Stage%201%20NO--GO-C0392B?style=flat-square)
![Certificate](https://img.shields.io/badge/realistic%20certificate-Nov%202027-1B4965?style=flat-square)

> [!IMPORTANT]
> **Fictional case study.** Cypher Group Inc. does not exist. Every finding, score, date and cost was created to demonstrate applied GRC method. ISO/IEC 27001 wording is paraphrased; the standard itself must be purchased from ISO or a national standards body.

## The question this answers

Enterprise buyers keep asking one thing: *"Are you ISO 27001 certified?"* After four projects the company has policies ([01](../01-security-policy-pack/)), a risk register ([02](../02-risk-register/)), a maturity scorecard ([03](../03-nist-csf-gap-assessment/)) and a vendor programme ([04](../04-vendor-risk-management/)). The CEO wants to know **what all of that is worth to a certification auditor, and what it will take to earn the certificate.**

## What's in this folder

| Document | What it is | Read online | Download |
|---|---|---|---|
| **Readiness Assessment & SoA** (CGI-ISO-001) | Scope statement, the full 93-control Statement of Applicability, clauses 4–10 readiness, documented-information checklist, weighted readiness score, costed roadmap, CEO one-pager | [View](05-iso27001-readiness-and-soa.md) | [PDF](05-iso27001-readiness-and-soa.pdf) · [Excel](05-iso27001-readiness-and-soa.xlsx) |
| **Statement of Applicability** | All 93 controls × 17 columns, one value per cell | [View as table](05-iso27001-readiness-and-soa.csv) | CSV |
| **Data sets** | Clause readiness, documented information, roadmap, REC reconciliation, gap-mapping reconciliation | [Browse](data/) | CSV |

## At a glance

| Measure | Result |
|---|---|
| Annex A controls applicable / excluded | **88 / 5** (no data centre, no server room, no outsourced development) |
| Implemented / Partial / Not started | **0 / 45 / 43** |
| Controls the earlier gap assessment never mapped | **38**, including **A.8.3**, the control the top code risk actually breaks |
| Controls included for non-risk reasons, and labelled that way | **10** |
| Clauses 4–10 readiness | **33.9%** (19 of 56 points) · only clause 8.2 fully met |
| Weighted certification readiness | **30.6%: Stage 1 is a NO-GO** (8 of 8 gate requirements fail) |
| Realistic path | Stage 1 **Jul 2027** → Stage 2 **Oct 2027** → certificate **Nov 2027** |
| Cost to certificate | **USD 22,900** ISO-specific · USD 55,000 whole programme (1.5% of ARR) |
| NIST CSF 2.0 maturity after this project | **1.32, unchanged.** An SoA maps the gaps; it closes none |

## How I did it

1. **Status is derived, not typed.** Each control gets a 0–4 maturity on the Project 03 scale, and a formula turns it into a status. An approved policy with no operating evidence is a 2, so it can never read *Implemented*. The honest result is zero Implemented.
2. **Nothing is justified by an invented risk.** Every control traces to a register risk, a maturity score or a vendor finding, or it is labelled *NOT risk-based*. Three gaps in the register are proposed as candidate risks instead of being quietly added.
3. **Earlier work is credited, but only once.** The policy pack maps 38 Annex A controls. Each of those rows either credits the clause (the screen-lock rule makes A.7.7 Partial) or names it as a fragment (the encryption requirement says *where*, not *how*, so A.8.24 stays Not started).
4. **The readiness score has a veto.** Scope, risk acceptance criteria, SoA approval, internal audit and management review are gates. Fail one and the answer is NO-GO whatever the percentage, the same idea as Project 04's two-strikes rule.
5. **Conflicts are written down, not smoothed over.** Six are recorded (RC-01 to RC-06). The biggest: the risk appetite was scheduled for Q2 2027, but ISO 27001 needs acceptance criteria before any SoA can be approved, so it moves to October 2026.

## Three things I would say in an interview

1. **"Zero Implemented is the honest answer, not a harsh one."** *Applicable* means our risks need the control; *status* means it is running. Applicable and not yet running is legitimate, provided the treatment plan dates it.
2. **"Annex A is not the standard."** Clauses 4–10 are, and none can be excluded. A company with good policies still fails Stage 1 if it has never run an internal audit or a management review.
3. **"The most likely serious finding isn't technical."** It is six vendors with no data processing agreement: a GDPR gap today, fixed with signatures by 31 October 2026.

## Reuse this work

- [Statement of Applicability template](../templates/iso27001-soa-template.md) · [Excel, with automatic status and readiness score](../templates/iso27001-soa-template.xlsx) · [CSV](../templates/iso27001-soa-template.csv)
- [Clauses 4–10 readiness assessment template](../templates/iso27001-readiness-assessment-template.md) · [Word](../templates/iso27001-readiness-assessment-template.docx) · [CSV](../templates/iso27001-readiness-assessment-template.csv)

---

[← 04 Vendor Risk](../04-vendor-risk-management/) · [Portfolio home](../README.md) · Next: 06 SOC 2 readiness & internal audit (coming soon)
