# Stage 07 Checklist

## Readiness checklist

- [ ] I validated config, model output, tool inputs, and other external boundaries explicitly.
- [ ] I added structured logs and identifiers that let me trace a run.
- [ ] I defined redaction or safe-logging rules for sensitive content.
- [ ] I can explain which failures are retryable and which are not.
- [ ] I documented timeout and fallback behavior.
- [ ] I have a regression set for prompts, schemas, retrieval, or tool use.
- [ ] I can compare system behavior across prompt or contract revisions.
- [ ] I wrote at least one incident-style review for a failure scenario.
- [ ] I documented how the system is started, monitored, and safely disabled or rolled back.
- [ ] I hardened at least one real project instead of only writing isolated examples.

## Progression gate

Advance only if you can:

- prove behavior with logs, tests, and evals
- explain operational behavior under common failure
- hand the system to another engineer without relying on tribal knowledge

## If you are not ready

Repeat Stage 07 work if any of these are still true:

- regressions are still being detected mainly by manual demos
- telemetry is too weak to explain a failed run
- deployment or operator behavior still depends on unrecorded assumptions
