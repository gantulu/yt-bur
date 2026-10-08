# EVIDENCE & DECISION AUDIT

**Status:** LOCKED  
**Phase:** 19

## Purpose
Audit whether user evidence is preserved, classified, weighted, traced, and transformed into career decisions without unsupported inference or loss of uncertainty.

## Audit Scope

The audit covers:
- evidence provenance;
- evidence strength;
- evidence-to-competency mapping;
- score vs confidence;
- evidence-to-career mapping;
- Fit vs Readiness vs Potential;
- contradiction handling;
- downstream decision propagation;
- development/project/portfolio/execution evidence integrity;
- feedback-driven reassessment;
- non-fabrication.

## Findings

### E01 — Evidence Provenance
**Result:** PASS.

User-specific claims require evidence IDs and provenance. State preserves source type, statement, source detail, strength, confidence, timestamp, supports, contradicts, and status.

### E02 — Evidence Strength
**Result:** PASS.

The canonical hierarchy is:

Interest → Preference → Self-report → Experience → Concrete example → Project → Demonstrated result.

Weights are evidentiary strength, not direct competency scores.

### E03 — Score vs Confidence
**Result:** PASS.

Competency score represents demonstrated/current capability. Confidence represents certainty in that assessment.

A correction was applied during this audit: competency score 1 now requires evidence of exposure or very limited capability. When there is no meaningful capability evidence, the agent must use unknown/provisional with low confidence rather than inventing a score.

Updated module:
`ai-career-agent/engines/assessment.md`

### E04 — Interest Is Not Skill
**Result:** PASS.

Interest and preference can influence career fit but cannot independently establish competency.

### E05 — Tool Familiarity Is Not Expertise
**Result:** PASS.

Tool usage alone does not establish advanced competency.

### E06 — Project Evidence
**Result:** PASS.

Projects can provide strong evidence, but project type alone is never proof. Actual implementation/result evidence is required for stronger claims.

### E07 — Career Decision Traceability
**Result:** PASS.

Material matching decisions require evidence IDs. Matching uses canonical dimensions and does not allow score alone to determine the winner.

### E08 — Fit / Readiness / Potential
**Result:** PASS.

The three concepts remain separate:
- Fit = match to current evidence.
- Readiness = preparedness to perform now.
- Potential = plausibility of development.

A strong fit with low readiness remains a valid development target.

### E09 — Matching Weight Integrity
**Result:** PASS.

Canonical matching weights remain:
- Competency 45%
- Interest 20%
- Experience 15%
- Activity preference 10%
- Goal 10%

### E10 — Contradictory Evidence
**Result:** PASS.

Contradictory evidence is preserved, not silently deleted. Material contradictions reduce confidence and can trigger a resolving question or reassessment.

### E11 — Evidence Lifecycle
**Result:** PASS.

Evidence follows:

NEW → ACTIVE → SUPPORTS DECISION → SUPERSEDED / CONTRADICTORY → REASSESS

Historical evidence remains available for audit.

### E12 — Development Traceability
**Result:** PASS.

Development gaps derive from competency evidence and the selected career direction. Each major priority has an observable evidence target.

### E13 — Project Decision Integrity
**Result:** PASS.

Project selection is tied to the current development gap and required evidence. Planned results cannot be represented as achieved results.

### E14 — Portfolio Integrity
**Result:** PASS.

Portfolio claims must trace to actual project/evidence records. Planned, implemented, tested, demonstrated, and outcome states remain distinct.

### E15 — Execution Integrity
**Result:** PASS.

Execution positioning and opportunity selection require demonstrated capability, portfolio/experience evidence, and known constraints. Unsupported expertise or opportunity claims are prohibited.

### E16 — Feedback Propagation
**Result:** PASS.

Actual outcomes become new evidence and trigger only materially affected reassessments. Downstream decisions are revalidated after material changes.

### E17 — Non-Fabrication
**Result:** PASS.

The architecture explicitly prohibits invented skills, experience, results, metrics, preferences, constraints, feedback, opportunities, or career history.

## Decision Integrity Chain

The canonical evidence-to-decision chain is:

```
USER INPUT
   ↓
EVIDENCE
   ↓
CLASSIFICATION
   ↓
COMPETENCY ASSESSMENT
   ↓
CAREER MATCHING
   ↓
DEVELOPMENT GAP
   ↓
PROJECT / EVIDENCE TARGET
   ↓
PORTFOLIO PROOF
   ↓
EXECUTION
   ↓
REAL-WORLD FEEDBACK
   ↓
REASSESSMENT
```

No stage is permitted to silently manufacture evidence for the next stage.

## Audit Result

**PASS**

One ambiguity was identified and corrected during the audit: assigning competency score 1 when there is no meaningful evidence. The corrected rule now requires evidence even for the lowest competency score and uses unknown/provisional when evidence is absent.

No remaining blocking evidence or decision-integrity issue was identified.

## Acceptance Criteria

- [x] Evidence provenance verified.
- [x] Evidence strength hierarchy verified.
- [x] Score/confidence separation verified.
- [x] Interest/skill separation verified.
- [x] Tool familiarity/expertise separation verified.
- [x] Career decision traceability verified.
- [x] Fit/Readiness/Potential separation verified.
- [x] Matching weights verified.
- [x] Contradiction handling verified.
- [x] Development evidence chain verified.
- [x] Project evidence integrity verified.
- [x] Portfolio evidence integrity verified.
- [x] Execution evidence integrity verified.
- [x] Feedback propagation verified.
- [x] Non-fabrication verified.
- [x] Identified ambiguity corrected.
- [x] No blocking evidence/decision-integrity issue remains.
