# Change Evidence Log

Record changes only after GitHub confirms them. A source commit is not proof of runtime success.

## Active project — SHADOWS OF THE LOST WORLD
- Date: 2026-10-18 (UTC)
- Status: in progress
- Game repository: [paz7azaab-lab/shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`.
- Workflow repository: this repository, branch `main`.
- Framework used: inspection, selected skill lenses, focused source changes, layered verification, and explicit blocked statuses from `SKILL_EXECUTION_WORKFLOW.md` and `QUALITY_GATES.md`.
- Relevant skill areas: 1, 4, 5, 11, 13, 15, 21, 22, 23, 27, 31, 32, 33, 41, 42, 43, 46, 47, 49, 50, 51, 52, 53, 69, 71, 73, 75, 79, 80, 83, 84, 85, 87, 89, 90, 92, 95, 98, 99, 100. These are chosen lenses, not installed plugins or automatically passed skills.

### Confirmed game-source commits
- [Main scene](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/adbabee11ed9aefb97b1221ad6ca46bc8663b4dd) — three shard placements and pickup component.
- [World controller survival loop](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/267950572245ca95543f4cbb277b872caa064188) — hunger/health state, wood/stone gatherables, resource HUD, campfire crafting and hunger restoration.
- [HUD layout warning fix](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b66cb329429a4dfc5c4585ee93ff8524a95d559b) — removed the explicit size assignment that conflicted with bottom-wide anchors.

### Verification evidence
- Freshly fetched `scripts/world_controller.gd` from `main`; confirmed the HUD sizing line was removed in the latest commit.
- GitHub Actions [run 39151090456](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151090456) succeeded on commit 267950572245ca95543f4cbb277b872caa064188. Godot 4.4.1 headless import/script parsing and main-scene smoke launch completed successfully.
- The smoke log showed a UI anchor/size warning. The follow-up fix is commit b66cb329429a4dfc5c4585ee93ff8524a95d559b; its new run [39151156526](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151156526) completed successfully. Godot 4.4.1 import/script parsing and the headless main-scene smoke launch passed on the HUD-fix commit.
- No APK has been built, no physical-device gameplay has been tested, and polished final art is not yet present.

## Evidence rules
- Preserve failed and blocked checks.
- Record exact commit/file links.
- A commit proves a change was committed, not that it works.
- Never record a test that was not run as passed.
- Keep secrets and private player data out of logs.
