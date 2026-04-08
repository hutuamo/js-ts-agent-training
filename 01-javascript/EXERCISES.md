# Stage 01 Exercises

## Exercise policy

Keep the exercises backend-oriented. Most should be solvable in one sitting. Prefer file, process, and API tasks over algorithm puzzles.

## Exercise 1 - Data-shape warmup

Objective: build fluency with arrays, objects, and transformations.

Tasks:

- take a small JSON file containing an array of records
- filter by one condition
- group by one field
- compute summary counts
- output a new JSON report

Progression check:

- you can explain the shape of the data before and after each transform

## Exercise 2 - Coercion and comparison audit

Objective: stop making accidental truthiness and equality bugs.

Tasks:

- write small examples for `==` vs `===`
- test empty string, zero, `null`, `undefined`, empty arrays, and empty objects in conditionals
- write a short rule set for your future code style

Progression check:

- you can justify when a loose check is unacceptable in backend code

## Exercise 3 - Closure and state drill

Objective: understand captured state well enough to recognize bugs.

Tasks:

- write a counter factory
- write a logger decorator that adds timing or labels
- write one intentionally broken example where shared mutable state leaks across calls

Progression check:

- you can explain what data each closure retains and why

## Exercise 4 - Text and JSON processor

Objective: practice everyday file and transform work.

Tasks:

- read a line-oriented text file
- parse each line into structured records
- reject malformed lines
- emit JSON output plus a short error report

Progression check:

- malformed input does not crash the entire script unless you deliberately choose fail-fast behavior

## Exercise 5 - Error-handling drill

Objective: distinguish normal failure from programmer mistakes.

Tasks:

- write a function that validates input and throws on invalid programmer usage
- write a function that returns a controlled operational error for bad external data
- compare the two cases in a short note

Progression check:

- you can explain when a caught error should be logged, wrapped, rethrown, or allowed to terminate execution

## Exercise 6 - Async sequencing drill

Objective: reason about promise control flow in ordinary code.

Tasks:

- run three async tasks sequentially
- run the same tasks concurrently
- add one failing task and inspect how the failure propagates
- add timing output to compare the two strategies

Progression check:

- you can explain the difference between concurrency and ordering in your own words

## Exercise 7 - Read unfamiliar code

Objective: transition from writing toy scripts to reading real code.

Tasks:

- pick a small JS CLI or API client module
- identify entry points, pure transforms, and side-effecting functions
- draw a short flow of how input reaches output

Progression check:

- you can explain the module without narrating every line

## Required minimum

Complete at least:

- Exercises 1, 4, 5, and 6
- one written coercion rule set
- one read-through of unfamiliar JS code
