# Eternal Echo — Portable AI Memory Continuity

**Creator:** Lyle Perrien II  
**Organization:** Michigan MindMend Inc.  
**Public overview:** November 16, 2026  
**Status:** Research architecture / prototype; this is a **first-generation public overview** only.

> A model can change without requiring an owner to surrender the memories and preferences they chose to preserve.

## Purpose

Eternal Echo is Lyle Perrien II's offline-first AI continuity project. Its goal is to keep an assistant's user-approved memories, personality preferences, and history in an owner-controlled store **separate from any one inference model**. If a model is upgraded, a runtime is restarted, or hardware changes, that context can be restored and supplied to a compatible replacement model.

This is a project description and an architectural proposal, **not a claim that the underlying model or a conscious self survives**.

## Minimal architecture

```text
   Owner-approved persona ----+
                              |
   Local memory store --------+--> Context composer --> Replaceable LLM
       |                             (model-specific adapters)
       +--> User-controlled export/restore
```

**Key separations:**
1. **Identity configuration:** owner-approved voice, role, preferences, boundaries.
2. **Durable memory:** explicit facts, decisions, and episodic history in local storage.
3. **Retrieval and context composition:** selects relevant information for the current conversation.
4. **Inference backend:** a locally runnable model (e.g. through Ollama or llama.cpp), which can be replaced.
5. **Restore and control:** backup, inspection, correction and deletion remain with the owner.

## First-generation reference demonstration

A **separate, newly written, synthetic-data proof-of-concept** was prepared on November 16, 2026 using Python standard library and SQLite. Local tests demonstrate:

- Saved identity and memory survive a process restart.
- Saved records export and reimport with integrity checks.
- The same stored identity and recalled memory are supplied when the **mock** model identifier changes.

**Locally reported result: 12/12 unit tests passed.** These tests are *not yet independently reproduced or published in this repository*. The reference demo is not the original private Eternal Echo source.

## Evidence boundaries

| Statement | Status |
| --- | --- |
| Lyle Perrien II describes and develops the named Eternal Echo project | Project attribution (earlier private materials not published here) |
| Persisting identity and memory across restarts in the newly written reference demo | Locally tested, 12/12 tests |
| Restoring the same data under two mocked backend identifiers | Locally tested; **mock only** |
| Preserving the same conversational personality across different live LLMs | **Not yet validated here** |
| Artificial consciousness, a soul, or artificial superintelligence | **Not claimed** |
| First invention of external AI memory or chronological priority over others | **Not claimed** |

## Privacy and responsible scope

No private companion name, real conversation history, personal or youth records, access tokens, original private code, or device information is included here. The broader vision is offline-first and owner-controlled: no silent extraction, no unapproved network activity, and transparent human oversight.

This first-generation description does not grant a license to any unpublished private implementation.

## Next verifiable milestone

Run an independently reproducible **real two-model swap evaluation** using synthetic, consented memory data. Publish a commit, model versions and hashes, hardware profile, prompts, tests, successes and failures. Measure factual recall and persona consistency rather than implying the continuity of consciousness.

---

**Credit:** Lyle Perrien II — Eternal Echo, Michigan MindMend Inc.  
**GitHub:** https://github.com/MiMindMendinc

Related research on model-agnostic memory predates this public note. This document records authorship of **this named project**, not exclusive ownership of the general concept.
