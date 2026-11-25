---
term: Token
section: model
order: 7
short: A small piece of text, often less than a word, that the model handles as one item. Context size, price and speed are all measured in them.
audience: public
related: [[Next-token prediction]], [[Training]]
---
Text is split into tokens before the [[Model]] sees it. A [[Context window]] holds a fixed number of them, and a [[Model provider]] charges per [[Input tokens|input token]], [[Output tokens|output token]] and [[Cache tokens|cached token]].

Code and unusual words tend to cost more tokens than plain English.

## Heard in the wild

- How big is this file to the model?
- About eleven thousand tokens; a twentieth of the window.

## Avoid

Counting words or characters and calling them tokens.
