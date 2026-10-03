---
name: work-on-project
description: Align a project's layout with approval and guide its issue-to-task lifecycle. Use when starting, opening, joining, or resuming project work, asking for status or next steps, or continuing across phases.
source: https://github.com/thinkforward-ai/project-guide
---

# Work on Project

Coordinate the lifecycle; leave each phase's work to its own skill. The loop
is: start a project and first issue → raise issues → refine selected
issues and review proposals → explicitly decide → update understanding and
review executable tasks → return to new or remaining issues as needed.

## Trigger

Someone brings a new goal, opens, joins or resumes a project, asks for status or
next steps, or wants to continue across phases. Direct phase skill calls
remain valid and need not pass through this skill.

## Entry Gate

Locate the intended project from the current context or ask which one the
user means; do not assume among multiple projects. When opening or resuming
an existing project, inspect its artifacts before routing lifecycle work.
If no project exists and a new goal was supplied, bootstrap it. When an
optional Project Guide glossary skill is installed, read its main terms and
check them internally before starting or resuming. Its absence does not
block progress or require a user-facing recitation.

## Work

1. On opening or resuming any existing project, compare its actual artifacts
   with the current Project Guide layout (`README.md`, `AGENTS.md`,
   `overview.md`, `open-issues.md`, `inputs/`, `decisions/`, and `tasks/`).
   Do not assume its layout is an older Project Guide version. If alignment
   is needed, propose a project-specific source-to-target translation,
   including planned file changes, content mapping, conflicts, and anything
   that cannot be mapped safely. For a project with `open-questions.md`,
   propose mapping its unresolved issues to `open-issues.md` while preserving
   `Q<n>` IDs, `Next question ID`, `### Question`, and all record content.
   If both registers exist, do not merge them by guesswork. Obtain explicit
   approval for the specific changes before applying them.
   Preserve raw inputs and accepted decisions unchanged; never overwrite,
   discard, or invent project content. Ask about ambiguous mappings instead
   of guessing. If approval is withheld, leave the project unchanged and
   offer status based on its existing artifacts or actions that do not
   require alignment; do not route to phase skills that require the target
   layout.
2. After alignment or when the layout already matches, read the project's
   overview, issue register, decisions, and tasks where available. After
   an approved alignment, re-read affected records.
   Use the records and explicit user confirmations to see which issues are
   open and which proposals were reviewed; do not invent a stage field,
   a completion percentage, or an approval.
3. If the user requested status, show it directly. Otherwise, if the user
   has not named an action, offer only applicable choices:
   **show current status** first, **refine an open issue**, **review
   proposals**, **decide a reviewed issue**, **work on a ready task**,
   **provide input or an idea**, or **pause**. Show full status only when
   requested or chosen: current understanding, issues and blockers,
   reviewed proposals, accepted decisions, and executable tasks. If several
   issues or tasks could be the focus, ask the user to choose.
4. Follow the chosen action's trigger: a new goal without structure needs
   bootstrap; a new issue needs registration; an explicitly selected
   issue needs refinement; reviewed proposals can be compared without
   acceptance; a requested choice enters the decision gate. New input
   about an issue does not itself authorize refinement. Registration
   offers refine now or leave open; proposal review offers **Review
   proposals / Continue refinement / Pause**; decision offers **Approve /
   Revise / Pause**. Preserve each phase's own entry gate.
5. Invoke an available phase skill only when the user's intent and its
   entry gate permit it. If it cannot be invoked, explain the handoff
   instead of claiming it ran. After a phase runs, check its exit gate,
   re-read affected records, and offer the next permitted action. Continue
   only while the user's choices authorize each transition.
6. Hand a ready task to execution only on explicit request and only
   through an available execution capability or a clear human handoff.
   Do not execute, schedule, assign, or create tasks here. Scheduling is
   offered only if a PM scheduling capability exists.

## Exit Gate

The user has received the requested status, chosen to pause, or a
phase-skill handoff has been verified against its exit gate. Do not claim
that an uninvoked skill ran or that an unapproved decision was accepted.

## Transition

After a verified handoff, offer the applicable next actions. If the user
does not choose one, stop without changing another phase's state.
