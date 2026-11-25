---
term: Permission request
section: tools
order: 31
short: The harness pausing to ask you before a tool call runs, because the permission mode says so.
audience: public
related: [[AFK]], [[Harness]], [[Human-in-the-loop]], [[Model]], [[Session]], [[Tool]], [[Tool call]], [[Tool result]]
---
Requests are how a human stays in the loop for risky actions: writing outside the repo, running a network command, deleting. Too many requests and people approve without reading; too few and the [[Agent]] can do damage. Tune them with the [[Permission mode]] and the [[Sandbox]].

## Heard in the wild

- It keeps asking about every git command.
- Allow read-only git and keep asking for push.
