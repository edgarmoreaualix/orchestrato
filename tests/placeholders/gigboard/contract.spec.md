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

## Loop 004 Stage 2
- Iteration 2 compatibility: envelope contract remains additive; original required keys unchanged.
- Iteration 3 compatibility: malformed payload rejection rules remain additive and backward-compatible.
- Listing key contract clarified with minimal expectations:
  - `listing_id`: non-empty string
  - `title`: non-empty string
  - `category`: non-empty string
  - `budget_type`: enum-like string (`fixed` or `hourly`)
  - `budget_min`: number
  - `budget_max`: number where `budget_max >= budget_min`
  - `currency`: non-empty string (ISO-style code allowed)
  - `location_type`: non-empty string
  - `posted_at`: timestamp string
  - `client`: object with `client_id` and `client_name` non-empty strings
- Updated: 2026-03-01T00:00:00Z
