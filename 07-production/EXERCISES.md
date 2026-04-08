# Stage 07 Exercises

## Exercise policy

Use an existing Stage 04, 05, or 06 project as the base whenever possible. Production hardening is most useful when applied to real systems you already understand.

## Exercise 1 - Boundary validation audit

Objective: find every place bad data can enter or leave the system.

Tasks:

- list config, model, tool, retrieval, and user-input boundaries
- define the validation expected at each boundary
- identify at least one boundary that is currently under-validated
- add or specify a fix

Progression check:

- you can explain what invalid data is blocked at each layer

## Exercise 2 - Structured logging and trace IDs

Objective: make runs diagnosable.

Tasks:

- add structured logs for key events
- attach request or run identifiers
- distinguish normal output from diagnostics
- define redaction rules for secrets and sensitive content

Progression check:

- a failed run can be reconstructed from the logs you keep

## Exercise 3 - Retry and timeout policy review

Objective: stop using generic resilience patterns blindly.

Tasks:

- list the external calls your system makes
- classify which failures are retryable
- add or document timeout behavior
- define one degraded-mode or fail-fast path
- test at least one rate-limit or timeout scenario

Progression check:

- you can justify why each retry exists

## Exercise 4 - Prompt and schema regression set

Objective: catch behavior drift before it reaches users.

Tasks:

- select representative inputs
- define expected output properties or failure behavior
- run the cases before and after a prompt or schema change
- record deltas and decide whether they are acceptable

Progression check:

- you have at least one repeatable set that exposes regressions

## Exercise 5 - Retrieval or tool-use eval drill

Objective: evaluate the parts that ordinary unit tests miss.

Tasks:

- choose retrieval quality or tool-use behavior as the target
- build a small labeled scenario set
- define pass conditions
- record at least one surprising miss or regression
- propose a fix at the correct layer

Progression check:

- the eval points to a concrete system weakness instead of a vague quality impression

## Exercise 6 - Incident-style failure review

Objective: practice postmortem thinking before production incidents happen.

Tasks:

- choose one real or simulated failure
- write a short incident note with timeline, impact, and root cause
- identify what telemetry was missing
- identify what guardrail would have reduced the impact

Progression check:

- the review distinguishes root cause from symptom

## Exercise 7 - Deployment and operator note

Objective: treat the system like something another engineer may have to run.

Tasks:

- define the runtime shape: CLI, service, worker, or hybrid
- document required configuration
- document startup checks and health signals
- document rollback or safe-disable steps

Progression check:

- another engineer could operate the system from your notes

## Required minimum

Complete at least:

- Exercises 1, 2, 3, and 4
- one retrieval or tool-use eval drill
- one incident-style review tied to a real project
