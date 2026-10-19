# Open Issues

This file contains only unresolved issues that currently require investigation or a decision.

**Next question ID:** Q21

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
  - **Details:** How the user as stakeholder (requirements, preferences, acceptance) differs from contributors, including AI roles in an AI-driven project (`decisions/20261004-1852-ai-driven-mode.md`).

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

## Q5: Integrations configuration

### Question

How does a project declare which integrations it uses and for what, so agents and skills work through Git, a wiki, Google Docs or any other service without being tied to one?

### Why It Matters

Contributors work remotely and need shared, persistent access, and the framework should not be tied to one tool. Sharing updates (Q16), connectors and views (Q17), and storage all depend on knowing which service serves which purpose.

### Context

`overview.md` section 4. Founder input (2026-10-11): integrations should be extracted and defined per project as configuration, covering every kind of integration; agents consult it to decide whether to go to Git, a wiki, or another service; a skill may help set them up. Storage becomes one integration purpose among others.

### Resolution Points

- ❓ **Abstraction model**
  - **Resolution:** Pending
  - **Details:** What the framework requires from each integration purpose (storage first), and how each service is supported.
- ❓ **Configuration**
  - **Resolution:** Pending
  - **Details:** Where it lives in the project layout, its format, and which purposes it covers.
- ❓ **Setup skill**
  - **Resolution:** Pending
  - **Details:** Whether a skill sets up integrations, and its scope.

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

## Q13: Project roadmap

### Question

What milestones lead Project Guide to its goal?

### Why It Matters

Without milestones, progress has no current focus and decisions and tasks cannot be tracked against a goal.

### Context

`roadmap.md` was missing when the project was aligned with the current layout (2026-10-10). It now has no milestones and refers to this issue. The collaboration mode moved to Q15 (2026-10-11); its outcome may change milestone order.

### Resolution Points

- ❓ **Milestones**
  - **Resolution:** Pending
  - **Details:** Names, intents, done-when criteria, and order, drawn from `overview.md` and the accepted decisions.

### Findings

1. The lifecycle skills (`start-project`, `raise-issue`, `refine`, `decide`, `work-on-project`, `glossary`) and AI-driven mode already exist, backed by six decisions from 2026-10-03 to 2026-10-04.
2. The remaining gaps cluster into three groups. A single person running a project end to end needs Q1 (input files), Q6 (progress and completion), Q7 (skill prefix) and Q14 (completed tasks). Teams need Q2 (roles), Q3 (input processing) and Q4 (facts). Tool independence needs Q5 (storage).
3. `overview.md` section 2 puts execution skills and domain packs out of scope for now.
4. Founder input (2026-10-11): the collaboration is open source (see Q15). Outside contributors could arrive at any time, which may make team readiness more urgent.
5. Founder ideas (2026-10-11) for sharing updates (Q16), integrations (Q5), a non-terminal interface (Q17), CI (Q18) and a contributing guide (Q19) point to a possible "Open for contributors" milestone. Revisit the proposals before deciding.
6. The glossary defines a roadmap as naming no issues or tasks (`skills/glossary/SKILL.md`, item 13). Proposals here may cross-reference issues, but the milestones written into `roadmap.md` must state done-when criteria without issue IDs (founder clarification, 2026-10-11).
7. Q14 was resolved on 2026-10-19 by the [complete-task decision](decisions/20261019-2137-complete-task-skill.md); its implementation remains to be done.

### Proposals

**Problem:** Project Guide has no milestones, so progress has no current focus and decisions and tasks can't be tracked against the goal in `overview.md`.

1. **Capability layers:** Four milestones, each one widening who can use the framework.
   1. M1 Core lifecycle (achieved): issues move from registration through refinement and decision to tasks, through gated skills, in either driving mode.
   2. M2 Solo-ready: one person can run a project end to end, including input files, roadmap progress, completion and task closure (Q1, Q6, Q7, Q14).
   3. M3 Team-ready: roles, expertise, bias, input processing and facts work for several contributors (Q2, Q3, Q4).
   4. M4 Tool-independent: the process runs on at least one store besides Git (Q5).
   - **Pros:** It matches the existing issue clusters, so every open issue maps to a milestone. Each milestone gives a usable result, and M2 makes the next focus small and concrete. It keeps domain packs out, as `overview.md` section 2 says.
   - **Cons:** M1 is recorded after the fact. M3 is large, and Q2 to Q4 depend on one another. Execution and domain packs get no milestone, so they need a later decision to change the roadmap.
