# Architecture

```
app/                 Next.js routes (pages + /api route handlers). Thin: validate, call service, respond.
components/          Presentational React components. No data fetching.
lib/db/              Drizzle schema (schema.ts) and connection (index.ts).
lib/tickets/         Ticket domain: service.ts (DB operations), validation.ts (zod), categorize.ts (AI enrichment).
lib/ai/              client.ts is the ONLY module that calls the LLM. prompts.ts holds all prompt templates.
drizzle/             Generated SQL migrations. Never edit by hand.
tests/               Vitest. In-memory SQLite; lib/ai/client is always mocked.
```

## Request flow: create ticket

`POST /api/tickets` → `createTicketSchema` (validation.ts) → `createTicket` (service.ts)
→ insert row → `categorizeTicket` (categorize.ts → ai/client.completeJson) → update row → 201.

## Rules

- AI enrichment never blocks or fails a write. On AI error, store null and log a warning.
- New AI features: add a prompt to `lib/ai/prompts.ts`, call `completeJson` with a zod schema
  and an `offline` fallback (see `offlineCategory` in categorize.ts). The app runs offline by default.
- Schema changes: edit `lib/db/schema.ts`, then `npm run db:generate`. Commit the generated SQL.
- Server components may call services directly; client components go through `/api`.
