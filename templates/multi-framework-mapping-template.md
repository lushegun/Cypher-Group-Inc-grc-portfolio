[← Portfolio home](../README.md) · [All templates](README.md)

# [ORGANISATION] — Multi-framework mapping (CIS → ISO/IEC 27001 → SOC 2 → NIST CSF 2.0 → risk) — TEMPLATE

> [!TIP]
> **How to use this template.** Blank reusable template from the CGI-AWS-001 portfolio project (simulated). One row
> per finding, traced through five systems so one remediation can be reported to every audience. Replace every
> `[BRACKETED]` field. Map to the outcome the control serves, not to a keyword in its title.

## The default mapping by control theme

Start here, then adjust for your own control set.

| Theme | CIS AWS v5.0.0 | ISO/IEC 27001:2022 Annex A | SOC 2 TSC | NIST CSF 2.0 |
|---|---|---|---|---|
| Root and privileged access | 1.3–1.6, 1.15 | A.8.2; A.8.5 | CC6.1; CC6.3 | PR.AA-03; PR.AA-05 |
| User credentials and MFA | 1.7–1.13 | A.5.17; A.8.5; A.5.18 | CC6.1; CC6.2 | PR.AA-01; PR.AA-03 |
| Least privilege and federation | 1.14, 1.15, 1.19, 1.20 | A.5.15; A.5.16; A.5.18 | CC6.1–CC6.3 | PR.AA-05 |
| Storage exposure | 2.1.4, 2.2.3 | A.8.3; A.5.15; A.8.20 | CC6.1; CC6.6 | PR.DS-01; PR.IR-01 |
| Encryption and keys | 2.1.1, 2.2.1, 2.3.1, 3.5, 3.6, 5.1.1 | A.8.24 | CC6.1; CC6.7 | PR.DS-01; PR.DS-02 |
| Data discovery | 2.1.3 | A.5.9; A.5.12 | C1.1 | ID.AM-07 |
| Logging and log integrity | 3.1, 3.2, 3.4, 3.8, 3.9 | A.8.15; A.5.28 | CC7.2 | PR.PS-04; DE.CM-09 |
| Configuration recording | 3.3 | A.8.9 | CC7.1; CC8.1 | DE.CM; PR.PS-01 |
| Monitoring and alerting | 4.1–4.16 | A.8.16 | CC7.2; CC7.3 (CC8.1 for change events) | DE.CM; DE.AE |
| Network boundary | 5.1.2–5.6, 3.7 | A.8.20; A.8.21; A.8.22 | CC6.6 | PR.IR-01; DE.CM-01 |
| Host hardening | 5.7, 2.2.2 | A.8.9; A.8.8 | CC6.1; CC7.1 | PR.PS-01; PR.PS-02 |

## The mapping

| Finding ID | Title | CIS | ISO/IEC 27001 Annex A | SOC 2 | NIST CSF 2.0 | Risk ID | Why this mapping |
|---|---|---|---|---|---|---|---|
| CF-01 | [Example] Admin port open to the internet | 5.3; 5.2 | A.8.20; A.8.21 | CC6.6 | PR.IR-01 | [RISK ID] | Boundary protection fails in every framework |
| [CF-NN] | [TITLE] | [CIS] | [ANNEX A] | [TSC] | [CSF] | [RISK] | [WHY] |
| [CF-NN] | [TITLE] | [CIS] | [ANNEX A] | [TSC] | [CSF] | [RISK] | [WHY] |
| [CF-NN] | [TITLE] | [CIS] | [ANNEX A] | [TSC] | [CSF] | [RISK] | [WHY] |
| [CF-NN] | [TITLE] | [CIS] | [ANNEX A] | [TSC] | [CSF] | [RISK] | [WHY] |
| [CF-NN] | [TITLE] | [CIS] | [ANNEX A] | [TSC] | [CSF] | [RISK] | [WHY] |
| [CF-NN] | [TITLE] | [CIS] | [ANNEX A] | [TSC] | [CSF] | [RISK] | [WHY] |

## Fill-in checklist

- [ ] Every finding maps to at least one entry in every column, or says 'none' and why
- [ ] CSF entries are Subcategories where you can defend them, Categories where you cannot
- [ ] Risk IDs come from your register; if a finding fits no existing risk, test whether it is genuinely new before adding one
- [ ] Criterion and control wording is paraphrased, not copied from licensed texts

<sub>Free to use and adapt with attribution. Provided as-is, without warranty.</sub>
