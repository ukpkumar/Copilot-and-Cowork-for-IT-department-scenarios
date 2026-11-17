# UC-17: Software request and licence entitlement agent

[Previous: UC-16](../copilot-studio/UC-16-joiner-mover-leaver-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-18](../copilot-studio/UC-18-security-alert-triage-agent.md)

## At a glance

| | |
|---|---|
| **Workload** | Copilot Studio agent + agent flow |
| **Persona** | Employees; Software Asset Manager |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Licences` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Licence_Usage` tab) |
| **Skills and tools** | Software catalogue knowledge, licence data, approval flow, Intune deployment request |
| **Output** | Employees request software in chat; the agent checks the catalogue and licence availability, suggests approved alternatives and routes approvals |
| **Value** | Avoids buying licences when free capacity or an approved alternative exists; faster fulfilment |

## Scenario

Employees request software by email. Licences are bought even when unused licences exist, and requests for tools that duplicate Microsoft 365 capabilities are approved without challenge.

## Before you start

- A software catalogue (approved, restricted, not approved) with alternatives.
- Licence availability data (the Licences tab simulates this).

## Steps

### Step 1: Create the agent

Describe it.

```text
Create a software request agent. When an employee asks for software:
1. Check the software catalogue: approved, restricted or not approved.
2. Suggest an approved alternative if one exists (for example, Teams instead of Zoom).
3. Check licence availability. If a free licence exists, assign it after manager approval.
4. If no licence exists, create a purchase request for the Software Asset Manager.
Always give the request number.
```

### Step 2: Add tools

Add the catalogue as knowledge, a licence availability lookup, the approval agent flow (reuse from UC-15) and an ITSM request action.

### Step 3: Test

Try common requests.

```text
I need Visio for a network diagram.
```

## What good looks like

- [ ] For Visio, the agent finds free licences (purchased minus assigned) and routes manager approval.
- [ ] For Zoom, the agent suggests Teams first.
- [ ] Restricted software goes to the Software Asset Manager.

## Try this next

**Reclaim prompt**

```text
When a licence is not used for 60 days, message the user and offer to remove it.
```

**Self-service install**

```text
After approval, request deployment through Intune and tell the user when it is ready.
```

## Make it repeatable

Feed outcomes into the [Licence and Asset Tracker](../../cowork-apps/APP-03-licence-and-asset-tracker.md).

## Tips

- Keep the catalogue current; the agent is only as good as the catalogue.

## Related

- [UC-05 Microsoft 365 licence optimisation](../../use-cases/cowork/UC-05-license-optimisation.md)
- [UC-15 Access request and approval agent](../../use-cases/copilot-studio/UC-15-access-request-agent.md)
- [APP-03 Software Licence and Asset Tracker](../../cowork-apps/APP-03-licence-and-asset-tracker.md)

---

[Previous: UC-16](../copilot-studio/UC-16-joiner-mover-leaver-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-18](../copilot-studio/UC-18-security-alert-triage-agent.md)
