# Skill Execution Workflow

## 1. Intake — before touching files
Create a task record with:
- Goal, target players, platform, and current version
- Exact repository and branch; current commit SHA
- Acceptance criteria written as observable outcomes
- Protected files/assets and explicit permission boundaries
- Known risks and what is out of scope

If the repo, branch, assets, or user permission is unclear, inspect or ask before editing.

## 2. Inspect the real project
- Read project docs, directory structure, manifests, scripts, and relevant source/assets.
- Identify engine/runtime and target platform from files, not assumptions.
- Check working-tree/diff or latest commit where available.
- Establish a reproducible baseline or write a failing/reproducible test when practical.
- Do not use this framework as evidence that another project was inspected.

## 3. Select skill areas
- Choose the smallest useful subset of IDs from `GAME_SKILLS_INDEX.md`.
- For each ID, write why it applies and what check will produce evidence.
- Include security/privacy and mobile/performance checks when the feature touches those concerns.
- Do not mark all 100 as executed by default.

## 4. Plan a focused change
- List files expected to change and intended behavior.
- Identify rollback strategy and risks.
- Prefer small, reversible edits. Preserve user-designated protected assets.
- For uncertain or high-impact changes, propose the plan and wait for approval.

## 5. Implement
- Keep changes tied to acceptance criteria.
- Avoid unrelated refactors.
- Record meaningful deviations and why they were necessary.
- Never include secrets, access tokens, private keys, or personal data in logs.

## 6. Verify in layers
1. Static review: diff, syntax, references, configuration.
2. Narrow checks: relevant unit/integration tests or reproducible manual steps.
3. Project checks: existing test/build commands, when available.
4. Platform check: actual target device/runtime when available.
5. Fresh final pass: acceptance criteria, changed files, protected assets, and evidence.

A successful build is not proof that gameplay works. Source edits are not proof of deployment. A screenshot is not proof of every device size.

## 7. Record status honestly
Allowed statuses:
- `planned`: identified but not attempted
- `in progress`: work/check has started
- `passed`: acceptance check passed with evidence
- `failed`: check was run and failed
- `blocked`: could not run because of a specific missing dependency/access/device/permission

Use separate delivery labels:
- **Changed**: exact files and commit confirmed
- **Tested**: checks and results recorded
- **Built**: artifact was actually produced and located
- **Deployed**: target deployment/service confirms it
- **Runtime-verified**: relevant flow was exercised in the actual runtime/device

## 8. Close the task
Update the task record, test report, and change evidence log. Note remaining issues, test gaps, and next steps. Do not call the task complete if critical acceptance criteria remain failed or unverified.
