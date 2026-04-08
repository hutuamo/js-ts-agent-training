# Stage 05 Exercises

## Exercise policy

Every exercise should include at least one saved trace or run log. Agent behavior must be inspectable while it is still small.

## Exercise 1 - Manual agent loop

Objective: make the control flow explicit.

Tasks:

- implement a simple observe-decide-act-update loop
- track step count and termination reason
- support a maximum number of steps
- print or persist a summary of what happened

Progression check:

- another engineer can tell where the loop begins, updates state, and stops

## Exercise 2 - Tool registry drill

Objective: stop treating tool calls as ad hoc helper functions.

Tasks:

- define two or three tools with clear names and argument shapes
- validate arguments before execution
- normalize tool results into a consistent structure
- record tool invocation metadata in the trace

Progression check:

- the loop can reason about tools without depending on tool-specific implementation details

## Exercise 3 - Working state design

Objective: separate active task state from durable session data.

Tasks:

- define a small state object for the current run
- identify which fields are ephemeral and which are safe to persist
- update the state after each step
- reject or clear stale state when it should not carry forward

Progression check:

- you can explain exactly what state survives between turns and why

## Exercise 4 - Planning versus direct execution comparison

Objective: decide whether planning adds value.

Tasks:

- pick one multi-step task
- implement a direct-execution version
- implement a version with an explicit plan step
- compare complexity, failure rate, and trace readability
- write a short note on which version you would keep

Progression check:

- you can justify planning with evidence instead of instinct

## Exercise 5 - Loop guardrails drill

Objective: ensure the loop fails safely.

Tasks:

- add a max-step limit
- add handling for invalid tool requests
- add a refusal or escalation path for unsupported tasks
- add one path that returns partial progress instead of silently failing

Progression check:

- you can show how the loop terminates under at least three different failure conditions

## Exercise 6 - Trace review session

Objective: learn to debug agent runs after the fact.

Tasks:

- run several representative tasks
- save the traces
- classify failures by loop phase
- identify one failure caused by prompt wording and one caused by orchestration logic
- propose one concrete fix for each

Progression check:

- you can debug from traces without rerunning the exact scenario immediately

## Exercise 7 - Human handoff boundary

Objective: avoid pretending automation is always the right answer.

Tasks:

- define one task class where the agent should stop and ask for confirmation
- define what context should be handed to the human
- make the handoff explicit in state and logs
- test the handoff on at least two scenarios

Progression check:

- the handoff preserves useful context without hiding what the agent already did

## Required minimum

Complete at least:

- Exercises 1, 2, 5, and 6
- one explicit planning comparison
- one example of a task that should become a workflow or human handoff instead of a loop
