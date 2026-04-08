# Stage 04 - LLM Integration, Structured Output, and Tool Calling

## Stage intent

This stage moves from general Node.js backend engineering into model-backed software. The goal is not to build a chatbot demo. The goal is to learn how to integrate an LLM as one unreliable subsystem inside a larger, testable, typed backend or CLI workflow.

For an experienced C/C++ engineer, the main adjustment is that model behavior is probabilistic even when the rest of your system is deterministic. Reliability comes from contracts, validation, retries, tool boundaries, and careful control of state, not from assuming the model will "just follow instructions."

## Why this stage matters

Before this stage, you have the Node.js skills needed to call external services safely. Now you need to apply those skills to model APIs, which add new failure modes:

- malformed or partial structured output
- prompt sensitivity and response variance
- token-window limits
- latency and cost tradeoffs
- tool invocation requests that may be incomplete or invalid
- provider-specific request and response conventions

If you do not learn these boundaries early, later "agent" systems will be difficult to debug because the model, tool layer, and orchestration logic will all be mixed together.

## Learning outcomes

At stage completion, you should be able to:

- integrate a model API into a Node.js CLI or backend utility
- structure prompts and message history for repeatable single-turn and short multi-turn tasks
- require structured output and validate it before downstream use
- stream responses when appropriate and handle partial output safely
- implement one full tool-calling roundtrip with validation on both request and result
- measure the practical impact of model choice, latency, and token usage
- explain which parts of the system are deterministic and which are not

## Topic sequence

### 1. Model API contracts

Learn:

- request and response shapes
- auth and secret handling
- provider SDKs versus direct HTTP calls
- model selection as an engineering choice, not a branding choice

You are learning how to treat the model provider as an external dependency with explicit contracts and failure handling.

### 2. Messages, prompts, and task framing

Learn:

- system, developer, and user instruction roles where applicable
- how to constrain scope and define output requirements
- how to separate durable instructions from per-request context
- how to reduce prompt ambiguity without writing prompt novels

Good prompting at this stage means writing clear task specifications for software behavior.

### 3. Structured output and runtime validation

Learn:

- JSON-oriented outputs
- schema-first thinking
- validating output before execution or storage
- handling "almost correct" model responses without silently accepting them

This is the first major reliability boundary in AI-backed software.

### 4. Streaming and incremental handling

Learn:

- when streaming improves UX or pipeline latency
- when it complicates validation and should be avoided
- buffering strategy for partial content
- end-of-stream checks before accepting output as complete

Streaming is useful, but only if the receiver logic is designed for incomplete data.

### 5. Tool calling fundamentals

Learn:

- how the model requests a tool
- validating tool name and arguments
- executing the tool in controlled code
- feeding the tool result back to the model
- deciding when to stop instead of looping

Tool calling is where the system stops being a text generator and starts acting like a controlled coordinator.

### 6. Cost, latency, and operational tradeoffs

Learn:

- token budgeting
- latency sources
- choosing smaller or larger models deliberately
- retries that do not multiply cost blindly
- logging enough context to debug without leaking secrets or large prompts unnecessarily

### 7. Evaluation at the integration level

Learn:

- golden examples for prompt and structured-output tasks
- tracking failure classes
- comparing prompt revisions on the same task set
- identifying when a bug is in the prompt, parser, schema, or tool layer

This prepares you for the deeper eval and production work in Stage 07.

## Recommended study pattern

For each new model-backed feature:

1. define the input contract and required output shape
2. build a happy-path call with minimal prompt text
3. add runtime validation around the response
4. record at least three realistic failure modes
5. decide whether retries, fallback, or rejection is correct
6. save examples so you can regression-test later

Do not move directly from "prompt works once" to "feature is done."

## Common mistakes at this stage

- treating the provider SDK as if it guarantees valid output
- passing model output directly into business logic without validation
- letting prompts encode business rules that should exist in code
- streaming output into downstream logic before completeness checks
- tool-calling without argument validation or tool result normalization
- retrying every failure class even when the request itself is bad
- adding multi-turn memory before single-turn contracts are stable

## Relationship to other stages

- Stage 03 provided the backend discipline needed for HTTP, config, logging, and retries.
- Stage 05 will build agent loops on top of the prompt, tool-calling, and state boundaries from this stage.
- Stage 06 will extend the context model with retrieval and memory once you already know how to validate model interactions.
- Stage 07 will harden these integrations with evals, observability, and production constraints.

## Required deliverables

- one single-turn CLI or backend task that calls an LLM API
- one structured-output task with runtime validation
- one tool-calling roundtrip with typed arguments and normalized tool results
- a short note describing at least five failure modes you observed and how you handled them

## Stage gate

Move on only when you can:

- explain the full request and response lifecycle for one model call
- validate structured output before using it
- implement one controlled tool-calling cycle without hidden side effects
- describe the tradeoffs between buffering and streaming for your use case
- show logs or saved examples that let you debug prompt or schema regressions

## Exit criteria

You are ready for Stage 05 when you can treat the model as a bounded subsystem with explicit contracts. You do not need a sophisticated agent yet. You do need model integration that is deliberate, inspectable, and hard to misuse.
