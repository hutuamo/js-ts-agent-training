# Stage 08 Projects

## Project 1 - Research Assistant Capstone

Build a serious research-oriented backend or CLI system.

Expected capabilities:

- bounded corpus ingestion or source collection
- retrieval with provenance
- structured intermediate artifacts such as summaries, extracts, or task lists
- citation-backed final outputs
- eval scenarios that include unsupported or conflicting-source cases

What this project demonstrates:

- grounded context handling
- workflow composition
- backend-style artifact generation

Acceptance criteria:

- answers and outputs can be traced back to sources
- the system documents how it handles weak or missing evidence
- the project includes at least one retrieval evaluation set and one operational note

## Project 2 - Codebase Analyst Capstone

Build a system that helps inspect and reason about a software repository.

Expected capabilities:

- repository or document traversal
- structured extraction of repo facts
- optional retrieval over code or notes
- report generation such as architecture summaries, review notes, or risk checklists
- traceable separation between observed facts and generated conclusions

What this project demonstrates:

- tool orchestration
- evidence-backed analysis
- practical AI support for backend engineering work

Acceptance criteria:

- outputs clearly separate factual evidence from interpretation
- the analysis path is inspectable through logs, traces, or artifacts
- limitations are documented, especially around incomplete repo visibility or stale context

## Project 3 - Operations or Task Workflow Capstone

Build a narrow operational assistant or workflow engine for repeated tasks.

Expected capabilities:

- bounded task intake
- deterministic workflow stages with selective model use
- approval or escalation points where appropriate
- structured outputs suitable for later review or automation
- eval coverage for success, rejection, and partial-failure cases

What this project demonstrates:

- workflow-first AI engineering
- state and tool contract discipline
- reliability under repeated operational use

Acceptance criteria:

- the workflow is easier to reason about than a generic autonomous loop
- each stage has explicit contracts and validation
- operator documentation exists for configuration, execution, and failure handling

## Project 4 - Custom Domain Capstone

Build a capstone in a domain you care about, but hold it to the same engineering bar.

Minimum requirements:

- explicit problem statement and scope
- bounded architecture
- at least one meaningful AI integration beyond plain text generation
- validation, evals, and operator documentation
- a limitations section that is specific and credible

What this project demonstrates:

- transfer of the curriculum to a new domain
- engineering judgment in scope control
- ability to defend architecture choices under review

Acceptance criteria:

- the project could survive a technical walkthrough with another experienced engineer
- the chosen architecture is justified against simpler alternatives
- artifacts are complete enough for someone else to run and evaluate the system

## Recommended selection rule

Choose the capstone whose core difficulty matches the skill you most want to prove:

- retrieval and grounding: Research Assistant
- tooling and repo reasoning: Codebase Analyst
- workflow reliability: Operations or Task Workflow
- domain transfer: Custom Domain Capstone
