# Change Evidence Log

Record changes only after the repository/tool confirms them. Keep evidence close to the claim.

## Initial workflow setup
- Date: 2026-10-17 (UTC)
- Repository: [paz7azaab-lab/game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills)
- Target branch: `main`
- Goal: establish a practical, auditable workflow for selecting and applying game-development skill areas.
- Initial repository inspection: repository was public and empty; no files or commit history existed before initialization.
- Protected scope: this repository only. Do not change any separate game repository as part of this setup.

## Active game task — SHADOWS OF THE LOST WORLD
- Date: 2026-10-18 (UTC)
- Status: in progress
- Target game repository: [paz7azaab-lab/shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`
- Framework repository: this repository, branch `main`
- Task record: [ACTIVE_PROJECTS/SHADOWS_OF_THE_LOST_WORLD.md](https://github.com/paz7azaab-lab/game-dev-100-skills/blob/main/ACTIVE_PROJECTS/SHADOWS_OF_THE_LOST_WORLD.md)
- Goal: incrementally build a third-person 3D exploration/survival game for Android in Godot 4, using selected skill areas and quality gates.
- Baseline inspected before edits: `README.md`, `project.godot`, `scripts/player_controller.gd`, and `scenes/main.tscn` fetched from the game repository.
- Skill areas selected for this milestone: 1, 4, 5, 11, 13, 15, 21, 22, 23, 27, 31, 32, 33, 41, 42, 43, 46, 47, 49, 50, 51, 52, 69, 71, 73, 75, 79, 80, 83, 84, 85, 87, 89, 90, 92, 95, 98, 99, 100. Selection does not mean each skill has passed.
- Confirmed game-repo files and latest relevant commits:
  - [project.godot](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/project.godot) — `494bc19f81c9ec11f5df6a607b01cf304ca10475`; Godot project config and landscape-first viewport.
  - [scenes/main.tscn](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scenes/main.tscn) — `29a0bf6ce2555773e802b11893b73558b56ed6f4`; scene wiring.
  - [scripts/player_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/player_controller.gd) — `d8a2528c11b723bad32cf9e20b1dc58a74410f61`; movement direction correction.
  - [scripts/forest_generator.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/forest_generator.gd) — `76e1016d29abbb1794641533b100b570f30e2d63`; generated trees, trunk collisions, rocks, and ruin landmark.
  - [scripts/mobile_controls.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/mobile_controls.gd) — `455a026f5f70ed7b4756c602e8bf1fcca101981d`; touch buttons and interaction input mapping.
  - [scripts/world_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/world_controller.gd) — `6662cc1ac7961829a72026170708f576ee6873ea`; objective HUD and relic collection.
- Static audit: all six active project/config/script/scene files were re-fetched from `main`. Text checks passed for configured main scene, referenced script paths, required node names, relic node lookup, and interaction action registration. This does not prove the GDScript parser or runtime passes.
- Runtime/build status: local environment check found neither `godot` nor `godot4` executable. Godot import/parse/run, Android export, device touch tests, and performance tests are blocked/not run. No APK exists; runtime-verified = no.
- Framework updates: task record updated in commit `549299d54609a463af17f2ee8bdb35ef3eb09bb2`; test report updated with static-audit and runtime-blocker evidence in commit `ae973ca8890ea7a3ce7ee34cb02a7285ca6393f5`.
- Follow-up: obtain a Godot 4 runtime for parser/import and play tests; then continue with exploration, interactions, inventory, enemies, health, save/load, audio/animation, and Android packaging.

## Task record template

### [Task title]
- Date:
- Status: planned / in progress / passed / failed / blocked
- Target repository:
- Branch:
- Base commit:
- Goal:
- Acceptance criteria:
- Protected files/assets:
- Selected skill IDs and why:
- Files inspected:
- Files changed:
- Tests/checks run:
- Results:
- Built artifact (if any):
- Deployment/runtime verification (if any):
- Known limitations:
- Evidence links (commit, diff, test logs, screenshots, artifact):
- Follow-up:

## Evidence rules
- Cite exact commit SHA and changed file paths.
- Use direct GitHub links where available.
- Keep failed/blocked checks in the record; do not erase them to make a task appear complete.
- A commit proves that a change was committed, not that it passed tests or works at runtime.
- Screenshots should identify the build/version and device when relevant; do not expose private player data.
