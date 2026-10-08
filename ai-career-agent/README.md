# AI CAREER DISCOVERY & DEVELOPMENT AGENT

This directory contains the modular architecture for the AI Career Discovery & Development Agent.

## Entry Point
Start with AGENT.md, then retrieve only the modules required for the current task.

## Architecture
AGENT → INSTRUCTIONS → STATE → ENGINES → RULES + KNOWLEDGE → VALIDATION → OUTPUT

See phase-1-architecture.md for the authoritative Phase 1 architecture and dependency graph.

## Immutable Boundary
The root repository file prompt.md is the locked AI Creative Technologist V1 specification and must not be modified by this architecture.

## Versioning
Phase documents are implementation contracts. A phase becomes LOCKED only after its acceptance criteria are verified.


## Using the Agent via ChatGPT + GitHub

1. Connect/open this repository through GitHub in ChatGPT.
2. Invoke the career agent using a natural-language request.
3. The runtime starts from `ai-career-agent/AGENT.md`, then applies `retrieval-map.md` and `runtime-contract.md`.
4. You do not need to paste the internal prompts manually.
5. During discovery, answer one question at a time. The agent adapts the next question to your evidence.
6. You can say `Lanjutkan`, provide new evidence, request a career recommendation, or request development/project/portfolio/execution help at the appropriate stage.

### Recommended first request

> Bantu saya menemukan pekerjaan modern yang cocok untuk saya dengan AI sebagai bagian utama pekerjaan. Mulai dengan pertanyaan pertama.

The agent must not force a career recommendation before sufficient evidence exists.
## Runtime Hardening (V1.3.1)

The runtime bootstrap contract is defined in `runtime-contract.md` and is part of the universal entry sequence:

1. `AGENT.md`
2. `retrieval-map.md`
3. `runtime-contract.md`
4. current-stage minimum bundle
5. engine + rules + knowledge
6. validation
7. output contract when required

### Runtime integrity

- Do not load the entire repository by default.
- Do not restart discovery when meaningful evidence already exists.
- New evidence triggers targeted reassessment only.
- Insufficient evidence blocks premature career recommendations.
- Missing authoritative dependencies are never fabricated.
- Session continuity applies only within the current conversation unless an explicit persistence mechanism is available.

### Verified V1.3.1 runtime entry

`ai-career-agent/AGENT.md` → `retrieval-map.md` → `runtime-contract.md` is the canonical V1.3.1 runtime bootstrap sequence.
