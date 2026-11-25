---
term: System prompt
section: sessions
order: 22
short: The standing instructions the harness puts at the top of every request, before the conversation.
audience: public
related: [[Agent]], [[Harness]], [[Input tokens]], [[Model]], [[Session]], [[Token]], [[Tool]], [[Turn]]
---
The system prompt sets role, rules and tool use. It sits at the front of the [[Context]], so it is part of the [[Prefix cache]] and is reread on every [[Model provider request]]. Project rules in [[AGENTS.md]] usually end up next to it.

## Heard in the wild

- Why does it keep adding emojis?
- The app's system prompt asks for a friendly tone. Override it in your own instructions.
