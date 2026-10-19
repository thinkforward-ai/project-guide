# Add skill update checks to status

**Decision:** [Skill update checks in status](../decisions/20261019-0218-skill-update-checks-in-status.md)

## What

1. Add the accepted read-only skill update check to `skills/work-on-project/SKILL.md`.

## Why

1. Implement the linked decision: check all skills used by the project while keeping the update list concise, exposing incomplete coverage, and preserving separate update approval.

## How

1. In `skills/work-on-project/SKILL.md`, replace the current text:

   ```md
   ## AI-driven mode
   ```

   with:

   ```md
   ## Skill Update Check

   1. Only when status is requested or chosen, check installed skills
      evidenced by project records and observed project work as used
      by this project. Include non-Project Guide skills; exclude
      unrelated installs. Briefly state scope and flag incomplete
      coverage. Do not introduce a configuration format.
   2. When source comparison is needed, use an available skill-management
      capability. Compare verified original sources, accounting for
      known installation transformations. Distinguish current skills,
      updates, local modifications or uncertain differences, and
      unchecked skills. Never call an uncertain difference an update.
      Missing sources, source access, or checking capabilities leave
      affected skills unchecked and must not block status.
   3. Show a short list of skill names with available updates, without
      delta details or change descriptions. Briefly summarize current
      results and uncertain or unchecked coverage, with short reasons
      where needed; do not produce a full per-skill report. If no
      updates are found, limit that claim to checked skills.
   4. Show detailed differences only on the user's request or during
      update review.
   5. Keep checks read-only. Reviewing and applying updates belongs to
      a separately requested and explicitly approved update flow.

   ## AI-driven mode
   ```

2. Review the wording against every case in the acceptance criteria and run `git diff --check`.
3. Do not install or update skills. Preserve all other skill text.

## Acceptance Criteria

1. Requested or chosen status checks project skills; ordinary resumption or a direct phase call does not automatically trigger the check.
2. The check includes evidenced Project Guide and non-Project Guide skills, excludes unrelated installs, and briefly discloses checked scope and incomplete coverage without requiring a new configuration format.
3. Source comparisons account for known installation transformations and distinguish available updates from local modifications or uncertain differences. Missing sources, source access, or checking capabilities leave affected skills unchecked without blocking status.
4. Status lists skill names with updates available, without delta details or change descriptions. Other results and coverage are summarized briefly, not as a full per-skill report. A no-update result is limited to checked skills.
5. Detailed differences appear only on request or during update review. Checks remain read-only; review and updates retain their separate request and approval gate.
6. The existing lifecycle gates and AI-driven behavior remain unchanged. No skill is installed or updated.
7. `git diff --check` passes.

## Prerequisites

1. The linked accepted decision exists.
2. `skills/work-on-project/SKILL.md` is available and contains the quoted `## AI-driven mode` heading once. Both prerequisites were verified during task review.

## Dependencies

1. None.

## Subsequent User Adjustment

1. After implementation (2026-10-19), the user asked for a shorter section with the same behavior. `skills/work-on-project/SKILL.md` now carries a condensed four-rule Skill Update Check that still meets every acceptance criterion. The verbatim text above and the linked decision remain as records.
