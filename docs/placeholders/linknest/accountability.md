# LinkNest Accountability Template

## KPI Fields
- metric_name
- target
- actual
- variance
- data_source
- confidence_level
- status

## Ownership
- owner
- due_date
- backup_owner
- escalation_contact

## Cadence
Weekly review with corrective actions tracked in notes.

## Weekly KPI Log Template
Use one entry per KPI per week.

| week_of | metric_name | target | actual | variance | owner | due_date | status | corrective_action | next_check_in |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| YYYY-MM-DD |  |  |  |  |  | YYYY-MM-DD | on_track \| at_risk \| off_track |  | YYYY-MM-DD |

## Accountability Rules
- Cadence: weekly KPI review every Monday.
- Owner updates `actual`, `variance`, and `status` before review.
- Any `off_track` KPI must include a corrective action and a dated next check-in.
- Escalate KPI risks to `escalation_contact` when variance remains negative for 2 consecutive weeks.

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: LinkNest
- Worker: worker-accountability
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for LinkNest (worker-accountability).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: LinkNest
- Worker: worker-accountability
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for LinkNest (worker-accountability).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: LinkNest
- Worker: worker-accountability
- Updated: 2026-03-01T00:00:00Z

### KPI Field Extensions (Additive)
- baseline
- threshold_green
- threshold_yellow
- threshold_red
- trend_direction
- blocker
- blocker_owner
- blocker_due_date

### Weekly KPI Log Template v2 (Additive)
Use this version when teams need risk visibility while preserving the original template above.

| week_of | metric_name | baseline | target | actual | variance | trend_direction | owner | due_date | status | blocker | blocker_owner | blocker_due_date | corrective_action | next_check_in |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| YYYY-MM-DD |  |  |  |  |  | improving \| flat \| declining |  | YYYY-MM-DD | on_track \| at_risk \| off_track |  |  | YYYY-MM-DD |  | YYYY-MM-DD |

## Loop 004 Stage 2
- Finalized additive KPI accountability updates for LinkNest (worker-accountability).
- Confirmed backward compatibility by retaining original KPI fields and weekly template.
- Updated: 2026-03-01T00:00:00Z

### Weekly Cadence SLA (Additive)
Use these due-date checkpoints to enforce ownership before each weekly review.

| checkpoint | owner | due_date_rule | output |
| --- | --- | --- | --- |
| KPI data refresh | metric owner | Friday EOD (local) before review week | `actual`, `variance`, and `status` updated |
| Risk triage | backup owner | Monday 09:00 (local) review day | `off_track` KPIs tagged with blocker and corrective action |
| Escalation handoff | escalation_contact | Monday 12:00 (local) if risk persists | escalation note with dated next check-in |
