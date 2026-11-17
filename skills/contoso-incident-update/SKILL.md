---
name: contoso-incident-update
description: Writes Contoso P1 and P2 major incident status updates in the standard format for executives, site managers, the service desk and Teams. Use when the user asks for an incident update, outage communication, status update, major incident notice or resolution notice. Version 1.0.
---

# Contoso incident update

## When to use
Use for any P1 or P2 incident communication: first notice, regular update, or resolution notice.

## Inputs to gather
1. Incident ID, priority and affected services.
2. Sites affected and estimated number of users affected.
3. Current status: Investigating, Identified, Mitigating or Resolved.
4. Actions in progress and the teams involved (roles, not names).
5. Workaround, if any.
6. Time of this update and time of the next update.

If an input is missing, ask for it once. If it is still missing, write "[To be confirmed]".

## Steps
1. Read the sources the user provides (bridge notes, incident log, chat). Extract only confirmed facts.
2. Write one message per audience requested. If no audience is given, write the executive and service desk versions.
3. Check that times, user numbers and status are identical in every message.
4. Create the messages as drafts. Never send or post.

## Output format

**Executive update** (no more than 6 lines)
- Subject: `[P1] <Service> – <Status> – Update <n> – <time> GST`
- Impact: who and what is affected, sites, users
- Status and current action
- Next update: <time> GST

**Site managers**
- What users will notice
- Workaround and who to call (24x7 service desk, extension 7000)
- Next update time

**Service desk script**
- What to tell callers in two sentences
- Log calls against <Incident ID> as related incidents
- Do not promise a fix time

**Teams post** (no more than 4 lines, for the IT Major Incident channel)

**Resolution notice**
- Restore time, total duration, confirmation from sites
- "A post-incident review will follow within 5 working days."

## Rules
- State times in Gulf Standard Time (GST), 24-hour format.
- Never state a root cause until the bridge has confirmed it. Before then, use "under investigation".
- Never name individuals; use roles and teams.
- Never blame a vendor in executive or site messages.
- Plain language. No jargon such as DNS or SD-WAN in site messages; say "network issue" instead.

## Example (executive update)
Subject: [P1] Email and Teams sign-in – Mitigating – Update 3 – 09:45 GST
Users at Remote Sites A and B (about 1,240) cannot sign in to email and Teams since 07:42.
The network team has identified a configuration issue and is applying a fix with the vendor.
Workaround: urgent requests by phone to the 24x7 service desk, extension 7000.
Next update: 10:30 GST.
