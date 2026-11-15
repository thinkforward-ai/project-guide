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
6. **Trigger:** An event or condition that makes an activity relevant.
7. **Gate:** A required condition or choice before an activity starts or ends.
   The mode sections say who passes a choice.
8. **Transition:** Movement from one activity to another after a gate.
9. **Collaboration mode:** How a project is worked on, stated in its
   overview: solo, team, or organization.
10. **Solo:** One person does the work and makes the decisions; no roles
    or decision attribution are used.
11. **Team:** Several contributors work on one project; roles apply and
    decisions record who accepted them.
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
    (delegated)`, asks only about reserved decisions in batches, and
    confirms milestones with the stakeholder through demos. The
    stakeholder may override any AI decision.
16. **User-driven:** The user passes every gate and makes every decision.
    The default.
17. **Reserved decision:** A decision that stays with the stakeholder in
    AI-driven mode: project direction and goal, milestone definitions and
    confirmation, scope changes, platform and technology, naming,
    irreversible or outward-facing actions, and anything the stakeholder
    reserves.
18. **Framework part:** The mode-independent part of a skill: its purpose,
    records, rules, and steps with entry and exit gates. It says what
    happens and what must be true, not who decides.
19. **Mode section:** A skill's `User-driven mode` or `AI-driven mode`
    section. It describes how the agent behaves and who passes each gate,
    tuning the framework part without breaking its rules.
