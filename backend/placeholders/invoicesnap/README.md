# InvoiceSnap Backend Contract

This placeholder defines a stable JSON contract for InvoiceSnap backend consumers.
Validation focuses on key presence, status values, and update cadence.

Last updated in loop 004 finalization.

## Endpoint Contract
- Path: `/api/invoices/metadata`
- Method: `GET`
- Response: `application/json`
- Compatibility: additive-only changes for new loop iterations
- Resource: `invoice_metadata`
- Schema version: `2026-03-01`

## Response Fields
- `product`: fixed product identifier (`InvoiceSnap`)
- `endpoint`: metadata endpoint path
- `version`: current placeholder schema version (`v0`)
- `schema_version`: date-based contract marker for placeholder revisions
- `resource`: logical payload descriptor for clients and docs
- `fields`: canonical invoice metadata keys expected by consumers
- `status_enum`: allowed invoice lifecycle values (`draft`, `sent`, `paid`, `overdue`, `void`)
- `response_example`: non-authoritative sample record showing field types
- `metadata.product`: product-level metadata (name, use case, domain)
- `metadata.contract`: transport and compatibility guarantees
- `metadata.contract.nullability`: required/nullability expectations for canonical fields

## Example Response Payload
```json
{
  "invoice_id": "inv_2026_0001",
  "client_name": "Acme Studio",
  "total_due": 1250.0,
  "currency": "USD",
  "due_date": "2026-03-15",
  "status": "sent"
}
```

## Consumer Notes
- Treat `fields` as the stable canonical key list.
- Treat `response_example` as documentation only, not test fixture data.
- Ignore unknown top-level keys to preserve additive compatibility.

## Loop 002 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-backend).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-backend).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-backend).
- Updated: 2026-02-28T12:00:00Z

## Loop 004 Stage 3
- Expanded metadata contract documentation and examples for backend consumers.
- Updated: 2026-03-01T00:00:00Z
