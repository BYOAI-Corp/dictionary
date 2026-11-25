---
term: Training
section: model
order: 4
short: How a model is made. Months of compute over a vast pile of text and code fix its parameters; after that it changes only with a new release.
audience: public
related: [[Context]], [[Model provider]], [[Next-token prediction]], [[Token]]
---
Training is where a [[Model]] gets its [[Parameters]] and with them its [[Parametric knowledge]]. It stops at a [[Knowledge cutoff]], so anything newer reaches the model only through its context.

Fine-tuning is more training on a smaller set; it is a separate project, not something a chat does.

## Heard in the wild

- Will it know the release from last week?
- Not from training. Give it the changelog or let it fetch the docs.

## Avoid

Saying a session "trained" the model.
