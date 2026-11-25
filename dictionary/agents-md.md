---
term: AGENTS.md
section: memory
order: 54
short: A file of standing instructions the harness loads into every session for a repo (CLAUDE.md in Claude Code).
audience: public
related: [[Agent]], [[Context window]], [[Environment]], [[Harness]], [[Model]], [[Progressive disclosure]], [[Session]], [[Skill]], [[Stateless]], [[Token]], [[Turn]]
---
It holds the project's rules, commands and vocabulary. It costs [[Attention budget]] in every request, so keep it short and point to longer docs with [[Context pointer]]s rather than pasting them in.

## Heard in the wild

- Where do I put 'always run the linter'?
- In AGENTS.md, one line, with the command.

## Avoid

Turning it into a manual; long rule files get ignored.
