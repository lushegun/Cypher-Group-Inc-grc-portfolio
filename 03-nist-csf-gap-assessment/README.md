[← Portfolio home](../README.md) · [← 02 Risk Register](../02-risk-register/) · [Next: 04 Vendor Risk →](../04-vendor-risk-management/)

# 03 · NIST CSF 2.0 Gap Assessment & Maturity Scorecard

**Cypher Group Inc. · CGI-GAP-001 · Version 1.0 · Assessed 15 Sep 2026 · all 22 CSF 2.0 Categories**

![CSF](https://img.shields.io/badge/NIST%20CSF%202.0-22%20Categories-0B2545?style=flat-square)
![Maturity](https://img.shields.io/badge/maturity-1.23%20→%20target%202.68-13315C?style=flat-square)
![ISO](https://img.shields.io/badge/ISO%2FIEC%2027001%3A2022-mapped%20on%20every%20row-1B4965?style=flat-square)

> [!IMPORTANT]
> **Fictional case study.** Cypher Group Inc. does not exist. Every finding, score and figure was created to demonstrate applied GRC method.

<p align="center"><img src="images/03-radar-current-vs-target.png" alt="Radar chart of current versus target maturity for the six NIST CSF 2.0 Functions" width="720"></p>

## The question this answers

The company has written five policies ([Project 01](../01-security-policy-pack/)) and scored its risks ([Project 02](../02-risk-register/)). The CEO's question: **"What are we still missing, how far are we from where we need to be, and what do we fix first?"**

## What's in this folder

| Document | What it is | Read online | Download |
|---|---|---|---|
| **Gap Assessment** (CGI-GAP-001) | Maturity scale, declared target, 22 findings with 16 fields each, heatmap, 18-item roadmap, CEO one-pager, consistency checks | [View](03-nist-csf-gap-assessment.md) | [PDF](03-nist-csf-gap-assessment.pdf) · [Excel](03-nist-csf-gap-assessment.xlsx) |
| **Heatmap data** | How every Function average was calculated, and how to build the radar chart yourself | [View](03-heatmap-data.md) | [Chart PNG](images/03-radar-current-vs-target.png) |
| **Data sets** | The 22-Category grid, the heatmap and the roadmap as CSV | [Browse](data/) | CSV |

## How I did it

1. **Declared the target before scoring anything.** Maturity 3 in the 15 Categories that carry residual risk or a written GDPR commitment, 2 in the other 7, and **4 in none**. A target of 4 everywhere produces 22 complaints; a declared target produces a budget request.
2. **Scored every Category on a written 0–4 scale.** An approved policy that nobody has evidenced using is a **2**, never a 3.
3. **Cited a specific policy clause and a specific evidence source in every finding.** For example, CGI-POL-003 §4.7.1 requires a quarterly privileged access review, and the tracker shows none has been done, so that control is *documented, not operating*.
4. **Reconciled the scores against the risk register**, including the one case that looks like a contradiction, explained in writing.
5. **Built an 18-item roadmap ordered by risk reduction ÷ effort**, and stated both places where a dependency overrides that order.

## Result

| | |
|---|---|
| Overall current maturity | **1.23 / 4.00** (27 ÷ 22) |
| Declared target | **2.68 / 4.00** (59 ÷ 22) — average gap **1.45** |
| Weakest Function | **RECOVER — 0.50** (backups exist, but no restore has ever been tested) |
| Categories scoring 0 | **GV.SC** supply chain · **PR.PS** platform security · **PR.IR** infrastructure resilience · **RC.CO** recovery communication |
| Only Category at 3 | **ID.RA** risk assessment — the one control shown to be designed *and* operating |
| Roadmap | 18 recommendations in 4 waves; Waves 1–2 lift maturity to about **1.73**, mostly with existing staff time |
| After [Project 04](../04-vendor-risk-management/) | GV.SC rises 0 → 2, so overall maturity becomes **1.32** |

| Function | Current | Target | Gap |
|---|:-:|:-:|:-:|
| GOVERN | 1.33 | 2.67 | 1.33 |
| IDENTIFY | 1.67 | 2.67 | 1.00 |
| PROTECT | 1.00 | 3.00 | **2.00** |
| DETECT | 1.00 | 2.50 | 1.50 |
| RESPOND | 1.50 | 2.50 | 1.00 |
| RECOVER | **0.50** | 2.50 | **2.00** |

## The finding that matters

The two risks that stayed **High** in Project 02 are a production API authorisation flaw (R-004) and an AWS misconfiguration (R-005). They sit behind the two Categories scoring **0**: PR.PS (control gap CG-02) and PR.IR (CG-03). **They are not High because the policy work failed. They are High because policy was never the control that addressed them.** A policy pack cannot reach the code path or the cloud configuration.

## Three rules I can defend

1. **A policy is a 2, a record is a 3, a metric is a 4.** Design effectiveness and operating effectiveness are different things.
2. **A clause is not a capability.** CGI-POL-001 §4.6.1 already requires CTO approval before anyone uses a new vendor, yet supply chain still scores 0. One approval rule, with no inventory, no method and no records behind it, is a fragment, not a programme. Every such fragment is named in its finding, so the reader can see it was weighed and not missed.
3. **Finding a High risk shows the risk process is working.** Risk Assessment scores 3 even though two risks sit at residual High. The High risks come from the Categories that own the *missing controls*, and both of those score 0.

## What I would do differently

- **Go to Subcategory depth on PROTECT**, where one Category score currently covers five very different outcomes.
- **Interview the engineers.** Informal code review probably happens, but on this scale an unrecorded practice still cannot score above 1.

## Reuse this work

- [NIST CSF 2.0 gap assessment template](../templates/nist-csf-gap-assessment-template.docx) (Word) · [CSV](../templates/nist-csf-gap-assessment-template.csv) · [Markdown](../templates/nist-csf-gap-assessment-template.md)

---

[← 02 Risk Register](../02-risk-register/) · [Portfolio home](../README.md) · [Next: 04 Vendor Risk →](../04-vendor-risk-management/)
