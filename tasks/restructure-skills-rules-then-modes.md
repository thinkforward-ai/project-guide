# Restructure skills into a framework part followed by mode sections

**Decision:** [AI-driven mode as delegation](../decisions/20261115-1809-ai-driven-mode-as-delegation.md)

## What

All seven skills (`start-project`, `raise-issue`, `refine`, `decide`, `work-on-project`, `complete-task`, `glossary`) follow the accepted structure: a mode-independent framework part, followed by `## User-driven mode` and `## AI-driven mode` sections. AI-driven sections carry the delegation rules. The glossary and `overview.md` match.

## Why

The decision linked above replaces the interim AI-driven gate split with delegation, and separates what must be true from who decides.

## How

1. In each phase skill, rewrite user-specific gates in the framework part as neutral conditions or choices that point to the mode sections. Keep the entry and exit gates and the transition in the framework part, before the mode sections.
2. Add a `## User-driven mode` section stating who passes each choice: the user, as before.
3. Replace each `## AI-driven mode` section with the delegation behaviour:
   1. The agent decides everything that is not reserved.
   2. Proposals for reserved decisions go to the stakeholder in full, with a recommendation.
   3. Agent decisions and task completions are recorded as `AI (delegated)`.
   4. Milestones reach a demo checkpoint and are confirmed by the stakeholder.
4. In the glossary, revise Gate, Milestone, AI-driven, and User-driven, and add Reserved decision, Framework part, and Mode section.
5. In `overview.md`, update the driving-mode description and link the decision.
6. Preserve the existing uncommitted `tasks/closed/` changes in `start-project` and `work-on-project`.

## Acceptance Criteria

1. Each of the six phase skills ends with `## User-driven mode` followed by `## AI-driven mode`, placed after its framework sections.
2. No framework part says that only the user decides or that the agent must ask the user, except for outward-facing sharing and information only the user has.
3. The glossary defines Reserved decision, Framework part, and Mode section.
4. `overview.md` links the decision; Q23 is no longer in `open-issues.md`.

## Prerequisites

None.

## Dependencies

[AI-driven mode as delegation](../decisions/20261115-1809-ai-driven-mode-as-delegation.md), accepted.

## Execution note

Executed on 2026-11-15 in the working tree, on request, right after the decision. Nothing is committed. Closing the task through `complete-task` awaits the user's confirmation.
