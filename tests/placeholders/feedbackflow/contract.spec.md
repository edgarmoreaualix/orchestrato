# FeedbackFlow Contract Spec

Required keys:
- id
- status
- created_at
- updated_at
- metadata

Last updated in loop 001 finalization.

## Loop 002 Stage 2
- Finalized placeholder updates for FeedbackFlow (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for FeedbackFlow (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: FeedbackFlow
- Worker: worker-qa
- Updated: 2026-03-01T06:49:38Z

### Contract Keys for Lifecycle Placeholders
- `id`: unique placeholder feedback identifier.
- `status`: lifecycle state (`submitted`, `under_review`, `published`, `rejected`, `archived`).
- `created_at`: first placeholder submission timestamp.
- `updated_at`: most recent lifecycle update timestamp.
- `metadata`: compatibility bag for additive fields.
- `metadata.lifecycle`: transition bookkeeping for placeholder status changes.
- `metadata.lifecycle.history`: ordered transition entries with actor/time/source details.
- `metadata.abuse`: abuse controls and enforcement evidence for duplicate/vote abuse checks.
- `metadata.abuse.vote_attempts`: per-actor vote attempt tracking.
- `metadata.abuse.duplicate_fingerprint`: normalized payload fingerprint for duplicate detection.

## Loop 004 Stage 2
- Finalized placeholder contract key documentation for lifecycle and vote abuse edge cases.
- Updated: 2026-03-01T06:49:38Z
