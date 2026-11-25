---
term: Sandbox
section: tools
order: 34
short: Limits enforced outside the model on what the agent can read, write and reach on the network.
audience: public
related: [[AFK]], [[Agent mode]], [[Environment]], [[Human-in-the-loop]]
---
A sandbox is set by the operating system or the [[Harness]], so the [[Agent]] cannot argue its way out. It decides which parts of the [[Filesystem]] and the network a [[Tool call]] can touch. With a good sandbox you can use a looser [[Permission mode]] safely.

## Heard in the wild

- Is it safe to leave it running overnight?
- In the sandbox on its own clone, yes. Outside it, no.

## Avoid

Calling a prompt rule ("don't touch .env") a sandbox; only enforced limits count.

