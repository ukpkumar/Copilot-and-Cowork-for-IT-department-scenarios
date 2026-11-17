# Module 2: Cowork for IT operations

[Previous: Module 1](01-foundations.md) | [Home](../README.md) | Next: [Module 3: Skills and plugins](03-skills-and-plugins.md)

## Learning objectives

- Write effective Cowork prompts for IT work.
- Understand how Cowork uses multiple sources and produces finished files.
- Apply eight IT operations use cases.

---

## 2.1 Anatomy of a good IT prompt

Use the **GOAL** pattern:

| Element | Question it answers | Example |
|---------|---------------------|---------|
| **G**oal | What outcome do you need? | "Prepare the CAB pack for Tuesday's meeting" |
| **O**rigin (sources) | Where should Cowork look? | "Use the attached change export and the CAB channel in Teams from the last 7 days" |
| **A**udience and format | Who is it for and what should it look like? | "A 6-slide deck for the CAB chair and a one-page risk summary in Word" |
| **L**imits and rules | What must it not do, and what should it flag? | "Do not approve or reject changes. Flag conflicts and any change without a rollback plan" |

**Weak prompt:** "Summarise the changes."

**Strong prompt:**

```text
Prepare the CAB pack for Tuesday 14:00. Use the attached change export
(changes-week-47.csv) and messages in the "Change Management" Teams channel
from the last 7 days. Build a 6-slide PowerPoint deck for the CAB chair and a
one-page risk summary in Word. Group changes by risk level, flag any change
that has no rollback plan or no tested backout, and highlight conflicts in the
same maintenance window. Do not approve or reject changes.
```

## 2.2 Working pattern

1. **Delegate** the outcome with the GOAL pattern.
2. **Review the plan.** Remove steps you do not want; add sources it missed.
3. **Let it run.** Cowork works across mail, Teams, calendar, OneDrive and SharePoint, and attached files.
4. **Check the output.** Ask: "Which source did each figure come from?" and "What did you infer?"
5. **Iterate.** Refine in the same conversation.
6. **Capture.** If you will do it again, turn it into a skill (Module 3).

## 2.3 The eight Cowork IT use cases

| ID | Use case | Built-in skills used | Typical output |
|----|----------|----------------------|----------------|
| [UC-01](../use-cases/cowork/UC-01-daily-it-operations-briefing.md) | Daily IT operations briefing | Daily Briefing, Email, Meetings, Enterprise Search | Briefing in chat or draft email |
| [UC-02](../use-cases/cowork/UC-02-major-incident-communications.md) | Major incident communications pack | Communications, Email, Word | Stakeholder updates, exec summary |
| [UC-03](../use-cases/cowork/UC-03-post-incident-review.md) | Post-incident review | Word, Meetings, Enterprise Search | PIR report with timeline and actions |
| [UC-04](../use-cases/cowork/UC-04-cab-pack.md) | CAB pack | Excel, PowerPoint, Word | CAB deck, risk summary |
| [UC-05](../use-cases/cowork/UC-05-license-optimisation.md) | Licence optimisation | Excel, PowerPoint | Analysis workbook, savings deck |
| [UC-06](../use-cases/cowork/UC-06-runbook-and-sop-authoring.md) | Runbook and SOP authoring | Word, Enterprise Search | Standardised runbook |
| [UC-07](../use-cases/cowork/UC-07-vendor-sla-review.md) | Vendor and SLA review | Excel, PDF, Word, Email | Scorecard, service credit letter draft |
| [UC-08](../use-cases/cowork/UC-08-audit-evidence-pack.md) | Audit evidence pack | Enterprise Search, Excel, Word | Evidence index and gap list |

## 2.4 Tips for IT teams

- **Exports are your friend.** Export incident, change, asset or licence data to CSV or Excel and attach it. Cowork analyses the file directly.
- **Name the channel and the time window.** "The Network Ops channel since Monday" is better than "Teams".
- **Ask for flags, not decisions.** For approvals, risk acceptance and personnel matters, ask Cowork to prepare evidence; people decide.
- **Keep outputs as drafts** until reviewed, especially for executive or vendor communication.
- **Protect sensitive data.** Do not paste passwords, keys or secrets into prompts. Sensitivity labels continue to apply to files Cowork reads and creates.

[Previous: Module 1](01-foundations.md) | [Home](../README.md) | Next: [Module 3: Skills and plugins](03-skills-and-plugins.md)
