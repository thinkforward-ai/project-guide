# Open Issues

This file contains only unresolved issues that currently require investigation or a decision.

**Next question ID:** Q26

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

## Q3: Who performs input processing

### Question

Who or what classifies input and detects bias and contradictions: an agent, a human, or both?

### Why It Matters

This decides how reliable and how automated the "under research" stage is, and who is accountable for its results.

### Context

`overview.md` section 8: every input is classified, checked for bias, validated against settled knowledge, and checked for contradictions.

The [project roles decision](decisions/20261115-1850-project-roles.md) settles part of this: input from a required expertise owner is expert opinion, and all other input is opinion, recorded but not binding. Opinions are not answered one by one ([framework consistency](decisions/20261115-1921-framework-consistency-and-guardian.md)).

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

Related: the [project roles decision](decisions/20261115-1850-project-roles.md) classifies opinion and expert opinion by the roster. Establishing facts remains open here; skills do not certify facts.

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

Verifying that only accepted members can write to `main` is the founder's top priority before inviting other contributors (2026-10-28). Public read access is intended.

### Context

`overview.md` section 3 defines the three modes; solo uses no roles and no decision attribution. Every accepted decision so far names an accepter ("Maxim Nikitin (project manager)"). Split from Q13 (roadmap); its outcome may change milestone order there. Related to the [project roles decision](decisions/20261115-1850-project-roles.md), which settled Q2: only expertise owners decide issues that need their expertise, and the stakeholder keeps reserved decisions. A proposal in which only the founder accepts decisions must be reconciled with that rule. The [framework consistency decision](decisions/20261115-1921-framework-consistency-and-guardian.md) gives Project Guide a provisional roster with a framework guardian.

### Resolution Points

- ❓ **Mode model**
  - **Resolution:** Pending
  - **Details:** A fourth mode, or a team or organization project with open membership.
- ❓ **Decision authority**
  - **Resolution:** Pending
  - **Details:** Who accepts decisions when contributors are unknown, for example maintainers or expertise holders, and whether decisions carry attribution. How repository and inherited organization permissions enforce member-only direct writes, while members retain direct access and non-members use reviewed merge requests.
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
12. Founder input (2026-10-28): protecting `main` is the top priority before inviting other people. This revisits the earlier assumption in findings 7 to 9 and proposal 4 that member direct pushes remove the need for branch protection. The required rules and any exceptions remain unresolved; no protection policy has been accepted or applied.
13. Founder clarification (2026-10-28): "Public may read; only members may write." Member access remains acceptable; the concern is public write access, not public visibility or requiring merge requests from members. This corrects the branch-protection interpretation in finding 12 and retains the access model in findings 8 and 9. Selecting that boundary clarified the requirement; it did not accept a complete Q15 proposal or authorize repository changes.
14. Read-only GitHub public API checks (2026-10-28) report repository visibility `public`, default branch `main`, and branch `protected: false`. Public visibility permits reading; absence of branch protection is not evidence of public write access. Actual collaborators, inherited organization permissions, and administrative access remain unchecked: no GitHub connector is offered in this environment and the GitHub CLI is not installed. No external settings were changed.
15. Proposal 4 below is refined against the latest clarification. Proposals 1 to 3 remain alternatives for comparison, not accepted directions. Repository permission verification is implementation follow-through, not evidence already obtained; whether changes are necessary is unknown. Maintainer-only merging must not be described as a platform guarantee merely because outsiders lack write access: member write access can also permit merging.

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
4. **Public read, member write:** Keep solo, team and organization modes. Add `**Visibility:** public | private` to the Collaboration section (absent means private). Public projects are readable by anyone, skills included; only project-accepted members may write directly to the default branch. Only the project owner adds or removes members and assigns their roles and expertise; list the owner, members and roles in the Collaboration section. Maintainers are members given that role by the owner. Non-members submit merge requests, which only maintainers may approve and merge under the project rules; their content is processed under `overview.md` section 8. Member direct pushes remain allowed. Skills govern role-specific conduct, and Git history records changes; this is not a claim of hard enforcement within the member group.
   1. **Project Guide:** Record team mode, public visibility, the founder as owner and initially the sole member and maintainer, and retain user-driven mode. Only the founder accepts project decisions for now; adding decision authority requires a later decision.
   2. **Access verification:** Before inviting contributors, audit repository collaborators, teams, organization base permissions and inherited administration. Public users must have no write access; accepted members may write directly. Keep membership administration with the owner and disclose any unavoidable organization-owner or platform-administrator authority. Public visibility and an unprotected branch do not establish an access gap; change settings only if the authenticated audit finds one, and only with separate approval. If maintainer-only merging cannot be enforced without removing member direct writes, retain it as an explicit project rule and disclose that limit rather than claim it is enforced.
   3. **Decision provenance:** Preserve `Accepted by` as the confirmed decision-maker, not the account transporting a change. A pipeline triggered by changes reaching the default branch adds one platform-derived stamp: `Made by` identifies the authenticated direct pusher or merge-request author with its request number; `Approved by` identifies the authenticated merger and recorded approvers for a merge request, or explicitly states that no merge-request approval applies to a direct push. These fields describe delivery, not decision authority. This one-time stamp is the only permitted post-record change; CI flags missing stamps rather than inventing approval. Detailed implementation remains with Q18.
   4. **Follow-through:** Update the glossary, relevant lifecycle skills and project guidance to reflect the accepted model. Detailed expertise definitions remain with Q2, integration and sharing mechanisms with Q5 and Q16, and CI and contributor guidance with Q18 and Q19. Acceptance does not certify current permissions, create unreviewed executable tasks, install skills, or authorize external changes.
   5. **Pros:** Fits the clarified public-read/member-write requirement and existing team rules. Preserves direct member work and reviewed outside contributions. Separates actual decision authority from platform provenance and avoids treating an unprotected branch as public write access.
   6. **Cons:** Current access still needs an authenticated audit; an implementation gap has not been established. Member conduct and potentially maintainer-only merging remain procedural rather than hard-enforced. The founder remains a membership and decision-authority bottleneck. Skill changes, provenance automation and contribution guidance require subsequent reviewed work.

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

