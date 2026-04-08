# Stage 04 Exercises

## Exercise policy

Every exercise in this stage should produce saved examples or notes. You are building the raw material for later evals and production hardening. Do not rely on memory.

## Exercise 1 - Minimal model call wrapper

Objective: treat the LLM provider like any other external service.

Tasks:

- create a small wrapper that sends one prompt and returns normalized text output
- load credentials from configuration instead of hardcoding them
- log request metadata that is safe to keep
- distinguish transport failure, provider rejection, and application-level parse failure

Progression check:

- the rest of your code does not depend on raw provider response objects

## Exercise 2 - Prompt contract drill

Objective: write prompts as engineering contracts rather than vague instructions.

Tasks:

- choose one concrete backend task such as summarization, extraction, or classification
- write a prompt that defines the task, constraints, and output expectations
- run multiple representative inputs through it
- record where the prompt fails or becomes ambiguous
- revise the prompt with minimal wording changes

Progression check:

- you can explain which changes improved reliability and which were unnecessary

## Exercise 3 - Structured JSON output with validation

Objective: ensure model output is not trusted by default.

Tasks:

- define a target JSON shape for a practical task
- ask the model to produce that shape
- validate the response at runtime
- reject or repair invalid responses explicitly
- record at least three invalid or imperfect cases

Progression check:

- downstream logic only receives validated data

## Exercise 4 - Streaming response drill

Objective: learn when streaming helps and when it complicates correctness.

Tasks:

- implement one streamed response path and one buffered response path
- capture partial chunks without assuming they form valid final output
- compare perceived latency and implementation complexity
- document which path you would choose for a CLI and why

Progression check:

- you can state the exact point where a streamed response becomes safe to consume

## Exercise 5 - Single tool-calling roundtrip

Objective: add one controlled action boundary.

Tasks:

- define one tool with a narrow purpose
- expose its name, description, and argument schema clearly
- validate tool arguments before execution
- normalize the tool result before returning it to the model
- stop after one tool execution and one follow-up model response

Progression check:

- invalid tool arguments fail as validation errors, not as hidden runtime behavior

## Exercise 6 - Cost and latency measurement drill

Objective: stop treating model usage as free and instantaneous.

Tasks:

- measure latency across several requests for one task
- compare at least two prompt variants or model choices if available
- record input size, output size, and observed cost indicators
- write a short note on what you would optimize first

Progression check:

- you can justify a latency or cost tradeoff with actual measurements

## Exercise 7 - Failure taxonomy notebook

Objective: learn how AI integration actually fails.

Collect concrete examples of:

- invalid JSON
- incomplete output
- wrong tool selection
- hallucinated fields or assumptions
- provider timeout or rate limit
- prompt ambiguity causing inconsistent behavior

For each example, write:

- the input
- the observed failure
- the boundary where it should be caught
- the mitigation you chose

Progression check:

- you can separate model mistakes from wrapper bugs and schema bugs

## Required minimum

Complete at least:

- Exercises 1, 3, 5, and 7
- one streaming comparison
- one saved set of prompt examples that you can reuse in Stage 07 eval work
