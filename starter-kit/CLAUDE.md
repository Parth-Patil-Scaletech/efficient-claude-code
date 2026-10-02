# <Project name>

<One line: stack, e.g. Next.js App Router + Drizzle (SQLite)>.
Architecture map: `docs/architecture.md`. Read it before exploring the codebase.

## Commands
- `<test command>` / `<typecheck command>` / `<build command>`
- <Any generate or migrate step, e.g. "`npm run db:generate` after editing the schema; never hand-edit generated files">

## Rules
- <Hard rule 1, e.g. "LLM calls only through `lib/ai/client.ts`">
- <Hard rule 2, e.g. "Tests mock external APIs; never call real services in tests">
- Work only inside this repository.
- Ask before installing, removing or upgrading packages, or changing anything outside the code (config, environment, lockfiles).
- When you run tests or builds, report only failures.
- Do not create markdown files unless asked. No change summaries in files.

<!-- Keep this file under ~30 lines. It's sent with every message. Link to docs instead of pasting them. -->
