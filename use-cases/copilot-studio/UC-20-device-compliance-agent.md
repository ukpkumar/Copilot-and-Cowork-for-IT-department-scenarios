# UC-20: Device and endpoint compliance agent for remote sites

[Previous: UC-19](../copilot-studio/UC-19-change-notification-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md)

## At a glance

| | |
|---|---|
| **Workload** | Copilot Studio agent (autonomous + conversational) |
| **Persona** | Endpoint team; site IT coordinators |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Devices` tab) |
| **Skills and tools** | Device data (Intune via connector or Microsoft Graph), recurrence trigger, Teams, ITSM |
| **Output** | A daily compliance check, messages to device users and site coordinators, and tickets for devices that stay non-compliant |
| **Value** | Raises device compliance at remote sites, where devices often miss updates because of limited connectivity |

## Scenario

Remote Site C has eight non-compliant devices: outdated OS or no check-in for more than 14 days. Site IT coordinators find out only during audits.

## Before you start

- Read access to device compliance data.
- A Teams channel per site for IT coordinators.

## Steps

### Step 1: Create the agent

Describe it.

```text
Create a device compliance agent. Every morning it checks devices that are
non-compliant or have not checked in for 14 days. It messages each device's user
with simple steps to fix it, sends each site IT coordinator a list for their site,
and creates a ticket for devices still non-compliant after 3 days.
Users can also ask it: 'Is my laptop compliant?' and get the reason and the fix.
```

### Step 2: Add trigger and tools

Add a recurrence trigger, a device lookup tool, Teams messaging and ITSM *Create incident*.

### Step 3: Test

Ask a site question.

```text
Which devices at Remote Site C are non-compliant and why?
```

## What good looks like

- [ ] The 8 non-compliant devices at Remote Site C are listed with the reason.
- [ ] Users get plain-language fix steps.
- [ ] Tickets are created only after the grace period.

## Try this next

**Patch window planning**

```text
Suggest the best patch window per site based on check-in patterns.
```

**Executive view**

```text
Every month, produce a compliance trend by site for the Head of IT.
```

## Make it repeatable

Provide endpoint context to the [security triage assistant](UC-18-security-alert-triage-agent.md).

## Tips

- Respect site shift patterns when messaging users.
- Use roles, not names, in site summaries shared in channels.

## Related

- [UC-18 Security alert triage assistant](../../use-cases/copilot-studio/UC-18-security-alert-triage-agent.md)
- [APP-03 Software Licence and Asset Tracker](../../cowork-apps/APP-03-licence-and-asset-tracker.md)

---

[Previous: UC-19](../copilot-studio/UC-19-change-notification-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md)
