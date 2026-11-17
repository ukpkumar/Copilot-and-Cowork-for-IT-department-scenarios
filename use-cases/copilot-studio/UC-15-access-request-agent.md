# UC-15: Access request and approval agent

[Previous: UC-14](../copilot-studio/UC-14-it-service-desk-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-16](../copilot-studio/UC-16-joiner-mover-leaver-agent.md)

## At a glance

| | |
|---|---|
| **Workload** | Copilot Studio agent + agent flow |
| **Persona** | Employees; Identity and Access team |
| **Reference files** | [Contoso-IT-Service-Desk-Knowledge-Articles.docx](../../reference-files/Contoso-IT-Service-Desk-Knowledge-Articles.docx)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Access_Review` tab) |
| **Skills and tools** | Agent flow with approvals, Microsoft Entra ID group connector, ITSM connector |
| **Output** | Employees request application access in chat; line manager and application owner approve; access is granted through group membership and logged |
| **Value** | Request-to-access time drops from days to hours; every grant has an approval trail for audit |

## Scenario

Access to applications such as the Finance ERP, the HR Portal and the OT Jump Host is requested by email today. Approvals get lost, access is granted without a record, and auditors find gaps. Contoso wants one conversational front door with approvals and an audit trail.

## Before you start

- A list of requestable applications with their Entra ID access groups and owners.
- Approval rules: line manager for all, plus application owner for sensitive apps (Finance ERP, OT Jump Host).

## Steps

### Step 1: Create the agent

Describe it.

```text
Create an access request agent. Employees ask for access to an application.
The agent confirms the application and access level from the catalogue,
asks for the business reason, and starts the approval flow.
It tells the user the request number and who must approve.
It never grants access itself without approval.
```

### Step 2: Build the agent flow

Create an agent flow named *Access request*: inputs (user, application, access level, reason) → look up owner and group → **approval** from the line manager → if sensitive, **approval** from the application owner → add the user to the Entra ID group → create a fulfilled request in ITSM → return the result to the agent.

### Step 3: Add the flow as a tool

Add the agent flow under **Tools**, and add a *Get my access requests* tool for status questions.

### Step 4: Test

Run through the flow.

```text
I need read access to the Finance ERP for the month-end close.
```

### Step 5: Govern

Use connector action control to allow only *Add member to group* on the approved groups, and review the agent's Entra Agent ID permissions after publishing.

## What good looks like

- [ ] Sensitive applications require two approvals.
- [ ] No access is granted before approval.
- [ ] The request, approvals and grant are recorded with timestamps.
- [ ] The user always receives a request number.

## Try this next

**Time-bound access**

```text
Add an end date for OT Jump Host access and a flow that removes access automatically on that date.
```

**Access review link**

```text
Every day, add newly approved access grants as review items in the Access Review Tracker app, so they are included in the next quarterly review.
```

## Make it repeatable

Reuse the agent flow for software requests in [UC-17](UC-17-software-request-agent.md).

## Tips

- Least privilege: the flow's connection should only manage the groups in the catalogue.
- Keep the application catalogue in a SharePoint list that owners maintain.

## Related

- [UC-16 Joiner, mover, leaver (JML) IT agent](../../use-cases/copilot-studio/UC-16-joiner-mover-leaver-agent.md)
- [APP-04 Access Review Campaign Tracker](../../cowork-apps/APP-04-access-review-tracker.md)

---

[Previous: UC-14](../copilot-studio/UC-14-it-service-desk-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-16](../copilot-studio/UC-16-joiner-mover-leaver-agent.md)
