# StatusDock Backend Contract

This placeholder defines a stable JSON contract for StatusDock backend consumers.
Validation focuses on key presence, status values, timeline entries, severity, and update cadence.

## Incident Contract Notes
- `incidents[].severity` uses: `minor | major | critical`.
- `incidents[].timeline[]` is append-only and ordered by `at` timestamp.
- Contract evolution is additive and backward-compatible across loop iterations.
- `incident_status_update_contract` describes required keys and cadence policy without removing legacy fields.
- `incidents[].last_updated_at` and `incidents[].next_update_due_at` provide scheduling hints for polling clients.
- `incidents[].title`, `incidents[].affected_components`, `incidents[].impact_scope`, and `incidents[].communication_channel` are optional additive fields.
- `incidents[].timeline[].actor`, `incidents[].timeline[].component`, and `incidents[].timeline[].public` are optional additive fields for richer incident updates.

## Update Cadence
- Publish incident updates every `30` minutes (`update_cadence_minutes` in `incidents.json`).
- For higher urgency events, use `incident_status_update_contract.cadence.urgent_minutes = 10`.
- Add an extra timeline entry as soon as status changes (`investigating`, `identified`, `monitoring`, `resolved`).
- Set `next_update_due_at` to `null` once no further updates are expected.
- Loop 004 keeps the cadence field stable and adds timeline detail without removing prior keys.
- Loop 004 finalization keeps required keys unchanged while adding optional metadata for incident context and authorship.

## Loop 002 Stage 2
- Finalized placeholder updates for StatusDock (worker-backend).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for StatusDock (worker-backend).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 2
- Added incident contract details while preserving backward compatibility.
- Updated: 2026-02-28T12:55:00Z

## Loop 004 Stage 3
- Added additive incident status update contract metadata and polling hints.
- Updated: 2026-03-01T00:00:00Z

## Loop 004 Stage 4
- Added optional incident/timeline metadata fields and kept required keys stable.
- Updated: 2026-03-01T18:00:00Z
