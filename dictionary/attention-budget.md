---
term: Attention budget
section: failures
order: 41
short: The model's limited focus. Every token in the context spends some of it, useful or not.
audience: public
related: [[Attention degradation]], [[Attention relationship]], [[Clearing]], [[Context]], [[Session]], [[Smart zone]], [[Token]]
---
The [[Context window]] may be large, but the budget for paying attention to it is not. Noise such as stale logs, long tool output or abandoned plans takes focus away from the instructions you care about. Keep context lean, use [[Progressive disclosure]], and clear or hand off before the budget runs out.

## Heard in the wild

- Can't it just read everything?
- It can read it. It cannot weigh it all well at once.
