---
term: Environment
section: tools
order: 25
short: Where the agent acts: the machine, folder, shell, network and services its tools can reach.
audience: public
related: [[AGENTS.md]], [[AX]], [[Agent]], [[Context window]], [[Handoff artifact]], [[Harness]], [[Memory system]], [[Session]], [[Stateful]], [[Tool]], [[Tool result]]
---
The environment is what a [[Tool call]] touches: a [[Filesystem]], a shell, the network. Its limits come from the [[Sandbox]] and the [[Permission mode]]. A good environment also holds the [[Automated check]]s the agent can run to test itself.

## Heard in the wild

- Can it run the tests?
- Only if the environment has the toolchain. It doesn't here, so it can only read.

