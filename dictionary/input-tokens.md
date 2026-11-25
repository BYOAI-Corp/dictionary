---
term: Input tokens
section: model
order: 13
short: The tokens you send with a request: prompt, history, files, tool results. Usually the biggest part of an agent's bill.
audience: public
related: [[AI]], [[Agent]], [[Clearing]], [[Compaction]], [[Harness]], [[Model]], [[Output tokens]], [[Stateless]], [[System prompt]], [[Token]], [[Tool result]], [[Turn]]
---
Every [[Model provider request]] resends the whole [[Context]], so input grows as a [[Session]] goes on. Input that matches the [[Prefix cache]] is billed as cheaper [[Cache tokens]].

## Heard in the wild

- Input is ten times output on this run.
- Normal for an agent; it rereads the whole history every turn.
