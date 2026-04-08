# Template - Stage 05 Tool Registry Agent

## Purpose

This template is a starter blueprint for a small agent with a visible loop and a controlled tool registry.

The point is not to build a general assistant. The point is to make tool use, state, and stop conditions explicit.

## Good use cases

- bounded research helper
- local repo inspection helper
- operations summary assistant
- small multi-step workflow with one or two dynamic choices

## Build goals

- define a small tool registry with validated arguments
- keep loop state explicit and inspectable
- add trace logging for each step
- enforce stop conditions and escalation paths

## Suggested file tree

```text
stage-05-tool-registry-agent/
  README.md
  ARCHITECTURE.md
  TODO.md
  src/
    agent.ts
    loop.ts
    state.ts
    tools/
      index.ts
      tool-a.ts
      tool-b.ts
    trace.ts
    stop-rules.ts
```

## Minimum acceptance criteria

- at least two tools with explicit contracts
- one loop with step count and termination reason
- one saved trace format
- one invalid-tool-request path
- one human handoff or refusal path

## Extension ideas

- planning versus direct-execution comparison
- side-effect classification for tools
- trace viewer or trace summarizer
- scenario-based loop evaluation
