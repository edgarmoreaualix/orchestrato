# HabitPulse Backend Contract

This placeholder defines a stable JSON contract for HabitPulse backend consumers.
Validation focuses on key presence, status values, and update cadence.

Last updated in loop 004 worker-backend.

## Compatibility Rules
- Keep `habits` and `streak` fields present for legacy clients.
- Additive fields are allowed (`habit_entries`, `streaks`, `constraints`) and must not remove legacy keys.
- New enum values or optional keys must be documented before use by consumers.

## Placeholder Constraints
- `habits[].id` and `habit_entries[].entry_id` are unique strings.
- `habit_entries[].habit_id` must reference an existing `habits[].id`.
- `habits[].frequency` supports `daily` and `weekly`.
- `habit_entries[].status` supports `completed`, `missed`, and `skipped`.
- `constraints.max_habits` is `50`.
- `constraints.max_entries_per_day_per_habit` is `1`.
- `streak.current` and `streak.longest` are non-negative integers.
- `streak.longest` must be greater than or equal to `streak.current`.
- Dates use ISO-8601 (`YYYY-MM-DD` for day-level fields, RFC3339 for timestamps).

## Loop 002 Stage 2
- Finalized placeholder updates for HabitPulse (worker-backend).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for HabitPulse (worker-backend).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Added additive schema contract notes for habit entries and per-habit streaks.
- Updated: 2026-02-28T12:05:00Z
