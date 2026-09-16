[← Portfolio home](../README.md) · [All templates](README.md)

# [COMPANY LEGAL NAME] — Master Information Security Risk Register

> [!TIP]
> **How to use this template.** Replace every [BRACKETED] field. Delete any section that does not apply. Delete this note before issuing. Originally developed for a fictional portfolio scenario by O.S, 2026. Method: NIST SP 800-30 Rev. 1 semi-quantitative 5 x 5.

### Assessed under [METHODOLOGY, e.g. NIST SP 800-30 Rev. 1], with control cross-references to [YOUR POLICY SET ID RANGE, e.g. XXX-POL-001 to XXX-POL-005]

---

## Metadata block

| Field | Value |
|---|---|
| Document ID | [DOC ID, e.g. XXX-RSK-001] |
| Document title | [TITLE] |
| Version | [VERSION, e.g. 1.0] |
| Classification | [CLASSIFICATION, e.g. Confidential] |
| Register owner (accountable) | [NAME], [JOB TITLE] |
| Prepared by (assessor) | [NAME], [JOB TITLE] |
| Approved by | [NAME], [JOB TITLE OF APPROVER] |
| Assessment method | [METHOD AND SCALE, e.g. NIST SP 800-30 Rev. 1, semi-quantitative 5 x 5] |
| Supporting standards referenced | [e.g. ISO/IEC 27005:2022, ISO 31000:2018, NIST CSF 2.0] |
| Assessment period | [DD – DD MONTH YYYY] |
| Assessment date | [DD MONTH YYYY] |
| Approval date | [DD MONTH YYYY] |
| Effective date | [DD MONTH YYYY] |
| Review cadence | [e.g. Quarterly for High and Critical; annually for the full register; on material change] |
| Next scheduled review | [DD MONTH YYYY] |
| Risks in scope of this version | [NUMBER] |
| Related documents | [LIST POLICY IDs, TRACKERS, PRIOR ASSESSMENTS] |
| Retention | [PERIOD AND POLICY REFERENCE] |

### Scope

**In scope.** [LIST THE ASSETS, SYSTEMS, DATA TYPES, LOCATIONS AND POPULATIONS ASSESSED.]

**Out of scope.** [STATE EXPLICITLY WHAT WAS NOT ASSESSED AND WHY. An unstated exclusion is a finding.]

**Time horizon.** All likelihood scores express probability within a rolling [NUMBER]-month period.

### Documented assumptions

| # | Assumption | Used for |
|---|---|---|
| A-01 | [e.g. Annual recurring revenue is approximately CURRENCY AMOUNT] | Calibrating the financial bands in the Impact scale |
| A-02 | [e.g. Headcount is NUMBER with annual attrition of NUMBER] | Frequency basis for [RISK ID] |
| A-03 | [e.g. Policy pack is approved but only NUMBER% acknowledged] | Control effectiveness discount applied to residual scores |
| A-04 | [ANY CONTROL DOMAIN THAT DOES NOT YET EXIST] | Explains residual scores that do not fall |
| A-05 | [INSURANCE POSITION] | Basis of any Transfer treatment |

---

## 1. Risk scoring legend

### 1.1 Likelihood scale (probability of occurrence within [NUMBER] months)

| Score | Label | Probability band | Frequency anchor | Evidence anchor |
|---|---|---|---|---|
| 1 | Rare | < [X]% | [e.g. no more than once in 20+ years] | [WHAT EVIDENCE JUSTIFIES A 1] |
| 2 | Unlikely | [X]% – [X]% | [FREQUENCY] | [EVIDENCE] |
| 3 | Possible | [X]% – [X]% | [FREQUENCY] | [EVIDENCE] |
| 4 | Likely | [X]% – [X]% | [FREQUENCY] | [EVIDENCE] |
| 5 | Almost Certain | > [X]% | [FREQUENCY] | [EVIDENCE] |

### 1.2 Impact scale

> Score the **highest** dimension reached. Do not average across columns.
> Calibrate the financial bands to this organisation's actual size — bands copied
> from an enterprise template will make every risk look trivial.

