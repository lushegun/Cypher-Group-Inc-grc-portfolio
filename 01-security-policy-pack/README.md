[← Portfolio home](../README.md) · [Next: 02 Risk Register →](../02-risk-register/)

# 01 · Startup Security Policy Pack

**Cypher Group Inc. · CGI-POL-001 to CGI-POL-005 · Version 1.0 · Approved 01 Sep 2026**

![ISO 27001](https://img.shields.io/badge/ISO%2FIEC%2027001%3A2022-38%20controls%20mapped-0B2545?style=flat-square)
![NIST CSF](https://img.shields.io/badge/NIST%20CSF%202.0-GV%20·%20ID%20·%20PR%20·%20DE%20·%20RS%20·%20RC-13315C?style=flat-square)
![NIST 800-63B](https://img.shields.io/badge/NIST%20SP%20800--63B--4-aligned-1B4965?style=flat-square)

> [!IMPORTANT]
> **Fictional case study.** Cypher Group Inc. does not exist. Every name, date, approval and record is invented to demonstrate policy development, framework mapping and policy governance.

## The business problem

Cypher Group kept receiving security questionnaires from prospective customers. The first question was almost always:

> *"Do you maintain a documented information security policy, approved by management and reviewed at least annually?"*

The answer was **No** — and three deals were stuck at security review. This pack changes the answer to **Yes**, and supplies the evidence an auditor would ask for.

## What's in this folder

| Document | What it is | Read online | Download |
|---|---|---|---|
| **Security Policy Pack** (CGI-POL-001 to 005) | Five approved policies with embedded standards, framework mapping, exception register and policy register | [View](01-security-policy-pack.md) | [PDF](01-security-policy-pack.pdf) · [Word](01-security-policy-pack.docx) |
| **Policy Sign-off & Training Tracker** (CGI-TRK-001) | The evidence that people actually acknowledged the policies, enrolled in MFA and completed training | [View](01-policy-signoff-tracker.md) | [PDF](01-policy-signoff-tracker.pdf) · [Excel](01-policy-signoff-tracker.xlsx) |
| **Data sets** | Policy register, exception register, framework mapping, tracker and escalation rules as CSV | [Browse](data/) | CSV |

> [!TIP]
> On a phone? Open the **PDF** — GitHub previews it in the browser. To download any file, open it and click the **Download raw file** button (↓) at the top right.

## The five policies at a glance

| ID | Policy | The decision that matters most |
|---|---|---|
| CGI-POL-001 | Acceptable Use | **AI tools:** approved list only; no Confidential or Restricted data in any unapproved AI tool; AI output is unverified until a competent person reviews it (§4.5) |
| CGI-POL-002 | Password & MFA | **Phishing-resistant MFA** (FIDO2 / passkeys) for every privileged account; SMS banned as a factor; length over complexity and no forced rotation, per NIST SP 800-63B-4 (§4.1, §4.3) |
| CGI-POL-003 | Onboarding & Offboarding (JML) | **All access revoked within four hours** of departure; quarterly privileged access review; monthly orphaned-account check (§4.5, §4.7) |
| CGI-POL-004 | Data Classification | **Four tiers and a 14-row handling matrix** — plus an aggregation rule: one customer record is Confidential, a full export is Restricted (§4.1.3, §4.2) |
| CGI-POL-005 | Incident Reporting | **Report within one hour**, SEV1–SEV4 response targets, the GDPR 72-hour notification path, and a non-retaliation commitment (§5.2, §5.4, §5.6, §6.1) |

## Framework coverage

| Framework | Coverage |
|---|---|
| ISO/IEC 27001:2022 Annex A | **38 controls** mapped — A.5 (20), A.6 (5), A.7 (3), A.8 (10) |
| NIST CSF 2.0 | GOVERN · IDENTIFY · PROTECT · DETECT · RESPOND · RECOVER |
| SOC 2 Trust Services Criteria | CC1, CC2, CC5, CC6, CC7, CC9 |
| GDPR | Art. 5(1)(f), Art. 32, Art. 33, Art. 34 |

<sub>Mappings are the author's own analysis for a fictional scenario. No certification or attestation is claimed.</sub>

## Evidence snapshot — CGI-TRK-001

*As at 05 September 2026, five-person illustrative sample.*

| AUP signed | MFA verified | Training complete | Joiners pending activation |
|:-:|:-:|:-:|:-:|
| **60%** | **80%** | **60%** | **1** |

A tracker where every row is green is usually a tracker nobody maintains. The amber and red rows here are deliberate — and they feed straight into [Project 02](../02-risk-register/), where the 60% acknowledgement rate limits how much credit the policies earn in the risk scores.

## Three design decisions I can defend

1. **No forced password rotation.** Scheduled rotation makes people choose weaker, predictable passwords. The pack follows NIST SP 800-63B-4: long, unique, breach-screened passwords, changed only on evidence of compromise.
2. **Exceptions are time-limited and owned.** Every exception names an approver, a compensating control and an expiry date (Appendix B). An exception without an expiry date is just an unmanaged gap.
3. **Reporting beats blame.** People who report their own mistakes are protected (CGI-POL-005 §6.1), because a hidden incident does far more damage than a reported one.

## Reuse this work

- [Acceptable Use Policy template](../templates/acceptable-use-policy-template.docx) (Word)
- [Policy Sign-off & Training Tracker template](../templates/policy-signoff-tracker-template.xlsx) (Excel)

---

[← Portfolio home](../README.md) · [Next: 02 Master Risk Register →](../02-risk-register/)
