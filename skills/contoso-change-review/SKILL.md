---
name: contoso-change-review
description: Reviews Contoso IT change requests against the change management checklist and returns a readiness verdict and fix list. Use when the user asks to review, check or quality-assure a change request, a CAB list or a change before submission. Version 1.0.
---

# Contoso change request review

## When to use
Before CAB, or when an implementer wants to self-check a change request.

## Checklist
For each change, check:
1. **Description**: clear what changes, where, and why.
2. **Type**: Standard, Normal or Emergency is correct for the work.
3. **Risk**: Low, Medium or High is justified by impact (users, sites, services) and likelihood.
4. **Window**: planned start and end in GST, inside an approved maintenance window, outside any change freeze (20 December to 3 January).
5. **Conflicts**: no overlap with another change on the same service or site.
6. **Test evidence**: tested in a non-production environment, or a reason why not.
7. **Rollback**: a rollback plan exists AND has been tested.
8. **Approval**: business approval recorded for Normal changes with Medium or High risk.
9. **Communications**: affected users and sites will be notified.
10. **Emergency changes**: approved in writing by the duty IT manager, and listed for retrospective CAB review.

## Output
A table with: Change ID, Verdict, Missing or weak items, Question for the implementer.

Verdicts:
- **Ready**: all checks pass.
- **Ready with conditions**: minor gaps or a conflict that can be resolved by rescheduling.
- **Not ready**: no rollback plan, no business approval for Medium or High risk, or missing description.

End with a short summary: number of changes per verdict and the top three risks for the CAB chair.

## Rules
- Never approve or reject a change. Only CAB decides.
- Be specific in questions, for example "Which configuration backup will you restore from, and when was it tested?"
- Flag any High-risk change at a remote site, because on-site support is limited.
