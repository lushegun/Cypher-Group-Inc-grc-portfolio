[← Portfolio home](../README.md) · [All templates](README.md)

# NIST CSF 2.0 Gap Assessment & Maturity Scorecard — Reusable Template

### Blank, bracketed version · derived from CGI-GAP-001 v1.0

> [!TIP]
> **How to use.** Replace every `[BRACKETED]` value. Delete nothing structural. Work top to bottom:
> declare the target state **before** you score anything, because scoring first and rationalising the
> target afterwards is the most common way a gap assessment becomes unfalsifiable.

> [!NOTE]
> If you are using this on a fictional scenario for a portfolio, keep a fictional-data notice at the top.
> If you are using it on a real organisation, delete the notice and mark the document with the appropriate
> classification instead.

---

## Document control

| Field | Value |
|---|---|
| Document ID | `[XXX-GAP-001]` |
| Title | `[Organisation]` NIST CSF 2.0 Security Gap Assessment and Maturity Scorecard |
| Version | `[1.0]` |
| Status | `[Draft / Final — issued for management review]` |
| Assessment date | `[DD Month YYYY]` |
| Prepared by (Assessor) | `[Name or initials]` |
| Approving authority | `[Name, Job Title]` |
| Framework | NIST Cybersecurity Framework (CSF) 2.0 — NIST CSWP 29, published 26 February 2024 |
| Assessment depth | `[Category level — 22 Categories / Subcategory level — 106 Subcategories]` |
| Maturity scale | 0–4 CMMI-style capability maturity |
| Secondary mapping | `[ISO/IEC 27001:2022 Annex A / SOC 2 TSC / CIS Controls v8]` |
| Inputs consumed | `[Policy pack IDs] · [Evidence tracker ID] · [Risk register ID]` |
| Next review | `[Date]` or on material change |

---

## 1. Scope

| In scope | Out of scope |
|---|---|
| `[All 22 CSF 2.0 Categories]` | `[Subcategory-level depth]` |
| `[Named systems and platforms]` | `[Physical security / data centre]` |
| `[Headcount and device estate]` | `[Penetration testing or technical validation]` |
| `[Policy pack and evidence tracker]` | `[Third-party providers themselves]` |
| `[Risk register IDs and control gaps]` | `[Financial audit, DPIA, Article 30 records]` |

---

## 2. Maturity scale

| Score | Level | Definition | Evidence required to claim this level |
|---|---|---|---|
| **0** | **Not Performed** | The outcome is not achieved in any form. No policy, no practice, no owner, no evidence. If asked, the honest answer is 'we do not do this'. | `[Evidence standard for this level]` |
| **1** | **Initial / Ad Hoc** | The outcome is achieved occasionally, reactively and person-dependently. There is no written expectation, nothing is scheduled, and if the individual concerned left, the activity would stop. No reliable evidence is produced. | `[Evidence standard for this level]` |
| **2** | **Documented / Repeatable** | An approved policy, standard or procedure exists, ownership is assigned and the expectation is communicated. Execution is inconsistent, incomplete or unevidenced. This is design effectiveness without operating effectiveness - the control would work if followed, but no artifact proves it was. | `[Evidence standard for this level]` |
| **3** | **Defined and Operating** | The activity is performed consistently on a defined schedule by the assigned owner, and each occurrence produces retained evidence. Exceptions are recorded and tracked. This is design plus operating effectiveness and is the level at which an external auditor can test the control. | `[Evidence standard for this level]` |
| **4** | **Managed and Measured** | Performance of the activity is measured against defined metrics or KRIs with thresholds, the results are reported to leadership, and the activity is adjusted on the basis of the data rather than on opinion. Continuous improvement is evidenced. | `[Evidence standard for this level]` |

> Replace the definitions only if you have a reason to. These are the standard CMMI-derived readings and
> keeping them means your scores are comparable to other people's.

**Scoring rules to keep:** score down when between two levels · an approved but unevidenced policy is a 2,
never a 3 · **a clause is not a capability** — a single clause that touches one outcome is recorded in the
finding but does not lift the Category a level on its own.

---

## 3. Declared target state

> **DECLARED TARGET STATE — `[Organisation]`, to be achieved by `[Quarter Year]`**
>
> `[Organisation]` will operate at **NIST CSF Implementation Tier `[1-4]` (`[Partial / Risk Informed /
> Repeatable / Adaptive]`)**, expressed at Category level as:
>
> - **Maturity `[3]` in `[n]` Categories** that `[trigger: carry a residual Medium or High risk / are
>   load-bearing for a stated regulatory obligation / are routinely tested by customer questionnaires]`.
> - **Maturity `[2]` in the remaining `[n]` Categories**, where `[justification]`.
> - **Maturity 4 in `[no / n]` Categories in this cycle**, because `[justification]`.
>
> Overall target: **`[X.XX]` / 4.00**.

**Justification — answer all four:**

1. **Proportionality.** `[Headcount, revenue, customer count, regulatory exposure — and why level 4 across
   the board would exceed the available budget or management capacity]`
