# Stage 03 Checklist

## Readiness checklist

- [ ] I can build and run a multi-command Node.js CLI.
- [ ] I can handle `argv`, environment variables, and exit codes deliberately.
- [ ] I can load and validate configuration before starting real work.
- [ ] I can distinguish user-facing output from logs and diagnostics.
- [ ] I can wrap HTTP calls with timeout and retry behavior.
- [ ] I know which failures should not be retried.
- [ ] I can explain transport errors versus application-level errors.
- [ ] I can choose between eager file reads and streaming for a given task.
- [ ] I can run child processes and handle stdout, stderr, and exit status.
- [ ] I can process multiple async jobs with explicit concurrency limits.
- [ ] I built at least one backend or CLI project with realistic failure handling.

## Progression gate

Advance only if you can:

- ship a small Node tool or service that behaves predictably under common failure
- explain the operational choices in the code
- keep side effects, orchestration, and business logic separate enough to reason about

## If you are not ready

Repeat Stage 03 work if any of these are still true:

- network calls have no timeout strategy
- shell commands are being invoked without structured result handling
- logs are too weak to explain what the tool did and why it failed
