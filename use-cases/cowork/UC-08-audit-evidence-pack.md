# UC-08: Security audit evidence pack

[Previous: UC-07](../cowork/UC-07-vendor-sla-review.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-09](../skills-plugins/UC-09-incident-update-skill.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork |
| **Persona** | IT Risk and Compliance Lead |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Audit_Controls` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Access_Review` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Changes` tab) |
| **Skills and tools** | Enterprise Search, Excel, Word |
| **Output** | Evidence index, gap list with owners, and request emails to control owners (drafts) |
| **Value** | Reduces audit preparation from weeks of chasing to a tracked, evidence-indexed pack |

## Scenario

Contoso's ISO/IEC 27001 surveillance audit is in four weeks. The IT Risk and Compliance Lead must show evidence for each control in scope, find gaps early and chase control owners.

## Before you start

- Attach the workbook. In your own tenant, Cowork can also search the compliance SharePoint site for evidence documents you can access.

## Steps

### Step 1: Assess evidence status

Find the gaps.

```text
Using the Audit_Controls tab, list every control with evidence missing or partial, the owner role, and what evidence is required. Sort by risk to the audit.
```

### Step 2: Cross-check with operational data

Look for evidence in the data you have.

```text
For control A.5.15 (access control), use the Access_Review tab: how many review items are still pending,
and how many leavers still have access? For control A.8.32 (change management),
use the Changes tab: which changes lack rollback plans or approval?
Summarise these as audit findings risks.
```

### Step 3: Build the evidence index

Create the auditor-facing index.

```text
Create an Excel evidence index: control ID, control name, evidence item, location, owner role, status, and a 'ready for auditor' flag.
```

### Step 4: Chase owners

Prepare the requests.

```text
Draft an email to each control owner role with the evidence they need to provide and the due date of 1 December 2026. Draft only.
```

## What good looks like

- [ ] 3 controls with missing evidence and 4 partial ones are listed.
- [ ] The access review shows 12 pending items and 5 leavers with access, flagged as a risk to A.5.15.
- [ ] Change records without rollback plans are flagged against A.8.32.
- [ ] Emails are drafts addressed to roles.

## Try this next

**Auditor briefing**

```text
Create a short briefing note for the auditors explaining our IT control environment and where evidence is stored.
```

**Weekly readiness**

```text
Every Monday until the audit, update the evidence status and show me what changed.
```

## Make it repeatable

Use the [Access Review Tracker app](../../cowork-apps/APP-04-access-review-tracker.md) to close the access review gaps.

## Tips

- Cowork finds only evidence you have permission to see.
- Label audit evidence with the right sensitivity label.

## Related

- [APP-04 Access Review Campaign Tracker](../../cowork-apps/APP-04-access-review-tracker.md)
- [UC-15 Access request and approval agent](../../use-cases/copilot-studio/UC-15-access-request-agent.md)

---

[Previous: UC-07](../cowork/UC-07-vendor-sla-review.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-09](../skills-plugins/UC-09-incident-update-skill.md)