2. **Sequencing.** `[Which Categories score 0 or 1, and why fixing those beats measuring the ones that work]`
3. **Falsifiability.** `[Why a uniform target of 4 is equivalent to having no target at all]`
4. **Risk appetite.** `[What level brings residual risk inside the appetite the business has declared]`

---

## 4. Assessment grid

Sixteen columns. Machine-readable blank: `templates/nist-csf-gap-assessment-template.csv`.

| Ref ID | Function | Category | Category Description | Current State Observation | Evidence Source | Current Score (0-4) | Target Score (0-4) | Gap | Related Risk ID (CGI-RSK-001) | Risk if Unaddressed | Priority (P1/P2/P3) | Recommended Action | Est. Effort (S/M/L) | Owner (Job Title) | ISO 27001:2022 Annex A Mapping |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| `[GAP-0XX]` | `[FUNCTION]` | `[XX.YY Category Name]` | `[Official CSF 2.0 Category outcome text]` | `[Full sentences. Cite a specific policy clause and the specific evidence that does or does not show it operating. No opinion without a citation.]` | `[Doc ID §clause; tracker ref; or an explicit statement that nothing is on file]` | `[0-4]` | `[0-4]` | `[=Target-Current]` | `[R-0XX]` | `[Business consequence, not technical. Tie back to a named risk where one exists.]` | `[P1/P2/P3]` | `[Specific, owned, verifiable]` | `[S/M/L]` | `[Job title, never a person]` | `[A.x.y Control name; A.x.y Control name]` |
| `[GAP-0XX]` | `[FUNCTION]` | `[XX.YY Category Name]` | `[Official CSF 2.0 Category outcome text]` | `[Full sentences. Cite a specific policy clause and the specific evidence that does or does not show it operating. No opinion without a citation.]` | `[Doc ID §clause; tracker ref; or an explicit statement that nothing is on file]` | `[0-4]` | `[0-4]` | `[=Target-Current]` | `[R-0XX]` | `[Business consequence, not technical. Tie back to a named risk where one exists.]` | `[P1/P2/P3]` | `[Specific, owned, verifiable]` | `[S/M/L]` | `[Job title, never a person]` | `[A.x.y Control name; A.x.y Control name]` |
| `[GAP-0XX]` | `[FUNCTION]` | `[XX.YY Category Name]` | `[Official CSF 2.0 Category outcome text]` | `[Full sentences. Cite a specific policy clause and the specific evidence that does or does not show it operating. No opinion without a citation.]` | `[Doc ID §clause; tracker ref; or an explicit statement that nothing is on file]` | `[0-4]` | `[0-4]` | `[=Target-Current]` | `[R-0XX]` | `[Business consequence, not technical. Tie back to a named risk where one exists.]` | `[P1/P2/P3]` | `[Specific, owned, verifiable]` | `[S/M/L]` | `[Job title, never a person]` | `[A.x.y Control name; A.x.y Control name]` |

**Repeat for all 22 Categories in this order:**

| Function | Categories to assess |
|---|---|
| GOVERN (6) | GV.OC Organizational Context · GV.RM Risk Management Strategy · GV.RR Roles, Responsibilities and Authorities · GV.PO Policy · GV.OV Oversight · GV.SC Cybersecurity Supply Chain Risk Management |
| IDENTIFY (3) | ID.AM Asset Management · ID.RA Risk Assessment · ID.IM Improvement |
| PROTECT (5) | PR.AA Identity Management, Authentication and Access Control · PR.AT Awareness and Training · PR.DS Data Security · PR.PS Platform Security · PR.IR Technology Infrastructure Resilience |
| DETECT (2) | DE.CM Continuous Monitoring · DE.AE Adverse Event Analysis |
| RESPOND (4) | RS.MA Incident Management · RS.AN Incident Analysis · RS.CO Incident Response Reporting and Communication · RS.MI Incident Mitigation |
| RECOVER (2) | RC.RP Incident Recovery Plan Execution · RC.CO Incident Recovery Communication |

---

## 5. Function-level heatmap

| Function | Categories | Avg Current | Target | Gap |
|---|:-:|:-:|:-:|:-:|
| GOVERN | 6 | `[X.XX]` | `[X.XX]` | `[X.XX]` |
| IDENTIFY | 3 | `[X.XX]` | `[X.XX]` | `[X.XX]` |
| PROTECT | 5 | `[X.XX]` | `[X.XX]` | `[X.XX]` |
| DETECT | 2 | `[X.XX]` | `[X.XX]` | `[X.XX]` |
| RESPOND | 4 | `[X.XX]` | `[X.XX]` | `[X.XX]` |
| RECOVER | 2 | `[X.XX]` | `[X.XX]` | `[X.XX]` |
| **OVERALL** | **22** | `[X.XX]` | `[X.XX]` | `[X.XX]` |

> Compute OVERALL as the mean of all 22 Category scores, **not** as the mean of the six Function averages.
> Exclude the OVERALL row from the radar chart.

---

## 6. Prioritised remediation roadmap

