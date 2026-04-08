# Stage 00 Exercises

## How to use these exercises

Do them in order. The point is to remove setup friction and force explicit comparisons with C/C++ thinking. Keep all work small and local.

## Exercise 1 - Install and inspect the toolchain

Objective: confirm you can run the core tools and identify their roles.

Tasks:

- install Node.js LTS
- choose one package manager for this repo workflow
- record the outputs of `node --version` and your package manager version command
- write a short note describing what `node`, the package manager, and `npx` each do

Completion check:

- you can explain the difference between the runtime and the package manager in one paragraph

## Exercise 2 - Create a minimal CLI workspace

Objective: create a project without scaffolding tools.

Tasks:

- make a new folder for stage-00 scratch work
- create a `package.json`
- add a simple `index.js`
- run it with `node`
- add a package script and run the same program through the script

Completion check:

- you can explain what changed, if anything, between direct execution and script execution

## Exercise 3 - Read your own package metadata

Objective: stop treating `package.json` as opaque.

Tasks:

- add `name`, `version`, `type`, and `scripts`
- add one dev tool such as a formatter or linter
- inspect the lockfile after installation
- write down which fields are for humans, which are for tooling, and which affect runtime behavior

Completion check:

- you can point to at least three fields in `package.json` and state why they exist

## Exercise 4 - Debug a trivial program on purpose

Objective: build basic debugging muscle before the programs get larger.

Tasks:

- write a small script with a bug involving mutation, coercion, or async ordering
- inspect it with `console` logging and then with your editor debugger
- record what you expected and what actually happened

Completion check:

- you can describe how the debugger helped more than print statements, or explain why it did not

## Exercise 5 - Event loop sanity check

Objective: replace vague async intuition with a concrete execution model.

Tasks:

- write a short script using synchronous code, `Promise.resolve().then(...)`, and `setTimeout(..., 0)`
- predict the output order before running it
- run it and compare with your prediction
- write a short explanation of the observed order

Completion check:

- you can explain why "async" does not automatically mean "runs first" or "runs in parallel"

## Exercise 6 - C/C++ assumption audit

Objective: surface the assumptions most likely to cause future bugs.

Write short answers for each prompt:

- what does "passing an object" mean in JS compared with passing a struct or pointer in C/C++?
- what does "module boundary" feel like compared with header/source separation?
- what kinds of errors move from compile time to runtime?
- what performance instincts still help, and which ones are premature at this stage?
- when does dynamic typing become a reliability problem?

Completion check:

- your answers are specific enough that you could revisit them later and refine them

## Exercise 7 - Read a small Node project

Objective: learn to orient yourself quickly in a JS/TS repo.

Tasks:

- pick a small open-source CLI or utility repo
- identify the entry point
- identify how scripts are run
- identify where dependencies are declared
- identify whether it uses ESM or CommonJS
- write a short map of the repo in your own words

Completion check:

- you can explain how to run the project and where you would start debugging it

## Minimum bar to pass Stage 00

You should have completed at least:

- Exercises 1 through 6
- one full written assumption audit
- one repo-orientation read of an existing small project
