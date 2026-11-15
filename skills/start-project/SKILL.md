---
name: start-project
description: Bootstrap a project from a new goal or idea when no project structure exists. Create the structure and first issue; leave clarification to refinement.
source: https://github.com/thinkforward-ai/project-guide
---

# Start Project

Create a place to refine the user's idea, not a completed project description.

Be concise: lead with what matters, ask only what is needed now, and
never repeat content the user has just seen. Proposals are exempt: they
must carry all information needed to make a decision.

## Trigger

Someone brings a new goal or idea and no project structure exists. If a project
already exists, do not replace its files; inspect its layout and seek approval
for alignment before continuing with its issues.

## Entry Gate

Capture the user's idea as stated, or ask for it if missing. Prepare the
first issue about the project's meaning, goal, collaboration mode (solo,
team, or organization), and driving mode (AI-driven or user-driven), and a
roadmap issue about the project's milestones; both need confirmation before
the structure is created. Do not treat a provisional goal as a settled
requirement. Until the user states a driving mode, follow user-driven mode.

## Work

1. Create `README.md`, `AGENTS.md`, `overview.md`, `roadmap.md`,
   `open-issues.md`, and directories for `inputs/`, `decisions/`, `tasks/`, and `tasks/closed/` without overwriting
   existing material. Preserve provided input files unchanged. `inputs/`
   holds only material imported from outside the session; never save
   session prompts or answers as input files.
2. Put the user's original idea in the first issue's context. Initialize
   `overview.md` with the goal, context, scope, constraints, and a
   Collaboration section (mode, `**Driving:**`, and contributors) marked
   unresolved, referring to the first issue rather than presenting guesses
   as settled facts. If the user already stated the mode or driving mode,
   record it. Initialize `roadmap.md` in the Roadmap Format with no milestones yet, referring
   to the roadmap issue.
3. Register the confirmed first issue and roadmap issue in
   `open-issues.md` using the project's issue format. Keep `AGENTS.md` about the project structure and
   `README.md` as its entry point.

## Roadmap Format

```md
# Roadmap

The journey toward the goal in [overview.md](overview.md).

## M<n>: <Milestone name>

**Intent:** <why it matters>

**Done when:**

- ❓ <observable criterion>

**Progress:**

- YYYY-MM-DD: <what was done>
```

Milestones appear in intended order. Achieved or cancelled milestones
stay listed and say so under their heading.

## Exit Gate

The structure exists, the first issue and roadmap issue are registered,
and the next-step choice is known. No interview, proposal, decision, or
task is required.

## Transition

After the first issue is registered comes the choice to refine it now or
leave it open for later. If now, hand off to refinement; if later, leave the
issue open and stop. A new input alone does not silently start refinement.

## User-driven mode

1. Show the two proposed issues and create the structure only after the
   user confirms them.
2. Ask whether to refine now or later. If the user already explicitly
   asked to start and refine now, use that choice without asking again.

## AI-driven mode

Applies only when the user stated AI-driven mode at the start.

1. Create the structure and register both issues without a confirmation
   gate, then report them.
2. Decide yourself whether to refine the first issue now and state why.
3. The project's goal is a reserved decision: ask the stakeholder for the
   goal, requirements, and preferences in one batch, with your
   recommendation when available.
