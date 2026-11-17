# Lab 1: Build a CAB pack with Cowork

[Previous: Lab 0](lab-00-setup.md) | [Labs](README.md) | [Home](../README.md) | Next: [Lab 2](lab-02-create-and-share-a-skill.md)

**Use case:** [UC-04 CAB pack](../use-cases/cowork/UC-04-cab-pack.md)
**Reference file:** [Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx), `Changes` tab

## Scenario

You are Contoso's Change Manager. Tuesday's CAB reviews 16 changes for the week of 17 to 23 November 2026. Prepare the pack, find the problems before the meeting and chase the implementers.

## Task 1: Analyse the changes

Attach the workbook and paste:

```text
Use the Changes tab of the attached workbook for the week of 17 to 23 November 2026.
Check every change and list:
- changes that overlap in the same service and site window
- changes with no rollback plan or an untested rollback
- high-risk changes without business approval
- emergency changes that need retrospective CAB review
Show the result as a table. Do not approve or reject any change.
```

## Task 2: Build the CAB deck

```text
Create a 6-slide CAB deck:
1. Week at a glance (counts by risk and type)
2. Forward schedule of change (timeline by day)
3. Conflicts and proposed resolutions
4. High-risk changes: summary, impact, rollback, approval status
5. Changes not ready for approval and what is missing
6. Retrospective review: emergency change CHG-3092
Add speaker notes with one question for each implementer.
```

## Task 3: Check the sources

```text
For each conflict and each 'not ready' change, show the row in the Changes tab it came from.
```

## Task 4: Chase the implementers

```text
Draft an email to each implementer group whose change is not ready,
listing exactly what is missing and asking for it by Monday 12:00. Drafts only.
```

## What good looks like

- [ ] CHG-3108 and CHG-3109 are shown as a conflict on Saturday 22 November, Head Office core network.
- [ ] CHG-3104 and CHG-3112 are flagged for missing rollback plans.
- [ ] CHG-3111 (Exchange hybrid certificate renewal) is shown as high risk.
- [ ] CHG-3092 is on the retrospective review slide.
- [ ] The deck has speaker notes; emails are drafts.

## Stretch

```text
Turn the checks you made in Task 1 into a reusable skill called contoso-cab-check.
```
