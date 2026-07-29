# Sprint 2 Architecture Review Addendum

## Document Purpose

This addendum records architectural clarification arising from the Sprint 2 review of the Homehelp AI Learning Companion implementation.

The purpose is not to redefine Sprint 2 scope, but to formally align the existing implementation with the long-term Education Intelligence Platform vision.

---

# 1. Background

Sprint 2 focused on establishing the foundational intelligence capabilities of the AI Learning Companion:

- Learner Discovery
- Learner Profile generation
- Learner Insights
- Conversation Intelligence
- Knowledge evolution mechanisms

During architectural review, it became clear that these capabilities represent foundational components of a broader Education Intelligence Platform.

---

# 2. Strategic Clarification

The AI Learning Companion remains the primary product and architectural boundary.

The Education Intelligence Platform is not a separate product.

It represents the evolution path of the Learning Companion.

The architecture therefore follows:

Education Intelligence Platform
│
└── AI Learning Companion
    │
    ├── Discovery Intelligence
    │
    ├── Conversation Intelligence
    │
    ├── Learner Knowledge Graph
    │
    ├── Assessment Intelligence
    │
    ├── Credential Intelligence
    │
    ├── Curriculum Intelligence
    │
    ├── Institutional Analytics
    │
    ├── Accreditation Services
    │
    └── Responsible AI Governance

---

# 3. Architectural Impact

This clarification does not invalidate existing architecture decisions.

Existing bounded contexts remain valid:

- Learner Profile
- Discovery
- Learner Insight
- Conversation Intelligence
- Parent Relationship

These become foundational domains within the Learning Companion.

---

# 4. Future Domain Evolution

The architecture allows future introduction of additional bounded contexts:

## Assessment Domain

Responsible for:

- assessments
- evaluation models
- competency measurement
- learning evidence


## Credential Domain

Responsible for:

- certificates
- badges
- achievement records
- verification mechanisms


## Curriculum Intelligence Domain

Responsible for:

- curriculum mapping
- learning pathways
- content alignment


These domains are intentionally deferred until business validation requires implementation.

---

# 5. Relationship With ADR-007

ADR-007 established Learner Knowledge Evolution as a core architectural principle.

This addendum extends that principle.

Learner knowledge evolves through:

Discovery
→ Insights
→ Profile Evolution
→ Learning Evidence
→ Assessment
→ Credentials

The Learning Companion therefore becomes an institutional knowledge system.

---

# 6. Founding Principles Alignment

This clarification remains aligned with the founding principles:

## Learner First

The learner remains the centre of the system.

## Responsible AI

AI assists understanding but does not replace institutional responsibility.

## Knowledge Ownership

Educational knowledge remains governed by the institution.

## Trust and Transparency

Families understand how learner information contributes to support decisions.

---

# 7. Sprint 2 Status

Sprint 2 remains considered complete for its original objectives.

The architecture review represents a strategic refinement rather than a scope change.

Implementation continues from the existing codebase.

---

# 8. Next Architectural Steps

Following this clarification:

1. Create ADR-008: Education Intelligence Platform
2. Review existing domains against the expanded model
3. Identify future bounded contexts without premature implementation
4. Continue implementation from the existing roadmap

---

## Decision

The AI Learning Companion will evolve into an Education Intelligence Platform while maintaining the Learning Companion as the primary user-facing product and architectural centre.