2. **Single core milestone:** One milestone, "Core framework complete", done when Q1 to Q7 and Q14 are resolved and the skills reflect the decisions.
   - **Pros:** It's the simplest to keep current, with no ordering debates.
   - **Cons:** There's no intermediate usable result. The current focus stays the same for the whole project, so roadmap progress shows little, and it duplicates `open-issues.md`.
3. **Dogfood then external:** M1 Self-hosted, where Project Guide runs its own development with all solo gaps closed (Q1, Q6, Q7, Q14). M2 First external project, where one real project outside this repository runs from `start-project` to ready tasks, and the gaps it reveals are raised. Team and storage issues (Q2 to Q5) stay unassigned until evidence places them.
   - **Pros:** Milestones come from real use, not from a design guess. It surfaces gaps the open issues don't yet cover.
   - **Cons:** It depends on finding a suitable external project. Q2 to Q5 have no milestone, so the roadmap doesn't show team or storage readiness.

## Q15: Open-source collaboration mode

### Question

How does the framework support open-source collaboration, and how does Project Guide apply it to itself?

### Why It Matters

Project Guide is open source (founder input, 2026-10-11), but the framework defines only solo, team and organization modes. The mode decides whether roles apply, who accepts decisions, and whether decisions name who accepted them.

### Context

`overview.md` section 3 defines the three modes; solo uses no roles and no decision attribution. Every accepted decision so far names an accepter ("Maxim Nikitin (project manager)"). Split from Q13 (roadmap); its outcome may change milestone order there. Related to Q2 (roles and stakeholder role).

### Resolution Points

- ❓ **Mode model**
  - **Resolution:** Pending
  - **Details:** A fourth mode, or a team or organization project with open membership.
- ❓ **Decision authority**
  - **Resolution:** Pending
  - **Details:** Who accepts decisions when contributors are unknown, for example maintainers or expertise holders, and whether decisions carry attribution.
- ❓ **Outside input**
  - **Resolution:** Pending
  - **Details:** How outside contributions, such as pull requests or issue comments, enter the process.
- ❓ **Project Guide's own mode**
  - **Resolution:** Pending
  - **Details:** What `overview.md` section 10 records for this project.

### Findings

1. The repository is licensed under Apache 2.0 and hosted at `github.com/thinkforward-ai/project-guide`.
2. The glossary (`skills/glossary/SKILL.md`, items 9 to 12) and `decide` tie roles and attribution to the mode. Solo uses neither. Team uses roles and records who accepted each decision. Organization makes roles and decision rights explicit across teams.
3. The current modes describe how many people take part, not who may join or who decides. Open source raises both questions: membership is open, and decision authority has to be named because contributors are unknown.
4. So far every decision was accepted by the founder ("Maxim Nikitin (project manager)").
5. Common to every option: outside input arrives through the shared store (for Git, pull requests and issues; Q16), is processed as input under `overview.md` section 8, and may lead to new issues. How contributors' roles and expertise are defined stays with Q2.
6. Founder input (2026-10-11): for now only the founder accepts decisions on Project Guide; more maintainers may be added later by a decision.
7. Founder input (2026-10-11) separates two ways of controlling changes:
   1. **Platform protection:** merge requests and branch protection. Specific to a platform, unaware of roles, and a merged request can rewrite anything.
   2. **Internal role model:** roles and expertise inside the project; the framework's skills tell each contributor what they may and may not do, and a contributor can still override it. This model assumes direct commits to the default branch: Git is used to track and share changes, not to protect them.
   An earlier input the same day proposed protecting the default branch with merge requests only; findings 8 and 9 replace it: members commit directly, and merge requests apply only to non-members. The internal role model depends on Q2 (roles and expertise).
