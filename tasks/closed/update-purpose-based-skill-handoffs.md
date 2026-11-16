# Replace direct cross-skill handoffs with purposes

**Decision:** [Project lifecycle orchestration](../../decisions/20261003-1603-project-lifecycle-orchestration.md).
**Approved rollout:** [ThinkForward-native reference cleanup](https://github.com/thinkforward-ai/agent-hub/blob/main/decisions/20261116-0215-rollout-purpose-based-native-skills.md).

## What

Apply the user-approved purpose-based reference edits to the six lifecycle
skills, without changing their lifecycle responsibilities or gates.

## Why

Keep direct phase calls and resource discovery independent of another
provider's installed skill name or folder layout.

## How

1. Retain the verified pre-edit source and metadata. Apply only the exact
   replacements below; stop rather than overwriting concurrent edits.

   1. **role-visibility** in `project-guide/skills/start-project/SKILL.md`, `project-guide/skills/refine/SKILL.md`, `project-guide/skills/decide/SKILL.md`, `project-guide/skills/raise-issue/SKILL.md`, `project-guide/skills/work-on-project/SKILL.md`, `project-guide/skills/complete-task/SKILL.md`:

      Replace:

      ```text
      For visible role involvement, follow the **Role visibility** convention
      in the Project Guide glossary skill when available. Its absence does
      not block this phase.
      ```

      With:

      ```text
      For visible role involvement, use an available project-terminology
      capability to find the **Role visibility** convention through its own
      instructions. Its absence does not block this phase.
      ```

   1. **starter-role-resource** in `project-guide/skills/start-project/SKILL.md`:

      Replace:

      ```text
         roles from the starter role catalogue (`roles-catalogue.md` in the
         Project Guide glossary skill) that the idea evidently needs, adapted to
         the project. For needed expertise
      ```

      With:

      ```text
         roles the idea evidently needs from an available starter role catalogue,
         adapted to the project. Identify a matching provider by description and
         follow its instructions to locate the catalogue. For needed expertise
      ```

   1. **optional-terminology** in `project-guide/skills/work-on-project/SKILL.md`:

      Replace:

      ```text
      If no project exists and a new goal was supplied, bootstrap it. When an
      optional Project Guide glossary skill is installed, read its main terms and
      check them internally before starting or resuming. Its absence does not
      block progress or require a user-facing recitation.
      ```

      With:

      ```text
      If no project exists and a new goal was supplied, bootstrap it. When an
      available capability provides project terminology, read its definitions
      and check them internally before starting or resuming. Its absence does
      not block progress or require a user-facing recitation.
      ```

   1. **task-completion-handoff** in `project-guide/skills/work-on-project/SKILL.md`:

      Replace:

      ```text
         task** when one looks finished (through `complete-task`; never move
         tasks here),
      ```

      With:

      ```text
         task** when one looks finished (through an available task-completion
         capability; never move tasks here),
      ```

   1. **completion-trigger** in `project-guide/skills/complete-task/SKILL.md`:

      Replace:

      ```text
      Someone reports a task done, or chooses **complete a task** in
      `work-on-project`.
      ```

      With:

      ```text
      Someone reports a task done, or chooses **complete a task** while
      coordinating project work.
      ```

   1. **milestone-progress-provider** in `project-guide/skills/complete-task/SKILL.md`:

      Replace:

      ```text
         3. Add the roadmap progress entry and mark satisfied milestone
            criteria `✅`, as `work-on-project` describes.
      ```

      With:

      ```text
         3. Add the roadmap progress entry and mark satisfied milestone
            criteria `✅`, following the milestone-progress rules from an
            available project-work coordination capability.
      ```

   1. **completion-transition** in `project-guide/skills/complete-task/SKILL.md`:

      Replace:

      ```text
      Next: complete another finished task, register a follow-up issue through
      `raise-issue`, or return to `work-on-project`.
      ```

      With:

      ```text
      Next: complete another finished task, use an available issue-registration
      capability for a follow-up, or return to an available project-work
      coordination capability.
      ```

   1. **proposal-format-provider** in `project-guide/skills/decide/SKILL.md`:

      Replace:

      ```text
      1. Compare every proposal, in full and in the refine Proposal Format,
         against the issue's constraints, evidence, risks, and dissent,
      ```

      With:

      ```text
      1. Compare every proposal, in full and in the proposal format supplied by
         the issue-refinement capability, against the issue's constraints,
         evidence, risks, and dissent,
      ```

2. Check that no foreign skill-name/path handoffs remain in these bodies,
   while preserving the glossary provider's own resource links.
3. Compare complete source files against the expected replacements.
   Preserve optional vocabulary, central role conventions, phase gates,
   driving-mode rules, and the already-accepted milestone demo safeguards.
4. Run whitespace and structural checks. The Framework guardian assesses
   consistency before confirmation. Do not change historical decisions,
   other project work, or any proposed roadmap milestones.

## Acceptance criteria

1. Exactly the six named lifecycle instruction files receive only the
   approved replacements; metadata and every other instruction are unchanged.
2. Provider-led catalogue lookup and purpose-based phase handoffs retain
   their required meanings; direct phase use and optional terminology
   remain supported.
3. The glossary's own internal resource link, central role definitions,
   phase gates, modes, and existing source milestone safeguards are preserved.
4. Complete-file comparisons, structural checks, and scoped whitespace
   checks pass; the Framework guardian has no unresolved objection.

## Prerequisites

1. The user requested the native-only rollout and approved exact source
   edits and publication.
2. Framework guardian verdict: no objection, conditional on the preserved
   framework boundaries stated above.
3. Current source files and the approved recovery baseline are available.

## Dependencies

None. Shared-skill reinstallation is tracked by the approved rollout's
Agent Hub task, not claimed complete by this source-only task.

## Completion

**Date:** 2026-11-16
**Confirmed by:** AI (Framework guardian, delegated)

1. **Exact edits, met:** All six complete source bodies matched the
   reviewed replacements, with original metadata and every other
   instruction preserved.
2. **Portable handoffs, met:** Replaced named terminology, proposal-format,
   task-completion, issue-registration, and coordination references with
   purposes. Starter roles are discovered through a matching provider's
   own instructions instead of a caller-specified resource filename.
   The wording retains direct phase use and optional terminology.
3. **Framework preservation, met:** The glossary and its internal catalogue
   link are unchanged. Complete-file comparisons preserve central role
   definitions, phase gates, driving modes, and existing source milestone
   demo/confirmation requirements. The Framework guardian has no objection.
4. **Validation, met:** Metadata and structural comparisons, foreign-name
   and cross-provider resource checks, and scoped whitespace checks passed.
   Whole-repository whitespace checks reported an unrelated issue-register
   EOF warning; that concurrent work was neither changed nor staged.
   These are source/policy checks, not model-behavior evaluation.
5. **Boundaries:** Publication is explicitly authorized and follows source
   validation. This task does not claim shared-skill installation or any
   milestone achieved; both remain under their own applicable checks.
