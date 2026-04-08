# Stage 06 Checklist

## Readiness checklist

- [ ] I can ingest a bounded corpus and describe its source and quality assumptions.
- [ ] I compared at least two chunking strategies on real queries.
- [ ] I can inspect retrieval results independently from model-generated answers.
- [ ] I can require citation-backed or source-referenced answers.
- [ ] I can explain the difference between retrieved context, working state, and stored memory.
- [ ] I wrote a memory policy that includes update and deletion rules.
- [ ] I compared an agent-loop solution against a workflow-oriented solution for the same task.
- [ ] I created a small labeled retrieval set for regression checking.
- [ ] I can explain how stale or conflicting source material should be handled.
- [ ] I built at least one retrieval-backed system whose context path is auditable.

## Progression gate

Advance only if you can:

- trace an answer back to source documents
- justify what the system stores and why
- show when workflow structure improves reliability over open-ended autonomy

## If you are not ready

Repeat Stage 06 work if any of these are still true:

- retrieval quality is being judged only by final answer fluency
- memory is being added without clear ownership or retention rules
- the system cannot explain which sources actually informed an output
