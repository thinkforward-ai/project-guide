# Overview

## 1. What It Is

A shared framework, not tied to any one tool, that takes a goal and works it into a fully resolved description that's ready to implement, optionally followed by domain-specific execution. It covers research, system design and work planning. Progress means steadily cutting down what is still unknown.

## 2. Scope

1. **Core (shared by every domain):** discovery, meaning research, design and planning. It covers starting a project, roles and expertise, open issues, refining meaning and requirements, handling input (classification, bias, contradictions), decisions, updating documents, and preparing tasks.
2. **Execution (optional, domain-specific):** some projects stay pure research (for example, science). Others move quickly into implementation (for example, agile IT projects).
3. **Domain packs:** what "implement" means differs by domain. In IT it means delivering tested code. In health care it can mean carrying out a patient's treatment, which is more physical and takes longer. Later, as the framework spreads, teams from each domain contribute their own skill sets for implementing tasks and decisions on top of the core.
4. **Out of scope for now:** designing execution skills. The core comes first. Recording that a task is complete is core document upkeep, not execution ([complete-task decision](decisions/20261019-2137-complete-task-skill.md)).

## 3. Who Takes Part

1. One or more contributors, each holding at least one role. The overview states the project's collaboration mode: solo (one person), team (several contributors), or organization (a group of teams). Solo projects use no roles and no decision attribution.
2. The overview also states the driving mode: user-driven (the user passes every gate and makes every decision) or AI-driven (the agent makes every decision not reserved for the stakeholder, without phase gates, and confirms milestones through demos). An absent field means user-driven. Each skill has a mode-independent framework part, followed by a user-driven and an AI-driven section that tune it ([AI-driven mode as delegation](decisions/20261115-1809-ai-driven-mode-as-delegation.md), superseding [AI-driven mode](decisions/20261004-1852-ai-driven-mode.md)).
3. Each role carries expertise areas, experience and background. Those decide whose input counts as expert on which topic.
4. Each role also carries known biases. For example, a PM may lean towards fast and cheap at the cost of quality or security. A backend engineer may lean towards over-engineering.
5. The framework is AI-inclusive: any contributor, role holder or expertise holder can be a human or an AI agent.
6. Each project keeps a roster of roles in the overview's Collaboration section, copied from a starter catalogue and adaptable. Each role states its interest, expertise, triggers, red lines, and known bias. Roles are tagged wherever their expertise is required, and only expertise owners decide such issues (relaxed in solo mode, where the one person decides); all other input is opinion, recorded for the complete picture. The stakeholder is the role held by the user and keeps the reserved decisions; AI roles run as lenses within one session. A role acts only within its own project; in other projects it may only raise an issue, which counts there as opinion ([role scope boundary](decisions/20261115-1929-role-scope-boundary.md)) ([project roles](decisions/20261115-1850-project-roles.md)).
7. **Role visibility:** Role-authored passages use bold bracket tags, and call-ins state their trigger. Coordinator is a shared catalogue role, explicitly rostered per project when needed; it protects process correctness and traceability, not domain decision authority. Coordination remains untagged when no Coordinator is rostered. Solo mode stays role-free ([visible role markers and Coordinator](decisions/20261115-2042-visible-role-markers-and-coordinator.md)).

## 4. Shared, Persistent Storage

1. All research state lives somewhere every contributor can reach: Git, Confluence or a wiki, Google Docs, and so on.
2. The framework's model is separate from the storage choice, so the same process can run on any of them.

## 5. Starting a Research Effort

1. Input: a stated idea or goal and any available input files. How those files are organized is still to be defined.
2. `start-project` creates the shared structure, preserves supplied input, records the idea without treating it as settled, and registers the first issue about the project's goal, collaboration mode, and driving mode, and a roadmap issue. Clarifying the goal and requirements belongs to refinement.

## 6. Breaking Problems Down, Layer by Layer

1. It starts with a few broad problems.
2. Each one splits into smaller problems, and each smaller problem is tagged with the expertise needed to resolve it.
3. Resolving issues reveals the next layer of issues. This is the "fog of war": the map is explored until everything needed for implementation is described, including risks and dependencies.

## 7. Lifecycle of an Issue

1. **Registered:** the initial project issue or a newly discovered issue is recorded. `raise-issue` registers later issues without analyzing them. After registration comes the choice to refine now or leave the issue open for later; the driving mode says who makes it.
2. **Refined:** `refine` clarifies meaning and requirements, examines inputs, and develops one or more reviewable proposals without choosing one. It may reveal smaller issues, which are registered separately. This loop can run across several issues at once.
3. **Decided:** when proposals and relevant blockers are ready, `decide` takes an explicit choice of one solution from whoever holds the decision (the required expertise owners, the stakeholder for reserved decisions, as the driving mode applies) and records it as an immutable decision. Without acceptance the issue remains open.
4. **Applied:** affected project understanding is updated. Actionable consequences become reviewed, decision-linked tasks under `tasks/` only when the [executable task handoff](decisions/20261003-1541-executable-task-handoff.md) is fully specified and unblocked. Consequences needing further design remain issues. Scheduling and execution are separate and may happen while unrelated issues remain open.
5. **Closed:** `complete-task` checks a finished task's acceptance criteria against evidence and, on confirmation (by the user, or by the AI in AI-driven mode), moves it to `tasks/closed/` with a Completion section and records roadmap progress. `tasks/` then holds only ready work ([complete-task decision](decisions/20261019-2137-complete-task-skill.md)).