| Rec ID | Recommendation | Closes (Risk ID / Control Gap) | Related CSF Category | Priority | Effort | Risk Reduction (1-5) | RR/Effort | Owner (Job Title) | Target Quarter | Dependency | Business Rationale |
|---|---|---|---|:-:|:-:|:-:|:-:|---|---|---|---|
| `[REC-01]` | `[Specific action]` | `[R-0XX / CG-0X]` | `[XX.YY]` | `[P1/P2/P3]` | `[S/M/L]` | `[1-5]` | `[=RR/effort units]` | `[Job title]` | `[QX YYYY]` | `[REC-XX or None]` | `[Why the business should fund this]` |
| `[REC-02]` | `[Specific action]` | `[R-0XX / CG-0X]` | `[XX.YY]` | `[P1/P2/P3]` | `[S/M/L]` | `[1-5]` | `[=RR/effort units]` | `[Job title]` | `[QX YYYY]` | `[REC-XX or None]` | `[Why the business should fund this]` |
| `[REC-03]` | `[Specific action]` | `[R-0XX / CG-0X]` | `[XX.YY]` | `[P1/P2/P3]` | `[S/M/L]` | `[1-5]` | `[=RR/effort units]` | `[Job title]` | `[QX YYYY]` | `[REC-XX or None]` | `[Why the business should fund this]` |

**Sort by RR ÷ effort units (S=1, M=2, L=3), then override for dependencies and state every override.**
Minimum 12 recommendations. Every one needs an owner, a quarter and a dependency — an unowned, undated
recommendation is a wish.

| Wave | Window | Recommendations | What it buys |
|---|---|---|---|
| Wave 1 | `[Q, 0-90 days]` | `[REC-xx to REC-xx]` | `[Usually: convert existing written controls into evidenced ones. No budget.]` |
| Wave 2 | `[Q]` | `[REC-xx to REC-xx]` | `[Usually: the first real controls that never existed.]` |
| Wave 3 | `[Q]` | `[REC-xx to REC-xx]` | `[Hardening and rehearsal.]` |
| Wave 4 | `[Q]` | `[REC-xx to REC-xx]` | `[Assurance. Budget-dependent.]` |

---

## 7. Executive summary (one page)

> **To:** `[CEO name, title]` · **From:** `[Assessor]` · **Date:** `[Date]`
> **Subject:** NIST CSF 2.0 security maturity — where we stand and what to do first

### Overall maturity: `[X.XX]` out of 4.00

`[One sentence: what was measured, on what scale, against what target, and what the gap is.]`

### The three findings that matter

**1. `[Finding headline]`.** `[Two or three sentences. Cite the evidence figure.]`

**2. `[Finding headline]`.** `[Two or three sentences. Tie to a named risk that stayed High.]`

**3. `[Finding headline]`.** `[Two or three sentences.]`

### Business impact

> `[One paragraph a CEO would repeat to a board. Must name a commercial consequence — deals blocked,
> revenue gated, certification out of reach, contractual commitment unmet — not a technical one.]`

### What I am asking for

| | Ask | Cost |
|---|---|---|
| **Now (0-90 days)** | `[Wave 1 recommendations]` | `[Usually: staff time only]` |
| **`[Next quarter]`** | `[Wave 2 recommendations]` | `[Figure, referenced to the risk register estimate]` |
| **Standing** | `[Governance cadence]` | `[Time per quarter]` |

**`[If Waves 1 and 2 complete, overall maturity moves from X.XX to approximately Y.YY out of 4.00.]`**

---

## 8. Internal consistency checks

> **The governing rule: no Category may be scored 3 or above while a residual High risk sits behind it,
> unless the reason is stated in writing.**

| Category | Score | Linked to residual High? | Explanation |
|---|:-:|---|---|
| `[XX.YY]` | `[n]` | `[Yes — R-0XX]` | `[Why it is not a contradiction — usually because the risk's driving control lives in a different Category]` |

**Inverse check — the one that would be a real contradiction:**

| Residual High risk | Driving control gap | Owning Category | Score | Consistent? |
|---|---|---|:-:|---|
| `[R-0XX]` | `[CG-0X]` | `[XX.YY]` | `[n]` | `[✅/❌]` |

**Verification checklist:**

- [ ] All 22 Categories assessed, no duplicates, all 6 Functions covered (6+3+5+2+4+2 = 22)
- [ ] Every Current and Target score is 0–4; no Target below Current
- [ ] Gap = Target − Current, computed not typed
- [ ] Function and overall averages recomputed programmatically
- [ ] Target distribution reconciles to the target sum
- [ ] No Category ≥ 3 behind a residual High risk without a written explanation
- [ ] Every Category cites a policy clause or names the absence of one
- [ ] Every Category carries a secondary framework mapping
- [ ] Every Owner is a job title, never a named individual
- [ ] At least 12 recommendations, each with priority, effort, owner, quarter and dependency
- [ ] Tables contain one value per cell and no merged cells
- [ ] Fictional-data notice present if this is a portfolio scenario

---

*Reusable template derived from CGI-GAP-001 v1.0. Replace all bracketed values.*
