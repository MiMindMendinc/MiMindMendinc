# Lyle Perrien II

**Founder, Michigan MindMend Inc. — building privacy-first, offline AI safety tools, and documenting exactly what they can and can't do.**

Michigan MindMend Inc. is a 501(c)(3) nonprofit in rural Michigan building privacy-first, offline AI for youth and family mental health. I come from compliance operations and security supervision, and I hold Firefighter I & II, so I work the same way in software: follow the procedure, check the result, write down the limits. My main repos run CI on every change, ship one-command verify steps, and label anything experimental.

**Open to remote W-2 roles in compliance, operations, and junior analyst / IT.**

**Why it's relevant:** [TrustLayer](https://github.com/MiMindMendinc/TrustLayer) and [MindMend Guardian](https://github.com/MiMindMendinc/mindmend-guardian) are compliance-style controls in code — audit logs that record SHA-256 hashes instead of raw text, PII redaction and data minimization, and written risk limits (threat models and explicit "what this does not claim" sections).

[LinkedIn](https://www.linkedin.com/in/lyle-perrien-b7918062) · [GitHub](https://github.com/MiMindMendinc) · [X @p_perrien](https://x.com/p_perrien)

## Focus areas

- **Local / offline AI** — assistants and tools that keep private data on the device by default.
- **AI safety and fail-closed guardrails** — deterministic rules, human-in-the-loop escalation, and audit trails that store hashes instead of raw text.
- **Compliance and operations** — written procedures, evidence beside every claim, and honest scope statements.
- **Edge AI** — small, inspectable runtimes and kernels for constrained hardware.

## Featured work

| Project | What it is |
| --- | --- |
| [TrustLayer](https://github.com/MiMindMendinc/TrustLayer) | Lightweight LLM safety and privacy gateway for OpenAI-compatible apps: PII redaction, prompt-injection and restricted-topic blocking, and JSONL audit logs with SHA-256 input hashes. Prototype. |
| [MindMend Guardian](https://github.com/MiMindMendinc/mindmend-guardian) | Privacy-first, local-first AI safety prototype for youth and family wellness, with risk-signal detection and explicit human review; demos run on synthetic samples only. Not a clinical product. |
| [MindMend Empathy Anchor](https://github.com/MiMindMendinc/OpenClaw-Empathy-Anchor-MindMend-OpenClaw-) | Local-first safety-signal demonstrator: deterministic rules flag predefined signals for human review, with local SQLite alerts and raw-text retention off by default. Technical demo; not clinical software or an emergency service. |
| [Annie Local](https://github.com/MiMindMendinc/annie-local) | Local-first AI assistant with FastAPI, Ollama integration, inspectable memory, and guarded streaming. Offline-first beta, not a clinical product. |
| [lyle-rope-kernel-js](https://github.com/MiMindMendinc/lyle-rope-kernel-js) | Zero-dependency JavaScript RoPE kernel with scalar-reference parity checks and a live browser playground. Experimental release candidate; not published to npm. |
| [DominusUltra](https://github.com/MiMindMendinc/DominusUltra) | Research Triton fused-RoPE causal attention (GQA/MQA) with correctness-gated GPU evidence against PyTorch SDPA. Research code, not a production attention library. |

### Evidence highlights

- **Annie Local** — [CI baseline, 12 September 2026](https://github.com/MiMindMendinc/annie-local/actions/runs/34663657989): 329 Python tests passed on each of Python 3.11/3.12, plus 31 JavaScript tests. Open items are tracked in [release readiness](https://github.com/MiMindMendinc/annie-local/blob/main/docs/RELEASE_READINESS.md).
- **lyle-rope-kernel-js** — [CI on `main`, 8 October 2026](https://github.com/MiMindMendinc/lyle-rope-kernel-js/actions/runs/37732478233): green across Ubuntu/Windows × Node 22/24. Benchmarks are one-machine indicative numbers; the package does not implement a KV cache.
- **DominusUltra** — [CPU CI baseline, 2 October 2026](https://github.com/MiMindMendinc/DominusUltra/actions/runs/36957069771) (CPU/contract only; skipped CUDA cases are not GPU passes) and [gated Tesla T4 evidence, 2 October 2026](https://github.com/MiMindMendinc/DominusUltra/blob/main/docs/evidence/T4_2026-10-02.md). Results are shape-specific, including both wins and losses versus SDPA.

## Upstream engineering

[xai-org/grok-1#434](https://github.com/xai-org/grok-1/pull/434) — fused Triton RoPE work for Grok-1. Earlier H100 timing claims were withdrawn after a kernel correction; current public claims are limited to reproducible evidence. Upstream project authorship remains with its maintainers.

## How I work

- **Correctness before speed** — optimization claims follow numerical checks.
- **Evidence beside the result** — record the tested commit, environment, commands, and limitations.
- **Local-first where practical** — keep private workloads local by default and make remote routes explicit.
- **Fail closed** — when a safety check is unsure, stop and hand off to a human.
- **AI assists; humans decide** — keep safety boundaries and operator control visible.

## Stack

`Python` · `FastAPI` · `Flask` · `pytest` · `GitHub Actions` · `JavaScript` · `Node.js` · `Express` · `Docker` · `Ollama` · `Triton (GPU)` · `PyTorch`

## Contact

[LinkedIn](https://www.linkedin.com/in/lyle-perrien-b7918062) · [GitHub](https://github.com/MiMindMendinc) · [X @p_perrien](https://x.com/p_perrien)

Nothing here is claimed as a clinical product. If someone may be in immediate danger, contact emergency services; in the United States, call or text **988**.
