# AGENT INTEGRATION

**Status:** LOCKED  
**Phase:** 15

## Purpose
Define the integrated operating contract connecting retrieval, state, engines, rules, knowledge, validation, and output.

## Integration Flow
USER INPUT → AGENT → RETRIEVAL MAP → STATE → ACTIVE ENGINE → RULES + KNOWLEDGE → VALIDATION → OUTPUT → STATE UPDATE → NEXT ACTION

## Stage Handoff
DISCOVERY → ASSESSMENT → MATCHING → DEVELOPMENT → PROJECT → PORTFOLIO → EXECUTION → FEEDBACK → REASSESSMENT.

A stage remains active when its exit conditions are not satisfied. Never force progression.

## Module Authority
- AGENT.md: navigation and runtime contract
- instructions/: behavior
- state/: session and evidence model
- engines/: decision procedures
- rules/: mandatory constraints
- knowledge/: reference data
- retrieval-map.md: minimum-sufficient retrieval
- output/: presentation contracts
- root prompt.md: immutable AI Creative Technologist V1 reference

## Integration Rules
1. Retrieve the minimum stage bundle.
2. Apply the active engine.
3. Apply authoritative rules and reference data.
4. Validate consequential results.
5. Present only validated conclusions.
6. Record new evidence with provenance.
7. Reassess only affected downstream decisions.
8. Produce exactly one primary next action when appropriate.
9. Never fabricate user facts, results, opportunities, or constraints.
10. Preserve stage boundaries.

## Cross-Stage Integrity
- Matching selects career direction.
- Development identifies capability gaps.
- Project creates evidence opportunities.
- Portfolio packages actual proof.
- Execution converts validated capability into real-world action.
- Feedback converts actual outcomes into evidence and routes reassessment.

No later engine may silently redefine an earlier-stage decision.

## Failure Handling
If a required dependency is unavailable, follow the retrieval and failure contract. If a consequential dependency is missing, return BLOCKED and identify the minimum missing dependency.

## Acceptance Criteria
- [x] All completed engines have an explicit integration path.
- [x] Retrieval, state, rules, validation, and output are connected.
- [x] Stage boundaries are preserved.
- [x] Feedback closes the loop.
- [x] Minimum-sufficient retrieval remains authoritative.
- [x] Immutable prompt.md boundary is preserved.
- [x] No-fabrication contract is preserved.
