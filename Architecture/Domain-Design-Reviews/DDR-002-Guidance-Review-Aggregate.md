# DDR-002 — GuidanceReview Aggregate

## Status

Approved

---

# Purpose

Define the GuidanceReview aggregate responsible for managing the parent lifecycle of educational guidance.

The aggregate records how parents interact with AI-generated educational guidance while preserving the immutability of the original guidance.

---

# Problem Statement

Sprint 04 introduced EducationalGuidance as a historical record of guidance generated from learner intelligence.

However, EducationalGuidance currently has no representation of:

- whether parents viewed the guidance
- whether guidance was acknowledged
- whether parents questioned it
- whether the guidance has been acted upon

Adding mutable state directly to EducationalGuidance would mix historical evidence with user interaction.

---

# Decision

Introduce a new aggregate:

GuidanceReview

EducationalGuidance remains immutable.

GuidanceReview represents the parent interaction lifecycle.

---

# Aggregate Responsibilities

GuidanceReview shall:

- reference EducationalGuidance
- record review state
- record timestamps
- maintain audit history
- publish domain events

---

# Lifecycle

Generated

↓

Viewed

↓

Acknowledged

↓

Completed

Alternative path

Generated

↓

Questioned

---

# Aggregate Root

GuidanceReview

---

# Identity

ReviewId

---

# References

EducationalGuidanceId

ParentId

---

# Domain Invariants

Current enforced invariants:

A GuidanceReview:

- belongs to one EducationalGuidance
- belongs to one parent
- is created with an initial status of Generated
- maintains its own audit timestamps


Future lifecycle invariants:

A GuidanceReview shall:

- not move backwards in lifecycle
- not be completed before acknowledgement
- preserve the history of parent interaction states

# Domain Events

Implemented:

GuidanceReviewCreated


Future lifecycle events:

GuidanceViewed

GuidanceAcknowledged

GuidanceQuestioned

GuidanceCompleted

# Architectural Consequences

EducationalGuidance remains immutable.

Parent interaction becomes independently auditable.

Future analytics become significantly easier.

---


Approved for Sprint 05 implementation.