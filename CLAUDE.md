# teal-sea-profile — agent rules

Every AI agent working here reads this file. Claude Code loads `CLAUDE.md`; Codex loads
`AGENTS.md`, which **is a symlink to this file** — one file, two names, so the two cannot
drift. Edit this file; do not replace the symlink with a copy.

## What this repo is

`teal-sea/teal-sea` — the **GitHub profile README**. Its `README.md` renders at the top of
`github.com/teal-sea`. It is the first thing a recruiter or hiring manager sees, and it is
unavoidably **PUBLIC**.

There is one file. Do not add code, workflows, or structure to it.

## Rules

- **Only link repos that are public and finished enough to be read.** Linking a private repo
  shows a 404 to everyone but Thomas. Verify before adding:

```bash
gh repo view teal-sea/<name> --json visibility -q .visibility   # must print PUBLIC
```

- **Never name the client.** Thomas is still employed at LimoCity. Describe capability and
  pattern, never the account, and never in a way that reads as job-search intent — his
  client can see this page.
- **Positioning: architecture-led, AI-accelerated, fully accountable.** Say built, designed,
  architected, owns production operation. Never say unaided, solo-authored or hand-written,
  and never cite commit counts as proof of authorship.
- **Label self-reported metrics as self-reported.** Lead with independently checkable things
  — live products and public repos — because that is what this page is for.

## Keep it in sync with reality

This page's failure mode is quietly going stale: it lists repos that were renamed, deleted
or made private. When a linked repo changes name or visibility, fix it here in the same
session. `fretboard-mapper` → `modalruns` (2026-08-03) is exactly that case.
