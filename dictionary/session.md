---
term: Session
section: sessions
order: 23
short: One running conversation with its history. A new session starts with an empty context.
audience: public
related: [[AGENTS.md]], [[Agent]], [[Clearing]], [[Compaction]], [[Context window]], [[Filesystem]], [[Memory system]], [[Model]], [[Model provider request]], [[Stateless]], [[Tool result]]
---
A session keeps the [[Context]] of its [[Turn]]s until you end it, clear it or compact it. Long sessions drift out of the [[Smart zone]]; the remedy is a [[Handoff]] or a fresh session that reads the [[Primary source]] files again.

## Heard in the wild

- Should I keep going in this session?
- You are at 160k tokens; hand off and start fresh.
