---
name: ideate
description: Kick off the ideate -> implement -> pr-review loop for this personal introduction site (Vue + Vite). Use whenever the user proposes a new feature, section, content change, or design tweak and hasn't already settled on an exact approach. Make sure to trigger this for any request that involves a new idea or design decision, even if the user doesn't say "ideate" explicitly (e.g. "thêm 1 section giới thiệu kỹ năng", "làm cho trang này đẹp hơn", "add a projects gallery").
---

Run the `ideate` custom agent (defined at `.claude/agents/ideate.md`) on the user's request.

1. Call the Agent tool with `subagent_type: "ideate"`. Pass it the user's raw request plus any context from the conversation it will need (e.g. which section of the site, any constraints already mentioned).
2. Run it in the foreground (`run_in_background: false`) — you need its output before you can talk to the user about next steps.
3. Present the agent's approaches and recommendation to the user as-is; don't compress it into a single option unless the user asks you to just pick one.
4. Ask the user which approach they want (or confirm the recommended one), then tell them you can proceed with `/implement` once they've chosen — offer to run it yourself right away if they'd rather not type the command.

Do not start writing or editing code yourself in this skill — that's `implement`'s job. This skill's only output is ideas + a decision point.