| Score | Label | Financial | Regulatory / Legal | Customer & Contractual | Operational | Reputational |
|---|---|---|---|---|---|---|
| 1 | Insignificant | < [AMOUNT] | [DESCRIPTION] | [DESCRIPTION] | < [TIME] disruption | [DESCRIPTION] |
| 2 | Minor | [RANGE] | [DESCRIPTION] | [DESCRIPTION] | [TIME RANGE] | [DESCRIPTION] |
| 3 | Moderate | [RANGE] | [DESCRIPTION] | [DESCRIPTION] | [TIME RANGE] | [DESCRIPTION] |
| 4 | Major | [RANGE] | [DESCRIPTION] | [DESCRIPTION] | [TIME RANGE] | [DESCRIPTION] |
| 5 | Severe | > [AMOUNT] | [DESCRIPTION] | [DESCRIPTION] | > [TIME] | [DESCRIPTION] |

### 1.3 Risk score calculation

> **Risk Score = Likelihood × Impact**, producing a value from 1 to 25.
> Calculated twice: **inherent** (controls assumed absent) and **residual** (existing, verified controls credited).

### 1.4 Qualitative risk thresholds

| Score range | Rating | Meaning | Acceptance authority | Mandatory review cadence |
|---|---|---|---|---|
| [RANGE] | **Low** | [MEANING] | [JOB TITLE] | [CADENCE] |
| [RANGE] | **Medium** | [MEANING] | [JOB TITLE] | [CADENCE] |
| [RANGE] | **High** | [MEANING] | [JOB TITLE] | [CADENCE] |
| [RANGE] | **Critical** | [MEANING] | [JOB TITLE] | [CADENCE] |

### 1.5 Risk treatment strategy definitions

| Strategy | Definition | When it is the right answer |
|---|---|---|
| **Mitigate** | Reduce likelihood, impact or both by implementing or strengthening controls. | [WHEN] |
| **Transfer** | Shift financial or operational consequence via insurance or contract. Reputational and regulatory liability cannot be transferred. | [WHEN] |
| **Avoid** | Stop, do not start, or redesign the activity creating the risk. | [WHEN] |
| **Accept** | Formally retain, by a named owner with authority, with justification, compensating controls and an expiry date. | [WHEN] |

---

## 2. THE RISK REGISTER

*One value per cell. No merged cells. Duplicate the row block for each additional risk.*

| Risk ID | Target Asset & Vulnerability | Threat Description | Inherent Likelihood (1-5) | Inherent Impact (1-5) | Total Inherent Risk Score (Likelihood x Impact) | Mitigating Controls (Cross-referenced to Project 1 policies) | Residual Likelihood (1-5) | Residual Impact (1-5) | Total Residual Risk Score (Likelihood x Impact) | Risk Treatment Strategy (Mitigate, Accept, Transfer, Avoid) | Action Owner (Job Title) |
|---|---|---|---|---|---|---|---|---|---|---|---|
| [R-001] | [NAME THE ASSET AND ITS CLASSIFICATION TIER]. Vulnerability: [THE SPECIFIC WEAKNESS THAT MAKES THIS ASSET EXPLOITABLE — not the threat, the weakness]. | [THREAT SOURCE] exploits [VULNERABILITY] affecting [ASSET], resulting in [IMMEDIATE TECHNICAL CONSEQUENCE], leading to [BUSINESS, REGULATORY AND CUSTOMER IMPACT]. | [1-5] | [1-5] | [PRODUCT] | [POLICY ID] §[SECTION] [what the clause requires]; [POLICY ID] §[SECTION] [what the clause requires]; [REPEAT — cite the clause, never just the policy name]. | [1-5] | [1-5] | [PRODUCT] | [ONE OF: Mitigate / Transfer / Avoid / Accept] | [JOB TITLE, never a personal name] |
| [R-002] | [ASSET AND VULNERABILITY] | [THREAT DESCRIPTION] | [1-5] | [1-5] | [PRODUCT] | [POLICY CROSS-REFERENCES] | [1-5] | [1-5] | [PRODUCT] | [STRATEGY] | [JOB TITLE] |
| [R-003] | [ASSET AND VULNERABILITY] | [THREAT DESCRIPTION] | [1-5] | [1-5] | [PRODUCT] | [POLICY CROSS-REFERENCES] | [1-5] | [1-5] | [PRODUCT] | [STRATEGY] | [JOB TITLE] |
| [R-004] | [ASSET AND VULNERABILITY] | [THREAT DESCRIPTION] | [1-5] | [1-5] | [PRODUCT] | [POLICY CROSS-REFERENCES] | [1-5] | [1-5] | [PRODUCT] | [STRATEGY] | [JOB TITLE] |
| [R-005] | [ASSET AND VULNERABILITY] | [THREAT DESCRIPTION] | [1-5] | [1-5] | [PRODUCT] | [POLICY CROSS-REFERENCES] | [1-5] | [1-5] | [PRODUCT] | [STRATEGY] | [JOB TITLE] |

