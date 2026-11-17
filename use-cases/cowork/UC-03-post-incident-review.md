# UC-03: Post-incident review (PIR) and root cause report

[Previous: UC-02](../cowork/UC-02-major-incident-communications.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-04](../cowork/UC-04-cab-pack.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork |
| **Persona** | Problem Manager |
| **Reference files** | [Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx](../../reference-files/Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Major_Incident_Log` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Changes` tab)<br>[Contoso-IT-Managed-Network-Services-SLA-Schedule.pdf](../../reference-files/Contoso-IT-Managed-Network-Services-SLA-Schedule.pdf) |
| **Skills and tools** | Word, Excel, Enterprise Search, Meetings |
| **Output** | A complete PIR report in Word, an action register in Excel and a 5-slide summary for leadership |
| **Value** | A PIR that usually takes 1 to 2 days to compile is drafted in under an hour, with a traceable timeline |

## Scenario

After INC-24117, Contoso's Problem Manager must publish a post-incident review within five working days. The facts are spread across messy bridge notes, the incident log, the change record for emergency change CHG-3092 and the vendor contract. The review must be blameless, factual and lead to owned actions.

## Before you start

- Upload the bridge notes, the workbook and the SLA schedule PDF.
- In your own tenant you can also point Cowork to the bridge meeting recording or transcript.

## Steps

### Step 1: Build the timeline

Start with facts only.

```text
Build a minute-by-minute timeline of INC-24117 from the attached bridge notes and
the Major_Incident_Log tab. Columns: time, event, source, owner role.
Flag any time where the two sources disagree. Calculate time to detect,
time to declare, time to restore and total duration.
```

### Step 2: Draft the PIR

Ask for the full report in your standard structure.

```text
Write a blameless post-incident review in Word with these sections:
Summary; Impact (users, sites, services, operational impact);
Timeline; Detection; Response; Root cause (use a 5 Whys analysis);
Contributing factors; What went well; What did not go well;
Actions (owner role, due date, priority); Appendix: sources.

Use the Changes tab for CHG-3092 and the SLA schedule for the vendor's
change management obligations. Mark anything that is inferred rather than stated.
```

### Step 3: Create the action register

Turn the actions into a trackable list.

```text
Create an Excel action register from the PIR actions with columns: Action ID, action, owner role, due date, priority, linked problem record, status. Add data validation for status.
```

### Step 4: Leadership summary

Prepare the short version.

```text
Create a 5-slide summary deck for the Head of IT: what happened, impact, root cause, top 5 actions, and what we ask leadership to support.
```

## What good looks like

- [ ] Restore time is 3 hours 16 minutes, within the 4-hour P1 SLA.
- [ ] The root cause names the emergency change that bypassed CAB and the untested rollback, without blaming individuals.
- [ ] Contributing factors include delayed detection (about 12 minutes) and no pilot-site test.
- [ ] The vendor's contract obligations (CAB approval, tested rollback, PIR within 5 business days) are cited with the clause.
- [ ] Every action has an owner role and a due date.

## Try this next

**Lessons learned for all of IT**

```text
Turn the PIR into a one-page lessons-learned article for the IT intranet, without vendor or individual names.
```

**Problem record**

```text
Draft the problem record text for the ITSM tool: problem statement, known error, workaround, and linked incidents and changes.
```

## Make it repeatable

Create a `contoso-pir-writer` skill with the section structure, the 5 Whys rule and the blameless tone.

## Tips

- Ask Cowork to flag disagreements between sources rather than resolve them silently.
- Keep PIRs blameless: refer to roles and process, not people.

## Related

- [UC-02 Major incident communications pack](../../use-cases/cowork/UC-02-major-incident-communications.md)
- [UC-07 Vendor contract and SLA performance review](../../use-cases/cowork/UC-07-vendor-sla-review.md)
- [APP-01 Major Incident Command Board](../../cowork-apps/APP-01-major-incident-command-board.md)

---

[Previous: UC-02](../cowork/UC-02-major-incident-communications.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-04](../cowork/UC-04-cab-pack.md)
