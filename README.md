# Lyle Perrien

**Self-Taught AI Kernel & Safety Engineer** — Privacy-First, Offline-Capable AI
*Founder, Michigan MindMend Inc. (501(c)(3)) · Michigan*

> Building AI that runs offline, respects privacy, and holds up under audit — high-performance inference kernels and safety infrastructure for youth mental health.

### Verified work

- **Triton fused RoPE + causal attention** — up to **7× over the PyTorch reference** at seq_len 2048 (~1.8 TB/s effective bandwidth, RTX PRO 6000 Blackwell); correctness via `allclose`, reproducible harness in-repo → [DominusUltra](https://github.com/MiMindMendinc/DominusUltra)
- **Pure-JS RoPE kernel** — zero deps, bit-exact Llama parity, in-place zero-allocation hot path; ~140M pairs/sec on desktop hardware (~30–40M on a shared cloud vCPU — harness included, run it yourself) → [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js)
- **Optimization PR submitted to xai-org/grok-1** — fused RoPE path ([PR #434](https://github.com/xai-org/grok-1/pull/434))
- **LLM safety gateway** — PII redaction, prompt-injection detection, deterministic audit logging for OpenAI-compatible endpoints → [TrustLayer](https://github.com/MiMindMendinc/TrustLayer)
- **Offline youth-safety AI** — local-first risk detection, deterministic crisis routing, edge deployment → [mindmend-guardian](https://github.com/MiMindMendinc/mindmend-guardian) · [OpenClaw Empathy Anchor](https://github.com/MiMindMendinc/OpenClaw-Empathy-Anchor-MindMend-OpenClaw-)
- **Local voice AI companion** — FastAPI + Ollama, fully offline, private JSONL memory → [annie-local](https://github.com/MiMindMendinc/annie-local)

### Core expertise

GPU kernels (Triton · CUDA · WebGPU) · LLM inference optimization · Local/edge AI (Ollama, llama.cpp, Raspberry Pi, rugged hardware) · AI safety engineering (audit chains, deterministic guardrails, threat modeling) · Rust & Python systems

### Open to

Remote roles in **kernel engineering**, **inference optimization**, **AI safety engineering**, and **edge/local AI**.

📧 michiganmindmendinc@proton.me · 🔗 [@p_perrien](https://x.com/p_perrien)
