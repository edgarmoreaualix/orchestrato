# HabitPulse Contract Spec

Required keys:
- id
- status
- created_at
- updated_at
- metadata
- habit_id
- user_id
- date
- completed

Last updated in loop 001 finalization.

## Loop 002 Stage 2
- Finalized placeholder updates for HabitPulse (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for HabitPulse (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 2
- Required field constraints:
  - `id`, `habit_id`, and `user_id` are stable string identifiers.
  - `status` is required and must be parseable by Loop 002 consumers.
  - `date` uses calendar-day format (`YYYY-MM-DD`) for streak calculations.
  - `completed` is required boolean-like completion state.
  - `created_at` and `updated_at` are required timestamps.
  - `metadata` is required object-like container for additive extensions.
- Optional additive fields:
  - `streak_current` (number, default-safe when absent)
  - `streak_best` (number, default-safe when absent)
  - `last_completed_at` (timestamp)
- Backward-compatibility notes:
  - Loop 002 payload shape remains valid and must still parse unchanged.
  - Loop 003 additions remain optional and cannot invalidate Loop 002 payloads.
  - Loop 004 streak fields are additive only and must not be required by legacy consumers.
- Updated: 2026-03-01T00:00:00Z
