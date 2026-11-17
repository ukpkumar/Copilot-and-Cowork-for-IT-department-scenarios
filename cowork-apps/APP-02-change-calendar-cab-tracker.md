# APP-02: Change Calendar and CAB Tracker

[Previous: APP-01](APP-01-major-incident-command-board.md) | [Cowork apps](README.md) | [Home](../README.md) | [Next: APP-03](APP-03-licence-and-asset-tracker.md)

## At a glance

| | |
|---|---|
| **Users** | Change Manager (edit), CAB members (vote and comment), implementers (edit own changes), service owners (view) |
| **Replaces** | Emailed change lists, manual conflict checks and CAB decisions recorded in minutes |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Changes` tab) |
| **Built with** | Cowork App skill (`/app`), SharePoint lists |

## Data model

**Changes**: Change ID, Title, Type, Risk, Service, Site, Planned start, Planned end, Implementer group, Rollback plan, Rollback tested, Business approval, CAB status, CAB decision notes, Conflict

## Screens

- **Calendar**: week view of changes by site and service, coloured by risk
- **Conflicts**: changes that overlap on the same service and site
- **CAB agenda**: changes pending CAB, with readiness checks (rollback, approval)
- **Decision log**: CAB decision and conditions for each change
- **Dashboard**: changes by risk and type, success rate, emergency changes this month

## Build it

1. Open Cowork and attach the reference files listed above.
2. Paste the prompt below. Review the requirements Cowork confirms and answer its questions.
3. Review the preview, then iterate with the prompts in the next section.
4. Publish the app and share it with a test group.

```text
/app Build a Change Calendar and CAB Tracker for Contoso IT.

Purpose: plan changes, spot conflicts and record CAB decisions in one place.
Users: Change Manager edits all; implementers edit their own changes; CAB members comment.
Data: one SharePoint list, Changes, with the columns from the Changes tab of the attached workbook,
plus CAB decision notes.
Seed data: import all rows from the Changes tab.
Screens: weekly calendar by site coloured by risk; conflicts view; CAB agenda with readiness checks;
decision log; dashboard.
Rules: flag a conflict when two changes overlap on the same service and site;
a change is 'Not ready' if it has no rollback plan or no business approval;
emergency changes appear in a 'Retrospective review' section.
```

## Iterate

```text
Add a change freeze period from 20 December to 3 January and block new changes in it.
```

```text
Let CAB members record Approve / Reject / Defer with a comment.
```

```text
Add a filter for remote sites.
```

## What to show in a demo

- [ ] CHG-3108 and CHG-3109 appear as a conflict on Saturday 22 November at Head Office.
- [ ] CHG-3104 and CHG-3112 show as Not ready.
- [ ] CHG-3092 appears under Retrospective review.

## Related use cases

- [UC-04 Change Advisory Board (CAB) pack](../use-cases/cowork/UC-04-cab-pack.md)
- [UC-10 Skill: change request quality review](../use-cases/skills-plugins/UC-10-change-request-review-skill.md)
- [UC-19 Change and maintenance notification agent](../use-cases/copilot-studio/UC-19-change-notification-agent.md)
- [Lab 4](../labs/lab-04-build-a-cowork-app.md)

---

[Previous: APP-01](APP-01-major-incident-command-board.md) | [Cowork apps](README.md) | [Home](../README.md) | [Next: APP-03](APP-03-licence-and-asset-tracker.md)
