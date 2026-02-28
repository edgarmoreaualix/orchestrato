# GigBoard Backend Contract

This placeholder defines a stable JSON contract for GigBoard backend consumers.
Validation focuses on key presence, status values, and update cadence.

Last updated in loop 004 execution.

## Listing contract
- `required_listing_fields` declares the minimum fields each listing must include.
- Existing keys remain stable; new keys are additive for compatibility.
- Unknown keys should be ignored by consumers.

## Filter semantics
- `category`: exact match; values are case-insensitive.
- `location`: exact match; recommended values include `remote`, `hybrid`, and `onsite`.
- `budget_min`: numeric lower bound; listing `budget_max` must be `>= budget_min` filter.
- `budget_max`: numeric upper bound; listing `budget_min` must be `<= budget_max` filter.
- `status`: exact match; current active value is `open`.
- Multiple filters are combined with `AND` semantics.
- If no filters are provided, return all listings.

## Loop 002 Stage 2
- Finalized placeholder updates for GigBoard (worker-backend).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for GigBoard (worker-backend).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 1
- Added required listing fields and explicit filter behavior.
- Updated: 2026-02-28T12:00:00Z
