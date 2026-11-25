---
term: Automated check
section: patterns
order: 62
short: A test, type check, linter or build that passes or fails on its own, with no judgement involved.
audience: public
related: [[AFK]], [[AX]], [[Context window]], [[Environment]], [[Sandbox]]
---
Checks are what an [[Agent]] can learn from without you: it runs them as a [[Tool call]], reads the failure in the [[Tool result]], fixes and runs again. They only cover what they test, which is why [[Automated review]] and [[Human review]] come after.

## Heard in the wild

- What checks run in the sandbox?
- Build, tests and clippy. It fixes those before the PR.

## Avoid

Calling a check flaky and moving on; a flaky check teaches the agent the wrong thing.
