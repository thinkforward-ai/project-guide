---
name: work-on-project
description: Align a project's layout with approval and guide its issue-to-task lifecycle. Use when starting, opening, joining, or resuming project work, asking for status or next steps, or continuing across phases.
source: https://github.com/thinkforward-ai/project-guide
---

# Work on Project

Coordinate the lifecycle; leave each phase's work to its own skill. The loop
is: start a project and first issue → raise issues → refine selected
issues → list proposals and take the choice as the decision →
update understanding and review executable tasks → return to new or
remaining issues as needed.

Be concise: lead with what matters, ask only what is needed now, and
never repeat content the user has just seen. Proposals are exempt: they
must carry all information needed to make a decision.

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
   `overview.md`, `roadmap.md`, `open-issues.md`, `inputs/`, `decisions/`,
   `tasks/`, and `tasks/closed/`).
   Do not assume its layout is an older Project Guide version. If alignment
   is needed, propose a project-specific source-to-target translation,
   including planned file changes, content mapping, conflicts, and anything
   that cannot be mapped safely. For a project with `open-questions.md`,
   propose mapping its unresolved issues to `open-issues.md` while preserving
   `Q<n>` IDs, `Next question ID`, `### Question`, and all record content.
   If both registers exist, do not merge them by guesswork. The specific
   changes need approval before they are applied, as the mode sections
   describe.
   Preserve raw inputs and accepted decisions unchanged; never overwrite,
   discard, or invent project content. Ask about ambiguous mappings instead
   of guessing. If approval is withheld, leave the project unchanged and
   offer status based on its existing artifacts or actions that do not
   require alignment; do not route to phase skills that require the target
   layout.
2. After alignment or when the layout already matches, read the project's
   overview, including its roster of roles, issue register, decisions,
   and tasks where available,
   treating `tasks/closed/` as completed work with nothing to do. After
   an approved alignment, re-read affected records.
   Use the records and explicit user confirmations to see which issues are
   open and which proposals were reviewed; do not invent a stage field,
   a completion percentage, or an approval. Keep the roadmap current: for
   each decision or completed task since the last progress entry, add a
   one-line entry to any milestone it moves or relates to and mark the
   criteria it satisfies `✅`. When all criteria of a milestone are met,
   it is achieved as the mode sections describe, and then the next one
   becomes current. Changing milestones
   needs a decision, not this step.
3. If status was requested, show it directly. Otherwise, when no action
   is named, the next action comes from the applicable choices:
   **show current status** first, **refine an open issue**, **decide an
   issue with ready proposals**, **work on a ready task**, **complete a
   task** when one looks finished (through `complete-task`; never move
   tasks here),
   **provide input or an idea**, or **pause**. Show full status only when
   requested or chosen: roadmap **Current focus** (the current milestone
   in full) and **Next** (name and one-line intent, never later
   milestones; say so if no roadmap exists), current understanding,
   the current role roster (roles and holders; flag provisional or
   unresolved entries, or state that solo mode uses no roles),
   issues and blockers,
   proposals ready for a choice, accepted decisions, and executable tasks.
4. Follow the chosen action's trigger: a new goal without structure needs
   bootstrap; a new issue needs registration; an explicitly selected
   issue needs refinement; proposals ready for a choice enter the
   decision phase. New input about an issue does not itself authorize
   refinement. Registration offers refine now or leave open; listing
   proposals is always followed by **choose a proposal / continue
   refining / pause**, and a choice is the decision. Preserve each
   phase's own entry gate.
5. Invoke an available phase skill only when the chosen action and its
   entry gate permit it. If it cannot be invoked, explain the handoff
   instead of claiming it ran. After a phase runs, check its exit gate,
   re-read affected records, and move to the next permitted action.
   Continue only while each transition is authorized, as the mode
   sections describe.
6. Hand a ready task to execution only when authorized, as the mode
   sections describe, and only through an available execution capability
   or a clear human handoff.
   Do not execute, schedule, assign, or create tasks here. Scheduling is
   offered only if a PM scheduling capability exists.

## Skill Update Check

1. Only when status is requested or chosen, check installed skills the
   project evidently uses, including non-Project Guide ones; skip
   unrelated installs. Briefly state scope and incomplete coverage; add
   no configuration format.
2. Compare with verified original sources through an available
   skill-management capability, allowing for known install
   transformations. Never call a local modification or uncertain
   difference an update. Skills without a source, access, or checking
   capability stay unchecked and never block status.
3. List only the names of skills with updates; summarize the rest
   briefly. Limit any "no updates" claim to checked skills. Show
   differences only on request or during update review.
4. Stay read-only; reviewing and applying updates needs a separate,
   explicitly approved flow.

## Exit Gate

Work pauses, or a phase-skill handoff has been verified against its exit
gate. Do not claim that an uninvoked skill ran or that an unapproved
decision was accepted.

## Transition

After a verified handoff, the applicable next actions follow. If none is
chosen, stop without changing another phase's state.

## User-driven mode

1. When no action is named, offer the applicable choices. If several
   issues or tasks could be the focus, ask the user to choose. After
   showing status or finishing a non-phase action, offer the choices
   again until the user pauses or a phase handoff begins.
2. The user approves alignment changes and authorizes each transition.
3. A milestone is achieved when all its criteria are met.
4. Hand a ready task to execution only on the user's explicit request.

## AI-driven mode

1. Read the driving mode from the overview. Choose the next action
   yourself, state it and why in one line, and proceed. Show the menu
   only when the stakeholder asks or a reserved decision is reached.
2. Approve alignment yourself when it preserves all project content.
   Changes that discard or rewrite content are reserved.
3. Pass transitions yourself within the delegation, and hand ready tasks
   to execution.
4. When all criteria of a milestone are met, the milestone is ready for a
   demo, not reached. Give the stakeholder a demo; it is reached when they
   confirm it.
5. Stop and report when the current milestone is ready for a demo, when
   only reserved decisions remain, or when no applicable action is left.
