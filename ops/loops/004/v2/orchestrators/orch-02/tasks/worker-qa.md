# Task | Loop 004 | orch-02 -> worker-qa

## Metadata
- task_id: L004-O2-QA-001
- title: HabitPulse contract fixture checks (Loop 2) (Loop 3) (Loop 4)
- product: HabitPulse
- use_case: Daily habit tracking
- token_budget_max: 650

## Goal
- Add QA checklist and contract notes for HabitPulse placeholders. Keep iteration 2 backward-compatible and additive. Keep iteration 3 additive and backward-compatible. Continue with real worker execution and preserve compatibility.

## Scope
- tests/placeholders/habitpulse/checklist.md
- tests/placeholders/habitpulse/contract.spec.md

## Do Not Modify
- backend/
- frontend/
- shared/

## Done Criteria
- covers streak edge cases
- spec includes required fields
- at least 2 commits

## Validation Command
- `cat tests/placeholders/habitpulse/checklist.md`

## Commit Guidance
- Minimum 2 commits for placeholder work, typed messages only (feat|fix|refactor|test|chore).
- Keep changes atomic and inside scope.

## Worker Output Contract
Write JSON to: `ops/loops/004/v2/orchestrators/orch-02/summaries/worker-qa.json`

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
- completed_scope:
  - tests/placeholders/habitpulse/checklist.md
  - tests/placeholders/habitpulse/contract.spec.md
- validation_run:
  - `cat tests/placeholders/habitpulse/checklist.md`
- commits:
  - `93876d6` (feat loop 003 stage1)
  - `3e8b61e` (refactor loop 003 finalize)
  - `f324bae` (test loop 004 streak guardrails)
