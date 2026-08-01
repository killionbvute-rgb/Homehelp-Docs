# ADR-013 — Knowledge Evolution Intelligence Model

## Status

Accepted

## Date

2026-08-01

## Context

The initial KnowledgeEvolution implementation provided a mechanism for recording changes in learner understanding.

As Homehelp evolves from a learner profile system into an AI Learning Companion, historical recording alone is insufficient.

Future AI guidance requires understanding not only what changed, but:

- why the change occurred
- what evidence supported the change
- how confidence in the understanding evolved over time

Without this capability, AI recommendations risk becoming disconnected observations rather than explainable learner intelligence.

---

## Decision

KnowledgeEvolution will be treated as a longitudinal learner intelligence capability.

The model will evolve from:

Observation
↓
Recorded Change

into:

Observation
↓
Learner Insight
↓
Knowledge Evolution
↓
Confidence & Evidence Context
↓
Future Guidance Intelligence

KnowledgeEvolution remains responsible for representing meaningful changes in learner understanding while preserving explainability and traceability.

---

## Architectural Principles

The implementation must preserve:

- bounded context integrity
- domain ownership of learner knowledge changes
- event traceability
- explainable AI foundations
- evidence-based reasoning

---

## Consequences

### Positive

- Enables personalised future AI guidance.
- Preserves historical learner understanding.
- Supports trend analysis and longitudinal intelligence.
- Improves parent trust through explainability.

### Trade-offs

- Domain complexity increases.
- Evolution validation rules become more important.
- Additional modelling is required for confidence and evidence.

---

## Governance Impact

Future learner intelligence capabilities must trace:

Observation

↓

Learner Insight

↓

Knowledge Evolution

↓

Guidance Decision

↓

Explanation

All future implementation changes must maintain alignment with:

- Product Execution Roadmap v2
- Traceability Matrix
- Responsible AI principles