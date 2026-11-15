# Open Issues

This file contains only unresolved issues that currently require investigation or a decision.

**Next question ID:** Q31

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

The stakeholder requested a team-proposed roadmap on 2026-11-15, including existing capabilities and considering all 19 currently open issues. This authorizes refinement, not milestone adoption or confirmation.

### Expertise

1. **Framework designer:** capability boundaries, useful outcomes, and dependency order.
2. **Framework guardian:** consistency with accepted decisions, original purpose, and scope.
3. **Coordinator:** evidence, status, lifecycle dependencies, and issue coverage.
4. **Stakeholder:** reserved decision on milestone definitions and order, and later milestone confirmation.

### Resolution Points

1. ❓ **Milestones**
   1. **Resolution:** Pending
   2. **Details:** Names, intents, done-when criteria, and order, drawn from `overview.md` and the accepted decisions. Only the stakeholder may adopt them.

### Findings

1. Existing capabilities include all seven source skills, the issue-to-task lifecycle, task-completion checks, both driving modes, expertise-based project roles, guardian review, visible role markers, and read-only skill-update checks during status. These are implementation evidence, not previously accepted or confirmed milestones. See the [lifecycle](decisions/20261003-1603-project-lifecycle-orchestration.md), [task closure](decisions/20261019-2137-complete-task-skill.md), [delegation](decisions/20261115-1809-ai-driven-mode-as-delegation.md), [roles](decisions/20261115-1850-project-roles.md), [consistency and guardian](decisions/20261115-1921-framework-consistency-and-guardian.md), and [role visibility](decisions/20261115-2042-visible-role-markers-and-coordinator.md) decisions.
2. The read-only audit on 2026-11-15 compared the then-19 open issues with 14 decision records, seven source skills, and eight unclosed task records. Each retained an unresolved part at that time; Q22 has since been resolved by the decision below. Several task criteria have since been superseded; feature presence alone does not establish task completion.
3. The earlier findings were stale: Q2 and Q14 are resolved, and the task-closure skill is implemented. The earlier proposal's "M1 achieved" was never an accepted milestone or stakeholder confirmation.
4. The [project-level driving-mode decision](decisions/20261115-2146-project-guide-ai-driven-mode.md) makes this project AI-driven. The later [required milestone demos and confirmation decision](decisions/20261115-2330-required-milestone-demos-and-confirmation.md) resolves Q22 across all modes: meeting criteria makes a milestone ready for a demo; achievement requires an evidence-backed demo followed by explicit human stakeholder confirmation.
5. The glossary defines a roadmap as naming no issues or tasks. Keep the issue mapping below with this proposal; if adopted, write outcome criteria and progress logs, not issue IDs or task lists, into `roadmap.md`.
6. Q15 remains parked until the stakeholder explicitly reopens it. It may be shown as a dependency of a future milestone, but roadmap acceptance must not reopen it or certify repository permissions. The existing provisional roster remains in force meanwhile.
7. Execution-skill design is out of scope under `overview.md` section 2. Q27 challenges that boundary, and Q17 may expand the framework into an interface. Both need separate stakeholder scope decisions before delivery commitments. No technology, external action, installation, or invitation is authorized by a roadmap.
8. The three earlier unaccepted drafts (capability layers, a single core milestone, and self-use followed by external use) are consolidated into the single updated proposal below. It retains existing capability recognition, capability-based sequencing, and evidence from actual use, without their stale issue groupings or unsupported achievement claim.
9. Stakeholder requirement (2026-11-15): when a milestone's outcome cannot be run or directly shown, prepare and deliver its demo/presentation as HTML slides. Runnable or directly showable outcomes may use a direct demonstration. This requirement is now part of the linked Q22 decision; neither that decision nor this proposal adopts the roadmap or confirms a milestone.

### Proposals

**Problem:** Project Guide needs an outcome-based roadmap that recognizes what already exists, orders the remaining capabilities, and accounts for every open issue without silently settling its design or expanding scope.

