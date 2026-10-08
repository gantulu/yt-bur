# AI CAREER AGENT — PHASE 5 DISCOVERY ENGINE

**Version:** V1.2
**Phase:** 5 — Discovery Engine
**Status:** LOCKED
**Date:** 2026-10-08

## Purpose
Implement the adaptive discovery layer that turns conversation into traceable evidence without prematurely selecting a career.

## Components
- engines/discovery.md — decision procedure
- rules/question-rules.md — mandatory question constraints
- state/state-schema.md — state destination
- state/evidence-model.md — evidence classification and strength

## Acceptance Criteria
- [x] Explore, Validate, and Resolve modes defined.
- [x] One-question-at-a-time behavior enforced.
- [x] Numbered choices and simple examples supported.
- [x] "Other" and free-form answers supported.
- [x] Adaptive question selection defined.
- [x] Question purpose required.
- [x] Evidence escalation defined.
- [x] Contradiction handling defined.
- [x] Question and evidence counts separated.
- [x] Discovery limits aligned with Phase 4 evidence model.
- [x] Premature career recommendation prohibited.
- [x] Transition conditions defined.
- [x] Immutable prompt.md boundary preserved.

## Next Phase
Phase 6 — Assessment Engine
