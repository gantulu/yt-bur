# CAREER MATCHING ENGINE

**Status:** LOCKED  
**Phase:** 7

## Purpose
Compare evidence-backed career candidates and select the strongest current AI-centered career direction while preserving uncertainty and separating fit from readiness and potential.

## Inputs
Retrieve:
- AGENT.md
- state/state-schema.md
- state/evidence-model.md
- engines/assessment.md
- knowledge/competencies.md
- knowledge/careers.md
- rules/matching-rules.md

## Procedure

1. Inspect current competency profile and active evidence.
2. Build candidate scores for all canonical careers.
3. Evaluate the five weighted dimensions:
   - Competency 45%
   - Interest 20%
   - Experience 15%
   - Activity preference 10%
   - Goal 10%
4. Record evidence IDs supporting each material dimension.
5. Rank candidates.
6. Calculate or estimate Fit separately from Readiness and Potential.
7. Identify the main competency gap for the leading candidate.
8. Apply tie-breaking rules when candidates are close.
9. Select one primary and up to two secondary directions.
10. Validate that the winner is supported by evidence rather than score alone.
11. If uncertainty can materially change the winner, request the smallest additional evidence instead of forcing a decision.

## Fit
Fit answers:
> How strongly does this career match the person's current evidence?

Fit is primarily informed by competency, interest, experience, activity preference, and goal alignment.

## Readiness
Readiness answers:
> How prepared is the person to perform this career today?

Readiness must reflect demonstrated capability and relevant experience, not enthusiasm alone.

## Potential
Potential answers:
> How plausible is development toward this direction?

Potential may consider:
- relevant current competencies;
- strength of learning/development evidence;
- interest sustainability;
- project engagement;
- realistic development gaps.

Potential is not a prediction of guaranteed success.

## Candidate Status

Each candidate should have:
- career_id
- fit
- readiness
- potential
- evidence_ids[]
- strengths[]
- gaps[]
- decision_status

Allowed decision_status:
candidate, primary, secondary, deferred, rejected_with_reason.

## Output

Return:
- primary direction;
- why it won;
- evidence;
- Fit;
- Readiness;
- Potential;
- main gap;
- up to two secondary directions;
- next action.

Do not create a development plan inside this engine. Development belongs to the Development Engine.

## Reassessment

Re-run matching when:
- competency scores materially change;
- important new experience/project evidence appears;
- goals or constraints materially change;
- feedback invalidates the current career assumption.

## Acceptance Criteria

- [x] Six canonical career candidates supported.
- [x] V1.1 matching weights preserved.
- [x] Fit/Readiness/Potential separated.
- [x] Evidence traceability required.
- [x] Primary limited to one.
- [x] Secondary limited to two.
- [x] Tie-breaking defined.
- [x] Insufficient evidence handled without fabrication.
- [x] Development decisions remain outside matching scope.
