---
term: Context window
section: sessions
order: 19
short: The fixed number of tokens a model can see at once. Anything outside it does not exist for that request.
audience: public
related: [[Harness]], [[Memory system]], [[Model]], [[Model provider request]], [[System prompt]], [[Token]], [[Tool call]], [[Tool result]]
---
The window holds the whole [[Context]]. When a [[Session]] nears the limit the harness must drop or summarise ([[Compaction]], [[Autocompact]]) or you start fresh ([[Clearing]]). Well before the limit, quality falls as the [[Attention budget]] is spread thinner; see [[Smart zone]].

## Heard in the wild

- Can I paste the whole monorepo?
- It would not fit, and most of it would be noise. Point it at the files the task touches.

## Avoid

Treating the window as memory; it is working space for one request.
