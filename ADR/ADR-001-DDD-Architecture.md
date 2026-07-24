# ADR-001: Domain-Driven Design Architecture

## Status

Accepted

## Date

2026-07-24

---

# 1. Context

Homehelp is being developed as an AI-powered learning institution.

The system is not only a software application. It represents educational knowledge, learner understanding, parent relationships, and responsible artificial intelligence.

Traditional software approaches often place technical structures at the centre of the design.

For Homehelp, the educational domain must remain the centre.

The architecture must allow the institution's knowledge to evolve independently from technology choices.

---

# 2. Decision

We have adopted Domain-Driven Design (DDD) as the foundation of the Homehelp architecture.

The system will be organised around domain concepts rather than technical frameworks.

The primary architectural layers are:

```text
Presentation Layer

Application Layer

Domain Layer

Infrastructure Layer
```

---

# 3. Reasons for the Decision

## 3.1 Educational Knowledge Is Core Value

The most valuable part of Homehelp is not the API, database, or user interface.

The core value is the ability to understand learners.

DDD allows educational concepts to be explicitly modelled.

Examples:

* LearnerProfile
* DiscoverySession
* Conversation Intelligence
* Learning Insights

---

## 3.2 Business Rules Need Protection

Important institutional rules should not be scattered throughout controllers, databases, or external services.

The Domain Layer protects:

* learner rules
* discovery workflows
* educational concepts
* institutional behaviour

---

## 3.3 Supports Long-Term Evolution

The education sector will continue to change.

AI capabilities will evolve.

New learning models will emerge.

DDD allows Homehelp to adapt without rewriting the entire system.

---

# 4. Architectural Consequences

## Positive Consequences

### Clear Business Ownership

The domain clearly represents institutional knowledge.

---

### Easier Testing

Domain behaviour can be tested independently.

---

### Technology Independence

The institution is not locked into specific:

* databases
* AI providers
* frameworks
* infrastructure choices

---

### Better Collaboration

Developers and education specialists can share a common language.

---

# 5. Trade-offs

DDD introduces additional complexity.

Examples:

* more classes
* more explicit modelling
* additional architectural discipline

However, this complexity is intentional because Homehelp is designed as a long-term institutional platform.

---

# 6. Implementation Principles

The implementation follows these rules:

## Domain First

New features begin with domain understanding.

---

## Explicit Models

Important concepts receive dedicated models.

---

## Protected Boundaries

Aggregates control their own state.

---

## Events Communicate Change

Important changes are represented as domain events.

---

# 7. Current Implementation

The following DDD concepts have been implemented:

## Domain Kernel

* Entity
* AggregateRoot
* ValueObject
* UniqueEntityID
* Result
* Either
* Guard

---

## Learner Domain

Implemented:

* LearnerProfile Aggregate
* LearnerName Value Object
* GradeLevel Value Object
* LearnerProfileStatus

---

## Discovery Domain

Implemented:

* DiscoverySession Aggregate
* DiscoverySessionStatus
* DiscoveryStarted Event
* DiscoveryCompleted Event

---

# 8. Future Considerations

Future domains may include:

* Conversation Intelligence
* Learning Recommendations
* Parent Engagement
* Assessment Intelligence
* Institutional Analytics

All future capabilities should preserve the same domain-centred approach.

---

# 9. Conclusion

Domain-Driven Design was selected because Homehelp is fundamentally a knowledge institution.

The architecture exists to preserve and grow educational intelligence.

The system must always keep the learner at the centre.
