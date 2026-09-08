# Lyle Perrien II

**ML systems engineer** focused on GPU kernels, local inference, AI safety, and proof-driven engineering.

I build systems that are meant to be inspected, reproduced, and challenged. My public work emphasizes correctness gates, explicit limitations, local-first design, and benchmark claims backed by committed evidence.

[LinkedIn](https://www.linkedin.com/in/lyle-perrien-b7918062) · [GitHub](https://github.com/MiMindMendinc)

## Featured work

### [DominusUltra](https://github.com/MiMindMendinc/DominusUltra)
Triton fused-RoPE causal-attention research kernel covering prefill, decode, GQA/MQA, correctness-gated CUDA evidence, and reproducible benchmark tooling.

### [Annie Local](https://github.com/MiMindMendinc/annie-local)
Local-first AI assistant with inspectable memory, FastAPI, Ollama integration, explicit model-routing state, deterministic safety canaries, and hardened local deployment defaults.

### [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js)
Zero-dependency JavaScript RoPE implementation with deterministic reference parity, cached hot paths, Node 20/22 CI, and reproducible performance markers.

## Upstream engineering

[xai-org/grok-1#434](https://github.com/xai-org/grok-1/pull/434) — fused Triton RoPE work for Grok-1. Earlier H100 timing claims were withdrawn after a kernel correction; current public claims are intentionally limited to evidence that can be reproduced.

## Engineering principles

- **Correctness before speed** — optimization claims come after numerical gates.
- **Evidence over hype** — benchmark context, source hashes, and limitations belong beside the result.
- **Local-first where practical** — private workloads should not require cloud exposure by default.
- **AI assists; humans decide** — safety boundaries and operator control should remain visible.

## Stack

`Python` · `Triton` · `CUDA` · `PyTorch` · `FastAPI` · `Docker` · `GitHub Actions` · `JavaScript` · `Node.js` · `Ollama`

## Current focus

GPU kernel engineering · inference optimization · agent infrastructure · AI safety tooling · local / edge AI

**Open to remote engineering opportunities.**
