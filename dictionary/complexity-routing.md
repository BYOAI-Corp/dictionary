---
term: Complexity routing
section: byoai-verify
order: 76
short: Sending each check to the cheapest tier that can settle it: plain code first, then a fast model, then a larger model, then a person.
audience: public
related: [[Audience-aware routing]], [[Fast decision model]], [[Frontier model]]
---
Not every check needs a large model. Complexity routing sends simple, exact checks to plain code, bounded choices to a [[Fast decision model]], and only hard cases to a [[Frontier model]] or a person. It keeps checks fast and cheap without lowering the bar for a [[Verdict]].

## Heard in the wild

- Why was that check almost free?
- It was an exact match, so routing settled it in code without calling a model.
