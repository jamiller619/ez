---
name: ez
description: Choose a cost-appropriate Codex model and reasoning level, briefly explain the choice, then execute the user's original request. Use when the user explicitly invokes $ez, /ez, or asks for the ez model-routing workflow.
---

# ez

Treat the text accompanying the invocation as the original request. Select an appropriate Codex model and reasoning level before doing the work, then complete that request.

## Select the execution profile

Balance expected total cost against the chance of retries or poor results. Consider:

- scope and number of files or systems involved;
- ambiguity and how much judgment the request requires;
- expected tool use and workflow length;
- technical complexity, debugging depth, and failure risk;
- whether the work is easy to verify or costly to get wrong.

Prefer the least expensive available profile that is likely to finish correctly in one pass. Use lighter models and low reasoning for narrow, routine, easily verified work. Increase reasoning before increasing model capability when the task mainly needs careful analysis. Use stronger models for ambiguous architecture, difficult debugging, broad multi-file changes, high-stakes reviews, or tasks where a weak attempt would create costly retries.

Choose only among models and reasoning levels actually available in the current runtime. Do not invent model names, prices, or capabilities. If exact pricing is unavailable, make a qualitative cost judgment.

## Report and execute

Before substantive work, give a compact routing note containing:

- chosen model;
- chosen reasoning level;
- one-sentence rationale;
- confidence from 1 to 100.

Delegate the original request to a subagent using the selected model and reasoning level. Pass through the complete request, relevant context, constraints, permissions, and success criteria. Return the subagent's completed result.

Do not ask the user to choose among profiles unless a missing requirement would materially change the work itself. Preserve the original request's scope, permissions, and safety constraints. Model selection does not authorize additional actions.

End the completed response with: `ez pz lemon squeezy`.
