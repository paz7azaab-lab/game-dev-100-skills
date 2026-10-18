# Active Game Task — SHADOWS OF THE LOST WORLD

- Date opened: 2026-10-18 (UTC)
- Status: in progress
- Game repository: [paz7azaab-lab/shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`
- Framework repository: [paz7azaab-lab/game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills), branch `main`
- Chosen direction: third-person 3D open-world survival adventure with exploration, resource gathering, base-building progression and RPG elements. Build single-player core first; consider online co-op only after offline play is stable.
- Target: polished, high-quality Android game built in stages with evidence-backed milestones.
- Protected scope: only edit the dedicated Shadows repo for game code; do not alter the older game repository. Do not claim a working game or APK without runtime/build evidence.

## Skill framework use
Selected skill areas guide concrete decisions and checks; they are not plugins installed into ChatGPT, and selection alone is not a pass:
- Vision/gameplay: 1, 4, 5, 11, 13, 15.
- Art/readability/UI/3D: 21, 22, 23, 27, 31, 32, 33.
- Code/input/architecture: 41, 42, 43, 46, 47, 49, 50, 51, 52, 53.
- Mobile/performance/accessibility: 69, 71, 73, 75, 79, 80.
- Test/verification/release: 83, 84, 85, 87, 89, 90, 92, 95.
- Monetization/security/privacy: 98, 99, 100.

## Current implementation
- [project.godot](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/project.godot) — Godot 4 configuration, landscape-first viewport, GL Compatibility renderer.
- [main scene](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scenes/main.tscn) — player, generated forest, ruin landmark, touch controls and three shard pickups.
- [player controller](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/player_controller.gd) — third-person movement foundation.
- [forest generator](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/forest_generator.gd) — primitive procedural trees, trunk collision, rocks and ruins.
- [mobile controls](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/mobile_controls.gd) — touch directional buttons and interaction input.
- [pickup component](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/relic_pickup.gd) — shard group registration.
- [survival loop](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/267950572245ca95543f4cbb277b872caa064188) — health/hunger state, wood/stone gathering, survival HUD and one-time campfire crafting that restores hunger.
- [HUD anchor warning fix](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b66cb329429a4dfc5c4585ee93ff8524a95d559b) — removed conflicting explicit sizing from the bottom-wide status label.

## Verification
- [Run 39151090456](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151090456) succeeded for commit 267950572245ca95543f4cbb277b872caa064188: Godot 4.4.1 headless import/script parse and main-scene smoke launch both exited successfully.
- The smoke log showed a HUD anchor/size warning. Fix committed as b66cb329429a4dfc5c4585ee93ff8524a95d559b. [Run 39151156526](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151156526) completed successfully; Godot import/script parsing and headless main-scene smoke launch passed on the HUD-fix commit.
- Not verified: physical phone input, actual rendered visual quality, performance, Android export, or APK installation.
- Built artifact: none. APK: none. Phone runtime test: no.
- Current visuals are primitive generated meshes, not polished final art.

## Next milestones
1. Confirm latest run 39151156526 and review logs for remaining warnings/errors.
2. Test gameplay paths: gathering, campfire crafting, hunger/health, all shard pickups, touch input and screen sizes.
3. Add food/healing, save/load, enemies/combat and placeable base structures as separate testable milestones.
4. Improve character/environment art, animation, lighting and audio within mobile performance constraints.
5. Consider online co-op only after single-player, persistence and stability are proven.
6. Build and test an Android APK only after a reproducible export setup is available.

## Release discipline
A source commit, CI pass, Android build, APK inspection, and physical-device runtime test are different evidence levels. Report each separately. No revenue or commercial success is guaranteed.


## Mandatory 100-skill operating rule (user requirement, 2026-10-18)
For every meaningful project phase and feature, consult the complete `GAME_SKILLS_INDEX.md` (all 100 areas), not only the initially selected list. Create/update a per-milestone skill matrix that records each area as `planned`, `in progress`, `passed`, `failed`, `blocked`, or `not applicable`, with a short reason and evidence/check where relevant. Apply every relevant skill area to real decisions and implementation; include cross-cutting mobile, performance, test, security/privacy, and commercial-readiness reviews whenever applicable.

Important integrity rule: reviewing all 100 is mandatory, but it is not truthful to claim that all 100 were actively executed or passed for every change. Areas that do not apply to the current milestone must be marked `not applicable` with a reason; unverified areas remain `planned` or `blocked`. The skill matrix is a workflow requirement, not a claim that 100 separate tools/plugins are installed.

## Current browser-alpha branch note
A browser-based Three.js alpha has been added at `index.html` to satisfy the user's instruction to avoid Godot for the playable version. GitHub Actions browser tests have passed on earlier commits; later documentation/workflow commits triggered fresh runs that must be checked separately. GitHub Pages deployment is not confirmed; a deployment attempt failed because repository Pages setup/permissions were unavailable. Do not claim a public live URL until a deployment run succeeds. The legacy Godot source still exists in this repository, but it is not needed to run the browser alpha.
