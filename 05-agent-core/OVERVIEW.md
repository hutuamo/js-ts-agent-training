# Stage 05 - Agent Loops, Tool Orchestration, and State Boundaries

## Stage intent

This stage turns model integration into agent engineering. The goal is not to imitate a general autonomous assistant. The goal is to design small agent systems whose control flow, state transitions, tool usage, and stop conditions are understandable to another engineer.

You should arrive here only after Stage 04 model and tool-calling basics are stable. If basic prompt contracts and structured outputs are still unreliable, adding an agent loop will only hide the problems.

## Why this stage matters

An agent is not just "an LLM with tools." It is a control system that:

- observes context
- selects or is given a next action
- invokes tools or workflow steps
- updates state
- decides whether to continue, branch, ask for help, or stop

If this control system is vague, debugging becomes impossible. A failed run could be caused by prompt wording, tool contracts, bad state, missing context, unbounded looping, or weak stop criteria.

This stage is where you learn to keep those concerns separate.

## Learning outcomes

At stage completion, you should be able to:

- implement a basic agent loop with explicit step boundaries
- define and manage short-term working state across turns
- structure a tool registry with clear contracts and ownership
- decide when planning is useful and when direct execution is simpler
- log agent steps so a failed run can be reconstructed
- impose guardrails such as max steps, validation checks, and human escalation points
- explain why a workflow should or should not be represented as an autonomous agent

## Topic sequence

### 1. Agent loop anatomy

Learn:

- observe, decide, act, update, stop
- explicit loop state
- max-step and max-cost controls
- what belongs inside the loop versus outside it

Keep the loop visible and boring. Hidden orchestration logic creates fragile systems.

### 2. Tool abstraction and execution control

Learn:

- tool registration patterns
- argument schemas and runtime validation
- result normalization
- side-effect classification
- idempotent versus risky actions

Treat tools as backend interfaces, not as prompt decorations.

### 3. State and memory boundaries

Learn:

- current request state
- scratchpad or working notes
- persisted conversation or session state
- what should never be stored automatically

At this stage, focus on bounded state, not long-term memory systems. Stage 06 will handle retrieval and memory in more depth.

### 4. Planning versus direct execution

Learn:

- explicit plans for multi-step tasks
- when to skip planning and act directly
- checking plans against tool availability
- keeping plans inspectable instead of mystical

Do not overuse planning for simple tasks. Planning should reduce risk or increase clarity.

### 5. Observability and debugging

Learn:

- step-level logs
- trace identifiers
- tool-call records
- state snapshots that are useful but not excessive
- post-run summaries

If you cannot reconstruct the agent's decisions, you do not control the system.

### 6. Recovery and guardrails

Learn:

- retries at the correct layer
- invalid-tool-request handling
- recovery from partial progress
- escalation to deterministic workflows or humans
- refusing unsafe or unsupported actions

### 7. Basic evaluation for agent behavior

Learn:

- scenario-based tests
- step-count expectations
- tool-use expectations
- failure categorization by stage in the loop

This prepares you for Stage 07 production eval suites.

## Recommended study pattern

For each agent design:

1. define the task boundary
2. list the available tools and their side effects
3. define the loop state explicitly
4. add stop conditions before adding extra capabilities
5. run representative tasks and save traces
6. review failures by layer: prompt, planning, tool selection, tool execution, state update, stop logic

## Common mistakes at this stage

- calling something an agent when it is really a deterministic workflow
- letting the model invent tool semantics that code never defined
- mixing transient reasoning state with durable user state
- allowing infinite or poorly bounded loops
- hiding control flow inside prompt instructions instead of code
- adding memory before tool and state boundaries are stable
- logging too little to debug or too much to operate safely

## Relationship to other stages

- Stage 04 gave you prompt, structured-output, and tool-calling foundations.
- Stage 06 will extend these systems with retrieval, memory, and workflow orchestration choices.
- Stage 07 will add stronger validation, evals, observability, and operational hardening.
- Stage 08 expects you to justify your architecture, not just present a working demo.

## Required deliverables

- one manual or semi-manual agent loop implementation
- one tool registry or equivalent explicit tool layer
- one trace log or run-record format that lets you inspect a failed execution
- one short design note explaining what state exists, who owns it, and when the loop stops

## Stage gate

Move on only when you can:

- explain your loop control flow without hand-waving
- justify why each tool exists and how it is validated
- show where state is stored and why
- stop the agent predictably under success, failure, and ambiguity
- compare your agent design against a simpler workflow and defend the choice

## Exit criteria

You are ready for Stage 06 when your agent code reads like backend orchestration rather than prompt theater. The loop should be explicit, bounded, and inspectable.
