# StatusDock Incidents Placeholder

This placeholder contract defines incident payloads for a service status page backend integration.

## Contract Notes
- Source file: `incidents.json`
- Each incident includes:
  - `severity` (`critical|major|minor|maintenance`)
  - `timeline` (ordered list of incident update events)

## Update Cadence
- Refresh `generated_at` and incident state every 5 minutes while an incident is active.
- Publish a new timeline event for each meaningful status transition (`investigating`, `identified`, `monitoring`, `resolved`).
- Keep resolved incidents available for at least 7 days for status page history.
