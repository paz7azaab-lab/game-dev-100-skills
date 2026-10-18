# Active Game Task — SHADOWS OF THE LOST WORLD

- Date opened: 2026-10-18 (UTC)
- Status: in progress
- Game repository: [paz7azaab-lab/shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world)
- Game branch: `main`
- Framework repository: [paz7azaab-lab/game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills), branch `main`
- Goal: build a polished third-person 3D exploration/survival adventure for Android in Godot 4, in incremental, evidence-backed milestones.
- Protected scope: do not edit any other game repository; only change the dedicated Shadows repo. Do not claim a working game or APK without runtime/build evidence.
- Acceptance criteria for the first playable milestone:
  1. Project structure and main scene references are internally consistent.
  2. Player can move in a 3D environment using keyboard/editor controls.
  3. Mobile touch movement UI is present and connected to movement.
  4. Environment contains readable forest/ruin landmarks rather than only a flat plane.
  5. Verification status distinguishes static inspection from Godot runtime and Android device tests.

## Skill areas selected
- 1 Product Vision & Audience; 4 Game Design Fundamentals; 5 Core Gameplay Loop.
- 11 Worldbuilding & Lore; 13 Level Design; 15 Mission & Objective Design.
- 21 Art Direction; 22 Visual Readability; 23 UI/UX Design; 27 3D Modeling & Materials; 31 3D Graphics & Rendering; 32 Lighting & Composition; 33 Camera Design.
- 41 Language & Runtime Fundamentals; 42 Code Organization; 43 Software Architecture; 46 Input Handling; 47 UI Implementation; 49 Error Handling & Logging; 50 Dependency & Build Management.
- 51 Character & Unit Controllers; 52 Physics & Collision; 53 AI Behavior.
- 69 Mobile Lifecycle; 71 Performance Profiling; 73 GPU & Overdraw Optimization; 75 Battery & Thermal Awareness; 79 Compatibility Matrix; 80 Accessibility & Reduced Motion.
- 83 Automated Testing; 84 Gameplay Testing; 85 Regression Testing; 87 Evidence-Based Debugging; 89 Acceptance Testing; 90 End-to-End Validation; 92 Completion Audit; 95 Build & Packaging Validation.
- 98 Revenue Forge; 99 Security & Anti-Cheat Review; 100 User Privacy & Safety.
- These are selected workflow lenses, not 100 installed plugins. No skill is marked passed just because it was selected.

## Current implementation evidence
GitHub confirmed commits and a subsequent file re-fetch/static reference audit for these game files:
- [project.godot](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/project.godot) — commit `494bc19f81c9ec11f5df6a607b01cf304ca10475`; Godot 4 project config, GL Compatibility renderer, landscape-first viewport.
- [scenes/main.tscn](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scenes/main.tscn) — commit `29a0bf6ce2555773e802b11893b73558b56ed6f4`; connects the player, environment, forest generator, relic and controls.
- [scripts/player_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/player_controller.gd) — commit `d8a2528c11b723bad32cf9e20b1dc58a74410f61`; movement direction correction.
- [scripts/forest_generator.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/forest_generator.gd) — commit `76e1016d29abbb1794641533b100b570f30e2d63`; procedural primitive trees, trunk collisions, rocks, and a ruin/altar landmark.
- [scripts/mobile_controls.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/mobile_controls.gd) — commit `455a026f5f70ed7b4756c602e8bf1fcca101981d`; on-screen directional and interaction buttons, E key mapping.
- [scripts/world_controller.gd](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/scripts/world_controller.gd) — commit `6662cc1ac7961829a72026170708f576ee6873ea`; objective HUD and proximity-gated relic collection.
- [README.md](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/README.md) — project intent and honest verification boundaries.

## Verification status
- Passed: GitHub connector confirmed writes; all six active game project/config/script/scene files were re-fetched from `main`.
- Passed: static text checks confirmed configured main-scene path, all four referenced scripts exist, required scene node names exist, and the controller's referenced relic node matches the scene.
- Blocked / not run: Godot import, GDScript parser, scene launch, gameplay, Android export, and real-device touch/performance tests. A local environment check found no `godot` or `godot4` executable.
- Built artifact: none. APK: none.
- Runtime-verified: no.
- Important limitation: static text checks do not prove GDScript parses or the game runs. The current scene uses generated primitive visuals and is an early prototype, not a finished game.

## Next steps
1. Run Godot 4 import and parser checks when an engine runtime is available; fix all reported issues.
2. Test movement, collisions, objective completion, touch input, and screen-size behavior.
3. Expand the core loop with exploration, interaction, inventory, enemies, health, save/load, audio, animation, and richer assets in staged commits.
4. Add security/privacy, performance, regression, and Android packaging checks before any release claim.
