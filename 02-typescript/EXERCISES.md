# Stage 02 Exercises

## Exercise policy

Every exercise should make a boundary safer or clearer. Avoid abstract type puzzles that do not improve runtime code.

## Exercise 1 - Convert a JS utility to strict TypeScript

Objective: feel the compiler pressure on real code.

Tasks:

- take one Stage 01 utility
- add a `tsconfig.json` with strict settings
- convert the utility to TypeScript
- remove implicit `any` and weak return types

Progression check:

- the typed version is easier to review than the JS version

## Exercise 2 - Model a CLI contract

Objective: express command inputs and outputs cleanly.

Tasks:

- define types for parsed CLI arguments
- define a result type for success and failure cases
- type the main execution path end to end

Progression check:

- you can point to where invalid states were reduced by the type design

## Exercise 3 - Union and narrowing drill

Objective: make conditional logic explicit and safe.

Tasks:

- create a discriminated union for three command outcomes
- write code that handles all cases
- add an impossible branch check or equivalent exhaustiveness pattern

Progression check:

- you can explain how the compiler helps detect missed cases

## Exercise 4 - Replace `any` with `unknown`

Objective: stop bypassing type safety at boundaries.

Tasks:

- take one function that accepts loose input
- change the boundary type to `unknown`
- add a narrowing function or schema validation
- compare the readability before and after

Progression check:

- you can explain why `unknown` is safer than `any` for external data

## Exercise 5 - Generic helper drill

Objective: practice useful generics without overengineering.

Tasks:

- write a generic `mapValues` or equivalent transform helper
- write a generic result wrapper for command execution or API calls
- avoid adding constraints you do not need

Progression check:

- the generic form is still understandable by a teammate seeing it for the first time

## Exercise 6 - Runtime validation boundary

Objective: separate compile-time belief from runtime truth.

Tasks:

- read JSON from a file or API
- validate it against a schema
- convert the validated data into internal typed objects
- reject invalid data with clear errors

Progression check:

- no direct type assertions are used in place of validation at the input boundary

## Exercise 7 - Read a typed codebase slice

Objective: learn to interpret real-world TS usage.

Tasks:

- inspect a small TS module from a backend tool or SDK
- list the exported public types
- identify where runtime validation happens, if it happens
- identify one place where the types improve design clarity and one place where they add noise

Progression check:

- you can critique the type design instead of only copying it

## Required minimum

Complete at least:

- Exercises 1, 2, 3, and 6
- one conversion of an existing JS utility to strict TS
- one written critique of a real TS module
