# ADR-003: LearnerProfile as an Aggregate Root

## Status

Accepted

## Date

2026-07-24

---

# 1. Context

Homehelp exists to understand and support learners through personalised educational experiences.

The learner is not simply a collection of data fields.

A learner profile represents accumulated institutional knowledge about:

* identity
* abilities
* preferences
* challenges
* goals
* learning journey

As the system evolves, learner understanding will grow through:

* discovery conversations
* parent observations
* learner interactions
* AI-generated insights
* educator feedback

The architecture requires a model that protects and manages this evolving knowledge.

---

# 2. Decision

The LearnerProfile entity is implemented as an Aggregate Root within the Homehelp domain.

The aggregate owns the learner profile lifecycle and controls changes to learner information.

External components must interact with LearnerProfile through its defined behaviours rather than directly modifying internal state.

---

# 3. Reasons for the Decision

## 3.1 Learner Knowledge Has Meaningful Rules

Learner information is not arbitrary data.

Examples:

* A learner profile must have a valid identity.
* Learning preferences must be meaningful.
* Profile status must follow a defined lifecycle.
* Changes should represent real educational understanding.

These rules belong inside the domain.

---

## 3.2 Protecting Consistency

The aggregate boundary ensures learner information remains consistent.

Without an aggregate boundary:

* different services could update learner data incorrectly
* business rules could become duplicated
* learner understanding could become fragmented

---

## 3.3 Supporting Continuous Growth

A learner profile is expected to evolve.

The lifecycle:

```text
Draft
 |
In Discovery
 |
Confirmed
```

represents increasing institutional confidence in learner understanding.

---

# 4. Aggregate Responsibilities

LearnerProfile is responsible for:

## Identity Management

Maintaining the learner's identity.

---

## Profile Evolution

Managing changes to learner knowledge.

---

## State Protection

Ensuring profile state remains valid.

---

## Domain Communication

Publishing meaningful changes through domain events.

---

# 5. LearnerProfile Structure

Current model:

```text
LearnerProfile

├── LearnerId
├── LearnerName
├── Age
├── GradeLevel
├── Strengths
├── Challenges
├── LearningGoals
├── LearningPreferences
├── Status
├── CreatedAt
└── UpdatedAt
```

---

# 6. Relationship With DiscoverySession

DiscoverySession and LearnerProfile have different responsibilities.

## DiscoverySession

Responsible for:

* discovering information
* managing discovery workflow
* capturing conversations

---

## LearnerProfile

Responsible for:

* representing learner understanding
* maintaining learner knowledge
* supporting future learning decisions

The relationship:

```text
Discovery Session

        |
        |
        v

Learner Understanding

        |
        |
        v

Learner Profile
```

---

# 7. Relationship With AI

AI does not directly control the LearnerProfile.

The flow is:

```text
Conversation

      |
      v

AI Insight Extraction

      |
      v

Application Layer

      |
      v

LearnerProfile Update
```

The domain remains the authority over learner information.

---

# 8. Architectural Consequences

## Positive Consequences

### Strong Domain Protection

Learner knowledge remains governed by business rules.

---

### Future Flexibility

New intelligence sources can contribute safely.

Examples:

* AI insights
* educator feedback
* assessments
* parent observations

---

### Better Auditability

Changes to learner understanding can be tracked.

---

# 9. Trade-offs

The aggregate introduces additional modelling effort.

Developers must understand:

* aggregate boundaries
* domain behaviours
* lifecycle rules

This is accepted because learner intelligence is a core institutional asset.

---

# 10. Future Evolution

The LearnerProfile aggregate may eventually include:

* learning history
* capability development
* behavioural patterns
* achievement milestones
* personalised learning strategies

The aggregate will remain the trusted representation of learner understanding.

---

# 11. Conclusion

LearnerProfile is modelled as an Aggregate Root because Homehelp is fundamentally about understanding learners.

The architecture protects learner knowledge by ensuring that changes happen intentionally, consistently, and responsibly.
