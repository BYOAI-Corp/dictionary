---
term: Verifier
section: byoai-verify
order: 74
short: The service that checks each claim against its source and issues the verdict. Only the verifier can issue a verdict.
audience: public
related: [[Hallucination]], [[Independent agreement]], [[MCP]], [[Sub-claim]], [[Verdict]], [[Verification discipline]], [[Verification receipt]]
---
The verifier splits a [[Claim]] into [[Sub-claim]]s, grounds each against the [[Source]] and returns a [[Verdict]] with a [[Supporting quote]]. Two judges must reach [[Independent agreement]], and every call leaves a [[Verification receipt]]. It reads only the source you give it, never its own memory, which is what keeps a [[Hallucination]] from passing.

## Heard in the wild

- Can I ask the model whether its own answer is right?
- You can, but that's grading itself. Send the claim and the source to the verifier instead.
