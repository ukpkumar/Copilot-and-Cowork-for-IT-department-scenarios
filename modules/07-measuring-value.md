# Module 7: Measuring value

[Previous: Module 6](06-administration.md) | [Home](../README.md)

## Learning objectives

- Choose measures for each IT use case.
- Take a baseline and estimate value with a simple model.

---

## 7.1 Measures by use case type

| Type | Measures | How to collect |
|------|----------|----------------|
| Cowork document work (CAB packs, PIRs, reports) | Hours per output; cycle time; rework | Time study of 5 outputs before and after |
| Skills | Consistency (format pass rate); time per task; number of users | Sample review; usage report |
| Scheduled and event-driven tasks | Hours saved per week; on-time delivery | Owner log |
| Cowork apps | Spreadsheets retired; status-chasing emails; data freshness | Before and after count |
| Service desk agent | Self-resolution rate; ticket deflection; time to resolve; CSAT | Copilot Studio analytics; ITSM reports |
| Access and JML agents | Request-to-fulfil time; orphaned accounts; audit findings | ITSM and Entra reports |
| Licence optimisation | Licences reclaimed; annual saving | Licence report |

## 7.2 Simple value model

```
Annual hours saved  = (baseline minutes - new minutes) x occurrences per year / 60
Annual value        = annual hours saved x loaded hourly cost
Net value           = annual value + direct savings (for example licences) - Copilot Credits consumed
```

Worked example for the CAB pack ([UC-04](../use-cases/cowork/UC-04-cab-pack.md)), using illustrative figures:

| Input | Value |
|-------|-------|
| Baseline time to prepare the pack | 180 minutes |
| Time with Cowork, including review | 45 minutes |
| CAB meetings per year | 52 |
| Annual hours saved | (180 - 45) x 52 / 60 = 117 hours |

Use your own loaded hourly cost and your actual credit consumption to complete the model.

## 7.3 Value tracker

Record every pilot use case in a tracker (or build one with a Cowork app):

| Use case | Owner | Baseline | Current | Users | Monthly occurrences | Status |
|----------|-------|----------|---------|-------|---------------------|--------|
| UC-04 CAB pack | Change Manager | 180 min | 45 min | 3 | 4 | Live |

[Previous: Module 6](06-administration.md) | [Home](../README.md)
