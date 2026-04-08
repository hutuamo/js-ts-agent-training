# Stage 04 Projects

## Project 1 - Single-Turn Assistant CLI

Build a CLI that performs one practical task with an LLM.

Suitable examples:

- summarize operational notes
- classify issue reports
- rewrite rough text into a strict internal format
- extract action items from meeting notes

Required capabilities:

- typed configuration
- normalized model wrapper
- safe logging
- clear separation between prompt construction, model call, and output handling

What this project trains:

- basic provider integration
- prompt-as-contract thinking
- backend-first LLM usage

Acceptance criteria:

- the CLI can be run repeatedly with predictable I/O behavior
- transport failures and invalid responses are reported clearly
- prompt text is not mixed into unrelated business logic

## Project 2 - Structured Extraction Tool

Build a tool that converts unstructured input into validated structured data.

Examples:

- extract TODOs, owners, and due dates from notes
- extract incident fields from log or support text
- convert rough research notes into a typed outline

Required capabilities:

- schema-defined output
- runtime validation
- explicit invalid-response handling
- saved input and output examples for regression comparison

What this project trains:

- structured output reliability
- schema-first design
- the difference between model generation and accepted system state

Acceptance criteria:

- only validated output is emitted to downstream consumers
- invalid output is either rejected or repaired by a documented path
- examples are saved in a way that can later support regression tests

## Project 3 - Typed Tool-Calling Assistant

Build a small assistant that can call one or two tools to complete a request.

Suggested tools:

- local file lookup
- a simple calculator or parser
- one HTTP-backed lookup
- a small internal data reader

Required capabilities:

- tool registry or equivalent explicit tool definition
- argument validation before execution
- normalized tool result shape
- one controlled loop with a stop condition

What this project trains:

- model-to-tool handoff
- action boundary design
- preparation for Stage 05 agent loops

Acceptance criteria:

- tools cannot be called with unchecked arguments
- tool execution and model reasoning remain visibly separate in the code
- the assistant can explain failure cleanly when the model requests an invalid action

## Recommended build order

1. Single-Turn Assistant CLI
2. Structured Extraction Tool
3. Typed Tool-Calling Assistant
