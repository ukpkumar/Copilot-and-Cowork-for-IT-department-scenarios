# UC-07: Vendor contract and SLA performance review

[Previous: UC-06](../cowork/UC-06-runbook-and-sop-authoring.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-08](../cowork/UC-08-audit-evidence-pack.md)

## At a glance

| | |
|---|---|
| **Workload** | Cowork |
| **Persona** | IT Vendor Manager |
| **Reference files** | [Contoso-IT-Managed-Network-Services-SLA-Schedule.pdf](../../reference-files/Contoso-IT-Managed-Network-Services-SLA-Schedule.pdf)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Vendors_SLA` tab)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`Vendor_Contracts` tab)<br>[Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx](../../reference-files/Contoso-IT-Major-Incident-Bridge-Notes-INC-24117.docx) |
| **Skills and tools** | PDF, Excel, Word, Email |
| **Output** | Vendor scorecard, service credit calculation and a formal claim letter (draft) |
| **Value** | Ensures service credits are claimed within the contract window and gives evidence for renewal decisions |

## Scenario

Northwind Networks provides Contoso's managed SD-WAN. October availability was below target and the INC-24117 outage was caused by a vendor change that did not follow Contoso's process. The IT Vendor Manager must claim service credits within 30 days and decide whether to renew before the notice deadline.

## Before you start

- Upload the SLA schedule PDF and attach the workbook. Optionally add the bridge notes for INC-24117.

## Steps

### Step 1: Extract the contract terms

Read the contract first.

```text
From the attached SLA schedule, extract the service levels, the service credit bands, the cap, the claim window, the change management obligations and the renewal terms. Cite the clause number for each.
```

### Step 2: Score performance

Apply the terms to the data.

```text
Using the Vendors_SLA tab, build a scorecard for Northwind Networks for July to October 2026:
availability vs target, P1 response vs target, credit band and service credit in AED per month.
Check whether the repeated-failure clause is triggered.
Show your calculation for October.
```

### Step 3: Draft the claim

Prepare the formal letter.

```text
Draft a formal service credit claim letter to Northwind Networks for October, citing the clauses, the measured availability, the credit amount and the claim deadline. Also request the post-implementation review for CHG-3092 that the contract requires. Draft only.
```

### Step 4: Renewal decision brief

Prepare for the renewal.

```text
Using the Vendor_Contracts tab, tell me the notice deadline for the Northwind contract and prepare a one-page renewal options brief: renew, renegotiate, or exit.
```

## What good looks like

- [ ] October service credit is 10% of AED 180,000 = AED 18,000.
- [ ] Clauses are cited for every figure.
- [ ] The notice deadline of 2 December 2026 is highlighted.
- [ ] The letter is a draft and refers to the contract reference.

## Try this next

**All vendors**

```text
Repeat the scorecard for all four vendors and rank them by risk.
```

**Quarterly business review**

```text
Create a QBR deck for the Northwind meeting with performance, incidents, credits and improvement asks.
```

## Make it repeatable

Package the scorecard logic as a `contoso-vendor-scorecard` skill and share it with the vendor management team.

## Tips

- Contract figures must come from the contract; ask Cowork to cite clauses.
- Keep vendor letters as drafts until the Vendor Manager and Legal have reviewed them.

## Related

- [UC-03 Post-incident review (PIR) and root cause report](../../use-cases/cowork/UC-03-post-incident-review.md)

---

[Previous: UC-06](../cowork/UC-06-runbook-and-sop-authoring.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-08](../cowork/UC-08-audit-evidence-pack.md)
