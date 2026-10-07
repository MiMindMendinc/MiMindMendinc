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

- Package `1.1.0-rc.1`; `engines.node` **`>=22`**. CI matrix: Ubuntu/Windows × Node **22 and 24**.
- [Verified CI baseline — 5 October 2026](https://github.com/MiMindMendinc/lyle-rope-kernel-js/actions/runs/37269375603): green PR CI on head `7bd49e9` across the Node 22/24 matrix. Tip of `main` merge `f9b7051` used `[skip ci]` after that green PR (no fresh push CI on the merge tip). No npm publication claimed.
- Benchmarks are environment-specific markers via the evidence harness; WebGPU remains a CPU fallback, not GPU acceleration.

### [DominusUltra](https://github.com/MiMindMendinc/DominusUltra)

Triton fused-RoPE causal-attention research code and correctness-gated benchmark tooling for prefill, decode, and GQA/MQA.

- [Verified CPU CI baseline — 6 September 2026](https://github.com/MiMindMendinc/DominusUltra/actions/runs/34014539891): 13 tests passed and 142 CUDA cases were skipped on each of Python 3.10/3.11; the runner also reports 3 subtests passed.
- [Latest gated GPU evidence — 2 October 2026](https://github.com/MiMindMendinc/DominusUltra/blob/main/docs/evidence/T4_2026-10-02.md): Tesla T4, pinned commit `a0d11750a9d5dfe858b2fa33348f8085e9bd5f2a`, clean `quick` suite **PASS** (`dirty=false`); **2.503×** on `decode:B2:Hq8:Hkv8:T128:D64` and **0.451× loss** on `prefill:B1:Hq8:Hkv2:T257:D64`, versus PyTorch SDPA with RoPE outside the timer.
- Research-only, shape-specific results; not a FlashAttention comparison, end-to-end generation result, or production-readiness claim. Short-cache decode wins are often launch-bound and do not establish long-context or broader hardware performance. No independent security or production-readiness audit. CPU CI remains CPU/contract-only; skipped CUDA cases are not GPU passes.

## Usable today

| Project | What a visitor can run now | Honest limits |
| --- | --- | --- |
| [Annie Local](https://github.com/MiMindMendinc/annie-local) | Local install + Ollama → `annie launch` (loopback UI) | Local-first beta; physical-device / real-model browser gates still open; not a clinical product |
| [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js) | Node **≥22**: `npm ci` (offline flags in README) → `npm run verify` | Release-candidate package; **not** published to npm; experimental CPU RoPE component |
| [DominusUltra](https://github.com/MiMindMendinc/DominusUltra) | CPU contract tests via CI / local `pytest`; GPU path documented under `docs/evidence/` | Research kernels only; green CPU CI is not a GPU pass |

Safety demos ([TrustLayer](https://github.com/MiMindMendinc/TrustLayer), [mindmend-guardian](https://github.com/MiMindMendinc/mindmend-guardian), [Empathy Anchor](https://github.com/MiMindMendinc/OpenClaw-Empathy-Anchor-MindMend-OpenClaw-)) are public prototypes with their own README quickstarts — not production clinical tools.

## Install

Full steps live in each repository README. Short pointers:

```bash
# Annie Local
git clone https://github.com/MiMindMendinc/annie-local.git && cd annie-local
python -m pip install -e . && ollama pull llama3.2 && annie launch
# → http://127.0.0.1:8787

# lyle-rope-kernel-js (Node ≥22)
git clone https://github.com/MiMindMendinc/lyle-rope-kernel-js.git && cd lyle-rope-kernel-js
npm ci --offline --ignore-scripts --no-audit --no-fund && npm run verify

# DominusUltra
git clone https://github.com/MiMindMendinc/DominusUltra.git && cd DominusUltra
python -m venv .venv && source .venv/bin/activate
pip install -e ".[dev]"
```

## Contribute

Issues and small, tested pull requests are welcome on the public featured repos. Prefer changes that keep local-first defaults, synthetic examples, and explicit limits intact.

- Start from each repo’s `CONTRIBUTING.md` when present (`annie-local`, `DominusUltra`, `TrustLayer`, `mindmend-guardian`, Empathy Anchor).
- For `lyle-rope-kernel-js`, open an issue before large API or numerical-contract changes (no dedicated CONTRIBUTING file yet).

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
