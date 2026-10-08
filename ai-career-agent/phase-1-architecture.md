# AI CAREER AGENT — PHASE 1 ARCHITECTURE

**Version:** V1.2
**Phase:** 1 — Agent Architecture
**Status:** LOCKED
**Date:** 2026-10-08

## 1. Purpose
Define the complete modular architecture, responsibility boundaries, dependency graph, retrieval strategy, and validation boundaries for the AI Career Discovery & Development Agent.

Phase 1 defines where responsibilities live and how modules depend on each other. It does not redefine the locked V1 prompt.md.

## 2. Architectural Principle
AGENT → INSTRUCTIONS → STATE → ENGINES → RULES + KNOWLEDGE → VALIDATION → OUTPUT

Operational flow:
USER EVIDENCE → DISCOVERY → ASSESSMENT → MATCHING → DEVELOPMENT → PROJECT → PORTFOLIO → EXECUTION → FEEDBACK → REASSESSMENT

## 3. Module Layers

### Entry Point
AGENT.md owns agent identity, mission, source-of-truth hierarchy, retrieval map, runtime behavior, immutable boundaries, and high-level operating loop.

### Instructions
Path: instructions/
- role.md
- principles.md
- behavior.md
- workflow.md

Owns role, operating principles, conversation behavior, and execution sequence.

### State
Path: state/
- state-schema.md
- evidence-model.md

Owns session stage, question count, user goals/interests/preferences/constraints, competency scores/confidence, evidence, career candidates, development priorities, projects, portfolio evidence, execution outcomes, feedback, and reassessment flags.

State is the current working model of the user and must never contain invented facts.

### Engines
Path: engines/
- discovery.md
- assessment.md
- matching.md
- development.md
- project.md
- portfolio.md
- execution.md

Engines define decision procedures. They consume rules, knowledge, and state; they do not invent domain data.

### Rules
Path: rules/
- question-rules.md
- matching-rules.md
- validation-rules.md

Rules define mandatory decision constraints.

### Knowledge
Path: knowledge/
- competencies.md
- careers.md
- questions.md
- project-types.md

Knowledge contains reference data. It never claims that the user possesses a capability.

### Output
Path: output/
- output-contracts.md

Owns presentation contracts for discovery, career recommendation, development, project, portfolio, execution, and validation/error states.

## 4. Dependency Graph

Foundation:
AGENT → instructions + state → evidence-model

Discovery:
AGENT → behavior + state → discovery + question-rules + questions + competencies

Assessment:
state/evidence-model → assessment → competencies

Matching:
state → matching → matching-rules + careers + competencies

Development:
state/competencies → development → competencies + careers

Project:
state/development → project → project-types + competencies

Portfolio:
state/projects → portfolio → output-contracts

Execution:
state/profile + portfolio → execution → careers + output-contracts

Validation:
all module outputs → validation-rules → output-contracts

## 5. Dependency Rules
1. AGENT.md is the navigation layer.
2. Instructions define behavior.
3. State defines current user/session knowledge.
4. Engines define decision procedures.
5. Rules define mandatory constraints.
6. Knowledge defines reference data.
7. Output defines presentation.
8. Validation may inspect every layer but must not silently rewrite authoritative inputs.
9. Engines may consume lower-level modules but must not redefine their source-of-truth rules.
10. Knowledge must not contain user-specific claims.
11. State must not contain unsupported claims.
12. A module may not depend on a later-stage output unless explicitly declared.

## 6. Source-of-Truth Boundaries
- Legacy AI Creative Technologist V1 → root prompt.md, immutable
- Agent navigation/runtime contract → AGENT.md
- Core behavior → instructions/
- Current user/session state → state/
- Decision procedures → engines/
- Mandatory constraints → rules/
- Reference data → knowledge/
- Presentation format → output/
- Validation → rules/validation-rules.md

If sources conflict, the higher-authority source wins. Do not silently merge contradictory rules.

## 7. Retrieval Strategy
Use minimum sufficient retrieval.

Initial discovery:
AGENT.md, instructions/behavior.md, state/state-schema.md, state/evidence-model.md, engines/discovery.md, engines/assessment.md, rules/question-rules.md, knowledge/questions.md, knowledge/competencies.md

Career matching:
AGENT.md, state/state-schema.md, engines/matching.md, rules/matching-rules.md, knowledge/careers.md, knowledge/competencies.md

Development/project planning adds:
engines/development.md, engines/project.md, knowledge/project-types.md

Portfolio/execution adds only relevant portfolio, execution, and output modules.

Validation rules are retrieved whenever a stage is completed or a decision is finalized.

## 8. Data Flow
User response → evidence extraction → state update → assessment → career candidates → evidence-based selection → development gap → project/evidence plan → portfolio proof → positioning/opportunity → outcome → feedback → reassessment.

The flow is iterative. New evidence can change scores, ranking, priorities, and recommendations.

## 9. Separation of Concerns
- What the agent is → AGENT/instructions
- What is known about the user → state
- How a decision is made → engines
- Which constraints must be obeyed → rules
- What reference information exists → knowledge
- How the result is shown → output
- Whether the result is acceptable → validation

## 10. Locked Legacy Boundary
The existing root prompt.md remains immutable. Phase 1 does not replace, rewrite, or merge it into the new architecture. The new agent may reference AI Creative Technologist V1 as a career/domain reference, but must not mutate its definition without a separately versioned change.

## 11. Phase 1 Acceptance Criteria
- [x] Complete module layers defined.
- [x] Responsibility boundary defined.
- [x] Dependency graph defined.
- [x] Retrieval strategy defined.
- [x] Source-of-truth boundaries defined.
- [x] Data flow defined.
- [x] Separation of concerns defined.
- [x] Legacy V1 immutable boundary preserved.
- [x] Architecture is ready for Phase 2–4 foundation implementation.

## 12. Next Phase
Phase 2 — Agent Entry Point

Phase 2 will formalize AGENT.md as the operating/navigation contract and align the physical repository module tree with this architecture.
