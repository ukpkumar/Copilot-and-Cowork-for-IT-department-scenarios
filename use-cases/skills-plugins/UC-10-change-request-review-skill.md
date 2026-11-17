# UC-10: Skill: change request quality review

[Previous: UC-09](../skills-plugins/UC-09-incident-update-skill.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-11](../skills-plugins/UC-11-weekly-service-report-skill.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork skill |
| **Persona** | Change Manager |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Changes` tab) |
| **Skills and tools** | Custom skill `contoso-change-review` + Excel, Word |
| **Output** | A quality verdict and a fix list for each change request before it reaches CAB |
| **Value** | Fewer changes deferred at CAB for missing information; fewer failed changes from untested rollbacks |

## Scenario

Change requests often arrive at CAB with weak risk assessments, no rollback plan or no test evidence. The Change Manager wants every request reviewed against the same checklist, and implementers want to self-check before they submit.

## Before you start

- Download [contoso-change-review/SKILL.md](../../skills/contoso-change-review/SKILL.md) and upload it to Cowork.

## Steps

### Step 1: Review one change

Paste or describe a change request.

```text
/contoso-change-review Review change CHG-3112 from the attached workbook.
```

### Step 2: Review a batch

Run it on the whole week.

```text
/contoso-change-review Review every Normal and Emergency change in the Changes tab and return a table: change ID, verdict (Ready / Ready with conditions / Not ready), missing items, and the question to ask the implementer.
```

### Step 3: Implementer self-check

Share the skill with implementer groups so they can check before submitting.

```text
I'm about to submit a change to upgrade the core switch firmware at Head Office on Saturday 22 November 22:00. Review my draft: <paste draft>.
```

## What good looks like

- [ ] CHG-3104 and CHG-3112 are Not ready (no rollback plan).
- [ ] CHG-3108 is Ready with conditions because it conflicts with CHG-3109.
- [ ] CHG-3092 is flagged for retrospective review as an emergency change with untested rollback.
- [ ] The skill never approves a change; it gives a verdict and fix list.

## Try this next

**Risk scoring**

```text
Edit the skill to calculate a risk score from impact, likelihood, number of users and site criticality.
```

**Standard change candidates**

```text
Find changes that have run successfully at least five times and could become standard changes.
```

## Make it repeatable

Include it in the [IT service management plugin](UC-12-itsm-plugin.md).

## Tips

- Keep the checklist in the skill aligned with your change policy; update the skill when the policy changes.
- Ask for questions to the implementer, not just a verdict.

## Related

- [UC-04 Change Advisory Board (CAB) pack](../../use-cases/cowork/UC-04-cab-pack.md)
- [APP-02 Change Calendar and CAB Tracker](../../cowork-apps/APP-02-change-calendar-cab-tracker.md)

---

[Previous: UC-09](../skills-plugins/UC-09-incident-update-skill.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-11](../skills-plugins/UC-11-weekly-service-report-skill.md)
