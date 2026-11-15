---
name: decide
description: List proposals for a registered issue, take the choice as the decision, record it, and prepare executable tasks.
source: https://github.com/thinkforward-ai/project-guide
---

# Decide

Choose a solution, record it, and hand off actionable work. Do not develop
proposals or start implementation here.

Be concise: lead with what matters, ask only what is needed now, and
never repeat content the user has just seen. Proposals are exempt: they
must carry all information needed to make a decision.

For visible role involvement, follow the **Role visibility** convention
in the Project Guide glossary skill when available. Its absence does
not block this phase.

## Trigger

Proposals for a registered issue are ready to be listed for a choice.

## Entry Gate

The issue and its proposals must be recorded and relevant blockers
explicit. If the issue, proposals, or needed evidence are missing, return
to registration or refinement without inferring a choice. Do not decide
while relevant blockers or contradictions are unresolved. If the project
uses a different register, layout alignment comes first.

## Work

### Choose and Accept

1. Compare every proposal, in full and in the refine Proposal Format,
   against the issue's constraints, evidence, risks, and dissent,
   including the expertise owners' objections and conditions and the
   recorded opinions. In a project with a roster, only holders of the
   issue's required expertise make the decision. Reserved decisions are
   made by the stakeholder after the required expertise owners have given
   their verdicts. In solo mode this is relaxed: the one person decides
   every issue, or, in AI-driven mode, the AI decides every issue that is
   not reserved. The choice gate is **choose a proposal / continue
   refining / pause**.
   Choosing, or approving a sole proposal, is the decision; continuing
   returns to refinement; pausing leaves the issue open. A sole proposal
   still needs an explicit choice.
2. Validate the choice against known facts, accepted decisions, the
   overview, and open issues. Each conflict, with its source, must be
   resolved explicitly before recording. If a resolution changes the
   chosen proposal, the changed proposal needs confirmation.
3. Mark resolution points settled by the chosen proposal `✅` with a
   `Resolution` and `Details`; keep unsettled points `❓` and the issue
   open.
4. Attribution: in team or organization mode, a decision accepted by a
   person records that person's full name and role, confirmed rather than
   inferred; in solo mode, it records no attribution. A decision made by
   the agent under AI-driven delegation records `**Decided by:** AI
   (<role>, delegated)` instead, naming the role whose expertise decided.

### Record and Apply

1. At acceptance, use the current UTC time for
   `decisions/<yyyymmdd-hhmm>-<unique-title>.md`. Create one immutable
   record per decision with the following structure. Use the attribution
   line from step 4 above, or omit it in solo mode:

   ```md
   # <Decision title>

   **Accepted by:** <Full name> (<relevant role>)
   **Date:** YYYY-MM-DD

   ## Problem Description
   <Issue, facts, constraints, proposals, and material disagreement,
   including expertise owners' objections and conditions and dissenting
   opinions>

   ## Decision
   <Accepted choice>

   ## Explanation
   <Meaning, boundaries, and reasons>

   ## Consequences
   - <Required changes or effects>
   ```

   After recording, show the record's path and a short summary.

2. Remove the resolved issue from `open-issues.md`; never reuse its ID.
   Leave earlier decisions untouched. If new evidence challenges one,
   raise a new issue instead of editing the accepted record.
3. Update affected project understanding, including `overview.md`, and any
   stale plans or instructions. Link to the decision rather than copying it.
4. Share the decision and the updated understanding through the project's
   shared store, for example by committing and pushing for Git or by
   updating the relevant wiki pages. If the store or the sharing method
   is unknown, ask. Sharing outside the local workspace is an
   outward-facing action and needs the user's approval.

### Prepare Tasks and Follow-ups

1. After acceptance, draft the actionable consequences as tasks. Create a
   file under `tasks/` only for a confirmed instruction with **what**,
   **why**, **how**, **acceptance criteria**, **prerequisites**, and
   **dependencies**. Use the project's task format if present; otherwise
   use `tasks/<unique-title>.md` with a title, a link to the accepted
   decision, and one section for each of those six fields. Specify exact
   actions, outputs, scope, and observable checks. For edits to existing
   text, quote the current text and its replacement. Verify prerequisites
   are available and dependencies complete; use "None" where applicable.
   Do not make the executor resolve an open design choice. A decision may
   yield zero or several tasks; never create one merely to fill the
   folder.
2. If work is blocked or a new issue appears, explain it and treat it as
   a follow-up issue for registration. Keep work still needing design
   with an open issue, not under `tasks/`.
3. Creating a task does not assign, schedule, or start it.

## Exit Gate

Complete when the decision is recorded and shared, the issue removed,
affected understanding updated, and tasks or their absence confirmed.
Report any unresolved blockers or declined tasks; do not claim they are
ready.

## Transition

Return to refining another open issue, or hand an executable task to an
execution capability or a human. Do not start work merely because a task
was created.

## User-driven mode

1. List the proposals neutrally and follow them with the choice gate.
   The user passes the gate. On an issue that requires expertise, the
   user confirms the expertise owner's choice or returns the issue to
   refinement, and does not substitute a choice unless the user holds
   that expertise.
2. The user resolves each conflict, including conflicts between
   expertise owners, and confirms any changed proposal.
3. Review drafted tasks and follow-up issues with the user before
   creating or registering them.
4. Hand a task to execution only on the user's explicit request.

## AI-driven mode

1. For a reserved decision, list every proposal in full with your
   recommendation, followed by the choice gate; only the stakeholder
   chooses.
2. For any other decision, choose yourself as the role whose expertise
   it requires, record it as `Decided by: AI (<role>, delegated)`, and
   report it in one line. Records may be written when
   a burst of work ends.
3. Resolve conflicts yourself unless they touch a reserved decision. AI
   expertise owners decide within their expertise. A conflict between
   expertise owners is settled by the owner of the affected interest.
   When both sides own an affected interest, or the conflict touches a
   reserved decision, it goes to the stakeholder with both positions and
   a recommendation.
4. Confirm tasks and follow-up issues yourself, and hand tasks straight
   to execution within the delegation. Outward-facing sharing remains
   reserved.
