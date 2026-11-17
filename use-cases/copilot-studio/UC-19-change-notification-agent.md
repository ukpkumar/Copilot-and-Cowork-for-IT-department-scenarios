# UC-19: Change and maintenance notification agent

[Previous: UC-18](../copilot-studio/UC-18-security-alert-triage-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-20](../copilot-studio/UC-20-device-compliance-agent.md)

## At a glance

| | |
|---|---|
| **Workload** | Copilot Studio agent flow (scheduled) |
| **Persona** | Change Manager; business users |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Changes` tab) |
| **Skills and tools** | Recurrence trigger, change data, AI prompt step, Outlook, Teams |
| **Output** | Business-friendly notices about approved changes, sent to affected sites and services before each window |
| **Value** | Fewer surprise outages and fewer calls to the service desk during maintenance windows |

## Scenario

Business users at Contoso's sites are not told about maintenance windows in language they understand, so the service desk is flooded with calls during planned work.

## Before you start

- Approved changes available from the ITSM system or a SharePoint list.
- Distribution lists or Teams channels per site.

## Steps

### Step 1: Build the agent flow

Create an agent flow with a **Recurrence** trigger (daily at 10:00): get approved changes starting in the next 48 hours → for each, run a **prompt** that rewrites the technical description in plain language (what users will notice, when, what to do) → post to the site's Teams channel and email the site distribution list.

### Step 2: Write the prompt step

Use this prompt in the AI step.

```text
Rewrite this change for business users in under 80 words.
Say what service is affected, when (local time), what users will notice,
and what they should do. No technical jargon. Change: {change_details}
```

### Step 3: Test

Run the flow against the Changes tab data in a test environment, then check the notices for CHG-3108 and CHG-3111.

## What good looks like

- [ ] Only approved changes are announced.
- [ ] Notices state local time and the affected site.
- [ ] Language is plain and short.

## Try this next

**Reminder and completion**

```text
Send a reminder 1 hour before and a completion notice when the change is closed.
```

**Ask the agent**

```text
Add a conversational agent so users can ask 'Is any maintenance planned for my site this week?'
```

## Make it repeatable

Link it to the [Change Calendar app](../../cowork-apps/APP-02-change-calendar-cab-tracker.md).

## Tips

- Include a human review step at first; remove it once the notices are consistently good.

## Related

- [UC-04 Change Advisory Board (CAB) pack](../../use-cases/cowork/UC-04-cab-pack.md)
- [APP-02 Change Calendar and CAB Tracker](../../cowork-apps/APP-02-change-calendar-cab-tracker.md)

---

[Previous: UC-18](../copilot-studio/UC-18-security-alert-triage-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-20](../copilot-studio/UC-20-device-compliance-agent.md)
