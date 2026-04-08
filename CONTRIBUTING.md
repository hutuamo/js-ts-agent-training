# Contributing

## Purpose

This repository is a staged training system, not a loose collection of notes. Contributions should improve sequencing, clarity, and practical outcomes for experienced programmers moving from C/C++ into JavaScript, TypeScript, Node.js, and AI-agent engineering.

## Content standard

Prefer content that is:

- practical
- concise
- structured
- backend- and CLI-oriented
- explicit about progression gates

Avoid content that is:

- hype-driven
- framework-chasing
- frontend-heavy unless clearly justified
- vague about prerequisites or expected outcomes

## Audience contract

Write for readers who:

- already know how to program
- may have strong systems or native-language experience
- need help with JS/TS runtime habits, Node workflows, and agent-system engineering patterns

Do not write as if the reader is a beginner to programming in general.

## Preferred document pattern

For stage content, preserve the current structure:

- `OVERVIEW.md` for purpose, sequence, and stage gate
- `EXERCISES.md` for concrete drills
- `PROJECTS.md` for applied builds
- `CHECKLIST.md` for progression decisions

When editing or adding stage material:

- define the target learner clearly
- explain why the stage exists
- include concrete exercises, not only reading
- include a progression gate
- connect the stage to later stages

## Scope guidance

Good additions:

- clearer stage sequencing
- better drills for backend and CLI work
- stronger agent-systems framing
- more realistic failure-mode exercises
- improved project prompts and acceptance criteria

Weak additions:

- long theory dumps without exercises
- frontend framework tutorials unrelated to agent work
- advanced type-system tricks without practical payoff
- generic productivity advice detached from the curriculum

## Style guidance

- keep headings informative and short
- prefer direct statements over motivational language
- use examples that reflect backend, tooling, automation, or agent use cases
- avoid unnecessary jargon
- define progression in terms of demonstrated ability, not time spent

## Editing rules

- preserve the repository structure unless there is a strong reason to change it
- improve existing documents rather than replacing them with unrelated formats
- keep stages coherent enough that a self-learner can proceed without guessing sequence
- if you add a new resource, state where it fits in the stage flow

## Review checklist for contributors

Before submitting documentation changes, confirm:

- [ ] the content is aimed at experienced programmers transitioning into JS/TS
- [ ] the content favors backend, CLI, and agent engineering over frontend work
- [ ] the sequence is explicit
- [ ] exercises and projects are concrete
- [ ] progression gates are visible
- [ ] the tone is practical and concise

## Commit guidance

Use commit messages that describe the instructional change clearly, for example:

- `docs: expand stage 02 TypeScript exercises`
- `docs: tighten progression gates for stage 03`
- `docs: add curriculum map for staged learner flow`
