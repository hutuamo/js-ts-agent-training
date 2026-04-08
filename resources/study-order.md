# Study Order

## Purpose

This file gives a practical sequence for using the curriculum. It is designed for a self-learner who already knows how to program and wants to move efficiently into JavaScript/TypeScript AI agent engineering.

## Core rule

Do not consume the repository as a library of notes.
Use it as a staged build sequence.

For each stage:
1. Read `OVERVIEW.md`.
2. Read the matching sections in `reading-map.md`.
3. Complete the required exercises.
4. Build one project.
5. Use the checklist to decide whether to advance.

## Recommended primary path

### Phase 1 - Language and runtime foundation
1. Stage 00 - Foundations
2. Stage 01 - JavaScript
3. Stage 02 - TypeScript
4. Stage 03 - Node.js

Do not skip this phase. Weakness here causes confusion everywhere else.

### Phase 2 - Model-backed software
5. Stage 04 - LLM Basics
6. Stage 05 - Agent Core

Only start Stage 05 when Stage 04 outputs, validation, and tool-calling boundaries are stable.

### Phase 3 - Grounding and system structure
7. Stage 06 - RAG, Memory, and Workflows
8. Stage 07 - Production

You should harden a real project here, not invent an entirely new one unless necessary.

### Phase 4 - Demonstration
9. Stage 08 - Capstones

Use the capstone to prove judgment, not to maximize scope.

## Suggested pacing

### 12-week path
- Weeks 1-4: Stages 00-03
- Weeks 5-6: Stage 04
- Weeks 7-8: Stage 05
- Weeks 9-10: Stage 06
- Week 11: Stage 07
- Week 12: Stage 08

### 16-week path
- Weeks 1-5: Stages 00-03
- Weeks 6-7: Stage 04
- Weeks 8-9: Stage 05
- Weeks 10-11: Stage 06
- Weeks 12-13: Stage 07
- Weeks 14-16: Stage 08

## Best way to study each week

Use a simple rhythm:
- 2 reading sessions
- 2 or 3 coding sessions
- 1 debugging/refactoring session
- 1 short review note

## What to do when stuck

If a stage feels weak:
- repeat the exercises with a different small problem
- build a narrower project instead of a larger one
- write down the exact failure mode
- go back to the reading map for that stage only

Do not jump ahead to agents when the current problem is really about JS runtime, TS boundaries, or Node I/O.

## Anti-patterns

Avoid these common mistakes:
- reading Stage 05 before building a real Stage 04 tool-calling path
- learning through frameworks before hand-building one small system yourself
- treating RAG as mandatory for every project
- trying to build a “general assistant” as your first serious project
- using capstones to cover weak fundamentals instead of proving them

## Completion heuristic

You are ready to move forward when:
- you can explain the current stage in your own words
- you can debug common failures without panic
- you have executable artifacts from the stage
- the checklist feels honestly passed, not negotiated
