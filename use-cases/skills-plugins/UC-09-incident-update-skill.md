# UC-09: Skill: incident update in the Contoso format

[Previous: UC-08](../cowork/UC-08-audit-evidence-pack.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-10](../skills-plugins/UC-10-change-request-review-skill.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork skill |
| **Persona** | Service Desk Lead |
| **Reference files** | [Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx](../../reference-files/Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx) |
| **Skills and tools** | Custom skill `contoso-incident-update` + Communications, Email |
| **Output** | P1/P2 updates in the same structure every time, for each audience, as drafts |
| **Value** | Every analyst produces executive-ready updates in the agreed format; no more rewriting by the Major Incident Manager |

## Scenario

Different analysts write incident updates in different ways. Some omit the next update time, some speculate about root cause, and executives complain about inconsistent messages. Contoso wants one format, enforced every time.

## Before you start

- Download [contoso-incident-update/SKILL.md](../../skills/contoso-incident-update/SKILL.md).
- Upload the bridge notes for testing.

## Steps

### Step 1: Upload the skill

Add it to Cowork.

```text
In Cowork, open **Customize**, filter by **Skills**, select **Add > Upload** and choose `SKILL.md`. Alternatively select **Add > New skill** and paste the content.
```

### Step 2: Test explicitly

Start a new conversation, type `/`, choose the skill, and run it.

```text
/contoso-incident-update Use the attached bridge notes. Write the 09:00 update for INC-24117 for executives and for the service desk.
```

### Step 3: Test automatic selection

Check that Cowork picks it up from a natural request.

```text
Give me a status update on the remote sites sign-in outage for the leadership team.
```

### Step 4: Share with the team

On the skill's detail page select **Share > Specific users in your organization** and add the service desk leads group. After any change, select **Re-share**.

## What good looks like

- [ ] Each update has: status, impact, sites, users affected, actions in progress, workaround, next update time.
- [ ] Root cause is stated only if the bridge confirmed it.
- [ ] Times are in Gulf Standard Time (GST).
- [ ] Output is a draft; nothing is sent.

## Try this next

**Add an audience**

```text
Edit the skill to add a 'Remote site radio announcement' format of no more than 40 words.
```

**Pair with an event trigger**

```text
When an email with subject starting 'P1 –' arrives from the monitoring system, use contoso-incident-update to draft the first executive notice for my review.
```

## Make it repeatable

Package this skill with UC-10 and UC-11 in the [IT service management plugin](UC-12-itsm-plugin.md).

## Tips

- Give skills distinctive names (prefix `contoso-`) so they do not clash with built-in skills.
- Test changes in a new conversation; skills load at the start of a session.

## Related

- [UC-02 Major incident communications pack](../../use-cases/cowork/UC-02-major-incident-communications.md)
- [UC-12 Plugin: IT service management (ITSM) plugin](../../use-cases/skills-plugins/UC-12-itsm-plugin.md)
- [Lab 2](../../labs/lab-02-create-and-share-a-skill.md)

---

[Previous: UC-08](../cowork/UC-08-audit-evidence-pack.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-10](../skills-plugins/UC-10-change-request-review-skill.md)
