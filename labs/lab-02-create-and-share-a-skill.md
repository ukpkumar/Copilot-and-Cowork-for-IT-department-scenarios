# Lab 2: Create, test and share an IT skill

[Previous: Lab 1](lab-01-cowork-cab-pack.md) | [Labs](README.md) | [Home](../README.md) | Next: [Lab 3](lab-03-scheduled-ops-briefing.md)

**Use case:** [UC-09 Incident update skill](../use-cases/skills-plugins/UC-09-incident-update-skill.md)
**Reference file:** [Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx](../reference-files/Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx)

## Scenario

You lead the service desk. Analysts write incident updates in different ways. You will capture the Contoso format as a skill, test it and share it.

## Option A: Create the skill in conversation

```text
Create a new skill called contoso-incident-update.
It writes P1 and P2 incident updates for executives, site managers, the service desk and Teams.
Rules:
- Subject line format: [P1] <Service> – <Status> – Update <n> – <time> GST
- Include impact, sites, users affected, current action, workaround and next update time
- Never state a root cause until the bridge confirms it; use "under investigation"
- Use roles, never names; plain language for sites
- Always create drafts; never send or post
Include a short example of an executive update.
```

## Option B: Upload the ready-made skill

1. Download [contoso-incident-update/SKILL.md](../skills/contoso-incident-update/SKILL.md).
2. In Cowork, open **Customize**, filter by **Skills**, select **Add > Upload** and choose the file.

## Task 1: Test it explicitly

Start a **new conversation** (skills load at the start of a session), attach the bridge notes, type `/` and select the skill:

```text
/contoso-incident-update Write update 3 at 09:45 for INC-24117 for executives and site managers.
```

## Task 2: Test automatic selection

New conversation, attach the bridge notes:

```text
Give the leadership team a status update on the remote sites sign-in outage as of 10:30.
```

Check the side panel: the skill should show as active.

## Task 3: Improve the skill

Open the skill from **Customize** and add a rule, for example: "Add a 'Radio announcement' format for remote sites of no more than 40 words." Test again in a new conversation.

## Task 4: Share it

Open the skill, select **Share > Specific users in your organization**, and add a colleague. After any later change, select **Re-share**.

## What good looks like

- [ ] The skill appears in your skills list with a clear description.
- [ ] Updates follow the subject format and include the next update time.
- [ ] No root cause is stated before 08:40 in the bridge notes.
- [ ] Output is draft only.
- [ ] A colleague can see and use the shared skill.
