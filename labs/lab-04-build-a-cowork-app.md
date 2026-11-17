# Lab 4: Build the Change Calendar and CAB Tracker app

[Previous: Lab 3](lab-03-scheduled-ops-briefing.md) | [Labs](README.md) | [Home](../README.md) | Next: [Lab 5](lab-05-copilot-studio-service-desk-agent.md)

**App:** [APP-02 Change Calendar and CAB Tracker](../cowork-apps/APP-02-change-calendar-cab-tracker.md)
**Reference file:** [Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx), `Changes` tab

## Task 1: Describe the app

Attach the workbook and paste:

```text
/app Build a Change Calendar and CAB Tracker for Contoso IT.

Purpose: plan changes, spot conflicts and record CAB decisions in one place.
Users: Change Manager edits all; implementers edit their own changes; CAB members comment.
Data: one SharePoint list, Changes, with the columns from the Changes tab of the attached
workbook, plus CAB decision notes.
Seed data: import all rows from the Changes tab.
Screens: weekly calendar by site coloured by risk; conflicts view; CAB agenda with
readiness checks; decision log; dashboard.
Rules: flag a conflict when two changes overlap on the same service and site;
a change is 'Not ready' if it has no rollback plan or no business approval;
emergency changes appear in a 'Retrospective review' section.
```

## Task 2: Review the design

Read the requirements and data design Cowork proposes. Answer its questions. Check the column types (dates, choices).

## Task 3: Iterate

```text
Add a change freeze from 20 December to 3 January and show a warning on any change in that period.
```

```text
Let CAB members record Approve, Reject or Defer with a comment on the CAB agenda screen.
```

## Task 4: Publish and share

Publish the app and share it with one colleague. Open it from the link.

## What good looks like

- [ ] The calendar shows the week of 17 to 23 November with changes coloured by risk.
- [ ] The conflicts view shows CHG-3108 and CHG-3109.
- [ ] CHG-3104 and CHG-3112 show as Not ready.
- [ ] Your change requests appear in the preview.

> A Cowork app is a fast team tool. Before using live operational data, agree the data store, owner and sharing with your platform team.
