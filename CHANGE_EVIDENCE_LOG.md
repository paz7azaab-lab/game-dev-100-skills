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
- [project.godot](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/project.godot) — Godot 4 configuration and landscape-first viewport.
- [scenes/main.tscn](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/adbabee11ed9aefb97b1221ad6ca46bc8663b4dd) — three shard placements and pickup component.
- [scripts/player_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/player_controller.gd) — third-person movement foundation.
- [scripts/forest_generator.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/forest_generator.gd) — primitive procedural trees, trunk collision, rocks and ruin landmark.
- [scripts/mobile_controls.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/mobile_controls.gd) — touch movement and interact button.
- [scripts/relic_pickup.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/9760aa5b4ed9373c28ee0e96aa9d14ffc078fc29) — reusable pickup group component.
- [scripts/world_controller.gd — survival loop](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/267950572245ca95543f4cbb277b872caa064188) — hunger/health state, wood/stone gatherables, resource counters and a craftable campfire that restores hunger.

### Verification
- Freshly fetched the changed `scripts/world_controller.gd` from `main`; its content matches the commit.
- Static review: survival state and HUD updates are present; resource nodes are created at fixed world positions; interaction prioritizes nearby shards, then resources, then campfire crafting when the required supplies are available.
- GitHub Actions run [39151090456](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151090456) was `in_progress` at last check. It has not yet been counted as a pass.
- Earlier validation run [39142756702](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39142756702) succeeded for the workflow setup commit only; it does not validate the later survival code.
- No APK has been built, no physical-device gameplay has been tested, and polished final art is not yet present.

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
