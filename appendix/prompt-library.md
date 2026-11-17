# Prompt library

[Home](../README.md)

Every prompt from the use cases and apps in one place, ready to copy. Attach the reference files listed on each use case page first.

## UC-01: Daily IT operations briefing

[Open use case](../use-cases/cowork/UC-01-daily-it-operations-briefing.md)

**Ask for today's briefing**

```text
Prepare my IT operations briefing for this morning's 08:30 stand-up.
Use the attached workbook (Incidents and Service_KPIs tabs) and, if available,
my email and the "IT Operations" Teams channel from the last 24 hours.

Structure:
1. Headline: overall service status in one sentence (green, amber or red)
2. Open P1 and P2 incidents: ID, service, site, age, owner, next update
3. SLA breaches in the last 24 hours
4. Changes planned in the next 48 hours, with any high-risk ones flagged
5. Service desk: backlog trend and anything unusual
6. Three decisions or escalations I need to make today

Keep it to one page. Use a table for incidents. Do not send anything.
```

**Check the sources**

```text
For each item in the briefing, show the source (file and tab, email subject, or Teams message) it came from, and list anything you inferred.
```

**Refine the format**

```text
Move the decisions section to the top, add a column for 'customer impact' in the incident table, and highlight remote sites in bold.
```

**Schedule it**

```text
Run this briefing every working day (Monday to Friday) at 07:15 Dubai time. Show it to me only; do not send email or post in Teams.
```

**Event-driven version**

```text
When an email arrives from the monitoring system with 'P1' in the subject, summarise it and add it to a running 'Today's major issues' note for me.
```

**Weekly roll-up**

```text
Every Friday at 15:00, summarise this week's daily briefings into a one-page weekly operations summary for the Head of IT Infrastructure as a draft email.
```

## UC-02: Major incident communications pack

[Open use case](../use-cases/cowork/UC-02-major-incident-communications.md)

**Generate the first communications round**

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

**Update as the incident evolves**

```text
It is now 09:45. The vendor confirmed that change CHG-3092 altered DNS forwarder settings and a rollback failed. Update all four messages. Keep the root cause wording as 'a network configuration change, under investigation'.
```

**Resolution notice**

```text
Service was restored at 10:58 and confirmed by the site IT coordinators. Draft the resolution notice for each audience, include the total duration, and say that a post-incident review will follow within 5 working days.
```

**Check consistency**

```text
Compare every message you drafted today. List any differences in times, numbers or wording between audiences, and correct them.
```

**Adaptive Card for Teams**

```text
Turn the executive update into an Adaptive Card with status, impact, next update time and a link to the incident record.
```

**Vendor escalation**

```text
Draft a formal escalation email to Northwind Networks asking for a written post-implementation review of CHG-3092 within 5 business days, as required by the contract.
```

## UC-03: Post-incident review (PIR) and root cause report

[Open use case](../use-cases/cowork/UC-03-post-incident-review.md)

**Build the timeline**

```text
Build a minute-by-minute timeline of INC-24117 from the attached bridge notes and
the Major_Incident_Log tab. Columns: time, event, source, owner role.
Flag any time where the two sources disagree. Calculate time to detect,
time to declare, time to restore and total duration.
```

**Draft the PIR**

```text
Write a blameless post-incident review in Word with these sections:
Summary; Impact (users, sites, services, operational impact);
Timeline; Detection; Response; Root cause (use a 5 Whys analysis);
Contributing factors; What went well; What did not go well;
Actions (owner role, due date, priority); Appendix: sources.

Use the Changes tab for CHG-3092 and the SLA schedule for the vendor's
change management obligations. Mark anything that is inferred rather than stated.
```

**Create the action register**

```text
Create an Excel action register from the PIR actions with columns: Action ID, action, owner role, due date, priority, linked problem record, status. Add data validation for status.
```

**Leadership summary**

```text
Create a 5-slide summary deck for the Head of IT: what happened, impact, root cause, top 5 actions, and what we ask leadership to support.
```

**Lessons learned for all of IT**

```text
Turn the PIR into a one-page lessons-learned article for the IT intranet, without vendor or individual names.
```

**Problem record**

```text
Draft the problem record text for the ITSM tool: problem statement, known error, workaround, and linked incidents and changes.
```

## UC-04: Change Advisory Board (CAB) pack

[Open use case](../use-cases/cowork/UC-04-cab-pack.md)

**Analyse the changes**

```text
Use the Changes tab of the attached workbook for the week of 17 to 23 November 2026.
Check every change and list:
- changes that overlap in the same service and site window
- changes with no rollback plan or an untested rollback
- high-risk changes without business approval
- emergency changes that need retrospective CAB review
Do not approve or reject any change.
```

