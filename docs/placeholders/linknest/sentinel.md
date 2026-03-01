# LinkNest Sentinel Checklist

- Dead code scan for placeholder directories
- Secret scanning before merge
- Input sanitization checks for sample payloads
- Dependency pruning review

## Rollback / Reliability Notes
Keep rollback steps documented and verify recovery path before release.

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: LinkNest
- Worker: worker-sentinel
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for LinkNest (worker-sentinel).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: LinkNest
- Worker: worker-sentinel
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for LinkNest (worker-sentinel).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: LinkNest
- Worker: worker-sentinel
- Updated: 2026-02-28T12:55:00Z

### Abuse Prevention Checks (Additive)
- Spam link checks:
  - Flag short-link chains that hide destination domains.
  - Flag mismatched anchor text vs final destination domain intent.
  - Reject known-malicious and parked domains from blocklist feeds.
  - Rate-limit repeated submissions from the same actor/IP fingerprint.
- Dead content removal checks:
  - Detect persistent 404/410 targets and queue for placeholder removal.
  - Detect expired invite links and deprecate stale profile buttons.
  - Remove orphaned placeholders that no longer map to active link sets.
  - Mark links with repeated timeout/DNS failures for manual review.
- Placeholder hygiene:
  - Keep quarantine notes for flagged links with timestamp and reviewer.
  - Require re-validation before restoring previously removed links.

## Loop 004 Stage 2
- Compatibility objective: additive only, no removals of prior checklist items.

### Sentinel Triage Baseline (Backward-Compatible)
- Spam link checks:
  - Score repeated destination-domain submissions over 24h/7d windows.
  - Flag bulk uploads with near-duplicate URL paths and query params.
  - Quarantine links that redirect more than 2 hops before final resolution.
- Dead content removal checks:
  - Place links in "watch" state after first hard failure before removal.
  - Remove links only after threshold: 3 failed checks across 48h minimum.
  - Preserve archived metadata (owner, label, last healthy timestamp) on removal.
- Operational safeguards:
  - Keep existing blocklist allowlist semantics unchanged.
  - Log every automated action with rule ID and execution timestamp.
