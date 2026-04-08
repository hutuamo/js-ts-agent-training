# Stage 03 Exercises

## Exercise policy

All exercises in this stage should include at least one failure-mode check. The baseline is not "works once." The baseline is "behaves predictably under common failure."

## Exercise 1 - File walker

Objective: handle local filesystem work cleanly.

Tasks:

- walk a directory tree
- filter files by extension or predicate
- emit a summary of counts and total size
- skip unreadable files with a clear warning

Progression check:

- the script distinguishes traversal logic from reporting logic

## Exercise 2 - Config loader

Objective: stop scattering configuration assumptions.

Tasks:

- load configuration from environment variables and optional file input
- validate required fields
- provide clear startup errors
- keep secrets out of normal logs

Progression check:

- startup fails fast when required config is missing or invalid

## Exercise 3 - Retry and timeout wrapper

Objective: treat external I/O as unreliable by default.

Tasks:

- wrap an async operation with timeout support
- add bounded retries with backoff
- define which errors are retryable
- log attempts and final failure

Progression check:

- you can explain why some failures should not be retried

## Exercise 4 - HTTP client hardening drill

Objective: prepare for model and tool API integrations.

Tasks:

- call an HTTP endpoint
- handle non-2xx responses
- handle malformed JSON
- handle timeout and network failure cases
- normalize the output shape for downstream consumers

Progression check:

- downstream code does not need to know transport-level details

## Exercise 5 - Stream processing drill

Objective: handle larger input without assuming eager loading is always fine.

Tasks:

- process a large text file or simulated large input stream
- count lines or extract records incrementally
- compare a whole-file approach with a streaming approach
- write a short note on the tradeoff

Progression check:

- you can explain when streaming is justified and when it adds unnecessary complexity

## Exercise 6 - Child process wrapper

Objective: integrate external tools safely.

Tasks:

- invoke an external command
- capture stdout and stderr
- handle non-zero exit codes
- surface a structured result to the caller

Progression check:

- the wrapper does not blur command failure and wrapper failure together

## Exercise 7 - Concurrency control drill

Objective: reason about multiple async tasks at once.

Tasks:

- process a list of async jobs
- implement a fixed concurrency limit
- record success and failure counts
- compare runtime and behavior with sequential execution

Progression check:

- you can explain why unbounded concurrency is often the wrong default

## Required minimum

Complete at least:

- Exercises 2, 3, 4, and 7
- one child-process integration
- one file-processing exercise with explicit failure handling
