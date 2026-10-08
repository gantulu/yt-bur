# PORTFOLIO ENGINE

**Status:** LOCKED  
**Phase:** 10

## Purpose
Convert completed project evidence into credible portfolio proof that communicates capability, AI contribution, implementation, and observable outcomes.

## Inputs

Retrieve:
- AGENT.md
- state/state-schema.md
- state/evidence-model.md
- engines/project.md
- engines/development.md
- knowledge/competencies.md
- career matching state
- completed project evidence

## Preconditions

A portfolio item must be grounded in an actual project or demonstrated result.

Do not create portfolio claims from:
- intentions;
- plans;
- course completion alone;
- unverified self-reports;
- fabricated metrics;
- unfinished work presented as completed.

If a project is incomplete, clearly mark it as in progress and do not present missing results as evidence.

## Procedure

1. Inspect the selected career direction.
2. Inspect the project and its actual implementation status.
3. Collect active evidence IDs.
4. Identify the competency demonstrated.
5. Identify the problem addressed.
6. Explain the AI contribution.
7. Describe the system/workflow/prototype that was actually built.
8. Record the actual result or explicitly state that results are pending.
9. Identify improvements or lessons supported by evidence.
10. Map the portfolio item to the target career.
11. Validate every material claim against evidence.
12. Produce a concise portfolio-ready case structure.

## Canonical Portfolio Structure

Every completed portfolio case should follow:

Problem
→ Concept
→ AI
→ System
→ Prototype
→ Result
→ Improvement
→ Evidence

### Problem
What real problem, need, or opportunity was addressed.

### Concept
The proposed solution and why the approach was chosen.

### AI
What AI materially contributed to the solution.

### System
How the components, workflow, automation, agent, or application worked.

### Prototype
What was actually implemented.

### Result
What actually happened after implementation.

Only verified results may be stated as facts.

### Improvement
What was learned, changed, optimized, or should be improved next.

### Evidence
References to the underlying project/evidence records.

## Evidence Integrity

Use evidence IDs for material claims.

Distinguish:

- planned capability → intended;
- implemented capability → built;
- tested capability → verified through testing;
- demonstrated capability → supported by observable evidence;
- outcome → supported by actual result.

Do not convert one category into another.

## Portfolio Quality

A strong portfolio item should make clear:

1. What problem was solved.
2. What the user/person/business needed.
3. What AI did.
4. What the creator built.
5. How the system worked.
6. What result was achieved.
7. What evidence proves the claims.

## Career Alignment

For the selected career, identify:
- demonstrated competencies;
- relevant AI capability;
- relevant technology/automation/creative capability;
- evidence strength;
- remaining gaps.

Portfolio evidence may improve readiness assessment, but it must not automatically change career fit without the matching engine.

## Output

Return:

### Portfolio Case
- title
- target career
- problem
- concept
- AI contribution
- system
- prototype
- result
- improvement
- evidence

### Evidence Map
For each major claim:
- claim
- evidence_id
- evidence status

### Career Value
- competencies demonstrated
- relevance to target career
- evidence strength
- remaining gap

### Next Action
Exactly one improvement, publication, validation, or evidence-capture action.

## Reassessment

Revisit a portfolio case when:
- new project evidence appears;
- results change;
- user feedback appears;
- the project is improved;
- the target career changes;
- a material claim can no longer be supported.

## Acceptance Criteria

- [x] Portfolio requires real project/evidence grounding.
- [x] Canonical Problem → Concept → AI → System → Prototype → Result → Improvement → Evidence structure implemented.
- [x] AI contribution explicitly documented.
- [x] Material claims traceable to evidence.
- [x] Planned vs implemented vs demonstrated vs outcome distinguished.
- [x] No fabricated results or metrics.
- [x] Career alignment separated from career matching.
- [x] One next action defined.
