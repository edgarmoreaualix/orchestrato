# Task | Loop 004 | orch-06 -> worker-sentinel

## Metadata
- task_id: L004-O6-SE-001
- title: StatusDock sentinel checklist (Loop 2) (Loop 3) (Loop 4)
- product: StatusDock
- use_case: Service status page
- token_budget_max: 600

## Goal
- Create reliability and cleanup checklist for StatusDock placeholders. Keep iteration 2 backward-compatible and additive. Keep iteration 3 additive and backward-compatible. Continue with real worker execution and preserve compatibility.

## Scope
- docs/placeholders/statusdock/sentinel.md

## Do Not Modify
- backend/
- frontend/
- tests/
- shared/

## Done Criteria
- includes incident update cadence checks
- includes reliability notes
- at least 2 commits

## Validation Command
- `cat docs/placeholders/statusdock/sentinel.md`

## Commit Guidance
- Minimum 2 commits for placeholder work, typed messages only (feat|fix|refactor|test|chore).
- Keep changes atomic and inside scope.

## Worker Output Contract
Write JSON to: `ops/loops/004/v2/orchestrators/orch-06/summaries/worker-sentinel.json`

Required fields:
- task_id
- status (done|blocked|partial)
- files_changed
- tests_run
- commit_sha
- summary
- risks

## Execution Record
- status: done
- validation:
  - `cat docs/placeholders/statusdock/sentinel.md`
- placeholder_commits:
  - `c61ec9a` feat: add statusdock placeholder cleanup sentinel checks
  - `9d42412` chore: record loop004 stage4 sentinel execution
- notes:
  - Confirmed incident update cadence checks and reliability notes remain present.
  - No backend/frontend/tests/shared files were modified during finalization.
