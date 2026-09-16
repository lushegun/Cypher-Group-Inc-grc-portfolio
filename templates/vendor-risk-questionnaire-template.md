[← Portfolio home](../README.md) · [All templates](README.md)

# [ORGANISATION] — Vendor Security Questionnaire

| Field | Value |
|---|---|
| Document ID | [DOC-ID] |
| Version | [1.0] |
| Issued to | [VENDOR] |
| Return by | [DD Month YYYY] |
| Tier applied | [1 / 2 / 3] |
| Assessor | [Name or initials] |

> [!TIP]
> **How to use this template.** Everything in `[SQUARE BRACKETS]` is a field to replace.
> Everything outside them is method and should be changed only deliberately. Guidance sits in
> `>` blockquotes and is deleted before the document is issued. Derived from CGI-TPR-001 v1.0.

## How this questionnaire is scored

- **Weighted deduction** = the **full risk weight** for every *Not Met*, plus **half the weight** for
  every *Partial*. **Not Applicable** questions are removed from the maximum.
- **Score** = 1 − (deduction ÷ maximum).

| Weighted score | Verdict | Action |
|---|---|---|
| **≥ [90]%** with no weight-5 *Not Met* | **Pass** | Onboard or continue; diary the next review |
| **[75]–[89]%**, or ≥ [90]% with one weight-5 *Not Met* | **Pass with conditions** | Written, dated, owned conditions and a re-check date |
| **< [75]%**, or **[two] or more weight-5 *Not Met*** | **Fail** | Remediate within [90] days or exit |
| Lowest tier, low exposure | **Accept with justification** | Written justification, named owner, expiry date |

> **Keep the veto.** Without the "two weight-5 failures = automatic fail" override, a vendor can fail the
> contract question and the breach-notification question and still pass on volume of easy answers.

## Tier subsets

- **Tier 1:** all [74] questions.
- **Tier 2 (Lite):** the **[24] questions carrying risk weight 5** — marked **T2**. Mechanical, so the
  rule can be published and audited.
- **Tier 3 (Attestation):** [6] fixed questions — marked **T3**.

## The questions

Legend: **Wt** = risk weight 1–5 · **T2** = Tier 2 Lite set · **T3** = Tier 3 attestation set

### 1. Governance and Security Programme

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-01 | Do you maintain a documented information security programme formally approved by executive management? | Yes/No + document | Approved security policy set with an approval record | **4** | A.5.1, A.5.4 | GV.PO |  |  | [  ] | [  ] |
| VQ-02 | Is a named individual accountable for information security (CISO or equivalent)? State the role title. | Yes/No + free text | Organisation chart or role description | **3** | A.5.2 | GV.RR |  |  | [  ] | [  ] |
| VQ-03 | How many staff are dedicated to information security on a full-time basis? | Numeric | Written headcount statement | **2** | A.5.2 | GV.RR |  |  | [  ] | [  ] |
| VQ-04 | Are security policies reviewed at least annually? State the date of the last review. | Yes/No + date | Dated review or approval record | **3** | A.5.1, A.5.36 | GV.PO |  |  | [  ] | [  ] |
| VQ-05 | Do you report security performance metrics to executive management at least quarterly? | Yes/No | Redacted sample management report | **2** | A.5.35 | GV.OV |  |  | [  ] | [  ] |

### 2. Risk Management

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-06 | Do you operate a documented information security risk assessment methodology? | Yes/No + document | Methodology document naming the scoring method | **4** | A.5.1 | ID.RA |  |  | [  ] | [  ] |
| VQ-07 | When was your last enterprise information security risk assessment completed? | Date | Assessment summary or management report | **3** | A.5.1 | ID.RA |  |  | [  ] | [  ] |
| VQ-08 | Is there a documented risk acceptance process with a defined approval authority? | Yes/No | Sample risk acceptance record | **3** | A.5.4 | GV.RM |  |  | [  ] | [  ] |
| VQ-09 | Does your risk register include risks arising from your own suppliers? | Yes/No | Redacted register extract | **3** | A.5.21 | GV.SC |  |  | [  ] | [  ] |

