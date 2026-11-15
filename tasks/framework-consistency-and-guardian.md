# Apply the framework consistency fixes and add the guardian role

**Decision:** [Framework consistency fixes and the guardian role](../decisions/20261115-1921-framework-consistency-and-guardian.md)

## What

The skills, glossary, catalogue, overview, open-issue contexts, and `AGENTS.md` reflect fixes 1 to 11 of the decision linked above, and Project Guide has a provisional roster with a framework guardian.

## Why

This removes the conflicts and stall risks that the review found, and gives the framework an immune system for changes.

## How

1. In `decide`, state that reserved decisions follow expertise verdicts, separate passing a gate from choosing, cover solo with AI-driven mode, list dissenting opinions, use role-named AI attribution, and add the two-owner conflict rule.
2. In `refine`, classify input by the roster, mark roster changes as neither issues nor decisions, and add the two-owner conflict rule.
3. In `raise-issue`, use a mode-neutral trigger and add roster-change confirmation per mode.
4. In `work-on-project`, add the AI-driven stop condition.
5. In `complete-task`, use role-named AI attribution.
6. In the glossary, update Solo, AI-driven, Reserved decision, Roster, and Opinion, and add Guardian. In the catalogue, add the Guardian role.
7. In `overview.md`, word §7 independently of mode, amend §8 on opinions and classification, and add a §10 Roles subsection. Update the contexts of Q3, Q4, and Q15, and add a Framework Guardian rule to `AGENTS.md`.

## Acceptance Criteria

1. Each skill and document named above contains its fix.
2. No skill's framework part assigns a delegated step to the user only.
3. Project Guide's overview lists the stakeholder and the framework guardian.

## Prerequisites

None.

## Dependencies

The [AI-driven delegation](../decisions/20261115-1809-ai-driven-mode-as-delegation.md) and [project roles](../decisions/20261115-1850-project-roles.md) decisions, accepted.

## Execution note

Executed on 2026-11-15 in the working tree, right after the decision. Nothing is committed. Closing the task through `complete-task` awaits the user's confirmation.
