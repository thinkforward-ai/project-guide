---
name: raise-issue
description: >
  Raise a newly spotted issue by registering an unresolved problem, unknown, or
  contradiction in open-issues.md. Use when a new issue needs investigation
  or resolution; do not investigate, decide, or resolve it here.
source: https://github.com/thinkforward-ai/project-guide
---

# Raise Issue

Register an issue requiring investigation, judgment, verification, or a decision.
Do not resolve the issue in this skill.

Be concise: lead with what matters, ask only what is needed now, and
never repeat content the user has just seen. Proposals are exempt: they
must carry all information needed to make a decision.

## Trigger

Use when:

- a new blocker, ambiguity, contradiction, or unresolved choice appears;
- missing information prevents safe progress;
- the user confirms a proposed follow-up should be tracked;
- an accepted decision must be reconsidered through a new issue.

## Entry Gate

The issue must be unresolved rather than a routine task. A small
clarification of an issue under discussion belongs to that issue, not a
new one.
Check for duplicates and accepted decisions before registering it; ask
only when missing information prevents a clear record. A user-confirmed
follow-up issue may be registered, but never infer that confirmation.
If the project uses a different register, do not create a parallel one;
seek approval for layout alignment before registration.

## Rules

- `open-issues.md` contains only unresolved issues (no status field).
- Use next stable `Q<n>` ID; advance `Next question ID`; never reuse IDs.
- One issue = one coherent decision. Split independent issues.
- Keep records concise: preserve meaning, not conversation transcripts.
- Check existing issues and decisions before creating duplicates.
- Record only known context; do not invent constraints or resolutions.
- Registration does not authorize investigation or external action.

## Work

### 1. Establish the Need

Capture: the issue's specific question, impact/blocker, minimum context, known constraints, resolution points.

For follow-ups: frame as an issue for investigation or decision. Mention the source decision filename in `### Context` when useful.

Ask user only when missing information prevents a clear record.

### 2. Check for Duplication

Read `open-issues.md` and `decisions/`:

- If an open issue exists: update with non-duplicative context only.
- If a decision resolves it: do not duplicate; explain the existing solution.
- If new evidence challenges a decision: open a new issue; identify the earlier decision in `### Context`.

### 3. Register the Issue

If `open-issues.md` does not exist, create:

```md
# Open Issues

This file contains only unresolved issues that currently require investigation or a decision.

**Next question ID:** Q1
```

Append the new issue using:

```md
## Q<n>: <Concise title>

### Question

<One specific question expressing the issue.>

### Why It Matters

<Concise impact, risk, or blocker.>

### Context

<Only the background needed to understand the issue.>

### Constraints

- <Known hard requirement or boundary>

### Resolution Points

- ❓ **<Point>**
  - **Resolution:** Pending
  - **Details:** <Known context or remaining uncertainty>
```

Omit `### Constraints` when unknown. Add `### Decision Criteria`, `### Findings`, or `### Proposals` later only when useful.

Advance `Next question ID` after appending.

### 4. Validate

Verify: new ID, next ID advanced, coherent issue, no status field, concise/no placeholders, resolution points use `❓`/`Resolution: Pending`, no duplicates, no unauthorized investigation.

Report the created/updated issue ID and title, then offer the transition
choice below. Do not begin investigating as part of registration.

## Exit Gate

This skill ends after registration and the next-step choice. Do not analyze,
decide, resolve, propagate, or create follow-up work here.

## Transition

After registration, ask whether to refine the issue now or leave it open
for later. If the user already explicitly asked to register and refine now,
use that choice without asking again. Refine only after the user chooses now;
if later, leave the issue open and stop. Registration or new input alone
does not authorize refinement, a decision, or a task.
