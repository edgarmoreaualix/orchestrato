# FeedbackFlow Sentinel Checklist

- Dead code scan for placeholder directories
- Secret scanning before merge
- Input sanitization checks for sample payloads
- Dependency pruning review

## Rollback / Reliability Notes
Keep rollback steps documented and verify recovery path before release.

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: FeedbackFlow
- Worker: worker-sentinel
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for FeedbackFlow (worker-sentinel).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: FeedbackFlow
- Worker: worker-sentinel
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for FeedbackFlow (worker-sentinel).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: FeedbackFlow
- Worker: worker-sentinel
- Updated: 2026-02-28T11:53:35Z

## Loop 004 Sanitization Checks
- Validate placeholders reject script tags and inline event handlers in free-text fields.
- Verify URL placeholders only allow approved schemes (`https`), and reject `javascript:`/`data:`.
- Confirm markdown placeholders strip raw HTML blocks before render.
- Ensure email-like placeholders normalize casing and trim surrounding whitespace.
- Check payload examples with nested arrays/objects are length-bounded and type-checked.
- Review logging paths to avoid storing unsanitized raw payloads in sentinel notes.
- Validate file-name placeholders reject path traversal tokens (`../`, `%2e%2e/`, mixed-encoding variants).
- Confirm control characters (NULL, newlines in single-line fields, bidi controls) are stripped or rejected.
- Ensure sanitizer behavior is idempotent (`sanitize(sanitize(x)) == sanitize(x)`) for canonical placeholder samples.
- Verify fallback behavior on malformed UTF-8 and invalid JSON remains fail-closed (reject with structured error).
- Confirm redaction rules run before persistence for emails, phone numbers, and free-form notes.

## Loop 004 Stage 2
- Product: FeedbackFlow
- Worker: worker-sentinel
- Finalized: 2026-03-01T00:00:00Z
- Real worker execution completed with additive-only placeholder checklist updates.

## Loop 004 Simplification Plan (Additive + Backward-Compatible)
- Keep all existing checklist headings intact in loop 004; add normalized substeps instead of removing legacy items.
- Group checks into five execution gates: Input Shape, Content Sanitization, Storage Safety, Rendering Safety, and Logging Safety.
- Add a single pass/fail template per gate with evidence notes to reduce duplicated free-form reporting.
- Preserve current placeholder examples as fixtures; add new edge-case fixtures without mutating previous samples.
- Track deprecated checklist lines as "legacy-mapped" through loop 005, then remove only after explicit migration sign-off.
- Keep failure semantics unchanged: any high-risk sanitization failure blocks release regardless of other gate status.

## Loop 004 Verification Trace
- Validation command: `cat docs/placeholders/feedbackflow/sentinel.md`
- Scope guard: updates limited to sentinel documentation and orchestrator summary artifact.
