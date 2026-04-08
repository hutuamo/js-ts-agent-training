# Stage 08 - Capstones and Portfolio-Grade AI Backend Systems

## Stage intent

This stage consolidates the curriculum into serious end-to-end projects. The objective is not to maximize feature count. The objective is to produce a project that shows engineering judgment across backend structure, model integration, tool use, retrieval or workflow design, validation, and operational clarity.

A strong capstone should look like software built by a disciplined engineer, not like a demo assembled from disconnected AI features.

## What a capstone must demonstrate

Your capstone should show that you can:

- choose an appropriate system shape for the problem
- justify where the model is used and where deterministic code is better
- define contracts around tools, state, and external data
- validate outputs before using them
- produce inspectable traces, logs, or artifacts
- evaluate behavior with representative tasks
- explain limitations honestly

The project does not need to be large. It does need to be coherent.

## Recommended capstone directions

### 1. Research Assistant

Good fit if you want to emphasize:

- retrieval
- citation-backed answers
- workflow composition
- notebook or report generation

Strong versions of this capstone avoid generic chat UX and instead focus on research artifacts, provenance, and repeatable workflows.

### 2. Codebase Analyst

Good fit if you want to emphasize:

- repository inspection
- tool orchestration
- code and document retrieval
- review or architecture summaries

Strong versions separate factual repo evidence from model-generated synthesis and keep the analysis traceable.

### 3. Personal Operations or Task Agent

Good fit if you want to emphasize:

- bounded task routing
- local tools and workflow execution
- state management
- operator visibility

Strong versions are narrow in scope and operationally clear. Avoid the temptation to build a fake universal assistant.

### 4. Domain-Specific Workflow System

Good fit if you want to emphasize:

- deterministic orchestration with selective model use
- approval points
- structured artifacts
- repeatable backend jobs

This is often the strongest option if you care more about reliability than broad autonomy.

## Capstone expectations

Your project should include:

- a clear problem statement
- architecture with explicit system boundaries
- implementation notes for model, tool, retrieval, and state decisions
- acceptance criteria for core tasks
- evidence of validation, testing, and eval work
- operational guidance for setup and execution
- limitations and next-step roadmap

## Scope guidance

Prefer a narrow, well-executed project over a broad and unstable one.

Good capstone scope:

- one primary workflow or user journey
- two to five meaningful tools or pipeline stages
- one retrieval corpus or one bounded state model
- eval coverage over representative cases

Bad capstone scope:

- "general assistant" with undefined capabilities
- many tools with weak contracts
- memory with no retention policy
- deployment claims without observability or operational notes

## Relationship to earlier stages

- Stage 04 should be visible in your prompt, structured-output, and tool-calling discipline.
- Stage 05 should be visible in your loop or orchestration design and traceability.
- Stage 06 should be visible in your retrieval, memory, or workflow choices.
- Stage 07 should be visible in your validation, evals, logs, and operator guidance.

If a capstone does not reflect these stages, it is not complete even if the demo appears impressive.

## Required artifacts

Every capstone should produce:

- `README` with project purpose and usage
- architecture note
- setup and configuration guide
- task or scenario list used for evaluation
- limitations document
- short demo script, walkthrough note, or equivalent

## Stage gate

A capstone passes only when you can:

- explain the system architecture and tradeoffs clearly
- demonstrate representative scenarios end to end
- show evidence of reliability work, not just feature work
- point to known limitations without guesswork
- defend why the project scope is appropriate

## Exit criteria

You complete the curriculum when you can present one or more capstones as real engineering work: structured, inspectable, validated, and credible to another backend engineer.
