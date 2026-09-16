<p align="center">
  <img src="assets/banner.svg" alt="GRC Portfolio — Governance, Risk and Compliance" width="100%">
</p>

<p align="center">
  <b>A complete information security governance programme, built project by project for one fictional 50-person SaaS company.</b><br>
  Policies → risk → maturity → vendors → ISO 27001 → SOC 2 → cloud compliance.
</p>

<p align="center">
  <a href="https://http://www.linkedin.com/in/olushegun-s">LinkedIn</a> ·
  <a href="https://rb.gy/bvvh4a">Notion portfolio</a> ·
  <a href="templates/">Free templates</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ISO%2FIEC%2027001-2022-0B2545?style=flat-square" alt="ISO/IEC 27001:2022">
  <img src="https://img.shields.io/badge/NIST%20CSF-2.0-13315C?style=flat-square" alt="NIST CSF 2.0">
  <img src="https://img.shields.io/badge/NIST%20SP-800--30%20Rev.1-1B4965?style=flat-square" alt="NIST SP 800-30">
  <img src="https://img.shields.io/badge/SOC%202-TSC-2E86DE?style=flat-square" alt="SOC 2">
  <img src="https://img.shields.io/badge/GDPR-Art.%2032--34-5FA8D3?style=flat-square" alt="GDPR">
  <img src="https://img.shields.io/badge/AI%20governance-focus-2BAE66?style=flat-square" alt="AI governance">
</p>

---

## Start here — a 2-minute tour

> [!TIP]
> **Short on time?** Read these three things:
> 1. **[Project 01](01-security-policy-pack/)** — the AI-tools clause (§4.5) and the phishing-resistant MFA rule (§4.3.3) in the policy pack.
> 2. **[Project 02](02-risk-register/)** — why two of five risks are deliberately left **High** after treatment, and what it would cost to fix them.
> 3. **[Templates](templates/)** — the same documents as blank, reusable templates you can download.

## Projects

| # | Project | What it demonstrates | Headline result | Status |
|:-:|---|---|---|:-:|
| 01 | **[Startup Security Policy Pack](01-security-policy-pack/)** | Policy writing · framework mapping · policy governance | 5 policies · 38 ISO 27001 Annex A controls mapped · exception register · sign-off tracker | 
Published |
| 02 | **[Master Information Security Risk Register](02-risk-register/)** | NIST SP 800-30 risk assessment · control mapping · treatment planning | 5 risks · aggregate exposure 92 → 44 (−52%) · 10 treatment actions · 7 KRIs |  Published |
| 03 | NIST CSF 2.0 Gap Assessment & Maturity Scorecard | Maturity scoring · gap analysis · roadmap | All 22 CSF Categories · maturity 1.23 → target 2.68 · 18 recommendations | ⏳ Next |
| 04 | Third-Party / Vendor Risk Management Programme | Vendor tiering · questionnaires · contract controls · AI vendor risk | 17 vendors tiered · 74-question questionnaire · 3 completed assessments | ⏳ Next |
| 05 | ISO/IEC 27001:2022 Readiness & Statement of Applicability | ISMS scoping · SoA · internal audit | — | 🔧 In progress |
| 06 | SOC 2 Type II Readiness & Audit Workpapers | Control testing · evidence · sampling | — | 🗓️ Planned |
| 07 | AWS Cloud Compliance (CIS Benchmark) | Cloud configuration review · control mapping | — | 🗓️ Planned |

## How the projects connect

Every project builds on the one before it, the way a real GRC programme does.

```mermaid
flowchart LR
    P1["01 · Policy pack<br/>the rules"] --> P2["02 · Risk register<br/>what could go wrong"]
    P1 --> P3["03 · CSF 2.0 gap assessment<br/>how mature are we"]
    P2 --> P3
    P2 --> P4["04 · Vendor risk<br/>who else holds our data"]
    P4 -->|new risks VR-001 to VR-009| P2
    P2 --> P5["05 · ISO 27001 SoA<br/>which controls and why"]
    P3 --> P5
    P5 --> P6["06 · SOC 2 readiness<br/>prove it works"]
    P6 --> P7["07 · AWS compliance<br/>prove it in the cloud"]
```

## The scenario — Cypher Group Inc. *(fictional)*

| | |
|---|---|
| **Company** | 50-person B2B SaaS, project-management platform, ~200 SMB customers |
| **Stack** | AWS · GitHub · Slack · Google Workspace · Stripe (payment metadata only) |
| **Starting point** | No formal GRC programme. Three enterprise deals stuck at security review. |
| **The job** | Build the programme that gets those deals through — and survives an audit. |

## Free templates

Blank, reusable versions of the documents in this portfolio. Download, replace the `[BRACKETED]` fields, and use them.

| Template | Formats |
|---|---|
| Acceptable Use Policy | [Word](templates/acceptable-use-policy-template.docx) · [Markdown](templates/acceptable-use-policy-template.md) |
| Policy Sign-off & Training Tracker | [Excel](templates/policy-signoff-tracker-template.xlsx) · [CSV](templates/policy-signoff-tracker-template.csv) |
| Information Security Risk Register (NIST SP 800-30, 5 × 5) | [Word](templates/risk-register-template.docx) · [Markdown](templates/risk-register-template.md) · [CSV](templates/risk-register-template.csv) |

➡️ **[Browse all templates](templates/)** · or download everything at once from **[Releases](../../releases/latest)**.

## Skills demonstrated

| Area | Evidence |
|---|---|
| **Governance** | Policy hierarchy, document control, exception management, policy register — [01](01-security-policy-pack/) |
| **Risk management** | Anchored 5 × 5 scales, inherent vs residual scoring, all four treatment strategies, KRIs — [02](02-risk-register/) |
| **Compliance mapping** | ISO/IEC 27001:2022 Annex A, NIST CSF 2.0, SOC 2 TSC, GDPR — [01](01-security-policy-pack/), [02](02-risk-register/) |
| **AI governance** | Approved-AI-tools control and data restrictions for AI use — [01 §4.5](01-security-policy-pack/01-security-policy-pack.md#45-use-of-artificial-intelligence-tools) |
| **Audit readiness** | Evidence trackers, escalation rules, retention periods, honest limitation statements |
| **Tooling** | Excel (formulas, validation, conditional formatting), Markdown, Notion, GitHub |

## About me

Documenting Governance, Risk and Compliance from an analytical background (MSc Applied Economics & Data Analytics). Focusing on practical security governance for growing companies, with a recent interest in **AI governance**: how organisations let people use AI tools without leaking the data they are trusted with.

**Open to:** GRC Analyst · Information Security Analyst · IT Audit · Security Compliance roles — Germany / EU, UK and remote.
**Contact:** [LinkedIn](https://www.linkedin.com/in/olushegun-s)

---

<sub>**Fictional data notice.** Cypher Group Inc. and every person, record, date and finding in this repository are invented to demonstrate applied GRC capability. No real company or personal data is used, and no certification or attestation is claimed. Framework mappings are the author's own analysis. Templates are free to reuse under the licence in this repository.</sub>
