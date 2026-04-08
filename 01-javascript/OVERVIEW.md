# Stage 01 - JavaScript for Backend and CLI Engineering

## Stage intent

This stage teaches enough JavaScript to read, write, and debug real backend and CLI code without depending on TypeScript as a crutch. If you come from C or C++, the target is not "learn the entire language." The target is to become operational in the subset of JavaScript that shows up constantly in Node-based tools and AI-agent systems.

## Why JavaScript first

Experienced engineers sometimes want to skip directly to TypeScript. That usually backfires. TypeScript explains intent; JavaScript determines runtime behavior. If you do not understand the language underneath the type layer, later agent bugs will be harder to diagnose:

- mutation leaks across tool boundaries
- truthiness checks drop valid values
- async control flow masks failure paths
- object shape assumptions drift from reality

Learn the runtime language first, then layer types on top.

## Learning outcomes

At stage completion, you should be able to:

- write medium-sized JavaScript modules for CLI and backend use
- read unfamiliar JS code and identify data flow and control flow quickly
- handle arrays, objects, functions, closures, and modules without hesitation
- use promises and `async`/`await` correctly in ordinary application code
- parse files, call HTTP APIs, and transform data with ordinary JS tools
- recognize common "clever" JS patterns and simplify them when needed

## Scope

Focus on practical JavaScript for:

- command-line utilities
- file processing
- API clients
- data transformation
- service glue code
- agent support code

Do not spend time here on DOM APIs, UI frameworks, or browser-specific patterns.

## Topic sequence

### 1. Values, variables, and coercion

Learn:

- primitives and reference-bearing objects
- `const` vs `let`
- equality and identity
- truthiness and falsiness
- string, number, and boolean conversion pitfalls

C/C++ transition note:

JavaScript has fewer compile-time barriers against bad state. You need sharper habits around validation and explicitness.

### 2. Functions, scope, and closures

Learn:

- function declarations and expressions
- arrow functions and their tradeoffs
- lexical scope
- closure behavior
- callback patterns you will still encounter in older code

C/C++ transition note:

Closures are ordinary design tools in JS, not special machinery. Read them as data plus behavior bundled by scope.

### 3. Objects, arrays, and iteration

Learn:

- object literals
- property access and optional chaining
- array iteration patterns
- destructuring
- spread syntax, with caution around copying assumptions

C/C++ transition note:

Object copying is often shallower than it looks. Aliasing bugs are common and subtle.

### 4. Errors and control flow

Learn:

- `throw` and `try/catch`
- when to catch and when to let failures propagate
- distinguishing programmer errors from expected operational errors

This matters later for agent tools, where swallowed errors create unreliable behavior that looks like model failure.

### 5. Modules and code organization

Learn:

- ESM imports and exports
- default vs named exports
- avoiding tangled utility files
- shaping modules around boundaries and responsibilities

### 6. JSON, text, regex, and dates

Learn enough to:

- parse and emit JSON safely
- process line-oriented text
- use regex for bounded parsing tasks
- handle dates without inventing fragile time logic

### 7. Promises and async/await

Learn:

- promise lifecycle
- sequential vs concurrent async work
- error propagation through `await`
- batching and rate-awareness at a basic level

This is a major progression gate. If async reasoning is weak here, Stage 03 and later will stay difficult.

## Recommended study pattern

For each topic:

1. write a small script from scratch
2. read an existing example
3. debug one failure case
4. explain the result in your own words

Do not overread. Build many small scripts instead.

## Common mistakes at this stage

- using array methods without understanding the intermediate shapes
- relying on implicit coercion in boundary logic
- mixing sync and async code without noticing where promises appear
- writing "utility" modules that hide state and make testing harder
- assuming destructuring or spread implies deep copy
- overusing terse syntax before the basic model is stable

## Relationship to later stages

- Stage 02 will add type discipline to the boundaries you define here.
- Stage 03 will assume you can already write asynchronous JS comfortably.
- Stage 04 and Stage 05 rely on clear JS control flow around model calls, tool execution, and result handling.

## Stage gate

Move on only when you can:

- build small JS CLI tools from scratch
- explain the data flow of a medium-sized file without line-by-line guessing
- debug mutation, coercion, and promise-ordering bugs
- choose between loops, array methods, and helper functions for readability
- write async code that is correct before it is clever

## Exit criteria

You are ready for Stage 02 when plain JavaScript feels usable, readable, and debuggable. TypeScript should feel like the next layer of rigor, not a rescue mechanism.
