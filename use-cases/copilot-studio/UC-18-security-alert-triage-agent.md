# UC-18: Security alert triage assistant

[Previous: UC-17](../copilot-studio/UC-17-software-request-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-19](../copilot-studio/UC-19-change-notification-agent.md)

## At a glance

| | |
|---|---|
| **Workload** | Copilot Studio agent |
| **Persona** | SOC analysts |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Incidents` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Devices` tab) |
| **Skills and tools** | Security data via approved connectors or MCP, device lookup, ITSM, Teams |
| **Output** | For each alert, an enriched summary: affected user and device, related incidents, recommended next steps and a draft ticket |
| **Value** | Reduces time to triage; analysts focus on investigation instead of collecting context |

## Scenario

Contoso's managed SOC sends alerts to the internal security team. Analysts spend most of their time collecting context: who the user is, whether the device is compliant, whether there are related incidents.

## Before you start

- Approved, read-only access to security alert data through a connector or MCP server.
- Device data (simulated by the Devices tab).

## Steps

### Step 1: Create the agent

Describe it.

```text
Create a security triage assistant for SOC analysts. Given an alert ID or
alert details, it gathers: user role and site, device compliance and last check-in,
related incidents in the last 7 days, and similar past alerts.
It proposes a severity and next steps from the SOC playbook, and drafts the ITSM
security incident. It never takes containment actions itself; it recommends them.
```

### Step 2: Add knowledge and tools

Add the SOC playbooks as knowledge and read-only tools for alerts, devices and incidents.

### Step 3: Restrict access

Share only with the SOC security group and require authentication.

### Step 4: Test

Use a sample alert.

```text
Alert: suspicious sign-in for device CTS-LT-0031 at Remote Site C. Triage it.
```

## What good looks like

- [ ] The summary includes the device's compliance status and days since check-in.
- [ ] Next steps reference the playbook.
- [ ] No containment action is taken by the agent.

## Try this next

**Shift handover**

```text
At 07:00 and 19:00, summarise open alerts and their status for the incoming shift.
```

**Phishing reports**

```text
Triage emails reported through the 'Report phishing' process and draft responses to reporters.
```

## Make it repeatable

Combine with the [device compliance agent](UC-20-device-compliance-agent.md) for endpoint context.

## Tips

- Read-only first; add actions only with approval steps and strict scoping.
- Security agents must be available only to security staff.

## Related

- [UC-20 Device and endpoint compliance agent for remote sites](../../use-cases/copilot-studio/UC-20-device-compliance-agent.md)

---

[Previous: UC-17](../copilot-studio/UC-17-software-request-agent.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-19](../copilot-studio/UC-19-change-notification-agent.md)