**Build the CAB deck**

```text
Create a 6-slide CAB deck:
1. Week at a glance (counts by risk and type)
2. Forward schedule of change (timeline by day)
3. Conflicts and proposed resolutions
4. High-risk changes: summary, impact, rollback, approval status
5. Changes not ready for approval and what is missing
6. Retrospective review: emergency change CHG-3092
Add speaker notes with questions for each implementer.
```

**Risk summary**

```text
Write a one-page Word risk summary for the CAB chair with a recommendation for each change: ready, ready with conditions, or not ready, and the reason.
```

**Implementer follow-ups**

```text
Draft an email to each implementer group whose change is not ready, listing exactly what is missing. Create drafts only.
```

**Change freeze check**

```text
List any change planned during the year-end change freeze from 20 December to 3 January and draft a note to the implementers.
```

**Post-CAB minutes**

```text
Using my notes from the CAB meeting, record the decision for each change and update the Changes tab with the CAB status.
```

## UC-05: Microsoft 365 licence optimisation

[Open use case](../use-cases/cowork/UC-05-license-optimisation.md)

**Analyse usage**

```text
Using the Licences and Licence_Usage tabs, calculate for each product:
assigned, active in the last 30 days, inactive 30 to 60 days, inactive over 60 days,
inactive %, and potential annual saving in AED (inactive over 60 days x unit cost x 12).
Rank the products by potential saving. Show the formulas you used.
```

**Find duplication**

```text
Identify products that duplicate capabilities we already own in Microsoft 365 (for example, meetings, PDF editing or diagramming) and estimate the saving if we retire them at renewal.
```

**Copilot licences**

```text
For Microsoft 365 Copilot, list how many licences are inactive for 30 days or more and propose a reassignment process: notify, wait 14 days, reclaim, reassign to the waiting list.
```

**Build the savings pack**

```text
Create a 5-slide deck for the IT Leadership Team with the total potential saving, top opportunities, risks, and a 90-day reclaim plan. Also draft the user notification email for inactive licence holders (draft only).
```

**Renewal negotiation brief**

```text
Prepare a one-page negotiation brief for the licence renewal with the true-down quantities and the evidence.
```

**Monthly check**

```text
Schedule this analysis on the first working day of each month and show me only the changes since last month.
```

## UC-06: Runbook and SOP authoring from existing material

[Open use case](../use-cases/cowork/UC-06-runbook-and-sop-authoring.md)

**Assess the legacy runbook**

```text
Review the attached legacy VPN certificate renewal runbook against the Contoso Standard Runbook Template at the end of the document. List every missing section, unclear step and outdated reference.
```

**Rewrite it**

```text
Rewrite the runbook into the Contoso Standard Runbook Template in Word.
- Number every procedure step and give each an expected result
- Add pre-checks, validation and rollback sections
- Add a communications section (who to notify before and after)
- Replace references to the old wiki with [Link to current knowledge article]
- Mark any step you had to infer with [Confirm]
```

**Plan the renewal**

```text
The certificate expires on 15 December 2026 and must be renewed 30 days before expiry. Propose a change window, draft the change request text, and list the people to notify.
```

**Bulk standardisation**

```text
Here are five more legacy runbooks. Convert each to the standard template and give me a table of gaps found per runbook.
```

**Quick reference card**

```text
Create a one-page quick reference card for night-shift engineers from the new runbook.
```

## UC-07: Vendor contract and SLA performance review

[Open use case](../use-cases/cowork/UC-07-vendor-sla-review.md)

**Extract the contract terms**

```text
From the attached SLA schedule, extract the service levels, the service credit bands, the cap, the claim window, the change management obligations and the renewal terms. Cite the clause number for each.
```

**Score performance**

```text
Using the Vendors_SLA tab, build a scorecard for Northwind Networks for July to October 2026:
availability vs target, P1 response vs target, credit band and service credit in AED per month.
Check whether the repeated-failure clause is triggered.
Show your calculation for October.
```

**Draft the claim**

```text
Draft a formal service credit claim letter to Northwind Networks for October, citing the clauses, the measured availability, the credit amount and the claim deadline. Also request the post-implementation review for CHG-3092 that the contract requires. Draft only.
```

**Renewal decision brief**

```text
Using the Vendor_Contracts tab, tell me the notice deadline for the Northwind contract and prepare a one-page renewal options brief: renew, renegotiate, or exit.
```

**All vendors**

```text
Repeat the scorecard for all four vendors and rank them by risk.
```

