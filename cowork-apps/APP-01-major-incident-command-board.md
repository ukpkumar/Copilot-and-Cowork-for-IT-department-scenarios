# APP-01: Major Incident Command Board

[Cowork apps](README.md) | [Home](../README.md) | [Next: APP-02](APP-02-change-calendar-cab-tracker.md)

## At a glance

| | |
|---|---|
| **Users** | Major Incident Manager (edit), resolver leads (edit), IT leadership (view) |
| **Replaces** | A shared spreadsheet, a whiteboard photo and several chat threads during every P1 |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Incidents` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Major_Incident_Log` tab)<br>[Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx](../reference-files/Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx) |
| **Built with** | Cowork App skill (`/app`), SharePoint lists |

## Data model

**Incidents**: Incident ID, Priority, Service, Sites affected, Users affected, Status (Investigating / Identified / Mitigating / Resolved), Incident manager role, Bridge link, Started, Restored, Next update due

**Actions**: Action ID, Incident ID, Action, Owner role, Due time, Status (Open / In progress / Done), Notes

**Comms log**: Time, Incident ID, Audience (Executives / Sites / Service desk / Vendor), Summary, Sent by role

## Screens

- **Live board**: one card per active major incident with status, duration, users affected and a countdown to the next update (red when overdue)
- **Action tracker**: actions per incident, filter by owner, overdue in red
- **Comms timeline**: all communications per incident in time order
- **Dashboard**: open major incidents, average time to restore this quarter, overdue updates

## Build it

1. Open Cowork and attach the reference files listed above.
2. Paste the prompt below. Review the requirements Cowork confirms and answer its questions.
3. Review the preview, then iterate with the prompts in the next section.
4. Publish the app and share it with a test group.

```text
/app Build a Major Incident Command Board for Contoso IT.

Purpose: run P1 and P2 major incidents from one place instead of spreadsheets and chat threads.
Users: Major Incident Manager and resolver leads edit; IT leadership views.
Data: store in SharePoint lists.
- Incidents: Incident ID, Priority, Service, Sites affected, Users affected,
  Status (Investigating, Identified, Mitigating, Resolved), Started, Restored,
  Next update due, Bridge link
- Actions: Action ID, Incident ID, Action, Owner role, Due time, Status
- Comms log: Time, Incident ID, Audience, Summary
Seed data: use INC-24117 from the attached workbook (Incidents and Major_Incident_Log tabs)
and the attached bridge notes for actions and communications.
Screens: live board with one card per active incident and a countdown to the next update;
action tracker with owner filter; comms timeline; dashboard.
Rules: next update turns red when overdue; duration calculated from Started to Restored or now.
```

## Iterate

```text
Add a 'Declare major incident' button that creates the incident and sets the next update to 15 minutes from now.
```

```text
Add a timeline view that merges actions and communications for the PIR.
```

```text
Show restore time against the P1 SLA of 4 hours.
```

## What to show in a demo

- [ ] INC-24117 shows a duration of 3 h 16 min and status Resolved within SLA.
- [ ] Comms entries at 08:15, 09:00, 09:45 and 10:30.
- [ ] Open the timeline and use it as input for the PIR in UC-03.

## Related use cases

- [UC-02 Major incident communications pack](../use-cases/cowork/UC-02-major-incident-communications.md)
- [UC-03 Post-incident review (PIR) and root cause report](../use-cases/cowork/UC-03-post-incident-review.md)

---

[Cowork apps](README.md) | [Home](../README.md) | [Next: APP-02](APP-02-change-calendar-cab-tracker.md)
