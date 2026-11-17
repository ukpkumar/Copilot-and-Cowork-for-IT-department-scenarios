# UC-01: Daily IT operations briefing

[Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-02](../cowork/UC-02-major-incident-communications.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork + scheduled task |
| **Persona** | IT Operations Manager |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Incidents` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Service_KPIs` tab) |
| **Skills and tools** | Daily Briefing, Enterprise Search, Email, Excel |
| **Output** | A one-page morning briefing in chat, or a draft email to the operations leads |
| **Value** | Replaces 30 to 45 minutes of reading dashboards, mail and chats every morning |

## Scenario

Every morning the IT Operations Manager at Contoso reads the overnight monitoring emails, the service desk queue, the change calendar and several Teams channels before the 08:30 operations stand-up. The information is scattered and the first half hour of the day goes on collecting it. Cowork gathers it and writes the briefing; a scheduled task makes it arrive every working day.

## Before you start

- Attach the practice workbook, or, in your own tenant, make sure you have access to the operations mailbox folders and Teams channels you want summarised.
- Decide who the briefing is for: yourself only, or a draft email to the operations leads.

## Steps

### Step 1: Ask for today's briefing

Start with a one-off briefing to check the content and format.

```text
Prepare my IT operations briefing for this morning's 08:30 stand-up.
Use the attached workbook (Incidents and Service_KPIs tabs) and, if available,
my email and the "IT Operations" Teams channel from the last 24 hours.

Structure:
1. Headline: overall service status in one sentence (green, amber or red)
2. Open P1 and P2 incidents: ID, service, site, age, owner, next update
3. SLA breaches in the last 24 hours
4. Changes planned in the next 48 hours, with any high-risk ones flagged
5. Service desk: backlog trend and anything unusual
6. Three decisions or escalations I need to make today

Keep it to one page. Use a table for incidents. Do not send anything.
```

### Step 2: Check the sources

Ask where each item came from.

```text
For each item in the briefing, show the source (file and tab, email subject, or Teams message) it came from, and list anything you inferred.
```

### Step 3: Refine the format

Adjust the briefing until it is right for your stand-up.

```text
Move the decisions section to the top, add a column for 'customer impact' in the incident table, and highlight remote sites in bold.
```

### Step 4: Schedule it

Turn the agreed prompt into a scheduled task.

```text
Run this briefing every working day (Monday to Friday) at 07:15 Dubai time. Show it to me only; do not send email or post in Teams.
```

## What good looks like

- [ ] Open P1/P2 incidents and SLA breaches match the Incidents tab.
- [ ] The backlog trend reflects the rise in the last two weeks of Service_KPIs.
- [ ] The briefing fits on one page and ends with clear decisions.
- [ ] The scheduled task is saved with the right days and time zone, and sends nothing.

## Try this next

**Event-driven version**

```text
When an email arrives from the monitoring system with 'P1' in the subject, summarise it and add it to a running 'Today's major issues' note for me.
```

**Weekly roll-up**

```text
Every Friday at 15:00, summarise this week's daily briefings into a one-page weekly operations summary for the Head of IT Infrastructure as a draft email.
```

## Make it repeatable

Save the final prompt as the skill `contoso-ops-briefing` so other operations managers get the same format (see [Module 3](../../modules/03-skills-and-plugins.md)).

## Tips

- Name the channels and folders explicitly; Cowork works better with clear sources.
- Keep the briefing private while you test it. Share it only once the format is stable.
- Pause or delete scheduled tasks you no longer need.

## Related

- [UC-11 Skill: weekly IT service report on a schedule](../../use-cases/skills-plugins/UC-11-weekly-service-report-skill.md)
- [APP-01 Major Incident Command Board](../../cowork-apps/APP-01-major-incident-command-board.md)

---

[Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-02](../cowork/UC-02-major-incident-communications.md)