**Quarterly business review**

```text
Create a QBR deck for the Northwind meeting with performance, incidents, credits and improvement asks.
```

## UC-08: Security audit evidence pack

[Open use case](../use-cases/cowork/UC-08-audit-evidence-pack.md)

**Assess evidence status**

```text
Using the Audit_Controls tab, list every control with evidence missing or partial, the owner role, and what evidence is required. Sort by risk to the audit.
```

**Cross-check with operational data**

```text
For control A.5.15 (access control), use the Access_Review tab: how many review items are still pending,
and how many leavers still have access? For control A.8.32 (change management),
use the Changes tab: which changes lack rollback plans or approval?
Summarise these as audit findings risks.
```

**Build the evidence index**

```text
Create an Excel evidence index: control ID, control name, evidence item, location, owner role, status, and a 'ready for auditor' flag.
```

**Chase owners**

```text
Draft an email to each control owner role with the evidence they need to provide and the due date of 1 December 2026. Draft only.
```

**Auditor briefing**

```text
Create a short briefing note for the auditors explaining our IT control environment and where evidence is stored.
```

**Weekly readiness**

```text
Every Monday until the audit, update the evidence status and show me what changed.
```

## UC-09: Skill: incident update in the Contoso format

[Open use case](../use-cases/skills-plugins/UC-09-incident-update-skill.md)

**Upload the skill**

```text
In Cowork, open **Customize**, filter by **Skills**, select **Add > Upload** and choose `SKILL.md`. Alternatively select **Add > New skill** and paste the content.
```

**Test explicitly**

```text
/contoso-incident-update Use the attached bridge notes. Write the 09:00 update for INC-24117 for executives and for the service desk.
```

**Test automatic selection**

```text
Give me a status update on the remote sites sign-in outage for the leadership team.
```

**Add an audience**

```text
Edit the skill to add a 'Remote site radio announcement' format of no more than 40 words.
```

**Pair with an event trigger**

```text
When an email with subject starting 'P1 –' arrives from the monitoring system, use contoso-incident-update to draft the first executive notice for my review.
```

## UC-10: Skill: change request quality review

[Open use case](../use-cases/skills-plugins/UC-10-change-request-review-skill.md)

**Review one change**

```text
/contoso-change-review Review change CHG-3112 from the attached workbook.
```

**Review a batch**

```text
/contoso-change-review Review every Normal and Emergency change in the Changes tab and return a table: change ID, verdict (Ready / Ready with conditions / Not ready), missing items, and the question to ask the implementer.
```

**Implementer self-check**

```text
I'm about to submit a change to upgrade the core switch firmware at Head Office on Saturday 22 November 22:00. Review my draft: <paste draft>.
```

**Risk scoring**

```text
Edit the skill to calculate a risk score from impact, likelihood, number of users and site criticality.
```

**Standard change candidates**

```text
Find changes that have run successfully at least five times and could become standard changes.
```

## UC-11: Skill: weekly IT service report on a schedule

[Open use case](../use-cases/skills-plugins/UC-11-weekly-service-report-skill.md)

**Run the skill once**

```text
/contoso-weekly-service-report Use the attached workbook for the week ending 16 November 2026.
```

**Adjust the commentary**

```text
Explain the rise in backlog over the last two weeks and propose two actions. Keep the tone factual.
```

**Schedule it**

```text
Every Monday at 07:00 Dubai time, run contoso-weekly-service-report using the latest export in my OneDrive folder IT Reports/Weekly, and create the cover email to the IT Leadership Team as a draft.
```

**Monthly version**

```text
Create a monthly service report for the CIO from the four weekly reports, with month-on-month trends.
```

**Site breakdown**

```text
Add a section that compares Head Office, Operations Centre and the remote sites.
```

## UC-12: Plugin: IT service management (ITSM) plugin

[Open use case](../use-cases/skills-plugins/UC-12-itsm-plugin.md)

**Design the plugin**

```text
Plugin: Contoso IT Service Management
Skills:
- contoso-incident-update       (UC-09)
- contoso-change-review         (UC-10)
- contoso-weekly-service-report (UC-11)
- contoso-pir-writer            (UC-03)
Connector:
- ITSM connector (read incidents, problems, changes; create work notes)
Audience: SG-IT-Operations, SG-Service-Desk
Owner: IT Service Management process owner
```

**Use it**

```text
Show me all open P1 and P2 incidents at the remote sites from the ITSM system and draft the 09:00 update using our incident format.
```

**Write-back**

```text
Add a skill that writes the agreed incident update as a work note on the ticket, with approval before writing.
```

