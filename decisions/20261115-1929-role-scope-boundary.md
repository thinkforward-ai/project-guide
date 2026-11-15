# Roles act only within their own project

**Accepted by:** Maxim Nikitin (project manager)
**Date:** 2026-11-15

## Problem Description

With [project roles](20261115-1850-project-roles.md) in place, nothing limited where a role may act. A role from one project could change another project's structure, work its tasks, or make its decisions. The founder stated: identities operate only within the scope of the projects they are assigned to; other projects are third-party projects. A role may raise a feature request or a question there, but may not modify structure, work on tasks, or make decisions.

Framework guardian verdict: no conflict with accepted decisions. Conditions: a cross-project issue names its origin project and role, and in the receiving project it counts as opinion, decided entirely by that project's own rules.

## Decision

1. A role, human or AI, acts only within the project whose roster lists it.
2. Every other project is a third-party project for that role. There, the role may only raise an issue, such as a feature request or a question, through that project's issue register.
3. A cross-project issue names its origin project and role. In the receiving project it counts as opinion, and that project's own roles and rules decide whether and how to handle it.
4. A role never modifies a third-party project's structure or records beyond raising the issue, never works its tasks, and never makes its decisions.

## Explanation

1. Each project's roster, decisions, and guardian stay in control of that project, which keeps projects independent and their records trustworthy.
2. A stakeholder of several projects may direct work in each of them. That work is then done by the receiving project's own roles, under its own rules.

## Consequences

- The glossary's Role term, overview §3, the role catalogue, and `raise-issue` state the boundary.
- Projects piloting roles add the boundary to their local rules.
