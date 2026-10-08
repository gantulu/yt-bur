# STATE ARCHITECTURE — STATE SCHEMA

**Status:** LOCKED  
**Phase:** 4

## Purpose
Define the canonical working-state structure used by the agent. State represents what is currently known, inferred, pending, or unresolved about the person and the career-development process.

## State Principles
- Never write unsupported user facts into state.
- Preserve evidence provenance.
- Separate observed evidence from interpretation.
- Separate score from confidence.
- Allow unknown, pending, and contradictory values.
- New evidence may update previous conclusions.
- State is session-scoped unless explicitly persisted by the host system.

## Top-Level Schema
state
├── meta
├── session
├── person
├── evidence
├── competencies
├── career_matching
├── development
├── projects
├── portfolio
├── execution
├── feedback
└── next_action

## meta
- schema_version
- agent_version
- last_updated
- source_version

## session
- stage
- status
- question_count
- evidence_count
- started_at
- last_activity
- discovery_status

Allowed stages: DISCOVER, ASSESS, MATCH, DEVELOP, BUILD, PROVE, POSITION, EXECUTE, FEEDBACK, REASSESS

## person
- goals
- interests
- preferences
- constraints
- experience_summary

Every populated item representing a user-specific claim must link to evidence IDs.

## evidence
Each evidence record:
- evidence_id
- category
- statement
- source_type
- source_detail
- strength
- confidence
- timestamp
- supports[]
- contradicts[]
- status

source_type: interest, preference, self_report, experience, concrete_example, project, demonstrated_result.

status: active, superseded, contradictory, unresolved.

## competencies
Canonical dimensions:
- AI
- Creative
- Technology
- Automation
- Problem Solving
- Product Thinking

Each competency contains:
- score: 1–5
- confidence: 0–5
- evidence_ids[]
- gap
- status

Score represents demonstrated/current capability. Confidence represents confidence in the assessment.

## career_matching
Contains candidates[], primary, secondary[], fit, readiness, potential, evidence_ids[], decision_status.

Candidate scores must be traceable to the matching engine and evidence.

## development
Contains priority, gaps[], NOW[], NEXT[], LATER[], target_evidence[].

Development priorities must reference the selected career direction and competency gaps.

## projects
Each project contains:
- project_id
- type
- problem
- goal
- approach
- ai_role
- technology
- workflow
- implementation_status
- result
- evidence_ids[]
- next_step

## portfolio
Contains:
- problem
- concept
- ai
- system
- prototype
- result
- improvement
- evidence_ids[]
- quality_status

Portfolio claims must be backed by project/evidence records.

## execution
Contains:
- track
- positioning
- opportunities[]
- actions[]
- outcomes[]

Tracks: Employment, Freelance, Contract, Consulting, Creator, AI Service, AI Product, AI Business.

## feedback
Contains:
- outcomes[]
- new_evidence_ids[]
- reassessment_needed
- reason

## next_action
Exactly one primary next action unless an output contract explicitly requires otherwise:
- action
- reason
- evidence_needed[]
- stage

## State Update Rule
For every user response:
1. Extract candidate evidence.
2. Classify evidence type.
3. Assign an evidence ID.
4. Preserve original meaning.
5. Link affected competencies/careers where justified.
6. Recalculate only affected assessments.
7. Mark contradictory or superseded evidence.
8. Revalidate downstream decisions.
9. Select the smallest useful next action.

Never silently delete evidence that explains a previous decision.
