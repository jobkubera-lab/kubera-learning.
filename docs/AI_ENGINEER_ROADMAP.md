# KUBERA AI Engineer Roadmap

A practical path from AI user to builder of reliable AI agents and local AI systems.

> This roadmap is curated for KUBERA LAB. It links to original sources instead of copying their content.

## 0. How to use this roadmap

Do not try to read everything. For every stage: learn one concept, build one small artifact, test it, document what failed, then move forward.

**Loop:** Learn → Build → Test → Explain → Improve.

## Stage 1 — Python, Git and software foundations

Learn enough Python and Git to read, modify, test and publish AI code.

**Build:** a command-line Python tool with tests and a clean README.

## Stage 2 — Machine learning and neural networks

Understand training, inference, loss, overfitting, embeddings, neural networks and transformers.

Recommended starting points:
- [Fast.ai Practical Deep Learning](https://course.fast.ai/)
- [Karpathy: Neural Networks — Zero to Hero](https://www.youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ)
- [MIT 6.S191](https://introtodeeplearning.com/)
- [Understanding Deep Learning](https://udlbook.github.io/udlbook/)

**Build:** a small neural-network experiment and explain the result in plain language.

## Stage 3 — LLM foundations

Learn tokenization, embeddings, attention, transformers, context windows, inference and fine-tuning.

Recommended:
- [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1)
- [Build a Large Language Model from Scratch](https://www.manning.com/books/build-a-large-language-model-from-scratch)
- [The 100-Page Language Models Book](https://www.thelmbook.com/)
- [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
- [LoRA](https://arxiv.org/abs/2106.09685)

**Build:** a minimal LLM application that accepts structured input and produces validated structured output.

## Stage 4 — AI application engineering

Move from prompts to systems: tools, structured outputs, retrieval, state and failure handling.

Recommended:
- [OpenAI Cookbook](https://cookbook.openai.com/)
- [Anthropic Prompt Engineering](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview)
- [12-Factor Agents](https://github.com/humanlayer/12-factor-agents)
- [OWASP Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/)

**Build:** an assistant that uses at least one external tool and validates its answer before returning it.

## Stage 5 — RAG, documents and knowledge

Learn ingestion, chunking, embeddings, retrieval, citations and document parsing.

Recommended:
- [LlamaIndex](https://docs.llamaindex.ai/)
- [Haystack](https://docs.haystack.deepset.ai/)
- [Docling](https://github.com/docling-project/docling)
- [Retrieval-Augmented Generation paper](https://arxiv.org/abs/2005.11401)

**Build:** a local knowledge assistant that answers from a controlled document collection and shows evidence.

## Stage 6 — Agents and orchestration

This is the key stage for KUBERA AGENT OS.

Recommended:
- [Anthropic — Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents)
- [OpenAI — Practical Guide to Building Agents](https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf)
- [OpenAI Agents SDK](https://openai.github.io/openai-agents-python/)
- [LangGraph](https://docs.langchain.com/oss/python/langgraph/overview)
- [Pydantic AI](https://ai.pydantic.dev/)
- [ReAct paper](https://arxiv.org/abs/2210.03629)

**Build:** an agent with tools, explicit permissions, memory boundaries, human approval for risky actions and a failure log.

## Stage 7 — Protocols and interoperability

Learn how agents connect to tools and to other agents.

- [Model Context Protocol](https://modelcontextprotocol.io/specification/2026-07-28)
- [Agent2Agent Protocol](https://a2a-protocol.org/latest/specification/)

**Build:** expose one safe tool through a standard protocol and document its permission model.

## Stage 8 — Evals, safety and reliability

A useful agent must be measurable, not merely impressive in a demo.

Recommended:
- [Anthropic — Demystifying Evals for AI Agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [OpenAI Evals](https://github.com/openai/evals)
- [Promptfoo](https://www.promptfoo.dev/docs/)
- [Ragas](https://docs.ragas.io/)

**Build:** a test suite with success criteria, adversarial cases, regression tests and a scorecard.

## Stage 9 — Local AI and model serving

For privacy, resilience and cost control, learn local inference and model routing.

Recommended:
- [vLLM](https://docs.vllm.ai/)
- [LiteLLM](https://docs.litellm.ai/)
- Hugging Face ecosystem and model documentation

**Build:** route simple tasks to a local model and harder tasks to a stronger provider while logging cost, latency and quality.

## Stage 10 — Durable agents and human control

Long-running agents need retries, checkpoints, resumability and human intervention.

Recommended:
- [Anthropic — Effective Harnesses for Long-Running Agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents)
- [OpenAI Agents SDK — Running Agents](https://openai.github.io/openai-agents-python/running_agents/)
- [OpenAI Agents SDK — Human in the Loop](https://openai.github.io/openai-agents-python/human_in_the_loop/)

**Build:** a multi-step task that can stop, persist state, request approval and safely resume.

## Stage 11 — Coding agents

Study how modern coding agents inspect repositories, edit files, run tests and recover from errors.

Explore:
- [OpenAI Codex](https://github.com/openai/codex)
- [Gemini CLI](https://github.com/google-gemini/gemini-cli)
- [Aider](https://aider.chat/)
- [OpenHands](https://docs.all-hands.dev/)
- [Cline](https://github.com/cline/cline)

**Build:** a constrained coding-agent experiment that can only modify an isolated test repository and must pass tests before proposing a change.

## Stage 12 — Production AI engineering

Learn observability, deployment, cost control, secrets, permissions, rollback and incident handling.

Recommended:
- [Full Stack Deep Learning](https://fullstackdeeplearning.com/)
- [Made With ML](https://madewithml.com/)
- [Langfuse](https://langfuse.com/docs)

**Build:** deploy one AI service with tracing, evaluation, health checks and documented failure modes.

---

## KUBERA specialization track

The roadmap should feed directly into these KUBERA AGENT OS capabilities:

1. Model Router — choose models by task, privacy, cost and quality.
2. Skill DNA — reusable, permissioned agent skills.
3. Evidence Ledger — retain sources and evidence behind important outputs.
4. Self-Check — verify outputs before action or publication.
5. Private/Public Gate — control what may leave the local environment.
6. Project Memory — durable project context without uncontrolled memory growth.
7. Failure Memory — learn from recurring operational failures.
8. Human Control Levels — explicit approval boundaries.
9. Agent Laboratory — test skills and agents before promotion to trusted use.
10. Evals — measurable acceptance criteria for every important skill.

## Primary curated source

This roadmap was inspired in part by the actively maintained [awesome-artificial-intelligence](https://github.com/owainlewis/awesome-artificial-intelligence) collection by Owain Lewis. The original repository is MIT licensed and remains the canonical source for its curated list.

We intentionally link to original resources rather than duplicating the upstream catalogue.

## Rule for adding new resources

A resource belongs here only if it helps us **understand, build, test, secure or operate** real AI systems. Popularity alone is not enough.
