# Lyle Perrien II

**AI Systems Engineer · LLM Inference · AI Safety · Local/Edge AI**

I build practical AI systems that run locally, protect user data, and come with visible tests, benchmarks, or demos. My work spans Triton attention kernels, JavaScript inference primitives, OpenAI-compatible safety middleware, and offline AI applications.

**Open to remote engineering roles and contract work.**

## Selected work

| Project | Engineering signal | Evidence |
| --- | --- | --- |
| [DominusUltra](https://github.com/MiMindMendinc/DominusUltra) | Triton causal attention with fused RoPE, GQA/MQA, and KV-cache decode paths | PyTorch correctness reference, CUDA tests, reproducible benchmark harness, recorded-demo workflow |
| [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js) | Zero-dependency, in-place RoPE kernel for JavaScript inference | Llama-reference parity tests, KV-cache continuation coverage, benchmark, browser demo |
| [TrustLayer](https://github.com/MiMindMendinc/TrustLayer) | OpenAI-compatible LLM safety and privacy gateway | PII redaction, prompt-injection rules, deterministic audit logs, Node tests and CI |
| [annie-local](https://github.com/MiMindMendinc/annie-local) | Fully local voice companion built with FastAPI and Ollama | Installable Python package, private JSONL memory, tests, CI, privacy and threat-model docs |
| [localcowork-ai](https://github.com/MiMindMendinc/localcowork-ai) | Local multi-agent CLI and Ollama orchestration | Typed Python package, tests, CI, CLI and Python API examples |
| [mindmend-guardian](https://github.com/MiMindMendinc/mindmend-guardian) | Privacy-first youth-safety prototype with human escalation boundaries | Python package structure, tests, CI, explicit safety limits |

## Systems and open-source work

- Submitted a fused-RoPE optimization to the upstream [xai-org/grok-1 project (PR #434)](https://github.com/xai-org/grok-1/pull/434).
- Built reproducible kernel benchmarks with correctness checks before timing.
- Built local-first AI applications around Ollama, FastAPI, Node.js, browser APIs, and edge-device constraints.
- Designed safety middleware with inspectable policies, data minimization, and honest prototype boundaries.
- Maintain a [Grok-1 research fork](https://github.com/MiMindMendinc/grok-1) for inference and RoPE experiments; it is clearly presented as a fork, not original ownership of Grok-1.

## Core stack

`Python` · `JavaScript/TypeScript` · `Triton` · `PyTorch` · `JAX` · `FastAPI` · `Node.js` · `Rust` · `Docker` · `GitHub Actions` · `Ollama` · `local/edge AI`

## What I care about

- Correctness before benchmark claims
- Privacy by default
- Local and offline operation where practical
- Human control in safety-sensitive systems
- Clear documentation that separates working code from roadmap ideas

## Contact

**Lyle Perrien II**  
Founder, Michigan MindMend Inc. · Owosso, Michigan  
[michiganmindmendinc@proton.me](mailto:michiganmindmendinc@proton.me) · [@p_perrien](https://x.com/p_perrien)

Remote roles: **LLM inference**, **AI safety**, **applied AI systems**, and **local/edge AI**.
