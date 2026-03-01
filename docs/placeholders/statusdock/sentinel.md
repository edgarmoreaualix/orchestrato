# StatusDock Sentinel Checklist

- Dead code scan for placeholder directories
- Secret scanning before merge
- Input sanitization checks for sample payloads
- Dependency pruning review

## Incident Update Cadence Checks
- Verify first public incident acknowledgement is posted within 15 minutes of detection.
- Verify status page updates are published at least every 30 minutes while impact is ongoing.
- Verify each update includes scope, customer impact, and current mitigation status.
- Verify mitigation or workaround guidance is added no later than the second update when available.
- Verify incident closure notice includes resolution time and next communication channel for follow-up.

## Rollback / Reliability Notes
Keep rollback steps documented and verify recovery path before release.
- Verify the rollback target version is explicitly mapped to the incident start window.
- Verify failover and rollback drills are logged at least once per quarter.
- Verify alert routing reaches both on-call engineering and incident communications owner.
- Verify runbook links used in incidents resolve and contain current escalation contacts.
- Verify post-incident action items have owners and due dates before closure.

## Placeholder Cleanup and Reliability Sentinel
- Verify placeholder-only TODO markers include an owner and expiration date.
- Verify temporary incident banner copy is removed within one release after resolution.
- Verify stale placeholder references are pruned from docs when canonical runbooks exist.
- Verify every placeholder checklist item maps to either detection, communication, mitigation, or recovery.
- Verify archived incident examples are tagged with date and timezone to prevent timeline ambiguity.

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: StatusDock
- Worker: worker-sentinel
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for StatusDock (worker-sentinel).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: StatusDock
- Worker: worker-sentinel
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for StatusDock (worker-sentinel).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: StatusDock
- Worker: worker-sentinel
- Updated: 2026-02-28T12:58:00Z

## Loop 004 Stage 2
- Added incident update cadence checks for reliability review continuity.
- Updated: 2026-02-28T12:58:00Z

## Loop 004 Stage 3
- Added reliability and cleanup checklist notes without removing prior loop content.
- Updated: 2026-02-28T12:58:00Z