8. Founder input (2026-10-11): letting anyone merge into the default branch doesn't scale safely. Instead, the public gets read-only access to the repository, skills included, at any time. Only accepted members contribute; on acceptance a member is given roles and expertise, and members commit directly to the default branch. This removes the need for branch protection.
9. Founder input (2026-10-11): non-members may contribute through merge requests only, and only a limited circle may approve and merge them; members keep direct access to the default branch.
10. Founder input (2026-10-11): only the project owner (the founder) adds or removes members.
11. Decision provenance (founder input and discussion, 2026-10-11): a decision file is plain text, so its accepter line is not enforced by a merge request or by Git. Plain Git only hints at whether a commit came from a merge request; the platform's API knows reliably. On github.com, server-side Git hooks are unavailable and client-side hooks can be skipped, but a post-merge pipeline runs on every change to the default branch and knows the authenticated pusher, merge-request author, merger and approvers. The founder accepts a one-time provenance stamp by the platform as an exception to decision immutability, and wants decisions to carry two fields: "Made by" and "Approved by".

### Proposals

**Problem:** The framework has no collaboration mode for open-source projects, where anyone may contribute but someone must still accept decisions. Project Guide itself needs a mode recorded in `overview.md` section 10.

1. **Open membership as a separate setting:** Keep the three modes for structure, and add a `**Membership:** open | closed` field to the Collaboration section (absent means closed). With open membership, anyone may give input, raise issues and develop proposals, while named maintainers accept decisions, and decisions record the maintainer's name and role. Project Guide would be recorded as team, open membership, with the founder as maintainer.
   - **Pros:** Size and openness are independent, so the change is small. An open organization (several teams) is also covered. The existing team rules for attribution apply unchanged.
   - **Cons:** It adds a third field to the Collaboration section. `start-project`, `decide` and the glossary need updates. "Team" may undersell an open community.
2. **A fourth mode, "open source":** Add open source next to solo, team and organization. Anyone may contribute. Maintainers listed in the overview accept decisions, which record the maintainer's name and role. Contributors' roles are self-declared, and expertise claims are treated as input to verify (with Q2).
   - **Pros:** One clear word matches how people describe such projects. Rules specific to open source, such as self-declared roles, have an obvious home.
   - **Cons:** It mixes openness with size, so a large open project with several teams fits neither "open source" nor "organization" cleanly. Self-declared roles get ahead of Q2.
3. **Solo decisions with open input:** Keep Project Guide solo, so one person decides with no roles or attribution, and allow open input on top: anyone may give input, raise issues and develop proposals.
   - **Pros:** It matches today's reality of one decision-maker and needs the fewest changes.
   - **Cons:** It conflicts with the definition of solo ("one person does the work") once others contribute. Decisions stop showing who accepted them, which hurts traceability for outside contributors (`overview.md` section 9). It doesn't scale to more maintainers.
