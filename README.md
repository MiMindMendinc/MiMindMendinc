# Lyle Perrien II

**AI Systems Engineer · LLM Inference · Agent Systems · AI Safety · Local/Edge AI**

I build practical AI systems with a systems-engineering mindset: correctness first, reproducible tests, local/offline operation where it matters, and safety boundaries that humans can inspect. My work sits at the intersection of **LLM inference**, **agent orchestration**, **privacy-first AI**, **kernel optimization**, and **production safety tooling**.

I am especially interested in remote roles and contract work involving **LLM systems**, **agent infrastructure**, **inference optimization**, **AI safety**, **local/edge AI**, and **developer tooling**.

## What I build

- **LLM inference and kernel work** — Triton, PyTorch, RoPE, attention paths, KV-cache experiments, correctness-first benchmarking.
- **Agent systems** — local-first assistants, multi-agent coordination, checkpointing, memory, tool execution, and human-in-the-loop control.
- **AI safety infrastructure** — OpenAI-compatible safety gateways, PII redaction, prompt-injection defenses, audit logs, and explicit escalation boundaries.
- **Offline and edge AI** — Ollama/FastAPI/Node systems designed for privacy, unreliable connectivity, and real-world use outside cloud-only assumptions.
- **Nonprofit technology** — Michigan MindMend Inc. builds privacy-first AI tools for youth wellness, family safety, and community resilience.

## Selected work

| Project | What it demonstrates | Evidence / signal |
| --- | --- | --- |
| [DominusUltra](https://github.com/MiMindMendinc/DominusUltra) | Triton causal attention work with fused RoPE, GQA/MQA direction, and KV-cache decode experiments | PyTorch correctness references, CUDA-oriented tests, benchmark harnesses, demo workflow |
| [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js) | Zero-dependency JavaScript RoPE kernel for browser/local inference primitives | Llama-reference parity tests, KV-cache continuation coverage, benchmark/demo path |
| [TrustLayer](https://github.com/MiMindMendinc/TrustLayer) | OpenAI-compatible LLM safety and privacy gateway | PII redaction, prompt-injection rules, deterministic audit logs, Node tests and CI |
| [annie-local](https://github.com/MiMindMendinc/annie-local) | Local voice companion architecture using FastAPI/Ollama-style local AI patterns | Installable Python package direction, private JSONL memory, tests, CI, privacy/threat-model docs |
| [localcowork-ai](https://github.com/MiMindMendinc/localcowork-ai) | Local multi-agent CLI and Ollama orchestration | Typed Python package direction, tests, CI, CLI/Python API examples |
| [mindmend-guardian](https://github.com/MiMindMendinc/mindmend-guardian) | Privacy-first youth-safety prototype with explicit human escalation boundaries | Python package structure, tests, CI, non-clinical safety limits |

## Open-source and research signal

- Submitted a fused-RoPE optimization to the upstream [xai-org/grok-1 project, PR #434](https://github.com/xai-org/grok-1/pull/434).
- Maintain a [Grok-1 research fork](https://github.com/MiMindMendinc/grok-1) for inference and RoPE experiments; this is clearly presented as a research fork, not original ownership of Grok-1.
- Build benchmarks that separate **correctness checks** from **timing claims**.
- Prefer visible tests, reproducible setup, and honest prototype boundaries over inflated demos.
- Design AI tooling around the principle: **AI assists; humans decide.**

## Current flagship direction

I am consolidating my strongest work into a cleaner portfolio centered on:

1. **A production-grade local agent stack** — checkpointed agent execution, tool use, memory, human approval gates, web/visual interfaces, and safety middleware.
2. **Inference and kernel optimization** — RoPE/attention experiments with correctness-first benchmarks.
3. **Safety and privacy infrastructure** — inspectable policy layers, auditability, and child/family-safe boundaries.

## Core stack

`Python` · `JavaScript/TypeScript` · `Triton` · `PyTorch` · `JAX` · `FastAPI` · `Node.js` · `Rust` · `Docker` · `GitHub Actions` · `Ollama` · `SQLite` · `local/edge AI`

## Engineering values

- Correctness before speed claims
- Reproducible tests before portfolio polish
- Local/private by default when user data is sensitive
- Human control for safety-sensitive systems
- Clear documentation that separates working code from roadmap ideas
- Practical systems that can run outside perfect cloud conditions

## Contact

**Lyle Perrien II**  
Founder, Michigan MindMend Inc. · Michigan  
[michiganmindmendinc@proton.me](mailto:michiganmindmendinc@proton.me) · [@p_perrien](https://x.com/p_perrien)

Open to remote roles and contract work in **LLM inference**, **agent systems**, **AI safety**, **applied AI infrastructure**, and **local/edge AI**.
