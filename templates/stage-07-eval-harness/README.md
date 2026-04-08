# Template - Stage 07 Eval Harness

## Purpose

This template is a starter blueprint for a small evaluation and regression harness around an existing AI-backed tool, workflow, or agent.

The purpose is not to build a leaderboard. The purpose is to make behavior change visible.

## Good use cases

- prompt regression checks
- structured-output validity checks
- retrieval quality checks
- tool-use scenario checks
- workflow-level pass/fail cases

## Build goals

- define a repeatable scenario set
- define acceptance criteria clearly
- record results across revisions
- make regressions visible before demo or deployment

## Suggested file tree

```text
stage-07-eval-harness/
  README.md
  ARCHITECTURE.md
  TODO.md
  eval/
    cases/
    results/
  src/
    runner.ts
    assertions.ts
    report.ts
```

## Minimum acceptance criteria

- one reusable scenario set
- one explicit pass/fail rule per case type
- one result-recording format
- one example of a real weak case or regression
- one short note on how to use the harness before releases or prompt changes

## Extension ideas

- compare results across prompt versions
- compare retrieval or tool behavior across revisions
- add simple summary reporting
- integrate with CI later if useful
