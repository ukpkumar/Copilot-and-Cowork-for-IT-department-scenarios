# UC-02: Major incident communications pack

[Previous: UC-01](../cowork/UC-01-daily-it-operations-briefing.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-03](../cowork/UC-03-post-incident-review.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork |
| **Persona** | Major Incident Manager |
| **Reference files** | [Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx](../../reference-files/Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Major_Incident_Log` tab) |
| **Skills and tools** | Communications, Email, Word, Adaptive Cards |
| **Output** | Stakeholder update, executive summary, site notice and service desk script, all as drafts |
| **Value** | Cuts the time to produce each round of P1 communications from 20 to 30 minutes to about 5, and keeps every audience consistent |

## Scenario

During P1 incident INC-24117, Remote Sites A and B lost email and Teams sign-in. Around 1,240 users were affected. The Major Incident Manager has to brief executives, site managers, the service desk and the vendor at the same time, while still running the bridge. Each audience needs different detail, and messages must not contradict each other.

## Before you start

- Upload the bridge notes for INC-24117.
- Optional: attach the workbook so Cowork can read the Major_Incident_Log tab.

## Steps

### Step 1: Generate the first communications round

Ask for all audiences at once so the facts stay consistent.

```text
We have an active P1, INC-24117. Use the attached bridge notes.
Draft the 08:15 communications round for four audiences:
1. Executive update (5 lines): impact, sites, users affected, what we are doing, next update time
2. Site managers at Remote Sites A and B: what users will notice, workarounds, who to call
3. Service desk script: what to tell callers, how to log calls against INC-24117
4. Teams post for the IT Major Incident channel

Use plain language. Do not speculate about the root cause. State the next update time as 09:00.
Create everything as drafts; do not send or post.
```

### Step 2: Update as the incident evolves

Ask for the next round using only the new facts.

```text
It is now 09:45. The vendor confirmed that change CHG-3092 altered DNS forwarder settings and a rollback failed. Update all four messages. Keep the root cause wording as 'a network configuration change, under investigation'.
```

### Step 3: Resolution notice

Close out the incident.

```text
Service was restored at 10:58 and confirmed by the site IT coordinators. Draft the resolution notice for each audience, include the total duration, and say that a post-incident review will follow within 5 working days.
```

### Step 4: Check consistency

Ask Cowork to compare all messages.

```text
Compare every message you drafted today. List any differences in times, numbers or wording between audiences, and correct them.
```

## What good looks like

- [ ] Times (07:42 detection, 10:58 restore) and the 1,240 users figure are consistent across every message.
- [ ] Executive messages are short; site messages give practical workarounds.
- [ ] No message states a confirmed root cause before the bridge agreed it.
- [ ] Everything is created as a draft.

## Try this next

**Adaptive Card for Teams**

```text
Turn the executive update into an Adaptive Card with status, impact, next update time and a link to the incident record.
```

**Vendor escalation**

```text
Draft a formal escalation email to Northwind Networks asking for a written post-implementation review of CHG-3092 within 5 business days, as required by the contract.
```

## Make it repeatable

Use the [incident update skill](../skills-plugins/UC-09-incident-update-skill.md) so every update follows the Contoso format automatically.

## Tips

- Ask for all audiences in one prompt; this keeps the facts aligned.
- Never let a draft leave without a human check during a live incident.
- Record the time of each round in the prompt so Cowork sets the next update time correctly.

## Related

- [UC-03 Post-incident review (PIR) and root cause report](../../use-cases/cowork/UC-03-post-incident-review.md)
- [UC-09 Skill: incident update in the Contoso format](../../use-cases/skills-plugins/UC-09-incident-update-skill.md)
- [APP-01 Major Incident Command Board](../../cowork-apps/APP-01-major-incident-command-board.md)

---

[Previous: UC-01](../cowork/UC-01-daily-it-operations-briefing.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-03](../cowork/UC-03-post-incident-review.md)
