# Task | Loop 004 | orch-01 -> worker-sentinel

## Metadata
- task_id: L004-O1-SE-001
- title: InvoiceSnap cleanup checklist (Loop 2) (Loop 3) (Loop 4)
- product: InvoiceSnap
- use_case: Invoice generator for freelancers
- token_budget_max: 600

## Goal
- Define minimal sentinel cleanup and security checklist for InvoiceSnap placeholders. Keep iteration 2 backward-compatible and additive. Keep iteration 3 additive and backward-compatible. Continue with real worker execution and preserve compatibility.

## Scope
- docs/placeholders/invoicesnap/sentinel.md

## Do Not Modify
- backend/
- frontend/
- tests/
- shared/

## Done Criteria
- checklist includes dead code and secret scanning steps
- contains rollback notes
- at least 2 commits

## Validation Command
- `cat docs/placeholders/invoicesnap/sentinel.md`

## Commit Guidance
- Minimum 2 commits for placeholder work, typed messages only (feat|fix|refactor|test|chore).
- Keep changes atomic and inside scope.

## Worker Output Contract
Write JSON to: `ops/loops/004/v2/orchestrators/orch-01/summaries/worker-sentinel.json`

Required fields:
- task_id
- status (done|blocked|partial)
- files_changed
- tests_run
- commit_sha
- summary
- risks

## Finalization
- status: done
- completion_notes:
  - Scope completed in `docs/placeholders/invoicesnap/sentinel.md` with additive Loop 004 Stage 3/4 updates.
  - Dead code scan, secret scanning, and rollback drill guidance preserved and extended without breaking prior loop content.
  - Worker summary JSON populated at `ops/loops/004/v2/orchestrators/orch-01/summaries/worker-sentinel.json`.
