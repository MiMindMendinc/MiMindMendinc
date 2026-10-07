# Lyle Perrien II

**Software engineer** focused on testing, debugging, local AI systems, and reproducible delivery.

I build systems that can be inspected and tested: FastAPI applications, local model integrations, JavaScript numerical kernels, and GPU research tooling. Public work pairs implementation with verification commands, CI evidence, and explicit limits.

[LinkedIn](https://www.linkedin.com/in/lyle-perrien-b7918062) · [GitHub](https://github.com/MiMindMendinc)

## At a glance

| | |
| --- | --- |
| **Who** | Lyle Perrien II — software engineer; open to remote roles in testing, debugging, local AI, and reliable delivery |
| **What** | Inspectable local AI apps, experimental JS numerical kernels, and research CUDA/Triton attention tooling |
| **Usable today** | Clone-and-run checkouts with documented install/verify commands (see Featured work). Nothing here is claimed as a clinical product or a production attention library |
| **Install** | Follow each repo README (`npm ci` / `pip install -e ".[dev]"`). Prefer Node **≥22** for the JS RoPE package; Python 3.10+ for DominusUltra CPU CI |
| **Evidence** | CI run URLs and committed gated reports beside the claims — not screenshots alone |
| **Experimental** | Release candidates, research kernels, and prototypes are labeled as such; RC ≠ npm publication |
| **Contribute** | Issues and PRs welcome on the public repos; include OS, runtime version, and pass/fail when reporting results |

## Featured work

Ordered for public inspectability: clone-friendly experimental package first, then gated GPU research, then the local-first assistant.

### [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js)

Zero-runtime-dependency JavaScript RoPE implementation with deterministic scalar-reference parity, cached plans, input validation, and numerical-invariant checks.

- Package `1.1.0-rc.1`; `engines.node` **`>=22`**. CI matrix: Ubuntu/Windows × Node **22 and 24**.
- [Verified CI baseline — 5 October 2026](https://github.com/MiMindMendinc/lyle-rope-kernel-js/actions/runs/37269375603): green PR CI on head `7bd49e9` across the Node 22/24 matrix. Tip of `main` merge `f9b7051` used `[skip ci]` after that green PR (no fresh push CI on the merge tip). No npm publication claimed.
- Benchmarks are environment-specific markers via the evidence harness; WebGPU remains a CPU fallback, not GPU acceleration. `startPos` supplies an absolute position — this package does **not** implement a KV cache.

### [DominusUltra](https://github.com/MiMindMendinc/DominusUltra)

Triton fused-RoPE causal-attention research code and correctness-gated benchmark tooling for prefill, decode, and GQA/MQA.

- [Verified CPU CI baseline — 2 October 2026](https://github.com/MiMindMendinc/DominusUltra/actions/runs/36957069771): tip of `main` `aaf5fb69`; **13 passed**, **142 CUDA skipped**, **3 subtests passed** on each of Python 3.10/3.11 (CPU/contract only).
- [Latest gated GPU evidence — 2 October 2026](https://github.com/MiMindMendinc/DominusUltra/blob/main/docs/evidence/T4_2026-10-02.md): Tesla T4, pinned commit `a0d11750a9d5dfe858b2fa33348f8085e9bd5f2a`, clean `quick` suite **PASS** (`dirty=false`); **2.503×** on `decode:B2:Hq8:Hkv8:T128:D64` and **0.451× loss** on `prefill:B1:Hq8:Hkv2:T257:D64`, versus PyTorch SDPA with RoPE outside the timer.
- Research-only, shape-specific results; not a FlashAttention comparison, end-to-end generation result, or production-readiness claim. Short-cache decode wins are often launch-bound and do not establish long-context or broader hardware performance. No independent security or production-readiness audit. CPU CI remains CPU/contract-only; skipped CUDA cases are not GPU passes. Upstream [xai-org/grok-1#434](https://github.com/xai-org/grok-1/pull/434) is separate from this repository's gated evidence.

### [Annie Local](https://github.com/MiMindMendinc/annie-local)

Local-first AI assistant with FastAPI, Ollama integration, inspectable memory, model-repair flows, and guarded streaming.

- [Verified CI baseline — 12 September 2026](https://github.com/MiMindMendinc/annie-local/actions/runs/34663657989): 329 Python tests passed on each of Python 3.11/3.12, plus 31 JavaScript tests. Repeated matrix runs are not counted as additional unique tests.
- Tip of `main` (including dependency audit fixes) remains CI-green as of 7 October 2026; see recent Actions on the repo. Local-first beta. Physical-device, accessibility, and successful real-model browser acceptance remain open; see [release readiness](https://github.com/MiMindMendinc/annie-local/blob/main/docs/RELEASE_READINESS.md).

## Other public prototypes

Inspectable, explicitly non-clinical prototypes (pin recommendations live in portfolio handoff notes):

- [TrustLayer](https://github.com/MiMindMendinc/TrustLayer) — OpenAI-compatible LLM safety gateway prototype (PII redaction, jailbreak rules, audit logs).
- [mindmend-guardian](https://github.com/MiMindMendinc/mindmend-guardian) — youth-safety prototype with explicit human escalation; screenshots still pending.
- [OpenClaw Empathy Anchor](https://github.com/MiMindMendinc/OpenClaw-Empathy-Anchor-MindMend-OpenClaw-) — privacy-first local journal coach prototype; research/nonprofit demo.

## Upstream engineering

[xai-org/grok-1#434](https://github.com/xai-org/grok-1/pull/434) — fused Triton RoPE work for Grok-1. Earlier H100 timing claims were withdrawn after a kernel correction; current public claims are limited to reproducible evidence. Upstream project authorship remains with its maintainers. Submission status is not DominusUltra benchmark evidence.

## Engineering principles

- **Correctness before speed** — optimization claims follow numerical checks.
- **Evidence beside the result** — record the tested commit, environment, commands, and limitations.
- **Local-first where practical** — keep private workloads local by default and make remote routes explicit.
- **AI assists; humans decide** — keep safety boundaries and operator control visible.

## Stack

`Python` · `FastAPI` · `pytest` · `GitHub Actions` · `JavaScript` · `Node.js` · `Docker` · `Ollama` · `Triton` · `CUDA` · `PyTorch`

**Open to remote software engineering opportunities**, especially testing, debugging, local AI applications, and reliable delivery.
