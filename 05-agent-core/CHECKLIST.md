# Stage 05 Checklist

## Readiness checklist

- [ ] I can implement an explicit observe-decide-act-update-stop loop.
- [ ] I can explain why each stop condition exists.
- [ ] I can define tools with validated arguments and normalized results.
- [ ] I can distinguish loop state, session state, and state that should not be stored.
- [ ] I compared a planning-based approach with a direct-execution approach on the same task.
- [ ] I added guardrails such as max steps, invalid-tool handling, and escalation paths.
- [ ] I save traces or logs that let me reconstruct a failed run.
- [ ] I can classify failures by prompt, state, tool selection, tool execution, or stop logic.
- [ ] I can explain when a deterministic workflow is better than an autonomous loop.
- [ ] I built at least one small agent system that another engineer could inspect and reason about.

## Progression gate

Advance only if you can:

- defend your agent architecture in backend terms
- trace a run from initial request through state updates and tool calls
- show that the loop is bounded and debuggable

## If you are not ready

Repeat Stage 05 work if any of these are still true:

- the model is still implicitly controlling business logic that should live in code
- state ownership is unclear
- a failed run cannot be reconstructed from the artifacts you kept
