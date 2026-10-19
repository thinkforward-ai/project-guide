# Complete-task skill and tasks/closed/

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-10-19

## Problem Description

Q14 asked what happens to a task in `tasks/` once its work is done. Finished tasks stayed next to ready ones (five by 2026-10-19 across this project and `integrations`), nothing defined who confirms completion or with what evidence, and no skill owned closure. The founder preferred moving finished tasks to `tasks/closed/` as a structural change rather than a status field, with skills aware of it. The [lifecycle orchestration decision](20261003-1603-project-lifecycle-orchestration.md) keeps phase work and execution out of `work-on-project`, and `overview.md` defers execution skills.

Three proposals shared the `tasks/closed/` structure and differed on ownership: a new core `complete-task` skill; extending `work-on-project`, which would require reopening the lifecycle orchestration decision; or a convention requiring executors to move tasks themselves, with no verification step.

## Decision

Add a core `complete-task` phase skill that closes finished tasks. A finished task moves unchanged to `tasks/closed/` with an appended `## Completion` section recording the date, who confirmed, and the evidence.

## Explanation

1. **Structure:** `tasks/` holds ready work only; `tasks/closed/` holds completed work with nothing to do. `start-project` creates `tasks/closed/`, and `work-on-project` includes it in the layout.
2. **complete-task:** Uses the standard Trigger, Entry Gate, Work, Exit Gate, and Transition contract. It is triggered when someone reports a task done or chooses **complete a task**. It checks each acceptance criterion against evidence such as commits, files, or test results and shows the result. Only on the user's confirmation does it append the Completion section, move the file, and add the roadmap progress entry. It offers to register follow-up issues for gaps and never closes a task with unmet criteria.
3. **work-on-project:** Treats `tasks/closed/` as completed work and uses it for roadmap progress. It offers **complete a task** when a task looks finished, but never moves tasks itself.
4. **Boundary:** Recording completion is core document upkeep, not execution. Executing tasks stays outside the core.
5. **Reasons:** One clear owner, consistent with the orchestrator's limits; works for any executor; explicit verification guards against false completion; roadmap progress is recorded at closure.

## Consequences

- Add `skills/complete-task/SKILL.md`.
- Update `start-project`, `work-on-project`, and `tasks/README.md` for `tasks/closed/` and the **complete a task** choice.
- Update `overview.md`, `AGENTS.md`, and `README.md` to describe task closure as core while execution stays out of scope.
- Close the five finished tasks through `complete-task` once it exists.
