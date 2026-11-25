---
term: Tool result
section: tools
order: 29
short: The reply to a tool call, added to the conversation so the next turn can use it. A file read, a test run's output, or the error that stopped it.
audience: public
related: [[Context]], [[Harness]], [[Model]], [[Model provider request]], [[Session]], [[Token]], [[Tool call]], [[Turn]]
---
Tool results are how an [[Agent]] learns about its [[Environment]]. Big results eat the [[Context window]] fast, and every result is untrusted text: a page or file can carry instructions that the agent must not follow.

## Heard in the wild

- Why is the context full already?
- It read a 9,000-line log as one tool result.
