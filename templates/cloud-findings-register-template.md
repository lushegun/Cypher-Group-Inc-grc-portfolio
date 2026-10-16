[← Portfolio home](../README.md) · [All templates](README.md)

# [ORGANISATION] — Cloud findings register — TEMPLATE

> [!TIP]
> **How to use this template.** Blank reusable template from the CGI-AWS-001 portfolio project (simulated). One row per
> finding, grouped by root cause rather than one row per failed check. Replace every `[BRACKETED]` field. Publish the
> severity rule before you grade anything.

## Severity rule (edit, then publish before grading)

| Severity | Rule |
|---|---|
| **Critical** | An exposure that exists now, reachable from outside Cypher (the internet or a third party), on a path to production or Restricted data, with no compensating control. |
| **High** | A missing guardrail or detective control on the R-005 path, or a failed CloudCo CUEC: one mistake away from Critical. |
| **Medium** | A Level 1 gap that weakens another control, or a policy breach with a compensating factor. |
| **Low** | A Level 2 defence-in-depth gap. |

**Effort:** S = up to one day · M = up to two weeks · L = more than two weeks.

## Register

| Finding ID | Severity | Title | CIS | What exists | Root cause | Remediation | Effort | Owner | Due | Roadmap | Risk ID | Provider CUEC | Status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| CF-01 | [Critical] | [A title a CEO understands] | [5.3; 5.2] | [What, where, since when, evidenced how] | [Why it happened] | [The control to implement, in order] | [S] | [JOB TITLE] | [DD Mon YYYY] | [ID] | [RISK] | [CUEC or -] | Open |
| [CF-NN] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | Open |
| [CF-NN] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | Open |
| [CF-NN] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | Open |
| [CF-NN] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | Open |
| [CF-NN] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | Open |
| [CF-NN] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | [ ] | Open |

## Writing a good finding

- **Title:** say the consequence in plain English ("a contractor login is still live, with no MFA"), not the check name.
- **What exists:** the asset, the setting, the date it changed and the evidence that shows it.
- **Root cause:** why the control failed. Three findings with one root cause usually need one fix.
- **Remediation:** name the control to implement; leave the engineering design to the engineer.

## Fill-in checklist

- [ ] Every failed check is covered by a finding
- [ ] Every finding has one owner (a job title) and one date
- [ ] Critical findings have a containment date in days, not quarters
- [ ] Each finding links to a roadmap ID and a risk ID

<sub>Free to use and adapt with attribution. Provided as-is, without warranty.</sub>
