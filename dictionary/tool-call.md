---
term: Tool call
section: tools
order: 28
short: The model asking the harness to run a tool with given arguments. The harness decides whether to allow it.
audience: public
related: [[Agent]], [[Model]], [[Model provider request]], [[Next-token prediction]], [[System prompt]], [[Turn]]
---
A tool call is text in the model's output that names a [[Tool]] and its arguments. The [[Harness]] checks it against the [[Permission mode]], may raise a [[Permission request]], runs it in the [[Environment]], and adds the [[Tool result]] to the [[Context window]].

## Heard in the wild

- Why did it stop?
- It wanted to run rm and the permission mode asks first.
