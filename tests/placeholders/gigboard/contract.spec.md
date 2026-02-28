# GigBoard Contract Spec

Required keys:
- id
- status
- created_at
- updated_at
- metadata

## Listing Envelope Contract (Loop 004)
Top-level required keys:
- id
- status
- created_at
- updated_at
- metadata
- listings

`listings` rules:
- Must be an array
- Empty array is valid (`[]`)
- Non-array values are invalid

## Listing Object Contract (Loop 004)
Each `listings[]` entry must include:
- listing_id
- title
- category
- budget_type
- budget_min
- budget_max
- currency
- location_type
- posted_at
- client

`client` object required keys:
- client_id
- client_name

Malformed payload examples to reject:
- Missing `listings` key
- `listings` present but not an array
- `listings` array with non-object items
- Listing object missing any required key above

Last updated in loop 001 finalization.

## Loop 002 Stage 2
- Finalized placeholder updates for GigBoard (worker-qa).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for GigBoard (worker-qa).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Added required listing keys and malformed payload contract notes.
- Updated: 2026-02-28T12:02:00Z
