---
term: Stateless
section: sessions
order: 17
short: The model keeps nothing between requests. Whatever it should remember has to be sent again each time.
audience: public
related: [[AGENTS.md]], [[Agent]], [[Context]], [[Context window]], [[Handoff artifact]], [[Inference]], [[Memory system]], [[Parameters]], [[Training]]
---
A [[Model]] does not store your conversation. The [[Harness]] resends it on every [[Model provider request]], which is what makes a chat feel [[Stateful]]. When the history is dropped, by [[Clearing]] or a new [[Session]], the model knows nothing of it.

## Heard in the wild

- Why doesn't it remember yesterday?
- It never did. Yesterday's session was a different context.

## Avoid

"It forgot"; it was never told this time.
