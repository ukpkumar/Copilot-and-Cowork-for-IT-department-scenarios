# UC-12: Plugin: IT service management (ITSM) plugin

[Previous: UC-11](../skills-plugins/UC-11-weekly-service-report-skill.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-13](../skills-plugins/UC-13-it-knowledge-plugin.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork plugin (skills + connector) |
| **Persona** | IT Operations and Service Desk |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Incidents` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Changes` tab) |
| **Skills and tools** | Plugin `Contoso IT Service Management` with skills from UC-09, UC-10, UC-11 and an ITSM connector |
| **Output** | The whole IT operations team gets the same skills and live access to tickets and changes inside Cowork |
| **Value** | Moves skills from individual use to a governed team capability, with live ITSM data instead of exports |

## Scenario

Individual skills work well, but each analyst uploads them separately and still works from exports. Contoso wants one package, deployed by IT admins to the operations and service desk groups, that also connects Cowork to the ITSM system so that prompts use live incidents and changes.

## Before you start

- You need an admin role (Copilot administrator, AI administrator or Global administrator) to deploy plugins.
- Your ITSM system needs a connector or an MCP server that Cowork can use, approved by your security team.

## Steps

### Step 1: Design the plugin

Define the contents before building.

```text
Plugin: Contoso IT Service Management
Skills:
- contoso-incident-update       (UC-09)
- contoso-change-review         (UC-10)
- contoso-weekly-service-report (UC-11)
- contoso-pir-writer            (UC-03)
Connector:
- ITSM connector (read incidents, problems, changes; create work notes)
Audience: SG-IT-Operations, SG-Service-Desk
Owner: IT Service Management process owner
```

### Step 2: Build and package

Use Plugin Builder, the Microsoft 365 Agents Toolkit or Work IQ developer tools to create a Microsoft 365 app package (`manifest.json` declaring the skills and connectors). Validate it. See *Build plugins for Copilot Cowork* in the [references](../../appendix/references.md).

### Step 3: Upload and deploy

In the Microsoft 365 admin center, go to **Agents > Tools > Registry > Upload**. Then open the plugin, select **Installed for > Specific users/groups**, and add the IT groups.

### Step 4: Use it

Users see the plugin in **Added** plugins, labelled **Managed by your organization**. Each user signs in to the ITSM connector the first time.

```text
Show me all open P1 and P2 incidents at the remote sites from the ITSM system and draft the 09:00 update using our incident format.
```

### Step 5: Monitor

Review usage in the Microsoft Purview audit log under **Copilot activities**, and update the plugin when skills change.

## What good looks like

- [ ] The plugin appears automatically for users in the target groups.
- [ ] Skills activate from natural requests and show in the side panel.
- [ ] ITSM data comes live from the connector, within each user's permissions.
- [ ] Plugin version and owner are recorded in the IT plugin catalogue.

## Try this next

**Write-back**

```text
Add a skill that writes the agreed incident update as a work note on the ticket, with approval before writing.
```

**Problem management**

```text
Add a skill that finds recurring incidents and proposes problem records.
```

## Make it repeatable

Keep the skill source files in this repository and version the plugin package.

## Tips

- Deploy to IT groups first; widen only after testing.
- Users must complete connector sign-in themselves; admins cannot do it for them.
- Check current limitations, such as Information Barriers support, before deployment.

## Related

- [UC-09 Skill: incident update in the Contoso format](../../use-cases/skills-plugins/UC-09-incident-update-skill.md)
- [UC-10 Skill: change request quality review](../../use-cases/skills-plugins/UC-10-change-request-review-skill.md)
- [UC-11 Skill: weekly IT service report on a schedule](../../use-cases/skills-plugins/UC-11-weekly-service-report-skill.md)
- [UC-13 Plugin: IT knowledge and runbook plugin for the service desk](../../use-cases/skills-plugins/UC-13-it-knowledge-plugin.md)

---

[Previous: UC-11](../skills-plugins/UC-11-weekly-service-report-skill.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-13](../skills-plugins/UC-13-it-knowledge-plugin.md)
