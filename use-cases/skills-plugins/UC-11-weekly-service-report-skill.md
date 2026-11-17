# UC-11: Skill: weekly IT service report on a schedule

[Previous: UC-10](../skills-plugins/UC-10-change-request-review-skill.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-12](../skills-plugins/UC-12-itsm-plugin.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork skill + scheduled task |
| **Persona** | Service Delivery Manager |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Service_KPIs` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Incidents` tab) |
| **Skills and tools** | Custom skill `contoso-weekly-service-report` + Excel, Word, Email |
| **Output** | A weekly service report in Word and a draft cover email, ready every Monday morning |
| **Value** | Saves 2 to 3 hours each week and delivers a consistent report that leadership can compare week to week |

## Scenario

Each Monday the Service Delivery Manager produces the weekly IT service report: ticket volumes, SLA performance, major incidents, backlog and customer satisfaction. The data comes from exports and the commentary takes the longest.

## Before you start

- Download [contoso-weekly-service-report/SKILL.md](../../skills/contoso-weekly-service-report/SKILL.md) and upload it.

## Steps

### Step 1: Run the skill once

Check the output.

```text
/contoso-weekly-service-report Use the attached workbook for the week ending 16 November 2026.
```

### Step 2: Adjust the commentary

Make sure the narrative matches your view.

```text
Explain the rise in backlog over the last two weeks and propose two actions. Keep the tone factual.
```

### Step 3: Schedule it

Have it ready every week.

```text
Every Monday at 07:00 Dubai time, run contoso-weekly-service-report using the latest export in my OneDrive folder IT Reports/Weekly, and create the cover email to the IT Leadership Team as a draft.
```

## What good looks like

- [ ] KPIs match the Service_KPIs tab, including the backlog rise in the last two weeks.
- [ ] Major incidents for the week are listed with duration and SLA status.
- [ ] The report has a trend chart and three to five commentary points.
- [ ] The email is a draft; the manager reviews before sending.

## Try this next

**Monthly version**

```text
Create a monthly service report for the CIO from the four weekly reports, with month-on-month trends.
```

**Site breakdown**

```text
Add a section that compares Head Office, Operations Centre and the remote sites.
```

## Make it repeatable

Share the skill with every service delivery manager so all towers report the same way.

## Tips

- Keep the export file name and location stable so the scheduled task always finds it.
- Pause scheduled tasks during holidays.

## Related

- [UC-01 Daily IT operations briefing](../../use-cases/cowork/UC-01-daily-it-operations-briefing.md)
- [Lab 3](../../labs/lab-03-scheduled-ops-briefing.md)

---

[Previous: UC-10](../skills-plugins/UC-10-change-request-review-skill.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-12](../skills-plugins/UC-12-itsm-plugin.md)
