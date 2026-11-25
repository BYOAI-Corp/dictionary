---
term: Next-token prediction
section: model
order: 8
short: The one trick under every answer. The model scores possible continuations, takes one token, adds it to the text and runs again until it stops.
audience: public
related: [[Agent]], [[Context]], [[Harness]], [[Model]], [[Output tokens]], [[Parameters]], [[Tool call]]
---
Every answer, plan and line of code is built one [[Token]] at a time from what is already in the [[Context window]]. The model has no separate step where it checks facts, which is why [[Hallucination]] and [[Sycophancy]] happen, and why sampling makes replies vary ([[Non-determinism]]).

## Heard in the wild

- So it is just autocomplete?
- Very good autocomplete over everything in its window. That is why what you put in the window matters so much.
