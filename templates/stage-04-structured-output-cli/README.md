# Template - Stage 04 Structured Output CLI

## Purpose

This template is a starter blueprint for a CLI that sends one bounded task to a model and expects validated structured output.

It is intentionally documentation-first. You should build the implementation yourself as part of the training.

## Good use cases

- extract tasks from meeting notes
- classify issue reports into a strict schema
- turn rough research notes into a structured summary
- normalize operational text into typed fields

## Build goals

- keep the model wrapper small
- define one explicit schema for accepted output
- validate before writing or printing final results
- save examples for later regression use

## Suggested file tree

```text
stage-04-structured-output-cli/
  README.md
  ARCHITECTURE.md
  TODO.md
  src/
    cli.ts
    config.ts
    model.ts
    prompt.ts
    schema.ts
    run.ts
  examples/
    inputs/
    outputs/
```

## Minimum acceptance criteria

- one command-line entry point
- one model-backed task
- one validated output schema
- one invalid-output handling path
- saved examples for at least three representative inputs

## Extension ideas

- add buffered versus streaming comparison
- add prompt revision notes
- add latency and token observation logs
- add a small regression runner over saved examples
