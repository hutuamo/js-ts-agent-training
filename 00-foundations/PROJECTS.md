# Stage 00 Projects

## Project policy for this stage

Keep the work deliberately small. Stage 00 projects exist to establish habits, not to show feature depth.

## Project 1 - Developer Environment Bring-Up Pack

Build a small folder or repo that contains:

- a minimal CLI entry point
- a `package.json` with at least two scripts
- one formatter or linter configuration
- a short `NOTES.md` documenting how to run and debug the project

What this project teaches:

- manual project setup
- script-driven workflow
- how much metadata surrounds even a tiny JS/TS project

Acceptance criteria:

- another engineer could clone the folder and run the main script by following your notes
- your setup is understandable without a framework generator

## Project 2 - Runtime Behavior Notebook

Create a small collection of tiny scripts that demonstrate:

- coercion surprises
- object mutation and aliasing
- promise scheduling
- timer ordering
- thrown errors vs rejected promises

For each script, include:

- your prediction
- actual observed behavior
- a brief explanation

What this project teaches:

- practical runtime reasoning
- how to test assumptions before relying on them

Acceptance criteria:

- each script is under 30 lines
- every example includes a written explanation
- at least two examples compare the behavior to a C/C++ expectation

## Project 3 - C/C++ to JS/TS Transition Memo

Write a concise internal-style memo aimed at a peer who knows C/C++ but is new to JS/TS backend work.

Required sections:

- what transfers cleanly
- what does not transfer cleanly
- common setup pitfalls
- the minimum tooling baseline
- what to learn next and why

What this project teaches:

- conceptual compression
- communication discipline
- preparation for later code reviews and architecture notes

Acceptance criteria:

- 1 to 2 pages
- concrete examples instead of general advice
- clearly oriented toward backend/CLI/agent development

## Recommended submission order

1. Developer Environment Bring-Up Pack
2. Runtime Behavior Notebook
3. C/C++ to JS/TS Transition Memo
