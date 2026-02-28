# FeedbackFlow Backend Contract

This placeholder defines a stable JSON contract for FeedbackFlow backend consumers.
Validation focuses on key presence, status values, and update cadence.

Last updated in loop 004 stage 2 finalization.

## Moderation Notes
- All new submissions enter `new` and require human review (`moderation.requires_review=true`).
- Rejected or non-actionable submissions may be moved directly to `closed`.
- Planned moderation automation is represented as placeholders only (`queue`, `auto_close_rejected`) and is non-breaking for existing consumers.

## Loop 002 Stage 2
- Finalized placeholder updates for FeedbackFlow (worker-backend).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for FeedbackFlow (worker-backend).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 2
- Added additive lifecycle transition contract (`status_lifecycle_v2`).
- Added moderation metadata placeholders (`queue`, `auto_close_rejected`).
- Updated: 2026-02-28T12:58:00Z
