# Stage 03 - Node.js Engineering for Tools, Services, and Agent Runtimes

## Stage intent

This stage is where JS and TS become operational backend engineering. You will learn how Node.js code behaves as a process that reads files, performs network I/O, spawns commands, handles failure, and coordinates asynchronous work. This is the stage that turns language knowledge into infrastructure for AI-agent systems.

For a C/C++-experienced engineer, the challenge is not low-level capability. The challenge is learning the Node idioms that make backend code reliable instead of fragile.

## Why this stage matters for agent engineering

Agents are not just prompts around API calls. Real agent systems need:

- filesystem access
- process control
- HTTP integration
- timeouts and retries
- validated config
- logs and traces
- concurrency discipline
- deterministic wrappers around nondeterministic models

Those are Node engineering problems before they are "AI" problems.

## Learning outcomes

At stage completion, you should be able to:

- build robust CLI and backend utilities on Node.js
- handle filesystem, environment, and process interactions deliberately
- structure HTTP clients with retries, timeouts, and clear failures
- use streams and buffering appropriately for common backend cases
- manage concurrency and task orchestration without accidental races
- package and run a small tool or service predictably

## Topic sequence

### 1. Filesystem and paths

Learn:

- reading and writing files
- directory traversal
- path normalization and cross-platform safety
- deciding when to load whole files versus stream them

This matters for log processing, local corpora ingestion, tool outputs, and artifact generation.

### 2. Process and environment

Learn:

- `process.argv`
- environment variable handling
- exit codes
- stdin, stdout, stderr
- signal awareness at a practical level

CLI and service reliability both start here.

### 3. HTTP, fetch, and boundary failure

Learn:

- request construction
- headers, auth, and payload handling
- retries and backoff
- timeouts and cancellation
- distinguishing transport failures from application-level failures

This is direct preparation for model-provider SDKs and API-backed tools.

### 4. Streams, buffers, and large-output handling

Learn:

- when streams help
- when they complicate code unnecessarily
- piping and transform patterns
- handling large output without naive memory assumptions

### 5. Child processes and automation

Learn:

- running external commands
- capturing output
- handling non-zero exits
- wrapping local tools safely

Many practical agent systems use external binaries, code search tools, package managers, or local scripts.

### 6. Logging, config, and operational hygiene

Learn:

- structured logging basics
- configuration loading and validation
- fail-fast vs degrade-gracefully decisions
- separating user-facing output from diagnostic output

### 7. Packaging and project structure

Learn:

- script layout
- reusable modules versus one-off scripts
- package entry points
- when to build a library, CLI, or service

## Common mistakes at this stage

- no timeout handling on network calls
- assuming retries are always safe
- mixing logging with user-facing output streams
- reading large files eagerly when streaming would be simpler and safer
- shelling out without handling stderr, exit codes, or argument safety
- writing "agent" code before the surrounding I/O and failure model is stable

## Recommended study pattern

For each subsystem:

1. build a minimal happy-path version
2. inject one realistic failure mode
3. add logging and error handling
4. document what assumptions your code now depends on

The failure-path work is not optional. This stage is mainly about operational behavior.

## Relationship to later stages

- Stage 04 will add model APIs on top of the HTTP and config discipline learned here.
- Stage 05 will build agent loops on top of the tool and process abstractions from this stage.
- Stage 06 and Stage 07 will assume you can handle files, services, and orchestration without runtime confusion.

## Stage gate

Move on only when you can:

- build a multi-command CLI or small backend service in Node.js
- explain how it handles config, logs, retries, and failures
- reason about sequential, concurrent, and externally spawned work
- structure code so side effects are visible and boundaries are testable

## Exit criteria

You are ready for Stage 04 when Node.js feels like an engineering environment you can control, not just a runtime you can execute code inside.