The [lifecycle orchestrator decision](decisions/20261003-1603-project-lifecycle-orchestration.md) defines `work-on-project` as the entry point that reads project state, presents the complete pipeline and contextual next actions, and coordinates phase skills only through their triggers and gates. On opening or resuming any project, it proposes a project-specific translation to the current layout and obtains approval before changing existing material. On resumption, showing current status is an option, not an automatic report. Phase skills also work directly and use a consistent Trigger, Entry Gate, Work, Exit Gate, and Transition contract. The [shared vocabulary decision](decisions/20261003-1525-shared-vocabulary-and-orchestrator-preflight.md) calls for an optional glossary skill: when installed, the orchestrator checks its terms internally before routing, but its absence does not block progress.

1. The [skill update checks decision](decisions/20261019-0218-skill-update-checks-in-status.md) adds a read-only check of all skills used by the project when status is requested or chosen. Status lists available updates concisely by skill name, without delta details; details appear only on request or during review. Incomplete checks are disclosed without blocking status, and applying updates requires separate approval.
2. The [required milestone demos and confirmation decision](decisions/20261115-2330-required-milestone-demos-and-confirmation.md) makes criteria completion readiness for a demo in every mode, not achievement. A milestone is achieved only after an evidence-backed demo and explicit human stakeholder confirmation (the user in role-free solo mode). Run or directly show the outcome where possible; otherwise present HTML slides. Record demo evidence and confirmation in roadmap progress; without confirmation, do not advance the current milestone on that basis.

## 8. Handling Input During Research

Every piece of input that comes in is processed like this:

1. **Classified** as one of:
   1. Opinion: from someone without the required expertise.
   2. Expert opinion: from someone holding the expertise the problem needs.
   3. Fact: something objectively true.
2. **Checked for bias:** the contributor's likely bias, based on their role, is flagged and noted on the input.
3. **Validated** against what's already settled (facts and decisions) and compared with other inputs on the same topic.
4. **Checked for contradictions:** any contradiction found must always be surfaced. It then becomes a new issue that needs the relevant expertise.
5. **Kept for the record:**
   1. Non-expert opinions are never thrown away. They stay attached to the problem they're about, so there's a full history.
   2. They're considered by the expertise owners but not answered one by one; they don't bind the decision, and dissenting ones are listed in the decision record ([framework consistency](decisions/20261115-1921-framework-consistency-and-guardian.md)).

The detailed responsibility split for this processing is still an open question. The refinement skill classifies input as opinion or expert opinion by the roster's expertise, and does not certify facts.

## 9. Guarantees the Framework Aims For

1. Every decision can be traced back to the inputs, opinions and reasoning behind it.
2. Contradictions can't slip through silently.
3. Expertise is weighed explicitly, and bias is visible rather than hidden.
4. Research documents always reflect the latest settled knowledge.
5. A particular task can be ready while other issues remain open. Project-wide research is finished when no open issues block the intended implementation.

## 10. Collaboration

1. **Mode:** Unresolved ([Q15](open-issues.md#q15-open-source-collaboration-mode)).
2. **Driving:** AI-driven ([project-level mode decision](decisions/20261115-2146-project-guide-ai-driven-mode.md)).

### Roles

Provisional while Q15 is open ([framework consistency and guardian](decisions/20261115-1921-framework-consistency-and-guardian.md)).

1. **Stakeholder:** the founder. Owns the framework's goal, requirements, and reserved decisions.
2. **Framework guardian** (AI): the Guardian from the [catalogue](skills/glossary/roles-catalogue.md), applied to Project Guide. Its expertise is required on every issue that changes skills, the glossary, the overview, the layout, or decisions. It checks that a change stays consistent with accepted decisions and serves the framework's original goal and purpose, and its objection blocks the change until it is resolved or the stakeholder overrides it.
3. **Coordinator** (AI), from the [catalogue](skills/glossary/roles-catalogue.md):
   1. **Interest:** correct, traceable workflow.
   2. **Expertise:** lifecycle, records, gates, readiness, and handoffs.
   3. **Triggers:** resuming work, phase transitions, readiness checks, and record inconsistencies.
   4. **Red lines:** invented approvals or evidence, skipped required gates, cross-project action, or overriding expertise owners and stakeholder decisions.
   5. **Known bias:** process and checking at the expense of progress.
4. **Framework designer** (AI), adapted from Domain designer in the [catalogue](skills/glossary/roles-catalogue.md):
   1. **Interest:** a useful, coherent, tool-independent framework.
   2. **Expertise:** research workflows, artifact contracts, role interactions, and skill-process design.
   3. **Triggers:** proposed changes to lifecycle rules, concepts, skills, or document structure.
   4. **Red lines:** contradicting accepted decisions, making the core tool-specific, or treating unresolved design as executable work.
   5. **Known bias:** elegant abstractions and richer systems at the expense of simplicity.
   6. **Boundary with Framework guardian and Stakeholder:** develops improvements; the guardian checks whether they fit. The designer cannot override the guardian or change stakeholder-reserved direction and scope.

## 11. Still Open

Unresolved issues are tracked in [open-issues.md](open-issues.md).