1. **Evidence-led capability roadmap (recommended):** Five milestones in intended order, followed by two conditional future directions. The order guides focus, not a blanket ban on independent later work. Every milestone needs an evidence-backed demo and stakeholder confirmation before it is achieved. Use a direct demonstration when the outcome can be run or directly shown; otherwise prepare and deliver the demo/presentation as HTML slides. This format requirement applies to every milestone demo below and does not replace evidence or confirmation. Each receives a one-line progress log when adopted; no milestone is confirmed by accepting this proposal.
   1. **M1. Lifecycle foundations**
      1. **Intent:** Recognize and demonstrate the framework already built, without claiming its known reliability gaps are solved.
      2. **Starting evidence:** All seven source skills, driving modes, roles, guardian, role visibility, and status update checks exist. Formal milestone review and confirmation have not happened.
      3. **Done when:** The seven skills and their shared contract, authority rules, and mode boundaries are present; an evidence-backed walkthrough shows bootstrap, registration, refinement, decision-linked task preparation, completion checks, and resumption; the evidence distinguishes implemented capabilities, known gaps, and unclosed or superseded task criteria.
      4. **Demo:** Walk through existing source skills and project records, explicitly disclosing remaining gaps rather than inventing a completed end-to-end run.
   2. **M2. Dependable project records**
      1. **Intent:** Make the durable project state trustworthy across phases, sessions, installations, and task closure.
      2. **Starting evidence:** Decisions and the overview already preserve settled understanding; phase routing and task closure exist, but record timing, durable-definition handling, reference portability, and moved-task links have unresolved gaps.
      3. **Done when:** Phase execution and record-timing rules are explicit and demonstrably followed; accepted changes keep the chosen durable definitions current and proposals are checked against them; task closure preserves valid incoming and internal trace links; project/skill naming is settled and cross-skill/resource references remain usable under the supported installation naming conventions.
      4. **Demo:** Resume from project files without session history, trace one accepted change into the current definition, and close a sample task while preserving its links and evidence.
   3. **M3. Trustworthy research and readiness**
      1. **Intent:** Turn uncertain input into a justified, implementation-ready description with visible remaining unknowns.
      2. **Starting evidence:** Input preservation, expertise-based opinion classification, role verdicts, and roadmap/status structure exist. The linked Q22 decision now requires demos and explicit human stakeholder confirmation across all modes. Detailed input organization, processing responsibility, fact policy, and research-readiness measures remain open.
      3. **Done when:** Input organization and required/optional material are defined; classification, bias checks, contradiction handling, and human/AI responsibilities are explicit; establishing and challenging facts has a policy; explored/unknown areas and implementation blockers are visible; milestone completion and demo rules are unambiguous across supported collaboration and driving modes.
      4. **Demo:** Process conflicting input into a reviewed decision and ready instruction, show what remains unknown and why it does or does not block implementation, and demonstrate the applicable milestone-confirmation rule.
   4. **M4. Tool-independent shared work**
      1. **Intent:** Let contributors find project services and exchange changes without making the core depend on Git.
      2. **Starting evidence:** The framework separates its model from storage and includes sharing instructions; per-project integration configuration and synchronization/conflict workflows remain undefined.
      3. **Done when:** Integration purposes, configuration, service contracts, and setup responsibility are defined; a store-independent sharing flow and a Git adapter handle synchronization, file conflicts, and logical contradictions without silently rewriting settled meaning; the same lifecycle is demonstrated using Git and one separately approved non-Git store.
      4. **Demo:** Exchange concurrent changes, surface a logical conflict as an issue, and show equivalent durable project state on the two stores.
   5. **M5. Contributor-ready framework**
      1. **Intent:** Make participation understandable, governed, checked, and capable of feeding reusable roles back into the framework.
      2. **Starting evidence:** Open-source licensing and a provisional role roster exist. Collaboration governance, authenticated permission verification, CI, contribution guidance, and catalogue feedback remain open.
      3. **Done when:** Collaboration, membership, decision authority, and outside-input rules are accepted and documented; an authenticated access audit verifies public-read/member-write requirements and discloses inherited administrative authority and enforcement limits; the selected CI checks run; contributor guidance covers setup through accepted changes; a role-feedback policy names collection, acceptance authority, and reuse evidence.
      4. **Demo:** Walk through an outside contribution and a member contribution using an authorized example or controlled exercise, show accepted/rejected check results and access-audit evidence, and review a candidate role through the agreed feedback policy.
      5. **Dependency:** Governance and access work stay blocked while the stakeholder keeps that subject parked. Other independent preparation may proceed; no contributor invitation or external settings change is implied.
   6. **Conditional future: accessible, non-terminal use**
      1. Investigate feasibility and build/adopt options. Only after a separate stakeholder scope/platform decision would delivery become a milestone, with criteria for a non-technical user to complete the selected lifecycle without a terminal and for any approved connectors or views.
   7. **Conditional future: traced task execution**
      1. Decide separately whether execution pickup belongs in core or remains outside it. Only an accepted scope change would add a delivery milestone covering ready-task selection, scoped execution, design-question escalation, evidence, and closure handoff. Keeping execution outside core is still a valid outcome.
   8. **Issue coverage (proposal rationale only, not roadmap content):**
      1. M1 recognizes previously delivered capabilities, including the resolved role and task-closure work; it closes no currently open issue merely by naming that work.
      2. M2: Q7, Q21, Q26, Q28, Q29.
      3. M3: Q1, Q3, Q4, Q6. Resolved Q22 contributes the settled demo-and-confirmation rule; it is no longer open work.
      4. M4: Q5, Q16. Its logical-conflict handling uses the research policies developed in M3.
      5. M5: Q15 (still parked), Q18, Q19, Q24. It uses the naming, reference, and sharing outcomes developed earlier.
      6. Conditional directions: Q17 and Q27, without accepting either delivery proposal.
      7. Q13 is resolved only if the stakeholder adopts a roadmap through the decision phase. This accounts for all 18 remaining open issues and the resolved Q22 contribution without treating milestone adoption as their resolution.
   9. **Focus and progress:** If adopted, first review and demo M1; do not label it achieved retrospectively. M2 is the next capability focus after confirmation. Record only evidence-backed progress, with no invented completion percentages, dates, or prior approvals. Technology choices and external actions keep their separate authorization requirements.
   10. **Pros:** Recognizes existing work honestly, addresses every open issue, repairs traceability before scaling collaboration, and measures usable outcomes rather than issue counts. Allows independent preparation without reopening parked work.
   11. **Cons:** Five milestones require more maintenance than a single finish line; M3 is substantial; the second-store demonstration needs separately approved platform/access choices; M5 cannot finish while governance is parked. The two scope-sensitive directions have no delivery commitment or date.
   12. **Verdicts:** Framework designer: no concern; capability boundaries and order are coherent, with a known bias toward richer structure and the explicit trade-off that M3 remains substantial. Framework guardian: no concern with recording/presenting this proposal, conditional on no unsupported achievement claims, no reopening Q15, no implicit scope expansion, no preselection of unresolved issue solutions, and keeping issue IDs outside the adopted roadmap; all conditions are incorporated. The HTML-slide amendment and required confirmation now follow the separate accepted Q22 decision without adopting this roadmap. Coordinator: no concern; all 18 remaining issues and the resolved Q22 contribution are accounted for, evidence and dependencies are explicit, and adoption remains a stakeholder decision.

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

