# Integrate project roles into the framework and skills

**Decision:** [Project roles](../decisions/20261115-1850-project-roles.md)

## What

Project Guide ships a starter role catalogue. Its skills, glossary, and overview use per-project rosters, trigger-based role involvement, and verdicts.

## Why

This implements the decision linked above, which settles Q2.

## How

1. Add `skills/glossary/roles-catalogue.md` with the six starter roles, each with interest, expertise, triggers, red lines, and known bias.
2. `start-project`: in team or organization mode, propose roles to add from the catalogue, defining missing roles from scratch. `raise-issue` and `refine` do the same when an issue needs expertise that no role has.
3. `raise-issue`: add an optional `### Expertise` section to the issue format, listing the roles whose expertise is required.
4. `refine`: expertise owners give verdicts, and all other input is recorded as opinion. Add a `Verdicts` line to the Proposal Format. Conflict handling goes in both mode sections.
5. `decide`: only expertise owners decide; record their objections and conditions. Conflict handling goes in both mode sections.
6. `complete-task`: expertise owners check the criteria in their area.
7. `work-on-project`: read the roster.
8. Glossary: extend Trigger and Team, and add Role, Interest, Roster, Role catalogue, Verdict, Stakeholder, Expert opinion, and Opinion.
9. `overview.md`: describe the role model. Remove Q2 from `open-issues.md`.

## Acceptance Criteria

1. The catalogue exists and the glossary links it.
2. Each listed skill contains the role behaviour above, within the framework part and mode-section structure.
3. Q2 is no longer in `open-issues.md`, and `overview.md` links the decision.

## Prerequisites

None.

## Dependencies

[Project roles](../decisions/20261115-1850-project-roles.md), accepted.

## Execution note

Executed on 2026-11-15 in the working tree, right after the decision. Nothing is committed. Closing the task through `complete-task` awaits the user's confirmation.
