# Copilot Cowork, Skills, Plugins and Copilot Studio for IT

**A learning guide and session kit for Contoso's IT administration team**

This repository shows how an enterprise IT team can use **Microsoft 365 Copilot Cowork**, **Cowork skills and plugins**, **Cowork apps** and **Microsoft Copilot Studio agents** to run IT operations, governance and service delivery with less manual effort.

You can use it in two ways:

- **As a self-paced learning guide.** Read the modules in order, try the prompts, and run the hands-on labs with the reference files.
- **As session content.** Facilitators can follow the [facilitator guide](facilitator/session-plan.md), which gives the session flow and demo scripts.

> **About the scenarios.** Contoso is a fictional, multi-site energy company with corporate offices, remote operational sites and a 24x7 IT service desk. All names, figures and data in this repository are illustrative.

---

## Contents

### Learning path

| # | Module | What you will learn |
|---|--------|---------------------|
| 1 | [Foundations](modules/01-foundations.md) | What Cowork, skills, plugins, apps, scheduled tasks and Copilot Studio agents are, and when to use each |
| 2 | [Cowork for IT operations](modules/02-cowork-for-it.md) | How Cowork plans and completes multi-step IT work across mail, Teams, files and calendar |
| 3 | [Skills and plugins](modules/03-skills-and-plugins.md) | How to capture IT know-how as reusable skills, and package skills and connectors as plugins |
| 4 | [Cowork apps](modules/04-cowork-apps.md) | How to build working IT apps from a plain-language description |
| 5 | [Copilot Studio agents](modules/05-copilot-studio-agents.md) | How to build, govern and publish enterprise IT agents with knowledge, tools and flows |
| 6 | [Administration for IT admins](modules/06-administration.md) | Tenant and Cowork settings, plugin deployment, Copilot Studio environments and DLP, auditing and rollout |
| 7 | [Measuring value](modules/07-measuring-value.md) | KPIs, baselines and a simple value model for IT use cases |

### Use case catalogue (20 use cases)

| ID | Use case | Workload | Primary persona |
|----|----------|----------|-----------------|
| [UC-01](use-cases/cowork/UC-01-daily-it-operations-briefing.md) | Daily IT operations briefing | Cowork + scheduled task | IT Operations Manager |
| [UC-02](use-cases/cowork/UC-02-major-incident-communications.md) | Major incident communications pack | Cowork | Major Incident Manager |
| [UC-03](use-cases/cowork/UC-03-post-incident-review.md) | Post-incident review (PIR) and root cause report | Cowork | Problem Manager |
| [UC-04](use-cases/cowork/UC-04-cab-pack.md) | Change Advisory Board (CAB) pack | Cowork | Change Manager |
| [UC-05](use-cases/cowork/UC-05-license-optimisation.md) | Microsoft 365 licence optimisation | Cowork | M365 Platform Owner |
| [UC-06](use-cases/cowork/UC-06-runbook-and-sop-authoring.md) | Runbook and SOP authoring from existing material | Cowork | Platform Engineer |
| [UC-07](use-cases/cowork/UC-07-vendor-sla-review.md) | Vendor contract and SLA performance review | Cowork | IT Vendor Manager |
| [UC-08](use-cases/cowork/UC-08-audit-evidence-pack.md) | Security audit evidence pack | Cowork | IT Risk and Compliance Lead |
| [UC-09](use-cases/skills-plugins/UC-09-incident-update-skill.md) | Skill: incident update in the Contoso format | Cowork skill | Service Desk Lead |
| [UC-10](use-cases/skills-plugins/UC-10-change-request-review-skill.md) | Skill: change request quality review | Cowork skill | Change Manager |
| [UC-11](use-cases/skills-plugins/UC-11-weekly-service-report-skill.md) | Skill: weekly IT service report on a schedule | Cowork skill + scheduled task | Service Delivery Manager |
| [UC-12](use-cases/skills-plugins/UC-12-itsm-plugin.md) | Plugin: IT service management (ITSM) plugin | Cowork plugin | IT Operations, Service Desk |
| [UC-13](use-cases/skills-plugins/UC-13-it-knowledge-plugin.md) | Plugin: IT knowledge and runbook plugin for the service desk | Cowork plugin | Service Desk Analysts |
| [UC-14](use-cases/copilot-studio/UC-14-it-service-desk-agent.md) | IT service desk agent | Copilot Studio | All employees |
| [UC-15](use-cases/copilot-studio/UC-15-access-request-agent.md) | Access request and approval agent | Copilot Studio | Employees, Identity team |
| [UC-16](use-cases/copilot-studio/UC-16-joiner-mover-leaver-agent.md) | Joiner, mover, leaver (JML) IT agent | Copilot Studio (autonomous) | Identity and Access team |
| [UC-17](use-cases/copilot-studio/UC-17-software-request-agent.md) | Software request and licence entitlement agent | Copilot Studio | Employees, Software Asset Manager |
| [UC-18](use-cases/copilot-studio/UC-18-security-alert-triage-agent.md) | Security alert triage assistant | Copilot Studio | SOC Analysts |
| [UC-19](use-cases/copilot-studio/UC-19-change-notification-agent.md) | Change and maintenance notification agent | Copilot Studio (agent flow) | Change Manager, business users |
| [UC-20](use-cases/copilot-studio/UC-20-device-compliance-agent.md) | Device and endpoint compliance agent for remote sites | Copilot Studio | Endpoint team, Site IT coordinators |

