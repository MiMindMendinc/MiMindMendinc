# Lyle Perrien II

**Developer with a compliance-operations background: I build tested, local-first tools and document what they can and can't do.**

I come from compliance operations and security supervision, and I hold Firefighter I & II, so I work the same way in software: follow the procedure, check the result, write down the limits. I founded Michigan MindMend Inc., a nonprofit building privacy-first, local AI tools, and my main repos run CI on every change, ship one-command verify steps, and label anything experimental. I'm open to remote IT support, junior analyst, and compliance-operations roles.

[LinkedIn](https://www.linkedin.com/in/lyle-perrien-b7918062) · [GitHub](https://github.com/MiMindMendinc)

## At a glance

| | |
| --- | --- |
| **Who** | Lyle Perrien II — developer with a compliance-operations background; open to remote IT support, junior analyst, and compliance-operations roles |
| **What** | Inspectable local AI apps, experimental JS numerical kernels, and research Triton (GPU) attention tooling |
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
- [Live browser playground](https://mimindmendinc.github.io/lyle-rope-kernel-js/playground.html): runs the same kernel file in the page, checks the result against the scalar reference, and times it on your device.
- [CI on `main` — 8 October 2026](https://github.com/MiMindMendinc/lyle-rope-kernel-js/actions/runs/37732478233): green on `main` commit `3f750cd` across Ubuntu/Windows × Node 22/24. Not yet published to npm.
- `npm run bench` reproduces the [benchmark table in the README](https://github.com/MiMindMendinc/lyle-rope-kernel-js#benchmarks-one-machine-indicative-only); each case is reference-checked before it is timed, and results are one-machine indicative numbers, not cross-hardware claims. WebGPU remains a CPU fallback, not GPU acceleration. `startPos` supplies an absolute position — this package does **not** implement a KV cache.

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

Inspectable, explicitly non-clinical prototypes:

- [TrustLayer](https://github.com/MiMindMendinc/TrustLayer) — OpenAI-compatible LLM safety gateway prototype (PII redaction, jailbreak rules, audit logs).
- [mindmend-guardian](https://github.com/MiMindMendinc/mindmend-guardian) — youth-safety prototype with explicit human escalation; local CLI and Streamlit demos run on synthetic sample messages only.
- [MindMend Empathy Anchor](https://github.com/MiMindMendinc/OpenClaw-Empathy-Anchor-MindMend-OpenClaw-) — local-first safety-signal demonstrator: deterministic rules flag predefined safety signals for human review; technical demonstration, not clinical software or an emergency service.

## Upstream engineering

[xai-org/grok-1#434](https://github.com/xai-org/grok-1/pull/434) — fused Triton RoPE work for Grok-1. Earlier H100 timing claims were withdrawn after a kernel correction; current public claims are limited to reproducible evidence. Upstream project authorship remains with its maintainers. Submission status is not DominusUltra benchmark evidence.

## Engineering principles

- **Correctness before speed** — optimization claims follow numerical checks.
- **Evidence beside the result** — record the tested commit, environment, commands, and limitations.
- **Local-first where practical** — keep private workloads local by default and make remote routes explicit.
- **AI assists; humans decide** — keep safety boundaries and operator control visible.

## Stack

`Python` · `FastAPI` · `pytest` · `GitHub Actions` · `JavaScript` · `Node.js` · `Docker` · `Ollama` · `Triton (GPU)` · `PyTorch`

**Open to remote IT support, junior analyst, and compliance-operations roles**, plus junior software roles in testing, debugging, and local AI applications.
