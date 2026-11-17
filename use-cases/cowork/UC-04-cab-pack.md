# UC-04: Change Advisory Board (CAB) pack

[Previous: UC-03](../cowork/UC-03-post-incident-review.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-05](../cowork/UC-05-license-optimisation.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork |
| **Persona** | Change Manager |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Changes` tab) |
| **Skills and tools** | Excel, PowerPoint, Word |
| **Output** | CAB deck, one-page risk summary and the forward schedule of change |
| **Value** | Preparing the weekly CAB pack drops from about 3 hours to 45 minutes including review |

## Scenario

Every week Contoso's Change Manager prepares the CAB pack: the list of proposed changes, risk assessment, conflicts and missing information. Two changes this week overlap on the Head Office core network on Saturday night, and two have no rollback plan.

## Before you start

- Attach the workbook (Changes tab), or export next week's changes from your ITSM tool to Excel or CSV.

## Steps

### Step 1: Analyse the changes

Ask for checks before the deck.

```text
Use the Changes tab of the attached workbook for the week of 17 to 23 November 2026.
Check every change and list:
- changes that overlap in the same service and site window
- changes with no rollback plan or an untested rollback
- high-risk changes without business approval
- emergency changes that need retrospective CAB review
Do not approve or reject any change.
```

### Step 2: Build the CAB deck

Turn the analysis into the meeting pack.

```text
Create a 6-slide CAB deck:
1. Week at a glance (counts by risk and type)
2. Forward schedule of change (timeline by day)
3. Conflicts and proposed resolutions
4. High-risk changes: summary, impact, rollback, approval status
5. Changes not ready for approval and what is missing
6. Retrospective review: emergency change CHG-3092
Add speaker notes with questions for each implementer.
```

### Step 3: Risk summary

One page for the CAB chair.

```text
Write a one-page Word risk summary for the CAB chair with a recommendation for each change: ready, ready with conditions, or not ready, and the reason.
```

### Step 4: Implementer follow-ups

Ask for missing information before the meeting.

```text
Draft an email to each implementer group whose change is not ready, listing exactly what is missing. Create drafts only.
```

## What good looks like

- [ ] CHG-3108 and CHG-3109 are flagged as a conflict on Saturday 22 November, 22:00 to 02:00, at Head Office.
- [ ] CHG-3104 and CHG-3112 are flagged for missing rollback plans.
- [ ] CHG-3111 (Exchange hybrid certificate renewal) is shown as high risk.
- [ ] CHG-3092 appears for retrospective review.
- [ ] No change is approved or rejected by Cowork.

## Try this next

**Change freeze check**

```text
List any change planned during the year-end change freeze from 20 December to 3 January and draft a note to the implementers.
```

**Post-CAB minutes**

```text
Using my notes from the CAB meeting, record the decision for each change and update the Changes tab with the CAB status.
```

## Make it repeatable

Use the [change request review skill](../skills-plugins/UC-10-change-request-review-skill.md) for quality checks, and the [Change Calendar app](../../cowork-apps/APP-02-change-calendar-cab-tracker.md) to track decisions.

## Tips

- Ask for flags and recommendations; the CAB decides.
- Keep the same slide order every week so CAB members know where to look.

## Related

- [UC-10 Skill: change request quality review](../../use-cases/skills-plugins/UC-10-change-request-review-skill.md)
- [UC-19 Change and maintenance notification agent](../../use-cases/copilot-studio/UC-19-change-notification-agent.md)
- [APP-02 Change Calendar and CAB Tracker](../../cowork-apps/APP-02-change-calendar-cab-tracker.md)
- [Lab 1](../../labs/lab-01-cowork-cab-pack.md)

---

[Previous: UC-03](../cowork/UC-03-post-incident-review.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-05](../cowork/UC-05-license-optimisation.md)
