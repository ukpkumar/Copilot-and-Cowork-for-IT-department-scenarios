# Module 3: Skills and plugins

[Previous: Module 2](02-cowork-for-it.md) | [Home](../README.md) | Next: [Module 4: Cowork apps](04-cowork-apps.md)

## Learning objectives

- Write, test, share and maintain a Cowork skill for an IT process.
- Understand how a plugin packages skills and connectors.
- Plan how admins deploy and govern plugins.

---

## 3.1 What makes a good skill

A skill turns "how our team does it" into instructions that Cowork follows every time.

| Good skills are... | Example |
|--------------------|---------|
| **Specific** to one task | "Write a P1/P2 incident update", not "Help with incidents" |
| **Clear about triggers** | The description says when to use it: "Use when asked for an incident update, status update or outage communication" |
| **Explicit about format** | Headings, length, tone, mandatory fields, time zone |
| **Explicit about rules** | "Never state a root cause until the problem record confirms it" |
| **Safe** | "Create drafts only; never send" |
| **Testable** | Includes a short example of good output |

## 3.2 Skill file structure

Skills use the open Agent Skills format: a folder containing a `SKILL.md` file.

```markdown
---
name: incident-update
description: Writes Contoso P1 and P2 incident status updates in the standard
  format. Use when the user asks for an incident update, outage communication,
  status update or major incident notice.
---

# Incident update

## When to use
...

## Inputs to gather
...

## Steps
1. ...

## Output format
...

## Rules
- ...

## Example
...
```

Ready-to-use skill files are in [skills/](../skills/).

## 3.3 Create, test and share a skill in Cowork

1. In Cowork, open **Customize** (or **Plugins**) and filter by **Skills**.
2. Select **Add > New skill** to create one in a guided conversation, or **Add > Upload** to import a `SKILL.md` file.
3. **Test** it in a **new conversation** (Cowork discovers skills at the start of each session). Trigger it explicitly by typing `/` and selecting it, then test that it is picked up automatically from a natural request.
4. **Refine.** Open the skill's detail page to edit the instructions. You can also open the file in OneDrive.
5. **Share.** On the skill's detail page select **Share** and choose **Specific users in your organization**. After changes, select **Re-share**.

Limits and notes:

- Each user can create up to 50 custom skills.
- If a plugin skill has the same name as a built-in skill, Cowork decides which to use, so give your skills distinctive names (for example, prefix with `contoso-`).

## 3.4 Skill lifecycle for an IT team

| Stage | Owner | Activity |
|-------|-------|----------|
| Draft | Process owner | Write the skill from the current SOP or template |
| Test | Two or three users | Run against five real (sanitised) cases; record issues |
| Approve | Team lead | Confirm format, rules and safety statements |
| Share | Process owner | Share with the team, or package into a plugin |
| Maintain | Process owner | Review each quarter or when the process changes; re-share |

Store the master copy of each team skill in a version-controlled location (for example, this repository) and record the version in the skill description.

## 3.5 Plugins

A **plugin** packages **skills** and **connectors** so that a whole team gets the same capability.

| Component | What it adds | IT example |
|-----------|--------------|------------|
| Skills | Expertise and process | Incident update, change review, PIR writer |
| Connectors | Access to systems outside Microsoft 365 | IT service management (ITSM) system, CMDB, monitoring tool, via connectors or MCP servers |

### How plugins are built

- Plugins use the **Microsoft 365 app package format** (the same family as Teams apps and Copilot agents), with a manifest that declares skills and connectors. See *Build plugins for Copilot Cowork* in the [references](../appendix/references.md).
- Authoring and packaging tools include Plugin Builder, the Microsoft 365 Agents Toolkit and Work IQ developer tools.
- Plugins that link to MCP servers need **admin consent**.

### How plugins are deployed and governed

| Task | Where |
|------|-------|
| Upload an organizational plugin | Microsoft 365 admin center > **Agents > Tools > Registry > Upload** |
| Deploy to all users or to specific users and groups | Microsoft 365 admin center > **Agents > Tools** (or **All agents**) > select plugin > **Installed for** |
| Control which plugins and publishers are allowed | Microsoft 365 admin center > **Agents > Settings > Agent and plugin access** |
| Audit usage | Microsoft Purview audit log > **Copilot activities** |

User experience after deployment:

- Admin-deployed plugins appear automatically in the user's **Added** plugins with a **Managed by your organization** label.
- Users can turn a plugin on or off for their conversations.
- Each user completes sign-in or consent for a connector the first time. Admins cannot sign in on behalf of users.

> Check current limitations before you plan, for example: Microsoft Purview Information Barriers are not currently supported for plugin and skill management and sharing.

## 3.6 Use cases in this module

| ID | Use case | Type |
|----|----------|------|
| [UC-09](../use-cases/skills-plugins/UC-09-incident-update-skill.md) | Incident update in the Contoso format | Skill |
| [UC-10](../use-cases/skills-plugins/UC-10-change-request-review-skill.md) | Change request quality review | Skill |
| [UC-11](../use-cases/skills-plugins/UC-11-weekly-service-report-skill.md) | Weekly IT service report on a schedule | Skill + scheduled task |
| [UC-12](../use-cases/skills-plugins/UC-12-itsm-plugin.md) | IT service management plugin | Plugin |
| [UC-13](../use-cases/skills-plugins/UC-13-it-knowledge-plugin.md) | IT knowledge and runbook plugin | Plugin |

[Previous: Module 2](02-cowork-for-it.md) | [Home](../README.md) | Next: [Module 4: Cowork apps](04-cowork-apps.md)
