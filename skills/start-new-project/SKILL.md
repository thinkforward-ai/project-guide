---
name: start-new-project
description: Initialize a new project, initiative or business idea. Use when someone wants to start one and no project structure exists yet.
source: https://github.com/thinkforward-ai/project-guide
---

# Start New Project

Start fast. A basic description with gaps is fine; gaps become open questions.
Leave analysis and decisions to later phases.

## Trigger

A new project, initiative or business idea.

## Workflow

1. Create `overview.md` from the template, with every section set to `N/A`.
2. Ask the user to choose: a short interview or providing input files. Place provided files in `inputs/` and fill the sections they cover.
3. Fill the remaining sections one at a time, asking one question per `N/A` section. When a reply covers several sections, fill them all and ask the user to review and add anything missing. When the user skips a question, keep that section `N/A`.
4. For Contributing Roles, propose up to 5 roles fitting the project, each with its expertise, and let the user adjust them.
5. Show the complete `overview.md` and revise it until the user approves the final version.
6. Propose the first layer of open questions: the broad, high-level problems the project must solve to reach its goal, plus each section still `N/A`. Keep them at the level of what must be achieved; lower levels come in later breakdowns. Open a new question for each one the user confirms.
7. Create `README.md` and an `AGENTS.md` that describes the project structure: `inputs/`, `overview.md`, `open-questions.md`, `decisions/`.

## Template

```md
# Overview

## Goal

N/A

## Context

N/A

## Scope

N/A

## Constraints

N/A

## Contributing Roles

N/A (role: expertise)
```

## Completed When

The user has approved `overview.md`, the first layer of open questions is registered, and the base files exist.

## After Completion

Summarize what was created, then invite the user to continue breaking the project down, starting with the open question they choose.
