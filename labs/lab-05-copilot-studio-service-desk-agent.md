# Lab 5: Build an IT service desk agent in Copilot Studio

[Previous: Lab 4](lab-04-build-a-cowork-app.md) | [Labs](README.md) | [Home](../README.md)

**Use case:** [UC-14 IT service desk agent](../use-cases/copilot-studio/UC-14-it-service-desk-agent.md)
**Reference file:** [Contoso-IT-Service-Desk-Knowledge-Articles.docx](../reference-files/Contoso-IT-Service-Desk-Knowledge-Articles.docx)

## Before you start

- Upload the knowledge articles document to a SharePoint site or library you own, for example `IT Knowledge (Practice)`.
- Open Copilot Studio in a development or trial environment.

## Task 1: Create the agent

Select **Create > New agent** and describe it:

```text
Create an IT service desk agent called "Contoso IT Help" for Contoso employees.
It answers IT how-to questions using only the IT knowledge base,
asks one question at a time, and keeps answers short with numbered steps.
It never asks for passwords and never resets privileged accounts.
For a lost or stolen laptop or phone, it tells the user to call the
24x7 service desk on extension 7000 immediately.
When it cannot solve the problem, it tells the user how to raise a ticket
in the IT Self-Service Portal and which category to choose.
```

Review the generated name, description and instructions, then select **Create**.

## Task 2: Add knowledge

1. Go to **Knowledge > Add knowledge > SharePoint** and add the site or document.
2. Turn off general web knowledge so answers come only from the knowledge base.

## Task 3: Add starter prompts

Add: "Reset my password", "Set up MFA on my new phone", "VPN from a remote site", "My printer is not working".

## Task 4: Test

In the test pane, try:

```text
I'm at Remote Site B and the printer isn't working.
```

```text
I left my laptop in a taxi.
```

```text
Can you tell me the admin password for the VPN gateway?
```

Open the **activity map** to see which knowledge the agent used.

## Task 5 (optional): Add a tool

If an approved ITSM connector is available in your environment, select **Tools > Add a tool**, add *Create incident*, and update the instructions: "When the knowledge does not solve the problem, offer to create a ticket and return the ticket number."

## Task 6: Publish

Publish the agent, add the **Teams and Microsoft 365 Copilot** channel and share it with a colleague.

## What good looks like

- [ ] The printer answer follows KB0006 and says when to raise a ticket.
- [ ] The lost laptop answer gives extension 7000 immediately.
- [ ] The agent refuses to share passwords.
- [ ] The agent is available in Teams for your test user.
