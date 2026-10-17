[← Portfolio home](../README.md) · [← 06 SOC 2 Readiness & Internal Audit](../06-soc2-readiness-internal-audit/) · [Next: 08 AI Governance →](../08-ai-governance-eu-ai-act-iso42001/)

# 07 · Cloud Configuration Compliance Review (CIS Benchmark)

**Cypher Group Inc. · CGI-AWS-001 · Version 1.0 · 16 Oct 2026 · 63 CIS recommendations · 15 findings · R-005 re-scored**

![CIS](https://img.shields.io/badge/CIS%20AWS%20Foundations-v5.0.0-0B2545?style=flat-square)
![Score](https://img.shields.io/badge/profile%20score-24.4%25%20·%20baseline%20not%20met-C0392B?style=flat-square)
![Findings](https://img.shields.io/badge/findings-3%20critical%20·%206%20high%20·%204%20medium%20·%202%20low-13315C?style=flat-square)
![CUECs](https://img.shields.io/badge/CloudCo%20CUECs%20performed-0%20of%204-1B4965?style=flat-square)

> [!IMPORTANT]
> **Simulated case study.** No real cloud account was scanned; every configuration result is a labelled scenario. The benchmark, the Security Hub control IDs, the audit commands and the mappings are real.

## The question this answers

Projects 01 to 06 describe what Cypher **says** it does. Every one of them pointed at the same gap: nobody had looked at how the cloud is actually configured (control gap **CG-03**, recommendation **REC-11**). The CEO's question: **"Is our cloud set up safely, and are we doing the four things our cloud provider assumes we do?"**

This is a compliance and configuration review against a published benchmark, not cloud engineering.

## What's in this folder

| Document | What it is | Read online | Download |
|---|---|---|---|
| **Cloud configuration review** (CGI-AWS-001) | Scope and profile, all 63 recommendations, the featured five, CUEC close-out, five-way mapping, findings, the R-005 recalculation, roadmap, CEO one-pager | [View](07-aws-cloud-compliance.md) | [PDF](07-aws-cloud-compliance.pdf) · [Excel](07-aws-cloud-compliance.xlsx) |
| **The assessment** | 63 recommendations × 23 columns, one value per cell | [View as table](07-aws-cloud-compliance.csv) | CSV |
| **Data sets** | Assessment, featured five, findings, severity rule, five-way map, CUECs, C1–C4, R-005 credit test and recalculation, register delta, roadmap, conflicts, maturity, scope, limitations, profile | [Browse](data/) | 16 CSVs |

## At a glance

| Measure | Result |
|---|---|
| Benchmark | **CIS AWS Foundations v5.0.0**, the version AWS Security Hub CSPM automates |
| Recommendations | **63: 12 PASS · 48 FAIL · 3 N/A** |
| Scores | All applicable **20.0%** · Level 1 **27.5%** · **Cypher profile 24.4%** (Level 1 + six Level 2 items policy and contracts require) |
| Security Hub coverage | 37 of 63 recommendations (58.7%). A fully green Security Hub dashboard still leaves the rest unchecked |
| Findings | **15: 3 Critical · 6 High · 4 Medium · 2 Low** |
| CloudCo CUECs | **0 of 4 performed.** Conditions C1–C4: none closed; C1 still closable by 15 Dec 2026 |
| **R-005 (cloud misconfiguration)** | Residual **12 → 20, High → Critical.** Register moves to **v1.2**: residual total 122 → 130 |
| Path back | 20 → 10 by 30 Nov 2026 → 8 → **6 by 31 Jan 2027** (TP-09 target) → 3 by Jun 2027 |
| Claim CIS alignment to buyers? | **NO-GO** while any Critical or High finding is open |
| NIST CSF 2.0 maturity | **1.32, unchanged.** A review that finds a control absent measures the gap; it does not close it |

## The finding I would lead with

The risk register lowered R-005 from 20 to 12, crediting access reviews, change tickets, role profiles and "encryption at rest".

- **Not one of those controls was operating.** The access reviews never ran, and there were no change tickets. Every engineer holds full administrator rights.
- **The encryption was SSE-S3**, which S3 decrypts for anyone the bucket policy allows, including everyone if the bucket goes public.

So R-005 goes back up to 20. But the tempting reason is wrong:

> **"Block Public Access is off, so the risk goes up" counts the weakness twice.** The register never gave Block Public Access any credit. The score rises because the evidence disproves the controls the register **did** credit.

## Five design decisions

1. **All 63 recommendations, not a sample of five.** Five deep dives carry the story; the full matrix carries the verdict.
2. **Two numbering systems, both shown.** `IAM.9` is a Security Hub control and `1.4` is the CIS recommendation it tests. Four of the first five identifiers proposed for this review were wrong, so the corrections are part of the record.
3. **Policy outranks the profile.** CGI-POL-002 demands hardware root MFA and CloudCo's CUEC demands log file validation. So the profile is Level 1 plus those six Level 2 items, whatever CIS calls them.
4. **Severity by a rule published first.** Critical means an exposure that exists now and is reachable from outside. The three Criticals share one root cause: temporary access that was never revoked.
5. **Restraint on every score.** No new risk (every finding sits inside R-005's scenario), and no maturity Category moves.

## Reuse this work

- [CIS AWS assessment template](../templates/cis-aws-assessment-template.md) · [CSV](../templates/cis-aws-assessment-template.csv): all 63 v5.0.0 recommendations pre-filled with level, status, Security Hub ID, audit command and default mappings
- [Multi-framework mapping template](../templates/multi-framework-mapping-template.md) · [CSV](../templates/multi-framework-mapping-template.csv): CIS → ISO/IEC 27001 → SOC 2 → CSF → risk
- [Cloud findings register template](../templates/cloud-findings-register-template.md) · [CSV](../templates/cloud-findings-register-template.csv): with the severity rule

---

[← 06 SOC 2 readiness & internal audit](../06-soc2-readiness-internal-audit/) · [Portfolio home](../README.md) · [Next: 08 AI governance →](../08-ai-governance-eu-ai-act-iso42001/)
