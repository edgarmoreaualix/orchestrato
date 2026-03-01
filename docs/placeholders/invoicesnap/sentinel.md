# InvoiceSnap Sentinel Checklist

- Dead code scan for placeholder directories
- Secret scanning before merge
- Input sanitization checks for sample payloads
- Dependency pruning review

## Rollback / Reliability Notes
Keep rollback steps documented and verify recovery path before release.
- Roll back by restoring the last known-good placeholder commit, then re-run dead code and secret scans before re-attempting merge.
- Store the rollback commit SHA in release notes so recovery can be executed without branch history lookup.

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: InvoiceSnap
- Worker: worker-sentinel
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-sentinel).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: InvoiceSnap
- Worker: worker-sentinel
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-sentinel).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: InvoiceSnap
- Worker: worker-sentinel
- Updated: 2026-02-28T12:55:00Z

### Cleanup and Security Checklist (Additive)
- Dead code scan: run `rg -n "TODO|FIXME|legacy|deprecated" docs/placeholders/invoicesnap` and remove stale placeholder snippets not referenced by docs.
- Dead file sweep: run `rg --files docs/placeholders/invoicesnap` and confirm every file is listed in InvoiceSnap placeholder index docs before merge.
- Secret scanning: run `rg -n "(AKIA|BEGIN PRIVATE KEY|SECRET|TOKEN|PASSWORD|api[_-]?key)" docs/placeholders/invoicesnap` and block merge if any hardcoded credential-like values are present.
- Secret policy verification: ensure any sample credentials stay redacted as `***REDACTED***` and never use production-like token formats.

## Loop 004 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-sentinel).
- Updated: 2026-03-01T00:00:00Z

### Loop 004 Sentinel Execution Steps (Additive)
1. Run dead code scan command and review each match for placeholder relevance.
2. Run dead file sweep and verify each file maps to an active placeholder doc index entry.
3. Run secret scan command and fail the change if credential-like literals are detected.
4. Re-run scans after any cleanup edits to confirm no regressions before merge.

### Rollback Drill (Loop 004 Additive)
1. Capture current candidate commit SHA and previous known-good SHA before merge.
2. If post-merge validation fails, reset placeholder docs to known-good SHA and notify release owner.
3. Re-run `rg -n "TODO|FIXME|legacy|deprecated" docs/placeholders/invoicesnap` after rollback to confirm baseline integrity.
4. Re-run `rg -n "(AKIA|BEGIN PRIVATE KEY|SECRET|TOKEN|PASSWORD|api[_-]?key)" docs/placeholders/invoicesnap` and document the clean result in release notes.

## Loop 004 Stage 3
- Compatibility objective: keep all prior checklist points unchanged while tightening operational cadence.

### Sentinel Operations Cadence (Additive)
- Run dead code scan once per placeholder change and once pre-merge for release branches.
- Run secret scan pre-commit and pre-merge; block release packaging until both scans pass.
- Require a second reviewer sign-off when any cleanup removes placeholder sections or files.
- Log scan command outputs in PR notes to preserve rollback context.

## Loop 004 Stage 4
- Finalized additive sentinel cleanup and security checklist expansion for InvoiceSnap placeholders (worker-sentinel).
- Updated: 2026-03-01T00:00:00Z
