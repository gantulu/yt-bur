# PROJECT ENGINE

**Status:** LOCKED  
**Phase:** 9

## Purpose
Convert development priorities into focused projects that build competency and generate credible career evidence.

## Inputs

Retrieve:
- AGENT.md
- state/state-schema.md
- state/evidence-model.md
- engines/development.md
- knowledge/competencies.md
- knowledge/project-types.md
- career matching state

## Preconditions

A project should have:
- a clear development or career purpose;
- a defined problem or hypothesis;
- an intended outcome;
- an AI role when AI is material to the target career;
- an evidence target.

If the development target is unclear, do not invent a project. Return the smallest missing definition.

## Procedure

1. Inspect the selected career and development priorities.
2. Identify the highest-priority competency gap.
3. Identify the evidence needed to demonstrate progress.
4. Define the smallest useful project capable of producing that evidence.
5. Select the appropriate canonical project type.
6. Define the problem.
7. Define the goal and observable success condition.
8. Define the AI role.
9. Define the technology/tools only when supported or necessary.
10. Define the workflow or approach.
11. Define implementation scope and boundaries.
12. Define the evidence that will be captured.
13. Define the next implementation step.
14. Validate that the project is feasible, focused, and aligned with the career target.

## Project Selection

Use this progression when appropriate:

Understand → Experiment → Mini Project → Workflow/Automation → Application/Agent → System/Product → Real-World Project

This is a progression model, not a mandatory sequence.

A smaller project is preferred when it can produce sufficient evidence.

## Project Definition

Every project should capture:

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

These fields align with the canonical state schema.

## AI Role

When the target career is AI-centered, explicitly identify what AI contributes.

Examples:
- generation;
- reasoning;
- classification;
- transformation;
- multimodal analysis;
- tool use;
- orchestration;
- automation;
- agentic execution.

Do not add AI merely for appearance. If AI is not materially useful, state why or reconsider the project.

## Success Condition

Prefer observable conditions:
- working output;
- successful workflow execution;
- automation completed;
- prototype usable;
- task accuracy;
- time saved;
- error reduction;
- user feedback;
- measurable outcome.

Do not fabricate results before implementation.

## Evidence Capture

Evidence may include:
- prompts/instructions;
- workflow definition;
- implementation;
- screenshots or recordings;
- source code;
- test results;
- before/after comparison;
- user feedback;
- measurable outcome.

Evidence must be recorded only after it actually exists.

## Output

Return:

### Project
- name
- type
- problem
- goal
- AI role
- approach
- technology
- workflow
- scope

### Evidence Target
- what capability it should demonstrate
- what evidence will prove it
- success condition

### Execution
- first step
- implementation status
- next step

### Validation
- career alignment
- competency alignment
- feasibility
- evidence potential

## Reassessment

Rework or replace the project when:
- the career target changes;
- the competency gap changes;
- the project fails to produce useful evidence;
- scope becomes disproportionate;
- real-world feedback reveals a better problem.

## Acceptance Criteria

- [x] Uses development priorities.
- [x] Uses canonical project types.
- [x] Smallest useful project principle defined.
- [x] AI role explicitly defined for AI-centered targets.
- [x] State project fields aligned.
- [x] Evidence capture defined.
- [x] No fabricated results.
- [x] Success condition defined.
- [x] One next implementation step defined.