## Q26: Every phase runs through its skill, also in AI-driven mode

### Question

Should AI-driven mode state explicitly that "flow without stops" still runs every phase through its skill, with records written as part of each phase rather than afterwards?

### Why It Matters

Records are the source of truth and leave the trace; a session is only a temporary work process, not the outcome. Without an explicit rule, an agent can read "flow without stops" and "records may be written when a burst of work ends" as permission to skip phases and fill in records later, which leaves records that describe steps that never happened.

### Context

Raised from the ninetiles project by its Project manager role. It counts as opinion here, under the [role scope boundary](decisions/20261115-1929-role-scope-boundary.md). In ninetiles, the M4 feature was delivered in AI-driven mode without invoking `raise-issue`, `refine`, or `decide`. No issue or task existed, the decision was written after implementation, and it falsely claimed that an issue had been registered. ninetiles corrected this with a new decision. The ninetiles stakeholder stated: "team should always follow the workflow and the structure - since it is a backbone. The purpose is to maintain the source of truth, keep traces - session is not one. Session is just an operational temprorary short-living entity. It is a work process. Not the outcome." Related to the [AI-driven delegation decision](decisions/20261115-1809-ai-driven-mode-as-delegation.md).

### Resolution Points

- ❓ **Phases in AI-driven mode**
  - **Resolution:** Pending
  - **Details:** Whether delegation removes only the stakeholder's gates, while every phase still runs through its skill.
- ❓ **Record timing**
  - **Resolution:** Pending
  - **Details:** Whether "records may be written when a burst of work ends" should be replaced by writing each record as its phase completes.

### Proposals

**Problem:** AI-driven mode can be read as permission to skip phases and fill in records afterwards.

1. **Phases are the backbone:** State in the AI-driven sections and the glossary that delegation removes waiting for the stakeholder, not phases. Each phase runs through its skill, and its records are written and shared as that phase completes. Records are the source of truth; a session is a temporary work process. Remove "records may be written when a burst of work ends".
   - **Pros:** Records stay true and complete, and the trace never depends on a session surviving. It costs no stakeholder time.
   - **Cons:** It adds a few record writes per feature.

## Q27: A skill that picks up and executes ready tasks

### Question

Should Project Guide's core include a domain-neutral skill that picks up a ready task and carries it out, between task creation and `complete-task`?

### Why It Matters

The lifecycle stops when a task is created. `decide` creates tasks and `complete-task` closes them, but nothing defines who picks up a task, when, how the work stays within its scope, or how evidence is recorded for closure. In practice the work happens spontaneously, outside the framework's trace, which conflicts with records being the source of truth.

### Context

Raised from the ninetiles project by its Project manager role. It counts as opinion here, under the [role scope boundary](decisions/20261115-1929-role-scope-boundary.md). The ninetiles stakeholder observed: "implementation went well - however do we have any skill doing actual work and picking up the task? So far it feels framework stops on task creation. The rest goes spontaneously." This challenges `overview.md` section 2, which puts the design of execution skills out of scope for now and keeps execution optional and domain-specific. Related to the [complete-task decision](decisions/20261019-2137-complete-task-skill.md), which treats recording completion as core upkeep rather than execution, and to Q26 (every phase runs through its skill).

