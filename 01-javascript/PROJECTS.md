# Stage 01 Projects

## Project 1 - File Summarizer CLI

Build a CLI that:

- accepts one or more input files
- parses content into structured data
- computes counts, warnings, and a short summary
- prints either JSON or human-readable output

Suggested input choices:

- log files
- newline-delimited JSON
- simple CSV-like text

What this project trains:

- file handling
- argument parsing
- data transformation
- output formatting

Acceptance criteria:

- handles malformed records explicitly
- separates parsing, transformation, and output logic into distinct functions or modules
- can be run repeatedly on different input files without code changes

## Project 2 - HTTP Client CLI

Build a CLI that:

- calls a public HTTP API
- validates required arguments
- prints a normalized result shape
- handles network errors and non-200 responses clearly

Examples:

- weather lookup
- currency conversion
- GitHub repository metadata fetcher

What this project trains:

- request construction
- JSON parsing
- boundary handling
- user-facing error output

Acceptance criteria:

- no unhandled promise rejections
- response parsing is isolated from display logic
- error messages are specific enough to distinguish network, input, and API-level failures

## Project 3 - Batch Transformer

Build a utility that:

- reads a directory of input files
- transforms each file into a normalized JSON representation
- skips or records failures without losing the whole batch
- emits a summary report at the end

What this project trains:

- iteration over many units of work
- state tracking
- partial-failure handling
- preparing for later tool and agent workflows

Acceptance criteria:

- success and failure counts are reported accurately
- the code distinguishes pure transformation logic from orchestration logic
- rerunning the tool on the same inputs produces stable output

## Recommended build order

1. File Summarizer CLI
2. HTTP Client CLI
3. Batch Transformer
