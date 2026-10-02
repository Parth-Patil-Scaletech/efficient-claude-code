# Starter kit

Copy into your project and fill in the placeholders.

| File | What it's for |
|---|---|
| `CLAUDE.md` | Short project instructions, loaded on every message. Keep it under ~30 lines. |
| `.claude/skills/handoff/SKILL.md` | `/handoff` writes a 25-line note to `.claude/handoff.md` so you can `/clear` and continue. |
| `docs/specs/_template.md` | Spec template for anything that touches more than one file. |
| `docs/architecture.md` | Example one-page architecture map (from the session's demo app). Replace it with your own; CLAUDE.md links to it. |

```bash
cp -r starter-kit/. <your-project>/
echo ".claude/handoff.md" >> <your-project>/.gitignore
```

Optional, in `~/.claude/settings.json`, so plan approval can clear the planning context:

```json
{ "showClearContextOnPlanAccept": true }
```

See `guide/guide.pdf` for how each piece fits into the workflow.
