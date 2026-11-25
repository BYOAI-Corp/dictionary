---
term: Parameters
section: model
order: 3
short: The learned numbers inside a model. More parameters usually means more capacity and more cost per token.
audience: public
related: [[Context]], [[Context window]], [[Knowledge cutoff]], [[Model]], [[Next-token prediction]], [[Session]], [[Stateless]], [[Token]]
---
Parameters are the weights set during [[Training]]. They hold everything the model knows on its own, its [[Parametric knowledge]]. They do not change while you use it: nothing you type at [[Inference]] time updates them.

## Heard in the wild

- Can we teach it our naming rules?
- Not into its parameters by chatting. Put the rules in CLAUDE.md so they land in context every session.

## Avoid

"The model learned from our last session"; the weights did not move.
