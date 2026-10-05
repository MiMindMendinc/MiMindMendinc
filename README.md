# Lyle Perrien II

**Software engineer** focused on testing, debugging, local AI systems, and reproducible delivery.

I build systems that can be inspected and tested: FastAPI applications, local model integrations, JavaScript numerical kernels, and GPU research tooling. My public work pairs implementation with verification commands, CI evidence, and explicit limits.

[LinkedIn](https://www.linkedin.com/in/lyle-perrien-b7918062) · [GitHub](https://github.com/MiMindMendinc)

## Featured work

### [Annie Local](https://github.com/MiMindMendinc/annie-local)

Local-first AI assistant with FastAPI, Ollama integration, inspectable memory, model-repair flows, and guarded streaming.

- [Verified CI baseline — 12 September 2026](https://github.com/MiMindMendinc/annie-local/actions/runs/34663657989): 329 Python tests passed on each of Python 3.11/3.12, plus 31 JavaScript tests. Repeated matrix runs are not counted as additional unique tests.
- Local-first beta. Physical-device, accessibility, and successful real-model browser acceptance remain open; see [release readiness](https://github.com/MiMindMendinc/annie-local/blob/main/docs/RELEASE_READINESS.md).

### [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js)

Zero-runtime-dependency JavaScript RoPE implementation with deterministic scalar-reference parity, cached plans, input validation, and numerical-invariant checks.

- [Verified CI baseline — 30 August 2026](https://github.com/MiMindMendinc/lyle-rope-kernel-js/actions/runs/33336990492): 17 tests passed on each of Node 20 and 22, with no skips.
- Benchmarks are environment-specific markers; WebGPU remains a preview fallback.

### [DominusUltra](https://github.com/MiMindMendinc/DominusUltra)

Triton fused-RoPE causal-attention research code and correctness-gated benchmark tooling for prefill, decode, and GQA/MQA.

- [Verified CPU CI baseline — 6 September 2026](https://github.com/MiMindMendinc/DominusUltra/actions/runs/34014539891): 13 tests passed and 142 CUDA cases were skipped on each of Python 3.10/3.11; the runner also reports 3 subtests passed.
- [Latest gated GPU evidence — 2 October 2026](https://github.com/MiMindMendinc/DominusUltra/blob/main/docs/evidence/T4_2026-10-02.md): Tesla T4, pinned commit `a0d11750a9d5dfe858b2fa33348f8085e9bd5f2a`, clean `quick` suite **PASS** (`dirty=false`); **2.503×** on `decode:B2:Hq8:Hkv8:T128:D64` and **0.451× loss** on `prefill:B1:Hq8:Hkv2:T257:D64`, versus PyTorch SDPA with RoPE outside the timer.
- Research-only, shape-specific results; not a FlashAttention comparison, end-to-end generation result, or production-readiness claim. Short-cache decode wins are often launch-bound and do not establish long-context or broader hardware performance. No independent security or production-readiness audit. CPU CI remains CPU/contract-only; skipped CUDA cases are not GPU passes.

## Upstream engineering

[xai-org/grok-1#434](https://github.com/xai-org/grok-1/pull/434) — fused Triton RoPE work for Grok-1. Earlier H100 timing claims were withdrawn after a kernel correction; current public claims are limited to reproducible evidence. Upstream project authorship remains with its maintainers.

## Engineering principles

- **Correctness before speed** — optimization claims follow numerical checks.
- **Evidence beside the result** — record the tested commit, environment, commands, and limitations.
- **Local-first where practical** — keep private workloads local by default and make remote routes explicit.
- **AI assists; humans decide** — keep safety boundaries and operator control visible.

## Stack

`Python` · `FastAPI` · `pytest` · `GitHub Actions` · `JavaScript` · `Node.js` · `Docker` · `Ollama` · `Triton` · `CUDA` · `PyTorch`

**Open to remote software engineering opportunities**, especially testing, debugging, local AI applications, and reliable delivery.
