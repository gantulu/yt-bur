# BEHAVIORAL AUDIT

**Status:** LOCKED  
**Phase:** 17

## Purpose
Audit whether the locked instructions, engines, rules, state model, validation, and output contracts produce the intended conversational behavior rather than only having correct file structure.

## Audit Method
The audit uses behavioral scenarios against the canonical contracts. A scenario passes only when the expected behavior is supported by authoritative repository rules.

## Behavioral Tests

### B01 — First Discovery Interaction
**Condition:** No meaningful user evidence exists.  
**Expected:** Enter DISCOVER; ask one primary question; prefer numbered choices; use a simple example when useful; include "other" when appropriate; no career recommendation yet.  
**Result:** PASS.

### B02 — Adaptive Follow-up
**Condition:** User provides a concrete activity or experience.  
**Expected:** Extract and classify evidence, update state, select the next question from the highest-impact uncertainty, and avoid restarting a fixed questionnaire.  
**Result:** PASS.

### B03 — "Tidak Tahu"
**Condition:** User cannot answer.  
**Expected:** Record uncertainty, do not treat it as negative preference, and ask an easier evidence-generating question.  
**Result:** PASS.

### B04 — Self-Reported Skill
**Condition:** User claims advanced ability without demonstrated evidence.  
**Expected:** Preserve it as self-report; do not automatically assign advanced competency; seek stronger evidence.  
**Result:** PASS.

### B05 — Tool Familiarity
**Condition:** User has used a tool but provides no substantial evidence.  
**Expected:** Do not equate familiarity with expertise; keep score and confidence separate.  
**Result:** PASS.

### B06 — Contradictory Evidence
**Condition:** New answer conflicts with earlier evidence.  
**Expected:** Preserve both records, mark contradiction, adjust confidence when appropriate, and resolve only when materially relevant.  
**Result:** PASS.

### B07 — Insufficient Matching Evidence
**Condition:** Evidence cannot distinguish candidate careers.  
**Expected:** Do not force a career; identify the smallest missing evidence and continue or defer.  
**Result:** PASS.

### B08 — Career Recommendation
**Condition:** Evidence is sufficient and stable.  
**Expected:** Compare candidates with canonical weights; select one primary and up to two secondary directions; separate Fit/Readiness/Potential; explain evidence and main gap; provide one next action.  
**Result:** PASS.

### B09 — High Fit / Low Readiness
**Condition:** Career fit is strong but current capability is underdeveloped.  
**Expected:** Preserve the career as a valid target and route the gap into development.  
**Result:** PASS.

### B10 — Development
**Condition:** Career is resolved and a meaningful competency gap exists.  
**Expected:** Define target capability first; prioritize by career impact, interest alignment, project relevance, and evidence value; use NOW/NEXT/LATER; attach observable evidence targets.  
**Result:** PASS.

### B11 — Project Selection
**Condition:** Development gap requires practical evidence.  
**Expected:** Select the smallest suitable project; define problem, goal, AI role when material, workflow, scope, success condition, and evidence target; never present planned results as achieved.  
**Result:** PASS.

### B12 — Portfolio Without Results
**Condition:** Project is planned or incomplete.  
**Expected:** Do not fabricate results; mark missing/in-progress evidence; distinguish planned, implemented, tested, demonstrated, and outcome states.  
**Result:** PASS.

### B13 — Real-World Feedback
**Condition:** User reports an actual project, client, interview, or market outcome.  
**Expected:** Separate observation from interpretation; convert the event into evidence; reassess only affected engines; revalidate downstream decisions; produce one next action.  
**Result:** PASS.

### B14 — User Correction
**Condition:** User says an earlier assumption is wrong.  
**Expected:** Replace the unsupported assumption and reassess affected conclusions without defending it.  
**Result:** PASS.

### B15 — Missing Dependency
**Condition:** Required repository module cannot be retrieved.  
**Expected:** Do not invent contents; verify path once; check retrieval map; if no replacement exists, identify the missing dependency and block the consequential decision.  
**Result:** PASS.

### B16 — AI-Centered Career Integrity
**Condition:** Candidate career uses AI only as a minor convenience.  
**Expected:** Do not label it AI-centered merely because an AI tool is used; AI must be materially relevant to the direction.  
**Result:** PASS.

### B17 — One Question at a Time
**Condition:** Discovery remains active.  
**Expected:** One primary question per turn; choices may be multiple, but unrelated questions are not batched.  
**Result:** PASS.

### B18 — End-to-End Stage Integrity
**Condition:** Evidence progresses through the full workflow.  
**Expected:** DISCOVER → ASSESS → MATCH → DEVELOP → BUILD → PROVE → POSITION → EXECUTE → FEEDBACK → REASSESS; each stage retrieves minimum dependencies, applies engine and rules, validates, and preserves earlier decisions unless new evidence justifies reassessment.  
**Result:** PASS.

## Findings

### Confirmed Strengths
1. Discovery is adaptive rather than a fixed questionnaire.
2. Evidence quality is explicitly modeled.
3. Self-report is not treated as demonstrated mastery.
4. Career matching is separated from readiness.
5. Development is evidence-oriented.
6. Projects are sized to produce required evidence.
7. Portfolio claims are constrained by actual evidence.
8. Feedback closes the loop through scoped reassessment.
9. Missing dependencies fail safely instead of being fabricated.
10. AI-centered recommendations require AI to be materially relevant.

### Non-Blocking Notes
- Phase 16 verified repository retrieval; Phase 17 verifies behavioral contracts at the specification level.
- A live multi-turn ChatGPT client session cannot be deterministically executed by the repository itself, so client-surface behavior remains outside this repository audit.

## Final Audit Status
**PASS**

No blocking behavioral contradiction was identified across the audited canonical modules.

## Acceptance Criteria
- [x] Discovery behavior audited.
- [x] Adaptive questioning audited.
- [x] Evidence handling audited.
- [x] Contradiction handling audited.
- [x] Matching behavior audited.
- [x] Development behavior audited.
- [x] Project behavior audited.
- [x] Portfolio evidence integrity audited.
- [x] Feedback/reassessment audited.
- [x] Missing dependency behavior audited.
- [x] AI-centered career integrity audited.
- [x] End-to-end stage integrity audited.
- [x] No blocking behavioral contradiction identified.
