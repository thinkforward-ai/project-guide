# Tasks

Store one reviewed, executable instruction per Markdown file. Each task links
to an accepted decision and specifies what, why, how, acceptance criteria,
prerequisites, and dependencies. Required inputs, access, and environment
must be available, dependencies complete, and implementation choices settled
before registration. Keep researchable gaps with an open issue, not under
`tasks/`. Readiness does not mean assigned, scheduled, or started.

Use this structure for each task:

```md
# <Outcome-oriented title>

**Decision:** ../decisions/<accepted-decision>.md

## What

<Specific output>

## Why

<Reason and link to the originating decision>

## How

1. <Exact action, target, and scope>

## Acceptance Criteria

1. <Observable completion check>

## Prerequisites

<Required available input, access, and environment, or None>

## Dependencies

<Completed prior work or decisions, or None>
```
