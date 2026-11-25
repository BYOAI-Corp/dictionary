---
term: Pre-generation gate
section: byoai-verify
order: 77
short: A check that runs before an agent acts or answers, so a bad step is stopped instead of graded after the fact.
audience: public
related: [[Agent]], [[Audience-aware routing]], [[Permission request]], [[Verdict]]
---
Most tools grade an [[Agent]]'s work after it is done. A pre-generation gate checks before the step runs, the same way a [[Permission request]] pauses before a risky [[Tool call]], so a bad step is stopped instead of explained afterwards.

## Heard in the wild

- Isn't it enough to review the output at the end?
- Only if nothing has happened yet. Gate the step before it runs.

## Avoid

`guardrail`, `guardrails`; say Pre-generation gate.
