# Decision guide: which tool for which IT job?

[Home](../README.md)

## Quick questions

1. **Is it for one person, done now?** Use **Cowork**.
2. **Will you do it again the same way?** Make it a **skill**.
3. **Does it need to run at a set time, or when an email or message arrives?** Add a **scheduled or event-driven task**.
4. **Does a whole team need it, or does it need data from an IT system?** Package it as a **plugin**.
5. **Does a team need a simple tracker, board or form?** Build a **Cowork app**.
6. **Is it for many employees, does it take actions in IT systems, does it run on its own, or does it need enterprise controls?** Build a **Copilot Studio agent**.

## Mapping of the use cases

| Use case | Cowork | Skill | Task | Plugin | App | Copilot Studio |
|----------|:------:|:-----:|:----:|:------:|:---:|:--------------:|
| UC-01 Daily operations briefing | ✓ | ✓ | ✓ | | | |
| UC-02 Major incident comms | ✓ | ✓ | | | | |
| UC-03 Post-incident review | ✓ | ✓ | | | | |
| UC-04 CAB pack | ✓ | ✓ | | | | |
| UC-05 Licence optimisation | ✓ | | ✓ | | | |
| UC-06 Runbook authoring | ✓ | ✓ | | | | |
| UC-07 Vendor SLA review | ✓ | ✓ | | | | |
| UC-08 Audit evidence pack | ✓ | | ✓ | | | |
| UC-09 Incident update | | ✓ | | ✓ | | |
| UC-10 Change review | | ✓ | | ✓ | | |
| UC-11 Weekly service report | | ✓ | ✓ | ✓ | | |
| UC-12 ITSM plugin | | ✓ | | ✓ | | |
| UC-13 IT knowledge plugin | | ✓ | | ✓ | | |
| UC-14 Service desk agent | | | | | | ✓ |
| UC-15 Access request agent | | | | | | ✓ |
| UC-16 JML agent | | | | | | ✓ |
| UC-17 Software request agent | | | | | | ✓ |
| UC-18 Security triage assistant | | | | | | ✓ |
| UC-19 Change notification agent | | | | | | ✓ |
| UC-20 Device compliance agent | | | | | | ✓ |
| APP-01 to APP-05 | | | | | ✓ | |

## Typical journey for one IT process

Take incident communications as an example:

1. **Cowork**: the Major Incident Manager drafts the first updates in a conversation (UC-02).
2. **Skill**: the format is captured as `contoso-incident-update` (UC-09).
3. **Event-driven task**: the first notice is drafted automatically when a P1 alert email arrives.
4. **Plugin**: the skill, plus a connector to the ITSM system, is deployed to all major incident managers (UC-12).
5. **App**: the Major Incident Command Board tracks actions and comms (APP-01).
6. **Copilot Studio**: the service desk agent tells employees about the outage automatically (UC-14).
