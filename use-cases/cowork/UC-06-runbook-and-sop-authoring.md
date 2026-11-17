# UC-06: Runbook and SOP authoring from existing material

[Previous: UC-05](../cowork/UC-05-license-optimisation.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-07](../cowork/UC-07-vendor-sla-review.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork |
| **Persona** | Platform Engineer |
| **Reference files** | [Contoso-IT-Legacy-Runbook-VPN-Certificate-Renewal.docx](../../reference-files/Contoso-IT-Legacy-Runbook-VPN-Certificate-Renewal.docx) |
| **Skills and tools** | Word, Enterprise Search |
| **Output** | A runbook in the Contoso standard template, with validation and rollback steps |
| **Value** | Brings legacy runbooks to standard in minutes; improves first-time-right execution during changes |

## Scenario

Many of Contoso's runbooks are old, inconsistent and missing validation and rollback steps. The VPN gateway certificate expires on 15 December 2026, and the current runbook is a set of long paragraphs that refer to an old wiki.

## Before you start

- Upload the legacy runbook. Its last section contains the Contoso Standard Runbook Template.

## Steps

### Step 1: Assess the legacy runbook

Ask for a gap analysis first.

```text
Review the attached legacy VPN certificate renewal runbook against the Contoso Standard Runbook Template at the end of the document. List every missing section, unclear step and outdated reference.
```

### Step 2: Rewrite it

Generate the new version.

```text
Rewrite the runbook into the Contoso Standard Runbook Template in Word.
- Number every procedure step and give each an expected result
- Add pre-checks, validation and rollback sections
- Add a communications section (who to notify before and after)
- Replace references to the old wiki with [Link to current knowledge article]
- Mark any step you had to infer with [Confirm]
```

### Step 3: Plan the renewal

Use the runbook to plan the actual work.

```text
The certificate expires on 15 December 2026 and must be renewed 30 days before expiry. Propose a change window, draft the change request text, and list the people to notify.
```

## What good looks like

- [ ] All template headings are present.
- [ ] Validation and rollback steps exist and are specific.
- [ ] Inferred steps are marked [Confirm] for the engineer to check.
- [ ] The renewal date (15 November 2026, 30 days before expiry) is identified, and Cowork flags that it has already passed, so the change is urgent.

## Try this next

**Bulk standardisation**

```text
Here are five more legacy runbooks. Convert each to the standard template and give me a table of gaps found per runbook.
```

**Quick reference card**

```text
Create a one-page quick reference card for night-shift engineers from the new runbook.
```

## Make it repeatable

Create a `contoso-runbook-standard` skill that always applies the template and the [Confirm] rule.

## Tips

- Never let an inferred step reach production without an engineer's check.
- Store runbooks in one SharePoint library so Cowork and agents can find them.

## Related

- [UC-13 Plugin: IT knowledge and runbook plugin for the service desk](../../use-cases/skills-plugins/UC-13-it-knowledge-plugin.md)
- [UC-14 IT service desk agent](../../use-cases/copilot-studio/UC-14-it-service-desk-agent.md)

---

[Previous: UC-05](../cowork/UC-05-license-optimisation.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-07](../cowork/UC-07-vendor-sla-review.md)
