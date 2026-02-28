# InvoiceSnap Backend Contract

This placeholder defines a stable JSON contract for InvoiceSnap backend consumers.
Validation focuses on key presence, status values, and update cadence.

Last updated in loop 004 finalization.

## Endpoint Contract
- Path: `/api/invoices/metadata`
- Method: `GET`
- Response: `application/json`
- Compatibility: additive-only changes for new loop iterations

## Response Fields
- `product`: fixed product identifier (`InvoiceSnap`)
- `endpoint`: metadata endpoint path
- `version`: current placeholder schema version (`v0`)
- `fields`: canonical invoice metadata keys expected by consumers
- `metadata.product`: product-level metadata (name, use case, domain)
- `metadata.contract`: transport and compatibility guarantees

## Loop 002 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-backend).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-backend).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-backend).
- Updated: 2026-02-28T12:00:00Z
