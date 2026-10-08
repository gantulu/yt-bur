# VALIDATION RULES

**Status:** LOCKED  
**Phase:** 13

## Purpose
Mandatory validation rules applied whenever a stage is completed or a consequential decision is finalized.

## Rules
1. Required authoritative modules must be retrieved.
2. Material claims must trace to evidence or authoritative reference data.
3. User-specific facts must never be invented.
4. Evidence, interpretation, score, confidence, Fit, Readiness, and Potential must remain distinct.
5. Each engine must remain within its defined scope.
6. Material uncertainty must be disclosed or the decision deferred.
7. Contradictions must be preserved and resolved or explicitly marked unresolved.
8. Outputs must not contradict higher-authority sources or active state without documented new evidence.
9. A blocked decision must identify its minimum missing evidence/dependency.
10. When action is appropriate, output exactly one smallest useful primary next action.

## Stage-Specific Checks

### Discovery
- One primary question.
- No premature career recommendation.
- Question has decision value.

### Assessment
- Competency scores are evidence-supported.
- Confidence is separate from score.
- No career selection.

### Matching
- All relevant candidates considered.
- V1.1 weights preserved.
- One primary and maximum two secondary directions.
- Fit, Readiness, Potential separated.

### Development
- Career target exists.
- Gaps derive from competency evidence.
- NOW/NEXT/LATER is prioritized.

### Project
- Project has a problem, goal, AI role when material, and evidence target.
- Scope is feasible.
- Planned results are not presented as achieved.

### Portfolio
- Material claims trace to actual project/evidence.
- Planned, implemented, tested, demonstrated, and outcome states remain distinct.

### Execution
- Positioning follows WHO + WHAT + FOR WHOM + OUTCOME.
- Opportunity weights are preserved.
- No unsupported expertise or opportunity claims.

### Feedback
- Observation is separated from interpretation.
- Outcomes are traceable to an actual event.
- Reassessment is limited to affected scope first.

## Status Decision
PASS when all required checks pass.
PASS WITH WARNINGS when only non-blocking uncertainty remains and it is disclosed.
BLOCKED when a required source/evidence/condition is missing or materially contradictory.

## Acceptance Criteria
- [x] Mandatory validation rules established.
- [x] Stage-specific checks defined.
- [x] Non-fabrication enforced.
- [x] Scope boundaries enforced.
- [x] Blocked status defined.
