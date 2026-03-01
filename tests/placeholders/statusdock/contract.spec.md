# StatusDock Contract Spec

Required keys:
- id
- status
- created_at
- updated_at
- metadata

Last updated in loop 001 finalization.

## Loop 002 Stage 2
- Finalized placeholder updates for StatusDock (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for StatusDock (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Contract Key Additions

### Service Status Payload
Required keys:
- id
- name
- status
- updated_at
- active_incident_ids

Optional keys:
- description
- region
- metadata

Validation notes:
- `status` values are constrained to `operational`, `degraded`, or `major_outage`.
- `updated_at` must be ISO-8601 and monotonic across sequential updates for the same service.
- `active_incident_ids` must only include incident IDs that exist in the incident payload set.
- Unknown service `status` values are rejected as contract violations.

### Incident Payload
Required keys:
- id
- title
- status
- started_at
- timeline

Optional keys:
- resolved_at
- impact
- source_event_key
- metadata

Validation notes:
- `id` must remain stable for outage and recovery events of the same incident.
- `status` values are constrained to `investigating`, `identified`, `monitoring`, or `resolved`.
- `timeline` entries must be in chronological order by timestamp.
- `resolved_at` is required when `status=resolved` and must be greater than or equal to `started_at`.
- Duplicate `source_event_key` values are treated as idempotent duplicates and do not create new incidents.
