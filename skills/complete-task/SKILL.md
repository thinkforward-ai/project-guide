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

## Trigger

Someone reports a task done, or chooses **complete a task** in
`work-on-project`.

## Entry Gate

The task must exist under `tasks/`, not `tasks/closed/`. If several tasks
could be meant, ask which one. If the project lacks `tasks/closed/`, seek
approval for layout alignment first.

## Work

1. Read the task and its linked decision. For each acceptance
   criterion, find evidence such as commits, files, or test results,
   and run read-only checks where the criterion names one. Do not
   change the work to make a criterion pass.
2. Show each criterion as met with its evidence, unmet, or
   unverifiable with the reason. The user may supply evidence for an
   unverifiable criterion.
3. If any criterion remains unmet or unverifiable, do not close the
   task. Offer to leave it open or to register a follow-up issue for
   the gap.
4. When every criterion is met, ask the user to confirm completion.
   Only on confirmation:
   1. Append this section to the task, leaving the rest unchanged
      (omit `Confirmed by` in solo mode):

      ```md
      ## Completion

      **Date:** YYYY-MM-DD
      **Confirmed by:** <Full name> (<role>)

      1. <Criterion>: <evidence>
      ```

   2. Move the file to `tasks/closed/` under the same name and update
      links to its old path.
   3. Add the roadmap progress entry and mark satisfied milestone
      criteria `✅`, as `work-on-project` describes.
5. Share the change through the project's shared store. Sharing outside
   the local workspace requires the user's approval.

## AI-driven mode

Gather evidence and state your assessment. Only the stakeholder
confirms completion; the gate stays.

## Exit Gate

The task is in `tasks/closed/` with a Completion section and roadmap
progress recorded, or it remains in `tasks/` with the reason stated.
Never claim completion without the user's confirmation.

## Transition

Offer to complete another finished task, register a follow-up issue
through `raise-issue`, or return to `work-on-project`.