### 3. Policies, Compliance and Certifications

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-10 | Do you hold a current ISO/IEC 27001 certificate issued by an accredited certification body? | Yes/No/NA + upload | Certificate showing certification body and accreditation mark | **5** | A.5.1, A.5.31 | GV.OC | • |  | [  ] | [  ] |
| VQ-11 | State the exact scope of that certificate, transcribed as written on the certificate itself. | Free text | Certificate scope statement | **5** | A.5.1, A.5.31 | GV.OC | • |  | [  ] | [  ] |
| VQ-12 | Do you provide a SOC 2 Type II report, and what period does it cover? | Yes/No + date range + upload | Complete report including Section 4 test results | **5** | A.5.1, A.5.31 | GV.OC | • | • | [  ] | [  ] |
| VQ-13 | Does that report use the CARVE-OUT or the INCLUSIVE method for sub-service organisations? Name every carved-out sub-service organisation. | Multiple choice + free text | Report Section 3 system description | **5** | A.5.21, A.5.23 | GV.SC | • |  | [  ] | [  ] |
| VQ-14 | List every exception, qualification or deviation in your most recent report, and its remediation status. | Free text | Report Section 4 plus written remediation plan | **5** | A.5.36 | GV.OV | • |  | [  ] | [  ] |

### 4. Identity and Access Management

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-15 | Is multi-factor authentication enforced for all personnel with access to customer data? | Yes/No | Policy plus configuration evidence | **5** | A.8.5, A.5.17 | PR.AA | • |  | [  ] | [  ] |
| VQ-16 | Is phishing-resistant MFA enforced for privileged and administrative accounts? | Yes/No | Configuration evidence | **4** | A.8.2, A.8.5 | PR.AA |  |  | [  ] | [  ] |
| VQ-17 | Is access granted on a documented least-privilege, role-based model? | Yes/No + document | Role-based access control model | **4** | A.5.15, A.5.18 | PR.AA |  |  | [  ] | [  ] |
| VQ-18 | How frequently are user access rights reviewed? State the date of the last completed review. | Multiple choice + date | Signed and dated access review record | **4** | A.5.18 | PR.AA |  |  | [  ] | [  ] |
| VQ-19 | What is your service-level commitment for revoking access on employee termination? | Numeric (hours) | Procedure plus a sample completed revocation record | **4** | A.5.18, A.6.5 | PR.AA |  |  | [  ] | [  ] |
| VQ-20 | Do you support SSO (SAML or OIDC) and automated provisioning and deprovisioning (SCIM) for customer administrators? | Yes/No | Product documentation | **4** | A.5.16 | PR.AA |  |  | [  ] | [  ] |

### 5. Data Protection and Encryption

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-21 | Is customer data encrypted at rest? State the algorithm and key length. | Yes/No + free text | Encryption standard | **5** | A.8.24 | PR.DS | • |  | [  ] | [  ] |
| VQ-22 | Is customer data encrypted in transit? State the minimum TLS version enforced. | Yes/No + free text | TLS configuration evidence | **5** | A.8.24 | PR.DS | • |  | [  ] | [  ] |
| VQ-23 | How are encryption keys generated, stored and rotated? Is a customer-managed key option available? | Free text | Key management procedure | **3** | A.8.24 | PR.DS |  |  | [  ] | [  ] |
| VQ-24 | Is customer data logically or physically segregated between tenants? Describe the mechanism. | Yes/No + free text | Architecture or multi-tenancy description | **5** | A.8.22, A.8.31 | PR.DS | • |  | [  ] | [  ] |
| VQ-25 | Do you operate documented data retention and secure deletion schedules? | Yes/No + document | Retention schedule | **4** | A.8.10 | PR.DS |  |  | [  ] | [  ] |
| VQ-26 | Do you deploy data loss prevention or egress monitoring on systems holding customer data? | Yes/No | DLP configuration summary | **3** | A.8.12 | PR.DS |  |  | [  ] | [  ] |

