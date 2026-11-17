# Facilitator guide

[Home](../README.md)

Use this guide to deliver the content as a live session for an IT administration team. Pick the tracks that match the audience.

## Before the session

- [ ] Your demo account has Cowork access, the App skill and Copilot Studio maker access.
- [ ] The [reference files](../reference-files/) are in your demo OneDrive.
- [ ] The [skills](../skills/) are uploaded to your Cowork, and the `contoso-incident-update` skill works in a new conversation.
- [ ] One Cowork app (APP-02) is already built, in case of a slow build during the demo.
- [ ] The service desk agent from Lab 5 is already published, as a fallback.
- [ ] Old scheduled tasks and drafts from earlier demos are removed.

## Session flow

| Part | Content | Demo | Material |
|------|---------|------|----------|
| 1. Why | IT challenges: scattered information, repetitive documents, manual requests | None | [Module 1](../modules/01-foundations.md) |
| 2. The building blocks | Cowork, skills, plugins, scheduled and event-driven tasks, apps, Copilot Studio | Decision guide | [Decision guide](../appendix/decision-guide.md) |
| 3. Cowork for IT operations | Delegating multi-step IT work | Demo 1 and Demo 2 | UC-04, UC-03 |
| 4. Skills and plugins | Capturing IT know-how; packaging for the team | Demo 3 | UC-09, UC-12 |
| 5. Cowork apps | Building IT tools from a description | Demo 4 | APP-02, APP-01 |
| 6. Copilot Studio agents | Employee-facing and autonomous IT agents | Demo 5 | UC-14, UC-15, UC-16 |
| 7. Administration | Access, plugins, environments, DLP, monitoring | Admin center walkthrough | [Module 6](../modules/06-administration.md) |
| 8. Hands-on | Participants run labs | Labs 1 to 5 | [Labs](../labs/README.md) |
| 9. Next steps | Choose pilot use cases and owners | Value tracker | [Module 7](../modules/07-measuring-value.md) |

## Demo scripts

### Demo 1: CAB pack (UC-04)

1. Attach the workbook. Paste the analysis prompt from [UC-04](../use-cases/cowork/UC-04-cab-pack.md), Step 1.
2. **Pause on the plan.** Point out that Cowork shows its plan before acting.
3. Show the conflict (CHG-3108 and CHG-3109) and the missing rollback plans.
4. Run Step 2 to build the deck. Open it and show the speaker notes.
5. **Message:** Cowork prepares; the CAB decides.

### Demo 2: From messy bridge notes to a PIR (UC-03)

1. Show the raw bridge notes for a few seconds; they are hard to read.
2. Run the timeline prompt, then the PIR prompt.
3. Show the 5 Whys root cause and the action register.
4. Ask: "Which source did the 3 hours 16 minutes come from?"
5. **Message:** traceable, blameless, ready for review.

### Demo 3: Skill (UC-09)

1. Show the `SKILL.md` file: description, format, rules.
2. In a new conversation, ask in natural language for a leadership update on the outage. Show the skill activating in the side panel.
3. Show **Share** on the skill.
4. Explain how the skill becomes part of a plugin deployed by admins ([UC-12](../use-cases/skills-plugins/UC-12-itsm-plugin.md)).

### Demo 4: Cowork app (APP-02)

1. Paste the `/app` prompt from [APP-02](../cowork-apps/APP-02-change-calendar-cab-tracker.md).
2. Show the clarifying questions and data design.
3. Open the pre-built app and show the conflict view and CAB agenda.
4. Make one live change: "Add a change freeze from 20 December to 3 January."

### Demo 5: Service desk agent (UC-14)

1. Show the agent's instructions, knowledge and tools in Copilot Studio.
2. Test: printer at Remote Site B; lost laptop; asking for a password.
3. Show the activity map.
4. Show the agent in Teams.
5. Explain how UC-15 and UC-16 extend it with approvals and autonomous triggers.

## Questions to expect

| Question | Short answer |
|----------|--------------|
| Can Cowork see data I cannot? | No. It uses the signed-in user's permissions. |
| Will Cowork send email without asking? | By default it asks for approval before sending, posting or changing shared systems. |
| Who controls which plugins are available? | Admins, in the Microsoft 365 admin center under Agents. |
| How is Cowork licensed? | Microsoft 365 Copilot licence plus usage-based billing (Copilot Credits); access through a spending policy. |
| Can a Copilot Studio agent act as an admin? | Use least-privilege connections, approvals and connector action control; avoid broad admin rights. |
| Where is activity logged? | Microsoft Purview audit, under Copilot activities. |

## After the session

- Agree three to five pilot use cases, an owner for each and a baseline measure.
- Share this repository with participants.
