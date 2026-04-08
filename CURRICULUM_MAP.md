# Curriculum Map

## Purpose

This file defines the intended flow of the curriculum so a self-learner can move through it without guessing sequence, scope, or readiness.

The repository is designed for an experienced programmer, especially someone coming from C or C++, who wants to become effective at backend, CLI, and AI-agent engineering in JavaScript and TypeScript.

## Audience assumptions

You are likely already comfortable with:

- functions, data structures, and debugging
- command-line workflows
- building and reading non-trivial code
- reasoning about performance and failure

You are likely not yet comfortable with:

- JavaScript runtime behavior
- TypeScript’s structural typing model
- Node.js process and I/O conventions
- model APIs, tool calling, and agent workflows

## Stage sequence

### Stage 00 - Foundations

Primary outcome:

- establish environment, tooling, and correct runtime mental models

Do not skip because:

- most later confusion comes from wrong assumptions about modules, async behavior, and package tooling

Advance when:

- Node workflow and runtime basics no longer feel opaque

### Stage 01 - JavaScript

Primary outcome:

- become productive in plain JavaScript for backend and CLI tasks

Do not skip because:

- TypeScript cannot compensate for weak JavaScript runtime understanding

Advance when:

- you can build and debug small JS tools confidently

### Stage 02 - TypeScript

Primary outcome:

- use types to clarify boundaries and reduce avoidable mistakes

Do not skip because:

- agent and tool code benefits heavily from explicit contracts

Advance when:

- types improve clarity instead of adding noise

### Stage 03 - Node.js

Primary outcome:

- build robust tools and services around filesystem, process, and network I/O

Do not skip because:

- agent systems are operational software, not just prompt wrappers

Advance when:

- you can build a reliable CLI or backend utility with real failure handling

### Stage 04 - LLM Basics

Primary outcome:

- integrate model APIs, structured outputs, and tool-calling fundamentals

Depends most on:

- Stage 02 typing discipline
- Stage 03 I/O and HTTP discipline

### Stage 05 - Agent Core

Primary outcome:

- build loops, tool abstractions, and stateful agent workflows

Depends most on:

- validated boundaries
- Node process and orchestration knowledge

### Stage 06 - RAG, Memory, and Workflows

Primary outcome:

- build retrieval and memory-backed systems without confusing workflow logic with agent autonomy

### Stage 07 - Production

Primary outcome:

- improve reliability, observability, evaluation, and operational safety

### Stage 08 - Capstones

Primary outcome:

- ship portfolio-grade end-to-end systems

## Suggested pacing

### Fast track

- 10 to 12 weeks
- suitable if you already have strong backend discipline and can study consistently

### Standard track

- 3 to 5 months
- suitable for most self-learners balancing work with study

### Deep track

- 6 months or longer
- suitable if you want stronger project polish, deeper reading, and repeated project rewrites

## Required progression rule

Do not advance just because you finished the reading.

Advance only when all three are true:

- you completed the required exercises
- you built the stage project or equivalent
- you can explain common failure cases without consulting notes

## Recommended weekly pattern

- 2 to 3 short study sessions for reading and note consolidation
- 2 to 4 build sessions for exercises and projects
- 1 review session for debugging, refactoring, and writing stage notes

## Minimum output per stage

Each completed stage should leave you with:

- executable code or scripts
- short written notes on confusing concepts
- one or more artifacts you can revisit later
- a pass/fail decision against the stage checklist

## Practical advice for C/C++ engineers

- resist the urge to map every concept directly onto native-language equivalents
- learn the platform conventions before optimizing them away
- prefer boring, explicit code over dense JS idioms
- treat external JSON, model output, and process output as untrusted input
- keep backend and CLI work central until the platform feels natural

## Recommended order of use inside each stage

1. Read `OVERVIEW.md`.
2. Complete `EXERCISES.md` in order.
3. Build one project from `PROJECTS.md`.
4. Use `CHECKLIST.md` to decide whether to advance.

If a stage still feels shaky, repeat it with a different project instead of skimming ahead.
