# ADR-008: Education Intelligence Platform

## Status

Accepted

## Date

2026-07-29

---

# 1. Context

Homehelp was initially conceived as an AI Learning Companion focused on understanding learners, supporting parents, and providing personalised educational guidance.

As implementation progressed, foundational capabilities emerged:

- Learner Discovery
- Learner Profiles
- Learner Insights
- Conversation Intelligence
- Knowledge Evolution

Architectural review identified that these capabilities represent the foundation of a broader educational intelligence capability.

The AI Learning Companion therefore requires an architectural model that supports future evolution while preserving its original purpose.

---

# 2. Decision

The AI Learning Companion will remain the primary product and architectural centre.

The Education Intelligence Platform is established as the long-term architectural evolution of the Learning Companion.

The Education Intelligence Platform is not a separate product.

It represents the expanding intelligence capabilities that enable the Learning Companion to support learners, families, educators, and institutions.

---

# 3. Architectural Model

The architecture is represented as:


Education Intelligence Platform

└── AI Learning Companion

├── Discovery Intelligence

├── Conversation Intelligence

├── Learner Knowledge Graph

├── Assessment Intelligence

├── Credential Intelligence

├── Curriculum Intelligence

├── Institutional Analytics

├── Accreditation Services

└── Responsible AI Governance

---

# 4. Relationship With Existing Domains

The current bounded contexts remain valid.

Existing domains represent foundational intelligence capabilities:

## Learner Domain

Responsible for:

- learner identity
- learner profile lifecycle
- learner understanding


## Discovery Domain

Responsible for:

- structured discovery journeys
- gathering learner context
- creating initial understanding


## Learner Insight Domain

Responsible for:

- representing discovered knowledge
- capturing meaningful observations
- supporting profile evolution


## Conversation Intelligence Domain

Responsible for:

- extracting educational meaning from conversations
- transforming interactions into structured insights

---

# 5. Future Domain Evolution

The architecture intentionally allows future bounded contexts.

Potential future domains include:

## Assessment Domain

Responsible for:

- assessments
- competency measurement
- evidence of learning


## Credential Domain

Responsible for:

- digital badges
- certificates
- achievement records
- verification


## Curriculum Intelligence Domain

Responsible for:

- curriculum mapping
- personalised pathways
- learning recommendations


## Accreditation Domain

Responsible for:

- institutional recognition
- standards alignment
- accreditation workflows

These domains will only be introduced when justified by validated business and educational requirements.

---

# 6. Relationship With ADR-007

ADR-007 established Learner Knowledge Evolution as a core architectural principle.

ADR-008 extends this principle.

Knowledge evolves through:

Discovery

↓

Learner Insights

↓

Learner Profile

↓

Learning Evidence

↓

Assessment

↓

Credentials

The Education Intelligence Platform provides the architectural foundation for this evolution.

---

# 7. Alignment With Founding Principles

This decision remains aligned with Homehelp's founding principles.

## Learner First

All intelligence capabilities exist to improve learner understanding and support.

## Responsible AI

AI assists understanding but does not replace human educational responsibility.

## Institutional Knowledge Ownership

The institution remains the authority over educational decisions.

## Trust and Transparency

Parents and learners must understand how information contributes to educational support.

---

# 8. Consequences

## Positive Consequences

- Provides a long-term architectural vision.
- Prevents fragmentation of intelligence capabilities.
- Allows future accreditation and credential pathways.
- Preserves the Learning Companion as the user-facing product.

## Negative Consequences

- Requires disciplined domain evolution.
- Requires stronger governance as capabilities expand.
- Future accreditation capabilities will require external partnerships and regulatory alignment.

---

# 9. Implementation Guidance

This ADR does not require immediate implementation of future capabilities.

Current development continues from the existing architecture.

Future capabilities should be introduced through additional ADRs and bounded-context reviews.

---

# Decision Summary

The AI Learning Companion evolves within an Education Intelligence Platform architecture.

The Learning Companion remains the primary product.

The Education Intelligence Platform provides the long-term foundation for learner understanding, assessment, cr