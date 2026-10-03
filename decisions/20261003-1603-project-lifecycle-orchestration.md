# Project lifecycle orchestration

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-10-03

## Problem Description

Project Guide had independently usable phase skills but no project-wide entry point that made the complete lifecycle visible and coordinated work across sessions and multiple issues. The earlier thin-router proposal could suggest or invoke a next skill, but did not own the full start, issue, refinement, proposal review, decision, and task-handoff loop. Suggestion-only routing would leave every handoff manual; a stored-stage dispatcher would add state that could go stale or be mistaken for consent. The accepted [shared vocabulary](20261003-1525-shared-vocabulary-and-orchestrator-preflight.md) and [executable task](20261003-1541-executable-task-handoff.md) decisions already constrain this design.

## Decision

Add a `work-on-project` lifecycle orchestrator that presents the whole project and issue pipeline, coordinates phase skills through their triggers and gates, and offers a contextual resume menu. Standardize the body of each phase skill around Trigger, Entry Gate, Work, Exit Gate, and Transition, using its frontmatter description for discovery. Do not add a separate question-stage field.

## Explanation

On starting or resuming, the orchestrator locates the project, reads its overview, open issues, accepted decisions, and executable tasks, and internally checks an installed glossary if available. When the user has not named an action, it offers **show current status**, **refine an open issue**, **review proposals or decide a reviewed issue**, **work on a ready task** through an explicitly requested future execution capability or human handoff, **provide input or an idea**, and **pause**, omitting inapplicable actions. Status is shown when chosen, not automatically on every resume. With multiple relevant issues, the user chooses a focus.

The orchestrator invokes a phase skill only when the user's intent and that skill's entry gate permit it, verifies the exit gate and changed records, then offers the next permitted action. It does not perform phase work, choose a proposal, approve a decision, create a task itself, or start execution. It does not claim a handoff ran if the client cannot invoke the skill. Proposal review offers **Review proposals / Continue refinement / Pause** and does not accept an answer; a later decision offers **Approve / Revise / Pause**. Confirmations needed for resumption stay with the question's existing findings, not in a new stage field. Direct phase calls remain valid.

## Consequences

- Add the orchestrator as an individually discoverable skill with the full lifecycle and consent-aware handoffs.
- Align phase-skill headings and proposal-review gates without changing their distinct responsibilities.
- Keep any new task execution or PM scheduling capability outside the core orchestrator until separately defined.
