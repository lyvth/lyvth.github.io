---
name: pr-review
description: Final step of the ideate -> implement -> pr-review loop for this personal introduction site (Vue + Vite). Use right after `/implement` finishes a change, or whenever the user asks to review a PR/diff with staff-engineer rigor and UI/UX judgment (e.g. "review this PR", "review my changes", "does this look good?", "check the UI/UX on this"). Not for general code review elsewhere in the machine — this is scoped to this repo.
---

Run the `staff-uiux-review` custom agent (defined at `.claude/agents/staff-uiux-review.md`) against the current diff or a specified PR.

1. Call the Agent tool with `subagent_type: "staff-uiux-review"`. Tell it what to diff (current working changes, a branch, or a specific PR number if the user names one) — default to the current uncommitted/branch diff if unspecified.
2. Run it in the foreground (`run_in_background: false`) since the user is waiting on the verdict.
3. Relay the findings from `ReportFindings` to the user directly — don't paraphrase away specifics like file/line references.
4. Based on the outcome:
   - If there are findings that need fixing, offer to run `/implement` again with those fixes as the next chosen approach.
   - If the review is clean, tell the user the loop is complete and ask if they have a new request to `/ideate`.

This closes the loop: `/ideate` picks a direction, `/implement` builds it, `/pr-review` checks it, and issues route back to `/implement` (or all the way back to `/ideate` if the review reveals the underlying idea itself needs rethinking, not just the code).
