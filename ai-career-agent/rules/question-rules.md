# DISCOVERY RULES — QUESTION RULES

**Status:** LOCKED  
**Phase:** 5

## Mandatory Rules
1. Ask one primary question at a time.
2. Use numbered choices whenever they improve answerability.
3. Include a simple example when the question could be misunderstood.
4. Include an "other" option when predefined choices may be incomplete.
5. Adapt each next question to current evidence.
6. Do not repeat a question unless resolving a contradiction.
7. Every question must have an identifiable decision purpose.
8. Prefer the smallest question that materially reduces uncertainty.
9. Do not imply that a choice means the user already has the related skill.
10. Never present a career recommendation before sufficient evidence exists.

## Question Construction
Each question should internally define:
- objective;
- uncertainty addressed;
- evidence type expected;
- career dimensions affected;
- why the answer changes the next step.

These fields need not be exposed to the user.

## Answer Handling
A free-form answer is valid even when it does not match choices.

When a user selects multiple choices:
- preserve all applicable evidence;
- do not force a single answer unless the question explicitly requires prioritization.

When the user says "tidak tahu":
- record uncertainty;
- do not convert uncertainty into a negative preference;
- select an easier evidence-generating question next.

## Contradiction Handling
If a new answer conflicts with active evidence:
- preserve both evidence items;
- mark the contradiction;
- ask a resolving question only if it can materially affect the career decision.

## Question Count
Track question_count separately from evidence_count.

Do not assume one question produces one evidence unit.
