# Add AI-driven mode to skills and glossary

**Decision:** [AI-driven mode](../decisions/20261004-1852-ai-driven-mode.md)

## What

Phase skills behave per the project's driving mode, `start-project` asks for and records it, and the glossary defines both modes.

## Why

Implement the accepted AI-driven mode decision linked above. Founder clarification (2026-10-04): recommendations are given when available, since AI cannot always form one.

## How

1. In `skills/glossary/SKILL.md`, append:
   1. **AI-driven:** AI, possibly a team of AI roles, runs the lifecycle and passes transition gates. The user, as stakeholder, makes decisions and is asked about anything in their interest, with a recommendation when available.
   2. **User-driven:** The user passes every gate. The default.
2. In `skills/start-project/SKILL.md`, make the Entry Gate also ask for the driving mode (AI-driven or user-driven) with the collaboration mode, and make Work step 2 record `**Driving:**` in the Collaboration section. Add before `## Exit Gate`:

   ```md
   ## AI-driven mode

   Decide yourself whether to refine the first issue now and state why. Ask the stakeholder about the goal, requirements, and preferences, with your recommendation when available.
   ```

3. In `skills/raise-issue/SKILL.md`, add before `## Exit Gate`:

   ```md
   ## AI-driven mode

   Register issues you discover without waiting to be asked. Decide yourself whether to refine now or later and state why.
   ```

4. In `skills/refine/SKILL.md`, add before `## Exit Gate`:

   ```md
   ## AI-driven mode

   Drive the refinement. Request missing information from the stakeholder and contributors. Ask the stakeholder about anything in their interest, including how to do the work, with your recommendation when available. Decide yourself when proposals are ready and state why.
   ```

5. In `skills/decide/SKILL.md`, add before `## Exit Gate`:

   ```md
   ## AI-driven mode

   List proposals with your recommendation when available. Only the stakeholder chooses; the gate stays. Review tasks with the stakeholder.
   ```

6. In `skills/work-on-project/SKILL.md`, add before `## Exit Gate`:

   ```md
   ## AI-driven mode

   Read the driving mode from the overview. Choose the next action yourself, state it and why, and proceed. Show the menu when the stakeholder asks or a stakeholder gate is reached.
   ```

## Acceptance Criteria

1. All five phase skills contain an `## AI-driven mode` section with the text above.
2. `start-project` asks for and records the driving mode.
3. The glossary defines AI-driven and user-driven.
4. User-driven behavior is unchanged.

## Prerequisites

None.

## Dependencies

None.
