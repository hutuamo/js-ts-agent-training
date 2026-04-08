# Architecture - Stage 04 Structured Output CLI

## Core idea

Keep the system split into five obvious parts:

1. CLI input handling
2. configuration loading
3. prompt construction
4. model invocation
5. schema validation and output handling

## Boundary rules

- CLI parsing should not know provider-specific response details.
- Prompt text should not contain business logic that belongs in code.
- The model wrapper should normalize provider responses.
- Output is not accepted until schema validation succeeds.

## Recommended flow

1. Parse CLI input.
2. Load and validate configuration.
3. Construct prompt from input.
4. Call model through a small wrapper.
5. Validate the response against schema.
6. Emit structured result or controlled error.

## Failure categories to plan for

- missing config
- provider/network failure
- invalid or partial model output
- schema mismatch
- unsupported input shape
