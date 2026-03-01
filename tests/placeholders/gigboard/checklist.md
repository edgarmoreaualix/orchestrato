# GigBoard QA Checklist

## Happy Path
- Placeholder artifacts load and parse
- Listing payload includes `listings` as an array of listing objects

## Edge Cases
- Empty payload handling
- Malformed payload rejection
- Duplicate/abuse case handling

## Listing Payload Checks (Loop 004)
- Empty list accepted: `listings: []`
- Empty list remains valid when envelope metadata is present
- Malformed payload rejected: missing `listings`
- Malformed payload rejected: `listings` is not an array
- Malformed payload rejected: array entries are not objects
- Malformed payload rejected: listing object missing required keys

Last updated in loop 001 finalization.

## Loop 002 Stage 1
- Product: GigBoard
- Worker: worker-qa
- Updated: 2026-02-28T11:38:52Z

## Loop 002 Stage 2
- Finalized placeholder updates for GigBoard (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 1
- Product: GigBoard
- Worker: worker-qa
- Updated: 2026-02-28T11:46:13Z

## Loop 003 Stage 2
- Finalized placeholder updates for GigBoard (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Product: GigBoard
- Worker: worker-qa
- Added explicit listing edge-case QA checks for empty and malformed payloads.
- Updated: 2026-02-28T12:00:00Z

## Loop 004 Stage 2
- Product: GigBoard
- Worker: worker-qa
- Iteration 2 compatibility: existing envelope keys remain valid; empty `listings` stays accepted.
- Iteration 3 compatibility: existing malformed payload guards remain unchanged and additive.
- Added concrete malformed samples to verify:
  - `{}` (missing `listings`)
  - `{ "listings": {} }` (`listings` not array)
  - `{ "listings": ["bad"] }` (non-object entry)
  - `{ "listings": [{ "listing_id": "x" }] }` (missing required listing keys)
- Updated: 2026-03-01T00:00:00Z
