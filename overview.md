# Overview

## 1. What It Is

A shared framework, not tied to any one tool, that takes a goal and works it into a fully resolved description that's ready to implement, optionally followed by domain-specific execution. It covers research, system design and work planning. Progress means steadily cutting down what is still unknown.

## 2. Scope

1. **Core (shared by every domain):** discovery, meaning research, design and planning. It covers starting a project, roles and expertise, open issues, refining meaning and requirements, handling input (classification, bias, contradictions), decisions, updating documents, and preparing tasks.
2. **Execution (optional, domain-specific):** some projects stay pure research (for example, science). Others move quickly into implementation (for example, agile IT projects).
3. **Domain packs:** what "implement" means differs by domain. In IT it means delivering tested code. In health care it can mean carrying out a patient's treatment, which is more physical and takes longer. Later, as the framework spreads, teams from each domain contribute their own skill sets for implementing tasks and decisions on top of the core.
4. **Out of scope for now:** designing execution skills. The core comes first.

## 3. Who Takes Part

1. One or more contributors, each holding at least one role. The overview states the project's collaboration mode: solo (one person), team (several contributors), or organization (a group of teams). Solo projects use no roles and no decision attribution.
2. Each role carries expertise areas, experience and background. Those decide whose input counts as expert on which topic.
3. Each role also carries known biases. For example, a PM may lean towards fast and cheap at the cost of quality or security. A backend engineer may lean towards over-engineering.
4. The framework is AI-inclusive: any contributor, role holder or expertise holder can be a human or an AI agent.

## 4. Shared, Persistent Storage

1. All research state lives somewhere every contributor can reach: Git, Confluence or a wiki, Google Docs, and so on.
2. The framework's model is separate from the storage choice, so the same process can run on any of them.

## 5. Starting a Research Effort

1. Input: a stated idea or goal and any available input files. How those files are organized is still to be defined.
2. `start-project` creates the shared structure, preserves supplied input, records the idea without treating it as settled, and registers the first issue about the project's goal and collaboration mode, and a roadmap issue. Clarifying the goal and requirements belongs to refinement.

## 6. Breaking Problems Down, Layer by Layer

1. It starts with a few broad problems.
2. Each one splits into smaller problems, and each smaller problem is tagged with the expertise needed to resolve it.
3. Resolving issues reveals the next layer of issues. This is the "fog of war": the map is explored until everything needed for implementation is described, including risks and dependencies.

## 7. Lifecycle of an Issue

1. **Registered:** the initial project issue or a newly discovered issue is recorded. `raise-issue` registers later issues without analyzing them. After registration, the user chooses whether to refine now or leave the issue open for later.
2. **Refined:** `refine` clarifies meaning and requirements, examines inputs, and develops one or more reviewable proposals without choosing one. It may reveal smaller issues, which are registered separately. This loop can run across several issues at once.
3. **Decided:** when proposals and relevant blockers are ready, `decide` asks for explicit acceptance of one solution and records it as an immutable decision. Without acceptance the issue remains open.
4. **Applied:** affected project understanding is updated. Actionable consequences become reviewed, decision-linked tasks under `tasks/` only when the [executable task handoff](decisions/20261003-1541-executable-task-handoff.md) is fully specified and unblocked. Consequences needing further design remain issues. Scheduling and execution are separate and may happen while unrelated issues remain open.

The [lifecycle orchestrator decision](decisions/20261003-1603-project-lifecycle-orchestration.md) defines `work-on-project` as the entry point that reads project state, presents the complete pipeline and contextual next actions, and coordinates phase skills only through their triggers and gates. On opening or resuming any project, it proposes a project-specific translation to the current layout and obtains approval before changing existing material. On resumption, showing current status is an option, not an automatic report. Phase skills also work directly and use a consistent Trigger, Entry Gate, Work, Exit Gate, and Transition contract. The [shared vocabulary decision](decisions/20261003-1525-shared-vocabulary-and-orchestrator-preflight.md) calls for an optional glossary skill: when installed, the orchestrator checks its terms internally before routing, but its absence does not block progress.

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
   2. They're also input for the expert, who must explicitly accept or reject each one and give the reason.

The detailed responsibility split for this processing is still an open question; the refinement skill does not certify facts or infer expertise.

## 9. Guarantees the Framework Aims For

1. Every decision can be traced back to the inputs, opinions and reasoning behind it.
2. Contradictions can't slip through silently.
3. Expertise is weighed explicitly, and bias is visible rather than hidden.
4. Research documents always reflect the latest settled knowledge.
5. A particular task can be ready while other issues remain open. Project-wide research is finished when no open issues block the intended implementation.

## 10. Still Open

Unresolved issues are tracked in [open-issues.md](open-issues.md).
