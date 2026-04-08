# Stage 07 - Production Reliability, Evals, and Operational Hardening

## Stage intent

This stage turns working AI systems into operable software. The goal is not "enterprise readiness" in the abstract. The goal is to build systems whose behavior under failure, drift, bad inputs, and operational stress can be described and verified.

By this point you should already have model integration, agent orchestration, and retrieval or workflow patterns. Now you need to prove that the system is reliable enough to trust with repeated use.

## Why this stage matters

Prototype AI systems often fail in ways that ordinary backend tests do not catch:

- prompt changes silently regress behavior
- tool outputs drift or change shape
- retrieval quality degrades as the corpus grows
- rate limits, timeouts, and provider changes surface intermittently
- logs are too weak to debug real failures
- secrets, prompts, and user data leak into traces or artifacts

This stage is about reducing surprise. Reliability requires contracts, test strategy, eval coverage, observability, and operational discipline.

## Learning outcomes

At stage completion, you should be able to:

- validate every external boundary in an AI-backed backend or CLI system
- build regression tests and eval suites for prompts, tools, retrieval, and workflows
- add logs, traces, and identifiers that make failures diagnosable
- handle rate limits, retries, backoff, and fallbacks deliberately
- manage prompt, schema, and tool version changes safely
- reason about security, secrets, and data handling in agent systems
- prepare a service or worker for repeatable deployment and operations

## Topic sequence

### 1. Validation and contracts everywhere

Learn:

- request validation
- tool argument and result validation
- model output validation
- retrieval result expectations
- config validation at startup

Production systems fail less when ambiguity is removed at boundaries.

### 2. Observability

Learn:

- structured logs
- request or run identifiers
- per-step traces
- latency and error metrics
- redaction and safe logging practices

You need enough detail to debug without turning telemetry into a liability.

### 3. Retries, backoff, and fallbacks

Learn:

- which failures are retryable
- backoff policies
- timeout design
- circuit-breaker style thinking where appropriate
- degraded-mode behavior

Not every failure should trigger another model call.

### 4. Evals and regression harnesses

Learn:

- golden task sets
- prompt regression checks
- retrieval evaluation sets
- tool-use scenario tests
- pass/fail criteria that are useful, not vague

Evals are how you keep the system stable while iterating.

### 5. Versioning and change management

Learn:

- prompt versions
- schema versions
- tool contract changes
- migration of stored artifacts or memory formats
- comparing runs across revisions

### 6. Security and data handling

Learn:

- secret management
- least-privilege access for tools
- prompt injection awareness where relevant
- output handling for unsafe or sensitive content
- retention and deletion of logs, traces, and memory artifacts

### 7. Deployment and runtime operations

Learn:

- service versus worker versus CLI deployment shape
- health checks and startup validation
- configuration differences across environments
- rollout and rollback thinking
- operator-facing documentation

## Recommended study pattern

For each existing Stage 04-06 project you harden:

1. map every external boundary
2. add validation at each boundary
3. add traceable logging with redaction rules
4. define retry, timeout, and fallback behavior
5. assemble a regression and eval set
6. run failure drills before claiming the system is ready

## Common mistakes at this stage

- treating evals as optional because "the demos still work"
- logging prompts and user data without retention or redaction rules
- adding retries without classifying failure types
- changing prompts or schemas without regression comparison
- assuming provider SDK updates are behaviorally neutral
- shipping retrieval-backed systems without a retrieval eval set
- deploying a service with no clear operator documentation

## Relationship to other stages

- Stage 04 established model boundaries and structured output validation.
- Stage 05 established inspectable agent loops and tool orchestration.
- Stage 06 established retrieval, memory, and workflow structure.
- Stage 07 hardens all of them into systems that can be operated and tested.
- Stage 08 capstones should reflect this discipline in both implementation and documentation.

## Required deliverables

- one hardened project from Stage 04, 05, or 06
- one regression or eval suite covering realistic cases
- one observability plan covering logs, traces, identifiers, and redaction
- one operational note covering deployment shape, failure handling, and rollback assumptions

## Stage gate

Move on only when you can:

- explain how the system is validated at every external boundary
- run a regression or eval suite that catches real behavior changes
- diagnose failures from logs and traces without guessing blindly
- justify retry, fallback, and timeout policies
- describe security and data-handling assumptions explicitly

## Exit criteria

You are ready for Stage 08 when your system is no longer a prototype held together by manual testing. It should be possible to change it, test it, operate it, and explain it under failure.
