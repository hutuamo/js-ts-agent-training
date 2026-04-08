# Stage 02 Projects

## Project 1 - Typed Task Runner

Build a small CLI task runner with:

- typed command definitions
- typed configuration input
- discriminated result types
- clear error messages

Examples:

- file cleanup tasks
- report generation tasks
- local automation tasks

What this project trains:

- boundary typing
- command dispatch structure
- typed result handling

Acceptance criteria:

- the main command flow is type-checked end to end
- invalid configuration is handled deliberately
- the type structure helps explain the design

## Project 2 - Typed API Client

Build a small SDK-style module for one HTTP API.

Requirements:

- typed request parameters
- typed normalized response shapes
- explicit error model
- no blind trust in remote JSON

What this project trains:

- interface design
- schema alignment
- making service integrations maintainable

Acceptance criteria:

- response parsing is separate from transport logic
- runtime validation exists at the API boundary
- public exported types are small and clear

## Project 3 - Typed Tool Registry

Build a tool registry suitable as a precursor to agent systems.

Requirements:

- each tool has a name, description, input contract, and execution function
- tool execution returns a typed result
- invalid input is rejected before tool logic runs

What this project trains:

- contract-first design
- preparation for model tool calling
- generic patterns with restraint

Acceptance criteria:

- adding a new tool follows a predictable pattern
- the registry API is readable without advanced TS knowledge
- runtime validation and TypeScript types agree on the expected shape

## Recommended build order

1. Typed Task Runner
2. Typed API Client
3. Typed Tool Registry
