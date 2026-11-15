# Require milestone demos and stakeholder confirmation

**Decision:** [Required milestone demos and stakeholder confirmation in every mode](../decisions/20261115-2330-required-milestone-demos-and-confirmation.md)

## What

1. Align the source glossary, lifecycle orchestrator, and project-start roadmap template with the accepted Q22 rule.

## Why

1. Criteria-only milestone achievement must not bypass a required demo and explicit human stakeholder confirmation in any mode. Non-runnable outcomes need an HTML-slide presentation.

## How

1. Apply the exact patch below from the repository root. Paths are repository-relative. It changes only `skills/glossary/SKILL.md`, `skills/work-on-project/SKILL.md`, and `skills/start-project/SKILL.md`.

```diff
*** Begin Patch
*** Update File: skills/glossary/SKILL.md
@@
 14. **Milestone:** A roadmap step with an intent, observable "done when"
-    criteria, and a one-line progress log. In user-driven mode it is
-    achieved when all criteria are met; in AI-driven mode it is then ready
-    for a demo and achieved when the stakeholder confirms it. Adding,
-    replacing, redefining, or cancelling one requires a decision.
+    criteria, a demo, and a one-line progress log. In every mode, meeting
+    the criteria makes it ready for a demo, not achieved. Achievement
+    requires an evidence-backed demo followed by explicit confirmation
+    from the project's designated human stakeholder acceptance authority.
+    In solo mode the user confirms without introducing roles; with several
+    stakeholders, use the project's accepted authority arrangements and
+    never infer consent or a quorum. Run or directly show the outcome
+    where possible; otherwise prepare and present HTML slides explaining
+    the outcome and its acceptance evidence. Slides do not replace unmet
+    criteria. Record the demo date, evidence or artifact reference, and
+    explicit confirmation in the progress log; without confirmation, keep
+    the milestone unachieved and do not advance the current milestone on
+    that basis. Adding, replacing, redefining, or cancelling one requires
+    a decision.
*** Update File: skills/work-on-project/SKILL.md
@@
-   criteria it satisfies `✅`. When all criteria of a milestone are met,
-   it is achieved as the mode sections describe, and then the next one
-   becomes current. Changing milestones
-   needs a decision, not this step.
+   criteria it satisfies `✅`. When all criteria of a milestone are met,
+   it is ready for a demo, not achieved. Follow Milestone Acceptance below;
+   only after the demo and explicit stakeholder confirmation is it
+   achieved and the next one becomes current. Changing milestones needs
+   a decision, not this step.
@@
-## Skill Update Check
+## Milestone Acceptance
+
+1. In every collaboration and driving mode, deliver an evidence-backed
+   demo when all milestone criteria are met. Run or directly show the
+   outcome where possible; otherwise prepare and present HTML slides
+   explaining the outcome and its acceptance evidence. Slides do not
+   compensate for unmet criteria.
+2. Achievement requires explicit confirmation after the demo from the
+   project's designated human stakeholder acceptance authority. In solo
+   mode the user confirms without introducing roles. With several
+   stakeholders, follow the project's accepted authority arrangements;
+   if those are unclear, do not infer confirmation or invent a quorum.
+3. Record the demo date, evidence or artifact reference, and explicit
+   confirmation in the existing roadmap progress log. Silence, checked
+   criteria, AI judgement, and slide delivery are not confirmation.
+4. Without confirmation, keep the milestone unachieved and do not advance
+   the current milestone on that basis. Independent work retains its
+   existing permissions.
+
+## Skill Update Check
@@
-3. A milestone is achieved when all its criteria are met.
+3. Meeting criteria alone never achieves a milestone; follow Milestone
+   Acceptance, including the demo and explicit stakeholder confirmation.
@@
-4. When all criteria of a milestone are met, the milestone is ready for a
-   demo, not reached. Give the stakeholder a demo; it is reached when they
-   confirm it.
+4. Follow Milestone Acceptance. Stakeholder confirmation after the demo
+   remains reserved and cannot be supplied by the AI.
*** Update File: skills/start-project/SKILL.md
@@
 - ❓ <observable criterion>

+**Demo:** <run or directly show the outcome; otherwise present HTML slides>
+
 **Progress:**

-- YYYY-MM-DD: <what was done>
+- YYYY-MM-DD: <progress; demo date and evidence/artifact reference, and explicit confirmation when received>
@@
 Milestones appear in intended order. Achieved or cancelled milestones
 stay listed and say so under their heading.
+In every mode, meeting criteria makes a milestone ready for a demo, not
+achieved. Achievement requires an evidence-backed demo and then explicit
+confirmation from the project's designated human stakeholder acceptance
+authority. In solo mode the user confirms without introducing roles; with
+several stakeholders, follow accepted authority arrangements and never
+infer consent or a quorum. Run or directly show the outcome where possible;
+otherwise prepare and present HTML slides with the acceptance evidence.
+Record the demo date, evidence or artifact reference, and explicit
+confirmation in Progress. Slides, checked criteria, silence, and AI judgement
+do not replace confirmation; without it, keep the milestone unachieved and
+do not advance the current milestone on that basis.
*** End Patch
```

