# GigBoard Sentinel Checklist

- Dead code scan for placeholder directories
- Secret scanning before merge
- Input sanitization checks for sample payloads
- Dependency pruning review

## Rollback / Reliability Notes
Keep rollback steps documented and verify recovery path before release.

Last updated in loop 001 finalization.

## Anti-Spam Checks (Loop 004)
- Enforce create-job and apply-rate limits per IP and per account with shared thresholds.
- Add a hidden honeypot field to placeholder forms and drop requests when populated.
- Block disposable-email domains for employer and freelancer signup samples.
- Detect duplicate job posts using title and body fingerprinting in a rolling time window.
- Flag burst submissions with repeated contact handles, URLs, or phone numbers for review.
- Require basic text normalization before duplicate detection (trim, lowercase, whitespace collapse).
- Add URL allowlist checks for job descriptions and reject known redirect-shortener abuse patterns.
- Record anti-spam decision reasons in audit logs for review and false-positive tuning.

## Simplification Targets (Loop 004)
- Keep one canonical placeholder job payload shape shared by docs and backend examples.
- Reduce validation rule variants to a single baseline profile per user role (employer/freelancer).
- Consolidate moderation outcomes into three states: allow, review, block.
- Standardize placeholder error responses to one compact envelope with code and message.
- Remove redundant checklist language that duplicates rollback guidance.

## Loop 002 Stage 1
- Product: GigBoard
- Worker: worker-sentinel
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for GigBoard (worker-sentinel).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: GigBoard
- Worker: worker-sentinel
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for GigBoard (worker-sentinel).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: GigBoard
- Worker: worker-sentinel
- Updated: 2026-03-01T00:00:00Z

## Loop 004 Stage 2
- Expanded anti-spam checklist and defined simplification targets for placeholders (worker-sentinel).
- Updated: 2026-03-01T00:00:00Z
