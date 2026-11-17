# Module 4: Cowork apps

[Previous: Module 3](03-skills-and-plugins.md) | [Home](../README.md) | Next: [Module 5: Copilot Studio agents](05-copilot-studio-agents.md)

## Learning objectives

- Describe how Cowork builds apps from a description.
- Write an app brief that produces a usable first version.
- Apply five IT app patterns and know when to move an app to a governed platform.

---

## 4.1 How Cowork builds an app

1. **You describe** the app: purpose, users, data, screens and rules.
2. **Cowork confirms** the requirements and asks clarifying questions.
3. **Cowork designs the data** (for example, a SharePoint list with columns and choices) and can **seed** it from a file you upload.
4. **Cowork builds** the screens and a dashboard, and shows a **preview** in the conversation.
5. **You iterate** in plain language: "Add a filter by owner", "Flag overdue items in red".
6. **Cowork publishes** the app and gives you a link to share.

> The App skill is a Frontier capability. Availability depends on your tenant.

## 4.2 The app brief template

```text
/app Build a <app name> for <team>.

Purpose: <the problem it solves in one sentence>
Users and roles: <who views, who edits, who approves>
Data: store in <SharePoint list / Dataverse table>. Columns: <name (type), ...>
Seed data: <attached file>, or create 10 realistic sample rows
Screens: <list view with filters>, <detail/edit form>, <dashboard with KPIs>
Rules: <status flow, required fields, colour rules, calculated fields>
Do not: <e.g. send email, connect to production systems>
```

## 4.3 The five IT apps

| ID | App | Users | Data | Key screens |
|----|-----|-------|------|-------------|
| [APP-01](../cowork-apps/APP-01-major-incident-command-board.md) | Major Incident Command Board | Incident managers, resolver leads | Incidents, actions, comms log | Live board, action tracker, comms timeline |
| [APP-02](../cowork-apps/APP-02-change-calendar-cab-tracker.md) | Change Calendar and CAB Tracker | Change manager, CAB members, implementers | Changes | Calendar, conflict view, CAB decision log |
| [APP-03](../cowork-apps/APP-03-licence-and-asset-tracker.md) | Software Licence and Asset Tracker | Software asset manager, finance | Licences, assignments, renewals | Entitlement vs usage, renewals due |
| [APP-04](../cowork-apps/APP-04-access-review-tracker.md) | Access Review Campaign Tracker | Identity team, reviewers | Review items | Reviewer worklist, campaign progress |
| [APP-05](../cowork-apps/APP-05-it-demand-intake.md) | IT Demand Intake and Prioritisation | Business requesters, IT portfolio board | Demands, scores | Intake form, scoring, pipeline board |

## 4.4 From prototype to production

| Question | If "yes" |
|----------|----------|
| Will more than one team rely on it daily? | Assign a business owner and a technical owner |
| Does it hold personal, security-sensitive or regulated data? | Review the data store, permissions and sensitivity labels with the security team |
| Does it need integration (ITSM, HR, Entra ID)? | Rebuild or extend on Power Platform or Copilot Studio with governed connectors |
| Does it need approvals or audit trails? | Add an agent flow or workflow with approvals |
| Will it live longer than a pilot? | Put it into your application lifecycle (ALM) process and environment strategy |

[Previous: Module 3](03-skills-and-plugins.md) | [Home](../README.md) | Next: [Module 5: Copilot Studio agents](05-copilot-studio-agents.md)
