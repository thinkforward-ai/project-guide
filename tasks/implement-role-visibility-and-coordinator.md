# Implement role visibility and the Coordinator catalogue role

**Decision:** [Visible role markers and an explicitly rostered Coordinator](../decisions/20261115-2042-visible-role-markers-and-coordinator.md)

## What

1. Add the role-visibility convention to `skills/glossary/SKILL.md`.
2. Add Coordinator to `skills/glossary/roles-catalogue.md`.
3. Reference the convention from all six lifecycle skills.
4. Remove the skill-integration-pending qualifier from the overview.

## Why

Implement the accepted Q25 decision linked above: make role involvement visible while preserving project-local rosters, existing authority, stakeholder separation, and role-free solo mode.

## How

1. Append `## Role visibility` to `skills/glossary/SKILL.md`, containing the accepted decision's **Display convention** and **Boundaries** verbatim, including their numbered structure. Preserve all existing glossary definitions.
2. Append Coordinator as catalogue item 8, using the six fields under the decision's **Coordinator definition** verbatim. Preserve the existing seven roles and catalogue rules.
3. In each of these files, replace the current `## Trigger` heading exactly once:
   1. `skills/start-project/SKILL.md`
   2. `skills/raise-issue/SKILL.md`
   3. `skills/refine/SKILL.md`
   4. `skills/decide/SKILL.md`
   5. `skills/complete-task/SKILL.md`
   6. `skills/work-on-project/SKILL.md`

   Current text:

   ```md
   ## Trigger
   ```

   Replacement:

   ```md
   For visible role involvement, follow the **Role visibility** convention
   in the Project Guide glossary skill when available. Its absence does
   not block this phase.

   ## Trigger
   ```

4. In `overview.md`, replace the current text:

   ```md
   **Role visibility (accepted; skill integration pending):**
   ```

   with:

   ```md
   **Role visibility:**
   ```

5. Run `git diff --check -- skills overview.md`. Review scenarios with Coordinator present, Coordinator absent, solo mode, cross-project roles, and stakeholder attribution. Verify that removing the added references restores the six phase skills exactly, so their existing gates and authority rules are unchanged.
6. Do not change any roster, accepted decision, input artifact, installed skill, or unrelated issue. Do not commit, push, or close the task.

## Acceptance Criteria

1. The glossary contains exactly one `## Role visibility` section, with the accepted display convention and boundaries verbatim.
2. Coordinator is catalogue item 8, and all six definition fields match the decision. Existing catalogue content is unchanged.
3. All six lifecycle skills contain the exact reference above once, before their unchanged `## Trigger` heading. No other phase-skill text changes.
4. The overview no longer marks skill integration pending, and its roster is unchanged.
5. Scenario review confirms that Coordinator tags require an explicitly rostered and acting Coordinator; absent Coordinator means untagged coordination; solo mode stays role-free; cross-project role use and AI impersonation of the stakeholder remain prohibited; tags grant no additional authority.
6. The glossary remains optional. Existing lifecycle gates, decision authority, and roster-confirmation rules remain unchanged.
7. `git diff --check -- skills overview.md` passes. Task and decision links resolve.
8. Installed skills, rosters, accepted decisions, and unrelated issues remain unchanged. No installation, commit, push, or task closure is performed.

## Prerequisites

1. The accepted decision and writable source files are available.
2. Each phase skill contains `## Trigger` exactly once.
3. The glossary has no Role visibility section, the catalogue ends at item 7, and the overview contains the quoted pending qualifier exactly once.
4. The user reviewed the task instructions and explicitly authorized both creation and execution.

## Dependencies

1. The linked visible-role-markers decision, accepted.
2. The [project roles](../decisions/20261115-1850-project-roles.md), [framework consistency](../decisions/20261115-1921-framework-consistency-and-guardian.md), and [role scope boundary](../decisions/20261115-1929-role-scope-boundary.md) decisions, accepted.

## Framework Guardian Verdict

1. No concern: the task implements the accepted convention and Coordinator definition, preserves the optional glossary and existing authority, and does not add Coordinator to any roster.

## Execution Evidence

Implemented locally on 2026-11-15 after the user's explicit authorization to create and implement the task. Formal closure through `complete-task` still awaits confirmation.

1. Criterion 1: an exact text comparison verified that the single `## Role visibility` section in `skills/glossary/SKILL.md` matches the decision's display convention and boundaries verbatim, with all earlier glossary content preserved.
2. Criterion 2: an exact text comparison verified that catalogue item 8 contains the decision's six Coordinator fields verbatim and that the preceding catalogue content is unchanged.
3. Criterion 3: each of the six phase skills matches its pre-execution content with only the approved reference inserted before `## Trigger`.
4. Criterion 4: the only implementation change to the overview removes the pending qualifier. Its entire Collaboration section, including the roster, is unchanged.
5. Criterion 5: source-based scenario review confirmed the explicit roster-and-acting requirement, untagged coordination when Coordinator is absent, role-free solo mode, cross-project scope limits, stakeholder separation, and authority-neutral tags. This was a review of the instructions, not a behavioral test of an autonomous agent.
6. Criterion 6: all six references retain the optional-glossary wording. Exact before-and-after comparisons confirmed that existing phase gates, authority, and roster-confirmation rules were not edited.
7. Criterion 7: `git diff --check -- skills overview.md` passed. All four task decision links resolve. Task whitespace and final-newline checks passed.
8. Criterion 8: before-and-after comparisons confirmed that the accepted decision and open issue register were unchanged during implementation. Only the nine source targets and this task were edited. No installed skills, rosters, or other records were changed; no installation, commit, push, or task closure was performed.
