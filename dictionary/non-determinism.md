---
term: Non-determinism
section: model
order: 9
short: The same prompt can give different answers. Sampling, model updates and small context changes all move the output.
audience: public
related: [[Agent]], [[Inference]], [[Model provider request]], [[Token]]
---
[[Next-token prediction]] usually samples rather than always taking the top token, so two runs differ. The [[Model provider]] may also update the [[Model]], and any change to the [[Context]] changes the odds.

That is why trust comes from [[Automated check]]s and review rather than from a reply having worked once.

## Heard in the wild

- It passed yesterday with the same prompt.
- Same prompt, different run. Make the test the judge, not the transcript.

## Avoid

Debugging a flaky answer by rewording the prompt until it passes once.