---

## 3. Residual scoring rationale and control effectiveness

| Risk ID | Inherent | Rating | Residual | Rating | Score reduction | Risk owner (accountable business role) | Justification for the residual score |
|---|---|---|---|---|---|---|---|
| [R-001] | [SCORE] | [BAND] | [SCORE] | [BAND] | [DIFFERENCE] | [JOB TITLE — must be a business leader, never the security analyst] | **Likelihood [X] → [Y].** [WHICH CONTROL CAUSED THE DROP, AND WHY IT CANNOT DROP FURTHER.] **Impact [X] → [Y].** [SAME REASONING FOR IMPACT.] |
| [R-002] | [SCORE] | [BAND] | [SCORE] | [BAND] | [DIFFERENCE] | [JOB TITLE] | [JUSTIFICATION] |

### Control effectiveness caveat

[STATE ANY REASON RESIDUAL SCORES ARE CREDITED AT PARTIAL STRENGTH — for example acknowledgement rate, training completion, controls not yet technically enforced, or controls not yet tested. If there is no reason, say so explicitly and state what evidence supports full crediting.]

---

## 4. Risk treatment plan

| Treatment ID | Risk ID | Strategy | Action | Control type | Existing policy anchor | Estimated cost | Action owner (job title) | Target completion | Target residual score |
|---|---|---|---|---|---|---|---|---|---|
| [TP-01] | [R-00X] | [STRATEGY] | [SPECIFIC, DATED, TESTABLE ACTION] | [Preventive / Detective / Corrective] | [POLICY ID §SECTION, or "New policy — gap CG-0X"] | [AMOUNT] | [JOB TITLE] | [DD MONTH YYYY] | [SCORE] |

### 4.1 Formally accepted risk

| Acceptance ID | Related risk | What is accepted | Justification | Compensating control | Accepting authority | Approval date | Expiry date | Review |
|---|---|---|---|---|---|---|---|---|
| [ACC-001] | [R-00X] | [WHAT IS BEING RETAINED] | [BUSINESS JUSTIFICATION] | [WHAT REDUCES IT IN THE MEANTIME] | [NAME, JOB TITLE — must hold authority for that band] | [DATE] | [DATE, never blank] | [TRIGGER] |

### 4.2 Risk avoided by design

| Avoidance ID | Risk avoided | Decision | Policy anchor |
|---|---|---|---|
| [AVD-001] | [THE RISK THAT DOES NOT EXIST BECAUSE THE ACTIVITY IS NOT PERFORMED] | [THE DECISION] | [POLICY ID §SECTION] |

### 4.3 Control gap register

| Gap ID | Gap | Risks affected | Consequence for scoring | Closure action |
|---|---|---|---|---|
| [CG-01] | [WHAT THE POLICY SET DOES NOT COVER] | [RISK IDs] | [WHICH RESIDUAL SCORE IS CAPPED AND AT WHAT VALUE] | [TP ID] |

---

