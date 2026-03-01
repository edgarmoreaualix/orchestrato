# Task | Loop 004 | orch-03 -> worker-lawyer

## Metadata
- task_id: L004-O3-LW-001
- title: GigBoard policy placeholder (Loop 2) (Loop 3) (Loop 4)
- product: GigBoard
- use_case: Freelance job board
- token_budget_max: 500

## Goal
- Create concise legal placeholder notes for listing terms and moderation policy. Keep iteration 2 backward-compatible and additive. Keep iteration 3 additive and backward-compatible. Continue with real worker execution and preserve compatibility.

## Scope
- docs/placeholders/gigboard/legal.md

## Do Not Modify
- backend/
- frontend/
- tests/
- shared/

## Done Criteria
- includes terms, prohibited content, takedown process
- under 250 words
- at least 2 commits

## Validation Command
- `wc -w docs/placeholders/gigboard/legal.md`

## Commit Guidance
- Minimum 2 commits for placeholder work, typed messages only (feat|fix|refactor|test|chore).
- Keep changes atomic and inside scope.

## Worker Output Contract
Write JSON to: `ops/loops/004/v2/orchestrators/orch-03/summaries/worker-lawyer.json`

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
- validation: `wc -w docs/placeholders/gigboard/legal.md` -> `249`
- scoped loop-004 commits:
  - `584de8f` (`feat: tighten gigboard legal placeholder language`)
  - `d5cd8d4` (`fix: add loop 004 stage 3 legal additive note`)
