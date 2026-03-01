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

## Dependency Pruning Checklist (Loop 004)
- Inventory placeholder-only tooling and mark runtime-critical vs optional dependencies.
- Remove unused placeholder scripts from onboarding docs once replacements are available.
- Validate lockfile entries map to actively referenced packages in `docs/` workflows.
- Flag duplicate utilities across placeholders and consolidate to one maintained path.
- Record deprecation windows before removing any compatibility shim references.
- Confirm rollback notes include a dependency re-pin path for emergency restores.

## Cleanup Checklist (Loop 004)
- Remove stale placeholder examples only after replacement examples are published in the same document section.
- Keep iteration 2 compatibility aliases active while iteration 4 notes are rolled out.
- Keep iteration 3 payload examples unchanged; add new examples as additive blocks only.
- Mark every removed placeholder reference with the replacement path and migration date.
- Verify links from `docs/placeholders/habitpulse/*.md` still resolve after cleanup edits.
- Re-run sentinel checklist after each cleanup PR to prevent silent drift.

## Loop 004 Stage 2
- Finalized placeholder updates for HabitPulse (worker-sentinel) with additive compatibility notes.
- Updated: 2026-02-28T11:53:37Z

## Loop 004 Stage 3
- Revalidated input hardening examples against additive loop 2/3 compatibility constraints.
- Confirmed required-field and enum guidance remains explicit and non-breaking for existing docs consumers.
- Updated: 2026-03-01T15:00:00Z

## Loop 004 Stage 4
- Added dependency-pruning execution notes for placeholder-only tooling to prevent drift.
- Logged rollback expectation: keep re-pin guidance present until runtime validation replaces placeholders.
- Updated: 2026-03-01T15:08:00Z
