# InvoiceSnap Preview States

- Primary view rendered
- Secondary/detail state rendered
- Error/empty fallback documented
- Mobile and desktop behavior documented

Last updated in loop 001 finalization.

## Loop 002 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-frontend).
- Updated: 2026-02-28T11:38:52Z

## Loop 003 Stage 2
- Finalized placeholder updates for InvoiceSnap (worker-frontend).
- Updated: 2026-02-28T11:46:13Z

## Loop 004 Web Placeholder Preview

### View Goal
A lightweight desktop/mobile web placeholder for freelancers to scan invoice health, recent invoices, and one-click actions from a single page.

### Primary View (Default)
- Header copy: `InvoiceSnap`
- Supporting copy: `Create polished invoices, track payments, and stay tax-ready.`
- KPI strip cards:
  - `Outstanding` with currency total
  - `Paid (30d)` with currency total
  - `Overdue` with invoice count
- Main CTA label: `Create invoice`
- Secondary CTA label: `Import client`

### Secondary/Detail View (Invoice Drill-In)
- Section title format: `Invoice #INV-XXXX`
- Metadata fields: `Client`, `Issue date`, `Due date`, `Status`
- Line-item table columns: `Item`, `Qty`, `Rate`, `Amount`
- Actions: `Send reminder`, `Mark as paid`, `Download PDF`

### Empty + Error States
- Empty headline: `No invoices yet`
- Empty body: `Create your first invoice in under two minutes.`
- Empty CTA: `Start first invoice`
- Error banner copy: `We could not load your latest invoices. Try again.`

### Responsive Notes
- Desktop (`>=1024px`): 3-column KPI strip + two-pane content region.
- Tablet (`768px-1023px`): 2-column KPI grid + stacked content modules.
- Mobile (`<768px`): single-column layout, sticky bottom `Create invoice` CTA.

### Interaction Notes
- Primary button hover darkens from `#1d4ed8` to `#1e40af`.
- Invoice row hover uses subtle surface tint `#f8fafc`.
- Overdue status chip uses `#dc2626` with high-contrast text.

### Loop 004 Stage 3
- Finalized additive preview spec for the InvoiceSnap web placeholder.
- Updated: 2026-03-01T00:00:00Z
