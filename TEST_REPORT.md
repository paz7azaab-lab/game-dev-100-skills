# Test Report

## Scope
- Framework: [game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills), branch `main`.
- Game: [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`.
- The framework repository records the workflow; it is not itself a game build.

## Results log

| Date (UTC) | Target | Check | Result | Evidence / Notes |
|---|---|---|---|---|
| 2026-10-17 | Framework repo | Repository access and empty-repo inspection | passed | Access and write permissions were checked before framework initialization. |
| 2026-10-18 | Game repo | Baseline inspection | passed | Fetched project config, main scene, player controller, and forest generator before editing. |
| 2026-10-18 | Game repo | Source writes for forest, touch controls, objective HUD and scene | passed (write confirmation only) | GitHub confirmed source commits. A write confirmation is not a runtime test. |
| 2026-10-18 | Game repo | Three-shard gameplay loop source update | passed (write confirmation only) | Commits: [pickup component](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/9760aa5b4ed9373c28ee0e96aa9d14ffc078fc29), [objective controller](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b0ee22ef4bf6d11d71de32b718df9cc0507f80c3), [scene placement](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/adbabee11ed9aefb97b1221ad6ca46bc8663b4dd). |
| 2026-10-18 | Game repo | Fresh fetch of seven project files | passed | Fetched project.godot, scenes/main.tscn, player_controller.gd, forest_generator.gd, mobile_controls.gd, world_controller.gd, relic_pickup.gd from `main`. |
| 2026-10-18 | Game repo | Static cross-file checks | passed | Main scene configured; every script referenced by scene exists; three shard nodes use pickup script; objective counts to three; pickup group names match; movement/interact controls are present. This is text/static validation only. |
| 2026-10-18 | Game repo | Godot import, GDScript parse, scene launch, actual gameplay | blocked / not run | No Godot 4 runtime executable available in this environment. |
| 2026-10-18 | Game repo | Android APK export and device test | blocked / not run | No APK built or tested. |

## Next checks
1. Run Godot 4 import and parser checks when an engine runtime is available.
2. Exercise movement, collisions, collecting all three shards, touch input, and different screen sizes.
3. Add more systems after the prototype is confirmed to parse and run.
4. Build and test an APK only after engine and device checks pass.

## Evidence policy
For every actual run, record date/time, commit, command/manual steps, environment/device, expected and actual result, exit code where available, and a log/artifact link. A commit is not a runtime pass. Never mark an unrun test as passed.


## Automated engine validation added — 2026-10-18
- Workflow file committed to the game repository: [godot-validation.yml](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/.github/workflows/godot-validation.yml)
- Workflow commit: 57f80112166f3ad0b0726161f66bdc7eacb6cdb8
- Intended checks: download Godot 4.4.1, import project/parse scripts in headless editor mode, launch main scene headlessly for a short smoke test, upload logs.
- Current result: **pending / not verified**. The GitHub connector returned no commit status checks for the workflow-file commit at the time of inspection. No successful workflow run or APK is claimed.
