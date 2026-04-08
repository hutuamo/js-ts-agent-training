# Stage 07 Projects

## Project 1 - Harden an Existing Agent or Workflow

Take a project from Stage 04, 05, or 06 and harden it for repeated use.

Required capabilities:

- boundary validation
- structured logging and run IDs
- explicit retry and timeout policy
- failure categorization
- operator-facing documentation

What this project trains:

- turning prototypes into maintainable systems
- disciplined failure handling
- cross-stage integration of reliability practices

Acceptance criteria:

- key failure paths are visible in logs and documentation
- inputs and outputs are validated at external boundaries
- another engineer can explain the runtime behavior by reading the project and notes

## Project 2 - Eval Suite and Benchmark Pack

Build a reusable eval harness for one AI-backed project.

Required capabilities:

- representative scenario set
- expected outcomes or acceptance properties
- prompt, retrieval, or tool-use coverage
- result recording across revisions

What this project trains:

- regression discipline
- measurable improvement work
- safe iteration on AI system behavior

Acceptance criteria:

- the suite can catch at least one real regression or weak case
- results are stored in a way that supports comparison over time
- pass/fail rules are explicit enough for another engineer to use

## Project 3 - Minimal Deployable Service or Worker

Package one project as something that can be run repeatedly outside your development shell.

Examples:

- a small API service
- a scheduled worker
- a command runner with deployment notes

Required capabilities:

- startup validation
- environment-specific configuration handling
- operational documentation
- safe shutdown or failure behavior

What this project trains:

- deployment shape decisions
- operational readiness
- translating local development work into repeatable execution

Acceptance criteria:

- startup fails clearly on invalid configuration
- runtime logs are useful and safe
- a basic rollout and rollback story exists

## Recommended build order

1. Harden an Existing Agent or Workflow
2. Eval Suite and Benchmark Pack
3. Minimal Deployable Service or Worker
