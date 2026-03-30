<div align="center">

# 🤖 Awesome Autonomous AI Agents

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
![GitHub stars](https://img.shields.io/badge/entries-90%2B-blue?style=flat-square)
![Last Updated](https://img.shields.io/badge/updated-March_2026-brightgreen?style=flat-square)
![License](https://img.shields.io/badge/license-CC0_1.0-lightgrey?style=flat-square)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-ff69b4?style=flat-square)

**A curated list of truly exceptional autonomous AI agent frameworks, tools, benchmarks, and papers.**

[Frameworks](#-general-purpose-frameworks) · [OpenClaw Ecosystem](#-the-openclaw-ecosystem) · [Coding Agents](#-coding-agents) · [Multi-Agent](#-multi-agent-systems) · [Web & Browser](#-web--browser-agents) · [Chinese Contributions](#-chinese-contributions) · [Benchmarks](#-benchmarks--evaluation) · [Papers](#-foundational-papers)

</div>

---

## Why this list?

The AI agent space exploded in 2023 and hasn't stopped. Hundreds of repos claim to be "autonomous agent frameworks." Most are weekend wrappers around API calls. **This list only includes projects that moved the field forward** — frameworks with real architectural ideas, benchmarks that changed how we evaluate agents, and papers that introduced paradigms now used everywhere.

Every entry was verified for active development status, genuine technical contribution, and community adoption. Chinese-origin projects are marked with 🇨🇳 — the Chinese AI ecosystem has produced some of the most impactful agent work and deserves first-class visibility.

> **Selection criteria:** Novel architecture OR significant community adoption (1,000+ ★) OR foundational paper (100+ citations) OR production deployment at scale. No vaporware, no thin wrappers.

---

## Contents

- [🏗️ General-Purpose Frameworks](#%EF%B8%8F-general-purpose-frameworks)
- [🐾 The OpenClaw Ecosystem](#-the-openclaw-ecosystem)
- [💻 Coding Agents](#-coding-agents)
- [👥 Multi-Agent Systems](#-multi-agent-systems)
- [🌐 Web & Browser Agents](#-web--browser-agents)
- [🖥️ Computer Use & GUI Agents](#%EF%B8%8F-computer-use--gui-agents)
- [🔬 Research & Science Agents](#-research--science-agents)
- [🧠 Memory & Knowledge Systems](#-memory--knowledge-systems)
- [🔧 Tool-Use & Function Calling](#-tool-use--function-calling)
- [🧩 Planning & Reasoning Frameworks](#-planning--reasoning-frameworks)
- [🇨🇳 Chinese Contributions](#-chinese-contributions)
- [📊 Benchmarks & Evaluation](#-benchmarks--evaluation)
- [🔗 Protocols & Standards](#-protocols--standards)
- [📄 Foundational Papers](#-foundational-papers)
- [📚 Surveys & Curated Lists](#-surveys--curated-lists)
- [Contributing](#contributing)

---

## 🏗️ General-Purpose Frameworks

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [AutoGPT](https://github.com/Significant-Gravitas/AutoGPT) | ~183k ★ | The original autonomous GPT-4 agent (April 2023), now evolved into a visual agent-builder platform with marketplace and cloud deployment. | **Pioneered autonomous agents** — defined the category; most-starred agent repo on all of GitHub. |
| [LangGraph](https://github.com/langchain-ai/langgraph) | ~27k ★ | Low-level graph-based orchestration for stateful agents  with durable execution, human-in-the-loop, and streaming.  | **Most downloaded agent framework** (~34.5M monthly PyPI downloads);  Pregel/Apache Beam–inspired execution model.  |
| [AutoGen / AG2](https://github.com/microsoft/autogen) | ~54k ★ | Microsoft's multi-agent conversation framework;  AG2 ([ag2ai/ag2](https://github.com/ag2ai/ag2)) is the community fork continuing active development. | **Best Paper at ICLR 2024 LLM Agents Workshop**;  defined the multi-agent conversation paradigm. Now merging into Microsoft Agent Framework with Semantic Kernel.  |
| [CrewAI](https://github.com/crewAIInc/crewAI) | ~44k ★ | Standalone framework for orchestrating role-playing AI agents with "Crews" (collaborative teams) and "Flows" (event-driven pipelines).  | **1.4B agentic automations** claimed; 60% of Fortune 500 as users.  Fully independent of LangChain.  |
| [Semantic Kernel](https://github.com/microsoft/semantic-kernel) | ~27k ★ | Microsoft's enterprise SDK  for .NET, Python, and Java with planners, function-calling, and deep Azure integration.  | **Enterprise-first** — merging with AutoGen into unified Microsoft Agent Framework (GA Q1 2026).  |
| [smolagents](https://github.com/huggingface/smolagents) | ~25k ★ | HuggingFace's minimal agent library  where agents write Python code as actions. ~1,000 lines of core logic.  | **Radical simplicity** — code-as-action paradigm  with Hub integrations for sharing tools. Sandboxed execution via E2B/Docker.  |
| [Agno](https://github.com/agno-agi/agno) | ~26k ★ | High-performance multi-modal agent runtime  (formerly Phidata) with memory, knowledge graphs, and MCP support.  | **Claims 5,000× faster** than LangGraph;  levels 0–3 of progressive agent autonomy. |
| [PydanticAI](https://github.com/pydantic/pydantic-ai) | ~15k ★ | Type-safe, code-first agent framework using Python type hints  — the "FastAPI for agents."  | **Zero magic** — built for senior Python teams wanting explicit control over every agent decision.  |
| [Open Interpreter](https://github.com/openinterpreter/open-interpreter) | ~62k ★ | Natural-language interface that lets LLMs run code locally — open-source alternative to OpenAI Code Interpreter. | **Full local access** — no internet restrictions, file size limits, or time limits.  Supports `--os` mode for computer control. |
| [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) | ~19k ★ | Lightweight, production-ready Python SDK (evolution from Swarm) with built-in web search, file search, and computer use tools. | **Official OpenAI agent primitive** — designed as the canonical way to build agents with OpenAI models. |
| [Google ADK](https://github.com/google/adk-python) | ~17k ★ | Code-first agent toolkit optimized for Gemini with Agent-to-Agent (A2A) protocol support and MCP Toolbox for Databases.  | **A2A-native** — first framework with built-in support for Google's agent interoperability protocol. Model-agnostic via LiteLLM.  |
| [Mastra](https://github.com/mastra-ai/mastra) | ~19k ★ | TypeScript-first agent framework from the Gatsby team with workflows, RAG, evals, and tool calling. 300k+ weekly npm downloads.  | **Fills the JS/TS gap** — native OpenTelemetry, workflow engine, and first-class TypeScript support.  |
| [Strands Agents](https://github.com/strands-agents/sdk-python) | Growing | AWS's model-agnostic agent framework with optional deep Bedrock integrations and first-class OpenTelemetry tracing.  | **AWS-native** — production-ready with deep AWS service integrations while remaining model-agnostic. |
| [DSPy](https://github.com/stanfordnlp/dspy) | ~33k ★ | Stanford's framework for *programming* (not prompting) LLMs — compiles declarative calls into self-improving pipelines with optimizers.  | **Paradigm-shifting** — replaces prompt engineering with compiled, optimizable programs.  ICLR 2024 paper. MIPROv2 optimizer. |
| [Haystack](https://github.com/deepset-ai/haystack) | ~23k ★ | Production-ready orchestration framework  for NLP/AI pipelines with retrieval, generation, and agent components. | **Mature production tooling** — battle-tested since pre-LLM era; comprehensive pipeline abstraction for RAG and agents. |

---

## 🐾 The OpenClaw Ecosystem

OpenClaw is the fastest-growing open-source project in GitHub history,  spawning **52+ derivatives across 9 programming languages**  as of March 2026. Community directory: [shelldex.com](https://shelldex.com/).

### Core Projects

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [OpenClaw](https://github.com/openclaw/openclaw) | ~337k ★ | Messaging-native autonomous personal AI agent connecting through 20+ platforms (WhatsApp, Telegram, Slack, Discord, Signal, iMessage, WeChat, etc.).  8 core agents, SOUL.md personality config, ClawHub skill marketplace (13,700+ skills).  | **Defined a new category** — always-on, messaging-native autonomous agents. Beat React's 10-year star record in ~60 days. Created by Peter Steinberger; transferred to independent foundation after he joined OpenAI.  |
| [NemoClaw](https://github.com/NVIDIA/NemoClaw) | ~16k ★ | NVIDIA's enterprise security wrapper for OpenClaw — adds OS-level sandboxing  (Landlock + seccomp + network namespaces), default-deny networking, YAML policy engine, and privacy routing to local Nemotron models.  | **Enterprise-grade security layer** — not a standalone agent but the missing security infrastructure for OpenClaw. Launched at GTC 2026.  Hardware-agnostic despite NVIDIA origin.  |
| [Hermes Agent](https://github.com/NousResearch/hermes-agent) | ~14k ★ | NousResearch's self-improving personal AI agent with built-in RL training via Atropos, GEPA-based skill evolution, and cross-session memory. Multi-platform gateway (Telegram, Discord, Slack, WhatsApp, Signal).  | **Only agent with a closed-loop learning system** — uses GEPA (ICLR 2026 Oral)  + DSPy to optimize its own skills from execution traces.  `hermes claw migrate` imports from OpenClaw.  |

### Major Rewrites & Alternatives

| Project | Stars | Language | Key Differentiator |
|---------|-------|----------|--------------------|
| [Nanobot](https://github.com/HKUDS/nanobot) | ~33k ★ | Python | Ultra-lightweight (~4,000 lines vs OpenClaw's ~430,000); research-ready with minimal dependencies.  |
| [ZeroClaw](https://github.com/zeroclaw/zeroclaw) | ~27k ★ | Rust | 99% less RAM than OpenClaw; 10ms cold boot; targets edge/IoT devices.  |
| [NanoClaw](https://github.com/qwibitai/nanoclaw) | ~26k ★ | TypeScript | Container-first security — every agent runs in an isolated Linux container by default.  |
| [PicoClaw](https://github.com/sipeed/picoclaw) | ~13k ★ | Go | Runs on $10 hardware with <10MB RAM; built for embedded and edge deployments.  |
| [OpenFang](https://github.com/openfang/openfang) | Growing | Rust | "Agent Operating System" with 7 autonomous modules, 38 tools, and 40 messaging channels.  |
| [Moltis](https://github.com/moltis/moltis) | ~2k ★ | Rust | Enterprise Rust — 150K lines with zero unsafe blocks; native Prometheus/Grafana observability.  |

### Ecosystem Tools

| Project | Description |
|---------|-------------|
| [awesome-openclaw-agents](https://github.com/mergisi/awesome-openclaw-agents) | 187 production-ready agent templates across 24 categories.  |
| [hermes-agent-self-evolution](https://github.com/NousResearch/hermes-agent-self-evolution) | GEPA-based self-improvement module for Hermes Agent.  |
| [claw0](https://github.com/shareAI-lab/claw0) | Educational 10-section tutorial for building an OpenClaw-compatible agent from scratch.  |
| [ClawWork](https://github.com/HKUDS/ClawWork) | Agents that earn income from professional tasks and pay for their own token usage  — earned $15K in 11 hours.  |

---

## 💻 Coding Agents

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [OpenHands](https://github.com/OpenHands/OpenHands) | ~69k ★ | Open-source AI software development platform — modifies code, runs terminals, browses the web, executes multi-step dev tasks in Docker sandboxes.  | **Most-starred coding agent on GitHub.** 77.6% on SWE-bench Verified. Model-agnostic. $18.8M Series A (All Hands AI).  |
| [Aider](https://github.com/Aider-AI/aider) | ~41k ★ | AI pair programming in your terminal  — every AI edit auto-committed to git.  Builds a map of your entire codebase for context.  | **Git-native workflow** — terminal-first, BYOM, top SWE-bench scores. Aider wrote 21% of its own recent code.  |
| [GPT-Engineer](https://github.com/AntonOsika/gpt-engineer) | ~55k ★ | Specify what you want built and it generates the entire codebase. Asks clarifying questions, writes specs, then codes.  | **Precursor to Lovable.dev** — one of the first "prompt-to-codebase" tools. Now mostly archived; commercial product spun out. |
| [GPT-Pilot](https://github.com/Pythagora-io/gpt-pilot) | ~33k ★ | AI developer with "95% AI / 5% human" paradigm — writes full features while keeping human-in-the-loop for review. Agent roles: Architect, Developer, etc. | **Human-in-the-loop by design** — YC W24 backed. Powers the Pythagora VS Code extension. |
| [SWE-agent](https://github.com/SWE-agent/SWE-agent) | ~19k ★ | Takes a GitHub issue and automatically fixes it.  Introduced the Agent-Computer Interface (ACI) concept.  Also handles cybersecurity CTFs via EnIGMA mode.  | **NeurIPS 2024 paper.** SoTA on SWE-bench with Claude 3.7. Open-weights SWE-agent-LM-32b. Princeton + Stanford.  |
| [Devin](https://www.cognition.ai/) | N/A | First widely-publicized fully autonomous AI software engineer — plans, codes, debugs, deploys with its own shell, editor, and browser.  | **Proprietary but category-defining.** 13.86% on SWE-bench at launch (vs 1.96% prior SOTA). Cognition valued at $billions. Acquired Windsurf. |
| [Cursor](https://cursor.com/) | N/A | AI-native code editor  (VS Code fork) with Tab completion, Composer multi-file edits, and agent mode. | **$1B ARR in <24 months**, $29.3B valuation.  50%+ of Fortune 500. Proprietary but sets the standard for AI-assisted coding. |

---

## 👥 Multi-Agent Systems

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [MetaGPT](https://github.com/FoundationAgents/MetaGPT) 🇨🇳 | ~58k ★ | Simulates an entire software company — product managers, architects, and engineers collaborate via SOPs to turn one-line requirements into working code. | **ICLR 2024 Oral (top 1.2%).**  Philosophy: "Code = SOP(Team)."  Also produced AFlow (ICLR 2025 oral).  DeepWisdom (Chinese company). |
| [ChatDev](https://github.com/OpenBMB/ChatDev) 🇨🇳 | ~32k ★ | Chat-powered virtual software company.  Now ChatDev 2.0: zero-code multi-agent orchestration platform for "Developing Everything."  | **NeurIPS 2025 paper** on evolving orchestration.  From Tsinghua/OpenBMB. Bilingual docs (CN/EN). |
| [CAMEL](https://github.com/camel-ai/camel) 🇨🇳 | ~15k ★ | Pioneering role-playing framework for multi-agent cooperation — agents assume roles and collaborate via inception prompting.  | **First multi-agent framework (March 2023).** NeurIPS 2023. Training data used in Microsoft Phi and OpenHermes. OWL subproject hit #1 on GAIA benchmark.  |
| [AgentVerse](https://github.com/OpenBMB/AgentVerse) 🇨🇳 | ~5k ★ | Dual-framework design: task-solving mode (collaborative problem-solving) and simulation mode (observing emergent behaviors).  | **Unique simulation capabilities** — observe and study emergent multi-agent behaviors. OpenBMB/Tsinghua. |
| [Generative Agents](https://github.com/joonspk-research/generative_agents) | ~21k ★ | 25 AI agents inhabiting "Smallville" — they form relationships, gossip, coordinate events, all emerging from memory + reflection + planning.  | **Landmark UIST 2023 paper.** Stanford (Park, Liang, Bernstein).  Introduced "believable simulacra of human behavior." |
| [Agency Swarm](https://github.com/VRSEN/agency-swarm) | Growing | Framework for creating collaborative AI agent swarms with role-based organization and inter-agent communication. | **Swarm-native** — agents self-organize with customizable communication topologies. |

---

## 🌐 Web & Browser Agents

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [Browser Use](https://github.com/browser-use/browser-use) | ~55k ★ | Open-source framework enabling LLMs to control browsers  for web automation. Claims 89% on WebVoyager (SOTA).  | **Y Combinator backed.**  Released open-source bu-30b model. MIT licensed.  Cloud offering available.  |
| [GPT Researcher](https://github.com/assafelovic/gpt-researcher) | ~26k ★ | Autonomous deep research agent — scrapes and synthesizes 20+ web sources to produce factual, cited research reports.  | **Original open-source deep research agent** (May 2023, predating the "deep research" trend by ~2 years).  Created by Tavily founder. |
| [BrowserGym](https://github.com/ServiceNow/BrowserGym) | Growing | Unified gym-like environment for web agent research — standardized observation/action spaces  across WebArena, MiniWoB, WorkArena, etc. | **TMLR 2025 paper.** ServiceNow. De facto standard for web agent evaluation infrastructure. |
| [MindSearch](https://github.com/InternLM/MindSearch) 🇨🇳 | ~5k ★ | LLM-based multi-agent web search engine (like Perplexity Pro). Supports DuckDuckGo, Bing, Brave, Google, Tencent search backends.  | **Open-source Perplexity alternative** from Shanghai AI Lab. Bilingual (CN/EN) query support. |

---

## 🖥️ Computer Use & GUI Agents

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [Agent TARS / UI-TARS](https://github.com/bytedance/UI-TARS-desktop) 🇨🇳 | ~10k ★ | ByteDance's multimodal AI agent stack — CLI and Web UI for browser automation + native GUI automation with remote computer/browser operators. | **Pioneering GUI agent paper** (arXiv:2501.12326). Ships as both CLI agent and desktop application. |
| [AppAgent](https://github.com/TencentQQGYLab/AppAgent) 🇨🇳 | ~5k ★ | Multimodal agent that operates smartphone apps through tap/swipe — two-phase approach: exploration (learning) then deployment (executing).  | **Mobile-first agent.** Tencent. Tested on 50 tasks across 10 apps.  Supports GPT-4V and Qwen-VL-Max. |
| [Voyager](https://github.com/MineDojo/Voyager) | ~7k ★ | First LLM-powered embodied lifelong learning agent in Minecraft — continuously explores, acquires skills, and makes discoveries without human intervention. | **NeurIPS 2023 paper.** NVIDIA (Jim Fan). 3.3× more unique items, 15.3× faster tech tree milestones vs prior SOTA. Code as action space. |
| [OSWorld](https://os-world.github.io/) | Research | First scalable real computer environment benchmark for multimodal agents  — 369 tasks across Ubuntu, Windows, macOS. | **NeurIPS 2024.** Best agents achieve ~30% vs much higher human baselines. The hardest computer-use benchmark. |

---

## 🔬 Research & Science Agents

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [BabyAGI](https://github.com/yoheinakajima/babyagi) | ~20k ★ | Pioneering AI task management system (140 lines of code) — creates, prioritizes, and executes tasks in a loop.  Now on BabyAGI 3 with scheduling. | **Defined task-driven agents** (March 2023). Created by VC Yohei Nakajima. One of the first viral autonomous agent concepts. |
| [Tongyi DeepResearch](https://github.com/Alibaba-NLP/DeepResearch) 🇨🇳 | Growing | Leading open-source deep research agent using on-policy RL with Group Relative Policy Optimization.  | **End-to-end RL approach** to deep research — not prompt-engineered. Alibaba NLP. Compatible with ReAct and IterResearch paradigms.  |
| [OpenAgents](https://github.com/xlang-ai/OpenAgents) | ~5k ★ | Three specialized agents: Data Agent, Plugins Agent (200+ tools), Web Agent — open-source ChatGPT Plus alternative.  | **COLM 2024 paper.**  XLANG Lab (HKU).  First attempt at replicating full ChatGPT Plus as open source. |

---

## 🧠 Memory & Knowledge Systems

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [Letta (MemGPT)](https://github.com/letta-ai/letta) | ~22k ★ | Platform for stateful agents with self-editing memory  inspired by OS virtual memory  — two-tier architecture: core memory + archival memory.  | **Foundational memory paper** ("MemGPT: Towards LLMs as Operating Systems").  UC Berkeley.  $10M seed (Felicis).  Transitioning to Letta V1 for GPT-5/Claude 4.5.  |
| [Mem0](https://github.com/mem0ai/mem0) | Growing | Memory layer for AI agents with personalization — short-term + long-term memory via conversation history and user preferences.  | **Plug-and-play memory** — flexible embedding and search configs. Works with any agent framework. |
| [Zep](https://github.com/getzep/zep) | Growing | Session-based memory with automatic summarization,  graph-based knowledge extraction, and fact extraction. | **Graph-based knowledge memory** — maintains conversation transcripts as memory blocks with automated summarization. |

---

## 🔧 Tool-Use & Function Calling

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [Gorilla](https://github.com/ShishirPatil/gorilla) | ~12k ★ | LLM fine-tuned for API/function calling.  Hosts the Berkeley Function Calling Leaderboard (BFCL V4 Agentic).  GoEx runtime for safe execution.  | **BFCL is the industry standard** for evaluating function-calling in LLMs. Apache 2.0.  UC Berkeley. |
| [ToolBench / ToolLLM](https://github.com/OpenBMB/ToolBench) 🇨🇳 | Growing | Training framework for LLMs to master 16,000+ real-world APIs  with DFSDT (Depth-First Search Decision Tree) reasoning. | **ICLR 2024.** Introduced backtracking in tool-use reasoning. Three-stage pipeline: API collection → instruction gen → solution annotation.  |
| [Composio](https://github.com/composio/composio) | Growing | Integration platform: 90+ tool connections for AI agents with managed authentication  and hierarchical task execution. | **Managed auth + 90 integrations** — solves the "connecting agents to real tools" problem out of the box. |
| [AgentLego](https://github.com/InternLM/agentlego) 🇨🇳 | ~500 ★ | Versatile tool API library extending agents with multimodal capabilities — vision, image gen/edit, speech, VL reasoning.  | **Multimodal tool library** from Shanghai AI Lab. Integrates with LangChain, Transformers Agents, and Lagent.  |

---

## 🧩 Planning & Reasoning Frameworks

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [DeerFlow 2.0](https://github.com/bytedance/deer-flow) 🇨🇳 | ~45k ★ | ByteDance's "SuperAgent harness" for research, coding, and creative tasks. v2.0 is a complete rewrite with sandboxed execution, persistent memory, sub-agent orchestration. | **Hit #1 GitHub Trending** and reached 45k stars in weeks.  Built on LangGraph. MIT license. Supports Doubao, DeepSeek, Kimi, GPT-4o, Claude. |
| [XAgent](https://github.com/OpenBMB/XAgent) 🇨🇳 | ~8k ★ | Autonomous agent with three-component architecture: Dispatcher (routing), Planner (milestones), Actor (execution). Proactive human collaboration via AskForHumanHelp tool.  | **Dispatcher-Planner-Actor paradigm.** OpenBMB/Tsinghua. Docker-sandboxed. ToolServer with file editor, Python notebooks, shell, web browser.  |
| [TaskWeaver](https://github.com/microsoft/TaskWeaver) | ~6k ★ | Microsoft's code-first agent for data analytics — converts natural language to executable Python with two-layer planning (Planner → Code Generator → Executor).  | **Data analytics specialist** — unique focus on rich data structures (pandas DataFrames). Stateful conversations.  ⚠️ Archived. |
| [SuperAGI](https://github.com/TransformerOptimus/SuperAGI) | ~17k ★ | Full-featured agent platform with toolkit marketplace, GUI dashboard, Docker deployment, and multi-agent workflows. | **Early marketplace approach** for agent toolkits and templates. Dev has slowed significantly since mid-2024. |
| [AgentGPT](https://github.com/reworkd/AgentGPT) | ~36k ★ | First browser-based autonomous agent UI — name a custom AI and set it on any goal. YC-backed. | **Pioneered browser-based agent UX.** ⚠️ Archived — Reworkd team pivoted to data extraction. |

---

## 🇨🇳 Chinese Contributions

China has produced some of the most impactful agent research and production frameworks. This section highlights projects not already featured above.

### Alibaba Ecosystem

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [AgentScope](https://github.com/agentscope-ai/agentscope) | ~20k ★ | Production-ready multi-agent framework with ReAct agents, MCP/A2A support,  real-time voice, memory management, and evaluation.  | **Broadest Chinese agent ecosystem** — AgentScope-Java (2.2k ★), ReMe memory kit, CoPaw assistant, Trinity-RFT for agentic RL. Biweekly community meetings. |
| [CoPaw](https://github.com/agentscope-ai/CoPaw) | ~13k ★ | Personal AI assistant workstation — multi-channel (DingTalk, Feishu, QQ, Discord, iMessage), local LLM support via llama.cpp/MLX, cron scheduling.  | **Chinese-platform native** — first-class support for DingTalk, Feishu, QQ, WeCom. Built on AgentScope. |
| [Qwen-Agent](https://github.com/QwenLM/Qwen-Agent) | ~13k ★ | Official agent framework for the Qwen model family — function calling, MCP, Code Interpreter, RAG (1M+ token context), Chrome extension.  | **Qwen ecosystem's agent layer.** Supports Qwen3, Qwen3-Coder, QwQ.  Includes DeepPlanning evaluation benchmark. |
| [ModelScope-Agent](https://github.com/modelscope/modelscope-agent) | ~4k ★ | Lightweight framework with MCP support, deep research (55.43 on DeepResearch Bench), code generation, and AgentFabric for custom agent creation. | **Alibaba's model-hub-native agent** with Anthropic Agent Skills protocol support. |
| [Qwen Code](https://github.com/QwenLM/qwen-code) | Growing | Terminal AI agent for coding (CLI), forked from Gemini CLI and optimized for Qwen models. | **Qwen's answer to Claude Code** — terminal-first coding agent with Qwen optimization. |

### ByteDance Ecosystem

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [Trae Agent](https://github.com/bytedance/trae-agent) | ~2k ★ | LLM-based agent for general software engineering — features "Lakeview" for concise step summarization, trajectory recording, YAML config. | **Research-friendly design** with trajectory recording for academic analysis. Multi-LLM support including Doubao. |

### Shanghai AI Lab / InternLM

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [Lagent](https://github.com/InternLM/lagent) | ~2k ★ | Lightweight, PyTorch-inspired agent framework with imperative Pythonic style, async/sync dual interface, ReAct/ReWOO agents. | **PyTorch-like API** for agent building. InternLM ecosystem integration. HTTP deployment for distributed multi-agent apps. |
| [HuixiangDou](https://github.com/InternLM/HuixiangDou) | Growing | Domain-specific QA agent — technical group chat assistant for answering questions in specialized domains. | **Domain QA specialist** from Shanghai AI Lab's InternLM team. |

### Tencent

| Project | Stars | Description | Key Differentiator |
|---------|-------|-------------|--------------------|
| [C3-Benchmark](https://github.com/Tencent-Hunyuan/C3-Benchmark) | Recent | Comprehensive agent evaluation covering all action spaces — bilingual (CN/EN) data generation, controllable task generation. | **Most analysis dimensions** among agent eval frameworks. Tencent Hunyuan. Multi-agent data generation. |

### Community & Education

| Project | Description |
|---------|-------------|
| [Hello-Agents](https://github.com/datawhalechina/hello-agents) | Chinese-language educational tutorial for building AI agents from scratch. Datawhale community. |
| [awesome-hermes-agent](https://github.com/0xNyk/awesome-hermes-agent) | Curated resource list for the Hermes Agent ecosystem. |

---

## 📊 Benchmarks & Evaluation

| Benchmark | GitHub / Link | Paper | Key Differentiator |
|-----------|--------------|-------|--------------------|
| [SWE-bench](https://github.com/SWE-bench/SWE-bench) | [arXiv:2310.06770](https://arxiv.org/abs/2310.06770) | **ICLR 2024 Oral.** 2,294 real GitHub issue-PR pairs. Gold standard for coding agents. Variants: Lite, Verified (500 human-validated), Multimodal. | The benchmark every coding agent cites. |
| [AgentBench](https://github.com/THUDM/AgentBench) 🇨🇳 | [arXiv:2308.03688](https://arxiv.org/abs/2308.03688) | **ICLR 2024.** First comprehensive multi-domain agent benchmark — 8 environments (OS, DB, KG, web, games). | Revealed massive gap between commercial and open-source LLMs on agent tasks. |
| [τ-bench](https://github.com/sierra-research/tau-bench) | [arXiv:2406.12045](https://arxiv.org/abs/2406.12045) | Emulates user-agent-tool conversations with domain-specific APIs and policy guidelines. pass^k reliability metric. | Even GPT-4o succeeds on <50% of tasks. Sierra AI (Shunyu Yao). Expanded to τ²-bench and τ³-bench. |
| [WebArena](https://github.com/web-arena-x/webarena) | [arXiv:2307.13854](https://arxiv.org/abs/2307.13854) | Realistic web environment with functional website replicas. 812 tasks. | Spawned VisualWebArena, WorkArena, TheAgentCompany. BrowserGym integration. |
| [GAIA](https://huggingface.co/spaces/gaia-benchmark/leaderboard) | Meta AI | 466 real-world questions requiring reasoning, multimodality, web browsing, tool use. Humans: 92%, GPT-4: 15%. | Conceptually simple for humans yet devastatingly hard for AI. |
| [ToolBench](https://github.com/OpenBMB/ToolBench) 🇨🇳 | [arXiv:2307.16789](https://arxiv.org/abs/2307.16789) | **ICLR 2024.** 16,000+ real-world APIs from RapidAPI with DFSDT reasoning. | Introduced backtracking reasoning for tool use. ToolLLaMA model. |
| [OSWorld](https://os-world.github.io/) | [arXiv:2404.07972](https://arxiv.org/abs/2404.07972) | **NeurIPS 2024.** Real computer environment (Ubuntu/Windows/macOS). 369 tasks. Best agents ~30%. | Most challenging computer-use benchmark. Requires actual VM execution. |
| [MLAgentBench](https://github.com/snap-stanford/MLAgentBench) | Stanford | Evaluates agents on ML research tasks: running experiments, analyzing results, writing code. | Tests the "AI researcher" use case end-to-end. |
| [Mind2Web](https://osu-nlp-group.github.io/Mind2Web/) | NeurIPS 2023 | 2,000+ crowd-sourced web tasks across 137 real websites. | Large-scale real-website benchmark. |
| [BFCL](https://gorilla.cs.berkeley.edu/leaderboard.html) | UC Berkeley / Gorilla | Berkeley Function Calling Leaderboard — V4 Agentic evaluates tool-calling in real-world agentic settings. | Industry standard for function-calling evaluation. |
| [ScienceAgentBench](https://osu-nlp-group.github.io/ScienceAgentBench/) | ICLR 2025 | 102 tasks for data-driven scientific discovery. | First rigorous benchmark for science agents. |

---

## 🔗 Protocols & Standards

| Protocol | Origin | Description |
|----------|--------|-------------|
| [MCP (Model Context Protocol)](https://modelcontextprotocol.io/) | Anthropic (Nov 2024) → Linux Foundation (Dec 2025) | Open standard for connecting AI models to tools and data sources. **97M+ monthly SDK downloads.** Supported by ChatGPT, Claude, Gemini, Cursor, VS Code. |
| [A2A (Agent-to-Agent Protocol)](https://google.github.io/A2A/) | Google → Linux Foundation | Protocol for agent discovery, capability advertisement, and collaboration across frameworks. **150+ supporting organizations.** |

---

## 📄 Foundational Papers

These papers introduced paradigms now embedded in virtually every agent framework.

| Paper | Year | Venue | Key Contribution |
|-------|------|-------|-----------------|
| [ReAct: Synergizing Reasoning and Acting](https://arxiv.org/abs/2210.03629) | 2023 | ICLR 2023 | **The agent paradigm.** Interleaved reasoning traces and actions — the foundation of modern LLM agents. Shunyu Yao et al. (Princeton). |
| [Chain-of-Thought Prompting](https://arxiv.org/abs/2201.11903) | 2022 | NeurIPS 2022 | **Step-by-step reasoning.** The foundational technique underlying all agent reasoning. Jason Wei et al. (Google). |
| [Reflexion: Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366) | 2023 | NeurIPS 2023 | **Self-correction without weight updates.** Agents learn from verbal self-reflection. 91% pass@1 on HumanEval. Noah Shinn et al. (Princeton). |
| [Tree of Thoughts](https://arxiv.org/abs/2305.10601) | 2023 | NeurIPS 2023 | **Search-based reasoning.** Extends CoT to explore multiple reasoning paths with BFS/DFS. Shunyu Yao et al. (Princeton). |
| [Toolformer](https://arxiv.org/abs/2302.04761) | 2023 | NeurIPS 2023 | **Self-supervised tool learning.** LLMs learn when/how to call tools. 6B model outperforms GPT-3 175B on math. Meta AI. |
| [HuggingGPT](https://arxiv.org/abs/2303.17580) | 2023 | NeurIPS 2023 | **LLM as model orchestrator.** ChatGPT plans and dispatches tasks to expert models from HuggingFace Hub. |
| [LATS: Language Agent Tree Search](https://arxiv.org/abs/2310.04406) | 2024 | ICML 2024 | **Unifies reasoning + acting + planning** via MCTS. 92.7% pass@1 on HumanEval with GPT-4. Andy Zhou et al. (UIUC). |
| [GEPA: Reflective Prompt Evolution](https://arxiv.org/abs/2507.19457) | 2026 | ICLR 2026 Oral | **Self-improving agents.** Outperforms GRPO by 6% with 35× fewer rollouts. Powers Hermes Agent's self-evolution. |
| [AutoGen](https://arxiv.org/abs/2308.08155) | 2024 | ICLR 2024 Workshop (Best Paper) | **Multi-agent conversation paradigm.** Defined how agents collaborate through structured dialogue. Microsoft. |
| [MetaGPT](https://arxiv.org/abs/2308.00352) | 2024 | ICLR 2024 Oral | **SOP-driven multi-agent collaboration.** "Code = SOP(Team)" — encodes human workflows as agent prompts. |
| [CAMEL](https://arxiv.org/abs/2303.17760) | 2023 | NeurIPS 2023 | **Role-playing agents.** First framework for multi-agent cooperation via inception prompting. |
| [Generative Agents](https://arxiv.org/abs/2304.03442) | 2023 | UIST 2023 | **Believable simulacra of human behavior.** Memory streams + reflection + planning = emergent social behaviors. Stanford. |
| [OpenHands](https://arxiv.org/abs/2407.16741) | 2024 | — | **AI software developer as generalist agent.** Defines the platform architecture for coding agents. |
| [SWE-agent (ACI)](https://arxiv.org/abs/2405.15793) | 2024 | NeurIPS 2024 | **Agent-Computer Interfaces.** How interface design changes agent performance. Princeton/Stanford. |
| [Voyager](https://arxiv.org/abs/2305.16291) | 2023 | NeurIPS 2023 | **Embodied lifelong learning.** Auto-curriculum + skill library + self-verification in Minecraft. NVIDIA. |
| [MemGPT](https://arxiv.org/abs/2310.08560) | 2023 | — | **LLMs as operating systems.** Self-editing memory with virtual context management. UC Berkeley. |
| [A Survey on LLM-based Autonomous Agents](https://arxiv.org/abs/2308.11432) | 2023 | Updated Mar 2025 | **Most-cited agent survey.** Unified framework: Profile + Memory + Planning + Action modules. |

---

## 📚 Surveys & Curated Lists

| Resource | Description |
|----------|-------------|
| [awesome-ai-agents](https://github.com/jim-schwoebel/awesome_ai_agents) | 1,500+ resources on AI agents — the largest general-purpose collection. |
| [awesome-ai-agents](https://github.com/slavakurilyak/awesome-ai-agents) | 300+ agentic resources with star counts and categorization. |
| [AI Agent Benchmark Compendium](https://github.com/philschmid/ai-agent-benchmark-compendium) | 50+ benchmarks categorized and compared. |
| [shelldex.com](https://shelldex.com/) | Community directory tracking 52+ OpenClaw derivatives across 9 languages. Weekly growth rankings. |
| [Agentic AI Survey](https://arxiv.org/abs/2510.25445) | Dual-paradigm framework (Symbolic vs Neural); PRISMA-based review of 90 studies. |
| [LLM Agent Methodology Survey](https://arxiv.org/abs/2503.21460) | March 2025 methodology-centered taxonomy of agent architectures. |

---

## Contributing

Contributions welcome! Please read the guidelines below before submitting a PR.

### What belongs here

- **Open-source frameworks** with a real GitHub repo, >500 stars or a published paper
- **Academic papers** that introduced a technique now widely used in agent systems
- **Benchmarks** that are actively used by the research community
- **Production deployments** that are open source and demonstrate novel architecture

### What doesn't belong

- Thin API wrappers with no novel architecture
- Closed-source products without open-source components (exceptions: category-defining products like Devin and Cursor)
- Projects with no activity for 12+ months and <1,000 stars
- Tutorials, courses, or blog posts (except as supplementary links)

### How to contribute

1. Fork this repository
2. Add your entry in the appropriate category with: `[Project Name](URL) | stars | One-line description | Key differentiator`
3. Verify the GitHub URL is live and the project is active
4. Submit a PR with a brief explanation of why this project is notable

---

<div align="center">

**⭐ Star this repo if you found it useful!**

*Last updated: March 2026 · Maintained with care · CC0 1.0 Universal*

</div>
