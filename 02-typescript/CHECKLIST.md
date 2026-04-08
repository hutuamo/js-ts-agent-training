# Stage 02 Checklist

## Readiness checklist

- [ ] I can explain what `tsconfig.json` is doing in my project.
- [ ] I use strict mode or can justify any deviation.
- [ ] I understand the difference between inference and explicit annotation.
- [ ] I can model ordinary application data with readable types.
- [ ] I know when to use unions and how to narrow them safely.
- [ ] I prefer `unknown` over `any` at external boundaries.
- [ ] I can design typed async function contracts.
- [ ] I can use generics for ordinary reuse without making the code harder to read.
- [ ] I do not confuse compile-time types with runtime validation.
- [ ] I added schema or manual validation where untrusted data enters the system.
- [ ] I converted at least one existing JS tool into a clean TS version.

## Progression gate

Advance only if you can:

- design and explain typed boundaries for CLI commands, APIs, or tools
- critique a TS design for both safety and readability
- validate external data instead of asserting it into place

## If you are not ready

Repeat Stage 02 if any of these are still true:

- you use `as` assertions to silence uncertainty routinely
- your type definitions are harder to understand than the runtime code
- you still expect the compiler to protect you from invalid external data
