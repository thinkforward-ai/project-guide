---
name: decide
description: Choose among reviewed proposals for a registered issue, record an accepted decision, and prepare executable tasks.
source: https://github.com/thinkforward-ai/project-guide
---

# Decide

Choose a solution, record it, and hand off actionable work. Do not develop
proposals or start implementation here.

## Trigger

Use when someone asks to choose among reviewable proposals for a registered
issue.

## Entry Gate

The issue and user-reviewed proposals must be recorded and relevant
blockers explicit. If the issue, proposals, or needed evidence are
missing, return to registration or refinement without inferring a choice.
Do not decide while relevant blockers or contradictions are unresolved.
If the project uses a different register, seek approval for layout alignment
before changing its issues.

## Work

### Choose and Accept

1. Show every reviewed proposal in full, in the refine Proposal Format,
   and compare them against the issue's constraints, evidence, risks,
   and dissent. A sole proposal still needs explicit acceptance.
   If none is acceptable, return to refinement.
2. State the exact choice and its consequences. Confirm all resolution
   points with the user; mark each `✅` with a `Resolution` and `Details`
   only after confirmation. Keep unconfirmed points `❓` and the issue
   open. Confirm the accepting individual's full name and role; never infer.
3. Show the final decision wording and confirm that the entire issue is
   ready to resolve. At this decision gate, always offer **Approve / Revise /
   Pause**: Approve accepts the whole decision, Revise returns to refinement,
   and Pause leaves the issue open without a new decision. Approval of one
   point is not approval of the whole issue. Do not create a record
   without explicit approval.

### Record and Apply

1. At acceptance, use the current UTC time for
   `decisions/<yyyymmdd-hhmm>-<unique-title>.md`. Create one immutable
   record per decision with the following structure:

   ```md
   # <Decision title>

   **Accepted by:** <Full name> (<relevant role>)
   **Date:** YYYY-MM-DD

   ## Problem Description
   <Issue, facts, constraints, proposals, and material disagreement>

   ## Decision
   <Accepted choice>

   ## Explanation
   <Meaning, boundaries, and reasons>

   ## Consequences
   - <Required changes or effects>
   ```

2. Remove the resolved issue from `open-issues.md`; never reuse its ID.
   Leave earlier decisions untouched. If new evidence challenges one, propose
   a new issue instead of editing the accepted record.
3. Update affected project understanding, including `overview.md`, and any
   stale plans or instructions. Link to the decision rather than copying it.
4. Share the decision and the updated project understanding through the
   project's shared store so the whole team can see them, e.g. commit
   and push for Git, or update the relevant pages for a wiki. If the
   store or the sharing method is unknown, ask. Sharing outside the
   local workspace requires the user's approval.

### Prepare Tasks and Follow-ups

1. After acceptance, draft the actionable consequences as tasks and review
   them with the user. Create a file under `tasks/` only for a confirmed
   instruction with **what**, **why**, **how**, **acceptance criteria**,
   **prerequisites**, and **dependencies**. Use the project's task format
   if present; otherwise use `tasks/<unique-title>.md` with a title, a link
   to the accepted decision, and one section for each of those six fields.
   Specify exact actions, outputs, scope, and observable checks. Verify
   prerequisites are available and dependencies complete; use "None" where
   applicable. Do not make the executor resolve an open design choice.
   A decision may yield zero or several tasks; never create one merely to
   fill the folder.
2. If work is blocked or a new issue appears, explain it and propose
   registering that issue. Keep work still needing design with an open
   issue, not under `tasks/`. Review follow-up issues with the user
   before registering them.
3. Creating a task does not assign, schedule, or start it. Execution and
   roadmap scheduling happen only when someone asks for them.

## Exit Gate

Complete when the decision is recorded and shared, the issue removed,
affected understanding updated, and tasks or their absence reviewed with
the user.
Report any unresolved blockers or declined tasks; do not claim they are ready.

## Transition

Offer to refine another open issue or, only on explicit request, hand an
executable task to a future execution capability or a human. Do not start
work merely because a task was created.
