---
term: Inference
section: model
order: 5
short: Running a trained model: tokens in, predicted tokens out. Every reply you get is inference.
audience: public
related: [[Context]], [[Context window]], [[Memory system]], [[Model]], [[Parameters]], [[Session]], [[Stateless]], [[Token]], [[Tool]], [[Training]], [[Turn]]
---
Inference is the work a [[Model provider]] bills for. Each [[Model provider request]] sends [[Input tokens]] and gets [[Output tokens]] back, produced by [[Next-token prediction]], one token at a time.

How hard the model thinks at inference time can often be tuned with [[Effort]].

## Heard in the wild

- Why is this so slow?
- Inference on the big model with high effort. Drop to medium for the renames.