4. **Public read, member write:** Keep the three modes. Add a `**Visibility:** public | private` field to the Collaboration section (absent means private). A public project can be read by anyone, skills included, but only accepted members commit directly. Non-members contribute through merge requests only, which a limited circle (the maintainers) approves and merges; their content is processed as input under `overview.md` section 8. Only the project owner adds or removes members and assigns their roles and expertise; members and roles are listed in the Collaboration section, and maintainers are members whom the owner has given that role. On the platform, only the owner holds the administrative rights needed to manage access (on GitHub, the admin role). Members commit directly to the default branch; the skills tell each member what their roles allow, a member can override, and Git history keeps overrides visible. Decisions may arrive by direct commit or by merge request. A post-merge pipeline stamps each new decision once with two fields taken from authenticated platform accounts: "Made by" (the pusher of a direct commit, or the merge request's author, with the merge request number) and "Approved by" (the maintainer who merged the merge request, and its approvers). This one-time platform stamp is the only permitted change to a decision after it lands. If the pipeline fails, CI (Q18) flags decisions without a stamp. Project Guide would be recorded as team, public, with the founder as the only maintainer.
   - **Pros:** Members are always known, so roles, expertise and attribution work as in team mode, and Q2 applies unchanged. Members work without merge-request overhead, while the public still has a reviewed path in. It fits the founder's input directly.
   - **Cons:** On some platforms, letting members push directly while only maintainers merge others' requests may need platform rules (for example, GitHub rulesets with a bypass list) or stay a rule the skills enforce; this must be checked at setup (Q5, Q16). Member write access relies on the skills and history rather than hard enforcement, so a mistaken push reaches the default branch until it's reverted (CI in Q18 can catch some). The owner is a single point of failure for membership; handing it over or sharing it later needs a decision.

## Q16: Sharing contributor updates

### Question

How does a contributor bring their changes up to date with the shared project and resolve conflicts before sharing them?

### Why It Matters

Distributed open-source work needs clear instructions for sharing updates. Without them, concurrent changes collide, and contradictions with settled knowledge can slip in.

### Context

Founder input (2026-10-11): a Git skill that fetches the latest default branch from origin, rebases changes on top, and resolves conflicts both at file level and at the logical level, where input contradicts the overview, decisions or facts. Agreed framing: a Git adapter behind a general "share updates" step (Q5). `decide` already says to commit and push for Git. `overview.md` section 8: contradictions become new issues. Related to Q15 (outside input) and Q19 (contributing guide).

### Resolution Points

- ❓ **Sharing step**
  - **Resolution:** Pending
  - **Details:** The store-independent "share updates" step, and the Git adapter's sync and rebase flow.
- ❓ **File-level conflicts**
  - **Resolution:** Pending
  - **Details:** How diff conflicts are resolved, and what needs the contributor's confirmation.
- ❓ **Logical conflicts**
  - **Resolution:** Pending
  - **Details:** How contradictions with the overview, decisions or facts are detected and turned into issues instead of being settled in the merge.

## Q17: Non-terminal interface

### Question

Is a lightweight shell around the agent CLI feasible, so that people outside IT can use the framework, and should it be built or adopted?

### Why It Matters

Most potential users are not IT people, and a terminal would put them off. Future connectors, views and plugins for third-party services (Google Docs, social networks, image browsing, browser links) go beyond plain text.

### Context

Founder input (2026-10-11). `overview.md` describes a tool-independent framework and does not cover a user interface, so this would widen the scope. Non-terminal agent front ends already exist, such as desktop and web apps. Related to Q5 (connectors as integrations).

### Resolution Points

- ❓ **Feasibility**
  - **Resolution:** Pending
  - **Details:** Effort, constraints, and what existing front ends already cover.
- ❓ **Build or adopt**
  - **Resolution:** Pending
  - **Details:** A custom shell, an existing front end, or a combination.
- ❓ **Extensions**
  - **Resolution:** Pending
  - **Details:** How connectors, views and plugins for third-party services fit in.

## Q18: CI checks

### Question

What should CI check on contributions to Project Guide, and where does it run?

### Why It Matters

Outside contributors will change the project's records and skills; automated checks keep the layout and rules intact without manual review of every rule.

### Context

Founder input (2026-10-11). The repository is mostly Markdown records and skills. Candidate checks: Project Guide layout, issue IDs and `Next question ID`, links, decision immutability, and skill format. Related to Q15 and Q19.

### Resolution Points

- ❓ **Checks**
  - **Resolution:** Pending
  - **Details:** Which rules are checked automatically and which stay with review.
- ❓ **Platform**
  - **Resolution:** Pending
  - **Details:** Where CI runs and what triggers it.

## Q19: Contributing guide

### Question

What must contributors know to take part in Project Guide, and where is it documented?

### Why It Matters

Open-source contributors need clear instructions on how to propose input, raise issues, share updates and get decisions accepted.

### Context

Founder input (2026-10-11). Depends on Q15 (open-source mode and decision authority) and Q16 (sharing updates); Q7 settles the skill names it refers to. Related to Q18 (CI).

### Resolution Points

- ❓ **Content**
  - **Resolution:** Pending
  - **Details:** Contribution paths, required skills and setup, and review and acceptance rules.
- ❓ **Location**
  - **Resolution:** Pending
  - **Details:** For example `CONTRIBUTING.md`, the README, or both.
