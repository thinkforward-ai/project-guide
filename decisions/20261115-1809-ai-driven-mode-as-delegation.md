# AI-driven mode as delegation, with rules-then-modes skills

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-11-15

## Problem Description

Q23 asked whether AI-driven mode should let the AI make every decision not reserved for the stakeholder, instead of returning every choice to them. Under the [earlier AI-driven decision](20261004-1852-ai-driven-mode.md), the AI passed transition gates, but decisions and "anything in the user's interest, including how to do the work" went to the stakeholder. In a game project piloting AI-driven mode (2026-11-15), this meant the stakeholder was asked about every rule detail, each answer produced several records, and phase gates interrupted the flow. The user's verdict: "too much bureaucracy going on, too much friction and micro management from my side. And very little progress." Real progress came only from playing the work and from the demo.

The founder preferred redefining AI-driven over adding a new mode, noting that no project depends on the current behaviour. The founder's vision, confirmed after review, sets the skill structure: a mode-independent framework part, followed by mode sections that tune it. One proposal was considered and chosen.

## Decision

1. **Skill structure:** Every skill has a framework part first: its purpose, the records and structure it works with, the rules that always hold, and its steps with entry and exit gates as conditions. It says what happens and what must be true, not who decides. A `## User-driven mode` section and a `## AI-driven mode` section follow and describe how the agent behaves and how the process is managed. They tune the framework part and never break its rules.
2. **User-driven mode:** The user passes the gates and makes the decisions; the agent asks before each transition and offers neutral choices.
3. **AI-driven mode as delegation:**
   1. **Reserved decisions stay with the stakeholder:** project direction and goal, milestone definitions, milestone confirmation, scope changes, platform and technology, naming, irreversible or outward-facing actions (including sharing outside the local workspace), and anything the stakeholder reserves. Everything else is the agent's to decide.
   2. **Flow without stops:** within the delegation, the agent moves from registration through refinement, decision, and task to execution without phase gates. It reports each choice and its reason in one line.
   3. **Records:** decisions the agent makes are recorded with `**Decided by:** AI (delegated)` in place of `Accepted by`, and may be written when a burst of work ends. Session prompts are never saved as input files; `inputs/` holds only material imported from outside the session.
   4. **Stakeholder touchpoints:** questions only for reserved decisions, batched, never during play or a demo; proposals for reserved decisions in full, with a recommendation; a milestone is reached only when the stakeholder confirms it after a demo; the stakeholder may override any AI decision, and an override is recorded as a new decision.
4. The glossary defines the framework part, mode sections, reserved decisions, and both modes accordingly.

## Explanation

1. This supersedes the [earlier AI-driven decision](20261004-1852-ai-driven-mode.md), which stays unchanged as history. Its driving field in the overview, its independence from collaboration mode, and `start-project` asking for the mode remain valid. Its interim gate split and "each section lists only differences" are replaced.
2. Separating what must be true from who acts makes modes possible without forking skills. For example, "proposals are recorded before a decision" is a framework rule, while "the user chooses a proposal" belongs to user-driven mode.
3. Entry and exit gates keep their names and stay in the framework part as conditions; the mode sections say who passes any choice a gate contains.
4. Whether milestone confirmation by demo applies in every mode stays open in Q22; this decision applies it to AI-driven mode only.

## Consequences

- All seven skills are restructured into a framework part, followed by user-driven and AI-driven sections.
- The glossary and `overview.md` describe the new structure and modes.
- Q23 is removed from `open-issues.md`.
- Installed copies of the skills need updating through Agent Hub, which is a separate, approved step.
