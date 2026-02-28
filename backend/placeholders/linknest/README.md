# LinkNest Backend Contract

This placeholder defines a stable JSON contract for LinkNest backend consumers.
Validation focuses on key presence, status values, and update cadence.

Last updated in loop 004 finalization.

## Unique Slug Rules
- `profile.slug` MUST be unique globally across all LinkNest profiles.
- Uniqueness is case-insensitive (`Creator-Hub` conflicts with `creator-hub`).
- Reserved prefixes cannot be used as full slugs: `admin`, `api`, `help`.
- Slug validation should run before profile create/update persistence.
- Existing consumers can continue to rely on `rules.slug_unique=true`; new consumers may read additive slug rule fields.

## Loop 002 Stage 2
- Finalized placeholder updates for LinkNest (worker-backend).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for LinkNest (worker-backend).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Added additive link analytics counters and per-link metadata while preserving existing fields.
- Updated: 2026-02-28T12:00:00Z
