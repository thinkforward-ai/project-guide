# Agent Instructions

Always use numbered lists.

## Project Rules

1. `overview.md` is the source of truth for the framework's concept and scope. Keep it current when understanding changes.
2. This project is developed with its own method: register unresolved choices in `open-questions.md` with the `open-question` skill, and resolve them with the `make-decision` skill.

## Project Structure

1. `inputs/`: raw input artifacts, kept word for word. Never edited after capture.
2. `overview.md`: current understanding of the framework's concept and scope.
3. `open-questions.md`: unresolved questions only.
4. `decisions/`: immutable decision records.
5. `skills/`: the framework's skills, one folder per skill with a `SKILL.md`.
