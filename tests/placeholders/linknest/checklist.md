# LinkNest QA Checklist

## Happy Path
- Placeholder artifacts load and parse

## Edge Cases
- Empty payload handling
- Malformed payload rejection
- Duplicate/abuse case handling

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: LinkNest
- Worker: worker-qa
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for LinkNest (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: LinkNest
- Worker: worker-qa
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for LinkNest (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: LinkNest
- Worker: worker-qa
- Updated: 2026-02-28T12:00:00Z

## Loop 004 Stage 2
- Finalized placeholder updates for LinkNest (worker-qa).
- Updated: 2026-02-28T12:00:00Z

## Loop 004 QA Additions

### Profile Placeholder Checks
- Placeholder profile exposes stable identity fields (`id`, `handle`, `display_name`).
- Empty `bio` is allowed and renders fallback copy.
- Oversized `bio` content is truncated or rejected according to contract limits.
- Missing avatar URL falls back to default placeholder asset.
- `is_verified` defaults to `false` when omitted and does not break rendering.

### Link Placeholder Checks
- Placeholder link list supports mixed providers (`website`, `youtube`, `instagram`).
- Each link item includes stable keys (`id`, `label`, `url`, `position`, `is_active`).
- Disabled links (`is_active=false`) are excluded from public rendering.
- Invalid URL schemes are rejected (`javascript:`, malformed protocol).
- Relative URL values are rejected for external links and reported as contract violations.

### Duplicate Link Edge Case
- Duplicate link `id` values in one payload are rejected by validation.
- Duplicate `url` values with different labels are flagged for dedupe review.
- Duplicate `position` values are normalized deterministically (stable sort by `id`).
- Exact duplicate link objects (`id`, `url`, `position` all equal) are collapsed to one record before render.
