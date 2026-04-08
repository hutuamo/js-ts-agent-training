# Stage 05 Projects

## Project 1 - Research Helper Agent

Build a small agent that can answer bounded research questions using a few controlled tools.

Suggested tools:

- local note lookup
- web or document fetch wrapper if available in your environment
- summarization or extraction helper
- citation formatter

Required capabilities:

- explicit agent loop
- tool registry with validated arguments
- per-step trace output
- final answer that separates evidence from synthesis

What this project trains:

- bounded research orchestration
- tool-use inspection
- preparation for retrieval-heavy work in Stage 06

Acceptance criteria:

- the agent stops after a clear completion rule
- traces show which tools were called and why
- unsupported or ambiguous questions are rejected or escalated explicitly

## Project 2 - Multi-Step Local Workflow Agent

Build an agent that coordinates local tools to complete a backend or CLI task.

Examples:

- inspect logs and produce an incident summary
- gather repo metadata and produce a review checklist
- run a local analysis pipeline with intermediate validation

Required capabilities:

- bounded steps
- structured intermediate state
- at least one side-effect-aware tool classification
- trace logs with step outcomes

What this project trains:

- local tool orchestration
- state management across steps
- deciding where agent behavior should stop and deterministic workflow should begin

Acceptance criteria:

- the system does not hide side effects behind vague tool descriptions
- state updates are visible and reviewable
- the final output can be traced back to concrete tool results

## Project 3 - Tool-Using Assistant with Reviewable Traces

Build an assistant for a small operational task that emphasizes inspectability.

Examples:

- support ticket triage assistant
- repo maintenance helper
- operations summary assistant

Required capabilities:

- short-lived session state
- trace persistence or reviewable run records
- invalid-tool-request handling
- explicit stop and escalation rules

What this project trains:

- review-friendly agent design
- operational debugging habits
- foundation for Stage 07 eval and hardening work

Acceptance criteria:

- a reviewer can reconstruct the run from logs or trace artifacts
- the assistant does not continue indefinitely on unclear tasks
- failure outcomes are categorized instead of collapsed into one generic error

## Recommended build order

1. Research Helper Agent
2. Multi-Step Local Workflow Agent
3. Tool-Using Assistant with Reviewable Traces
