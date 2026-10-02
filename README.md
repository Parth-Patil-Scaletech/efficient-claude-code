# Efficient Claude Code

Reference material from our session on using Claude Code efficiently: one idea (the meter), ten Golden Rules, and a real comparison of the same ticket built twice. Following the rules cut the cost by 57% for the same feature set.

**Start here:** [`guide/cheat-sheet.pdf`](guide/cheat-sheet.pdf), one page with all ten rules.

| Folder | What's in it |
|---|---|
| `guide/` | `guide.pdf`, the full reference guide (source: `guide.md`), and `cheat-sheet.pdf` (source: `cheat-sheet.html`). |
| `deck/` | `index.html`, the session slides. `replay.html` steps through the two recorded runs prompt by prompt. |
| `starter-kit/` | A short CLAUDE.md template, the `/handoff` skill, a spec template and an example architecture map, ready to copy into a project. |

## Viewing the slides

Download or clone the repo and open `deck/index.html` in a browser. Arrow keys or space to move, **N** for speaker notes, **F** for fullscreen. On the replay slide, click the viewer first, then use the arrow keys inside it.

## Setting up a project

Copy the starter kit into your project and fill in the placeholders:

```bash
cp -r starter-kit/. <your-project>/
echo ".claude/handoff.md" >> <your-project>/.gitignore
```

See `starter-kit/README.md` for what each file does.

Commands were checked on Claude Code 2.1.287. If something doesn't match your version, run `/help`.
