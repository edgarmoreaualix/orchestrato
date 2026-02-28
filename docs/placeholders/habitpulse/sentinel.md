# HabitPulse Sentinel Checklist

- Dead code scan for placeholder directories
- Secret scanning before merge
- Input sanitization checks for sample payloads
- Dependency pruning review

## Rollback / Reliability Notes
Keep rollback steps documented and verify recovery path before release.

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: HabitPulse
- Worker: worker-sentinel
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for HabitPulse (worker-sentinel).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: HabitPulse
- Worker: worker-sentinel
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for HabitPulse (worker-sentinel).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: HabitPulse
- Worker: worker-sentinel
- Updated: 2026-02-28T11:53:37Z

## Input Validation Hardening Checks (Loop 004)
- Confirm all placeholder request examples define required fields (`habit_id`, `event_date`, `status`).
- Verify type constraints are explicit in docs (`habit_id` as UUID/string, `event_date` as ISO-8601 date, `status` as enum).
- Reject empty strings and whitespace-only values in documented sample payloads.
- Reject unknown enum values and add explicit allowed examples (`done`, `skipped`, `missed`).
- Add max-length guidance for free-text notes to avoid unbounded placeholder inputs.
- Ensure invalid payload examples include expected error shape (`code`, `message`, `field`).
