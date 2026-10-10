[← Portfolio home](../README.md) · [← 05 ISO 27001 Readiness & SoA](../05-iso27001-readiness-soa/)

# 06 · SOC 2 Type II Readiness Assessment & Internal Audit Workpapers

**Cypher Group Inc. · CGI-SOC-001 + CGI-IAU-001 · Version 1.0 · 25 Sep 2026 · 38 criteria · 24 workpapers · 37 findings**

![SOC 2](https://img.shields.io/badge/SOC%202-2017%20TSC%20·%202022%20PoF-0B2545?style=flat-square)
![Criteria](https://img.shields.io/badge/criteria-38%20in%20scope%20·%208%20adequate%20design-13315C?style=flat-square)
![Readiness](https://img.shields.io/badge/Type%20I%2053.9%25%20·%20Type%20II%2036.0%25-NO--GO-C0392B?style=flat-square)
![Audit](https://img.shields.io/badge/internal%20audit-9%20major%20·%2010%20minor%20·%2018%20OFI-1B4965?style=flat-square)

> [!IMPORTANT]
> **Fictional case study.** Cypher Group Inc. does not exist. Every finding, score, date and cost was created to demonstrate applied GRC method. AICPA Trust Services Criteria and ISO/IEC 27001 wording are paraphrased; both must be obtained from their publishers.

## The question this answers

US and enterprise buyers ask for a SOC 2 report, not an ISO certificate. [Project 05](../05-iso27001-readiness-soa/) put the company on an ISO path for November 2027. The CEO's two questions here: **"Can we sell against a SOC 2, and did the controls we wrote down actually run?"** The second question is answered by auditing the company against its own ISMS — the internal audit ISO/IEC 27001 clause 9.2 requires.

## What's in this folder

| Document | What it is | Read online | Download |
|---|---|---|---|
| **SOC 2 readiness + internal audit** (CGI-SOC-001 · CGI-IAU-001) | Criteria selection, the 38-criterion crosswalk, draft system description with CUECs and CSOCs, readiness score with gates, 24 workpapers, findings register, audit report, PBC list, roadmap, CEO one-pager | [View](06-soc2-readiness-and-internal-audit.md) | [PDF](06-soc2-readiness-and-internal-audit.pdf) · [Excel](06-soc2-readiness-and-internal-audit.xlsx) |
| **The crosswalk** | All 38 criteria × 18 columns, one value per cell | [View as table](06-soc2-readiness-and-internal-audit.csv) | CSV |
| **Data sets** | Criteria selection, CUECs, CSOCs, the mirror, gates, score, framework overlap, workpapers, the WP-06 sample, findings, PBC list, roadmap, conflicts, maturity projection | [Browse](data/) | 15 CSVs |

## At a glance

| Measure | Result |
|---|---|
| Criteria in scope | **38** — Security CC1–CC9 (33), Availability A1 (3), Confidentiality C1 (2). Processing Integrity and Privacy excluded, with reasons |
| Criteria with adequate design / operating evidence | **8 / 0** |
| Type I readiness · Type II readiness | **53.9% · 36.0%** — both **NO-GO**, and **6 of 8 gates fail** |
| Internal audit findings | **37: 9 major · 10 minor · 18 OFI**, from **24 workpapers** |
| Evidence requests answered | **7 received · 7 partial · 36 of 50 do not exist (72%)** |
| Framework overlap | 77 of 88 applicable ISO controls have a criterion counterpart · 11 do not · **7 ISO clause requirements have no SOC 2 counterpart** |
| Realistic path | ISO certificate Nov 2027 → **Type I as of 31 Mar 2028** → Type II period Apr–Sep 2028 → **report ~Nov 2028** |
| Cost | **USD 50,000** for SOC 2, on top of the USD 55,000 already planned for ISO |
| NIST CSF 2.0 maturity after this project | **1.32, unchanged.** A crosswalk maps controls and a dry run tests them; neither implements anything |

## The finding I would lead with

The company must publish **ten complementary user entity controls** telling ~200 customers what they have to do for the platform's controls to work: enable MFA, review their own access, read their own logs, classify their own data.

Its own cloud provider wrote **four** such controls for Cypher Group Inc. **It has accepted none of them.** Four of the ten mirror those four, one for one.

> **A system description is only as honest as the layer beneath it.**

## Five design decisions

1. **The criteria were chosen against the risk register, not the sales objection.** Processing Integrity is out because no risk concerns calculation accuracy; Privacy is out because it is the weakest evidence ground the company has — six vendors with no data processing agreement and no Article 30 record.
2. **Scores come from controls, not opinions.** Each criterion inherits the mean maturity of the ISO controls mapped to it (CRL 0–3), and **design is "adequate" only if no mapped control sits at zero** — one hole sinks a good average.
3. **The dating rule was published before any finding was graded.** Clause requirements are due now; a control is a nonconformity only once its own target date has passed, or where it breaches a present-tense legal duty. That is why nine of ten control findings are OFIs, and why six vendors with no DPA is a major.
4. **You cannot sample nothing.** Where the population is zero, no sample is drawn and no operating conclusion is reached. The most instructive finding is OFI-06: the leaver control is not failed, it is **untestable**, because no leaver register exists.
5. **The audit declares its own limitation.** The auditor wrote the Statement of Applicability being tested, so this is a **dry run** that does not discharge clause 9.2. Saying so is the finding (OFI-08). *The project that proves a control cannot be the control.*

## Reuse this work

- [TSC crosswalk template](../templates/soc2-tsc-crosswalk-template.md) · [CSV](../templates/soc2-tsc-crosswalk-template.csv) — 38 criteria pre-filled, scoring method restated
- [Internal audit workpaper template](../templates/internal-audit-workpaper-template.md) · [Word](../templates/internal-audit-workpaper-template.docx) · [CSV](../templates/internal-audit-workpaper-template.csv)
- [PBC evidence request list template](../templates/pbc-request-list-template.md) · [CSV](../templates/pbc-request-list-template.csv)

---

[← 05 ISO 27001 Readiness & SoA](../05-iso27001-readiness-soa/) · [Portfolio home](../README.md) · Next: 07 AWS cloud compliance, CIS Benchmark (coming soon)
