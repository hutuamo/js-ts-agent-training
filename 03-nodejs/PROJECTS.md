# Stage 03 Projects

## Project 1 - Multi-Command Utility

Build a Node.js CLI with multiple subcommands.

Suggested commands:

- inspect files
- summarize JSON or logs
- call an HTTP endpoint
- run a local automation task

Required capabilities:

- argument parsing
- config loading
- structured error handling
- clean separation between command handlers and shared helpers

What this project trains:

- CLI architecture
- operational discipline
- reusable backend utility structure

Acceptance criteria:

- each command has a clear contract
- failures return useful exit behavior
- logs and user output are separated intentionally

## Project 2 - Resilient API Integration Service

Build a small service or worker-style script that integrates with one external API.

Requirements:

- typed configuration
- retries and timeouts
- normalized output
- logging around attempts and failures
- support for partial failure handling if multiple requests are processed

What this project trains:

- durable I/O behavior
- service-style control flow
- preparation for model-provider integration

Acceptance criteria:

- transport and application errors are distinguished
- timeout and retry policies are explicit
- the service can be reasoned about from logs

## Project 3 - Local Automation Suite

Build a small suite of scripts that wrap local tools or processes.

Examples:

- repo inspection helpers
- code search and summary workflow
- file conversion pipeline
- batch command runner with structured result output

What this project trains:

- child-process handling
- job orchestration
- integrating external capabilities into a controlled Node shell

Acceptance criteria:

- command execution results are structured
- partial failures are reported without collapsing unrelated work
- rerunning the suite is predictable

## Recommended build order

1. Multi-Command Utility
2. Resilient API Integration Service
3. Local Automation Suite
