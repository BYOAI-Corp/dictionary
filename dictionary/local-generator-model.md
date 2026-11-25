---
term: Local generator model
section: byoai-models
order: 99
short: A model run on the client's own hardware that drafts answers, trained on BYOAI-checked examples. It drafts; it never verifies itself.
audience: public
related: [[Frontier model]]
---
A local generator model runs on the client's own hardware and drafts answers. It learns from examples that passed BYOAI's checks, and a new version replaces the old one only after passing a review gate. It drafts; the [[Verifier]] decides.

## Heard in the wild

- Can the local model check its own drafts?
- No. It drafts; the verifier checks.
