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
