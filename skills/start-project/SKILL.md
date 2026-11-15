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

For visible role involvement, follow the **Role visibility** convention
in the Project Guide glossary skill when available. Its absence does
not block this phase.

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
   record it. In team or organization mode, propose the roles to add to a
   Roles subsection of the Collaboration section: the stakeholder plus the
   roles from the starter role catalogue (`roles-catalogue.md` in the
   Project Guide glossary skill) that the idea evidently needs, adapted to
   the project. For needed expertise
   the catalogue lacks, as in a domain new to the framework, define the
   role from scratch with the same fields. The roster may define new
   roles or redefine catalogue roles. Initialize `roadmap.md` in the Roadmap Format with no milestones yet, referring
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

**Demo:** <run or directly show the outcome; otherwise present HTML slides>

**Progress:**

- YYYY-MM-DD: <progress; demo date and evidence/artifact reference, and explicit confirmation when received>
```

Milestones appear in intended order. Achieved or cancelled milestones
stay listed and say so under their heading.
In every mode, meeting criteria makes a milestone ready for a demo, not
achieved. Achievement requires an evidence-backed demo and then explicit
confirmation from the project's designated human stakeholder acceptance
authority. In solo mode the user confirms without introducing roles; with
several stakeholders, follow accepted authority arrangements and never
infer consent or a quorum. Run or directly show the outcome where possible;
otherwise prepare and present HTML slides with the acceptance evidence.
Record the demo date, evidence or artifact reference, and explicit
confirmation in Progress. Slides, checked criteria, silence, and AI judgement
do not replace confirmation; without it, keep the milestone unachieved and
do not advance the current milestone on that basis.

## Exit Gate

The structure exists, the first issue and roadmap issue are registered,
and the next-step choice is known. No interview, proposal, decision, or
task is required.

## Transition

After the first issue is registered comes the choice to refine it now or
leave it open for later. If now, hand off to refinement; if later, leave the
issue open and stop. A new input alone does not silently start refinement.

## User-driven mode

1. Show the two proposed issues and the proposed roles, and create the
   structure only after the user confirms them.
2. Ask whether to refine now or later. If the user already explicitly
   asked to start and refine now, use that choice without asking again.

## AI-driven mode

Applies only when the user stated AI-driven mode at the start.

1. Create the structure, register both issues, and add the proposed
   roles without a confirmation gate, then report them. The stakeholder
   may change the roster at any time.
2. Decide yourself whether to refine the first issue now and state why.
3. The project's goal is a reserved decision: ask the stakeholder for the
   goal, requirements, and preferences in one batch, with your
   recommendation when available.
