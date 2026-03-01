# Task | Loop 004 | orch-06 -> worker-qa

## Metadata
- task_id: L004-O6-QA-001
- title: StatusDock incident QA checks (Loop 2) (Loop 3) (Loop 4)
- product: StatusDock
- use_case: Service status page
- token_budget_max: 650

## Goal
- Add QA checklist for incident lifecycle placeholders. Keep iteration 2 backward-compatible and additive. Keep iteration 3 additive and backward-compatible. Continue with real worker execution and preserve compatibility.

## Scope
- tests/placeholders/statusdock/checklist.md
- tests/placeholders/statusdock/contract.spec.md

## Do Not Modify
- backend/
- frontend/
- shared/

## Done Criteria
- includes outage and recovery edge cases
- contract keys documented
- at least 2 commits

## Validation Command
- `cat tests/placeholders/statusdock/checklist.md`

## Commit Guidance
- Minimum 2 commits for placeholder work, typed messages only (feat|fix|refactor|test|chore).
- Keep changes atomic and inside scope.

## Worker Output Contract
Write JSON to: `ops/loops/004/v2/orchestrators/orch-06/summaries/worker-qa.json`

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
- validation: `cat tests/placeholders/statusdock/checklist.md` -> `pass`
- scoped loop-004 commits:
  - `933a8e7` (`test(loop004): expand statusdock incident QA checklist and contract`)
