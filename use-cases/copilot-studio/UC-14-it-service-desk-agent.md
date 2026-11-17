# UC-14: IT service desk agent

[Previous: UC-13](../skills-plugins/UC-13-it-knowledge-plugin.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-15](../copilot-studio/UC-15-access-request-agent.md)

## At a glance

| | |
|---|---|
| **Workload** | Copilot Studio agent |
| **Persona** | All employees (built by the service desk team) |
| **Reference files** | [Contoso-IT-Service-Desk-Knowledge-Articles.docx](../../reference-files/Contoso-IT-Service-Desk-Knowledge-Articles.docx)<br>[Contoso-IT-Practice-Data-Workbook.xlsx](../../reference-files/Contoso-IT-Practice-Data-Workbook.xlsx) (`KB_Index` tab) |
| **Skills and tools** | Knowledge (SharePoint), ITSM connector tools, escalation to a live agent, Teams and Microsoft 365 Copilot channels |
| **Output** | An agent in Teams and Microsoft 365 Copilot that answers IT questions, checks ticket status and logs tickets |
| **Value** | Deflects common L1 calls (password, MFA, VPN, printer, access how-to) and gives 24x7 answers at remote sites |

## Scenario

Contoso's service desk receives thousands of calls a month, many of them how-to questions that the knowledge base already answers. Staff at remote sites work shifts and need help outside office hours. The service desk team wants an agent that answers from approved knowledge, checks ticket status and logs tickets when needed.

## Before you start

- A Copilot Studio environment for IT (see [Module 6](../../modules/06-administration.md)).
- The knowledge articles document uploaded to a SharePoint site, for example `/sites/IT-Knowledge`.
- An approved ITSM connector or MCP server for ticket creation and lookup.

## Steps

### Step 1: Create the agent

In Copilot Studio select **Create > New agent** and describe it.

```text
Create an IT service desk agent for Contoso employees.
It answers IT how-to questions using only the IT knowledge base,
checks the status of the user's open tickets, and logs a new ticket
when the answer does not solve the problem. It is friendly and brief,
asks one question at a time, and always gives the ticket number.
It never asks for passwords and never resets privileged accounts.
For lost or stolen devices it tells the user to call the 24x7 service desk on extension 7000 immediately.
```

### Step 2: Add knowledge

Add the IT knowledge SharePoint site as a knowledge source. Turn off general web knowledge so answers come only from approved content.

### Step 3: Add tools

Select **Tools > Add a tool** and add the ITSM connector actions: *Create incident*, *Get my incidents*, *Add comment*. Set the inputs the agent collects (category, description, site, impact).

### Step 4: Add escalation

Configure handoff to a live service desk analyst, and a fallback that logs a ticket when the agent cannot help.

### Step 5: Test

Use the test pane and the activity map.

```text
I'm at Remote Site B and the printer isn't working.
```

### Step 6: Publish

Publish, add the **Teams and Microsoft 365 Copilot** channel, and share with all employees (or a pilot group first).

## What good looks like

- [ ] Answers cite the knowledge article (for example KB0006 for printers).
- [ ] For a lost laptop, the agent gives extension 7000 immediately.
- [ ] When the knowledge does not solve the problem, a ticket is created and the number returned.
- [ ] The agent never asks for a password.

## Try this next

**Arabic support**

```text
Enable Arabic as a secondary language and test the top 10 questions in Arabic.
```

**Proactive outage notice**

```text
When a P1 is open for a service, start conversations about that service with the outage message and the incident number.
```

## Make it repeatable

Use the [IT knowledge plugin](../skills-plugins/UC-13-it-knowledge-plugin.md) to keep the knowledge base current.

## Tips

- Start with the top 20 call drivers; measure deflection before adding more.
- Use Copilot Studio evaluations with a test set of real (sanitised) questions before each publish.

## Related

- [UC-13 Plugin: IT knowledge and runbook plugin for the service desk](../../use-cases/skills-plugins/UC-13-it-knowledge-plugin.md)
- [UC-15 Access request and approval agent](../../use-cases/copilot-studio/UC-15-access-request-agent.md)
- [Lab 5](../../labs/lab-05-copilot-studio-service-desk-agent.md)

---

[Previous: UC-13](../skills-plugins/UC-13-it-knowledge-plugin.md) | [Use case catalogue](../README.md) | [Home](../../README.md) | [Next: UC-15](../copilot-studio/UC-15-access-request-agent.md)
