# ADR-011 — Parent Trust and Human Feedback Model

## Status

Accepted

## Date

30 July 2026

---

# Context

Homehelp has evolved from collecting learner information into generating personalised educational guidance.

Sprint 04 introduced Learner Intelligence, enabling the system to transform:

- Learner Profiles
- Learner Insights
- Knowledge Evolution

into Educational Guidance.

Sprint 05 introduces parent interaction with this guidance.

The architecture requires a clear model for:

- Parent feedback
- Guidance review
- Explainability
- Human oversight

---

# Decision

Parent interactions with educational guidance will be modelled as explicit domain concepts within the Learner Intelligence bounded context.

The system will introduce:

- GuidanceReview
- ParentGuidanceFeedback
- GuidanceExplanation

---

# Rationale

Parent feedback represents additional evidence about the learner.

It should not directly mutate learner intelligence.

Instead:


Parent Observation

    ↓

ParentGuidanceFeedback

    ↓

Evidence Review

    ↓

Knowledge Evolution

    ↓

Updated Learner Understanding


This preserves traceability and prevents unsupported assumptions.

---

# Architectural Boundaries

## AI Layer

Responsible for:

- Generating explanations
- Identifying patterns
- Suggesting interpretations

## Domain Layer

Responsible for:

- Guidance lifecycle
- Feedback records
- Evidence history
- Trust state

AI remains replaceable.

---

# Consequences

## Positive

- Improved transparency
- Stronger parent trust
- Auditable intelligence evolution
- Human oversight maintained

## Negative

- Additional domain complexity
- Additional storage requirements
- More workflow states

---

# Responsible AI Alignment

This decision reinforces:

> AI assists understanding; humans provide context and judgement.

Parent feedback becomes part of the learner understanding journey without replacing verified knowledge.

---

# Related Decisions

- ADR-007 Learner Knowledge Evolution Model
- ADR-008 Education Intelligence Platform
- ADR-010 Learner Intelligence and Guidance

---

# Implementation Impact

Implementation has commenced.

Implemented:

- GuidanceReview aggregate foundation
- GuidanceReview lifecycle states
- GuidanceReviewCreated domain event
- ParentGuidanceFeedback aggregate
- ParentGuidanceFeedbackRecorded domain event
- GuidanceExplanation model foundation
- Parent feedback recording workflow

Application capabilities implemented:

- RecordParentGuidanceFeedback

Validation evidence:

- Domain build successful
- Application build successful
- 39 application test files passing
- 54 application tests passing

Pending implementation:

- GuidanceReview creation workflow
- Parent guidance review interaction
- Guidance explanation generation workflow
- Feedback-driven Knowledge Evolution integration

Implementation principle:

Parent feedback is captured as additional evidence and does not directly mutate learner intelligence. All changes continue through controlled knowledge evolution processes.