# Stage 00 - Foundations, Environment, and Mental Model Reset

## Stage intent

This stage is for an experienced programmer, especially one coming from C or C++, who is new to modern JavaScript, TypeScript, and Node.js. The goal is not to relearn programming. The goal is to replace the wrong assumptions that will slow you down when building backend tools, CLIs, and AI-agent systems in the JS/TS ecosystem.

By the end of this stage, you should have a working development environment, a realistic mental model of the runtime, and a repeatable workflow for learning and debugging the rest of the curriculum.

## Why this stage exists

Strong systems programmers often struggle in JS/TS for reasons that have little to do with raw programming ability:

- they expect the runtime to behave like a native process with explicit ownership and predictable blocking behavior
- they treat package tooling as incidental instead of part of the platform
- they underestimate module-system friction, async behavior, and library-driven conventions
- they jump straight into frameworks before understanding the backend and CLI foundations that agent systems depend on

This stage corrects that early.

## What you are training for

The curriculum is biased toward:

- CLI tools
- backend services
- automation scripts
- model API integrations
- tool-calling and agent runtime engineering

It is not primarily a frontend track. You can ignore browser concerns unless a later project explicitly needs them.

## Learning outcomes

At stage completion, you should be able to:

- set up and inspect a Node.js-based project without guessing
- explain how JS execution differs from C/C++ execution
- describe the event loop, task scheduling, and async boundaries at a practical level
- use `node`, package scripts, a debugger, and package metadata comfortably
- identify which C/C++ instincts transfer well and which ones mislead you in JS/TS
- keep a small engineering journal for decisions, failures, and terminology

## Core mental model shifts

### 1. The runtime is the platform

In C/C++, you often own the build chain and can reason close to the machine. In JS/TS, much of day-to-day engineering is about understanding the runtime contract:

- module loading
- package resolution
- event loop behavior
- async APIs
- process environment
- library conventions

Ignoring these is the fastest route to fragile code.

### 2. Tooling is not optional overhead

`package.json`, lockfiles, scripts, formatters, linters, and test runners are not decorations. They are the operational shell around most JS/TS codebases. Learn them early so later agent projects feel normal instead of improvised.

### 3. Asynchrony is structural, not advanced

In many C/C++ environments, asynchronous design is explicit and often isolated. In Node.js, async I/O is default behavior and shapes ordinary application code. You need to understand when work blocks, when it yields, and where errors actually surface.

### 4. Dynamic by default, disciplined by choice

JavaScript lets weak assumptions survive surprisingly long. TypeScript, tests, runtime validation, and clear module boundaries are how professional teams make JS/TS code reliable enough for production agents.

## Topics to cover

### Environment and workflow

- Node.js LTS installation and version management
- `npm`, `pnpm`, or `yarn` basics, with a preference for one package manager per repo
- `package.json`, scripts, dependencies, devDependencies, lockfiles
- editor setup, formatting, linting, and debugger attachment
- using `node`, `npx`, and the REPL

### Runtime and execution

- interpreted vs JIT-compiled expectations
- single-threaded JS execution model versus background I/O and worker escape hatches
- event loop basics
- microtasks vs macrotasks at a conceptual level
- stack traces, uncaught exceptions, and promise rejections

### Code organization

- ESM modules and imports/exports
- file layout for small backend and CLI projects
- using scripts as entry points
- reading package metadata to understand a project quickly

### Transition notes for C/C++

- no header/source split in the same sense
- reference semantics and mutation surprises
- truthiness, `undefined`, `null`, and coercion
- no compile-time safety by default in plain JS
- different performance assumptions and profiling workflow

## Recommended sequence

Work through this stage in order:

1. Install Node.js LTS and one package manager.
2. Create a minimal CLI project and run it directly with `node`.
3. Inspect and edit `package.json` manually.
4. Add formatter and linter scripts.
5. Use the debugger or `console` tracing to inspect execution.
6. Read a few short docs on the event loop and promise scheduling.
7. Write your own notes on "what felt wrong coming from C/C++ and why."

Do not skip the notes. Writing down model mismatches is one of the fastest ways to reduce repeated confusion in later stages.

## Common mistakes at this stage

- treating package tooling as cargo-cult configuration
- memorizing syntax before understanding execution behavior
- assuming `async` means parallel
- assuming filesystem, network, and timers behave like blocking system calls
- copying frontend-oriented starter templates when the target is backend agent work
- using TypeScript before understanding what plain JavaScript actually does at runtime

## How this stage supports later stages

- Stage 01 depends on you being comfortable reading and running JS without friction.
- Stage 02 depends on knowing what problems TypeScript is actually solving.
- Stage 03 depends on your understanding of process, I/O, and async boundaries.
- Stage 04 and beyond depend on backend discipline, not framework hype.

## Stage gate

Move on only when you can do all of the following without tutorial-following:

- initialize a small Node project
- explain the purpose of `package.json` fields you are using
- run code through both `node` and a package script
- describe the difference between synchronous code, promise-based code, and deferred callbacks
- explain at least five C/C++ assumptions that do not map cleanly to JS/TS

## Required deliverables

- one small scratch repo or folder used to test setup and scripts
- a one-page transition note from C/C++ to JS/TS runtime thinking
- a short command cheat sheet for your own future reference

## Exit criteria

You are ready for Stage 01 when the tooling no longer feels mysterious and the runtime no longer feels "magical." You do not need fluency yet. You do need a stable working baseline.
