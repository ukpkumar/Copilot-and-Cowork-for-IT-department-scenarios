# Reference files

[Home](../README.md) | [Lab 0: Setup](../labs/lab-00-setup.md)

Fictional practice files for Contoso IT. Download them, save them to your OneDrive and attach them to Cowork (or use them as knowledge in Copilot Studio). All names, systems and figures are illustrative.

| File | Type | What it is | Used in |
|------|------|-----------|---------|
| [Contoso-IT-Practice-Data-Workbook.xlsx](Contoso-IT-Practice-Data-Workbook.xlsx) | Excel, 14 tabs | IT operations data: incidents, changes, licences, devices, access review, vendors, KPIs, audit controls, knowledge index | Most use cases, all apps, Labs 1, 3, 4 |
| [Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx](Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx) | Word | Raw, unpolished bridge notes for P1 incident INC-24117 | UC-02, UC-03, UC-09, APP-01, Lab 2 |
| [Contoso-IT-Legacy-Runbook-VPN-Certificate-Renewal.docx](Contoso-IT-Legacy-Runbook-VPN-Certificate-Renewal.docx) | Word | An old, inconsistent runbook, with the Contoso Standard Runbook Template in the appendix | UC-06, UC-13 |
| [Contoso-IT-Service-Desk-Knowledge-Articles.docx](Contoso-IT-Service-Desk-Knowledge-Articles.docx) | Word | 10 employee-facing knowledge articles (KB0001 to KB0010) | UC-13, UC-14, Lab 5 |
| [Contoso-IT-Managed-Network-Services-SLA-Schedule.pdf](Contoso-IT-Managed-Network-Services-SLA-Schedule.pdf) | PDF | Schedule 3 (service levels and credits) of the managed network services contract with Northwind Networks | UC-03, UC-07 |

## Workbook tabs

| Tab | Contents | Used in |
|-----|----------|---------|
| Read me | Tab guide, formula notes, report date and credit bands | All |
| Incidents | 42 incidents, 1 to 16 November 2026, with SLA calculation | UC-01, UC-02, UC-03, APP-01 |
| Major_Incident_Log | Timeline of P1 INC-24117 | UC-02, UC-03, APP-01 |
| Changes | 16 changes for 17 to 23 November 2026, plus emergency change CHG-3092, with conflict flag | UC-04, UC-10, UC-19, APP-02 |
| Licences | Purchased, assigned, unit cost and renewal per product | UC-05, APP-03 |
| Licence_Usage | Active and inactive licences with potential annual saving | UC-05, APP-03 |
| Devices | 40 devices with compliance by site | UC-20, APP-03 |
| Access_Review | Q4 2026 access review campaign, 60 items | APP-04, UC-15 |
| Vendors_SLA | Monthly vendor performance and service credit calculation | UC-07 |
| Vendor_Contracts | Contract dates, values, auto-renewal and notice deadlines | UC-07 |
| Demand_Intake | 12 IT demand requests with priority score | APP-05 |
| Service_KPIs | 8 weeks of service desk KPIs | UC-01, UC-11 |
| Audit_Controls | 15 ISO/IEC 27001 Annex A-style controls and evidence status | UC-08 |
| KB_Index | 15 knowledge article titles | UC-13, UC-14 |

## Facts built into the data (answer key)

Use these to check results in a demo or lab.

| Topic | What the data shows |
|-------|---------------------|
| P1 INC-24117 | Opened 9 Nov 2026 07:42, restored 10:58: 196 minutes, within the 4-hour P1 SLA. About 1,240 users at Remote Sites A and B. Caused by emergency change CHG-3092 (Northwind Networks) that bypassed CAB; rollback untested and failed |
| Other incidents | P1 INC-24090 (ERP, Head Office) restored in 205 minutes. P2 SLA breaches: INC-24095 (610 min) and INC-24108 (545 min). 6 incidents still open |
| Changes | CHG-3108 and CHG-3109 conflict on Sat 22 Nov, 22:00 to 02:00, Head Office core network. CHG-3104 and CHG-3112 have no rollback plan. CHG-3111 is high risk. CHG-3092 needs retrospective review |
| Licences | Microsoft 365 E5: 214 inactive over 60 days (about AED 539,280 a year). Copilot: 61 inactive over 30 days. Visio 72, Project 49, Zoom 95 unused |
| Devices | Remote Site C: 8 non-compliant devices (4 on an outdated OS, 4 not checked in for 16 to 31 days) |
| Access review | 12 items pending; 5 leavers still have access |
| Vendors | Northwind October availability 99.41%: 10% credit = AED 18,000. Contract ends 31 Jan 2027; notice deadline 2 Dec 2026 |
| Service KPIs | Backlog rises over the last two weeks (148, 185, 210) |
| Audit | 3 controls with missing evidence, 4 partial |
| Runbook | VPN certificate expires 15 Dec 2026; renewal due 30 days before (15 Nov 2026) |
