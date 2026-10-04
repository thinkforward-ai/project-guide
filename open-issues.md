# Open Issues

This file contains only unresolved issues that currently require investigation or a decision.

**Next question ID:** Q13

## Q1: Input file organization

### Question

How should the input files that feed a new research effort be organized?

### Why It Matters

Initialization sources the goal and requirements from input files, so it can't be designed until their layout is known.

### Context

`overview.md` section 5: input is a goal plus input files with requirements.

### Resolution Points

- ❓ **Layout**
  - **Resolution:** Pending
  - **Details:** Structure, naming, and required versus optional files.

## Q2: Roles, expertise and bias definitions

### Question

How are roles, their expertise and their known biases defined: a fixed catalogue, set per project, or both?

### Why It Matters

Expertise decides whether input counts as opinion or expert opinion, and who can decide an issue. Bias definitions drive bias tagging.

### Context

`overview.md` sections 3 and 8. Solo collaboration mode uses no roles (founder input, 2026-10-04; `overview.md` section 3 and the glossary). Example biases: a PM leans towards fast and cheap at the cost of quality or security, and a backend engineer leans towards over-engineering.

### Resolution Points

- ❓ **Source of definitions**
  - **Resolution:** Pending
  - **Details:** A fixed catalogue, per-project definitions, or a shared catalogue with project overrides.
- ❓ **Role-to-question matching**
  - **Resolution:** Pending
  - **Details:** How an issue's required expertise is matched to contributors' roles.
- ❓ **Stakeholder role**
  - **Resolution:** Pending
  - **Details:** How the user as stakeholder (requirements, preferences, acceptance) differs from contributors, including AI roles in an AI-driven project (Q12).

## Q3: Who performs input processing

### Question

Who or what classifies input and detects bias and contradictions: an agent, a human, or both?

### Why It Matters

This decides how reliable and how automated the "under research" stage is, and who is accountable for its results.

### Context

`overview.md` section 8: every input is classified, checked for bias, validated against settled knowledge, and checked for contradictions.

### Resolution Points

- ❓ **Responsibility split**
  - **Resolution:** Pending
  - **Details:** What an agent does, what a human confirms, and how disagreements are handled.

## Q4: Establishing facts

### Question

How is a fact established, who certifies it, and can a later decision overturn it?

### Why It Matters

Input is validated against settled facts and decisions, so an unclear notion of "fact" weakens contradiction checks.

### Context

`overview.md` section 8: a fact is something objectively true.

### Resolution Points

- ❓ **Certification**
  - **Resolution:** Pending
  - **Details:** Who or what confirms that an input is a fact.
- ❓ **Revision**
  - **Resolution:** Pending
  - **Details:** How a fact is challenged or overturned, and how this relates to decision records.

## Q5: Storage layer abstraction

### Question

How is the storage layer abstracted so the framework works on Git, a wiki, Google Docs and similar shared stores?

### Why It Matters

Contributors work remotely and need shared, persistent access, and the framework should not be tied to one tool.

### Context

`overview.md` section 4.

### Resolution Points

- ❓ **Abstraction model**
  - **Resolution:** Pending
  - **Details:** What the framework requires from a store, and how each store is supported.

## Q6: Measuring progress and completion

### Question

How are progress through the fog of war and the completion of research measured or shown?

### Why It Matters

Teams need to see what is still unknown and when research is ready for implementation.

### Context

`overview.md` sections 6 and 9: research is finished when no open issues block implementation.

### Resolution Points

- ❓ **Progress view**
  - **Resolution:** Pending
  - **Details:** How explored versus unexplored areas are shown.
- ❓ **Completion criteria**
  - **Resolution:** Pending
  - **Details:** How an issue is judged as blocking implementation or not.

## Q7: Project name and skill prefix

### Question

Is `project-guide` the final project name, and what prefix should skills use?

### Why It Matters

Skill names and domain-pack naming depend on the prefix.

### Context

The repository is `thinkforward-ai/project-guide`. Working candidate prefix: `pg-` (for example `pg-init`, `pg-question`, `pg-decide`; domain packs as `pg-it-*`, `pg-health-*`).

### Resolution Points

- ❓ **Skill prefix**
  - **Resolution:** Pending
  - **Details:** `pg-` or an alternative, including domain-pack naming.

## Q12: AI-driven mode

### Question

How should a project choose between AI-driven and user-driven work, and how do skills behave in each mode?

### Why It Matters

Today the user drives every transition and AI only keeps records and offers neutral choices. The founder wants an AI-centric option where AI, possibly a team of AI roles (CEO, PM, Architect, Developer), runs the process and consults the user as a stakeholder for requirements and preferences.

### Context

AI-centric (business-lab glossary): AI drives the work and treats the user as its customer; it asks for everything in the user's interest, including how to do the work, always with a recommendation; the user sets the goal, supplies information, and accepts decisions. The founder expects the lifecycle (issue → research → proposals → decision → implementation), records, and tasks to stay unchanged; only who drives changes. Related: Q2 (roles; the stakeholder role is defined there), the collaboration mode pattern, and the ask-or-decide boundary open as Q14 in `thinkforward-ai/business-lab`.

### Resolution Points

- ❓ **Mode field and values**
  - **Resolution:** Pending
  - **Details:** Where the mode is stated and which values it takes.
- ❓ **Mode selection**
  - **Resolution:** Pending
  - **Details:** When it is asked, the default for existing projects, and how it changes later.
- ❓ **Skill mechanics**
  - **Resolution:** Pending
  - **Details:** How each skill describes its AI-driven behavior.
- ❓ **Gate ownership**
  - **Resolution:** Pending
  - **Details:** Which gates the AI team passes and which go to the stakeholder.

### Findings

- Lifecycle, records, and gates stay; only who drives changes (founder).
- The collaboration mode is the existing pattern: stated in the overview, asked at start, changed only by a decision.
- No accepted decision conflicts: the resume menu (`decisions/20261003-1603-project-lifecycle-orchestration.md`) and "a choice is the decision" (`decisions/20261004-1551-proposal-choice-is-the-decision.md`) both remain.
- Interim gate split until the ask-or-decide boundary is clear (founder confirmed, 2026-10-04): the AI team passes transition gates (refine now or later, next action, continue refining); decisions and anything in the user's interest, including how to do the work, go to the stakeholder with a recommendation.

### Proposals

**Problem:** Let a project run AI-driven, with AI driving the lifecycle and the user consulted as stakeholder, without changing the workflow or records.

1. **Driving field with per-skill sections:** State `**Driving:** AI-driven | user-driven` in the overview's Collaboration section; absent means user-driven. `start-project` asks it with the collaboration mode; changing it needs a decision. Each phase skill gains an `## AI-driven mode` section with only its differences under the interim gate split. The glossary adds AI-driven and user-driven.
   - **Pros:** Follows the collaboration-mode pattern; each skill stays correct when called directly; existing projects are unaffected; a named field allows a hybrid later.
   - **Cons:** Similar text in six skills can drift; the gate split is interim until the boundary is settled.
2. **Boolean flag with a project-level rule:** State `ai-driven: true|false` in the project's `AGENTS.md`; `start-project` asks it and, when true, writes one AI-driven section there. Skills stay unchanged.
   - **Pros:** No skill edits; one rule per project.
   - **Cons:** Skills do not know the mode, so behavior depends on each project's copy; copies drift across projects; a boolean leaves no room for a hybrid.
