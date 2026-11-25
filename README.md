# The BYOAI dictionary of AI coding

The words people use when they build software with AI agents, each with a short and a full
definition, how people say it, what to avoid, and the terms it connects to. 72 terms in 7
sections, written in BYOAI's own words.

The notes are plain Markdown with `[[links]]` between terms, so the `dictionary` folder opens as an
[Obsidian](https://obsidian.md) vault and draws the same map. The same notes feed the Dictionary
pages on BYOAI's sites. Every release is sealed and verifiable: see [Verify a release](#verify-a-release).

## The model (16)

What a model is, how it is run and what it costs.

- [AI](dictionary/ai.md): The umbrella word. In coding talk it almost always means a large language model behind a chat or an agent.
- [Model](dictionary/model.md): The trained network itself: a large file of numbers that turns input tokens into a prediction of the next one.
- [Parameters](dictionary/parameters.md): The learned numbers inside a model. More parameters usually means more capacity and more cost per token.
- [Training](dictionary/training.md): How a model is made. Months of compute over a vast pile of text and code fix its parameters; after that it changes only with a new release.
- [Inference](dictionary/inference.md): Running a trained model: tokens in, predicted tokens out. Every reply you get is inference.
- [Effort](dictionary/effort.md): A setting you choose per request. Turn it up for a tricky bug or a design call and pay in time and tokens; turn it down for quick edits.
- [Token](dictionary/token.md): A small piece of text, often less than a word, that the model handles as one item. Context size, price and speed are all measured in them.
- [Next-token prediction](dictionary/next-token-prediction.md): The one trick under every answer. The model scores possible continuations, takes one token, adds it to the text and runs again until it stops.
- [Non-determinism](dictionary/non-determinism.md): The same prompt can give different answers. Sampling, model updates and small context changes all move the output.
- [Model provider](dictionary/model-provider.md): The company or service that runs a model and sells access to it, such as Anthropic, OpenAI or a cloud host.
- [Harness](dictionary/harness.md): The program around a model that gives it tools, rules, memory and a loop: Claude Code, a chat app, an IDE plugin.
- [Model provider request](dictionary/model-provider-request.md): One call to the provider's API: the whole context goes in, one reply comes out. An agent makes many per task.
- [Input tokens](dictionary/input-tokens.md): The tokens you send with a request: prompt, history, files, tool results. Usually the biggest part of an agent's bill.
- [Output tokens](dictionary/output-tokens.md): The tokens the model writes back, including any thinking. Priced higher per token than input.
- [Prefix cache](dictionary/prefix-cache.md): The provider keeps the start of a recent context ready, so a request that begins the same way is cheaper and faster.
- [Cache tokens](dictionary/cache-tokens.md): Input tokens served from the prefix cache, billed at a discount. Writing to the cache may cost a little extra.

## Sessions, context windows and turns (8)

What the model sees on each request, and how a conversation is built.

- [Stateless](dictionary/stateless.md): The model keeps nothing between requests. Whatever it should remember has to be sent again each time.
- [Context](dictionary/context.md): Everything the model is given for one request: instructions, history, files, tool results.
- [Context window](dictionary/context-window.md): The fixed number of tokens a model can see at once. Anything outside it does not exist for that request.
- [Stateful](dictionary/stateful.md): Something that carries information from one step to the next. A chat feels stateful because the harness resends history.
- [Agent](dictionary/agent.md): A model in a loop with tools: it plans, calls a tool, reads the result, and decides what to do next until the job is done.
- [System prompt](dictionary/system-prompt.md): The standing instructions the harness puts at the top of every request, before the conversation.
- [Session](dictionary/session.md): One running conversation with its history. A new session starts with an empty context.
- [Turn](dictionary/turn.md): From the moment you send a message until the agent stops and waits for you again, however many steps it takes in between.

## Tools and environment (10)

How an agent acts: tools, permissions and the sandbox around it.

- [Environment](dictionary/environment.md): Where the agent acts: the machine, folder, shell, network and services its tools can reach.
- [Filesystem](dictionary/filesystem.md): The files and folders the agent can read and write. Most of its work happens here.
- [Tool](dictionary/tool.md): A function the harness offers the model: read a file, run a command, search, fetch a page.
- [Tool call](dictionary/tool-call.md): The model asking the harness to run a tool with given arguments. The harness decides whether to allow it.
- [Tool result](dictionary/tool-result.md): The reply to a tool call, added to the conversation so the next turn can use it. A file read, a test run's output, or the error that stopped it.
- [MCP](dictionary/mcp.md): Model Context Protocol: a standard way to plug tools and data sources into any harness that speaks it.
- [Permission request](dictionary/permission-request.md): The harness pausing to ask you before a tool call runs, because the permission mode says so.
- [Permission mode](dictionary/permission-mode.md): The harness setting for how much the agent may do without asking: ask for everything, allow edits, or run freely.
- [Agent mode](dictionary/agent-mode.md): A harness setting where the model may act with tools over many steps, rather than only answering.
- [Sandbox](dictionary/sandbox.md): Limits enforced outside the model on what the agent can read, write and reach on the network.

## Failure modes (9)

How and why models go wrong, and what to do about it.

- [Sycophancy](dictionary/sycophancy.md): The model's pull to agree with you, praise your idea or back down when you push, whether or not you are right.
- [Hallucination](dictionary/hallucination.md): A confident answer that is not true: an invented function, a wrong citation, a made-up fact.
- [Parametric knowledge](dictionary/parametric-knowledge.md): Facts and habits baked into the weights. Nothing you type adds to it; it only covers the world up to the cutoff, and it can be vague on detail.
- [Knowledge cutoff](dictionary/knowledge-cutoff.md): The date the training data ends. The model knows nothing after it unless it is told in context.
- [Contextual knowledge](dictionary/contextual-knowledge.md): What the model knows because it is in the current context: the files, docs and results you gave it.
- [Attention relationship](dictionary/attention-relationship.md): Each token weighs every other token in the window. The more there is, the more relationships compete.
- [Attention budget](dictionary/attention-budget.md): The model's limited focus. Every token in the context spends some of it, useful or not.
- [Attention degradation](dictionary/attention-degradation.md): Quality falling as the context fills: forgotten instructions, repeated mistakes, contradicting itself.
- [Smart zone](dictionary/smart-zone.md): The early part of a context window where the model still reasons sharply, well before the hard limit.

## Handoffs (9)

Moving work between sessions, agents and people without losing the truth.

- [Clearing](dictionary/clearing.md): Emptying the context and starting over in the same harness. Cheap and clean, and it forgets everything.
- [Handoff](dictionary/handoff.md): Passing work to a fresh session, another agent or a person, with what they need written down.
- [Primary source](dictionary/primary-source.md): The thing itself: the code, the test output, the actual document. Not someone's account of it.
- [Secondary source](dictionary/secondary-source.md): A description of the thing: a summary, a ticket's retelling, an agent's report. Useful and lossy.
- [Handoff artifact](dictionary/handoff-artifact.md): The file left for whoever picks the work up: what was done, what is next, where the truth lives.
- [Spec](dictionary/spec.md): A written description of what to build and why, settled before the build starts.
- [Ticket](dictionary/ticket.md): One unit of work on the tracker, small enough for one session, with what blocks it stated.
- [Compaction](dictionary/compaction.md): Replacing a long history with a summary of it, so the session can go on in less space.
- [Autocompact](dictionary/autocompact.md): Compaction you did not ask for: once the window is close to its limit, the harness summarises the session by itself and carries on.

## Memory and steering (7)

Carrying knowledge across sessions and loading it only when needed.

- [Memory system](dictionary/memory-system.md): Anything that carries knowledge across sessions: rule files, notes, a database the harness reads back in.
- [AGENTS.md](dictionary/agents-md.md): A file of standing instructions the harness loads into every session for a repo (CLAUDE.md in Claude Code).
- [Progressive disclosure](dictionary/progressive-disclosure.md): Giving the agent a short index first and the details only when it needs them.
- [Context pointer](dictionary/context-pointer.md): A short reference in context to where fuller information lives: a path, a doc name, a command.
- [Skill](dictionary/skill.md): A packaged set of instructions, and sometimes scripts, that the agent loads only when the task calls for it.
- [Subagent](dictionary/subagent.md): A second agent started by the first for one focused task, with its own fresh context; it reports back a summary.
- [Home Repo](dictionary/home-repo.md): A repository that holds your agent setup itself: skills, rule files and notes, shared across projects.

## Patterns of work (13)

Ways of working with agents, from watching every step to a factory.

- [Human-in-the-loop](dictionary/human-in-the-loop.md): Working with the agent step by step, watching and steering as it goes.
- [AFK](dictionary/afk.md): Away from keyboard: the agent works on its own for a while and you check the result afterwards.
- [Automated check](dictionary/automated-check.md): A test, type check, linter or build that passes or fails on its own, with no judgement involved.
- [Automated review](dictionary/automated-review.md): A model reading the change and judging it: against the standards, against the spec, for risk.
- [Human review](dictionary/human-review.md): A person reading the change and deciding whether it ships.
- [Vibe coding](dictionary/vibe-coding.md): Building by prompting and accepting whatever comes back, without reading the code closely.
- [Design concept](dictionary/design-concept.md): The shared idea of how something should work, held by you and the agent before code is written.
- [Grilling](dictionary/grilling.md): Letting the agent interview you, question by question, until the plan has no open gaps.
- [Prototyping](dictionary/prototyping.md): Throwaway code written to answer one question, then kept as evidence and not shipped.
- [DX](dictionary/dx.md): Developer experience: how easy and pleasant a code base or tool is for people to work with.
- [AX](dictionary/ax.md): Agent experience: how easy a code base is for an agent to understand, change and check.
- [Software factory](dictionary/software-factory.md): A set-up where agents take tickets from a backlog and turn them into reviewed changes, with people setting goals and approving.
- [Dark factory](dictionary/dark-factory.md): A factory with nobody watching: agents plan, build, review and ship on their own.

## Verify a release

```bash
sha256sum -c MANIFEST.sha256
cargo install --locked --git https://github.com/byoai-corp/verify byoai-release
byoai-release verify . --pubkey "$(cat BYOAI_RELEASE_PUBKEY)"
```

`VERIFIED` means every file is exactly what BYOAI sealed. The checker is open source
([byoai-corp/verify](https://github.com/byoai-corp/verify)); BYOAI's public key is in
`BYOAI_RELEASE_PUBKEY`; check it matches the one pinned on https://github.com/byoai-corp.

## Licence

The text is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/).
Use it, adapt it and share it; credit "BYOAI dictionary" with a link to this repository.
