# Test Report

## Scope
- Framework: [game-dev-100-skills](https://github.com/paz7azaab-lab/game-dev-100-skills), branch `main`.
- Game: [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world), branch `main`.
- Current game HEAD inspected: `050a61ebaddf3ff1054a6ccaadc6114b3e4570cb`.
- The framework repository records the workflow; it is not itself a game build.

## Results log

| Date (UTC) | Target | Check | Result | Evidence / Notes |
|---|---|---|---|---|
| 2026-10-18 | Game repo | Baseline source inspection | passed | Fetched project config, main scene, player controller, forest generator, world controller, pickup script and touch controls before the gameplay change. |
| 2026-10-18 | Game repo | Three-shard gameplay loop source update | passed (write confirmation only) | [pickup component](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/9760aa5b4ed9373c28ee0e96aa9d14ffc078fc29), [objective controller](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b0ee22ef4bf6d11d71de32b718df9cc0507f80c3), [scene placement](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/adbabee11ed9aefb97b1221ad6ca46bc8663b4dd). |
| 2026-10-18 | Game repo | Survival loop implementation | source committed | [Commit 267950572245ca95543f4cbb277b872caa064188](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/267950572245ca95543f4cbb277b872caa064188) adds hunger/health state, gatherable wood/stone, HUD counters and campfire crafting. |
| 2026-10-18 | Game repo | Godot 4.4.1 headless import/script parse | passed | [GitHub Actions run 39151090456](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151090456) completed successfully for commit 267950572245ca95543f4cbb277b872caa064188. |
| 2026-10-18 | Game repo | Headless main-scene smoke launch | passed with UI layout warning | Same run launched the scene; follow-up source fix addressed the warning. |
| 2026-10-18 | Game repo | HUD anchor warning fix | passed in follow-up CI | [Commit b66cb329429a4dfc5c4585ee93ff8524a95d559b](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/commit/b66cb329429a4dfc5c4585ee93ff8524a95d559b); [run 39151156526](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39151156526) completed successfully. |
| 2026-10-18 | Browser alpha | Latest browser test workflow on inspected HEAD | passed | [Run 39152053859](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/actions/runs/39152053859), head SHA `050a61ebaddf3ff1054a6ccaadc6114b3e4570cb`; job `browser-tests` and step `npm test` completed successfully. The test source defines five tests: canvas/HUD startup; campfire crafting state/cost/reward; three-shard objective completion; keyboard movement; phone-sized viewport controls/overflow. |
| 2026-10-19 | Framework repo | 100-skill status matrix | recorded and re-fetched | [SHADOWS_100_SKILL_STATUS.md](https://github.com/paz7azaab-lab/game-dev-100-skills/blob/main/ACTIVE_PROJECTS/SHADOWS_100_SKILL_STATUS.md) contains 100 rows, one per skill ID, with honest status and project-specific reason/evidence. Only skill #83 is marked passed, scoped to the automated test workflow; many other areas remain in progress/planned/not applicable. |
| 2026-10-18 onward | Game repo | Android APK export and physical-device test | not run | No APK built or tested. |

## What the browser CI does and does not prove
- Proven for the current inspected commit: the five automated browser assertions above pass in GitHub-hosted headless Chromium.
- Not proven: physical Android touch input, APK export/installation, final visual quality, measured performance, save/load, enemy/combat behavior, networked play, security penetration testing, store readiness, or a public Pages deployment.
- The resource/crafting test sets resource counts through a test debug interface before checking crafting. It does not fully prove natural resource-gathering behavior.
- The mobile viewport test checks control visibility and horizontal overflow, not real touch interaction on a phone.

## Next checks
1. Add tests for actual resource pickup, repeated/invalid crafting, hunger/health edge cases, visibility/resize/orientation, and runtime errors.
2. Exercise touch controls in a real mobile browser/device when available.
3. Implement and test save/load, combat and placeable base structures as separate milestones.
4. Build and inspect an Android package only after a reproducible export setup is available.

## Evidence policy
A commit proves a source change was committed; a CI pass proves only the checks performed on that commit. Neither proves physical-device gameplay. Never mark unrun tests as passed.

## Automated engine validation (legacy source)
- Workflow: [godot-validation.yml](https://github.com/paz7azaab-lab/shadows-of-the-lost-world/blob/main/.github/workflows/godot-validation.yml).
- Earlier Godot headless import and main-scene smoke checks passed on the cited commits. The active playable browser alpha is the Three.js implementation in `index.html`; legacy Godot files remain in the repository but are not needed to run the browser alpha.
