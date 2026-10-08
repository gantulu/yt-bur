# AI CAREER AGENT — PHASE 0 PLATFORM CONTRACT

**Version:** V1.2
**Phase:** 0 — Platform & Documentation Research
**Status:** LOCKED
**Date:** 2026-10-08

## 1. Purpose

Phase 0 defines the platform and documentation constraints for the AI Career Discovery & Development Agent.

The agent is designed primarily to be used inside ChatGPT with GitHub-connected repository access. The repository is the source of truth for the agent's modular knowledge, rules, workflows, and future runtime instructions.

Phase 0 does not implement the career engines. It establishes the contract they must follow.

---

## 2. Target Runtime

### Primary runtime

- ChatGPT conversation
- GitHub connected to ChatGPT
- Repository content retrieved on demand
- Human user interacts directly with the agent through conversation

### Secondary runtime

The same modular specification may later be adapted to:
- ChatGPT Workspace Agents
- GPT/agent configuration where available
- Codex-assisted implementation
- Other LLM runtimes

The repository architecture must not depend on a single runtime-specific implementation.

---

## 3. GitHub Retrieval Contract

According to the current OpenAI GitHub integration documentation:

1. ChatGPT can retrieve permitted repository content on demand.
2. GitHub access does not create a synchronized repository index.
3. The repository selector identifies repositories, not individual files.
4. Within a supported GitHub-connected experience, the user can ask ChatGPT to search using a file name, function name, error message, or known path.
5. Repository access is controlled by the GitHub connection and repository permissions.
6. The GitHub ChatGPT app is read-oriented for repository analysis/search; direct creation, editing, and pushing to GitHub are handled through Codex where supported.

### Architectural consequence

The repository MUST be structured for retrieval.

Do not assume that ChatGPT will automatically read the entire repository before answering.

The agent must have:
- a clear entry point;
- predictable file names;
- explicit module boundaries;
- small, focused documents;
- source-of-truth declarations;
- cross-references between modules.

---

## 4. Instruction vs Knowledge Contract

OpenAI documentation distinguishes between:

### Instructions

Instructions define:
- behavior;
- workflow;
- decision process;
- response requirements;
- constraints;
- validation behavior.

### Knowledge / reference material

Knowledge provides:
- definitions;
- domain information;
- reference data;
- examples;
- career profiles;
- competency information;
- question banks;
- project types;
- rules/data used by the engines.

### Architecture rule

Do not put the entire system into one giant prompt.

Use:

AGENT
→ CORE INSTRUCTIONS
→ STATE
→ ENGINES
→ RULES
→ KNOWLEDGE
→ OUTPUT
→ VALIDATION

Behavior belongs to instruction/engine/rule modules.

Reference information belongs to knowledge/data modules.

---

## 5. Prompt Design Contract

The agent must follow these prompt-design principles:

### 5.1 Clarity

Instructions must be:
- explicit;
- specific;
- unambiguous;
- operational.

### 5.2 Explicit workflow

Multi-step behavior must be represented as explicit sequences.

Example:

WHEN condition
→ perform action
→ update state
→ validate result
→ continue or stop.

### 5.3 Positive operational instructions

Prefer:

"Ask one question at a time."

over:

"Do not ask multiple questions."

Negative constraints may still be used when necessary for safety or validation.

### 5.4 Structured documents

Use:
- headings;
- numbered steps;
- tables where useful;
- explicit schemas;
- named rules;
- examples for important classifications.

### 5.5 Iterative validation

Every major module must be testable independently before the complete agent is considered validated.

---

## 6. Repository Architecture Contract

The planned repository architecture is:

```
ai-career-agent/
├── README.md
├── AGENT.md
│
├── instructions/
│   ├── role.md
│   ├── principles.md
│   ├── behavior.md
│   └── workflow.md
│
├── state/
│   ├── state-schema.md
│   └── evidence-model.md
│
├── engines/
│   ├── discovery.md
│   ├── assessment.md
│   ├── matching.md
│   ├── development.md
│   ├── project.md
│   ├── portfolio.md
│   └── execution.md
│
├── rules/
│   ├── question-rules.md
│   ├── matching-rules.md
│   └── validation-rules.md
│
├── knowledge/
│   ├── competencies.md
│   ├── careers.md
│   ├── questions.md
│   └── project-types.md
│
└── output/
    └── output-contracts.md
```

This is an architectural target, not a requirement to create all files during Phase 0.

---

## 7. Entry Point Contract

A future `AGENT.md` will be the repository's primary navigation and operating contract.

It must eventually define:

