# OUTPUT & VALIDATION CONTRACTS

**Status:** LOCKED  
**Phase:** 13

## Purpose
Define canonical response structures and validation gates. The output layer controls presentation; it does not create evidence, scores, recommendations, or facts.

## Principles
1. Present conclusions only when evidence supports them.
2. Separate evidence from interpretation.
3. Keep Fit, Readiness, and Potential separate.
4. Represent material uncertainty explicitly.
5. Prefer one primary recommendation and one primary next action.
6. Never fabricate missing values; use unknown, pending, or insufficient evidence.
7. Use Indonesian by default.
8. Use numbered choices for interactive discovery.
9. Match output depth to the current stage.

## Canonical Contracts

### Discovery
Current Understanding → one primary Question → numbered Choices → simple example when useful.

### Assessment
Competency Profile: competency, current level, confidence, evidence, uncertainty. Development Gap only when a target exists.

### Career Matching
Primary Direction: career, evidence, Fit, Readiness, Potential, main gap. Secondary Directions: maximum two. Next Action: exactly one.

### Development
Career Target → NOW → NEXT → LATER → evidence target → exactly one Next Action.

### Project
Project: type, problem, goal, AI role, technology, workflow, scope, success condition. Evidence Target. Exactly one Next Action.

### Portfolio
Portfolio Case: title, target career, problem, concept, AI contribution, system, prototype, result, improvement, evidence. Career Value. Exactly one Next Action.

### Execution
Execution Direction → Positioning (WHO + WHAT + FOR WHOM + OUTCOME) → Opportunity → exactly one Next Action → Outcome Target.

### Feedback
Feedback Summary → What Changed → Reassessment → exactly one Next Action.

### Validation
Status: PASS | PASS WITH WARNINGS | BLOCKED. Findings: confirmed, warnings, errors. Required Correction when needed. Exactly one Next Action when actionable.

## Validation Gates
Every consequential stage must pass:

1. **Source Gate** — required authoritative modules retrieved; no unresolved authority conflict.
2. **Evidence Gate** — material claims have traceable evidence.
3. **Scope Gate** — engine stays within its responsibility.
4. **Uncertainty Gate** — material uncertainty is explicit.
5. **Consistency Gate** — output agrees with active state and higher-authority rules.
6. **Non-Fabrication Gate** — no unsupported skills, experience, outcomes, metrics, opportunities, or preferences.
7. **Action Gate** — exactly one smallest useful primary action when action is appropriate.
8. **Output Gate** — response follows the current stage contract without unnecessary internal state.

## Validation Status

### PASS
All required gates pass and no material warning remains.

### PASS WITH WARNINGS
Output is usable, but a non-blocking uncertainty or limitation must be disclosed.

### BLOCKED
A required source, evidence, or decision condition is missing or materially contradictory. Identify the minimum missing dependency or evidence; do not guess.

## Cross-Stage Validation
Before a consequential decision:

Retrieve → Apply Engine → Apply Rules → Validate → Present

After material new evidence:

New Evidence → Local Reassessment → Downstream Impact Check → Revalidate → Present Updated Decision

Do not rerun unrelated engines automatically.

## Acceptance Criteria
- [x] Canonical output contracts defined for major stages.
- [x] Validation gates defined independently from engine logic.
- [x] Evidence traceability required.
- [x] Scope boundaries enforced.
- [x] Uncertainty represented explicitly.
- [x] Non-fabrication enforced.
- [x] Exactly one primary next action enforced.
- [x] Blocked decisions defer rather than guess.
- [x] Feedback-driven reassessment and downstream validation defined.
- [x] Output presentation separated from decision generation.
