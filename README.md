# Game Dev 100 Skills — Practical Workflow

A practical, evidence-based workflow for improving games and game projects. This repository is separate from any individual game repository.

## Important distinction

The 100 entries are **skill areas and review lenses**, not 100 installed plugins, executable agents, or guaranteed capabilities. Use relevant areas for each task; do not claim an area was executed unless there is a recorded action and evidence.

## Start here

1. Read [the 100-area index](GAME_SKILLS_INDEX.md).
2. Follow [the execution workflow](SKILL_EXECUTION_WORKFLOW.md) before making a project change.
3. Apply [quality gates](QUALITY_GATES.md) appropriate to the change.
4. Record actual checks in [the test report](TEST_REPORT.md).
5. Record changed files, commits, links, and evidence in [the change evidence log](CHANGE_EVIDENCE_LOG.md).

## Operating rules

- Identify the exact repository, branch, goal, and protected files before editing.
- Inspect the current code and assets first. If the project is not accessible, report the blocker instead of guessing.
- For risky or user-protected assets, do not modify without explicit approval.
- Select only relevant skill areas and explain why they apply.
- Prefer small, reversible changes; use tests or a reproducible baseline when practical.
- Separate **Changed**, **Tested**, **Built**, **Deployed**, and **Runtime-verified**. These are different claims.
- A skill-area status must be one of: `planned`, `in progress`, `passed`, `failed`, or `blocked`.
- Mark a check `passed` only when evidence supports it. Link logs, commit IDs, screenshots, test outputs, or reproducible steps.
- Never claim all 100 areas ran just because the index exists.
- Do not promise revenue, security, compatibility, or quality without appropriate validation.

## Default task record

For every meaningful feature or fix, record:
- Goal and acceptance criteria
- Target repository / branch / commit
- Relevant skill-area IDs and reason for selection
- Files inspected and files changed
- Tests attempted and exact outcomes
- Known limitations / follow-up work
- Evidence URLs or reproducible steps

## Initial repository status

This repository starts as a workflow framework. No game project has been tested by these documents alone. Add real task records as work happens.
