---
term: Cache tokens
section: model
order: 16
short: Input tokens served from the prefix cache, billed at a discount. Writing to the cache may cost a little extra.
audience: public
related: [[Harness]], [[Model]], [[Model provider]], [[Model provider request]], [[Stateless]], [[System prompt]], [[Tool result]], [[Turn]]
---
On a long [[Session]] most [[Input tokens]] are often cache reads from the [[Prefix cache]]. Watching the ratio tells you whether your context is stable enough to benefit.

## Heard in the wild

- Most of the bill says cache read.
- Good. That is the cheap kind.
