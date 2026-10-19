# Global 100-Skill Rule — Every Game Project

**Owner requirement:** Apply this rule to every game project the user asks us to create, continue, port, or maintain, regardless of genre, engine, repository, platform, or project name.

## Mandatory workflow

1. **Before each meaningful phase or feature**, identify the exact target repository, branch, current commit, protected assets, and acceptance criteria. Inspect the project's real files before planning changes.
2. **Review all 100 areas** in `GAME_SKILLS_INDEX.md` at each meaningful milestone. Maintain a milestone matrix that accounts for every ID from 1–100 and records a truthful status plus a short reason/evidence. Reviewing an area is not the same as executing it.
3. **Apply relevant skills to actual work.** For each applicable area, record what action/check was performed and the evidence produced. Include security/privacy, mobile lifecycle, performance, QA, and commercial readiness whenever relevant.
4. **Mark non-applicable areas explicitly** with a project-specific reason. Do not silently omit IDs. If an area cannot be applied or verified because of missing access, hardware, tooling, or dependencies, mark it blocked and say why.
5. **Never fabricate success.** Do not mark a skill passed merely because its title was reviewed, a plan was written, or a build succeeded. A test must have an observable result; a deployment must be independently confirmed; runtime verification must occur in the actual runtime/device.
6. **Respect project-specific constraints.** Never switch repository, engine, platform, or protected assets without permission. The framework does not require a particular engine; use the user's approved stack for that project.
7. **Close each meaningful milestone** by updating its project record, test report, and evidence log with the exact commit, changed files, relevant skill statuses, test results, blockers, and next steps.
8. **Use the 100 skills for all games**, not just the currently active title. For a new project, create a new project record and its own milestone matrix; do not copy another game's evidence as if it belonged to the new project.

## Required milestone matrix fields

- Skill ID and exact title from `GAME_SKILLS_INDEX.md`
- Status: `planned`, `in progress`, `passed`, `failed`, `blocked`, or `not applicable`
- Project-specific reason for applicability/non-applicability
- Actual action or verification performed
- Evidence link, test output, commit, or reason evidence is unavailable
- Follow-up action for failed, blocked, or still-planned items

## Honest delivery labels

Report separately: **Changed**, **Tested**, **Built**, **Deployed**, and **Runtime-verified**. Never imply that all 100 skills were executed for every individual code change. The standing requirement is to review all 100 at every meaningful milestone, apply the relevant ones, and account for every ID honestly.

This document is a workflow policy, not a claim that 100 plugins, tools, or specialist agents are installed.
