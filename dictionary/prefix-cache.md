---
term: Prefix cache
section: model
order: 15
short: The provider keeps the start of a recent context ready, so a request that begins the same way is cheaper and faster.
audience: public
related: [[Harness]], [[Model provider request]], [[Session]], [[Token]], [[Turn]]
---
Agents resend the same opening again and again: [[System prompt]], tool list, earlier turns. When that prefix matches a recent request, the [[Model provider]] reuses it and bills [[Cache tokens]] instead of full [[Input tokens]].

Changing something early in the context, like editing the system prompt mid-session, breaks the cache.

## Heard in the wild

- Why did costs jump after I edited CLAUDE.md?
- The prefix changed, so the cache started over.
