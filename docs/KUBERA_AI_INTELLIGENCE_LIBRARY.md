# KUBERA AI Intelligence Library

A curated intelligence layer for studying external AI projects and turning useful ideas into stronger KUBERA systems.

> Principle: do not copy projects blindly. Study the architecture, understand the tradeoffs, reuse ideas only when licensing and design make sense, and keep KUBERA's protected implementation separate.

## How to read this library

Each entry answers four questions:

1. **What is it?**
2. **Why does it matter?**
3. **What can KUBERA learn from it?**
4. **What should we avoid copying blindly?**

---

## 1. OpenAI Agents SDK

Repository / docs: https://github.com/openai/openai-agents-python

**What it is:** a lightweight framework for agent tools, handoffs, guardrails, tracing and orchestration.

**Useful for KUBERA:**
- clear agent lifecycle;
- explicit tool calls;
- handoff patterns;
- tracing and observability;
- human-in-the-loop approval patterns.

**Potential KUBERA adaptation:** use these ideas to strengthen Human Control Levels, tool permissions, execution traces and resumable workflows.

**Do not copy blindly:** framework-specific abstractions may not fit a local-first architecture.

## 2. LangGraph

Docs: https://docs.langchain.com/oss/python/langgraph/overview

**What it is:** graph-based orchestration for stateful, long-running agents.

**Useful for KUBERA:**
- explicit state transitions;
- checkpoints;
- recoverable execution;
- long-running workflows;
- deterministic control around LLM calls.

**Potential KUBERA adaptation:** strengthen Execution Engine and Project Memory with state-machine concepts.

**Risk:** graphs can become complex quickly; KUBERA should keep simple tasks simple.

## 3. Pydantic AI

Repository / docs: https://github.com/pydantic/pydantic-ai

**What it is:** typed agent development based on Pydantic.

**Useful for KUBERA:**
- validated inputs and outputs;
- typed tools;
- structured failures;
- predictable contracts between modules.

**Potential KUBERA adaptation:** formalize Skill DNA and tool schemas so every skill has validated inputs, outputs and permission requirements.

## 4. LlamaIndex

Repository / docs: https://github.com/run-llama/llama_index

**What it is:** framework for ingestion, indexing, retrieval, agents and knowledge workflows.

**Useful for KUBERA:**
- document ingestion pipelines;
- retrieval abstractions;
- metadata-aware search;
- citation-oriented knowledge systems.

**Potential KUBERA adaptation:** strengthen Knowledge Store, Project Memory and Evidence Ledger.

**Risk:** avoid importing a huge framework when a small local retrieval layer is enough.

## 5. Haystack

Repository: https://github.com/deepset-ai/haystack

**What it is:** modular retrieval and generative AI pipeline framework.

**Useful for KUBERA:**
- pipeline composition;
- retrievers and generators as separate components;
- evaluation of retrieval quality.

**Potential KUBERA adaptation:** modular RAG pipelines and swappable retrieval components.

## 6. Docling

Repository: https://github.com/docling-project/docling

**What it is:** document parsing and conversion for AI applications.

**Useful for KUBERA:**
- PDF/document ingestion;
- structured extraction;
- document normalization before retrieval.

**Potential KUBERA adaptation:** safer document ingestion into Knowledge Store and Evidence Ledger.

## 7. LiteLLM

Repository: https://github.com/BerriAI/litellm

**What it is:** unified model gateway across many model providers.

**Useful for KUBERA:**
- provider abstraction;
- model fallback;
- cost tracking;
- routing across providers.

**Potential KUBERA adaptation:** Model Router should expose one internal interface while switching between local and remote models.

**Risk:** provider abstraction can hide important differences in model behaviour. Keep provider-specific metadata.

## 8. vLLM

Repository: https://github.com/vllm-project/vllm

**What it is:** high-performance inference and model-serving engine.

**Useful for KUBERA:**
- efficient serving;
- batching;
- local/private model infrastructure.

**Potential KUBERA adaptation:** future local model server for stronger hardware.

**Risk:** not suitable for every low-resource computer; hardware constraints matter.

## 9. Ollama

Repository: https://github.com/ollama/ollama

**What it is:** simple local model runtime and API.

**Useful for KUBERA:**
- easy local inference;
- model swapping;
- privacy-friendly experimentation;
- consistent local API.

**Potential KUBERA adaptation:** local provider behind Model Router for private/simple tasks.

## 10. llama.cpp

Repository: https://github.com/ggml-org/llama.cpp

**What it is:** efficient LLM inference in C/C++ across consumer hardware.

**Useful for KUBERA:**
- quantized models;
- CPU-friendly inference;
- low-level control;
- portable local execution.

**Potential KUBERA adaptation:** low-resource local execution path where heavier serving stacks are impractical.

## 11. OpenAI Evals

Repository: https://github.com/openai/evals

**What it is:** framework and registry for evaluating model/system behaviour.

**Useful for KUBERA:**
- repeatable evaluation cases;
- regression testing;
- measurable quality.

**Potential KUBERA adaptation:** every important skill should have acceptance tests before Agent Laboratory promotes it to trusted status.

## 12. Promptfoo

Repository: https://github.com/promptfoo/promptfoo

**What it is:** evaluation, model comparison and red-team testing for LLM apps.

**Useful for KUBERA:**
- prompt regression tests;
- side-by-side model comparisons;
- adversarial testing;
- structured assertions.

**Potential KUBERA adaptation:** benchmark Model Router choices and Self-Check effectiveness.

## 13. Ragas

Repository: https://github.com/explodinggradients/ragas

