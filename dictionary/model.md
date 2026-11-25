---
term: Model
section: model
order: 2
short: The trained network itself: a large file of numbers that turns input tokens into a prediction of the next one.
audience: public
related: [[Agent]], [[Context]], [[Model provider request]], [[Next-token prediction]], [[Session]], [[Stateless]], [[System prompt]], [[Tool]]
---
A model is what [[Training]] produces: billions of [[Parameters]] that, at [[Inference]] time, read a run of [[Token]]s and score every possible next token. It has no memory of its own between calls and no tools; those come from the [[Harness]] around it.

Models differ in size, price, speed and what they were trained on, and a [[Model provider]] may serve several versions under similar names.

## Heard in the wild

- Which model was that?
- Opus 5.5 for the plan, Haiku for the bulk edits.

## Avoid

Calling the app or the harness "the model".
