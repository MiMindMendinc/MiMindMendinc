# Lyle Perrien

**Self-Taught AI Systems Engineer** — LLM Inference · AI Safety · Offline/Edge AI
*Founder, Michigan MindMend Inc. (501(c)(3)) · Michigan · Open to remote AI engineering roles*

> I build practical AI systems that run locally, protect user data, and can be tested: high-performance RoPE/attention kernels, safety gateways, and offline-capable AI tools.

## Start here

| Project | Signal | Why it matters |
| --- | --- | --- |
| [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js) | JavaScript inference kernel | Zero-dependency, in-place RoPE with bit-exact Llama parity and reproducible benchmarks |
| [DominusUltra](https://github.com/MiMindMendinc/DominusUltra) | Triton/GPU kernel work | Fused RoPE + causal attention, correctness gated against PyTorch reference, measured on Blackwell |
| [TrustLayer](https://github.com/MiMindMendinc/TrustLayer) | AI safety infrastructure | PII redaction, prompt-injection checks, OpenAI-compatible safety gateway, deterministic audit logging |
| [mindmend-guardian](https://github.com/MiMindMendinc/mindmend-guardian) | Local-first youth safety | Privacy-first safety prototype with human escalation boundaries |
| [annie-local](https://github.com/MiMindMendinc/annie-local) | Offline AI product | FastAPI + Ollama local companion with private JSONL memory and reactive UI |

## Hiring signal

I am strongest where **systems engineering meets applied AI**:

- optimizing inference paths and positional-encoding kernels
- building local-first AI apps around Ollama, llama.cpp, FastAPI, and edge hardware
- designing deterministic safety layers, audit logs, and privacy controls
- turning rough prototypes into testable, documented portfolio artifacts

## Verified work

- **Triton fused RoPE + causal attention** — up to **7× over the PyTorch reference** at seq_len 2048 (~1.8 TB/s effective bandwidth, RTX PRO 6000 Blackwell); correctness via `allclose`, reproducible harness in-repo → [DominusUltra](https://github.com/MiMindMendinc/DominusUltra)
- **Pure-JS RoPE kernel** — zero deps, bit-exact Llama parity, in-place zero-allocation hot path; ~140M pairs/sec on desktop hardware (~30–40M on a shared cloud vCPU — harness included, run it yourself) → [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js)
- **Optimization PR submitted to xai-org/grok-1** — fused RoPE path ([PR #434](https://github.com/xai-org/grok-1/pull/434))
- **LLM safety gateway** — PII redaction, prompt-injection detection, deterministic audit logging for OpenAI-compatible endpoints → [TrustLayer](https://github.com/MiMindMendinc/TrustLayer)
- **Offline youth-safety AI** — local-first risk detection, deterministic crisis routing, edge deployment → [mindmend-guardian](https://github.com/MiMindMendinc/mindmend-guardian) · [OpenClaw Empathy Anchor](https://github.com/MiMindMendinc/OpenClaw-Empathy-Anchor-MindMend-OpenClaw-)
- **Local voice AI companion** — FastAPI + Ollama, fully offline, private JSONL memory → [annie-local](https://github.com/MiMindMendinc/annie-local)

## Core stack

Triton · CUDA concepts · JavaScript/TypeScript · Python · Rust · FastAPI · Node.js · Ollama · llama.cpp · Raspberry Pi / edge hardware · GitHub Actions · privacy and safety engineering

## Open to

Remote roles in **LLM inference optimization**, **AI safety engineering**, **kernel/performance engineering**, and **local/edge AI systems**.

📧 michiganmindmendinc@proton.me · 🔗 [@p_perrien](https://x.com/p_perrien)
