# Active Game Task — SHADOWS OF THE LOST WORLD

- Date opened: 2026-10-18 (UTC)
- Status: in progress
- Game repository: [paz7azaab-lab/shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`
- Framework repository: [paz7azaab-lab/game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills), branch `main`
- Chosen direction: third-person 3D open-world survival adventure with exploration, resource gathering, base-building progression and RPG elements. Build single-player core first; consider online co-op only after the offline game is stable.
- Target: polished, high-quality Android game built in stages with evidence-backed milestones.
- Protected scope: only edit the dedicated Shadows repo for game code; do not alter the older game repository. Do not claim a working game or APK without runtime/build evidence.

## Skill framework use
The selected skill areas below guide concrete decisions and checks; they are not plugins installed into ChatGPT, and selection alone is not a pass:
- Vision/gameplay: 1, 4, 5, 11, 13, 15.
- Art/readability/UI/3D: 21, 22, 23, 27, 31, 32, 33.
- Code/input/architecture: 41, 42, 43, 46, 47, 49, 50, 51, 52, 53.
- Mobile/performance/accessibility: 69, 71, 73, 75, 79, 80.
- Test/verification/release: 83, 84, 85, 87, 89, 90, 92, 95.
- Monetization/security/privacy: 98, 99, 100.

## Current implementation
- [project.godot](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/project.godot) — Godot 4 configuration, landscape-first viewport, GL Compatibility renderer.
- [scenes/main.tscn](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scenes/main.tscn) — player, generated forest, ruin landmark, touch controls, three shard pickups.
- [scripts/player_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/player_controller.gd) — third-person movement foundation.
- [scripts/forest_generator.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/forest_generator.gd) — primitive procedural trees, trunk collision, rocks and ruins.
- [scripts/mobile_controls.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/mobile_controls.gd) — touch directional buttons and interact input.
- [scripts/relic_pickup.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/relic_pickup.gd) — pickup group registration.
- [scripts/world_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/267950572245ca95543f4cbb277b872caa064188) — health/hunger state, wood and stone gathering, survival HUD, and one-time campfire crafting that restores hunger.

## Latest milestone and evidence
- Commit: [267950572245ca95543f4cbb277b872caa064188](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/267950572245ca95543f4cbb277b872caa064188).
- Fresh source fetch of `scripts/world_controller.gd` confirmed the committed content.
- Static review indicates the intended survival state, HUD, gatherable objects and campfire crafting paths are present.
- GitHub Actions validation run [39151090456](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151090456) was still in progress at last check. Do not call this commit runtime-tested until the run concludes and logs are reviewed.
- Earlier run [39142756702](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39142756702) succeeded on the workflow setup commit, not on the current survival commit.
- Not yet verified: Godot parsing for the latest commit, scene launch, actual gameplay, touch on a physical phone, performance, Android export or APK installation.
- Built artifact: none. APK: none. Runtime-verified on phone: no.
- Visuals remain mostly primitive generated meshes; quality-art pass remains ahead.

## Next milestones
1. Inspect run 39151090456 and its logs after completion; fix concrete parse/runtime errors before adding more systems.
2. Verify resource gathering, hunger/health progression, campfire crafting and all three shard pickups.
3. Add food and healing, save/load, enemies/combat, and proper placeable base structures in separate testable milestones.
4. Improve character, environment, animation, lighting and audio with mobile performance constraints.
5. Consider online co-op only after the single-player loop, persistence and stability are proven.
6. Build and test Android APK when automated engine checks pass and a reproducible export setup is available.

## Release discipline
A source commit, static review, CI pass, Android build, APK inspection, and physical-device runtime test are different evidence levels. Report each separately. No revenue or commercial success is guaranteed.
