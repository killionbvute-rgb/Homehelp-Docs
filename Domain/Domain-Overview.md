# Homehelp Domain Overview

## 1. Introduction

The Homehelp domain represents the educational knowledge and business rules that define how the institution understands and supports learners.

The domain is the heart of the system.

Technical frameworks, databases, APIs, and artificial intelligence services exist to support the domain — not replace it.

The central domain question is:

> How do we understand a learner deeply enough to provide meaningful support?

---

# 2. Domain-Driven Design Approach

Homehelp follows Domain-Driven Design (DDD) principles.

DDD ensures that software models reflect real institutional concepts.

The architecture separates:

* Domain knowledge
* Application workflows
* Infrastructure concerns
* External services

This allows the institution's educational philosophy to remain independent from technology choices.

---

# 3. Domain Structure

The domain is organised around important educational concepts.

Current bounded areas include:

```text
Domain

├── Learner Management
│
├── Discovery
│
├── Conversation Intelligence
│
└── Future Learning Intelligence
```

---

# 4. Domain Kernel

The Domain Kernel provides reusable building blocks.

Current components:

* Entity
* AggregateRoot
* ValueObject
* UniqueEntityID
* Domain Events
* Result
* Either
* Guard

These components provide consistency across all domain models.

---

# 5. Aggregates

Aggregates represent important institutional concepts with controlled boundaries.

Each aggregate:

* protects its own rules
* controls changes to its state
* exposes meaningful behaviours
* communicates through domain events

---

# 6. LearnerProfile Aggregate

## Purpose

LearnerProfile represents the institution's understanding of an individual learner.

It is a living profile that evolves as more knowledge is discovered.

---

## Information Captured

The learner profile includes:

* learner identity
* learner name
* age
* grade level
* strengths
* challenges
* learning goals
* learning preferences

---

## Lifecycle

```text
Draft
 |
In Discovery
 |
Confirmed
```

A learner profile begins with limited knowledge and becomes richer through interaction.

---

# 7. DiscoverySession Aggregate

## Purpose

DiscoverySession represents the structured process of understanding a learner.

Before personalised support is provided, the institution first discovers:

* who the learner is
* how they learn
* what challenges they experience
* what goals they have

---

## Lifecycle

```text
Draft
 |
In Progress
 |
Completed
```

---

## Domain Events

Discovery generates meaningful events.

Examples:

```text
DiscoveryStarted
DiscoveryCompleted
```

Events allow other parts of the system to react without creating tight dependencies.

---

# 8. Value Objects

Value Objects represent concepts defined by their meaning rather than identity.

Examples:

## LearnerName

Represents a valid learner name.

Rules may include:

* required value
* formatting validation
* consistency

---

## GradeLevel

Represents the learner's educational level.

It protects the system from invalid grade information.

---

# 9. Domain Events

Domain events represent important changes that occurred.

Examples:

```text
LearnerProfileCreated

DiscoveryStarted

DiscoveryCompleted
```

Events provide a foundation for:

* notifications
* AI processing
* analytics
* integrations
* future workflows

---

# 10. Conversation Intelligence Domain

Future development will introduce Conversation Intelligence.

Its purpose is to transform conversations into structured learner understanding.

Possible concepts:

```text
Conversation

ConversationFact

Insight

LearningPattern

ParentObservation
```

Conversation Intelligence will connect naturally with Discovery and LearnerProfile.

---

# 11. Domain Rules

The domain follows these principles:

## The learner comes first

Every model must represent learner value.

---

## Knowledge is built progressively

Understanding develops over time.

---

## AI insights require context

Information without context can create poor decisions.

---

## Domain rules must remain independent

Educational knowledge must not depend on technical infrastructure.

---

# 12. Long-Term Domain Vision

The Homehelp domain will evolve into a complete learner intelligence model.

Future capabilities include:

* personalised learning journeys
* adaptive support
* educator insights
* parent intelligence
* institutional learning analytics

The domain represents the educational intelligence of Homehelp.

It is the foundation upon which the entire institution is built.
