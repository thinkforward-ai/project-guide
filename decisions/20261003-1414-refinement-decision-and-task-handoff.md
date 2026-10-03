# Refinement, decision, and task handoff

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-10-03

## Problem Description

Project Guide registered questions and recorded decisions but blurred the work between them. `start-new-project` interviewed for a nearly complete description, while `make-decision` also researched and developed proposals. A project begins with an initial question about its purpose; clarifying it may reveal more questions and several proposals. The existing phase-orchestration and input-processing questions remain unresolved. Accepted choices may require implementable work, but work should not start or be scheduled merely because a decision was recorded.

## Decision

Use `start-project` to create the structure and first question, `refine` to develop reviewable proposals and discover further questions, `open-question` to register those questions, and `decide` to accept a choice, record and propagate the decision, and prepare reviewed, unblocked implementation tasks under `tasks/`.

## Explanation

These activities are event-driven and recursive, not a single project-wide sequence. Starting requires only a stated idea and a confirmed first question, not approved requirements. Refinement may produce one or more proposals but does not select one. Choosing requires a registered question, reviewable proposals, explicit acceptance, and no relevant unresolved blocker. A task must link to its decision and state its outcome, scope, dependencies, and completion checks before it is ready. Creating a task does not assign, schedule, or execute it; domain-specific execution skills may be added later. Decisions without actionable work need no task.

## Consequences

- Rename the existing source skills and narrow their triggers and completion gates; add a dedicated `refine` skill.
- Keep `overview.md` aligned with the recursive question lifecycle and keep task artifacts separate from open questions and immutable decisions.
- Leave input-processing responsibility and phase orchestration choices open. Do not treat an implementation-ready task as evidence that all project questions are resolved.
