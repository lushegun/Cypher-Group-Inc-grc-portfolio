[← Portfolio home](../README.md) · [All templates](README.md)

# [ORGANISATION] — Vendor Inventory and Tiering Register

| Field | Value |
|---|---|
| Document ID | [DOC-ID] |
| Version | [1.0] |
| Date | [DD Month YYYY] |
| Prepared by | [Assessor] |
| Approved by | [Approver, Job Title] |
| Next review | [DD Month YYYY] |

> [!NOTE]
> **[FICTIONAL DATA NOTICE — delete if this is a real engagement. If it is a portfolio artifact,
> keep it and state that all vendor assurance and contract statuses are invented for the scenario.]**

> [!TIP]
> **How to use this template.** Everything in `[SQUARE BRACKETS]` is a field to replace.
> Everything outside them is method and should be changed only deliberately. Guidance sits in
> `>` blockquotes and is deleted before the document is issued. Derived from CGI-TPR-001 v1.0.

## 1. The tiering model — publish this BEFORE assigning any tier

**Step 1 — score four factors, each 0 to 3.**

| Factor | 0 | 1 | 2 | 3 |
|---|---|---|---|---|
| **D — Data exposure** (highest classification reachable) | [Public] | [Internal] | [Confidential] | [Restricted] |
| **A — Availability dependency** | No operational effect | Internal inconvenience | Major internal disruption | Customer-facing outage |
| **C — Connectivity / privilege** | No system access | Read-only integration | Read-write or SSO | Production or source-code access |
| **R — Replaceability** | < 1 business day | < 1 week | < 1 month | > 1 month or lock-in |

**Step 2 — mandatory escalation triggers, applied BEFORE the total.**

| Trigger | Condition | Effect |
|---|---|---|
| **T1-a** | Processes or can access [RESTRICTED] data | Forces Tier 1 |
| **T1-b** | Holds or can access production customer data | Forces Tier 1 |
| **T1-c** | Write access to production infrastructure or source code | Forces Tier 1 |
| **T1-d** | Failure causes a customer-facing outage | Forces Tier 1 |
| **T1-e** | Named to customers as a sub-processor | Forces Tier 1 |
| **T2-f** | Processes content through an automated or AI system that may retain, review or train on it | Forces minimum Tier 2 |
| **[T1-g]** | *[Add a sector trigger here — e.g. supports a critical or important function under DORA]* | [Forces Tier 1] |

**Step 3 — where no trigger fires, the total decides.**

| Tier | Total | Assessment depth | Evidence standard | Approval | Cadence | Onboarding SLA |
|:-:|---|---|---|---|---|---|
| **1** | ≥ 8 or any T1 trigger | [Full questionnaire + assurance artifact review + DPA + data-flow review] | Independent attestation mandatory | [CEO] | [12 months] | [15 business days] |
| **2** | 4–7 or T2-f | [Lite questionnaire + artifact + DPA] | Attestation preferred; self-assessment with written justification | [CTO] | [18 months] | [7 business days] |
| **3** | ≤ 3 | [Attestation + DPA confirmation] | Self-assessment accepted | [Business owner] | [24 months] | [2 business days] |

## 2. Discovery sources — use all four, not just the first

| # | Source | What only this source finds |
|:-:|---|---|
| 1 | Known architecture and existing documentation | The production stack you already knew about |
| 2 | **[12] months of finance and card transactions** | **Anything with a recurring charge, including personal-card expenses** |
| 3 | **OAuth grants and connected apps in the identity provider** | **Anything holding a token against company data, paid or not** |
| 4 | One [20]-minute conversation per business function | Departmental tools and the business reason for them |

> Sources 2 and 3 are what find shadow IT. Source 1 alone typically returns a quarter of the true estate.

## 3. The inventory

*Paste-ready version: `vendor-risk-inventory-template.csv`*

| Vendor ID | Vendor Name | Service | Owner (Job Title) | Class. | Hosting | Sub-proc. | DPA | Assurance Held | D | A | C | R | Total | Trigger | Tier | L | I | Inherent | Status | Next Review |
|---|---|---|---|---|---|---|---|---|:-:|:-:|:-:|:-:|:-:|---|:-:|:-:|:-:|:-:|---|---|
| [VEN-001] | [Name] | [Service] | [Job title] | [Class] | [Region] | [Y/N] | [Y/N/Date] | [Artifact + date] | [0-3] | [0-3] | [0-3] | [0-3] | [=SUM] | [T1-x/-] | [1/2/3] | [1-5] | [1-5] | [=LxI] | [Status] | [Date] |
| [VEN-002] | | | | | | | | | | | | | | | | | | | | |
| [VEN-003] | | | | | | | | | | | | | | | | | | | | |

## 4. Summary statistics to report

| Metric | Value |
|---|---|
| Vendors in scope | [n] |
| Tier 1 / 2 / 3 | [n] / [n] / [n] |
| **With no executed DPA** | **[n] ([%])** |
| **With no assurance artifact held on file** | **[n] ([%])** |
| Discovered outside any procurement process | [n] |
| Aggregate inherent vendor risk | [n], mean [n.nn] |
| Vendors at inherent Critical / High | [n] / [n] |

## 5. Concentration analysis

> Draw the dependency graph, not the list. Identify every vendor sharing an underlying provider with
> your own platform, and state what fails together.

```
                    [SHARED UNDERLYING PROVIDER]
                              │
        ┌──────────┬──────────┼──────────┬──────────┐
        ▼          ▼          ▼          ▼          ▼
   [your platform] [monitoring] [ticketing] [docs]  [other]
```

**[State the second-order consequence: what you lose the ability to DO, not just what goes offline.]**
