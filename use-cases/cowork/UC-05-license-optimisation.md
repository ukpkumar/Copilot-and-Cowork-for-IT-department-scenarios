# UC-05: Microsoft 365 licence optimisation

[Previous: UC-04](../cowork/UC-04-cab-pack.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-06](../cowork/UC-06-runbook-and-sop-authoring.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork |
| **Persona** | Microsoft 365 Platform Owner |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Licences` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Licence_Usage` tab) |
| **Skills and tools** | Excel, PowerPoint, Word |
| **Output** | Licence analysis workbook, savings deck and reclaim communication drafts |
| **Value** | Identifies reclaimable licences and their annual value in one session instead of a week of spreadsheet work |

## Scenario

Contoso's licence renewal is approaching. The Microsoft 365 Platform Owner needs to know which licences are unused or duplicated, the annual saving, and a safe plan to reclaim them, including which Microsoft 365 Copilot licences should be reassigned to active users.

## Before you start

- Attach the workbook, or in your own tenant export licence assignment and activity reports from the Microsoft 365 admin center.

## Steps

### Step 1: Analyse usage

Start with the numbers.

```text
Using the Licences and Licence_Usage tabs, calculate for each product:
assigned, active in the last 30 days, inactive 30 to 60 days, inactive over 60 days,
inactive %, and potential annual saving in AED (inactive over 60 days x unit cost x 12).
Rank the products by potential saving. Show the formulas you used.
```

### Step 2: Find duplication

Look for overlapping tools.

```text
Identify products that duplicate capabilities we already own in Microsoft 365 (for example, meetings, PDF editing or diagramming) and estimate the saving if we retire them at renewal.
```

### Step 3: Copilot licences

Focus on Copilot.

```text
For Microsoft 365 Copilot, list how many licences are inactive for 30 days or more and propose a reassignment process: notify, wait 14 days, reclaim, reassign to the waiting list.
```

### Step 4: Build the savings pack

Create the outputs for the decision.

```text
Create a 5-slide deck for the IT Leadership Team with the total potential saving, top opportunities, risks, and a 90-day reclaim plan. Also draft the user notification email for inactive licence holders (draft only).
```

## What good looks like

- [ ] Microsoft 365 E5 shows 214 licences inactive for more than 60 days.
- [ ] 61 Microsoft 365 Copilot licences are identified for reassignment.
- [ ] Visio, Project and Zoom opportunities are listed with annual values.
- [ ] Every saving figure is a formula you can check.

## Try this next

**Renewal negotiation brief**

```text
Prepare a one-page negotiation brief for the licence renewal with the true-down quantities and the evidence.
```

**Monthly check**

```text
Schedule this analysis on the first working day of each month and show me only the changes since last month.
```

## Make it repeatable

Use the [Licence and Asset Tracker app](../../cowork-apps/APP-03-licence-and-asset-tracker.md) to track reclaim actions.

## Tips

- Agree a grace period and a communication before reclaiming any licence.
- Exclude shared, service and break-glass accounts from reclaim lists.

## Related

- [APP-03 Software Licence and Asset Tracker](../../cowork-apps/APP-03-licence-and-asset-tracker.md)
- [UC-17 Software request and licence entitlement agent](../../use-cases/copilot-studio/UC-17-software-request-agent.md)

---

[Previous: UC-04](../cowork/UC-04-cab-pack.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-06](../cowork/UC-06-runbook-and-sop-authoring.md)