**What it is:** evaluation tooling for RAG and generative AI systems.

**Useful for KUBERA:**
- retrieval quality metrics;
- answer faithfulness;
- evidence quality.

**Potential KUBERA adaptation:** evaluate whether Evidence Ledger and retrieval actually improve grounded answers.

## 14. Langfuse

Repository: https://github.com/langfuse/langfuse

**What it is:** observability, tracing, prompt management and evaluation for LLM systems.

**Useful for KUBERA:**
- traces;
- cost/latency visibility;
- debugging agent chains;
- prompt versioning concepts.

**Potential KUBERA adaptation:** local/private observability layer for agent runs.

## 15. 12-Factor Agents

Repository: https://github.com/humanlayer/12-factor-agents

**What it is:** practical engineering principles for controllable agentic software.

**Useful for KUBERA:**
- deterministic software around probabilistic models;
- explicit state;
- small focused prompts;
- tools as software contracts.

**Potential KUBERA adaptation:** strong design reference for keeping the agent understandable and controllable.

## 16. Model Context Protocol (MCP)

Specification: https://modelcontextprotocol.io/specification/2026-07-28

**What it is:** open protocol for connecting AI applications to tools, prompts and data sources.

**Useful for KUBERA:**
- standard tool interface;
- reusable external capabilities;
- cleaner separation between agent and integrations.

**Potential KUBERA adaptation:** Skill DNA can expose selected capabilities through a standard protocol while Private/Public Gate controls access.

## 17. Agent2Agent (A2A)

Specification: https://a2a-protocol.org/latest/specification/

**What it is:** vendor-neutral protocol for agent discovery and task delegation.

**Useful for KUBERA:**
- multi-agent collaboration;
- remote task delegation;
- status and lifecycle concepts.

**Potential KUBERA adaptation:** future interoperability between specialized KUBERA agents without merging them into one giant agent.

## 18. OpenHands

Repository: https://github.com/All-Hands-AI/OpenHands

**What it is:** open platform for software-development agents.

**Useful for KUBERA:**
- sandboxed coding tasks;
- repository work;
- agent-computer interaction;
- failure recovery.

**Potential KUBERA adaptation:** safer coding skill with isolated workspace, tests and explicit approval before publishing.

## 19. Aider

Repository: https://github.com/Aider-AI/aider

**What it is:** terminal pair-programming agent with deep Git integration.

**Useful for KUBERA:**
- Git-aware edits;
- commit discipline;
- repository context;
- model-provider flexibility.

**Potential KUBERA adaptation:** Git Skill should understand diffs, branches, commits and tests rather than merely editing files.

## 20. OpenAI Codex CLI

Repository: https://github.com/openai/codex

**What it is:** coding agent designed to inspect and modify software projects under sandbox and approval controls.

**Useful for KUBERA:**
- sandbox-first execution;
- approval boundaries;
- repository-aware software work;
- command/tool control.

**Potential KUBERA adaptation:** execution permissions and human control for sensitive computer actions.

## 21. Cline

Repository: https://github.com/cline/cline

**What it is:** coding agent available through editor/CLI workflows.

**Useful for KUBERA:**
- tool-rich developer workflow;
- user approval loops;
- filesystem and terminal integration.

**Potential KUBERA adaptation:** desktop automation should expose actions individually and require approval by risk level.

## 22. Continue

Repository: https://github.com/continuedev/continue

**What it is:** open-source coding agents and developer workflows with source-controlled configuration.

**Useful for KUBERA:**
- configuration as code;
- reusable team rules;
- IDE/CI integration ideas.

**Potential KUBERA adaptation:** store agent policy, skill metadata and test requirements in version-controlled files.

---

# KUBERA extraction matrix

| External idea | KUBERA module to strengthen | Priority |
|---|---|---|
| Typed inputs/outputs | Skill DNA | High |
| Provider abstraction | Model Router | High |
| Local inference | Model Router / Runtime | High |
| Retrieval + citations | Knowledge Store / Evidence Ledger | High |
| State checkpoints | Execution Engine / Project Memory | High |
| Human approval | Human Control Levels | High |
| Tracing | Evidence Ledger / Runtime | High |
| Regression evals | Agent Laboratory / Self-Check | High |
| Sandboxed code execution | Tool Runtime | High |
| Standard tool protocol | Skill DNA / MCP adapter | Medium |
| Agent-to-agent delegation | Orchestration layer | Medium |
| Production observability | Runtime / diagnostics | Medium |

# What KUBERA should NOT become

- a clone of LangChain, OpenHands or any other project;
- a giant dependency stack that cannot run locally;
- a black box where the model can execute tools without permission;
- a memory system that stores everything forever;
- a router that chooses models only by price;
- an agent that calls itself successful without tests or evidence.

# KUBERA design doctrine derived from this research

1. **Small core, replaceable models.**
2. **Every tool has a contract and permission level.**
3. **Every important answer can carry evidence.**
4. **Every important skill has evals.**
5. **Failures become structured memory, not folklore.**
6. **Local-first where practical; cloud when justified.**
7. **Human approval increases with action risk.**
8. **External frameworks are references, not dependencies by default.**
9. **Architecture must remain understandable by a human owner.**
10. **A working tested feature is worth more than ten fashionable libraries.**

# Upstream curated source

A major discovery source for this library is:

- https://github.com/owainlewis/awesome-artificial-intelligence

The upstream project remains the canonical source for its own curation. This KUBERA library adds a different layer: **what each technology teaches us and how it maps to KUBERA architecture**.
