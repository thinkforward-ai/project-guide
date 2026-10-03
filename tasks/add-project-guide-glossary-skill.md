# Add the Project Guide glossary skill

**Decision:** [Shared vocabulary and orchestrator preflight](../decisions/20261003-1525-shared-vocabulary-and-orchestrator-preflight.md)

## What

An optional, individually installable Project Guide glossary skill defines
the agreed core terms. Direct phase skills remain usable without it.

## Why

Implement the accepted shared vocabulary decision linked above. The first
two terms, **Issue** and **Task**, distinguish researchable problems from
instructions ready for execution.

## How

1. Create `skills/glossary/SKILL.md` with exactly this content:

   ````md
   ---
   name: glossary
   description: Define Project Guide terminology. Use when a term needs clarification.
   source: https://github.com/thinkforward-ai/project-guide
   ---

   # Glossary

   1. **Issue:** An identified, unresolved problem, unknown, contradiction, or
      choice that requires investigation or resolution.
   2. **Task:** A specific, reviewed instruction for executable work with no
      unresolved design choices.
   3. **Solution:** A way to resolve an issue, whether proposed or accepted.
   4. **Proposal:** A candidate solution with supporting reasons and trade-offs.
   5. **Decision:** An explicitly accepted choice of a solution for an issue.
   6. **Trigger:** An event or condition that makes an activity relevant.
   7. **Gate:** A required condition or user choice before an activity starts or ends.
   8. **Transition:** Movement from one activity to another after a gate.
   ````

2. Do not change the orchestrator, the Agent Hub installer, existing phase
   skills, accepted decisions, or task files as part of this task. Do not
   install or publish the new skill.
3. Check the new file's frontmatter, eight terms, final newline, and
   `git diff --check`. Report the checks and the new source path.

## Acceptance Criteria

1. `skills/glossary/SKILL.md` exists with `name: glossary` and the Project Guide source URL.
2. All eight definitions, including **Issue**, **Task**, and **Solution**, match the instructions above.
3. No unrelated files were changed; the glossary neither requires installation nor defines facts or expertise.
4. `git diff --check` passes. No installation or publication was performed.

## Prerequisites

A writable Project Guide source checkout with the accepted decision and
current phase skills available. No external account or orchestrator is
needed.

## Dependencies

The accepted decision linked above. The accepted
[orchestrator decision](../decisions/20261003-1603-project-lifecycle-orchestration.md)
defines its future use of the glossary, but implementing the orchestrator
is not a prerequisite for this source-file change. No other prior work is
required.
