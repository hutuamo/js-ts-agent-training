# Architecture - Stage 07 Eval Harness

## Core idea

An eval harness should make change measurable, not mystical.

## Core components

1. scenario definitions
2. execution runner
3. assertion rules or acceptance checks
4. results storage
5. comparison and reporting layer

## Boundary rules

- scenarios should represent real tasks or failure classes
- assertions should be explicit enough that another engineer can review them
- results should be comparable over time
- evaluation logic should be separate from the system under test

## Recommended flow

1. define representative cases
2. run the target system
3. apply assertions or acceptance checks
4. record outputs and results
5. compare with prior runs when relevant

## Failure categories to plan for

- prompt regressions
- invalid structured output
- retrieval misses
- tool-use mistakes
- workflow step failures
- operator-visible behavior drift
