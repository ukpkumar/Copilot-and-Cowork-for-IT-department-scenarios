---
name: contoso-weekly-service-report
description: Produces the Contoso weekly IT service report in Word with KPIs, trends, major incidents and commentary, plus a draft cover email. Use when the user asks for the weekly service report, weekly IT KPIs or service performance summary. Version 1.0.
---

# Contoso weekly IT service report

## Inputs
- KPI export with weekly tickets opened, resolved, backlog, SLA met %, first contact resolution %, CSAT and major incidents.
- Incident export for the week.
If the user does not say which week, use the latest complete week.

## Steps
1. Calculate this week's KPIs and the change against last week and the 8-week average.
2. List P1 and P2 incidents of the week with service, site, duration and SLA status.
3. Identify the two or three most important trends.
4. Write the report in Word using the structure below, with one line chart of tickets opened, resolved and backlog over 8 weeks.
5. Create a cover email to the IT Leadership Team as a draft.

## Report structure
1. **Headline** (two sentences)
2. **KPI table**: KPI, this week, last week, 8-week average, target, status (green, amber, red)
3. **Major incidents**
4. **Trends and commentary** (three to five bullet points, factual)
5. **Actions and asks**

## Targets
- SLA met: 95% or more (amber 90 to 95, red below 90)
- First contact resolution: 70% or more
- CSAT: 4.2 or more
- Backlog: lower than the previous week

## Rules
- Every figure must come from the data. Show "n/a" if a figure is missing.
- No blame; describe causes and actions.
- The email is always a draft.
