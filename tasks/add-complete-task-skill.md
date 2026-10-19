# Add the complete-task skill and tasks/closed/

**Decision:** [Complete-task skill and tasks/closed/](../decisions/20261019-2137-complete-task-skill.md)

## What

1. A new `skills/complete-task/SKILL.md`.
2. `start-project`, `work-on-project`, `tasks/README.md`, `AGENTS.md`, and `README.md` updated for `tasks/closed/` and the **complete a task** choice.

## Why

1. Implement the linked decision: one core skill closes finished tasks with verified evidence, and `tasks/` holds only ready work.

## How

1. Create `skills/complete-task/SKILL.md` with exactly this content:

   ````md
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
   ````

2. In `skills/start-project/SKILL.md`, replace:

   ```md
      `open-issues.md`, and directories for `inputs/`, `decisions/`, and `tasks/` without overwriting
   ```

   with:

   ```md
      `open-issues.md`, and directories for `inputs/`, `decisions/`, `tasks/`, and `tasks/closed/` without overwriting
   ```

3. In `skills/work-on-project/SKILL.md`:
   1. Replace:

      ```md
         `overview.md`, `roadmap.md`, `open-issues.md`, `inputs/`, `decisions/`,
         and `tasks/`).
      ```

      with:

      ```md
         `overview.md`, `roadmap.md`, `open-issues.md`, `inputs/`, `decisions/`,
         `tasks/`, and `tasks/closed/`).
      ```

   2. Replace:

      ```md
         overview, issue register, decisions, and tasks where available. After
      ```

      with:

      ```md
         overview, issue register, decisions, and tasks where available,
         treating `tasks/closed/` as completed work with nothing to do. After
      ```

   3. Replace:

      ```md
         issue with ready proposals**, **work on a ready task**,
      ```

      with:

      ```md
         issue with ready proposals**, **work on a ready task**, **complete a
         task** when one looks finished (through `complete-task`; never move
         tasks here),
      ```

4. In `tasks/README.md`, replace:

   ```md
   `tasks/`. Readiness does not mean assigned, scheduled, or started. For edits to existing text, quote the current text and its replacement.
   ```

   with:

   ```md
   `tasks/`. Readiness does not mean assigned, scheduled, or started. For edits to existing text, quote the current text and its replacement.

   When a task's work is finished, close it with `complete-task`: it checks the
   acceptance criteria against evidence and, on confirmation, moves the task
   unchanged to `tasks/closed/` with an appended Completion section. `tasks/closed/`
   holds completed work with nothing to do.
   ```

5. In `AGENTS.md`:
   1. Replace:

      ```md
      `refine` develops proposals, and `decide` accepts solutions and prepares executable tasks.
      ```

      with:

      ```md
      `refine` develops proposals, `decide` accepts solutions and prepares executable tasks, and `complete-task` closes finished tasks.
      ```

   2. Replace:

      ```md
      6. `tasks/`: decision-linked executable instructions with no open design choices, not automatically started or scheduled.
      ```

      with:

      ```md
      6. `tasks/`: decision-linked executable instructions with no open design choices, not automatically started or scheduled. `tasks/closed/` holds closed tasks with their Completion section.
      ```

6. In `README.md`:
   1. Replace:

      ```md
      `start-project`, `raise-issue`, `refine`, and `decide`, each usable directly.
      ```

      with:

      ```md
      `start-project`, `raise-issue`, `refine`, `decide`, and `complete-task`, each usable directly.
      ```

   2. Replace:

      ```md
      live in `tasks/`. Task execution is outside the core skills for now.
      ```

      with:

      ```md
      live in `tasks/`; closed tasks move to `tasks/closed/`. Task execution is
      outside the core skills for now.
      ```

7. Create `tasks/closed/.gitkeep` so the empty folder is tracked.
8. Do not install the skill, close any task, or change other text.

## Acceptance Criteria

1. `skills/complete-task/SKILL.md` matches step 1 exactly.
2. Each replacement in steps 2 to 6 is applied once, and no other text changed.
3. `tasks/closed/` exists and is tracked.
4. `git diff --check` passes.

## Prerequisites

1. Each quoted current text exists exactly once in its file.

## Dependencies

1. None.
