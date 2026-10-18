# Test Report

## Scope
- Framework: [game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills), branch `main`.
- Game: [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`.
- The framework repository records the workflow; it is not itself a game build.

## Results log

| Date (UTC) | Target | Check | Result | Evidence / Notes |
|---|---|---|---|---|
| 2026-10-17 | Framework repo | Repository access and empty-repo inspection | passed | Access and write permissions were checked before framework initialization. |
| 2026-10-18 | Game repo | Baseline inspection | passed | Fetched project config, main scene, player controller, forest generator, world controller, pickup script and touch controls before the latest gameplay change. |
| 2026-10-18 | Game repo | Source writes for forest, touch controls, objective HUD and scene | passed (write confirmation only) | GitHub confirmed source commits. A write confirmation is not a runtime test. |
| 2026-10-18 | Game repo | Three-shard gameplay loop source update | passed (write confirmation only) | [pickup component](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/9760aa5b4ed9373c28ee0e96aa9d14ffc078fc29), [objective controller](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b0ee22ef4bf6d11d71de32b718df9cc0507f80c3), [scene placement](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/adbabee11ed9aefb97b1221ad6ca46bc8663b4dd). |
| 2026-10-18 | Game repo | Survival loop implementation | source committed; runtime pending | [Commit 267950572245ca95543f4cbb277b872caa064188](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/267950572245ca95543f4cbb277b872caa064188) adds hunger/health state, gatherable wood/stone, HUD counters and campfire crafting. |
| 2026-10-18 | Game repo | Fresh fetch of changed controller | passed | Fetched `scripts/world_controller.gd` from `main`; content matches the committed survival loop. |
| 2026-10-18 | Game repo | GitHub Actions Godot validation for survival commit | in progress at last check | [Run 39151090456](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151090456) was `in_progress`; no conclusion available yet. |
| 2026-10-18 | Game repo | Earlier CI run for workflow setup commit | passed | [Run 39142756702](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39142756702) completed with conclusion `success`. This validates the earlier commit only, not the new survival changes. |
| 2026-10-18 | Game repo | Android APK export and device test | blocked / not run | No APK built or tested. |

## Next checks
1. Read the active GitHub Actions result and logs for commit 267950572245ca95543f4cbb277b872caa064188; fix real parser/runtime errors if found.
2. Exercise movement, gathering, crafting, hunger/health behavior, collecting all three shards, touch input, and different screen sizes.
3. Improve the survival loop with food, saving/loading, enemies, and a proper base-building placement system after current checks pass.
4. Build and test an Android APK only after engine and device checks pass.

## Evidence policy
For every actual run, record date/time, commit, command/manual steps, environment/device, expected and actual result, exit code where available, and a log/artifact link. A commit is not a runtime pass. Never mark an unrun test as passed.

## Automated engine validation
- Workflow: [godot-validation.yml](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/.github/workflows/godot-validation.yml)
- It downloads Godot 4.4.1 on a GitHub-hosted runner, imports/parses the project in headless editor mode, launches the main scene for a short smoke test, and uploads logs.
- Latest observed run is listed above. Never infer success until its conclusion and job logs are checked.
