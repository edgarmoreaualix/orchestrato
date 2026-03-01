# LinkNest Contract Spec

Required keys:
- id
- status
- created_at
- updated_at
- metadata

Last updated in loop 001 finalization.

## Loop 002 Stage 2
- Finalized placeholder updates for LinkNest (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for LinkNest (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Contract Key Additions

### Profile Payload
Required keys:
- id
- handle
- display_name
- bio
- avatar_url
- is_verified

Optional keys:
- theme
- locale
- metadata

Validation notes:
- `id` and `handle` must be stable across updates.
- `bio` may be empty but must remain a string.
- `avatar_url` can be null; renderer must fallback safely.
- `is_verified` must be boolean; default is `false` when missing.

### Link Item Payload
Required keys:
- id
- label
- url
- position
- is_active

Optional keys:
- provider
- icon
- metadata

Validation notes:
- `id` must be unique within a payload.
- `url` must include `http` or `https` scheme.
- `position` must be integer; duplicate positions are normalized with deterministic order.
- `is_active=false` excludes the link from public render output.