**Problem management**

```text
Add a skill that finds recurring incidents and proposes problem records.
```

## UC-13: Plugin: IT knowledge and runbook plugin for the service desk

[Open use case](../use-cases/skills-plugins/UC-13-it-knowledge-plugin.md)

**Write an article from a ticket**

```text
/contoso-kb-article Create an employee knowledge article from the most recently resolved Printing incident in the attached workbook. Use our KB format.
```

**Find knowledge gaps**

```text
Compare the Incidents tab with the KB_Index tab. Which recurring issues have no knowledge article? Rank them by number of incidents.
```

**Standardise runbooks**

```text
/contoso-runbook-standard Rewrite the attached VPN certificate runbook in our template.
```

**Knowledge review**

```text
Every month, list knowledge articles not updated for 12 months and draft a review request to each owner role.
```

**Feed the agent**

```text
Once the knowledge manager approves these new articles, save them as Word files in the IT knowledge SharePoint library used by the service desk agent.
```

## UC-14: IT service desk agent

[Open use case](../use-cases/copilot-studio/UC-14-it-service-desk-agent.md)

**Create the agent**

```text
Create an IT service desk agent for Contoso employees.
It answers IT how-to questions using only the IT knowledge base,
checks the status of the user's open tickets, and logs a new ticket
when the answer does not solve the problem. It is friendly and brief,
asks one question at a time, and always gives the ticket number.
It never asks for passwords and never resets privileged accounts.
For lost or stolen devices it tells the user to call the 24x7 service desk on extension 7000 immediately.
```

**Test**

```text
I'm at Remote Site B and the printer isn't working.
```

**Arabic support**

```text
Enable Arabic as a secondary language and test the top 10 questions in Arabic.
```

**Proactive outage notice**

```text
When a P1 is open for a service, start conversations about that service with the outage message and the incident number.
```

## UC-15: Access request and approval agent

[Open use case](../use-cases/copilot-studio/UC-15-access-request-agent.md)

**Create the agent**

```text
Create an access request agent. Employees ask for access to an application.
The agent confirms the application and access level from the catalogue,
asks for the business reason, and starts the approval flow.
It tells the user the request number and who must approve.
It never grants access itself without approval.
```

**Test**

```text
I need read access to the Finance ERP for the month-end close.
```

**Time-bound access**

```text
Add an end date for OT Jump Host access and a flow that removes access automatically on that date.
```

**Access review link**

```text
Every day, add newly approved access grants as review items in the Access Review Tracker app, so they are included in the next quarterly review.
```

## UC-16: Joiner, mover, leaver (JML) IT agent

[Open use case](../use-cases/copilot-studio/UC-16-joiner-mover-leaver-agent.md)

**Create the autonomous agent**

```text
Create an agent that runs when an HR event (joiner, mover or leaver) is recorded.
For a joiner: create the IT onboarding tasks (account, licence, laptop, access groups by role),
and send the line manager the new-joiner checklist in Teams.
For a mover: list access to remove and add, and request approvals.
For a leaver: disable sign-in on the last working day, remove group memberships,
reclaim licences, and create a device return task.
Log every action in ITSM. Ask a human for approval before removing access for movers.
```

**Leaver sweep**

```text
Every Monday, compare HR leavers with active accounts and report any mismatch.
```

**Joiner welcome**

```text
Send the joiner a welcome message on day one with the top five knowledge articles.
```

## UC-17: Software request and licence entitlement agent

[Open use case](../use-cases/copilot-studio/UC-17-software-request-agent.md)

**Create the agent**

```text
Create a software request agent. When an employee asks for software:
1. Check the software catalogue: approved, restricted or not approved.
2. Suggest an approved alternative if one exists (for example, Teams instead of Zoom).
3. Check licence availability. If a free licence exists, assign it after manager approval.
4. If no licence exists, create a purchase request for the Software Asset Manager.
Always give the request number.
```

**Test**

```text
I need Visio for a network diagram.
```

**Reclaim prompt**

```text
When a licence is not used for 60 days, message the user and offer to remove it.
```

**Self-service install**

```text
After approval, request deployment through Intune and tell the user when it is ready.
```

## UC-18: Security alert triage assistant

[Open use case](../use-cases/copilot-studio/UC-18-security-alert-triage-agent.md)

**Create the agent**

```text
Create a security triage assistant for SOC analysts. Given an alert ID or
alert details, it gathers: user role and site, device compliance and last check-in,
related incidents in the last 7 days, and similar past alerts.
It proposes a severity and next steps from the SOC playbook, and drafts the ITSM
security incident. It never takes containment actions itself; it recommends them.
```

