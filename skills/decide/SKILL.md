---
name: decide
description: List proposals for a registered issue, take the user's choice as the decision, record it, and prepare executable tasks.
source: https://github.com/thinkforward-ai/project-guide
---

# Decide

Choose a solution, record it, and hand off actionable work. Do not develop
proposals or start implementation here.

## Trigger

Use when proposals for a registered issue are ready to be listed for a
choice.

## Entry Gate

The issue and its proposals must be recorded and relevant blockers
explicit. If the issue, proposals, or needed evidence are
missing, return to registration or refinement without inferring a choice.
Do not decide while relevant blockers or contradictions are unresolved.
If the project uses a different register, seek approval for layout alignment
before changing its issues.

## Work

### Choose and Accept

1. List every proposal in full, in the refine Proposal Format, compared
   against the issue's constraints, evidence, risks, and dissent. Always
   follow the list with the gate: **choose a proposal / continue
   refining / pause**. Choosing (or approving a sole proposal) is the
   decision; continuing returns to refinement; pause leaves the issue
   open. A sole proposal still needs an explicit choice.
2. Validate the choice against known facts, accepted decisions, the
   overview, and open issues. Show every conflict with its source and ask
   the user to resolve each one explicitly before recording. If a
   resolution changes the chosen proposal, show the change and get the
   user's confirmation.
3. Mark resolution points settled by the chosen proposal `✅` with a
   `Resolution` and `Details`; ask only about points it leaves open, and
   keep unconfirmed points `❓` and the issue open. In team or
   organization mode, confirm the accepting individual's
   full name and role; never infer. In solo mode, record no attribution.

### Record and Apply

1. At acceptance, use the current UTC time for
   `decisions/<yyyymmdd-hhmm>-<unique-title>.md`. Create one immutable
   record per decision with the following structure (omit the
   `Accepted by` line in solo mode):

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

   After recording, show the record's path and a short summary.

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