### 6. Data Privacy and GDPR

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-27 | Will you execute our Data Processing Agreement, or provide one satisfying GDPR Article 28(3)? | Yes/No | Executed DPA | **5** | A.5.34, A.5.20 | GV.OC | • | • | [  ] | [  ] |
| VQ-28 | In which countries will our data be stored, processed and accessed from, including support access? | Free text | Data residency statement | **5** | A.5.34 | GV.OC | • | • | [  ] | [  ] |
| VQ-29 | Where data leaves the EEA, which GDPR Article 46 transfer mechanism applies? | Multiple choice + free text | Standard Contractual Clauses or adequacy reference, plus transfer impact assessment | **5** | A.5.34 | GV.OC | • |  | [  ] | [  ] |
| VQ-30 | Have you appointed a Data Protection Officer or equivalent? Give the contact route. | Yes/No + free text | Appointment record | **2** | A.5.34 | GV.RR |  |  | [  ] | [  ] |
| VQ-31 | Can you support data subject access, rectification and erasure requests, and within what period? | Yes/No + numeric (days) | Data subject request procedure | **4** | A.5.34 | GV.OC |  |  | [  ] | [  ] |
| VQ-32 | Do you maintain records of processing activities under GDPR Article 30? | Yes/No | Records of processing extract | **3** | A.5.34 | GV.OC |  |  | [  ] | [  ] |

### 7. Sub-processors and Fourth Parties

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-33 | Provide your complete current sub-processor list, with the service each performs and its location. | Free text + upload | Published or contractual sub-processor register | **5** | A.5.19, A.5.21 | GV.SC | • |  | [  ] | [  ] |
| VQ-34 | How much prior notice is given of a new or changed sub-processor, and do we have a right to object? | Numeric (days) + Yes/No | Contract clause | **5** | A.5.22 | GV.SC | • |  | [  ] | [  ] |
| VQ-35 | Do you security-assess your own sub-processors before engagement? To what standard? | Yes/No + free text | Supplier assessment procedure | **4** | A.5.19, A.5.21 | GV.SC |  |  | [  ] | [  ] |
| VQ-36 | Do you flow down equivalent security and privacy obligations to your sub-processors? | Yes/No | Template sub-processor agreement | **4** | A.5.20 | GV.SC |  |  | [  ] | [  ] |

### 8. Secure Development and Change Management

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-37 | Do you follow a documented secure development lifecycle? | Yes/No + document | SDLC procedure | **4** | A.8.25 | PR.PS |  |  | [  ] | [  ] |
| VQ-38 | Is peer code review mandatory before any merge to a production branch? | Yes/No | Branch protection configuration evidence | **4** | A.8.28, A.8.32 | PR.PS |  |  | [  ] | [  ] |
| VQ-39 | Are development, test and production environments separated? Is production data ever used in lower environments? | Yes/No + free text | Environment separation policy | **4** | A.8.31 | PR.PS |  |  | [  ] | [  ] |
| VQ-40 | Do you perform static and dynamic application security testing within the pipeline? | Yes/No + free text | Scan configuration and redacted sample output | **4** | A.8.29 | PR.PS |  |  | [  ] | [  ] |
| VQ-41 | Do you maintain a software bill of materials and monitor third-party components for known vulnerabilities? | Yes/No | SBOM sample or software composition analysis report | **3** | A.8.8 | PR.PS |  |  | [  ] | [  ] |

### 9. Vulnerability and Patch Management

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-42 | Do you perform authenticated vulnerability scanning, and at what frequency? | Yes/No + multiple choice | Scan schedule and redacted sample report | **4** | A.8.8 | ID.RA |  |  | [  ] | [  ] |
| VQ-43 | State your remediation service levels by severity for Critical, High, Medium and Low findings. | Free text | Vulnerability management policy | **4** | A.8.8 | PR.PS |  |  | [  ] | [  ] |
| VQ-44 | Is an independent penetration test performed at least annually? Will you share the executive summary? | Yes/No + date | Executive summary of the most recent test | **4** | A.8.29 | ID.RA |  |  | [  ] | [  ] |
| VQ-45 | Do you operate a coordinated vulnerability disclosure or bug bounty programme? | Yes/No + free text | Published disclosure policy | **2** | A.5.7 | ID.RA |  |  | [  ] | [  ] |

