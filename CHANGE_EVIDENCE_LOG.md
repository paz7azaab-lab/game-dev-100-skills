# Change Evidence Log

Record changes only after GitHub confirms them. A source commit is not proof of runtime success.

## Framework setup
- Date: 2026-10-17 (UTC)
- Repository: [game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills), branch `main`.
- Purpose: practical, auditable workflow for applying game-development skill areas.
- Protected scope: game code belongs only in the dedicated game repository.

## Active project — SHADOWS OF THE LOST WORLD
- Date: 2026-10-18 (UTC)
- Status: in progress
- Game repository: [paz7azaab-lab/shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`.
- Workflow repository: this repository, branch `main`.
- Task record: [ACTIVE_PROJECTS/SHADOWS_OF_THE_LOST_WORLD.md](https://github.com/paz7azaab-lab/game-dev-100-skills/blob/main/ACTIVE_PROJECTS/SHADOWS_OF_THE_LOST_WORLD.md)
- Framework used: intake/inspection, relevant skill selection, focused changes, layered verification, and explicit blocked statuses from `SKILL_EXECUTION_WORKFLOW.md` and `QUALITY_GATES.md`.
- Relevant skill areas: 1, 4, 5, 11, 13, 15, 21, 22, 23, 27, 31, 32, 33, 41, 42, 43, 46, 47, 49, 50, 51, 52, 53, 69, 71, 73, 75, 79, 80, 83, 84, 85, 87, 89, 90, 92, 95, 98, 99, 100. These are chosen lenses, not installed plugins or automatically passed skills.

### Confirmed game-source commits
- [project.godot](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/project.godot) — project config and mobile landscape-oriented viewport.
- [scenes/main.tscn](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/adbabee11ed9aefb97b1221ad6ca46bc8663b4dd) — adds three shard placements and connects the pickup component.
- [scripts/player_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/player_controller.gd) — player movement foundation.
- [scripts/forest_generator.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/forest_generator.gd) — primitive trees, trunk collision, rocks, and ancient ruin landmark.
- [scripts/mobile_controls.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/mobile_controls.gd) — directional touch controls and interaction input.
- [scripts/world_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b0ee22ef4bf6d11d71de32b718df9cc0507f80c3) — objective HUD and collect-nearby-shard loop, with progress to three.
- [scripts/relic_pickup.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/9760aa5b4ed9373c28ee0e96aa9d14ffc078fc29) — reusable pickup group component.

### Fresh verification pass
- Re-fetched seven game files from `main`: project.godot, scenes/main.tscn, player_controller.gd, forest_generator.gd, mobile_controls.gd, world_controller.gd, relic_pickup.gd.
- Static checks passed for: main-scene configuration; all scene-referenced script files present; three shard nodes assigned the pickup script; three-shard objective logic present; pickup group name consistent; movement and interaction controls present.
- Runtime checks remain blocked/not run because no Godot 4 executable was available in the environment. No Android APK has been built; no phone gameplay has been tested. Do not claim runtime success.
- Framework records updated: [task record](https://github.com/paz7azaab-lab/game-dev-100-skills/blob/main/ACTIVE_PROJECTS/SHADOWS_OF_THE_LOST_WORLD.md), [test report](https://github.com/paz7azaab-lab/game-dev-100-skills/blob/main/TEST_REPORT.md).

## Template for future milestones
- Date:
- Target repo/branch/base commit:
- Goal and observable acceptance criteria:
- Selected skill IDs and why:
- Files inspected/changed:
- Exact commits:
- Tests/checks and results:
- Built artifact/runtime status:
- Blockers and next milestone:

## Evidence rules
- Preserve failed and blocked checks.
- Record exact commit/file links.
- A commit proves that a change was committed, not that it works.
- Never record a test that was not run as passed.
- Keep secrets and private player data out of logs.
