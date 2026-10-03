# Executable task handoff

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-10-03

## Problem Description

The [refinement and task handoff decision](20261003-1414-refinement-decision-and-task-handoff.md) and [shared vocabulary decision](20261003-1525-shared-vocabulary-and-orchestrator-preflight.md) called for ready, decision-linked work. The first glossary task described an outcome and checks but left its executor to design the skill. The project manager distinguished issues, which hold researchable problems, from tasks, which should be instructions someone can pick up and execute. A less prescriptive task could leave routine implementation discretion, but the boundary between routine and unresolved design would be ambiguous.

## Decision

Register a task only when it is an executable instruction with **what**, **why**, **how**, **acceptance criteria**, **prerequisites**, and **dependencies** specified. Required prerequisites must be available, dependencies complete, and no open design choice left for the executor. Keep work that still needs design with an open issue until it can be reviewed as a task.

## Explanation

What identifies the output; why gives the reason and originating decision; how gives specific steps and permitted scope; acceptance criteria are observable checks; prerequisites name needed inputs, access, and environment; dependencies identify prior work or decisions that must already be complete. "None" is valid where applicable. Creating a task does not assign, schedule, or execute it. A decision may have consequences that cannot yet be registered as tasks.

## Consequences

- Update `decide` and the task format to enforce the six-field gate rather than treating an outcome and checks as sufficient.
- Bring the glossary task into the executable format, including issue and task as its first terms.
- Keep researchable implementation gaps in `open-questions.md`; do not place blocked work under `tasks/`.
