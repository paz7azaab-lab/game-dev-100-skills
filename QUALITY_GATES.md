# Quality Gates

Apply gates relevant to the change. Mark each `passed`, `failed`, `blocked`, or `not applicable` and include evidence. A gate is not passed merely because someone reviewed its title.

## Gate A — Requirements and gameplay
- [ ] The player problem and intended behavior are stated.
- [ ] Acceptance criteria are observable and testable.
- [ ] Normal, boundary, invalid, and failure cases are considered.
- [ ] Rewards, costs, timers, and progression are consistent with game rules.
- [ ] UI feedback explains success, failure, waiting, and unavailable actions.

## Gate B — Art, UI, and readability
- [ ] The implementation follows the approved art direction.
- [ ] Important units, threats, resources, and controls are distinguishable on a small screen.
- [ ] Text, contrast, touch targets, safe areas, and orientation are checked.
- [ ] Animation and effects do not hide essential gameplay information.
- [ ] Protected images/assets are unchanged unless explicit permission was given.
- [ ] Reduced-motion or less-intensive effects are considered where appropriate.

## Gate C — Code and architecture
- [ ] Change is focused and understandable.
- [ ] No obvious broken references, syntax errors, or accidental duplicate logic.
- [ ] State transitions and invalid input are handled.
- [ ] Saves, migrations, and existing data are not silently broken.
- [ ] Errors are actionable; logs contain no secrets or unnecessary personal data.
- [ ] Dependencies and licenses are understood.

## Gate D — Performance and device behavior
- [ ] Baseline and target device/runtime are recorded when available.
- [ ] Startup, loading, frame performance, memory, and asset sizes are considered.
- [ ] Touch input, pause/resume, interruptions, low memory, and network changes are considered for mobile.
- [ ] Rendering/particle/animation cost is reasonable for target hardware.
- [ ] Compatibility claims match actual test coverage.

## Gate E — Security, privacy, and abuse
- [ ] Trust boundaries are identified; valuable state is validated by a trusted server where applicable.
- [ ] Purchases/rewards cannot be granted solely on an untrusted client claim.
- [ ] Authentication, sessions, permissions, and player data are protected.
- [ ] Chat/social features have appropriate reporting, blocking, moderation, and abuse controls.
- [ ] Data collection is minimized and purpose is clear.
- [ ] Relevant exploit, tampering, replay, spam, and rate-limit cases are considered.

## Gate F — Tests and release
- [ ] Relevant automated/manual tests and exact results are recorded.
- [ ] Regression risks and existing flows are checked.
- [ ] Build artifact exists and has the expected type if a build is claimed.
- [ ] Store/platform requirements and third-party licenses are reviewed where relevant.
- [ ] Release notes, versioning, rollback, and known limitations are recorded.
- [ ] Deployment/runtime is independently checked before claiming deployed/working.

## Gate G — Evidence and completion
- [ ] Exact repo, branch, commit, and changed files are listed.
- [ ] Each passed item has a log, output, screenshot, link, or reproducible procedure.
- [ ] Failed and blocked items remain visible.
- [ ] The final report separates Changed / Tested / Built / Deployed / Runtime-verified.
- [ ] No income, quality, compatibility, or security guarantee is inferred from a checklist.
