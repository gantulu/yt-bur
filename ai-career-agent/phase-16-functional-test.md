# @GITHUB FUNCTIONAL TEST

**Status:** LOCKED  
**Phase:** 16

## Purpose
Verify that the integrated AI Career Discovery & Development Agent can retrieve its authoritative runtime modules through GitHub and that the retrieval contract points to available canonical files.

## Test Scope

### T01 — Primary Entry Point
- Path: `ai-career-agent/AGENT.md`
- Result: PASS
- Verified SHA: `cfe980b7edbf36a0475a70bbcbe7dcfcda8264bc`

### T02 — Retrieval Map
- Path: `ai-career-agent/retrieval-map.md`
- Result: PASS
- Verified SHA: `83758b90f56065f7f24b7ffd22aef974ca5fe34b`

### T03 — Integration Contract
- Path: `ai-career-agent/integration.md`
- Result: PASS
- Verified SHA: `eb7f2e323653cf2f4b3b2d655c650686bf836361`

### T04 — Instruction + State Bundle
- Behavior: PASS
- State schema: PASS
- Evidence model: PASS

### T05 — Engine Bundle
- Discovery: PASS
- Assessment: PASS
- Matching: PASS
- Development: PASS
- Project: PASS
- Portfolio: PASS
- Execution: PASS
- Feedback: PASS

### T06 — Rules Bundle
- Question rules: PASS
- Matching rules: PASS
- Development rules: PASS
- Validation rules: PASS

### T07 — Knowledge + Output Bundle
- Competencies: PASS
- Careers: PASS
- Project types: PASS
- Output contracts: PASS

### T08 — Immutable Root Boundary
- Path: `prompt.md`
- Result: PASS
- Verified SHA: `08deae89a2bcc69958844aa8d843eba8ffc52408`
- No modification detected.

### T09 — Missing Dependency Handling
- `knowledge/questions.md` is intentionally absent.
- Retrieval map explicitly excludes it from Discovery.
- Discovery uses `engines/discovery.md` + `rules/question-rules.md`.
- Result: PASS.

## Functional Retrieval Result

```
AGENT.md
→ retrieval-map.md
→ stage bundle
→ engine
→ rules / knowledge
→ validation
→ output
```

All tested canonical paths were retrievable from the repository.

## Limitations

This phase verifies GitHub repository retrieval and architectural wiring. It does not simulate a complete end-user multi-turn conversation inside every ChatGPT client surface.

## Acceptance Criteria

- [x] Primary agent entry point retrievable.
- [x] Retrieval map retrievable.
- [x] Integration contract retrievable.
- [x] All completed engines retrievable.
- [x] Required rules retrievable.
- [x] Required knowledge modules retrievable.
- [x] Output contract retrievable.
- [x] Immutable prompt boundary verified.
- [x] Missing optional/reference path handled without fabrication.
- [x] Functional retrieval test passed.
