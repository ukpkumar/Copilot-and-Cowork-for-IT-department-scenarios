# APP-03: Software Licence and Asset Tracker

[Previous: APP-02](APP-02-change-calendar-cab-tracker.md) | [Cowork apps](README.md) | [Home](../README.md) | [Next: APP-04](APP-04-access-review-tracker.md)

## At a glance

| | |
|---|---|
| **Users** | Software Asset Manager (edit), M365 Platform Owner (edit), Finance (view) |
| **Replaces** | Separate licence, renewal and device spreadsheets that are never in sync |
| **Reference files** | [Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Licences` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Licence_Usage` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Devices` tab) |
| **Built with** | Cowork App skill (`/app`), SharePoint lists |

## Data model

**Licences**: Product, SKU, Purchased, Assigned, Unit cost per month (AED), Annual cost, Renewal date, Owner role

**Reclaim actions**: Product, Licences to reclaim, Notification sent, Reclaim date, Status, Saving (AED)

**Devices**: Device name, Site, OS version, Last check-in, Compliance

## Screens

- **Entitlement vs usage**: purchased, assigned and active per product with a utilisation bar
- **Renewals due**: renewals in the next 30, 60 and 90 days
- **Reclaim tracker**: reclaim actions and realised savings
- **Devices by site**: compliance by site

## Build it

1. Open Cowork and attach the reference files listed above.
2. Paste the prompt below. Review the requirements Cowork confirms and answer its questions.
3. Review the preview, then iterate with the prompts in the next section.
4. Publish the app and share it with a test group.

```text
/app Build a Software Licence and Asset Tracker for Contoso IT.

Purpose: see licence entitlement against usage, plan renewals and track reclaim savings.
Users: Software Asset Manager and M365 Platform Owner edit; Finance views.
Data: SharePoint lists Licences, Reclaim actions and Devices.
Seed data: import the Licences, Licence_Usage and Devices tabs from the attached workbook.
Screens: entitlement vs usage with utilisation %; renewals due in 30/60/90 days;
reclaim tracker with total realised saving; devices by site with compliance.
Rules: utilisation below 80% shows amber, below 60% red;
annual saving = licences reclaimed x unit cost x 12.
```

## Iterate

```text
Add a 'Create reclaim action' button on each product.
```

```text
Show the total potential saving from the Licence_Usage tab as a KPI.
```

```text
Add a site filter on the devices view.
```

## What to show in a demo

- [ ] Microsoft 365 E5 and Copilot show reclaim opportunities (214 and 61).
- [ ] Remote Site C shows 8 non-compliant devices.
- [ ] Renewals view highlights upcoming renewals.

## Related use cases

- [UC-05 Microsoft 365 licence optimisation](../use-cases/cowork/UC-05-license-optimisation.md)
- [UC-17 Software request and licence entitlement agent](../use-cases/copilot-studio/UC-17-software-request-agent.md)
- [UC-20 Device and endpoint compliance agent for remote sites](../use-cases/copilot-studio/UC-20-device-compliance-agent.md)

---

[Previous: APP-02](APP-02-change-calendar-cab-tracker.md) | [Cowork apps](README.md) | [Home](../README.md) | [Next: APP-04](APP-04-access-review-tracker.md)
