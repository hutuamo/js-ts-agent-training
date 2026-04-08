# Chapter Mapping

## Purpose

This file maps major books and reference materials to the stages in this curriculum.

It is written for an experienced programmer, especially someone coming from C or C++, who wants to learn JavaScript/TypeScript backend and AI agent engineering without getting lost in frontend-heavy or low-value detours.

The goal is not total coverage. The goal is high-yield reading tied to real implementation work.

---

## 1. *JavaScript: The Definitive Guide (7th ed.)*

### Use in this curriculum
This is the main book for **Stage 01**, with small supporting value for **Stage 00** and **Stage 03**.

### Read carefully for Stage 01
Prioritize chapters covering:
- JavaScript language basics
- expressions and operators
- statements and control flow
- objects
- arrays
- functions
- classes only at a practical level
- modules
- standard library essentials
- asynchronous programming, promises, and async/await
- iterators and generators at a practical level

### Read selectively
Use selective reading for:
- regular expressions
- errors and exception handling
- meta-programming features
- JavaScript tools and package ecosystem sections

### Skim or defer
Usually defer browser-heavy material unless your capstone needs it:
- DOM-heavy chapters
- browser event/UI APIs
- client-side graphics and browser-specific APIs

### What to extract into practice
After each major section, implement one small CLI or backend utility. Do not let this remain a reading-only book.

### C/C++ transition note
Pay extra attention to:
- closures
- prototype-based object behavior
- reference semantics
- coercion and truthiness
- async execution model

These are the areas most likely to create false confidence if you map JS too directly onto C++.

---

## 2. *Programming TypeScript*

### Use in this curriculum
Main book for **Stage 02**.

### Read carefully for Stage 02
Prioritize:
- the role of TypeScript over JavaScript
- basic types and inference
- functions and callable shapes
- object types
- unions and intersections
- generics
- compiler configuration and strictness
- declaration files at a practical level

### Read selectively
Useful, but not urgent on first pass:
- advanced generic patterns
- library authoring concerns
- more abstract type-level techniques

### Skim or defer
Defer anything that turns into type-system sport rather than application engineering.

### What to extract into practice
Map book material into:
- typed CLI inputs
- typed API request/response boundaries
- runtime validation around external data
- one typed tool registry

### C/C++ transition note
The most important lesson is this:

> TypeScript improves design clarity, but it does not remove runtime uncertainty.

If the book section tempts you to replace runtime checks with assertions, slow down and validate instead.

---

## 3. *Effective TypeScript*

### Use in this curriculum
Best used alongside **late Stage 02**, then revisited during **Stage 03**, **Stage 04**, and **Stage 07**.

### Best timing
- First pass: after you already wrote some TS
- Second pass: while refining architecture and reliability

### Focus areas
Prioritize items related to:
- avoiding `any`
- narrowing and soundness
- designing maintainable public types
- distinguishing compile-time safety from runtime truth
- improving readability instead of cleverness
- safer refactoring and configuration patterns

### Use style
Do not read this like a novel. Use it as:
- a code review companion
- a pitfall checklist
- a “why is this TS design awkward?” troubleshooting book

### What to extract into practice
Apply it to:
- strict TS refactors
- tool and schema boundaries
- cleaning up inferred types that became too broad
- making project code easier to review

---

## 4. *TypeScript Handbook*

### Use in this curriculum
Reference source for **Stage 02**, with continuing value later.

### Best sections for this path
Prioritize:
- Everyday Types
- Narrowing
- More on Functions
- Object Types
- Generics
- Modules
- Utility Types
- tsconfig reference entries as needed

### Use style
Treat it as the authoritative syntax and feature reference, not your only teacher.

### What to extract into practice
Use it when:
- a book explanation is fuzzy
- you need precise compiler behavior
- you need a concrete example of a language feature

---

## 5. *Node.js Design Patterns*

### Use in this curriculum
Main engineering book for **Stage 03**, with supporting value for **Stage 07**.

### Read carefully for Stage 03
Prioritize chapters related to:
- asynchronous control flow
- modules and project structure
- streams
- event-driven patterns
- process and service structure
- integration patterns for external systems
- resilience and maintainability concerns

### Revisit for Stage 07
Return to sections relevant to:
- reliability
- system structure
- scaling patterns
- operational discipline

### What to extract into practice
Apply directly to:
- CLI architecture
- service wrappers
- retries and timeout wrappers
- stream handling
- child process orchestration
- reusable Node modules

### C/C++ transition note
This book is useful because it helps bridge from “I know systems” to “I know Node systems.”

---

## 6. Node.js Official Documentation

### Use in this curriculum
Primary reference for **Stage 00**, **Stage 03**, and parts of **Stage 07**.

### Prioritize
- `fs`
- `path`
- `process`
- `stream`
- `child_process`
- `http` / `fetch`
- environment variables and process lifecycle

### Use style
Read on demand, tied to exercises and projects. Avoid trying to read the docs end to end.

---

## 7. MDN JavaScript Documentation

### Use in this curriculum
Reference for **Stage 00** and **Stage 01**.

### Best use
- quick clarification of language behavior
- standard library lookup
- examples for syntax you partially remember

### Warning
Do not let MDN pull you into frontend/browser APIs unless your project actually needs them.

---

## 8. Provider SDK / API Documentation

### Use in this curriculum
Primary external reading for **Stage 04**, then referenced in **Stages 05-07**.

### Prioritize
- authentication and configuration
- request and response shapes
- structured output support
- tool calling
- streaming behavior
- error handling and rate limits
- model selection and cost basics

### Use style
Pick one provider path first. Avoid trying to compare many providers before you have one stable implementation.

---

## 9. Retrieval / Embedding Documentation

### Use in this curriculum
Selective reading for **Stage 06**.

### Prioritize
- ingestion APIs
- indexing setup
- query and filtering behavior
- metadata support
- operational constraints

### Warning
Do not let documentation reading replace corpus inspection and retrieval evaluation.

---

## 10. *Designing Data-Intensive Applications*

### Use in this curriculum
Selective long-term systems reading for **Stage 07** and stronger capstones in **Stage 08**.

### Best use
Read selectively for:
- data flow thinking
- logs and event streams
- storage and indexing tradeoffs
- consistency and operational reasoning

### Warning
This is not a first-pass build book for this curriculum. Use it to deepen system thinking after you have working projects.

---

## 11. *Designing Machine Learning Systems*

### Use in this curriculum
Selective support for **Stage 07** and **Stage 08**.

### Best use
Read for:
- evaluation thinking
- production AI system concerns
- monitoring and operational quality
- feedback and iteration loops

### Warning
Do not let it replace actually hardening one of your own projects.

---

## Recommended reading order for this curriculum

### Minimum effective sequence
1. *JavaScript: The Definitive Guide (7th ed.)*
2. *Programming TypeScript*
3. *Effective TypeScript* (parallel or second pass)
4. *Node.js Design Patterns*
5. one provider SDK / API documentation path
6. selective retrieval and production readings as needed

### Best pairing strategy
- Stage 01: JS book + MDN
- Stage 02: Programming TypeScript + Handbook + Effective TypeScript
- Stage 03: Node.js Design Patterns + Node docs
- Stage 04: provider docs + your own saved examples
- Stage 05: your own traces + agent design notes
- Stage 06: retrieval docs + your own retrieval experiments
- Stage 07: production readings + your hardened project
- Stage 08: capstone docs + architecture review materials

---

## Final advice

A good rule for this entire repository is:

> Read until the next useful implementation becomes clear, then stop reading and build.

For this path, code, traces, notes, and project artifacts matter more than finishing every chapter of every book.
