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
- Baseline inspected: `README.md`, `project.godot`, `scripts/player_controller.gd`, `scenes/main.tscn` fetched from the game repository before edits.
- Skill areas applied/planned for this milestone: 1, 4, 5, 11, 13, 15, 21, 22, 23, 27, 31, 32, 33, 41, 42, 43, 46, 47, 49, 50, 51, 52, 69, 71, 73, 75, 79, 80, 83, 84, 85, 87, 89, 90, 92, 95, 98, 99, 100.
- Confirmed game-repo writes during this task:
  - [scripts/forest_generator.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/forest_generator.gd) — procedural primitive forest, ruin landmark, rocks, and trunk collision.
  - [scripts/mobile_controls.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/mobile_controls.gd) — on-screen directional and interaction buttons, plus E input mapping.
  - [scripts/world_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/world_controller.gd) — objective HUD and relic collection interaction.
  - [scripts/player_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/player_controller.gd) — third-person movement input direction correction.
  - [scenes/main.tscn](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scenes/main.tscn) — connected world generator, player, relic, HUD controls and environment.
- Evidence status: GitHub connector confirmed successful commits for the listed writes. File re-fetch/static reference audit and Godot runtime checks must be recorded separately.
- Not claimed: no Android APK, successful Godot import/run, device performance, or gameplay runtime verification has been established.
- Follow-up: re-fetch all changed files, check scene/script paths and required node names, fix any discovered issues, then update test report with the precise outcomes.

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
