# Module 1: Foundations

[Home](../README.md) | Next: [Module 2: Cowork for IT operations](02-cowork-for-it.md)

## Learning objectives

By the end of this module you can:

- Explain what Copilot Cowork is and how it differs from Copilot Chat.
- Describe skills, plugins, scheduled tasks and Cowork apps.
- Explain what Copilot Studio adds for enterprise agents.
- Choose the right tool for an IT scenario.

---

## 1.1 The building blocks

```
                        Microsoft 365 Copilot
                                 |
        +------------------------+-------------------------+
        |                                                  |
  Copilot Cowork                                   Copilot Studio
  (works for one person,                           (builds governed agents
   plans and completes                              and workflows for many
   multi-step work)                                 users and systems)
        |                                                  |
  +-----+------+-----------+-----------+          +--------+---------+
  |            |           |           |          |        |         |
 Built-in   Custom      Plugins   Scheduled     Agents  Agent    Tools and
 skills     skills   (skills +     tasks                flows/   connectors
                     connectors)                       workflows (incl. MCP)
              |
         Cowork apps
        (App skill)
```

### Copilot Cowork

Cowork is the part of Microsoft 365 Copilot that **does the work for you**. You describe an outcome, and Cowork:

1. Builds a **plan** and shows it to you before it acts.
2. Gathers context from your mail, meetings, Teams chats, files and the files you upload.
3. Uses **skills** for each type of task (Word, Excel, PowerPoint, PDF, Email, Scheduling, Calendar Management, Meetings, Daily Briefing, Enterprise Search, Communications, Deep Research, Adaptive Cards and others).
4. Produces **finished outputs**, such as a Word report, an Excel model, a PowerPoint deck or a draft email, and saves them to OneDrive.
5. Asks for your **approval** before actions such as sending email or changing your calendar.

You open Cowork at `m365.cloud.microsoft`, in the Microsoft 365 Copilot desktop app, or in the Copilot mobile app.

| | Copilot Chat | Copilot Cowork |
|---|---|---|
| Interaction | Question and answer | Delegate an outcome |
| Steps | Usually one response | Plans and runs many steps |
| Output | Text in chat | Finished files, drafts, apps |
| Reuse | Saved prompts | Skills, plugins, scheduled tasks |

### Skills

A **skill** is a reusable instruction that teaches Cowork how to do a specific task. You write it once, and then:

- trigger it by typing `/` and selecting it, or
- let Cowork select it automatically when your request matches its description.

A skill is a `SKILL.md` file with a name, a description and instructions (steps, rules, format, examples). Skills follow the open Agent Skills format, so the same skill can be reused in other tools that support it.

Typical IT skills: incident update format, change request review, weekly service report, PIR writer, licence optimisation analysis.

### Plugins

A **plugin** is a package, distributed through the Microsoft 365 App Store or uploaded by your organization, that can contain:

- **Skills**: prompt-based workflows that add domain expertise.
- **Connectors**: links to external data sources and services (for example, an IT service management system) that Cowork can use in conversations.

Admins manage plugins in the **Microsoft 365 admin center > Agents > Tools**, and can deploy them to all users or to specific users and groups.

### Automated tasks: scheduled and event-driven

Cowork can run work without you being present:

- A **scheduled task** is a prompt that Cowork runs on a recurring schedule, such as every weekday at 07:00. IT examples: a daily operations briefing, a weekly service report draft, a Friday licence-usage check.
- An **event-driven task** runs when a matching email or Teams message arrives. IT examples: when a P1 alert email arrives from the monitoring system, draft the first stakeholder notice; when a vendor posts in the escalation channel, summarise and log it.

Automated tasks run with the permissions of the user who created them, and by default ask for approval before they send email, post a message or change a shared system.

### Cowork apps

With the **App** skill (Frontier), Cowork builds a working business app from a description. It confirms requirements, designs the data (for example, a SharePoint list), builds the screens, lets you iterate in the conversation and publishes the app so that you can share it.

> Treat a Cowork app as a fast prototype or a team tool. Confirm data connections, ownership, sharing and lifecycle with your platform team before you put live operational data in it.

### Copilot Studio agents

**Copilot Studio** is a low-code studio for building **agents** and **workflows** that serve many users and connect to enterprise systems.

| Building block | What it does | IT example |
|----------------|--------------|------------|
| Agent | Conversational assistant that follows instructions, uses knowledge and calls tools | IT service desk agent |
| Knowledge | Grounding sources such as SharePoint sites, files and websites | IT knowledge base, policies |
| Tools | Connectors (1,000+ prebuilt), custom connectors, MCP servers, agent flows, prompts | Create a ticket, look up a device, reset MFA |
| Agent flows and workflows | Deterministic automations with AI steps and human approval | Access approval, notification flows |
| Triggers | Start an agent from an event or a schedule (autonomous agents) | New hire record, new security alert |
| Channels | Teams, Microsoft 365 Copilot, web and others | Publish to Teams and Copilot |
| Governance | Environments, DLP, authentication, analytics, auditing | Managed IT environment |

---

## 1.2 Choosing the right tool

```
Is the work for one person (or a small team) and mostly knowledge work?
  |
  +-- Yes --> Is it repeated the same way?
  |             +-- No  --> Cowork prompt
  |             +-- Yes --> Cowork skill (add a scheduled task if it is time-based)
  |                           +-- Needed by a whole team, or needs an IT system? --> Plugin
  |             Does the team need a simple tracker or board? --> Cowork app
  |
  +-- No  --> Many users, actions in IT systems, autonomous triggers,
              or strict controls (authentication, DLP, analytics)?
                  +-- Yes --> Copilot Studio agent (plus agent flows)
```

| Criteria | Cowork | Skill | Plugin | Cowork app | Copilot Studio |
|----------|:------:|:-----:|:------:|:----------:|:--------------:|
| Time to first value | Minutes | Minutes | Days | Hours | Days to weeks |
| Builder | Any licensed user | Any licensed user | Admin or developer | Licensed user (Frontier) | Maker or developer |
| Audience | Me | Me or shared | Users or groups | Team | Organization |
| Writes to IT systems | Through approved connectors | Through approved connectors | Through its connectors | Its own data store | Yes, with connectors and flows |
| Runs without a user | Scheduled tasks | Scheduled tasks | No | No | Yes, autonomous triggers |
| Central governance | Tenant settings | Sharing controls | Admin center | Platform controls | Environments, DLP, ALM |

---

## 1.3 How Cowork works with your data and approvals

- **Plan first.** Cowork shows its plan before it acts. Review and adjust it.
- **Approvals.** Actions that send, post or change things ask for approval.
- **Your permissions.** Cowork can only use data that you can already access.
- **Drafts by default.** For external or high-impact communication, ask for drafts and review before sending.
- **Traceability.** Ask Cowork which file, page or message a figure came from.

---

## Knowledge check

1. Your service desk lead wants every P1 update to use the same structure. Which tool fits best?
2. The identity team wants employees to request access to an application, with manager approval and automatic provisioning. Which tool fits best?
3. What two kinds of components can a plugin contain?

<details>
<summary>Answers</summary>

1. A Cowork skill (see [UC-09](../use-cases/skills-plugins/UC-09-incident-update-skill.md)).
2. A Copilot Studio agent with an agent flow (see [UC-15](../use-cases/copilot-studio/UC-15-access-request-agent.md)).
3. Skills and connectors.

</details>

[Home](../README.md) | Next: [Module 2: Cowork for IT operations](02-cowork-for-it.md)
