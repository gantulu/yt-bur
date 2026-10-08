# ASSESSMENT ENGINE

**Status:** LOCKED  
**Phase:** 6

## Purpose
Convert discovery evidence into a calibrated competency profile without confusing interest, confidence, familiarity, or activity with demonstrated capability.

## Inputs
Retrieve:
- AGENT.md
- state/state-schema.md
- state/evidence-model.md
- engines/discovery.md when discovery evidence is being assessed
- knowledge/competencies.md
- authoritative career/reference modules when downstream matching requires them

## Operating Procedure

1. Inspect active evidence.
2. Classify each evidence item by source type.
3. Map relevant evidence to one or more competencies.
4. Evaluate evidence quality and strength.
5. Estimate a competency score from demonstrated capability.
6. Estimate confidence separately from score.
7. Record evidence IDs supporting the assessment.
8. Identify gaps and unresolved uncertainty.
9. Recalculate only competencies materially affected by new evidence.
10. Validate the profile before passing it to matching.

## Evidence Interpretation

Use the evidence hierarchy:
Interest 1 → Preference 1 → Self-report 2 → Experience 3 → Concrete example 4 → Project 5 → Demonstrated result 5.

The weight is evidence strength, not a direct score conversion.

### Important distinctions
- Interest indicates attraction, not capability.
- Preference indicates desired activity, not capability.
- Self-report is useful but weaker than observable evidence.
- Experience indicates exposure/performance, but does not automatically prove mastery.
- A completed project is stronger evidence than stated familiarity.
- A demonstrated result is strong evidence of applied capability.
- Tool familiarity does not equal expertise.

## Scoring Rules

Assign 1–5 only when the available evidence supports a meaningful estimate.

Use:
- 1 when evidence supports only exposure or very limited capability.
- If there is no meaningful capability evidence, do not assign a competency score; mark it unknown/provisional with low confidence.
- 2 when basic/guided capability is evidenced.
- 3 when independent working capability is evidenced.
- 4 when strong, repeatable capability is evidenced.
- 5 when advanced/system-level capability is evidenced.

Do not inflate a score because the user is enthusiastic about a competency.

If evidence is insufficient, keep the score provisional and lower confidence rather than inventing evidence.

## Confidence

Confidence reflects assessment certainty, not ability.

Increase confidence when:
- multiple relevant evidence items agree;
- evidence is concrete or demonstrated;
- evidence is recent and specific;
- results are observable or reproducible.

Decrease confidence when:
- evidence is only self-report;
- evidence is old, vague, or indirect;
- evidence conflicts;
- mapping to the competency is ambiguous.

## Gap Detection

For a target career:
gap = target competency level − current competency level.

Do not define a development gap until a target direction exists or a target level is explicitly supplied.

## Reassessment Triggers

Reassess when:
- new project evidence appears;
- a demonstrated result changes the evidence base;
- contradictory evidence is material;
- a major career direction changes;
- meaningful feedback indicates the current score is inaccurate.

## Output

Return a compact assessment object:

- competency
- score
- confidence
- evidence_ids
- rationale
- gap_if_target_exists
- uncertainty

The engine must not recommend a career. Career selection belongs to the matching engine.

## Acceptance Criteria

- [x] Six canonical competencies supported.
- [x] Evidence weights preserved.
- [x] Score separated from confidence.
- [x] Unsupported scores prohibited.
- [x] Evidence traceability required.
- [x] Contradictions handled without deletion.
- [x] Career recommendation remains outside assessment scope.
