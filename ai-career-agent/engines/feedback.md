# FEEDBACK ENGINE

**Status:** LOCKED  
**Phase:** 12

## Purpose
Convert real-world outcomes, feedback, failures, successes, and new constraints into reliable evidence, update career-development state, and trigger targeted reassessment when justified.

The Feedback Engine closes the loop:
EXECUTE → OUTCOME → EVIDENCE → REASSESS → NEXT ACTION

## Inputs
Retrieve:
- AGENT.md
- state/state-schema.md
- state/evidence-model.md
- engines/assessment.md
- engines/matching.md
- engines/development.md
- engines/project.md
- engines/portfolio.md
- engines/execution.md
- current feedback and execution state

## Preconditions
Feedback must come from an actual interaction, test, implementation, project, opportunity, user/client response, application process, or other observable event.
Do not treat expectation as outcome.
If feedback is vague, preserve it as unresolved evidence rather than converting it into a strong conclusion.

## Feedback Sources
Valid sources include:
- project/test result;
- user feedback;
- client feedback;
- employer/recruiter feedback;
- application/interview outcome;
- audience response;
- product usage;
- workflow performance;
- measurable operational result;
- failure or rejection;
- self-reflection tied to a concrete event.

## Procedure
1. Inspect the action or decision that produced the feedback.
2. Capture the actual event and outcome.
3. Separate observation from interpretation.
4. Classify each new evidence item.
5. Assign evidence strength and confidence.
6. Link evidence to affected competencies, career directions, development items, projects, portfolio claims, or execution assumptions.
7. Detect contradiction with existing evidence.
8. Recalculate only materially affected assessments.
9. Determine whether matching, development, project, portfolio, or execution must be reassessed.
10. Select exactly one smallest useful next action.

## Evidence Integrity
Always distinguish:
- planned → what was intended;
- attempted → what was actually tried;
- observed → what happened;
- tested → what was verified;
- demonstrated → what can be reproduced or shown;
- outcome → what measurable or externally observable result occurred.

A failure is evidence. It must not automatically be interpreted as lack of career fit.
A rejection is evidence about that opportunity/process, not automatic proof that the person is unsuitable for the career.
Positive feedback is not proof of mastery unless the evidence supports that conclusion.

## Outcome Interpretation
### Success
Ask:
- What specifically worked?
- What evidence demonstrates it?
- Is the result repeatable?
- Which competency did it demonstrate?

### Failure
Ask:
- What specifically failed?
- Was the failure caused by skill, process, scope, execution, environment, or external factors?
- What can be tested or improved next?

### Contradiction
If new evidence conflicts with an existing conclusion:
- preserve both evidence records;
- mark the relevant evidence relationship;
- lower confidence when appropriate;
- reassess the affected decision;
- do not silently overwrite the previous evidence.

## Reassessment Routing
Route only when evidence materially affects the corresponding area.

### Assessment
Reassess when new evidence changes the estimate of a competency.

### Matching
Reassess when evidence materially changes career fit, goals, experience, or activity preference.

### Development
Reassess when a competency gap closes, changes, or a new critical gap appears.

### Project
Reassess when project scope, technical direction, or evidence target changes.

### Portfolio
Reassess when a result, implementation status, feedback, or material portfolio claim changes.

### Execution
Reassess when opportunity fit, positioning, accessibility, constraints, or real-world market feedback changes.

Do not rerun the entire pipeline when a local reassessment is sufficient.

## Feedback State
Update the feedback state fields:
- outcomes[]
- new_evidence_ids[]
- reassessment_needed
- reason

Also update only affected downstream state.

## Feedback Quality
Prefer feedback that is:
1. Specific
2. Direct
3. Recent
4. Relevant
5. Observable
6. Reproducible
7. Outcome-linked

Feedback quality does not automatically determine career fit.

## Output
### Feedback Summary
- action/context
- observed result
- feedback source
- evidence strength
- confidence

### What Changed
- new evidence
- affected competency/career/project/portfolio/execution state
- contradiction or confirmation

### Reassessment
- required: yes/no
- engine(s) affected
- reason

### Next Action
Exactly one smallest useful action.

## Reassessment Rules
Reassess only the smallest affected scope first.
Escalate when:
- local evidence changes a consequential downstream decision;
- contradictions remain unresolved;
- new evidence materially changes the primary career direction;
- execution feedback invalidates positioning;
- repeated outcomes reveal a systematic pattern.

After reassessment, revalidate downstream decisions before presenting a new recommendation.

## Safety and Non-Fabrication
Never invent:
- user/client reactions;
- success metrics;
- employment outcomes;
- revenue;
- interview results;
- audience growth;
- competency improvements;
- external validation.

If an outcome is unknown, state that it is unknown.

## Acceptance Criteria
- [x] Real-world feedback is converted into traceable evidence.
- [x] Observation is separated from interpretation.
- [x] Planned/attempted/observed/tested/demonstrated/outcome states are distinguished.
- [x] Positive and negative outcomes are both treated as evidence.
- [x] Failure/rejection is not automatically treated as career mismatch.
- [x] Contradictions are preserved and routed for reassessment.
- [x] Reassessment is scoped to affected engines.
- [x] Downstream state is revalidated after material changes.
- [x] Exactly one smallest useful next action is produced.
- [x] No fabricated outcomes or feedback.
