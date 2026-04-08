# Stage 08 Exercises

## Exercise policy

These exercises are for shaping the capstone before implementation drifts. Do them before expanding scope.

## Exercise 1 - Problem statement and boundaries

Objective: define a capstone that is narrow enough to execute well.

Tasks:

- write the user or operator problem in one page or less
- define what the system will do
- define what it will explicitly not do
- list the main external dependencies and data sources

Progression check:

- the project scope is specific enough that acceptance criteria can be written

## Exercise 2 - Architecture sketch

Objective: make the system shape visible early.

Tasks:

- sketch the major components
- identify model boundaries, tool boundaries, and retrieval or memory boundaries
- identify deterministic workflow steps
- identify where validation occurs

Progression check:

- another engineer could critique the design before any code exists

## Exercise 3 - Acceptance criteria pack

Objective: define what "done" means before implementation grows.

Tasks:

- choose representative user scenarios
- define expected outputs or success properties
- define failure behavior for unsupported or unsafe cases
- identify what evidence is needed to claim the project works

Progression check:

- the criteria are concrete enough to support an eval suite

## Exercise 4 - Risk register

Objective: identify the ways the project can become weak or misleading.

Tasks:

- list likely reliability, data, and scope risks
- list at least one prompt-level risk, one tool-level risk, and one operational risk
- decide which risks must be mitigated before completion
- decide which risks are acceptable but must be documented

Progression check:

- the project has explicit non-goals and known tradeoffs

## Exercise 5 - Eval and demo plan

Objective: avoid building a capstone that only works in one happy-path demo.

Tasks:

- define a small eval set of representative scenarios
- define what artifacts or logs will be shown in the demo
- include at least one failure or limitation case
- define how results will be recorded

Progression check:

- the project can be presented honestly without hiding weak cases

## Exercise 6 - Documentation outline

Objective: make explanation part of the engineering work.

Tasks:

- outline the README
- outline the architecture note
- outline the setup guide
- outline the limitations section

Progression check:

- the project can be handed to another engineer without relying on verbal explanation alone

## Required minimum

Complete all six exercises before declaring capstone scope stable.
