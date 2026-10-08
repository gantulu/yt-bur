# DEVELOPMENT ENGINE

**Status:** LOCKED  
**Phase:** 8

## Purpose
Convert a selected career direction and competency profile into a focused development roadmap that closes the most valuable gaps while generating practical evidence.

## Inputs

Retrieve:
- AGENT.md
- state/state-schema.md
- state/evidence-model.md
- engines/assessment.md
- engines/matching.md
- knowledge/competencies.md
- knowledge/careers.md
- rules/development-rules.md

## Preconditions

A development plan requires:
- a primary career direction, or an explicitly defined target career;
- current competency evidence;
- sufficient confidence to identify meaningful gaps.

If the career direction is unresolved, do not invent a target. Return the minimum evidence needed to resolve it.

## Procedure

1. Inspect primary career direction and matching evidence.
2. Inspect current competency scores and confidence.
3. Identify target competencies required by the selected direction.
4. Compare current capability with target capability.
5. Identify meaningful gaps.
6. Prioritize gaps using career impact, interest alignment, and project relevance.
7. Sequence priorities into NOW, NEXT, and LATER.
8. Attach an observable evidence target to each high-priority development item.
9. Prefer project-based/application-based development.
10. Validate that the roadmap is feasible and not overloaded.
11. Select one primary next action.

## Target Competencies

Target levels are directional rather than claims about the user. Use the career's actual demands to establish them.

The engine must distinguish:
- current score;
- target level;
- gap;
- confidence;
- evidence target.

## Development Output

Return:

### Career Target
- primary career
- reason
- Fit
- Readiness
- Potential

### Gap Analysis
For each material gap:
- competency
- current level
- target level
- gap
- evidence supporting current level
- why the gap matters

### Roadmap
- NOW
- NEXT
- LATER

Each item:
- capability to develop
- practical activity
- evidence target
- dependency, if any

### Next Action
Exactly one smallest useful action.

## Learning Principle

Prefer:
Understand → Practice → Build → Measure → Reflect → Reassess

Do not equate:
watching/reading/course completion → mastery.

## Reassessment

Recalculate development priorities when:
- the primary career changes;
- competency evidence changes materially;
- a development project produces new evidence;
- goals or constraints change;
- feedback indicates the plan is ineffective.

## Acceptance Criteria

- [x] Career target required.
- [x] Competency gaps defined.
- [x] Current score separated from target.
- [x] NOW/NEXT/LATER implemented.
- [x] Evidence target required.
- [x] Applied learning preferred.
- [x] Plan avoids unsupported assumptions.
- [x] Single next action defined.
