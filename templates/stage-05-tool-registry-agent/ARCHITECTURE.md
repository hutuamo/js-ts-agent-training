# Architecture - Stage 05 Tool Registry Agent

## Core idea

The system should read like backend orchestration, not prompt theater.

## Core components

1. input/task boundary
2. agent loop
3. state model
4. tool registry
5. trace/log layer
6. stop and escalation rules

## Boundary rules

- tools must validate arguments before execution
- loop state must be explicit, not hidden in prompt text
- traces must record actions and outcomes at step boundaries
- tool results should be normalized before re-entering the loop
- stop conditions should exist in code, not only in model instructions

## Recommended flow

1. accept a bounded task
2. initialize state
3. select next action
4. validate and run tool if needed
5. update state and trace
6. stop, continue, or escalate

## Failure categories to plan for

- invalid tool selection
- invalid tool arguments
- loop exceeds step budget
- ambiguous task requiring handoff
- partial progress with no safe next step
