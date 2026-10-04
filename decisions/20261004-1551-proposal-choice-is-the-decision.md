# Proposal choice is the decision

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-10-04

## Problem Description

This decision replaces the gate rules in `20261003-1603-project-lifecycle-orchestration.md`, which said proposal review offers **Review proposals / Continue refinement / Pause** and does not accept an answer, and a later decision offers **Approve / Revise / Pause**. In use, the user reviewed and chose a proposal, then saw the same proposals again and had to approve the same choice a second time. Choosing a proposal is already an explicit acceptance.

## Decision

Listing proposals belongs to the decision phase and is always followed by the gate **choose a proposal / continue refining / pause**. Choosing a proposal, or approving a sole proposal, is the decision. Refinement keeps discussion free of gates until proposals are ready to be listed.

## Explanation

- After a choice, the decision phase validates it against known facts, accepted decisions, the overview, and open issues; every conflict is resolved explicitly before recording. If a resolution changes the chosen proposal, the user confirms the change.
- Resolution points settled by the chosen proposal are marked resolved; only points it leaves open are asked about.
- After recording, the user sees the record's path and a short summary instead of approving the wording beforehand.
- All other rules of the replaced decision stay in force: the orchestrator coordinates phase skills through triggers and gates, does not choose or approve itself, and adds no stage field.

## Consequences

- `refine` hands ready proposals to `decide` instead of running its own review gate.
- `decide` lists proposals with the gate and records the chosen one; the separate Approve / Revise / Pause gate is removed.
- `work-on-project` routes proposals ready for a choice to the decision phase.
- The earlier decision stays unchanged as history.
