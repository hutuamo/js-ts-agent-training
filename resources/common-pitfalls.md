# Common Pitfalls

## Purpose

This file collects the most common failure modes for experienced programmers moving into JavaScript/TypeScript backend and AI agent engineering.

## 1. Treating JavaScript as if it were just a slower C++

Problem:
- You keep expecting runtime behavior, object structure, and typing discipline to behave like a static native-language environment.

What goes wrong:
- confusion around closures, `this`, prototypes, coercion, and async behavior
- frustration that leads to overcomplicated abstractions too early

Better approach:
- learn the runtime on its own terms first
- prefer explicit code over clever JS idioms

## 2. Trying to use TypeScript to erase runtime uncertainty

Problem:
- You expect TypeScript types to make external JSON, model output, and config magically trustworthy.

What goes wrong:
- invalid data passes through because it was asserted, not validated
- code looks typed but fails at runtime

Better approach:
- use TypeScript for design clarity
- use runtime validation at every external boundary

## 3. Learning frameworks before learning the runtime

Problem:
- You reach for heavy frameworks before you can write or debug a plain Node script.

What goes wrong:
- you cannot tell whether a bug belongs to your code, the framework, or the platform
- abstractions feel magical instead of useful

Better approach:
- hand-build one small version first
- adopt frameworks only after you can name the problem they solve

## 4. Building agent loops before model boundaries are stable

Problem:
- You jump to autonomous systems before you can get structured output and tool calling to behave predictably.

What goes wrong:
- failures blur together
- you cannot tell whether the issue is prompt design, output parsing, tool validation, or orchestration

Better approach:
- make Stage 04 reliable before entering Stage 05

## 5. Using prompts to encode rules that belong in code

Problem:
- Business logic drifts into long prompt text.

What goes wrong:
- behavior becomes harder to test and refactor
- prompt changes create invisible regressions

Better approach:
- keep prompts focused on interpretation or generation tasks
- keep deterministic rules in ordinary code

## 6. Treating RAG as mandatory

Problem:
- You assume every AI system needs embeddings, chunking, and retrieval.

What goes wrong:
- complexity grows without improving the task
- weak workflows are hidden behind retrieval jargon

Better approach:
- first ask whether the task really needs external grounded context
- if not, keep the system simpler

## 7. Calling something a memory system when it is really a log dump

Problem:
- Everything gets stored because it might be useful later.

What goes wrong:
- stale, irrelevant, or risky data accumulates
- state becomes harder to reason about

Better approach:
- define memory classes explicitly: ephemeral, session, durable, forbidden
- add retention and deletion rules

## 8. Ignoring operational failure in Node.js

Problem:
- Scripts work on the happy path but have weak handling for bad config, network errors, rate limits, or child-process failures.

What goes wrong:
- the first non-ideal environment breaks the system
- “AI failures” are blamed for ordinary engineering mistakes

Better approach:
- add timeouts, retries, logging, startup validation, and structured errors early

## 9. Over-scoping the capstone

Problem:
- You try to build a universal assistant instead of one strong system.

What goes wrong:
- no part of the project is reliable enough to be impressive
- architecture becomes hard to explain

Better approach:
- choose one narrow workflow or domain
- prove depth, not breadth

## 10. Confusing a demo with a system

Problem:
- One successful run is treated as evidence of readiness.

What goes wrong:
- regressions are missed
- failure modes stay invisible
- maintenance becomes guesswork

Better approach:
- save examples
- build eval cases
- test failure behavior, not just success behavior

## 11. Logging too little or too much

Problem:
- Either you have no trace of what happened, or you log prompts, secrets, and sensitive data carelessly.

What goes wrong:
- debugging is impossible, or observability becomes a liability

Better approach:
- log boundaries, identifiers, decisions, and failure classes
- redact secrets and sensitive payloads

## 12. Using autonomy where workflow would be better

Problem:
- You use a free-form loop for a task that is really a fixed sequence with approvals.

What goes wrong:
- control is weaker than necessary
- reliability is worse than it needs to be

Better approach:
- choose workflows when the task is repeatable and structure helps
- reserve agent loops for places where dynamic choice truly adds value
