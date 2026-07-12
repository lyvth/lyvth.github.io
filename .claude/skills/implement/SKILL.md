---
name: implement
description: Middle step of the ideate -> implement -> pr-review loop for this personal introduction site (Vue + Vite). Use once a direction has been chosen — either right after the `ideate` skill produced a recommendation the user picked, or when the user already knows exactly what they want built/changed and just needs it coded. Trigger on things like "implement option 2", "go with that", "just build it", or a direct code-change request that doesn't need brainstorming.
---

Run the `implement` custom agent (defined at `.claude/agents/implement.md`) to make the actual code change.

1. Call the Agent tool with `subagent_type: "implement"`. Pass it a clear statement of the chosen approach: if this follows an `/ideate` run, include which option was picked and the relevant details from that agent's output; if the user skipped straight here, pass their request directly.
2. Run it in the foreground (`run_in_background: false`) so you can report back and decide next steps once it's done.
3. Summarize for the user what changed (files touched, what the change does) — don't just relay the agent's raw output if it's verbose.
4. Tell the user the change is ready for review and offer to run `/pr-review` now (or run it yourself if they say yes/go ahead).

If the direction is genuinely ambiguous (not just an implementation detail), it's better to hand back to `/ideate` than to guess — but for small ambiguities, make the smallest reasonable choice per the `implement` agent's own instructions rather than stalling.
