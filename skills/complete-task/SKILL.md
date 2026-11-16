---
name: complete-task
description: Close a finished task by checking its acceptance criteria against evidence and, on confirmation, moving it to tasks/closed/. Use when a task is reported done or chosen for completion.
source: https://github.com/thinkforward-ai/project-guide
---

# Complete Task

Record that a task's work is finished. Do not execute, fix, or redesign
the task here.

Be concise: lead with what matters, ask only what is needed now, and
never repeat content the user has just seen.

For visible role involvement, use an available project-terminology
capability to find the **Role visibility** convention through its own
instructions. Its absence does not block this phase.

## Trigger

Someone reports a task done, or chooses **complete a task** while
coordinating project work.

## Entry Gate

The task must exist under `tasks/`, not `tasks/closed/`. If several tasks
could be meant, ask which one. If the project lacks `tasks/closed/`, layout
alignment comes first.

## Work

1. Read the task and its linked decision. For each acceptance
   criterion, find evidence such as commits, files, or test results,
   and run read-only checks where the criterion names one. Do not
   change the work to make a criterion pass. In a project with a roster,
   holders of the expertise a criterion requires check it, for example
   the developer for a test result or the user advocate for
   presentation.
2. Show each criterion as met with its evidence, unmet, or
   unverifiable with the reason. Missing evidence for an unverifiable
   criterion may be supplied.
3. If any criterion remains unmet or unverifiable, do not close the
   task. Leave it open or register a follow-up issue for the gap, as the
   mode sections describe.
4. When every criterion is met, completion needs confirmation, as the
   mode sections describe. Only on confirmation:
   1. Append this section to the task, leaving the rest unchanged. Use
      `**Confirmed by:** AI (<role>, delegated)` when the agent confirms
      under AI-driven delegation; otherwise omit `Confirmed by` in solo mode:

      ```md
      ## Completion

      **Date:** YYYY-MM-DD
      **Confirmed by:** <Full name> (<role>)

      1. <Criterion>: <evidence>
      ```

   2. Move the file to `tasks/closed/` under the same name and update
      links to its old path.
   3. Add the roadmap progress entry and mark satisfied milestone
      criteria `✅`, following the milestone-progress rules from an
      available project-work coordination capability.
5. Share the change through the project's shared store. Sharing outside
   the local workspace requires the user's approval.

## Exit Gate

The task is in `tasks/closed/` with a Completion section and roadmap
progress recorded, or it remains in `tasks/` with the reason stated.
Never claim completion without confirmation.

## Transition

Next: complete another finished task, use an available issue-registration
capability for a follow-up, or return to an available project-work
coordination capability.

## User-driven mode

1. Show the assessment of each criterion. The user may supply evidence
   for unverifiable criteria and chooses whether a gap leaves the task
   open or becomes a follow-up issue.
2. Only the user confirms completion.

## AI-driven mode

1. Gather evidence and assess each criterion. When every criterion is
   met with evidence, confirm completion yourself and record `Confirmed
   by: AI (<role>, delegated)`.
2. Register follow-up issues for gaps yourself. Ask the stakeholder only
   for evidence that only they can supply.
3. If completing the task fulfils a milestone's criteria, the milestone
   becomes ready for a demo; confirming it is reserved for the stakeholder.