## 5. Key risk indicators

| KRI ID | Indicator | Related risk | Source | Threshold (green / amber / red) | Reporting cadence | Owner |
|---|---|---|---|---|---|---|
| [KRI-01] | [A MEASURABLE NUMBER THAT MOVES BEFORE AN INCIDENT DOES] | [RISK IDs] | [SYSTEM OR POLICY CLAUSE THAT PRODUCES IT] | [THRESHOLDS] | [CADENCE] | [JOB TITLE] |

---

## 6. Register summary

| Metric | Value |
|---|---|
| Risks assessed | [NUMBER] |
| Inherent: Critical / High / Medium / Low | [COUNTS] |
| Aggregate inherent score | [SUM] of a possible [NUMBER x 25] |
| Residual: Critical / High / Medium / Low | [COUNTS] |
| Aggregate residual score | [SUM] |
| Total risk reduction attributable to existing controls | [DIFFERENCE] points, a [PERCENTAGE]% reduction |
| Risks remaining above appetite | [NUMBER] |
| Treatment actions raised | [NUMBER] |
| Estimated treatment cost, year one | [AMOUNT] |
| Control gaps identified | [NUMBER] |

**The single headline for leadership.** *[ONE SENTENCE A CHIEF EXECUTIVE COULD REPEAT IN A BOARD MEETING WITHOUT NOTES.]*

---

## 7. Methodology, limitations and honest caveats

**Method.** [RESTATE THE METHOD, THE SCALES AND THE RULE FOR CREDITING CONTROLS.]

**Limitations.**

1. **Range compression.** [EXPLAIN THAT EQUAL PRODUCTS CAN DESCRIBE DIFFERENT RISKS.]
2. **Ordinal arithmetic.** [EXPLAIN THAT ORDINAL SCALES RANK RATHER THAN MEASURE.]
3. **Estimate provenance.** [STATE WHERE LIKELIHOOD ESTIMATES CAME FROM AND WHAT WOULD IMPROVE THEM.]
4. **Control effectiveness is asserted, not tested.** [STATE WHETHER ANY TESTING HAS BEEN PERFORMED.]
5. **Scope.** [RESTATE WHAT IS NOT COVERED.]

**Assurance statement.** [IF THIS IS A PORTFOLIO ARTEFACT: state that all content is fictional and that no certification or attestation is claimed. IF REAL: state the review and approval status.]

---

## 8. Approval

| Role | Name | Action | Date |
|---|---|---|---|
| Prepared by | [NAME], [TITLE] | Assessment performed and register drafted | [DATE] |
| Reviewed by | [NAME], [TITLE] | Register owner; reviewed scoring and control mapping | [DATE] |
| Approved by | [NAME], [TITLE] | [WHAT WAS APPROVED OR ACCEPTED] | [DATE] |

*Signature: ______________________  Date: ______________*

---

## Fill-in checklist before you issue this

- [ ] Every `[BRACKETED]` field replaced or the row deleted
- [ ] Impact financial bands calibrated to **this** organisation's revenue, not copied
- [ ] Every likelihood and impact score has a written justification in section 3
- [ ] Every mitigating control cites a **specific clause number**, never just a policy name
- [ ] Residual score is lower than inherent **only** where a real, operating control justifies it
- [ ] Any residual score that did **not** fall is explained, with the gap recorded in 4.3
- [ ] Every risk owner is a **business leader**; no risk is owned by the security analyst
- [ ] Every action owner is a **job title**, not a personal name
- [ ] At least one risk demonstrates each of Mitigate, Transfer, Avoid and Accept across sections 2, 4.1 and 4.2
- [ ] Every acceptance has a named authority with the right approval level, and an expiry date
- [ ] Arithmetic verified: every score column equals Likelihood × Impact
- [ ] Table pastes into a spreadsheet with one value per cell and no merged cells
- [ ] Limitations section written honestly, including what the model cannot do
- [ ] Fictional-data notice present if this is a portfolio artefact
- [ ] Added to the document register with owner, approver and review dates
