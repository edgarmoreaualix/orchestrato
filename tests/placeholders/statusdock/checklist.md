# StatusDock QA Checklist

## Happy Path
- Placeholder artifacts load and parse

## Edge Cases
- Empty payload handling
- Malformed payload rejection
- Duplicate/abuse case handling

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: StatusDock
- Worker: worker-qa
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for StatusDock (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: StatusDock
- Worker: worker-qa
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for StatusDock (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: StatusDock
- Worker: worker-qa
- Updated: 2026-02-28T12:58:00Z

## Loop 004 Stage 2
- Incident lifecycle placeholder QA additions are additive and backward-compatible.
- Updated: 2026-02-28T12:58:00Z

## Incident Lifecycle Placeholder QA (Loop 004)
- Outage starts from operational state and transitions to degraded or major_outage with timestamp ordering preserved.
- Outage creates incident placeholder entry with deterministic `id` and non-empty `title`.
- Recovery transition requires status movement toward operational and sets `resolved_at` when fully recovered.
- Recovery without prior outage is rejected as invalid lifecycle ordering.
- Multiple outage updates for same incident preserve `id` and append timeline entries in chronological order.
- Duplicate outage events with same source event key are ignored (idempotent ingest).
- Out-of-order outage/recovery events do not corrupt latest incident status placeholder.
- Partial recovery state is represented without forcing full resolution.
- Full recovery clears active outage marker while retaining incident history placeholder records.

## Contract Coverage Checks (Loop 004)
- Service placeholder objects include required keys (`id`, `name`, `status`, `updated_at`, `active_incident_ids`).
- Incident placeholder objects include required keys (`id`, `title`, `status`, `started_at`, `timeline`).
- `resolved_at` exists only on resolved incidents and is never earlier than `started_at`.
- Unknown enum values for service/incident status are treated as invalid payloads.