### Resolution Points

- ❓ **Scope**
  - **Resolution:** Pending
  - **Details:** Whether picking up and carrying out a task is core and domain-neutral, or stays with domain packs.
- ❓ **Pickup**
  - **Resolution:** Pending
  - **Details:** How a task is chosen: ready, dependencies complete, prerequisites available, and in which order.
- ❓ **Execution rules**
  - **Resolution:** Pending
  - **Details:** Who executes (the role whose expertise the task requires), staying within the task's scope, what happens when a design question appears, and how evidence is recorded for `complete-task`.

### Proposals

**Problem:** No skill covers the work between a ready task and its closure.

1. **Core `work-on-task` skill (domain-neutral):** It picks a ready task (dependencies complete, prerequisites verified) and has the role whose expertise the task requires carry out its **How** steps, staying strictly within the task's scope. If the work reveals a design question, it stops and raises an issue rather than deciding inline. It records evidence for each acceptance criterion in the task and hands off to `complete-task`. Domain packs may add domain-specific practices, such as tests or builds, on top. User-driven mode: the user chooses which task to start. AI-driven mode: the agent picks the next ready task itself, in roadmap order.
   - **Pros:** It closes the lifecycle gap and keeps execution traced from task to evidence to closure, while staying domain-neutral.
   - **Cons:** It reopens a settled scope boundary, and domain-neutral rules may be too thin for some domains until packs exist.
2. **Keep execution out of core; projects describe their own execution:** Each project defines how tasks are carried out.
   - **Pros:** The core stays small, as currently scoped.
   - **Cons:** Process rules would scatter into projects, against Project Guide being the single source of process, and execution would stay untraced.

## Q28: Relative links inside a task moved to tasks/closed/

### Question

Should `complete-task` also adjust the relative links inside a task when it moves the task to `tasks/closed/`?

### Why It Matters

`complete-task` updates links that point to the moved task, but the task's own links (for example `../decisions/...`) break because the file is one folder deeper. Closed tasks then lose their trace to decisions and the roadmap.

### Context

Raised from the ninetiles project by its Project manager role. It counts as opinion here, under the [role scope boundary](decisions/20261115-1929-role-scope-boundary.md). In ninetiles, three closed tasks had broken decision links until they were fixed by hand. Related to the [complete-task decision](decisions/20261019-2137-complete-task-skill.md), which says the task moves unchanged apart from the appended Completion section.

### Resolution Points

- ❓ **Link adjustment**
  - **Resolution:** Pending
  - **Details:** Whether adjusting relative links counts as part of "unchanged", or whether tasks should use links that stay valid after the move.

### Proposals

**Problem:** Moving a task one folder deeper breaks its relative links.

1. **Adjust relative links on the move:** `complete-task` rewrites the task's relative links so they still resolve from `tasks/closed/`, and treats this as part of moving it unchanged.
   - **Pros:** Closed tasks keep a working trace with no change to how tasks are written.
   - **Cons:** It is one more mechanical step, and it conflicts with the wording "unchanged" unless that is clarified.

## Q29: Purpose-based references in Project Guide skills

### Question

Should Project Guide's skills refer to each other and to their resources by phase, capability, or purpose rather than by skill or file name?

### Why It Matters

People may fill a phase or capability with a different skill, and installed names carry prefixes. References by identifier then fail or mislead.

### Context

Raised from the ninetiles project by its Project manager role. It counts as opinion here, under the [role scope boundary](decisions/20261115-1929-role-scope-boundary.md). The start-project fix (`64c5afb`) replaced a relative link with "`roles-catalogue.md` in the Project Guide glossary skill", which is still an identifier. Skills also name each other, for example "through `complete-task`" and "`raise-issue`". The user's principle: references should be "generic purpose-based / trigger-based definitions, rather than identificators." A related authoring rule is raised in Agent Hub (Q9 there).

### Resolution Points

- ❓ **References to rewrite**
  - **Resolution:** Pending
  - **Details:** Which phase-skill and resource references become purpose-based, and how a bundled resource such as the role catalogue is found by purpose.

### Proposals

**Problem:** Project Guide skills name other skills and files.

1. **Phase and capability references:** Phase skills refer to each other by phase or capability (for example "issue registration" or "task completion"), and to the role catalogue as "the starter role catalogue", never by skill name, file name, or path.
   - **Pros:** Any provider can fill a phase, and references survive install prefixing.
   - **Cons:** The agent must map purposes to installed skills, and the catalogue's location must be discoverable by purpose.
