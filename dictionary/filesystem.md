---
term: Filesystem
section: tools
order: 26
short: The files and folders the agent can read and write. Most of its work happens here.
audience: public
related: [[AGENTS.md]], [[Agent]], [[Context pointer]], [[Context window]], [[Environment]], [[Harness]], [[Skill]], [[Tool]], [[Tool call]]
---
Reading files is how an agent fills its [[Context]]; writing them is how its work lasts beyond the [[Session]]. The [[Sandbox]] decides which paths are open.

## Heard in the wild

- Can it see my SSH keys?
- Not if the sandbox denies reads outside the repo. Check before you start.
