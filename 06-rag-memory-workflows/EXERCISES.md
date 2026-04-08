# Stage 06 Exercises

## Exercise policy

Every exercise should preserve provenance. If the system uses external context, you should be able to point to the specific source material involved.

## Exercise 1 - Small corpus ingestion

Objective: build a retrieval corpus you can inspect.

Tasks:

- choose a small set of documents, notes, or operational records
- normalize them into a consistent internal format
- assign metadata such as source, timestamp, and category
- document any cleanup assumptions

Progression check:

- you can explain the contents and boundaries of the corpus without guessing

## Exercise 2 - Chunking strategy comparison

Objective: understand how chunking changes retrieval behavior.

Tasks:

- create at least two chunking strategies for the same corpus
- compare chunk size, overlap, and metadata retention
- run representative queries against both
- record which failures each strategy introduces

Progression check:

- you can justify the chosen chunking approach with observed retrieval behavior

## Exercise 3 - Retrieval inspection drill

Objective: debug retrieval before generation.

Tasks:

- issue a small set of known queries
- inspect the top retrieved results manually
- label each result as useful, weak, or wrong
- identify at least one case of missing relevant context
- propose one retrieval-layer fix

Progression check:

- you can diagnose retrieval errors without blaming generation first

## Exercise 4 - Citation-backed answer generation

Objective: prevent unsupported answers from looking authoritative.

Tasks:

- generate answers using retrieved context
- require source references in the output
- distinguish direct support from inferred synthesis
- refuse or mark claims that are not grounded in retrieved evidence

Progression check:

- each answer makes its support path inspectable

## Exercise 5 - Memory boundary drill

Objective: define what should persist and what should not.

Tasks:

- list candidate memory items such as preferences, summaries, and task artifacts
- classify each as ephemeral, session-scoped, durable, or forbidden
- define update and deletion rules
- write down one privacy or correctness risk for each durable memory type

Progression check:

- your memory policy is specific enough that another engineer could implement it

## Exercise 6 - Workflow instead of agent comparison

Objective: learn when autonomy is unnecessary.

Tasks:

- choose one task that could be handled by either an agent loop or a deterministic workflow
- implement or sketch both approaches
- compare debuggability, reliability, and operator confidence
- decide which version you would ship first

Progression check:

- the decision is grounded in system behavior, not in novelty

## Exercise 7 - Retrieval evaluation set

Objective: create the beginnings of a real eval harness.

Tasks:

- assemble a small labeled set of queries and expected source hits
- define what counts as acceptable retrieval
- record misses and partial matches
- add at least one adversarial or ambiguous query

Progression check:

- you have a reusable set that can catch regressions after corpus or prompt changes

## Required minimum

Complete at least:

- Exercises 2, 3, 4, and 5
- one workflow-versus-agent comparison
- one labeled retrieval set that can be reused in Stage 07
