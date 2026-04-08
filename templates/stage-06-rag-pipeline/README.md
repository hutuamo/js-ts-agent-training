# Template - Stage 06 RAG Pipeline

## Purpose

This template is a starter blueprint for a retrieval-backed workflow or assistant over a bounded corpus.

It is not a generic vector-search demo. It is a structure for learning ingestion, chunking, retrieval inspection, and grounded output.

## Good use cases

- document QA over technical notes
- research notebook generation
- incident or operations context lookup
- support-response drafting with source grounding

## Build goals

- define a small inspectable corpus
- implement ingestion and metadata handling
- make retrieval inspectable before generation
- require grounded outputs with source references

## Suggested file tree

```text
stage-06-rag-pipeline/
  README.md
  ARCHITECTURE.md
  TODO.md
  corpus/
  src/
    ingest.ts
    chunk.ts
    index.ts
    retrieve.ts
    answer.ts
    citations.ts
  eval/
    queries.json
```

## Minimum acceptance criteria

- one bounded corpus
- one chunking strategy documented and justified
- one retrieval inspection path
- one answer path with citations or explicit refusal
- one small labeled query set

## Extension ideas

- compare two chunking strategies
- add metadata filtering
- add workflow path versus free-form assistant comparison
- add simple retrieval quality metrics
