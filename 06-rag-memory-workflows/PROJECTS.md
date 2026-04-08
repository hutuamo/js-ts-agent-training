# Stage 06 Projects

## Project 1 - Document QA Assistant

Build a retrieval-backed assistant over a bounded document set.

Suitable corpora:

- internal notes
- technical design docs
- incident reports
- documentation snapshots

Required capabilities:

- ingestion pipeline
- chunking and metadata strategy
- retrieval step that can be inspected independently
- grounded answers with citations or source references

What this project trains:

- end-to-end retrieval design
- provenance-aware answer generation
- preparation for production eval work

Acceptance criteria:

- answers cite the retrieved evidence they rely on
- unsupported questions are refused or marked explicitly
- retrieval results can be inspected separately from final output

## Project 2 - Research Notebook Generator

Build a workflow that collects material, extracts key points, and produces a structured notebook or report.

Required capabilities:

- retrieval over prior materials
- intermediate summaries or extracted facts
- explicit distinction between source-backed content and synthesis
- workflow stages that can be rerun independently

What this project trains:

- workflow composition
- intermediate artifact design
- memory and retrieval boundaries for research tasks

Acceptance criteria:

- the workflow is more inspectable than a single free-form agent loop
- each stage produces an artifact that can be reviewed
- final output includes references back to source material

## Project 3 - Retrieval-Backed Workflow Runner

Build a backend or CLI workflow that uses retrieval to support a repeated operational task.

Examples:

- incident triage helper
- support-response draft pipeline
- change-review context assembler

Required capabilities:

- clear workflow stages
- retrieval-backed context assembly
- typed intermediate data
- explicit handoff or approval points when needed

What this project trains:

- practical retrieval in operations-style workflows
- bounded model use inside deterministic orchestration
- preparation for production hardening in Stage 07

Acceptance criteria:

- each workflow stage has a clear contract
- context assembly is reproducible
- the system can explain which retrieved inputs influenced the final output

## Recommended build order

1. Document QA Assistant
2. Research Notebook Generator
3. Retrieval-Backed Workflow Runner
