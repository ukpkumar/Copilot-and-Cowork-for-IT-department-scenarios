# Module 5: Copilot Studio agents for IT

[Previous: Module 4](04-cowork-apps.md) | [Home](../README.md) | Next: [Module 6: Administration for IT admins](06-administration.md)

## Learning objectives

- Design an IT agent: purpose, audience, knowledge, tools, triggers and channels.
- Build, test and publish an agent in Copilot Studio.
- Understand authentication, connectors, MCP and agent flows for IT scenarios.
- Apply seven IT agent use cases.

---

## 5.1 When Cowork is not enough

Cowork works **for one person**, with that person's permissions. Use Copilot Studio when you need:

- **Many users**, for example every employee asking the service desk agent.
- **Actions in IT systems** through governed connectors, such as creating a ticket or adding a user to a group.
- **Autonomous behaviour**, where an event (a new hire record, a security alert) starts the agent with no user present.
- **Enterprise controls**: environments, DLP, authentication, analytics, versioning and application lifecycle management (ALM).

## 5.2 Anatomy of an IT agent

| Component | Design question | Service desk agent example |
|-----------|-----------------|----------------------------|
| **Purpose and instructions** | What does it do, and what must it never do? | Answer IT how-to questions and log tickets; never reset privileged accounts |
| **Audience and channel** | Who uses it, and where? | All employees, in Teams and Microsoft 365 Copilot |
| **Knowledge** | Where do answers come from? | IT knowledge base on SharePoint, IT policies |
| **Tools** | What actions can it take? | ITSM connector: create and look up tickets; Microsoft Graph: check device status |
| **Agent flows** | Which steps must be deterministic or approved? | Access request with manager and app-owner approval |
| **Triggers** | Does it start on its own? | New ticket assigned to the service desk queue |
| **Authentication** | Whose identity does it act with? | User sign-in with Microsoft Entra ID; actions on behalf of the user |
| **Escalation** | When does a human take over? | Hand off to a live service desk analyst |
| **Measures** | How do you know it works? | Resolution rate, escalation rate, CSAT, sessions |

## 5.3 Build flow

1. **Create.** In Copilot Studio, select **Create > New agent** and describe the agent in plain language. Copilot Studio drafts the name, description and instructions.
2. **Instructions.** Refine them: tone, scope, what to ask, what never to do, and how to format answers.
3. **Knowledge.** Add SharePoint sites, files and public websites. Keep IT knowledge in one well-structured site.
4. **Tools.** Select **Tools > Add a tool** and add:
   - **Connectors** (1,000+ prebuilt, such as ServiceNow, Office 365 Outlook, SharePoint and Microsoft Teams) or custom connectors.
   - **Model Context Protocol (MCP) servers**, prebuilt or your own.
   - **Agent flows** for deterministic, multi-step automations with approvals.
   - **Prompts** for structured AI steps, such as classifying a ticket.
5. **Topics** (optional) for fixed conversations, such as a mandatory security questionnaire.
6. **Triggers** (optional) for autonomous agents, for example "When an item is created" or a recurrence.
7. **Test.** Use the test pane and the activity map to follow every step. Run evaluations with a test set before you publish.
8. **Publish.** Publish, then add channels: **Teams and Microsoft 365 Copilot**, and others as needed.
9. **Share.** Share with users or groups, or submit for admin approval to appear in **Built for your org**.
10. **Monitor.** Review analytics: sessions, resolution, escalation, satisfaction and topic performance.

## 5.4 Authentication and connectors

- Most connectors use **on-behalf-of** authentication: the agent acts with the signed-in user's permissions. Users may see a consent prompt the first time.
- Actions appear in audit logs as performed by the user, with agent context.
- Admins govern connectors through **Power Platform DLP policies** and **connector action control**, by environment.
- When a maker publishes an agent, the platform attaches API permissions for its connectors to the agent's **Microsoft Entra Agent ID**. Admins can review these and target them with **Conditional Access**.
- For privileged IT actions (resetting MFA, changing group membership), use a dedicated connection or flow with least privilege, approval steps and logging. Do not give the agent broad admin rights.

## 5.5 Agent Builder or Copilot Studio?

| Need | Agent Builder (in the Microsoft 365 Copilot app) | Copilot Studio |
|------|-----------------------------------------------|----------------|
| Q&A over a few documents for a team | Yes | Yes |
| Actions in IT systems | Limited | Yes: connectors, MCP, flows |
| Autonomous triggers | No | Yes |
| Approvals and deterministic steps | No | Yes: agent flows and workflows |
| Environments, DLP, ALM | Tenant settings | Full Power Platform governance |
| Analytics and evaluations | Basic | Detailed |

Start with Agent Builder for a quick team agent; scale to Copilot Studio when you need actions, automation or enterprise controls.

## 5.6 The seven IT agent use cases

| ID | Agent | Pattern | Key tools |
|----|-------|---------|-----------|
| [UC-14](../use-cases/copilot-studio/UC-14-it-service-desk-agent.md) | IT service desk agent | Conversational, knowledge + actions | Knowledge base, ITSM connector, live-agent handoff |
| [UC-15](../use-cases/copilot-studio/UC-15-access-request-agent.md) | Access request and approval agent | Conversational + approval flow | Agent flow, approvals, Entra ID groups |
| [UC-16](../use-cases/copilot-studio/UC-16-joiner-mover-leaver-agent.md) | Joiner, mover, leaver agent | Autonomous, event-triggered | HR trigger, Entra ID, ITSM, Teams |
| [UC-17](../use-cases/copilot-studio/UC-17-software-request-agent.md) | Software request and licence entitlement | Conversational + flow | Software catalogue, licence data, approvals |
| [UC-18](../use-cases/copilot-studio/UC-18-security-alert-triage-agent.md) | Security alert triage assistant | Analyst assistant | Security data via connectors or MCP, ITSM |
| [UC-19](../use-cases/copilot-studio/UC-19-change-notification-agent.md) | Change and maintenance notification agent | Scheduled agent flow | Change data, Outlook, Teams |
| [UC-20](../use-cases/copilot-studio/UC-20-device-compliance-agent.md) | Device and endpoint compliance agent | Autonomous + conversational | Intune data, Teams, ITSM |

[Previous: Module 4](04-cowork-apps.md) | [Home](../README.md) | Next: [Module 6: Administration for IT admins](06-administration.md)