**Test**

```text
Alert: suspicious sign-in for device CTS-LT-0031 at Remote Site C. Triage it.
```

**Shift handover**

```text
At 07:00 and 19:00, summarise open alerts and their status for the incoming shift.
```

**Phishing reports**

```text
Triage emails reported through the 'Report phishing' process and draft responses to reporters.
```

## UC-19: Change and maintenance notification agent

[Open use case](../use-cases/copilot-studio/UC-19-change-notification-agent.md)

**Write the prompt step**

```text
Rewrite this change for business users in under 80 words.
Say what service is affected, when (local time), what users will notice,
and what they should do. No technical jargon. Change: {change_details}
```

**Reminder and completion**

```text
Send a reminder 1 hour before and a completion notice when the change is closed.
```

**Ask the agent**

```text
Add a conversational agent so users can ask 'Is any maintenance planned for my site this week?'
```

## UC-20: Device and endpoint compliance agent for remote sites

[Open use case](../use-cases/copilot-studio/UC-20-device-compliance-agent.md)

**Create the agent**

```text
Create a device compliance agent. Every morning it checks devices that are
non-compliant or have not checked in for 14 days. It messages each device's user
with simple steps to fix it, sends each site IT coordinator a list for their site,
and creates a ticket for devices still non-compliant after 3 days.
Users can also ask it: 'Is my laptop compliant?' and get the reason and the fix.
```

**Test**

```text
Which devices at Remote Site C are non-compliant and why?
```

**Patch window planning**

```text
Suggest the best patch window per site based on check-in patterns.
```

**Executive view**

```text
Every month, produce a compliance trend by site for the Head of IT.
```

## APP-01: Major Incident Command Board

[Open app](../cowork-apps/APP-01-major-incident-command-board.md)

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

```text
Add a 'Declare major incident' button that creates the incident and sets the next update to 15 minutes from now.
```

```text
Add a timeline view that merges actions and communications for the PIR.
```

```text
Show restore time against the P1 SLA of 4 hours.
```

## APP-02: Change Calendar and CAB Tracker

[Open app](../cowork-apps/APP-02-change-calendar-cab-tracker.md)

```text
/app Build a Change Calendar and CAB Tracker for Contoso IT.

Purpose: plan changes, spot conflicts and record CAB decisions in one place.
Users: Change Manager edits all; implementers edit their own changes; CAB members comment.
Data: one SharePoint list, Changes, with the columns from the Changes tab of the attached workbook,
plus CAB decision notes.
Seed data: import all rows from the Changes tab.
Screens: weekly calendar by site coloured by risk; conflicts view; CAB agenda with readiness checks;
decision log; dashboard.
Rules: flag a conflict when two changes overlap on the same service and site;
a change is 'Not ready' if it has no rollback plan or no business approval;
emergency changes appear in a 'Retrospective review' section.
```

```text
Add a change freeze period from 20 December to 3 January and block new changes in it.
```

```text
Let CAB members record Approve / Reject / Defer with a comment.
```

```text
Add a filter for remote sites.
```

## APP-03: Software Licence and Asset Tracker

[Open app](../cowork-apps/APP-03-licence-and-asset-tracker.md)

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

```text
Add a 'Create reclaim action' button on each product.
```

```text
Show the total potential saving from the Licence_Usage tab as a KPI.
```

```text
Add a site filter on the devices view.
```

## APP-04: Access Review Campaign Tracker

[Open app](../cowork-apps/APP-04-access-review-tracker.md)

```text
/app Build an Access Review Campaign Tracker for Contoso IT.

Purpose: run the Q4 2026 access review and give auditors clear evidence.
Users: identity team edits; reviewers decide on their own items; auditors view.
Data: SharePoint list Review items with the columns of the Access_Review tab plus Decided on and Comment.
Seed data: import the Access_Review tab from the attached workbook.
Screens: my reviews worklist with Keep and Remove actions; campaign progress by application;
risk view of leavers and movers with access; evidence view of completed decisions.
Rules: leavers with access are always shown in red at the top;
a Remove decision requires a comment; due date 30 November 2026.
```

```text
Add a progress KPI: % of items decided.
```

```text
Add a reminder list of reviewers with pending items.
```

```text
Add a column showing days to due date.
```

## APP-05: IT Demand Intake and Prioritisation

[Open app](../cowork-apps/APP-05-it-demand-intake.md)

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

```text
Add a 'Similar requests' check on submit that shows existing requests with similar titles.
```

```text
Add a capacity line on the portfolio view.
```

```text
Add a decision date and decision notes for the board.
```
