# Reading Map

## Purpose

This file maps books, official documentation, and selected study materials to the curriculum stages in this repository.

The intended reader already knows how to program, likely has strong systems-language habits from C or C++, and wants to become effective at JavaScript/TypeScript backend and AI agent engineering.

The goal is not to read everything. The goal is to read enough at each stage to support building.

## Reading principles

- Prefer one main source per layer, then build.
- Use official docs as reference, not as the only learning method.
- Read in service of a stage project whenever possible.
- If a book chapter does not affect how you build or debug, defer it.

## Stage 00 - Foundations

### Primary reading
- Node.js official documentation: getting started, modules, process basics
- MDN JavaScript guide: overview-level refreshers

### Why it matters
At this stage, you are replacing incorrect assumptions about runtime, packaging, modules, and tooling.

### C/C++ transition focus
- runtime versus compiled-binary expectations
- package manager and ecosystem habits
- async model differences
- modules and project layout conventions

### Read just enough to:
- install the toolchain confidently
- run and inspect a small CLI
- explain the event loop at a practical level

## Stage 01 - JavaScript

### Primary reading
- *JavaScript: The Definitive Guide (7th ed.)* — main structured source
- MDN docs — lookup and clarification while building
- *You Don't Know JS Yet* — optional selective reading for language mechanics

### Focus areas
- values and coercion
- functions, closures, scope
- objects and arrays
- prototypes at a practical level
- modules
- errors
- promises and async/await

### What to skim
- browser-heavy sections not relevant to backend/CLI work

### C/C++ transition focus
- dynamic typing and runtime coercion
- object model versus class-first instincts
- closures and functional patterns
- asynchronous thinking

## Stage 02 - TypeScript

### Primary reading
- *Programming TypeScript* — main book
- TypeScript Handbook — authoritative syntax and feature reference
- *Effective TypeScript* — best practices and pitfalls

### Focus areas
- type annotations and inference
- object and function typing
- unions and narrowing
- generics for ordinary engineering
- strict mode and tsconfig
- runtime validation boundary thinking

### What to defer
- advanced type-level programming
- clever type-system tricks without practical payoff

### C/C++ transition focus
- structural typing
- compile-time help versus runtime truth
- when types improve design versus when they add noise

## Stage 03 - Node.js

### Primary reading
- *Node.js Design Patterns* — main engineering book
- Node.js official docs — fs, path, process, streams, child_process, fetch/http

### Focus areas
- filesystem and paths
- config and environment variables
- retries, timeouts, and external I/O failure
- streams and buffers
- child process integration
- packaging and CLI/service structure

### C/C++ transition focus
- high-level runtime convenience without losing operational discipline
- evented I/O and concurrency patterns
- shell/tool integration from Node

## Stage 04 - LLM Basics

### Primary reading
- one model provider SDK/documentation set
- official docs for structured output and tool calling in your chosen provider
- provider API error and rate-limit docs

### Focus areas
- request and response lifecycle
- prompt contracts
- structured output
- streaming tradeoffs
- tool calling roundtrip
- token and latency awareness

### What to avoid
- reading five providers at once
- vague prompt-engineering content without implementation detail

### C/C++ transition focus
- probabilistic subsystem inside deterministic software
- validation at every model boundary
- logging and saved examples as debugging tools

## Stage 05 - Agent Core

### Primary reading
- your own Stage 04 project notes and traces
- selected docs or articles on tool orchestration and eval-minded design
- framework docs only after you can hand-build a loop

### Focus areas
- loop anatomy
- state boundaries
- tool registry design
- planning versus direct execution
- traces and guardrails

### What to avoid
- framework-first learning
- abstract “agent” essays with no system design consequences

## Stage 06 - RAG, Memory, and Workflows

### Primary reading
- vector/retrieval documentation only as needed for your chosen stack
- selected materials on chunking, retrieval evaluation, and citation grounding
- internal notes from your own experiments

### Focus areas
- ingestion
- chunking and metadata
- retrieval inspection
- grounded output
- memory policy
- workflow versus autonomy

### What to avoid
- adding retrieval before defining corpus quality
- treating “memory” as a marketing term instead of retained state

## Stage 07 - Production

### Primary reading
- *Designing Data-Intensive Applications* — selective, for long-term systems thinking
- *Designing Machine Learning Systems* — selective, for production AI perspective
- provider docs for rate limits, retries, and operational guidance

### Focus areas
- validation and contracts
- observability
- retries, backoff, fallbacks
- evals and regression
- secrets and data handling
- deployment shape and operator notes

### What to avoid
- over-reading architecture books instead of hardening a real project

## Stage 08 - Capstones

### Primary reading
- your own project documentation and prior stage notes
- comparable open-source projects, read critically
- deployment and operator documentation for your chosen runtime shape

### Focus areas
- architecture coherence
- evaluation discipline
- limitations and scope control
- documentation quality

## Minimal reading stack for this curriculum

If you want the shortest useful stack, use:

- *JavaScript: The Definitive Guide (7th ed.)*
- *Programming TypeScript*
- *Effective TypeScript*
- *Node.js Design Patterns*
- TypeScript Handbook
- Node.js official docs
- one provider SDK/documentation set

## Advice for experienced C/C++ engineers

- Do not try to reproduce native-language certainty through excessive TypeScript tricks.
- Learn the runtime and ecosystem conventions before optimizing them away.
- Prefer boring backend code over fashionable abstractions.
- Keep frontend reading out of the critical path unless your capstone truly needs it.
- Read enough to unblock implementation, then return to code.