1. What the agent is.
2. What the agent does.
3. The source-of-truth policy.
4. Which modules are authoritative for each decision.
5. How modules should be retrieved.
6. The execution sequence.
7. How state is maintained.
8. How validation is performed.
9. What to do when required information is missing.
10. What must never be fabricated.

Phase 0 does not implement `AGENT.md`; that belongs to Phase 2.

---

## 8. Source-of-Truth Policy

The agent must use this authority hierarchy:

1. Current locked version specification
2. Repository module explicitly marked authoritative
3. Other repository reference material
4. User-provided information in the current conversation
5. External documentation/research
6. Model knowledge

If sources conflict:

- higher authority wins;
- do not silently merge contradictory rules;
- identify the conflict when it affects the decision;
- never fabricate a missing rule.

### Version boundary

Existing V1 `prompt.md` remains locked and unchanged.

V1.1 and V1.2 are separate evolution layers.

Phase 0 MUST NOT modify the V1 canonical prompt.

---

## 9. Retrieval Strategy

The agent should retrieve the minimum relevant set of modules needed for the current task.

### Example

For initial career discovery:

```
AGENT.md
→ instructions/role.md
→ instructions/behavior.md
→ state/state-schema.md
→ state/evidence-model.md
→ engines/discovery.md
→ engines/assessment.md
→ rules/question-rules.md
→ knowledge/competencies.md
→ knowledge/questions.md
```

For career matching:

```
AGENT.md
→ state/state-schema.md
→ engines/matching.md
→ rules/matching-rules.md
→ knowledge/careers.md
→ knowledge/competencies.md
```

Do not retrieve unrelated modules unless required by dependencies.

---

## 10. Module Contract

Every module should have:

- clear title;
- version;
- status;
- purpose;
- scope;
- inputs;
- outputs;
- rules;
- dependencies;
- source of truth;
- examples where ambiguity is possible;
- validation requirements.

A module should answer one primary question.

### Engine

Defines **how decisions are made**.

### Rule

Defines **what decision rule must be applied**.

### Knowledge

Defines **what information/data is available**.

### State

Defines **what the agent currently knows about the user/session**.

### Output

Defines **how results are presented**.

---

## 11. No-Fabrication Contract

The agent MUST NOT invent:

- user experience;
- user skills;
- user interests;
- project results;
- career history;
- portfolio evidence;
- tool expertise;
- achievements;
- external facts presented as verified facts;
- repository modules that do not exist;
- rules that are not defined.

When evidence is insufficient, the agent must:
- ask for evidence;
- mark uncertainty;
- or defer the decision.

---

## 12. Testing Contract

The agent will eventually be evaluated at four levels:

### Retrieval

Can ChatGPT find the correct module?

### Interpretation

Does it understand the module correctly?

### Decision

Does it apply the correct rule?

### Output

Does it produce the required response format?

A successful retrieval alone does not prove that the agent is behaviorally correct.

---

## 13. Phase 0 Acceptance Criteria

Phase 0 is complete when:

- [x] Target runtime is defined.
- [x] GitHub retrieval behavior is documented.
- [x] Instruction vs knowledge boundary is defined.
- [x] Prompt design principles are documented.
- [x] Modular repository architecture is defined.
- [x] Source-of-truth hierarchy is defined.
- [x] Retrieval strategy is defined.
- [x] Module contract is defined.
- [x] No-fabrication policy is defined.
- [x] Testing contract is defined.
- [x] V1 locked boundary is preserved.
- [x] Official documentation sources are recorded.

---

## 14. Official Documentation

### OpenAI — Connecting GitHub to ChatGPT

https://help.openai.com/en/articles/11145903-connecting-github-to-chatgpt

### OpenAI — Prompt Engineering Best Practices for ChatGPT

https://help.openai.com/en/articles/10032626-prompt-engineering-best-practices-for-chatgpt

### OpenAI — Creating and Editing GPTs

https://help.openai.com/en/articles/8554397-creating-a-gpt

### OpenAI — Workspace Agents

https://help.openai.com/en/articles/20001143/

---

## 15. Phase Boundary

### Phase 0 owns

- platform assumptions;
- documentation findings;
- retrieval constraints;
- source-of-truth policy;
- architecture constraints.

### Phase 0 does not own

- agent role implementation;
- state schema implementation;
- question engine;
- career matching;
- development planning;
- project recommendation;
- portfolio generation;
- opportunity matching;
- runtime system prompt.

Those are implemented in later phases.

---

## 16. Next Phase

**Phase 1 — Agent Architecture**

Goal:

Define the complete modular architecture and dependency graph for the AI Career Discovery & Development Agent without implementing the individual engines yet.
