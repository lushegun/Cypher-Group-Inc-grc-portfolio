[← Portfolio home](../README.md) · [All templates](README.md)

# [ORGANISATION] — Vendor Security Assessment Report

**Assessment ID:** [VRA-YYYY-nnn]

> [!TIP]
> **How to use this template.** Everything in `[SQUARE BRACKETS]` is a field to replace.
> Everything outside them is method and should be changed only deliberately. Guidance sits in
> `>` blockquotes and is deleted before the document is issued. Derived from CGI-TPR-001 v1.0.

## 1. Assessment header

| Field | Value |
|---|---|
| Assessment ID | [VRA-YYYY-nnn] |
| Vendor | [Vendor legal name] — [VEN-nnn] |
| Service assessed | [What it does for us — be specific about the plan or tier in use] |
| Business owner | [Job title — never a person's name] |
| **Tier** | **[1/2/3]** — [trigger(s) fired, or factor total D+A+C+R] |
| Assessment depth applied | [Full questionnaire / Lite / Attestation] |
| Assessor / Approver | [Assessor] / [Approver, job title] |
| Date | [DD Month YYYY] |
| **Weighted score** | **[nn]%** ([deduction] deducted from a maximum of [max], net of [n] N/A) |
| Weight-5 questions Not Met | **[n]** (against a Fail threshold of [2]) |
| Inherent vendor risk | **[n] — [band]** (L[n] × I[n]) |
| Residual vendor risk | **[n] — [band]** (L[n] × I[n]) |
| Post-remediation target | **[n] — [band]** |
| **Decision** | **[PASS / PASS WITH CONDITIONS / FAIL — REMEDIATE OR EXIT / ACCEPTED]** |

## 2. Reviewer assessment

> Three or four paragraphs, and make the first one do real work. State plainly **whether the failures
> are the vendor's or yours** — in a well-run assessment of a mature vendor, most findings are the
> customer's governance failures, and saying so changes what the remediation looks like.
>
> Then justify the residual score explicitly. **If no control of yours reduces the risk, residual equals
> inherent, and that is itself the finding.** Scoring a reduction because the vendor is reputable is the
> "your vendor's certification is your vendor's control" error.

[Paragraph 1 — what this vendor is to us and why the tier is what it is.]

[Paragraph 2 — the headline judgement, and where the failure actually sits.]

[Paragraph 3 — justification of the residual score.]

## 3. Findings

| ID | Sev | Finding | Question(s) | Evidence | Risk if unaddressed |
|---|---|---|---|---|---|
| [F-001] | [🔴 Critical / 🟠 High / 🟡 Medium / 🟢 Low / ⚪ Observation] | [What is true, stated as a fact, not as an opinion] | [VQ-nn] | [What was or was not produced] | [Business consequence, tied to a risk ID or a policy clause] |
| [F-002] | | | | | |

> **Severity guidance.** Critical = a present-tense regulatory non-conformity, or a control whose absence
> defeats a written commitment. High = a control gap that materially raises likelihood or impact.
> Medium = an assurance or visibility gap. Low = recorded, accepted as normal commercial practice.

## 4. Remediation plan *(Fail and Pass-with-conditions only)*

| Action | Closes | Owner (Job Title) | Due | Cost | Verification |
|---|---|---|---|---|---|
| [R1] [Verb-first action] | [F-001] | [Job title] | [DD Mon YYYY] | [Nil / USD n] | [The artifact that proves it happened] |
| [R2] | | | | | |

**Total remediation cost: [approximately USD n].** [State how many actions cost nothing — at small
companies most findings are governance failures with a near-zero price tag.]

**Re-assessment: [DD Month YYYY].** [Vendor] may not operate in Fail status beyond [one quarter] without
an approved, **expiring** risk acceptance.

## 5. Conditions of the pass *(Pass-with-conditions only)*

| # | Condition | Owner (Job Title) | Due | Evidence required |
|:-:|---|---|---|---|
| [C1] | [Condition] | [Job title] | [Date] | [Artifact] |

**[State which condition, if missed, lapses the conditional pass to Fail — and why.]**

## 6. Acceptance record *(Accepted only)*

| Field | Value |
|---|---|
| Acceptance ID | **[ACC-Vnn]** |
| What is accepted | [The specific residual exposure, in one sentence] |
| Justification | [Data classification · production access · availability dependency · replaceability · assurance held · residual score] |
| Compensating control | [What you changed so the acceptance is narrower than it would otherwise be] |
| Owner (Job Title) | [Job title] |
| Approved by | [Approval authority for this tier] |
| Date | [DD Month YYYY] |
| **Expiry** | **[DD Month YYYY]** — or earlier on any change of service, data type or plan |

> **Every acceptance expires.** An acceptance with no expiry is a decision that quietly becomes permanent
> without anyone deciding it should be.
>
> **If your organisation has not declared a risk appetite, record that here.** An acceptance made against
> an undeclared tolerance is personal rather than institutional, and the next reviewer needs to know.

## 7. Distribution and retention

| | |
|---|---|
| Distribution | [Approver] · [Business owner] · [Risk register owner] |
| Retained in | [Location] |
| Retention period | [n] years after the vendor relationship ends |
| Linked records | Inventory row [VEN-nnn] · Risk IDs [  ] · Acceptance [ACC-Vnn] |
