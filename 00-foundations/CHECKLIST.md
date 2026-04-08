# Stage 00 Checklist

## Readiness checklist

- [ ] I installed Node.js LTS and can verify the version from the terminal.
- [ ] I chose a package manager and can explain why the repo should stay consistent on one.
- [ ] I created and ran a minimal CLI with `node`.
- [ ] I created and ran the same CLI through a package script.
- [ ] I can explain the purpose of `package.json` at a practical level.
- [ ] I know whether my scratch project is using ESM or CommonJS.
- [ ] I can explain why `async` does not imply parallel execution.
- [ ] I tested event-loop ordering with a small script instead of relying on intuition.
- [ ] I wrote down at least five C/C++ assumptions that fail or change in JS/TS.
- [ ] I used a debugger or equivalent tracing on a small program.
- [ ] I can orient myself in a small Node project and identify its entry point.

## Progression gate

Advance only if you can do all of the following without searching every step:

- initialize a small backend or CLI project
- run, modify, and debug it
- explain the runtime model at a practical level
- describe what TypeScript will add later and what it will not fix

## If you are not ready

Repeat Stage 00 if any of these are still true:

- package scripts still feel opaque
- module format differences are still confusing
- async behavior still feels surprising most of the time
- you are still trying to map every JS concept directly onto C/C++
