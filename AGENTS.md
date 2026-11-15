# Agent Instructions

Always use numbered lists.

## Project Rules

1. `overview.md` is the source of truth for the framework's concept and scope. Keep it current when understanding changes.
2. This project is developed with its own method: `work-on-project` aligns an opened project's layout with approval and coordinates the lifecycle; `start-project` bootstraps, `raise-issue` registers issues, `refine` develops proposals, `decide` accepts solutions and prepares executable tasks, and `complete-task` closes finished tasks. Phase skills also work directly.

## Project Structure

1. `inputs/`: raw input artifacts, kept word for word. Never edited after capture.
2. `overview.md`: current understanding of the framework's concept and scope.
3. `roadmap.md`: milestones toward the goal and their progress.
4. `open-issues.md`: unresolved issues only.
5. `decisions/`: immutable decision records.
6. `tasks/`: decision-linked executable instructions with no open design choices, not automatically started or scheduled. `tasks/closed/` holds closed tasks with their Completion section.
7. `skills/`: the framework's skills, one folder per skill with a `SKILL.md`.

## Framework Guardian

Every change to skills, the glossary, the overview, the layout, or decisions needs the framework guardian's verdict (roster in `overview.md` section 10). Check it against accepted decisions and the framework's original goal and purpose. An objection blocks the change until it is resolved or the founder overrides it.
