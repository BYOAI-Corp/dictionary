---
term: Tool
section: tools
order: 27
short: A function the harness offers the model: read a file, run a command, search, fetch a page.
audience: public
related: [[Agent]], [[Environment]], [[Filesystem]], [[Model provider request]], [[Token]]
---
A tool is described in the [[Context]] so the [[Model]] can ask for it by name. The model only asks; the [[Harness]] runs the [[Tool call]] and returns a [[Tool result]]. [[MCP]] is a common way to add tools.

## Heard in the wild

- Can it query our database?
- Only if we give it a tool for that, read-only.
