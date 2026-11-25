---
term: Model provider
section: model
order: 10
short: The company or service that runs a model and sells access to it, such as Anthropic, OpenAI or a cloud host.
audience: public
related: [[Agent]], [[Input tokens]], [[Output tokens]], [[Parameters]], [[Prefix cache]], [[Session]], [[Turn]]
---
A provider hosts the [[Model]], takes each [[Model provider request]], runs [[Inference]] and bills for [[Token]]s. Different providers can serve the same open model at different prices, speeds and data terms.

The [[Harness]] decides which provider it calls.

## Heard in the wild

- Where does our code go when the agent runs?
- To the provider's API for each request; check their data terms for retention.
