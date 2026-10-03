# Shared vocabulary and orchestrator preflight

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-10-03

## Problem Description

Project Guide skills use terms such as issue, proposal, decision, task, trigger, gate, and transition. Without a shared meaning, their handoffs can diverge. Agent Hub installs skills individually, without enforced dependencies, so a repository-only glossary is unavailable to many users and a separate skill cannot be assumed present. Packaging a reference with every skill would duplicate it; putting terms only in a future orchestrator would leave direct calls uncovered. The orchestrator's overall design remains open in Q8, and detailed definitions of facts and expertise remain open in Q2–Q4.

## Decision

Provide a separate, optional Project Guide glossary skill. If it is installed, a future orchestrator must read it and internally check its main terms when starting or resuming project work. Direct phase skills remain usable without the glossary or orchestrator; missing glossary installation never blocks progress.

## Explanation

The first shared vocabulary covers issue (an unresolved question or blocker), proposal (a candidate answer, not yet accepted), decision (an explicitly accepted answer), task (reviewed actionable work linked to a decision), and trigger, gate, and transition for skill handoffs. Phase skills keep self-descriptive essential triggers and gates instead of relying on the glossary to run. The orchestrator's check is internal, not a user-facing recitation. This decision defines the vocabulary boundary and conditional preflight, not the unresolved orchestration design or the disputed rules for certifying facts and expertise.

## Consequences

- Add an installable glossary skill and keep phase skill wording consistent with its core terms.
- If an orchestrator is built, make its start/resume path consult an installed glossary before routing; leave direct calls operational without it.
- Preserve Q8's remaining orchestration choices and Q2–Q4's input and expertise questions.
