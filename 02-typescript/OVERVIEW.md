# Stage 02 - TypeScript as an Engineering Constraint

## Stage intent

This stage turns your JavaScript into maintainable, reviewable backend code. The goal is not to exercise every advanced type feature. The goal is to use TypeScript to make boundaries explicit, remove common classes of mistakes, and support larger Node and agent codebases.

For an experienced C/C++ programmer, TypeScript will feel familiar in one sense: it rewards precise contracts. It will feel unfamiliar in another sense: the type system is structural, optional at runtime, and easy to misuse if you chase cleverness instead of clarity.

## What TypeScript is for in this curriculum

Use TypeScript to improve:

- function and module contracts
- request and response modeling
- tool input and output boundaries
- configuration safety
- refactoring confidence
- code review clarity

Do not use TypeScript to:

- hide weak runtime understanding
- encode every invariant into unreadable generic machinery
- assume runtime data is safe just because the compiler is satisfied

## Learning outcomes

At stage completion, you should be able to:

- configure a strict TypeScript project and explain key compiler options
- model ordinary application data with type aliases, interfaces, unions, and generics
- narrow unknown values safely before using them
- design typed boundaries for CLI commands, APIs, and tool execution
- separate compile-time guarantees from runtime validation
- refactor a JS module into TS without creating type noise

## Topic sequence

### 1. Compiler setup and strictness

Learn:

- `tsconfig.json`
- module and target settings at a practical level
- strict mode and why it matters
- emitting JS versus type-check-only workflows

C/C++ transition note:

Unlike a native compiler, the TS compiler does not make runtime invalid states disappear. It improves reasoning; it does not replace validation.

### 2. Everyday types

Learn:

- annotations and inference
- object types
- arrays and records
- optional properties
- readonly intent where useful

Aim for code that a teammate can read quickly.

### 3. Unions, narrowing, and guards

Learn:

- discriminated unions
- `unknown` versus `any`
- type guards
- narrowing through control flow

This is core preparation for model outputs, tool results, and structured workflow state.

### 4. Function and module contracts

Learn:

- typed parameters and return types
- async return types
- exported public types
- minimizing leakage of implementation details

### 5. Generics for ordinary engineering

Learn:

- reusable container and helper patterns
- generic functions over collections
- simple generic registries

Avoid type-level stunts. If the generic design is harder to read than the code it supports, simplify it.

### 6. Runtime validation alignment

Learn:

- why TypeScript cannot trust external input
- schema-based validation at boundaries
- aligning parsed runtime data with internal types

This is mandatory for agent systems, where model outputs and tool inputs are external data.

## Common mistakes at this stage

- using `any` to get past confusion instead of fixing the model
- overmodeling trivial code with excessive generics
- confusing optional properties with absent validation
- asserting types instead of narrowing them
- letting inferred types become too broad at module boundaries
- assuming JSON from a file, API, or model already matches the declared type

## Recommended study pattern

For each topic:

1. start from working JavaScript
2. add types to the boundary first
3. tighten the compiler settings
4. remove unsafe assumptions
5. add runtime validation where data enters the system

This order keeps the type system grounded in actual runtime code.

## Relationship to later stages

- Stage 03 will depend on typed process, config, HTTP, and I/O boundaries.
- Stage 04 and Stage 05 rely heavily on typed tool definitions and validated model responses.
- Production agent work becomes much easier when your TS boundaries are clear and modestly strict.

## Stage gate

Move on only when you can:

- configure and explain a strict TS project
- choose between `type`, `interface`, union, and generic patterns without cargo culting
- model external data as untrusted until validated
- write typed application code that is clearer than the JS version, not noisier

## Exit criteria

You are ready for Stage 03 when TypeScript feels like a design tool for backend software, not just a compiler that complains.
