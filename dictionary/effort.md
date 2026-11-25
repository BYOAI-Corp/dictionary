---
term: Effort
section: model
order: 6
short: A setting you choose per request. Turn it up for a tricky bug or a design call and pay in time and tokens; turn it down for quick edits.
audience: public
related: [[Inference]], [[Model provider request]], [[Session]], [[Token]]
---
Many models can spend extra [[Output tokens]] reasoning before the visible reply. A higher effort setting raises that budget. It helps on planning and debugging and wastes money on simple edits.

Effort is chosen per request by the [[Harness]], so the same [[Model]] can be fast and shallow or slow and careful.

## Heard in the wild

- Should I turn effort up for this?
- For the race condition, yes. For the copy changes, no.

## Avoid

Treating high effort as a fix for missing context; it cannot think its way to facts it was never shown.
