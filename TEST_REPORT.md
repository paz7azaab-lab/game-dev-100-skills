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
| 2026-10-18 | [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world) | Initial milestone source writes | passed (write confirmation only) | GitHub confirmed commits for forest_generator.gd, mobile_controls.gd, world_controller.gd, player_controller.gd, and main.tscn. This is not a runtime pass. |
| 2026-10-18 | [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world) | Godot import/parse/run | blocked / not run | No Godot runtime was executed in this session. |
| 2026-10-18 | [shadows-of-the-lost-world](https://github.com/paz7azaab-lab/shadows-of-the-lost-world) | Android export and device test | blocked / not run | No APK has been built or tested on an Android device. |

## Next checks
- Re-fetch the changed game files and inspect paths, referenced nodes, resource counts, and input-action wiring.
- Run the project with Godot 4 when an engine runtime is available.
- Export and test on Android only after the editor/runtime checks pass.

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