### 10. Logging, Monitoring and Detection

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-46 | Are security-relevant events logged centrally? For how many months are logs retained? | Yes/No + numeric (months) | Logging standard | **4** | A.8.15 | DE.CM |  |  | [  ] | [  ] |
| VQ-47 | Is there 24x7 monitoring and alerting on security events? In-house or outsourced? | Yes/No + free text | Monitoring or SOC description | **3** | A.8.16 | DE.CM |  |  | [  ] | [  ] |
| VQ-48 | Can you provide customer-accessible audit logs of administrative activity within our tenant? | Yes/No | Product documentation | **4** | A.8.15 | DE.CM |  |  | [  ] | [  ] |
| VQ-49 | Do you alert on anomalous access to customer data, such as bulk export or mass download? | Yes/No + free text | Alerting rule description | **3** | A.8.16, A.8.12 | DE.CM |  |  | [  ] | [  ] |

### 11. Incident Response and Breach Notification

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-50 | Do you maintain a documented incident response plan? When was it last exercised? | Yes/No + date | Incident response plan plus dated exercise record | **5** | A.5.24, A.5.26 | RS.MA | • |  | [  ] | [  ] |
| VQ-51 | Within how many hours will you notify us of a security incident affecting our data? | Numeric (hours) | Contractual notification clause | **5** | A.5.26, A.6.8 | RS.CO | • | • | [  ] | [  ] |
| VQ-52 | Who is the named security incident contact, and what is the out-of-hours escalation route? | Free text | Contact record with 24x7 route | **4** | A.5.5 | RS.CO |  |  | [  ] | [  ] |
| VQ-53 | Have you experienced a reportable security breach in the last 24 months? Describe it and the remediation. | Yes/No + free text | Breach summary and remediation evidence | **5** | A.5.27 | RS.AN | • |  | [  ] | [  ] |
| VQ-54 | Do you support customer forensic requests and preserve evidence to a defined standard? | Yes/No | Evidence handling and chain-of-custody procedure | **3** | A.5.28 | RS.AN |  |  | [  ] | [  ] |

### 12. Business Continuity, Backup and Resilience

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-55 | State your contractual availability commitment and your achieved availability over the last 12 months. | Free text | Service level agreement plus uptime report | **4** | A.5.30 | PR.IR |  |  | [  ] | [  ] |
| VQ-56 | State the documented Recovery Time Objective and Recovery Point Objective for the service we consume. | Free text | Business continuity or disaster recovery plan | **5** | A.5.29, A.5.30 | RC.RP | • |  | [  ] | [  ] |
| VQ-57 | When was the disaster recovery plan last tested, and what was the documented result? | Date + free text | Disaster recovery test report | **5** | A.5.30 | RC.RP | • |  | [  ] | [  ] |
| VQ-58 | Are backups encrypted, and are restores tested at a defined frequency? | Yes/No + multiple choice | Backup policy and a dated restore test record | **4** | A.8.13 | RC.RP |  |  | [  ] | [  ] |
| VQ-59 | Can we export our complete dataset in a documented, machine-readable format on demand? | Yes/No + free text | Export documentation | **4** | A.5.29 | RC.RP |  |  | [  ] | [  ] |

### 13. Personnel Security and Awareness

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-60 | Are background checks performed on personnel with access to customer data, where lawful? | Yes/No + free text | Screening policy | **3** | A.6.1 | PR.AT |  |  | [  ] | [  ] |
| VQ-61 | Do all personnel and contractors sign confidentiality agreements? | Yes/No | Template confidentiality clause | **3** | A.6.6 | PR.AT |  |  | [  ] | [  ] |
| VQ-62 | Is security awareness training mandatory at induction and at least annually? State current completion rate. | Yes/No + numeric (%) | Training completion report | **3** | A.6.3 | PR.AT |  |  | [  ] | [  ] |
| VQ-63 | Do you run phishing simulations? State the click rate recorded in the most recent exercise. | Yes/No + free text | Simulation results | **2** | A.6.3 | PR.AT |  |  | [  ] | [  ] |

