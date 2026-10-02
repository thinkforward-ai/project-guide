# Problem Description

## 1. What It Is

A shared framework, not tied to any one tool, that takes a goal and works it into a fully resolved description that's ready to implement, optionally followed by domain-specific execution. It covers research, system design and work planning. Progress means steadily cutting down what is still unknown.

## 2. Scope

1. **Core (shared by every domain):** discovery, meaning research, design and planning. It covers starting a project, roles and expertise, open questions, handling input (classification, bias, contradictions), decisions, and updating documents.
2. **Execution (optional, domain-specific):** some projects stay pure research (for example, science). Others move quickly into implementation (for example, agile IT projects).
3. **Domain packs:** what "implement" means differs by domain. In IT it means delivering tested code. In health care it can mean carrying out a patient's treatment, which is more physical and takes longer. Later, as the framework spreads, teams from each domain contribute their own skill sets for implementing tasks and decisions on top of the core.
4. **Out of scope for now:** designing execution skills. The core comes first.

## 3. Who Takes Part

1. Several contributors, each holding at least one role.
2. Each role carries expertise areas, experience and background. Those decide whose input counts as expert on which topic.
3. Each role also carries known biases. For example, a PM may lean towards fast and cheap at the cost of quality or security. A backend engineer may lean towards over-engineering.
4. The framework is AI-inclusive: any contributor, role holder or expertise holder can be a human or an AI agent.

## 4. Shared, Persistent Storage

1. All research state lives somewhere every contributor can reach: Git, Confluence or a wiki, Google Docs, and so on.
2. The framework's model is separate from the storage choice, so the same process can run on any of them.

## 5. Starting a Research Effort

1. Input: a goal plus input files with requirements. How those files are organized is still to be defined.
2. Output: the research structure. That means a project description, the goal definition, constraints, and the first blockers and open questions.

## 6. Breaking Problems Down, Layer by Layer

1. It starts with a few broad problems.
2. Each one splits into smaller problems, and each smaller problem is tagged with the expertise needed to resolve it.
3. Resolving problems reveals the next layer of questions. This is the "fog of war": the map is explored until everything needed for implementation is described, including risks and dependencies.

## 7. Lifecycle of a Question

1. **Registered:** a problem, question or blocker is recorded. Today's `open-question` skill does this.
2. **Under research:** an important stage that is mostly missing today. It means gathering information, thinking, and contributors exchanging opinions.
3. **Decided:** an expert resolves it with reasons, and it becomes a decision record. Today's `make-decision` skill does this.
4. **Applied:** after the decision, every affected research document is updated to show current understanding and status.

## 8. Handling Input During Research

Every piece of input that comes in is processed like this:

1. **Classified** as one of:
   1. Opinion: from someone without the required expertise.
   2. Expert opinion: from someone holding the expertise the problem needs.
   3. Fact: something objectively true.
2. **Checked for bias:** the contributor's likely bias, based on their role, is flagged and noted on the input.
3. **Validated** against what's already settled (facts and decisions) and compared with other inputs on the same topic.
4. **Checked for contradictions:** any contradiction found must always be surfaced. It then becomes a new blocker or open question that needs the relevant expertise.
5. **Kept for the record:**
   1. Non-expert opinions are never thrown away. They stay attached to the problem they're about, so there's a full history.
   2. They're also input for the expert, who must explicitly accept or reject each one and give the reason.

## 9. Guarantees the Framework Aims For

1. Every decision can be traced back to the inputs, opinions and reasoning behind it.
2. Contradictions can't slip through silently.
3. Expertise is weighed explicitly, and bias is visible rather than hidden.
4. Research documents always reflect the latest settled knowledge.
5. Research is finished when there are no open questions left that block implementation.

## 10. Still Open

Unresolved points are tracked in [open-questions.md](open-questions.md).
