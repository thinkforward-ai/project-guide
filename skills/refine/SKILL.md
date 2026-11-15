---
name: refine
description: Investigate an open project issue, clarify meaning and requirements, and develop reviewable proposals without choosing one.
source: https://github.com/thinkforward-ai/project-guide
---

# Refine

Develop an open issue into proposals for a decision. Work on the initial
project issue or a later registered issue; do not decide it.

Be concise: lead with what matters, ask only what is needed now, and
never repeat content the user has just seen. Proposals are exempt: they
must carry all information needed to make a decision.

## Trigger

Refinement of a registered issue has been chosen, whether right after
registration, by explicit request, or by continuing an authorized
refinement. The mode sections say who chooses.

## Entry Gate

The issue must be registered and its refinement chosen. New input for an
issue not under refinement does not start refinement by itself; it raises
the refine-now-or-later choice. An unregistered issue goes to registration
first. Do not treat a provisional goal or unreviewed idea as settled. If the
project uses a different register, layout alignment comes first.

## Work

1. Read the issue, relevant input, current overview, and accepted
   decisions. Identify what is known, disputed, and missing.
2. Clarify the issue's meaning, requirements, constraints, and evidence.
   Distinguish facts, opinions, and proposals; record sources,
   uncertainty, and contradictions without inventing certainty. Do not
   settle unresolved rules for classifying input or authority.
3. When a question arises, judge its size. A small question that
   clarifies the current issue stays with it and is resolved as part
   of its decision. A question big enough to start its own discussion,
   or a new independent gap or contradiction, becomes a candidate for
   registration as another open issue. Keep its relationship to the
   parent in the issue context; do not silently choose a solution for
   either.
4. Develop one or more distinct proposals in the Proposal Format. Keep
   concise findings and proposals with the open issue. Update the
   overview only with understanding already settled.
5. When proposals are ready to be listed for a choice, hand off to the
   decision phase; listing proposals belongs to it. Do not mark
   resolution points accepted, create a decision record, or create
   tasks here.

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

Whenever a choice is requested, show every proposal in full; never refer
to proposals only by name, number, or summary.

## Exit Gate

Proposals are recorded with the open issue, relevant blockers are
explicit, and they are ready to be listed for a choice. A single proposal
is valid but is not automatically accepted. Pause leaves the issue open
without a decision.

## Transition

When proposals are ready, hand off to the decision phase. Otherwise stop
or continue refinement.

## User-driven mode

1. The user chooses whether to refine new input now or later, approves
   registering split-off issues, and decides when to continue, hand off,
   or pause.
2. Discuss with contributors without gates until the proposals are ready.

## AI-driven mode

1. Drive the refinement. Choose refine now or later, register split-off
   issues, and judge when proposals are ready; state each choice and its
   reason in one line.
2. Settle details yourself and record them as findings. Ask the
   stakeholder only about reserved decisions or facts only they can
   supply, and batch such questions.
3. For a reserved decision, hand off so the stakeholder chooses. For any
   other decision, continue straight into the decision phase without
   stopping.
