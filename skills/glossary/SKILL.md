---
name: glossary
description: Define Project Guide terminology. Use when a term needs clarification.
source: https://github.com/thinkforward-ai/project-guide
---

# Glossary

1. **Issue:** An identified, unresolved problem, unknown, contradiction, or
   choice that requires investigation or resolution.
2. **Task:** A specific, reviewed instruction for executable work with no
   unresolved design choices.
3. **Solution:** A way to resolve an issue, whether proposed or accepted.
4. **Proposal:** A candidate solution with supporting reasons and trade-offs.
5. **Decision:** An explicitly accepted choice of a solution for an issue.
6. **Trigger:** An event or condition that makes an activity, or a role's
   involvement, relevant.
7. **Gate:** A required condition or choice before an activity starts or ends.
   The mode sections say who passes a choice.
8. **Transition:** Movement from one activity to another after a gate.
9. **Collaboration mode:** How a project is worked on, stated in its
   overview: solo, team, or organization.
10. **Solo:** One person does the work and makes the decisions; no roles
    or decision attribution are used. The rule that only expertise owners
    decide is relaxed: the one person decides every issue, or, in
    AI-driven mode, the AI decides every issue that is not reserved. Any
    role perspective counts as opinion.
11. **Team:** Several contributors work on one project; roles apply and
    decisions record who accepted them. One person working with AI role
    holders is a team.
12. **Organization:** A group of teams; roles and decision rights are
    explicit and may span teams.
13. **Roadmap:** The journey toward the project's goal as milestones in
    intended order. It names no issues or tasks.
14. **Milestone:** A roadmap step with an intent, observable "done when"
    criteria, and a one-line progress log. In user-driven mode it is
    achieved when all criteria are met; in AI-driven mode it is then ready
    for a demo and achieved when the stakeholder confirms it. Adding,
    replacing, redefining, or cancelling one requires a decision.
15. **AI-driven:** The agent, possibly a team of AI roles, runs the
    lifecycle and makes every decision not reserved for the stakeholder,
    without phase gates. It records its decisions as `Decided by: AI
    (<role>, delegated)`, asks only about reserved decisions in batches, and
    confirms milestones with the stakeholder through demos. It stops and
    reports when a milestone is ready for a demo, when only reserved
    decisions remain, or when nothing applicable is left. The stakeholder
    may override any AI decision.
16. **User-driven:** The user passes every gate and makes every decision.
    The default.
17. **Reserved decision:** A decision that stays with the stakeholder in
    AI-driven mode: project direction and goal, milestone definitions and
    confirmation, scope changes, platform and technology, naming,
    irreversible or outward-facing actions, and anything the stakeholder
    reserves. The stakeholder decides them after the required expertise
    owners have given their verdicts.
18. **Framework part:** The mode-independent part of a skill: its purpose,
    records, rules, and steps with entry and exit gates. It says what
    happens and what must be true, not who decides.
19. **Mode section:** A skill's `User-driven mode` or `AI-driven mode`
    section. It describes how the agent behaves and who passes each gate,
    tuning the framework part without breaking its rules.
20. **Role:** A part in the project that represents one interest, with its
    expertise, triggers, red lines, and known bias. Any role can be held by
    a human or an AI; AI roles run as lenses within one session. A role
    acts only within its own project; in any other project it may only
    raise an issue, which counts there as opinion.
21. **Interest:** What a role protects or represents, such as scope and
    schedule for a project manager.
22. **Roster:** A project's roles, in the Roles subsection of the
    overview's Collaboration section. It may add roles or redefine
    catalogue roles; its definition wins. Roster changes are neither
    issues nor decisions: the user confirms them in user-driven mode, and
    the AI adds and reports them in AI-driven mode.
23. **Role catalogue:** Project Guide's starter roles in
    [roles-catalogue.md](roles-catalogue.md), copied into rosters as
    needed. Roles the catalogue lacks are defined in the roster from
    scratch with the same fields.
24. **Verdict:** A required expertise owner's one- or two-line judgement
    of a proposal: objection, condition, or no concern, flagged when it
    matches the role's known bias.
25. **Stakeholder:** The role held by the user. It owns requirements,
    preferences, acceptance, and reserved decisions, and is never played by
    the AI.
26. **Expert opinion:** Input from a holder of the expertise an issue
    requires. Only expertise owners decide such an issue.
27. **Opinion:** Input from anyone without the required expertise. It is
    recorded briefly and attributed, for the complete picture and to keep
    the think-tank space open, but does not bind the decision. Dissenting
    opinions are listed in the decision record.
28. **Guardian:** A role that protects a project's durable definition and
    its original goal and purpose. Its objection blocks a change until it
    is resolved or the stakeholder overrides it.

## Role visibility

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
