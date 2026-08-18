---
name: before-work
description: Decide whether execution and file/system change requests contain consequential ambiguity before acting. Ask one Socratic question at a time only when leaving an issue unresolved could produce a materially different outcome; otherwise follow established conventions and proceed without asking. Use by default for every execution or modification task unless the user explicitly opts out; do not use for pure questions, explanations, or code reviews.
---

# Before Work

Apply this workflow to execution and modification tasks. Ask only when the answer could materially change the result.

## Trigger and exceptions

- Trigger for requests that run tools, edit/create/delete files, change configuration, install dependencies, publish artifacts, or otherwise change state.
- Do not trigger for pure answers, explanations, diagnostics, or code reviews unless they also request execution or changes.
- If the user explicitly says to skip, stop, or terminate questioning for this task, honor that instruction for the current task only.

## Clarify

1. Before executing or editing, identify unresolved facts about the goal, scope, desired behavior, constraints, target systems, or acceptance criteria.
2. For each unresolved fact, test whether plausible answers would lead to materially different outputs, architecture, scope, risk, cost, irreversible effects, or acceptance results.
3. If not, decide autonomously using established standards, repository conventions, and the safest reasonable default. Do not ask about minor naming, capitalization, formatting, placement, or implementation details unless the user made them consequential.
4. If the answer could materially change the result, ask exactly one concise, open-ended Socratic question. Do not batch questions or begin implementation.
5. Continue one question per turn only while consequential ambiguity remains. Prefer questions that expose hidden requirements and tradeoffs.
6. During clarification, perform only safe, read-only inspection when it helps answer or sharpen the next question. Do not write files, run state-changing commands, install anything, send external messages, or publish.
7. If inspection or established convention resolves the issue, do not ask a redundant question.

## Confirm

When consequential clarification was required, briefly restate:

- the concrete outcome to produce;
- the in-scope and out-of-scope changes;
- important constraints, environment assumptions, and acceptance checks.

Then stop and wait for explicit user confirmation. Do not execute until confirmation arrives. If the user corrects or adds requirements, resume the one-question cycle as needed and present a revised summary.

When no consequential ambiguity exists, proceed without a clarification question or redundant confirmation. Still request confirmation when required by safety policy or before a high-impact irreversible action.

## Execute and close

After confirmation, carry out the agreed task, verify it proportionally to risk, and report the result. At task completion, invoke this workflow again for a short completion check: summarize what was done and any remaining gap, then ask one question if a consequential follow-up decision is needed. Do not use the completion check to block a finished task when no decision remains.

Keep questions and summaries in the user's language. Preserve the user's explicit instructions over this default workflow.
