---
name: refine
description: Investigate an open project issue, clarify meaning and requirements, and develop reviewable proposals without choosing one.
source: https://github.com/thinkforward-ai/project-guide
---

# Refine

Develop an open issue into proposals for a decision. Work on the initial
project issue or a later registered issue; do not decide it.

## Trigger

Use when someone explicitly asks to refine a registered issue, chooses
to refine now after registration, or continues an already authorized
refinement.

## Entry Gate

The issue must be registered and the user must have chosen to refine
it. If new input arrives for an issue not under refinement, ask whether
to refine now or leave it open for later. If unregistered, propose
registering it first. Do not treat a provisional goal or unreviewed idea
as settled. If the project uses a different register, seek approval for
layout alignment before changing its issues.

## Work

1. Read the issue, relevant input, current overview, and accepted
   decisions. Identify what is known, disputed, and missing.
2. Clarify the issue's meaning, requirements, constraints, and evidence
   with contributors. Distinguish facts, opinions, and proposals; record
   sources, uncertainty, and contradictions without inventing certainty.
   Do not settle unresolved rules for classifying input or authority.
3. When a new independent gap or contradiction appears, propose registering
   it as another open issue. Keep its relationship to the parent in the
   issue context; do not silently choose a solution for either.
4. Develop one or more distinct proposals in the Proposal Format. Keep
   concise findings and proposals with the open issue. Update the
   overview only with understanding already settled.
5. Offer **Review proposals / Continue refinement / Pause**. When the
   user chooses review, present the proposals in the Proposal Format,
   then the remaining uncertainty.
   Ask whether they are ready for a later decision or need revision;
   record the confirmation with the open issue. Do not select a
   winner, mark resolution points accepted, create a decision record, or
   create tasks.

## Proposal Format

Use this format whenever proposals are recorded or presented:

```md
**Problem:** <what the proposals solve, in one or two sentences>

1. **<Proposal name>:** <solution description>
   - **Pros:** <benefits and supporting evidence>
   - **Cons:** <risks, trade-offs, and dependencies>
```

Always use a numbered list so proposals can be selected or referenced
by number. Do not use tables.

Whenever asking for review or a choice, show every proposal in full;
never refer to proposals only by name, number, or summary.

## Exit Gate

The proposals were reviewed, relevant blockers are explicit, and the user
confirmed they are ready for decision. A single proposal is valid but is
   not automatically accepted. Continue refinement when revisions are
requested; Pause leaves the issue open without a decision.

## Transition

When the user asks to choose among the reviewed proposals, hand off to
the decision phase. Otherwise stop or continue refinement as chosen.
