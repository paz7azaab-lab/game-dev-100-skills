# Test Report

## Scope
- Framework: [game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills), branch `main`.
- Game: [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`.
- The framework repository records the workflow; it is not itself a game build.

## Results log

| Date (UTC) | Target | Check | Result | Evidence / Notes |
|---|---|---|---|---|
| 2026-10-18 | Game repo | Baseline source inspection | passed | Fetched project config, main scene, player controller, forest generator, world controller, pickup script and touch controls before the gameplay change. |
| 2026-10-18 | Game repo | Three-shard gameplay loop source update | passed (write confirmation only) | [pickup component](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/9760aa5b4ed9373c28ee0e96aa9d14ffc078fc29), [objective controller](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b0ee22ef4bf6d11d71de32b718df9cc0507f80c3), [scene placement](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/adbabee11ed9aefb97b1221ad6ca46bc8663b4dd). |
| 2026-10-18 | Game repo | Survival loop implementation | source committed | [Commit 267950572245ca95543f4cbb277b872caa064188](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/267950572245ca95543f4cbb277b872caa064188) adds hunger/health state, gatherable wood/stone, HUD counters and campfire crafting. |
| 2026-10-18 | Game repo | Godot 4.4.1 headless import/script parse | passed | [GitHub Actions run 39151090456](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151090456) completed successfully for commit 267950572245ca95543f4cbb277b872caa064188. |
| 2026-10-18 | Game repo | Headless main-scene smoke launch | passed with UI layout warning | Same run launched the main scene and exited successfully. Log showed a warning about setting size with non-equal opposite anchors; a follow-up source fix was committed. |
| 2026-10-18 | Game repo | HUD anchor warning fix | source committed; validation pending | [Commit b66cb329429a4dfc5c4585ee93ff8524a95d559b](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b66cb329429a4dfc5c4585ee93ff8524a95d559b) removes the conflicting explicit size assignment; fresh fetch confirmed the line is absent. [Run 39151156526](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151156526) completed successfully. The follow-up run confirms import/script parsing and headless scene launch succeed after the HUD fix. |
| 2026-10-18 | Game repo | Android APK export and physical-device test | not run | No APK built or tested. |

## Next checks
1. Confirm the latest validation run 39151156526 and review its logs for remaining warnings/errors.
2. Verify movement, gathering, crafting, hunger/health progression, all three shard pickups, touch input, and different screen sizes.
3. Add food, healing, saving/loading, enemies/combat and proper placeable base structures in separate testable milestones.
4. Build and test an Android APK only after engine and device checks pass.

## Evidence policy
A commit proves source was committed; a CI pass proves only the checks performed on that commit. Neither is proof of correct physical-device gameplay. Record exact commits and test evidence; never mark unrun tests as passed.

## Automated engine validation
- Workflow: [godot-validation.yml](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/.github/workflows/godot-validation.yml)
- It downloads Godot 4.4.1 on a GitHub-hosted runner, imports/parses the project in headless editor mode, launches the main scene for a short smoke test, and uploads logs.
