# Architecture - Stage 06 RAG Pipeline

## Core idea

Treat retrieval as a data pipeline plus a grounded answer step.

## Core components

1. corpus definition
2. ingestion and normalization
3. chunking and metadata
4. indexing and retrieval
5. grounded answer generation
6. citation or provenance handling
7. retrieval evaluation set

## Boundary rules

- corpus quality should be inspectable before retrieval tuning
- retrieval should be testable independently from generation
- final answers should identify their evidence
- unsupported claims should be refused or marked clearly
- memory and retrieval should remain separate concepts

## Recommended flow

1. ingest source material
2. normalize and chunk
3. attach metadata
4. index and retrieve
5. inspect retrieved evidence
6. generate a grounded response
7. record success or failure against labeled queries

## Failure categories to plan for

- bad or stale source material
- weak chunking strategy
- irrelevant retrieval results
- missing supporting evidence
- answer over-claiming beyond retrieved evidence
