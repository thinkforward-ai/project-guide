# Framework consistency fixes and the guardian role

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-11-15

## Problem Description

The founder asked for a review of how the [AI-driven delegation](20261115-1809-ai-driven-mode-as-delegation.md) and [project roles](20261115-1850-project-roles.md) decisions land in the framework, looking for conflicts and dead loops. The founder also asked for a project-guide guard and change reviewer role: an immune system that filters additions and modifications to keep the framework consistent and true to its original goal and purpose.

The review found five conflicts, three stall or loop risks, and several gaps:

1. Reserved decisions versus expertise-owner authority.
2. Gate passing versus expertise authority in user-driven mode.
3. Solo relaxation versus AI-driven delegation.
4. Earlier decisions and overview §7 that still assign delegated steps to the user.
5. Overview §8 requiring experts to answer every opinion, versus opinions that are only recorded.
6. No acceptance step for roster changes, which risks a loop.
7. Conflicts in which both sides own an affected interest.
8. No stop condition in AI-driven mode.

The gaps were that AI attribution does not name the deciding role, that some passages and open issues are stale, and that Project Guide has no roster of its own. The founder accepted every recommended fix.

## Decision

1. **Reserved decisions:** the stakeholder decides them, after the required expertise owners have given their verdicts.
2. **Gates versus authority:** passing a gate is not choosing. In user-driven mode, the user confirms the expertise owner's choice or returns the issue to refinement, and does not substitute a choice unless the user holds that expertise.
3. **Solo:** the one person decides every issue, or, in AI-driven mode, the AI decides every issue that is not reserved.
4. **Alignment of earlier decisions:** in AI-driven mode, the user-specific steps in [proposal choice is the decision](20261004-1551-proposal-choice-is-the-decision.md), [project lifecycle orchestration](20261003-1603-project-lifecycle-orchestration.md), and the [complete-task skill](20261019-2137-complete-task-skill.md) are carried out as the AI-driven mode sections describe. They remain unchanged in user-driven mode. Overview §7 is worded independently of mode.
5. **Opinions:** opinions are recorded and considered, not answered one by one. Dissenting opinions are listed in the decision record's Problem Description. Overview §8 is amended accordingly.
6. **Roster changes:** roster changes are neither issues nor decisions. In user-driven mode the user confirms them; in AI-driven mode the AI adds them and reports them. The stakeholder may change the roster at any time.
7. **Conflicts with two owners:** when both sides of a conflict own an affected interest, it goes to the stakeholder with both positions and a recommendation.
8. **Stopping in AI-driven mode:** the agent stops and reports when the current milestone is ready for a demo, when only reserved decisions remain, or when nothing applicable is left.
9. **Attribution:** an AI decision records `**Decided by:** AI (<role>, delegated)`, and an AI completion records `**Confirmed by:** AI (<role>, delegated)`.
10. **Stale passages:** `refine` and overview §8 classify input by the roster's expertise and still do not certify facts. Q3, Q4, and Q15 reference the roles decision. `raise-issue`'s trigger and wrapping leftovers are fixed.
11. **Guardian role:** the catalogue gains a generic Guardian, which protects a project's durable definition and its original goal and purpose. Project Guide's own roster starts with the stakeholder and a framework guardian. The framework guardian's expertise is required on every issue that changes skills, the glossary, the overview, the layout, or decisions. Its objection blocks the change until it is resolved or the stakeholder overrides it.

## Explanation

1. These fixes keep both new decisions and remove contradictions and stalls without adding steps.
2. The earlier decisions stay unchanged as records. This decision states how they apply in AI-driven mode.
3. Project Guide's roster is provisional while its collaboration mode stays open in Q15.

## Consequences

- Update `decide`, `refine`, `raise-issue`, `work-on-project`, `complete-task`, the glossary, the role catalogue, `overview.md` §3, §7, §8, and §10, and the contexts of Q3, Q4, and Q15.
- Projects piloting these rules align their local overrides.
