[← Portfolio home](../README.md) · [← 01 Policy Pack](../01-security-policy-pack/)

# 02 · Master Information Security Risk Register

**Cypher Group Inc. · CGI-RSK-001 · Version 1.0 · Assessed 08 Sep 2026 · NIST SP 800-30 Rev. 1**

![Method](https://img.shields.io/badge/method-NIST%20SP%20800--30%20Rev.1%20·%205×5-0B2545?style=flat-square)
![Reduction](https://img.shields.io/badge/aggregate%20exposure-92%20→%2044%20(−52%25)-2BAE66?style=flat-square)
![High](https://img.shields.io/badge/residual%20High-2%20of%205-E67E22?style=flat-square)

> [!IMPORTANT]
> **Fictional case study.** Cypher Group Inc. does not exist. All scores, costs, names and approvals are invented to demonstrate risk identification, scoring, control mapping and treatment decisions.

## The question this answers

Project 01 wrote the rules. This project asks: **how much safer did those rules actually make the company — and where are we still exposed?**

Five realistic threat scenarios were scored twice — **inherent** (no controls) and **residual** (crediting only controls that exist and operate) — and every mitigating control is traced to a specific clause in the [Project 01 policy pack](../01-security-policy-pack/).

## What's in this folder

| Document | What it is | Read online | Download |
|---|---|---|---|
| **Master Risk Register** (CGI-RSK-001) | Scoring scales, the register, residual rationale, treatment plan, accepted and avoided risk, control gaps, KRIs, limitations | [View](02-master-risk-register.md) | [PDF](02-master-risk-register.pdf) · [Excel](02-master-risk-register.xlsx) |
| **Data sets** | Register, residual rationale, treatment plan, control gaps and KRIs as CSV | [Browse](data/) | CSV |

## The five risks

| ID | Scenario | Inherent | Residual | Treatment | Owner |
|---|---|:-:|:-:|---|---|
| R-001 | Phishing → account takeover via relayed one-time codes | 🟥 20 | 🟨 6 | Mitigate | IT Operations Manager |
| R-002 | Ransomware on an employee endpoint | 🟥 20 | 🟨 8 | Mitigate + Transfer | IT Operations Manager |
| R-003 | Departing employee exports customer data | 🟧 12 | 🟨 6 | Mitigate | Head of People and Operations |
| R-004 | Broken object-level authorisation in the production API | 🟥 20 | 🟧 **12** | Mitigate | Chief Technology Officer |
| R-005 | Public S3 bucket through AWS misconfiguration | 🟥 20 | 🟧 **12** | Mitigate | Chief Technology Officer |

<sub>🟩 Low 1–4 · 🟨 Medium 5–9 · 🟧 High 10–14 · 🟥 Critical 15–25</sub>

## Heat maps

Each square is one likelihood × impact cell, coloured by rating band.

**Inherent** — before any controls

| Likelihood ↓ / Impact → | 1 | 2 | 3 | 4 | 5 |
|:-:|:-:|:-:|:-:|:-:|:-:|
| **5** | 🟨 | 🟧 | 🟥 | 🟥 **R-001** | 🟥 |
| **4** | 🟩 | 🟨 | 🟧 | 🟥 | 🟥 **R-002** **R-004** **R-005** |
| **3** | 🟩 | 🟨 | 🟨 | 🟧 **R-003** | 🟥 |
| **2** | 🟩 | 🟩 | 🟨 | 🟨 | 🟧 |
| **1** | 🟩 | 🟩 | 🟩 | 🟩 | 🟨 |

**Residual** — after the Project 01 policy pack

| Likelihood ↓ / Impact → | 1 | 2 | 3 | 4 | 5 |
|:-:|:-:|:-:|:-:|:-:|:-:|
| **5** | 🟨 | 🟧 | 🟥 | 🟥 | 🟥 |
| **4** | 🟩 | 🟨 | 🟧 | 🟥 | 🟥 |
| **3** | 🟩 | 🟨 | 🟨 | 🟧 **R-004** **R-005** | 🟥 |
| **2** | 🟩 | 🟩 | 🟨 **R-001** **R-003** | 🟨 **R-002** | 🟧 |
| **1** | 🟩 | 🟩 | 🟩 | 🟩 | 🟨 |

R-004 and R-005 only move one step on likelihood: the policy pack governs *who* may change code and cloud settings, not *how* software is tested or *how* cloud storage must be configured.

## The honest headline

> **The policy pack removes just over half of the assessed exposure at almost no direct cost. It does not touch two of the five scenarios — because it contains no rules on how software is built or how cloud infrastructure is configured.** Those two stay High, and they are where the next USD 32,100 should go.

| Metric | Value |
|---|---|
| Aggregate inherent → residual | 92 → 44 (**−52%**) |
| Residual High | 2 (R-004, R-005) — accepted by the CEO pending treatment |
| Treatment actions | 10 (TP-01 to TP-10), year-one cost **USD 32,100** |
| Control gaps | 5 (CG-01 to CG-05) |
| New policies recommended | Backup & Recovery · Secure Development · Vulnerability Management |
| Key risk indicators | 7 (KRI-01 to KRI-07) with green / amber / red thresholds |

## All four treatment strategies, on the record

| Strategy | Where |
|---|---|
| **Mitigate** | All five risks — TP-01 to TP-10 |
| **Transfer** | Cyber insurance for ransomware (TP-04) — noting that reputational and regulatory liability cannot be transferred |
| **Accept** | ACC-001: SMS MFA for two finance users on a legacy portal, owned by the CTO, **expires 03 Mar 2027** |
| **Avoid** | AVD-001: Cypher never stores card numbers, so PCI DSS scope is avoided by design |

## Three things I would say in an interview

1. **"I score the control that is operating, not the control that is written."** Only 60% of staff had acknowledged the policies, so no residual score was credited at full policy strength.
2. **Backups are the seatbelt, not the brakes.** Patching and least privilege lower the *likelihood* of ransomware; tested backups are what lower the *impact* — and the pack has no backup policy, so R-002's impact only falls from 5 to 4.
3. **A 5 × 5 matrix ranks; it does not measure.** The register states its own limits: range compression, ordinal arithmetic, no incident history, and controls asserted rather than tested.

## Reuse this work

- [Risk register template](../templates/risk-register-template.docx) (Word) · [CSV](../templates/risk-register-template.csv) · [Markdown](../templates/risk-register-template.md)

---

[← 01 Policy Pack](../01-security-policy-pack/) · [Portfolio home](../README.md)
