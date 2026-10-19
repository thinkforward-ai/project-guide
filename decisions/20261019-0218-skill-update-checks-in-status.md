# Skill update checks in status

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-10-19

## Problem Description

1. Q20 asked how project status should check for skill updates and report the result. Founder input (2026-10-19): "status should also check skill updates". The status path in `skills/work-on-project/SKILL.md` covered project records but not skill updates.
2. During refinement, the founder selected "All skills used by this project", rather than only Project Guide skills or every installed skill, and added: "Make sure that the list of skills to update - is short and concise. No delta details. More details can be shown on request from user / during review".
3. The current layout does not require a complete project skill inventory. Integration configuration remains unresolved in Q5. Available skill-management capabilities can compare verified sources and installed copies, but source access, local changes, and incomplete evidence can prevent a reliable result. No live update check was performed during refinement.
4. One proposal, a read-only project skill check, was developed and revised to include the concise display requirement. The founder explicitly approved the revised proposal and confirmed the attribution above. This decision does not resolve Q15's collaboration mode.

## Decision

1. Whenever project status is requested or chosen, check installed skills used by the project, including Project Guide and other skills evidenced by project records and observed project work. Exclude unrelated installed skills.
2. Keep the result concise: list the names of skills with available updates, without delta details or change descriptions. Show detailed differences only at the user's request or during update review.
3. Keep checks read-only. They do not authorize skill installation or updates.

## Explanation

1. Briefly state the checked scope and flag incomplete coverage when the full set of project skills cannot be established. Do not introduce a configuration format while Q5 remains unresolved.
2. Use an available skill-management capability to compare each skill with its verified original source, accounting for known installation transformations. Project Guide does not require Agent Hub or any other particular manager.
3. Distinguish up-to-date skills, available updates, local modifications or uncertain differences, and unchecked skills. A difference alone is not proof of an update when local changes or provenance make it uncertain.
4. Summarize up-to-date results and uncertain or unchecked coverage briefly, with short reasons where needed. Do not expand status into a full per-skill report. When no updates are found, limit that claim to checked skills; do not imply unchecked skills are current.
5. Missing sources, source access, or checking capabilities leave affected skills unchecked and do not block the rest of status. Remote checks may add latency, and coverage may remain partial without a complete inventory.
6. Reviewing and applying updates belongs to a separately requested and explicitly approved update flow. Requested explanations and update review may show detailed differences; status alone must not install or update anything.
7. The check runs only when status is requested or chosen, not automatically on every resume or direct phase call. It preserves the orchestrator's existing lifecycle gates.

## Consequences

1. Add these status-check requirements to `skills/work-on-project/SKILL.md` through a reviewed implementation task.
2. Link this decision from `overview.md` and remove resolved Q20 from `open-issues.md`, retaining `Next question ID: Q21`.
3. Do not install or update skills as part of this framework change. Task creation does not authorize execution.
