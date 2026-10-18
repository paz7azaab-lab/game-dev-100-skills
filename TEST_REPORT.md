# Test Report

## Framework repository baseline
- Repository: `paz7azaab-lab/game-dev-100-skills`
- Branch: `main`
- Purpose: workflow and evidence framework; the game source lives in a separate repository.
- The framework repository itself is not a game build and has no Android APK by default.

## Results log

| Date (UTC) | Target / commit | Check | Result | Evidence / Notes |
|---|---|---|---|---|
| 2026-10-17 | Initial setup | Repository access and empty-repo inspection | passed | Repository existence and write access were checked before the first commit. |
| 2026-10-17 | Initial setup | Game build/runtime tests in framework repo | blocked / not applicable | This repository contains workflow documentation only. |
| 2026-10-18 | [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world) | Baseline file inspection | passed | GitHub connector fetched README.md, project.godot, scripts/player_controller.gd, and scenes/main.tscn before edits. |
| 2026-10-18 | [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world) | Initial milestone source writes | passed (write confirmation only) | GitHub confirmed commits for the forest generator, mobile controls, world controller, player controller, project configuration, and main scene. This is not a runtime pass. |
| 2026-10-18 | [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world) | Re-fetch and static cross-file audit | passed | All six active project/config/script/scene files were re-fetched. Text checks confirmed main scene config, referenced script paths, required node names, relic-node lookup, and interaction-action registration. Static checks do not prove GDScript parses or the game runs. |
| 2026-10-18 | [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world) | Godot import/parse/run | blocked / not run | Checked local environment; neither `godot` nor `godot4` executable is installed. |
| 2026-10-18 | [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world) | Android export and device test | blocked / not run | No APK has been built or tested on an Android device. |

## Next checks
- Run Godot 4 import and parser checks when an engine runtime is available; fix all errors before expanding the game.
- Test movement, collisions, objective completion, touch input, and screen-size behavior.
- Export and test on Android only after editor/runtime checks pass.

## How to add a test result
For every actual run, record:
- Date/time (UTC)
- Commit SHA
- Command or manual steps and environment/device
- Expected outcome
- Actual outcome and exit code, if available
- Result: passed / failed / blocked
- Log, screenshot, artifact, or reproducible evidence link

Never convert a test that was not run into a pass. A commit proves that a change was committed, not that the game runs.
