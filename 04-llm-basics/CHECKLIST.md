# Stage 04 Checklist

## Readiness checklist

- [ ] I can integrate one model API behind a small, normalized wrapper.
- [ ] I can explain the request, response, and error boundaries of that wrapper.
- [ ] I can write prompts that specify task, constraints, and output format clearly.
- [ ] I can require structured output and validate it before use.
- [ ] I can explain why model output should not be trusted even when the SDK call succeeds.
- [ ] I implemented one streamed path and can justify whether it is worth the added complexity.
- [ ] I implemented at least one tool-calling roundtrip with argument validation.
- [ ] I can distinguish prompt failure, model variance, schema failure, and tool-layer failure.
- [ ] I saved representative examples that can be reused as regression cases later.
- [ ] I measured at least one latency or cost tradeoff instead of guessing.

## Progression gate

Advance only if you can:

- build a model-backed backend or CLI feature with explicit validation
- keep prompts, schemas, and tool execution boundaries separate
- explain how your integration fails and where each failure is handled

## If you are not ready

Repeat Stage 04 work if any of these are still true:

- model output is still flowing directly into business logic
- tool calls are being executed without validated arguments
- prompt revisions are being made without saved examples or comparison cases
