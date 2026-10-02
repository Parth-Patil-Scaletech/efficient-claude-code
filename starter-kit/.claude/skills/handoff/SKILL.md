---
name: handoff
description: Write a short handoff note so the work can continue in a fresh session. Use when the user asks for a handoff or says they are about to clear the session.
---

Overwrite `.claude/handoff.md` with at most 25 lines:

1. Goal: one line, link the spec file if there is one.
2. Done: files changed, one line each.
3. Decisions not obvious from the code.
4. Next steps, in order.
5. Known issues or failing checks.

Do not restate the spec. Do not paste code longer than 5 lines. Reply with "Handoff written." only.
