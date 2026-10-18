# Active Game Task — SHADOWS OF THE LOST WORLD

- Date opened: 2026-10-18 (UTC)
- Status: in progress
- Game repository: [paz7azaab-lab/shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`
- Framework repository: [paz7azaab-lab/game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills), branch `main`
- Goal: build a polished third-person 3D exploration/survival adventure for Android in Godot 4, in staged, evidence-backed milestones.
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
Game source is in the dedicated game repository:
- [project.godot](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/project.godot) — Godot 4 configuration, landscape-first viewport, GL Compatibility renderer.
- [scenes/main.tscn](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scenes/main.tscn) — connects player, generated forest, ruin area, touch controls, and three shard pickups.
- [scripts/player_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/player_controller.gd) — third-person movement foundation.
- [scripts/forest_generator.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/forest_generator.gd) — primitive procedural trees, trunk collision, rocks, ruin/altar landmark.
- [scripts/mobile_controls.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/mobile_controls.gd) — touch directional buttons and interact button; E key mapping.
- [scripts/world_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/world_controller.gd) — HUD and three-shard exploration objective; nearby shard collection updates objective progress.
- [scripts/relic_pickup.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/relic_pickup.gd) — reusable pickup component/group registration.

## Latest milestone and evidence
- Confirmed GitHub writes: [relic_pickup.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/9760aa5b4ed9373c28ee0e96aa9d14ffc078fc29), [world_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b0ee22ef4bf6d11d71de32b718df9cc0507f80c3), [main.tscn](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/adbabee11ed9aefb97b1221ad6ca46bc8663b4dd).
- Fresh static audit fetched seven files from `main`: project config, main scene, player controller, forest generator, mobile controls, world controller, and pickup script.
- Static checks passed: configured main-scene path; every script path referenced by the scene exists; all three shard nodes exist and use the pickup script; objective counts to three; pickup group name matches; movement/interact controls are present.
- Not verified: GDScript parsing, Godot scene launch, real gameplay, touch on an actual phone, performance, Android export, or APK installation. The local environment previously had no `godot` or `godot4` executable.
- Built artifact: none. APK: none. Runtime-verified: no.
- Current art uses generated primitive meshes; this is a playable-design prototype target, not yet a polished finished game.

## Next milestones
1. Obtain access to a Godot 4 runtime and run import/parser/scene checks; fix any actual errors.
2. Add survival state and more interactions only after the current scene parses and runs.
3. Add animation, audio, higher-quality environment assets, responsive touch testing, and save/load.
4. Add security/privacy, performance, regression, and Android packaging checks before release claims.
