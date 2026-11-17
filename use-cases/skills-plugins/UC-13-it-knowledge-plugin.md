# UC-13: Plugin: IT knowledge and runbook plugin for the service desk

[Previous: UC-12](../skills-plugins/UC-12-itsm-plugin.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-14](../copilot-studio/UC-14-it-service-desk-agent.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork plugin |
| **Persona** | Service Desk Analysts |
| **Reference files** | [Contoso-IT-Service-Desk-Knowledge-Articles.docx](../../reference-files/Contoso-IT-Service-Desk-Knowledge-Articles.docx)<br>[Contoso-IT-Legacy-Runbook-VPN-Certificate-Renewal.docx](../../reference-files/Contoso-IT-Legacy-Runbook-VPN-Certificate-Renewal.docx)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`KB_Index` tab) |
| **Skills and tools** | Plugin `Contoso IT Knowledge` with skills `contoso-kb-article`, `contoso-runbook-standard` and a knowledge connector |
| **Output** | Analysts find and write knowledge in a consistent format; gaps in the knowledge base are found from ticket data |
| **Value** | Higher first-contact resolution; faster creation of knowledge articles from resolved tickets |

## Scenario

Contoso's service desk analysts resolve the same issues repeatedly, but knowledge articles are inconsistent and often missing. The knowledge manager wants analysts to turn resolved tickets into articles in a standard format, and to find gaps.

## Before you start

- Upload the knowledge articles document and the workbook.
- Download the [contoso-kb-article skill](../../skills/contoso-kb-article/SKILL.md).

## Steps

### Step 1: Write an article from a ticket

Use the KB skill.

```text
/contoso-kb-article Create an employee knowledge article from the most recently resolved Printing incident in the attached workbook. Use our KB format.
```

### Step 2: Find knowledge gaps

Compare tickets with the knowledge base.

```text
Compare the Incidents tab with the KB_Index tab. Which recurring issues have no knowledge article? Rank them by number of incidents.
```

### Step 3: Standardise runbooks

Use the runbook skill on legacy material.

```text
/contoso-runbook-standard Rewrite the attached VPN certificate runbook in our template.
```

### Step 4: Package as a plugin

Bundle the two skills with a knowledge connector to the IT knowledge SharePoint site and deploy it to SG-Service-Desk, as in [UC-12](UC-12-itsm-plugin.md).

## What good looks like

- [ ] New articles follow the KB structure: applies to, steps, if this does not work, last updated.
- [ ] Gaps are ranked by incident volume.
- [ ] Runbook steps that were inferred are marked [Confirm].

## Try this next

**Knowledge review**

```text
Every month, list knowledge articles not updated for 12 months and draft a review request to each owner role.
```

**Feed the agent**

```text
Once the knowledge manager approves these new articles, save them as Word files in the IT knowledge SharePoint library used by the service desk agent.
```

## Make it repeatable

This plugin feeds the knowledge used by the Copilot Studio service desk agent.

## Tips

- One well-structured SharePoint library improves Cowork, agents and search at the same time.
- Require knowledge manager approval before publishing new articles.

## Related

- [UC-06 Runbook and SOP authoring from existing material](../../use-cases/cowork/UC-06-runbook-and-sop-authoring.md)
- [UC-14 IT service desk agent](../../use-cases/copilot-studio/UC-14-it-service-desk-agent.md)

---

[Previous: UC-12](../skills-plugins/UC-12-itsm-plugin.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-14](../copilot-studio/UC-14-it-service-desk-agent.md)
