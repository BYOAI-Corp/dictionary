---
term: Model provider request
section: model
order: 12
short: One call to the provider's API: the whole context goes in, one reply comes out. An agent makes many per task.
audience: public
related: [[Agent]], [[Context]], [[Harness]], [[Model]], [[Model provider]], [[Session]], [[Token]], [[Tool]], [[Tool call]], [[Turn]]
---
Because the model is [[Stateless]], each request carries everything: [[System prompt]], history, tool definitions and every [[Tool result]] so far, all as [[Input tokens]]. The reply's [[Output tokens]] are added and the next request sends it all again.

The [[Prefix cache]] is what keeps that repetition affordable.

## Heard in the wild

- Why did one task cost so much?
- Sixty requests, each resending a long context.
