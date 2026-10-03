---
name: start-project
description: Bootstrap a project from a new goal or idea when no project structure exists. Create the structure and first issue; leave clarification to refinement.
source: https://github.com/thinkforward-ai/project-guide
---

# Start Project

Create a place to refine the user's idea, not a completed project description.

## Trigger

Someone brings a new goal or idea and no project structure exists. If a project
already exists, do not replace its files; inspect its layout and seek approval
for alignment before continuing with its issues.

## Entry Gate

Capture the user's idea as stated, or ask for it if missing. Show the proposed
first issue about the project's meaning and goal; confirm it before creating
the structure. Do not treat a provisional goal as a settled requirement.

## Work

1. Create `README.md`, `AGENTS.md`, `overview.md`, `open-issues.md`, and
   directories for `inputs/`, `decisions/`, and `tasks/` without overwriting
   existing material. Preserve provided input files unchanged.
2. Put the user's original idea in the first issue's context. Initialize
   `overview.md` with the goal, context, scope, constraints, and contributing
   roles marked unresolved, referring to the first issue rather than
   presenting guesses as settled facts.
3. Register the confirmed first issue in `open-issues.md` using the
   project's issue format. Keep `AGENTS.md` about the project structure and
   `README.md` as its entry point.

## Exit Gate

The structure exists, the first issue is registered, and the user's
next-step choice is known. No interview, proposal, decision, or task
is required.

## Transition

After registering the first issue, ask whether to refine it now or leave
it open for later. If the user already explicitly asked to start and refine
now, use that choice without asking again. If now, hand off to refinement;
if later, leave the issue open and stop. A new input alone does not
silently start refinement.
