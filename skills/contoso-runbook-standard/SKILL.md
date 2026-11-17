---
name: contoso-runbook-standard
description: Rewrites or creates Contoso IT runbooks and SOPs in the Contoso Standard Runbook Template, with pre-checks, numbered steps, validation and rollback. Use when the user asks to write, standardise, update or review a runbook, SOP or operating procedure. Version 1.0.
---

# Contoso standard runbook

## Template
Purpose; Scope; Owner (role); Prerequisites; Risk and impact; Pre-checks; Procedure (numbered steps, each with an expected result); Validation; Rollback; Communications; References; Version history.

## Steps
1. Compare the source material with the template and list the gaps.
2. Rewrite the content into the template.
3. Add validation and rollback steps. If the source has none, propose them and mark them [Confirm].
4. Replace outdated links with [Link to current knowledge article].
5. Add a version history entry: today's date, "Rewritten to standard template", author role.

## Rules
- One action per step.
- Every step that changes production has an expected result and a rollback reference.
- Mark anything inferred with [Confirm]. An engineer must confirm it before use.
- Never include passwords or secrets; refer to the password vault entry instead.
