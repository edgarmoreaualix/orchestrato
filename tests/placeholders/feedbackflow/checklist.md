# FeedbackFlow QA Checklist

## Happy Path
- Placeholder artifacts load and parse

## Edge Cases
- Empty payload handling
- Malformed payload rejection
- Duplicate/abuse case handling

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: FeedbackFlow
- Worker: worker-qa
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for FeedbackFlow (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: FeedbackFlow
- Worker: worker-qa
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for FeedbackFlow (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: FeedbackFlow
- Worker: worker-qa
- Updated: 2026-02-28T12:00:00Z

### Feedback Lifecycle Placeholder Coverage
- Submission lifecycle placeholder states are represented: `submitted -> under_review -> published`.
- Rejection lifecycle placeholder state is represented: `under_review -> rejected`.
- Archived lifecycle placeholder state is represented: `published -> archived`.

### Abuse and Integrity Checks
- Vote abuse edge case: repeated vote attempts from the same placeholder actor are rejected or ignored consistently.
- Rapid duplicate submissions with equivalent payload fingerprints are flagged as potential abuse.
- Lifecycle transitions triggered by abuse handling do not corrupt existing placeholder records.

## Loop 004 Stage 2
- Finalized placeholder updates for FeedbackFlow (worker-qa) with lifecycle and abuse-focused QA checks.
- Updated: 2026-02-28T12:00:00Z

## Loop 004 Stage 3
- Re-validated lifecycle and abuse checks against placeholder contract keys for additive compatibility.
- Updated: 2026-03-01T06:49:38Z

### Contract Key Assertions
- Lifecycle placeholders continue to require baseline keys: `id`, `status`, `created_at`, `updated_at`, `metadata`.
- Additive keys under `metadata.*` remain optional for backward-compatible placeholder fixtures.
