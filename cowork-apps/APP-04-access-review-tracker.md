# APP-04: Access Review Campaign Tracker

[Previous: APP-03](APP-03-licence-and-asset-tracker.md) | [Cowork apps](README.md) | [Home](../README.md) | [Next: APP-05](APP-05-it-demand-intake.md)

## At a glance

| | |
|---|---|
| **Users** | Identity team (edit), reviewers (decide on their items), auditors (view) |
| **Replaces** | Quarterly access reviews run by email and spreadsheet attachments |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Access_Review` tab) |
| **Built with** | Cowork App skill (`/app`), SharePoint lists |

## Data model

**Review items**: Item ID, Application, Account, Access level, Reviewer role, Decision (Keep / Remove / Pending), Employment status, Due date, Decided on, Comment

## Screens

- **My reviews**: items for the signed-in reviewer with Keep and Remove buttons
- **Campaign progress**: completion by application and reviewer
- **Risk view**: leavers and movers still holding access
- **Evidence export**: completed decisions for the auditors

## Build it

1. Open Cowork and attach the reference files listed above.
2. Paste the prompt below. Review the requirements Cowork confirms and answer its questions.
3. Review the preview, then iterate with the prompts in the next section.
4. Publish the app and share it with a test group.

```text
/app Build an Access Review Campaign Tracker for Contoso IT.

Purpose: run the Q4 2026 access review and give auditors clear evidence.
Users: identity team edits; reviewers decide on their own items; auditors view.
Data: SharePoint list Review items with the columns of the Access_Review tab plus Decided on and Comment.
Seed data: import the Access_Review tab from the attached workbook.
Screens: my reviews worklist with Keep and Remove actions; campaign progress by application;
risk view of leavers and movers with access; evidence view of completed decisions.
Rules: leavers with access are always shown in red at the top;
a Remove decision requires a comment; due date 30 November 2026.
```

## Iterate

```text
Add a progress KPI: % of items decided.
```

```text
Add a reminder list of reviewers with pending items.
```

```text
Add a column showing days to due date.
```

## What to show in a demo

- [ ] 12 items pending and 5 leavers with access at the top of the risk view.
- [ ] Record a Remove decision and see progress update.
- [ ] Use the evidence view for control A.5.15 in UC-08.

## Related use cases

- [UC-08 Security audit evidence pack](../use-cases/cowork/UC-08-audit-evidence-pack.md)
- [UC-15 Access request and approval agent](../use-cases/copilot-studio/UC-15-access-request-agent.md)
- [UC-16 Joiner, mover, leaver (JML) IT agent](../use-cases/copilot-studio/UC-16-joiner-mover-leaver-agent.md)

---

[Previous: APP-03](APP-03-licence-and-asset-tracker.md) | [Cowork apps](README.md) | [Home](../README.md) | [Next: APP-05](APP-05-it-demand-intake.md)