## Q21: Durable definitions shaped by increments

### Question

How should issues, decisions and tasks, as increments, shape durable definition files that every accepted change updates and every new proposal is checked against?

### Why It Matters

Without a durable definition, settled meaning is scattered across issue records, inputs, decisions and the overview. New proposals have nothing stable to be checked against, and the current definition must be reconstructed from history.

### Context

User input from a project managed with Project Guide (2026-11-15): "open issues ande decisions and tasks - these are increments. However they should shape durable definitions. For instanst in this case - we can decide to create a concept file. It means we keep updating it every time the concept changes. It also means - we check any new proposals - if they match it and how to integrate them".

That project adopted it locally: a `concept.md` whose statements link to their source input or decision, a **Concept fit** line in every proposal, and an update of `concept.md` in the same step as each accepted decision. Related to `overview.md` (settled understanding), the refine Proposal Format, decide (Record and Apply), and the layouts in work-on-project and start-project.

### Resolution Points

- ❓ **Definition files**
  - **Resolution:** Pending
  - **Details:** Whether the layout names durable definition files or lets each project choose them (for example concept, requirements, architecture), and how they differ from `overview.md`.
- ❓ **Proposal fit**
  - **Resolution:** Pending
  - **Details:** Whether the refine Proposal Format adds a fit line stating which definitions a proposal matches, changes or extends, and how it would be integrated.
- ❓ **Update on decision**
  - **Resolution:** Pending
  - **Details:** Whether decide updates affected definitions in the same step, and how statements link to their decision or input.
- ❓ **Layout handling**
  - **Resolution:** Pending
  - **Details:** How work-on-project and start-project treat definition files when bootstrapping or aligning a project.

## Q22: Milestone confirmation by demo

### Question

Should a milestone count as reached only after the stakeholder has been given a demo and has confirmed it, rather than as soon as its criteria are met?

### Why It Matters

work-on-project and the glossary say a milestone is achieved when all its criteria are met, and the next becomes current. An agent can therefore claim completion and start the next milestone without stakeholder sign-off, especially in AI-driven mode.

### Context

User correction in a project managed with Project Guide (2026-11-15). After the AI marked a milestone achieved because its criteria were met, the user said: "Reaching milestone means - giving me a demo - so I can confirm it is reached." That project recorded it as a decision and added a confirmation criterion to every milestone. Related to Q13 (project roadmap) and Q6 (measuring progress and completion).

### Resolution Points

- ❓ **Confirmation rule**
  - **Resolution:** Pending
  - **Details:** Whether meeting the criteria makes a milestone ready for a demo rather than reached, and who confirms it in solo, team, and organization modes.
- ❓ **Demo form**
  - **Resolution:** Pending
  - **Details:** What counts as a demo for non-software milestones, and whether its form is agreed per milestone.
- ❓ **Skill wording**
  - **Resolution:** Pending
  - **Details:** Changes to the work-on-project roadmap step, the glossary's Milestone term, and the start-project roadmap template.
- ✅ **AI-driven mode**
  - **Resolution:** Settled by [AI-driven mode as delegation](decisions/20261115-1809-ai-driven-mode-as-delegation.md)
  - **Details:** In AI-driven mode, a milestone is reached only when the stakeholder confirms it after a demo. Whether this applies in user-driven mode stays open here.

## Q24: Growing the role catalogue from projects

### Question

How should roles that projects define from scratch, or redefine, flow back into Project Guide's starter role catalogue?

### Why It Matters

The catalogue covers only domains the framework has seen. Without a feedback loop, every project in a new domain defines the same missing roles again, and improvements made in project rosters stay local.

### Context

Founder input (2026-11-15), while refining the [project roles decision](decisions/20261115-1850-project-roles.md): skills define missing roles from scratch in a project's roster, and later a feedback loop could source roles from projects back to the framework, so the catalogue keeps growing. The founder framed this as a future step.

### Resolution Points

- ❓ **Collection**
  - **Resolution:** Pending
  - **Details:** How new or redefined roles in project rosters are noticed and proposed back, for example during the skill update check or at milestone completion.
- ❓ **Acceptance**
  - **Resolution:** Pending
  - **Details:** Who accepts a role into the catalogue, and what evidence of reuse it needs.
