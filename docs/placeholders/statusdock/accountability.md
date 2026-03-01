# StatusDock Accountability Template

## KPI Fields
- metric_name
- target
- actual
- variance

## Ownership
- owner
- due_date

## Cadence
Weekly review with corrective actions tracked in notes.

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: StatusDock
- Worker: worker-accountability
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for StatusDock (worker-accountability).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: StatusDock
- Worker: worker-accountability
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for StatusDock (worker-accountability).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: StatusDock
- Worker: worker-accountability
- Updated: 2026-02-28T12:55:00Z

### SLA KPI Ownership Matrix
| SLA KPI | Target | Primary Owner | Secondary Owner | Reporting Source |
| --- | --- | --- | --- | --- |
| API uptime (monthly) | >= 99.95% | SRE Lead | Platform Engineer | Uptime monitor dashboard |
| Incident acknowledgement (P1) | <= 10 minutes | On-call Engineer | Incident Commander | Incident timeline log |
| Incident resolution (P1) | <= 60 minutes | Incident Commander | Service Owner | Incident postmortem record |
| Status page freshness | <= 5 minutes lag | Support Lead | On-call Engineer | Status event stream |
| Planned maintenance notice lead time | >= 72 hours | Release Manager | Product Manager | Change calendar |

## Loop 004 Stage 2
- Finalized SLA KPI accountability baseline for StatusDock with primary and backup ownership retained for all tracked SLAs.
- Updated: 2026-03-01T00:00:00Z

### Weekly SLA Review Cadence
- Meeting window: Every Tuesday at 15:00 UTC (30 minutes)
- Required attendees: SRE Lead, Incident Commander, Support Lead, Release Manager
- Inputs reviewed: prior-week SLA report, open corrective actions, incident postmortems, maintenance calendar
- Outputs recorded: SLA pass/fail by KPI, owner-assigned remediations, due dates, escalation notes


## Loop 004 Stage 3
- Added execution guardrails to keep reviews actionable and owner-accountable without changing existing schema.
- Updated: 2026-03-01T00:15:00Z

### Accountability Execution Rules
- Any SLA miss must have one directly responsible owner and one supporting owner assigned in the same weekly review.
- Corrective actions must include an explicit due date and a measurable completion check.
- Overdue actions are escalated to Product Manager and Service Owner in the next review cycle.
- Repeated misses on the same KPI for two consecutive weeks trigger a mitigation plan entry.

## Loop 004 Stage 4
- Finalized operational handoff criteria for SLA accountability records while preserving prior template fields and cadence.
- Updated: 2026-03-01T00:30:00Z

### SLA Exception Closure Checklist
- Exception ticket includes impacted KPI, breach window, and customer impact summary.
- Primary owner confirms remediation evidence before closure.
- Secondary owner verifies monitoring recovery for one full review cycle.
- Weekly review notes capture closure decision and any follow-up action owners.
