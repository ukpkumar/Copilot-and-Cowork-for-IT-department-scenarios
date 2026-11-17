# APP-05: IT Demand Intake and Prioritisation

[Previous: APP-04](APP-04-access-review-tracker.md) | [Cowork apps](README.md) | [Home](../README.md)

## At a glance

| | |
|---|---|
| **Users** | Business requesters (submit), IT demand manager (edit), IT portfolio board (view and decide) |
| **Replaces** | Project and enhancement requests sent by email and discussed without a common scoring method |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Demand_Intake` tab) |
| **Built with** | Cowork App skill (`/app`), SharePoint lists |

## Data model

**Demands**: Request ID, Title, Requesting department, Business value (1-5), Urgency (1-5), Effort (1-5), Risk reduction (1-5), Priority score, Status (New / Assessing / Approved / Rejected / In delivery), Submitted, Decision notes

## Screens

- **Submit a request**: a simple form for business users
- **Scoring**: demand manager scores value, urgency, effort and risk reduction
- **Pipeline board**: requests by status
- **Portfolio view**: top requests by priority score for the board

## Build it

1. Open Cowork and attach the reference files listed above.
2. Paste the prompt below. Review the requirements Cowork confirms and answer its questions.
3. Review the preview, then iterate with the prompts in the next section.
4. Publish the app and share it with a test group.

```text
/app Build an IT Demand Intake and Prioritisation app for Contoso IT.

Purpose: one front door for IT project and enhancement requests, scored consistently.
Users: business requesters submit; the IT demand manager scores; the portfolio board decides.
Data: SharePoint list Demands with the columns of the Demand_Intake tab plus Decision notes.
Seed data: import the Demand_Intake tab from the attached workbook.
Screens: submit form; scoring screen; pipeline board by status; portfolio view ranked by priority score.
Rules: priority score = (business value x 0.4 + urgency x 0.3 + risk reduction x 0.3) x 5 / effort;
requesters see only their own requests.
```

## Iterate

```text
Add a 'Similar requests' check on submit that shows existing requests with similar titles.
```

```text
Add a capacity line on the portfolio view.
```

```text
Add a decision date and decision notes for the board.
```

## What to show in a demo

- [ ] Requests ranked by priority score.
- [ ] Submit a new request as a business user and score it.
- [ ] Move a request through the pipeline board.

## Related use cases

- [UC-01 Daily IT operations briefing](../use-cases/cowork/UC-01-daily-it-operations-briefing.md)

---

[Previous: APP-04](APP-04-access-review-tracker.md) | [Cowork apps](README.md) | [Home](../README.md)
