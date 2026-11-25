---
term: Harness
section: model
order: 11
short: The program around a model that gives it tools, rules, memory and a loop: Claude Code, a chat app, an IDE plugin.
audience: public
related: [[AGENTS.md]], [[Agent]], [[Compaction]], [[Context]], [[Context window]], [[Filesystem]], [[Session]], [[Tool call]], [[Turn]]
---
A bare [[Model]] only predicts tokens. The harness builds each [[Model provider request]]: it adds the [[System prompt]], the conversation, the [[Tool]] definitions and every [[Tool result]], and it enforces the [[Permission mode]] and the [[Sandbox]].

Swapping the harness changes behaviour as much as swapping the model.

## Heard in the wild

- Is it the model that is bad at this, or the setup?
- Try the same model in another harness before you blame it.

