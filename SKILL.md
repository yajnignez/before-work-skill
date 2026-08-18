---
name: before-work
description: Socratically clarify execution and file/system change requests before acting, one question at a time, with read-only inspection allowed; summarize the understood goal and constraints and wait for explicit confirmation before making changes. Use by default for every execution or modification task unless the user explicitly opts out or terminates questioning; do not use for pure questions, explanations, or code reviews.
---

# Before Work

Apply this workflow to execution and modification tasks. Treat it as a gate before any state-changing action.

## Trigger and exceptions

- Trigger for requests that run tools, edit/create/delete files, change configuration, install dependencies, publish artifacts, or otherwise change state.
- Do not trigger for pure answers, explanations, diagnostics, or code reviews unless they also request execution or changes.
- If the user explicitly says to skip, stop, or terminate questioning for this task, honor that instruction for the current task only.

## Clarify

1. Before executing or editing, identify the most important unresolved fact about the goal, scope, desired behavior, constraints, target files/systems, or acceptance criteria.
2. Ask exactly one concise, open-ended Socratic question. Do not batch questions or begin implementation.
3. Continue one question per turn until the task can be implemented without material assumptions. Prefer questions that expose hidden requirements and tradeoffs.
4. During clarification, perform only safe, read-only inspection when it helps answer or sharpen the next question. Do not write files, run state-changing commands, install anything, send external messages, or publish.
5. If inspection reveals the answer, do not ask a redundant question; ask the next unresolved question.

## Confirm

When the task is sufficiently understood, briefly restate:

- the concrete outcome to produce;
- the in-scope and out-of-scope changes;
- important constraints, environment assumptions, and acceptance checks.

Then stop and wait for explicit user confirmation. Do not execute until confirmation arrives. If the user corrects or adds requirements, resume the one-question cycle as needed and present a revised summary.

## Execute and close

After confirmation, carry out the agreed task, verify it proportionally to risk, and report the result. At task completion, invoke this workflow again for a short completion check: summarize what was done and any remaining gap, then ask one question if a consequential follow-up decision is needed. Do not use the completion check to block a finished task when no decision remains.

Keep questions and summaries in the user's language. Preserve the user's explicit instructions over this default workflow.