### Cowork apps (5 apps)

| ID | App | What it replaces |
|----|-----|------------------|
| [APP-01](cowork-apps/APP-01-major-incident-command-board.md) | Major Incident Command Board | Spreadsheets and chat threads during a P1 |
| [APP-02](cowork-apps/APP-02-change-calendar-cab-tracker.md) | Change Calendar and CAB Tracker | Emailed change lists and manual conflict checks |
| [APP-03](cowork-apps/APP-03-licence-and-asset-tracker.md) | Software Licence and Asset Tracker | Disconnected licence and asset spreadsheets |
| [APP-04](cowork-apps/APP-04-access-review-tracker.md) | Access Review Campaign Tracker | Email-based quarterly access reviews |
| [APP-05](cowork-apps/APP-05-it-demand-intake.md) | IT Demand Intake and Prioritisation | Unstructured project and enhancement requests |

### Hands-on labs

| Lab | Title | Reference files |
|-----|-------|-----------------|
| [Lab 1](labs/lab-01-cowork-cab-pack.md) | Build a CAB pack with Cowork |
| [Lab 2](labs/lab-02-create-and-share-a-skill.md) | Create, test and share an IT skill |
| [Lab 3](labs/lab-03-scheduled-ops-briefing.md) | Set up a scheduled IT operations briefing |
| [Lab 4](labs/lab-04-build-a-cowork-app.md) | Build the Change Calendar app with Cowork |
| [Lab 5](labs/lab-05-copilot-studio-service-desk-agent.md) | Build an IT service desk agent in Copilot Studio |

### Toolkit

| Folder | What is in it |
|--------|---------------|
| [skills/](skills/) | Ready-to-upload skill files (`SKILL.md`) for IT |
| [reference-files/](reference-files/) | Fictional Contoso IT practice files (workbook, bridge notes, legacy runbook, knowledge articles, vendor SLA schedule) for labs and demos |
| [facilitator/](facilitator/) | Session flow, demo scripts and the reset checklist |
| [appendix/](appendix/) | Prompt library, decision guide, glossary and references |

---

## Which tool should I use?

| If you need to... | Use | Why |
|-------------------|-----|-----|
| Complete a one-off, multi-step piece of IT work (analyse, write, build files) | **Cowork** | Cowork plans the work, uses many sources and produces finished documents, decks, workbooks and emails |
| Do the same task the same way every time | **Cowork skill** | A skill captures your format, rules and steps once; you trigger it by name or Cowork picks it up automatically |
| Run a task on a recurring schedule | **Cowork scheduled task** | Cowork runs the prompt for you (for example, every weekday at 07:00) |
| Give a whole team the same skills and connections to IT systems | **Cowork plugin** | A plugin packages skills and connectors, and admins deploy it to users or groups |
| Give a team a simple working tool (tracker, board, form) | **Cowork app** | Describe the app; Cowork designs the data, builds the screens and publishes it |
| Serve many employees, take actions in IT systems, run autonomously, or enforce enterprise controls | **Copilot Studio agent** | Knowledge, tools, connectors, flows, triggers, authentication, channels and analytics, managed in governed environments |

See the full [decision guide](appendix/decision-guide.md).

---

## Prerequisites

- Microsoft 365 Copilot licences for the users who use Cowork, skills, plugins and Cowork apps.
- Cowork access granted by the admin. Cowork uses usage-based billing (Copilot Credits), and access is granted through a **spending policy that selects Cowork** in the Microsoft 365 admin center (see [Module 6](modules/06-administration.md)).
- Some capabilities, such as the App skill, may be in the Frontier program and not available in every tenant.
- For Copilot Studio: a Power Platform environment, maker access, and the connectors approved by your data loss prevention (DLP) policies.
- For plugin administration: the Copilot administrator, AI administrator or Global administrator role in the Microsoft 365 admin center.

Product capabilities change often. Always check the latest guidance in the [references](appendix/references.md) before a production rollout.

---

## How to use this repository in a session

1. Start with [Module 1](modules/01-foundations.md) and the decision guide.
2. Demo three or four use cases live. The [facilitator guide](facilitator/session-plan.md) suggests a running order.
3. Run one or two labs with the [reference files](reference-files/).
4. Close with [administration](modules/06-administration.md) and [measuring value](modules/07-measuring-value.md), and agree on the pilot use cases.

## Contributing

Add a new use case with the [use case template](appendix/use-case-template.md). Keep all data fictional and use the Contoso naming.

## Disclaimer

This is community learning content, not official product documentation. Features, names and availability of Microsoft products change; validate in your own tenant.