### 14. Physical and Environmental Security

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-64 | Where is customer data physically hosted, and is it in your own facilities or a sub-service provider's? | Free text | Facility description or provider attestation | **3** | A.7.1 | PR.IR |  |  | [  ] | [  ] |
| VQ-65 | Is physical access to hosting facilities controlled, logged and periodically reviewed? | Yes/No | Facility attestation or sub-service provider report | **3** | A.7.2, A.7.4 | PR.IR |  |  | [  ] | [  ] |
| VQ-66 | Are storage media securely destroyed at end of life to a recognised standard? | Yes/No + free text | Sample certificate of destruction | **2** | A.7.10, A.7.14 | PR.DS |  |  | [  ] | [  ] |

### 15. AI and Automated Processing

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-67 | Does the service process our data using AI or machine learning, including for features we have not explicitly enabled? | Yes/No + free text | Product and data-flow documentation | **5** | A.5.34, A.8.25 | GV.SC | • |  | [  ] | [  ] |
| VQ-68 | Is our data used to train, fine-tune or evaluate any model, whether yours or a third party's? | Yes/No | Contractual prohibition or signed written confirmation | **5** | A.5.20, A.5.34 | GV.SC | • | • | [  ] | [  ] |
| VQ-69 | Is our data exposed to human review by your staff or contractors for quality, safety or model improvement? | Yes/No + free text | Human review policy and the access controls around it | **5** | A.5.34, A.5.20 | GV.SC | • |  | [  ] | [  ] |
| VQ-70 | Name every AI sub-processor or model provider in the data path, and the retention period at each. | Free text | Sub-processor register entry covering AI providers | **5** | A.5.21 | GV.SC | • |  | [  ] | [  ] |

### 16. Contract, Exit and Termination

| ID | Question | Response Type | Evidence Required | Wt | ISO 27001:2022 Annex A | CSF 2.0 | T2 | T3 | Vendor Response | Verdict |
|---|---|---|---|:-:|---|---|:-:|:-:|---|---|
| VQ-71 | Will you accept a contractual right of audit, or an annual assurance review in place of one? | Yes/No + free text | Contract clause | **3** | A.5.20, A.5.22 | GV.SC |  |  | [  ] | [  ] |
| VQ-72 | Do you carry cyber liability insurance? State the limit of indemnity. | Yes/No + free text | Certificate of insurance | **3** | A.5.20 | GV.SC |  |  | [  ] | [  ] |
| VQ-73 | On termination, within how many days is our data deleted, and will you certify the deletion in writing? | Numeric (days) + Yes/No | Template certificate of deletion | **5** | A.8.10, A.5.20 | GV.SC | • | • | [  ] | [  ] |
| VQ-74 | Do you provide transition assistance on exit, and is the scope contractually defined? | Yes/No + free text | Contract clause | **3** | A.5.20 | GV.SC |  |  | [  ] | [  ] |

## Adapting the question set

| If the scenario is… | Change |
|---|---|
| **US healthcare (HIPAA)** | Domain 6 rewrites around the **BAA** (45 CFR §164.502(e), §164.308(b)) and **PHI**. Add: minimum necessary §164.502(b) · workforce sanctions §164.308(a)(1)(ii)(C) · unique user ID and automatic logoff §164.312(a) · audit controls §164.312(b) · integrity and transmission security §164.312(c),(e). Add a third mapping column for the HIPAA Security Rule; **NIST SP 800-66 Rev. 2** carries the CSF column across |
| **EU financial (DORA)** | Add an escalation trigger for critical-or-important functions; add Article 30 mandatory contractual provisions to the clause checklist |
| **Cardholder data (PCI DSS)** | Add a domain for Requirement 12.8 service provider due diligence and for the vendor's own AoC and responsibility matrix |
| **No EU nexus** | Replace Domain 6 entirely with the applicable privacy regime |

> **Domain 15 (AI and Automated Processing) gets more important in regulated sectors, not less.** Model
> training on regulated data is usually an impermissible disclosure, not merely a contract gap.

