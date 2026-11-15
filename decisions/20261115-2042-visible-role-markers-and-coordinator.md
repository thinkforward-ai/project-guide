# Visible role markers and an explicitly rostered Coordinator

**Accepted by:** Maxim Nikitin (stakeholder)
**Date:** 2026-11-15

## Problem Description

Q25 asked how a session should show which role is acting or has been called in. A project roster names who can participate, but does not show who actually decided, advised, or implemented during the session.

1. The issue originated in ninetiles, raised by its Project manager role. Its stakeholder wanted very clear indication when a role was involved or called in, after five AI roles were visible only in a retrospective summary. Under the [role scope boundary](20261115-1929-role-scope-boundary.md), this was opinion in Project Guide, not authority over its process.
2. One proposal was refined: bold bracket tags for acting roles and separate call-in announcements. Its original Coordinator label for work outside any role was replaced, at the Project Guide founder's request, by a shared catalogue role explicitly included in each project's roster.
3. Required expertise: the framework guardian for consistency with the framework and accepted decisions, and the stakeholder for presentation requirements and acceptance.
4. Framework guardian verdict: conditional on retaining the five authority and scope boundaries below, explicit per-project rostering, and the distinction from Project manager. The accepted proposal incorporates these conditions; no unresolved objection remains. No dissenting opinions were recorded.
5. The choice was checked against the [project roles](20261115-1850-project-roles.md), [framework consistency](20261115-1921-framework-consistency-and-guardian.md), and [role scope boundary](20261115-1929-role-scope-boundary.md) decisions. Their roster, authority, stakeholder, and solo-mode rules remain unchanged.

## Decision

1. **Display convention:**
   1. Each passage written while a role acts starts with its bold bracket tag, for example `**[Framework guardian]** Condition: ...`.
   2. A call-in appears on its own line: `↳ **[Framework guardian]** called in: <trigger>`.
   3. Project Guide supplies Coordinator in the starter role catalogue. Projects explicitly add it to their rosters when needed.
   4. Coordination uses `**[Coordinator]**` only when that role is rostered and acting. Otherwise coordination continues without a role tag or an implied assignment.
   5. Define the display convention once in the glossary and Coordinator once in `skills/glossary/roles-catalogue.md`. Skills involving roles reference these definitions rather than duplicate them.
2. **Boundaries:**
   1. Role names come from the current project's roster. Do not invent roles or use another project's roles.
   2. Coordinator is project-scoped, not globally empowered or automatically included. Roster additions follow the existing mode-specific confirmation rules. This decision does not itself add Coordinator to Project Guide's roster.
   3. A call-in means actually applying the role's perspective and stating its trigger, not merely displaying a name. It does not imply a separate agent session.
   4. The AI never speaks as the stakeholder. Attribute stakeholder input to its actual source. Solo mode still uses no roles, so these markers do not apply there.
   5. Tags grant no authority. Wording such as "decides", "advises", and "implements" reflects what actually happened under the project's existing rules.
3. **Coordinator definition:**
   1. **Interest:** a coherent, traceable project workflow whose records faithfully reflect the work and choices made.
   2. **Expertise:** Project Guide's lifecycle, artifacts, gates, phase readiness, and handoffs. It may assess process readiness but gains no domain decision authority.
   3. **Triggers:** opening or resuming a project, phase handoffs, readiness checks, and process or record inconsistencies.
   4. **Red lines:** skipping required phases or gates, inventing acceptance or evidence, acting outside its project, or overriding expertise owners or stakeholder-reserved decisions.
   5. **Known bias:** procedural overhead and excessive checking at the expense of progress.
   6. **Boundary with Project manager:** Coordinator protects process correctness and traceability. Project manager protects scope, priorities, risk, and delivery. Neither takes over the other's expertise merely by coordinating.

## Explanation

1. This settles all three Q25 resolution points: marker format, definition placement, and Coordinator's responsibilities and scope.
2. Shared role definitions do not create shared authority across projects. A Coordinator acts only in the project whose roster includes it, under that project's rules.
3. The convention makes role involvement and process responsibility visible without adding a gate or requiring separate agent sessions.
4. The trade-offs are extra characters in role-authored passages, a role definition to maintain, and explicit roster selection before using the Coordinator tag. Tags alone cannot prove genuine role thinking or enforce authority.
5. This does not settle Q26's record-timing question or Q27's execution-skill question. Existing phase and execution boundaries remain in force.

## Consequences

1. Remove resolved Q25 from `open-issues.md` without reusing its ID, and link this decision from `overview.md`.
2. Prepare a reviewed, decision-linked implementation task to add the glossary convention, Coordinator catalogue entry, and references from the six lifecycle skills.
3. Do not add Coordinator automatically to any roster or change Project Guide's current roster.
4. Implementing the convention, creating the reviewed task, updating installed skills, and sharing outside the local workspace retain their separate authorization requirements. Approval of this decision does not authorize execution, installation, or pushing.
