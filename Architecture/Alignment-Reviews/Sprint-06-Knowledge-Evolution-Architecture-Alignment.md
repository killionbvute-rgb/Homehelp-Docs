# ADR-013 — Knowledge Evolution Intelligence Model

## Status

Accepted

## Date

1 August 2026

## Context

Homehelp's initial Learner Knowledge Evolution capability allowed the system to record changes in learner understanding over time.

However, the initial model represented evolution primarily as historical records:
Learner Insight
|
v
Knowledge Evolution Record

As Homehelp evolves into an explainable educational intelligence platform, learner evolution must become more meaningful.

The system must understand:

- What changed about the learner
- Why the change occurred
- How confident the system is about the change
- What evidence supports the change
- How learner understanding develops over time

Knowledge Evolution therefore becomes a foundation for responsible learner intelligence.

---

# Decision

Homehelp will implement Knowledge Evolution as an explainable intelligence history model within the Learner Intelligence bounded context.

Knowledge Evolution will represent:

- learner changes
- evolution reasoning
- confidence levels
- supporting evidence references
- historical context

The model will remain domain-owned and independent from AI execution.

AI components may suggest interpretations, but the domain remains responsible for preserving learner intelligence history.

---

# Architectural Principle

## AI Suggests

## Domain Preserves Truth

AI responsibilities:

- Analyse learner information
- Identify possible patterns
- Generate interpretation suggestions
- Assist future intelligence workflows

Domain responsibilities:

- Store learner evolution
- Preserve historical changes
- Maintain evidence references
- Maintain confidence information
- Support auditability

---

# Domain Alignment

Bounded Context:

Learner Intelligence

Knowledge Evolution integrates with:

Conversation Intelligence
|
v
Learner Insights
|
v
Knowledge Evolution
|
v
Personalised Guidance

---

# Domain Model Changes

The Knowledge Evolution aggregate is extended to include:

## Confidence Tracking

Purpose:

Represent certainty associated with a learner intelligence change.

Example:
Learner preference changed:
"Prefers visual learning"

Confidence:

High

Confidence originates from learner insights and is preserved with the evolution record.

---

## Evidence References

Purpose:

Maintain traceability between learner changes and supporting information.

Example:


Confidence originates from learner insights and is preserved with the evolution record.

---

## Evidence References

Purpose:

Maintain traceability between learner changes and supporting information.

Example:

Conversation Evidence
|
v
Learner Insight
|
v
Knowledge Evolution

Evidence references allow future:

- reasoning traces
- audit reviews
- explainable AI workflows

---

## Contextual Evolution History

The system will support retrieval of learner evolution history with context.

Example:

Instead of:

Preference changed

Homehelp can understand:

Preference changed

Reason:
Repeated learner conversations indicate visual explanations improve engagement.

Confidence:
High

Evidence:
Conversation observations
Parent feedback
Learning interactions

---

# Aggregate Responsibilities

KnowledgeEvolution aggregate is responsible for:

- Recording meaningful learner changes
- Maintaining evolution metadata
- Preserving historical intelligence
- Publishing evolution events

It is not responsible for:

- Generating AI conclusions
- Analysing raw conversations
- Making educational decisions

---

# Domain Events

The following domain event remains:

KnowledgeEvolutionRecorded

Purpose:

Records that learner understanding has evolved.

Future events may include:
KnowledgeEvolutionConfidenceChanged

KnowledgePatternDetected

KnowledgeEvolutionReviewed

---

# Application Layer Impact

The following workflows support the capability:

## RecordKnowledgeEvolution

Purpose:

Create a learner evolution record.

Supports:

- learner change
- confidence
- evidence references
- reasoning context


---

## GetLearnerEvolutionHistoryWithContext

Purpose:

Retrieve learner evolution history enriched with intelligence context.

Provides:

- historical changes
- confidence information
- source information
- supporting context

---

# Repository Impact

Updated repository responsibilities:

IKnowledgeEvolutionRepository

Supports:

- storing evolution history
- retrieving learner evolution records
- supporting contextual intelligence workflows

---

# Responsible AI Considerations

The Knowledge Evolution model supports:

## Explainability

Every learner change should answer:

"What changed and why?"

---

## Transparency

Parents and educators should understand how learner understanding develops.

---

## Auditability

Historical learner intelligence should remain reviewable.

---

## Human Oversight

Parent and educator observations remain valuable sources of intelligence.

---

# Alternatives Considered

## Alternative 1 — Store Evolution Only as Events

Rejected.

Reason:

Events alone do not provide sufficient contextual intelligence retrieval.

---

## Alternative 2 — Let AI Own Learner Evolution

Rejected.

Reason:

Creates opaque intelligence ownership and reduces trust.

---

## Alternative 3 — Store Evolution Inside Learner Profile

Rejected.

Reason:

Learner Profile represents current learner identity, not historical intelligence development.

---

# Consequences

## Positive

- Stronger learner intelligence foundation
- Improved explainability
- Better future AI reasoning capability
- Evidence-backed educational guidance
- Clear separation between AI and domain responsibilities

---

## Negative

- Increased domain complexity
- Additional metadata management
- Requires disciplined evidence handling

---

# Traceability

This ADR supports:

Sprint Blueprint:

Sprint-06-Learner-Knowledge-Evolution.md

Domain Design Review:

Knowledge-Evolution-Domain-Design.md

Implementation:

KnowledgeEvolution Aggregate

RecordKnowledgeEvolution

GetLearnerEvolutionHistoryWithContext

Validation:

46 test files passing
63 tests passing
pnpm -r build successful

---

# Outcome

Knowledge Evolution has evolved from:

> "Homehelp records learner changes"

into:

> "Homehelp understands how learner understanding evolves over time."

This ADR establishes the foundation for future:

- learner development trends
- intelligence pattern recognition
- evidence-backed reasoning
- personalised guidance evolution
