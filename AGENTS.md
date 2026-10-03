# Agent Instructions

Always use numbered lists.

## Project Rules

1. `overview.md` is the source of truth for the framework's concept and scope. Keep it current when understanding changes.
2. This project is developed with its own method: `work-on-project` aligns an opened project's layout with approval and coordinates the lifecycle; `start-project` bootstraps, `raise-issue` registers issues, `refine` develops proposals, and `decide` accepts solutions and prepares executable tasks. Phase skills also work directly.

## Project Structure

1. `inputs/`: raw input artifacts, kept word for word. Never edited after capture.
2. `overview.md`: current understanding of the framework's concept and scope.
3. `open-issues.md`: unresolved issues only.
4. `decisions/`: immutable decision records.
5. `tasks/`: decision-linked executable instructions with no open design choices, not automatically started or scheduled.
6. `skills/`: the framework's skills, one folder per skill with a `SKILL.md`.
