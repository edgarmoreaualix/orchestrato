# StatusDock Backend Contract

This placeholder defines a stable JSON contract for StatusDock backend consumers.
Validation focuses on key presence, status values, timeline entries, severity, and update cadence.

## Incident Contract Notes
- `incidents[].severity` uses: `minor | major | critical`.
- `incidents[].timeline[]` is append-only and ordered by `at` timestamp.
- Contract evolution is additive and backward-compatible across loop iterations.

## Update Cadence
- Publish incident updates every `30` minutes (`update_cadence_minutes` in `incidents.json`).
- Add an extra timeline entry as soon as status changes (`investigating`, `identified`, `monitoring`, `resolved`).

## Loop 002 Stage 2
- Finalized placeholder updates for StatusDock (worker-backend).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for StatusDock (worker-backend).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 2
- Added incident contract details while preserving backward compatibility.
- Updated: 2026-02-28T12:55:00Z