2. Check every criterion below using exact source comparisons and source-based scenario review. This is an instruction review, not an autonomous-agent behavioral test.
3. Record execution evidence here. Do not change installed skills, accepted decisions, rosters, unrelated issues, or `roadmap.md`; do not commit, push, or close this task as part of execution.

## Acceptance Criteria

1. The three source files match the exact patch, with all unrelated content preserved.
2. All modes distinguish criteria met, demo delivered, and explicit human confirmation. Neither criteria checks nor AI judgement can achieve a milestone.
3. Direct demonstrations are used for runnable/showable outcomes; otherwise HTML slides are prepared and presented with acceptance evidence. Slides do not compensate for unmet criteria or replace confirmation.
4. Solo remains role-free and the user confirms. Multi-stakeholder projects use accepted authority arrangements; unclear authority, silence, or an invented quorum cannot supply acceptance.
5. Demo date, evidence/artifact reference, and explicit confirmation are recorded in the existing roadmap progress log. Without confirmation the milestone remains unachieved, while unrelated independent work keeps its existing permissions.
6. The roadmap template has a Demo field and confirmation guidance, without a new tracking file or automatic milestone creation.
7. Whitespace checks pass, the decision link resolves, and source-based scenarios cover user-driven, AI-driven, solo, multiple stakeholders, HTML presentations, withheld confirmation, and unmet criteria.
8. Installed skills, earlier decisions, rosters, unrelated records, and the unadopted roadmap remain unchanged. No commit, push, installation, or task closure occurs.

## Prerequisites

1. The linked Q22 decision is accepted and present locally.
2. The three writable source files contain the exact current snippets in the patch.
3. The current project is AI-driven; the Framework designer approves this exact implementation wording within the accepted policy, and the Framework guardian gives a no-concern verdict before execution.

## Dependencies

1. The linked Q22 decision, accepted.
2. Existing lifecycle, delegation, roles, and guardian rules remain in force. No dependency requires adopting Q13 or reopening Q15.

## Framework Guardian Verdict

1. No concern: the exact source patch implements the accepted Q22 policy, preserves human confirmation and role-free solo mode, and does not alter existing permissions or imply roadmap acceptance. Framework designer approved this exact wording under the existing AI delegation before execution.

## Execution Evidence

Implemented locally on 2026-11-15 under the project's AI delegation after the stakeholder accepted the linked Q22 proposal. This records implementation evidence, not formal task closure or milestone confirmation.

1. Criterion 1: exact comparisons against the three HEAD source files with only the task's recorded patch applied matched all three working files. All surrounding source content is preserved.
2. Criterion 2: source checks verified the shared readiness/demo/confirmation rule, removal of automatic user-driven achievement, and the explicit prohibition on AI-supplied stakeholder confirmation.
3. Criterion 3: all three files require direct demonstration where possible and HTML slides otherwise. The shared orchestrator rules explicitly reject slides as compensation for unmet criteria or as confirmation.
4. Criterion 4: all three files preserve role-free solo confirmation by the user and accepted multi-stakeholder authority arrangements. The orchestrator rejects inferred confirmation and invented quorums.
5. Criterion 5: the shared rules require the demo date, evidence or artifact reference, and explicit confirmation in existing roadmap progress; withheld confirmation prevents achievement/current-milestone advancement while preserving independent-work permissions.
6. Criterion 6: the starter template includes a Demo field, progress guidance, and the shared human-confirmation requirement. No new tracking file or milestone was created.
7. Criterion 7: `git diff --check` passed. Ten source-based scenarios covered mode consistency, direct/HTML demonstrations, solo and multiple stakeholders, removal of automatic achievement, AI non-authority, withheld confirmation, unmet criteria, template guidance, and trace evidence. The task's decision link and local Markdown file links in the decision, overview, and issue register resolve. These were source checks, not an autonomous-agent behavioral demonstration.
8. Criterion 8: only the three source targets and this task were edited during source implementation. No installed skills, earlier decisions, rosters, unrelated records, or adopted roadmap were changed; no installation, commit, push, or task closure occurred. Decision-phase reconciliation left 18 unique open issues, removed Q22, retained Q13 and Q31, and preserved all other issue records. Q15 remains parked. The new decision remains local and unshared.
