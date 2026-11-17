# UC-16: Joiner, mover, leaver (JML) IT agent

[Previous: UC-15](../copilot-studio/UC-15-access-request-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-17](../copilot-studio/UC-17-software-request-agent.md)

## At a glance

| | |
|---|---|
| **Workload** | Copilot Studio autonomous agent |
| **Persona** | Identity and Access team |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Access_Review` tab)<br>[Contoso-IT-Service-Desk-Knowledge-Articles.docx](../../reference-files/Contoso-IT-Service-Desk-Knowledge-Articles.docx) |
| **Skills and tools** | Event trigger (HR record), Entra ID, ITSM, Intune, Teams, Outlook |
| **Output** | IT tasks for new joiners, movers and leavers created and tracked automatically, with a checklist message to the manager |
| **Value** | No orphaned accounts after leavers; new joiners productive on day one; fewer audit findings |

## Scenario

The Q4 access review found five leavers who still had access. New joiners at remote sites often wait days for a laptop and accounts. Contoso wants an agent that reacts to HR events and coordinates the IT tasks.

## Before you start

- An HR event source (for example, a SharePoint list or an HR system connector) that the agent can trigger on.
- Standard task templates for joiner, mover and leaver.

## Steps

### Step 1: Create the autonomous agent

Describe it.

```text
Create an agent that runs when an HR event (joiner, mover or leaver) is recorded.
For a joiner: create the IT onboarding tasks (account, licence, laptop, access groups by role),
and send the line manager the new-joiner checklist in Teams.
For a mover: list access to remove and add, and request approvals.
For a leaver: disable sign-in on the last working day, remove group memberships,
reclaim licences, and create a device return task.
Log every action in ITSM. Ask a human for approval before removing access for movers.
```

### Step 2: Add the trigger

Under **Triggers**, add *When an item is created* on the HR events list (or the HR connector trigger).

### Step 3: Add tools

Add ITSM *Create task*, Entra ID group actions, Teams *Post message* and Outlook *Send email* tools.

### Step 4: Test

Create test HR events for each type in the test environment and follow the activity map.

## What good looks like

- [ ] Each event type creates the right tasks.
- [ ] Leaver sign-in is disabled on the last working day, not before.
- [ ] Mover access changes wait for approval.
- [ ] Every action is logged against the HR event.

## Try this next

**Leaver sweep**

```text
Every Monday, compare HR leavers with active accounts and report any mismatch.
```

**Joiner welcome**

```text
Send the joiner a welcome message on day one with the top five knowledge articles.
```

## Make it repeatable

Use the agent's logs as evidence for control A.5.15 in [UC-08](../cowork/UC-08-audit-evidence-pack.md).

## Tips

- Start in a test environment with test accounts only.
- Keep human approval for destructive actions until the agent is proven.

## Related

- [UC-15 Access request and approval agent](../../use-cases/copilot-studio/UC-15-access-request-agent.md)
- [UC-08 Security audit evidence pack](../../use-cases/cowork/UC-08-audit-evidence-pack.md)
- [APP-04 Access Review Campaign Tracker](../../cowork-apps/APP-04-access-review-tracker.md)

---

[Previous: UC-15](../copilot-studio/UC-15-access-request-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-17](../copilot-studio/UC-17-software-request-agent.md)
