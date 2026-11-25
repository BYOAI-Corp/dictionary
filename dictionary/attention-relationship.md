---
term: Attention relationship
section: failures
order: 40
short: Each token weighs every other token in the window. The more there is, the more relationships compete.
audience: public
related: [[Attention degradation]], [[Model]], [[Model provider request]], [[Token]]
---
The model's attention links tokens to one another. With a short [[Context]], the links that matter are strong; with a long one they are diluted. This is the mechanism behind the [[Attention budget]] and the [[Smart zone]].

## Heard in the wild

- Why did it miss the rule at the top?
- Two hundred thousand tokens later, that rule is one voice among many.
