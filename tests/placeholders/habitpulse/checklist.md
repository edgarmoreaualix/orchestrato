# HabitPulse QA Checklist

## Happy Path
- Placeholder artifacts load and parse

## Edge Cases
- Empty payload handling
- Malformed payload rejection
- Duplicate/abuse case handling

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: HabitPulse
- Worker: worker-qa
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for HabitPulse (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: HabitPulse
- Worker: worker-qa
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for HabitPulse (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: HabitPulse
- Worker: worker-qa
- Focus: streak and completion edge coverage
- Updated: 2026-02-28T11:53:39Z

## Loop 004 Stage 2
- Additive checks for streak rollover:
  - Completing habit on consecutive days increments `streak_current` by 1.
  - Missing one day resets `streak_current` to 0 without mutating `streak_best`.
  - Multiple completions in one day do not double-increment streak.
- Time boundary checks:
  - Completion at 23:59 local and next completion at 00:01 counts as consecutive days.
  - DST shift days still evaluate streak by local calendar date.
- Historical correction checks:
  - Backfilled completion updates derived streak values deterministically.
  - Deleting a completion recomputes streak fields and preserves data integrity.
- Contract guardrails:
  - Loop 002 fields remain accepted without requiring streak fields.
  - Loop 003 additive fields remain optional for Loop 002-compatible payloads.
  - Loop 004 streak fields are additive and default-safe when omitted.
- Updated: 2026-02-28T11:53:39Z
