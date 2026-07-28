# ADR-007: Learner Knowledge Evolution Model

## Status

Accepted

## Date

2026-07-28

## Context

Homehelp is designed as an AI Learning Companion whose primary capability is developing a deep understanding of each learner.

Traditional educational systems often treat learner information as static data:

* name
* age
* grade level
* academic results
* preferences

However, meaningful educational support requires an evolving understanding of the learner.

A learner's:

* strengths
* challenges
* motivations
* learning preferences
* goals
* behaviours
* interests

change over time as new information becomes available.

Homehelp therefore requires an architectural approach where learner knowledge can accumulate, evolve, and improve without losing historical understanding.

The system must support knowledge emerging from:

* parent discovery conversations
* learner conversations
* observations
* AI-assisted insight extraction
* educational interactions
* future assessment data

The architecture must ensure that learner understanding is treated as institutional knowledge rather than temporary application data.

---

# Decision

Homehelp will model learner understanding as an evolving knowledge model centred around the LearnerProfile aggregate.

The LearnerProfile represents the institution's current trusted understanding of a learner.

It will evolve through controlled domain processes rather than direct data modification.

The lifecycle is:

```
Discovery Session
        |
        |
        v
Structured Learner Information
        |
        |
        v
Learner Insights
        |
        |
        v
LearnerProfile Evolution
        |
        |
        v
Improved Learner Understanding
```

---

# LearnerProfile as Living Knowledge

The LearnerProfile is not considered a simple database record.

It represents accumulated institutional knowledge about a learner.

The profile may evolve as new understanding emerges.

Examples:

Initial understanding:

```
Learner enjoys practical activities.
```

Later understanding:

```
Learner demonstrates stronger engagement when lessons include problem-solving challenges.
```

The second understanding does not replace the first. It enriches institutional knowledge.

---

# Responsibilities

## DiscoverySession

DiscoverySession is responsible for discovering information.

It manages:

* discovery workflow
* questions
* responses
* completion state

Discovery answers:

"What do we currently know about the learner?"

---

## LearnerInsight

LearnerInsight represents extracted understanding.

Examples:

* learner strengths
* possible challenges
* learning patterns
* motivation indicators

Insights are potential knowledge contributions.

They are not automatically considered final truth.

---

## LearnerProfile

LearnerProfile is responsible for maintaining trusted learner understanding.

It controls:

* learner identity
* profile lifecycle
* accepted learner knowledge
* profile evolution rules

External systems must not directly modify learner knowledge.

---

# AI Relationship

AI systems assist knowledge discovery but do not own learner truth.

The flow is:

```
Conversation
      |
      v
AI Extraction
      |
      v
Learner Insight
      |
      v
Domain Validation
      |
      v
LearnerProfile Update
```

AI may suggest:

* possible strengths
* learning preferences
* patterns

The domain remains responsible for deciding what becomes institutional knowledge.

---

# Domain Principles

## Knowledge Must Have Meaning

Learner information must represent meaningful educational understanding.

The system should avoid becoming a collection of disconnected attributes.

---

## Knowledge Must Evolve Safely

Changes to learner understanding should happen through defined domain behaviours.

This protects against:

* accidental overwrites
* inconsistent learner information
* fragmented understanding

---

## Knowledge Should Be Traceable

Future versions of the system should support understanding:

* when knowledge was added
* why it was added
* what source contributed it
* whether it was confirmed

---

# Consequences

## Positive Consequences

The architecture supports:

* personalised learning experiences
* continuous learner understanding
* explainable AI assistance
* responsible educational decision making
* long-term institutional knowledge retention

The system becomes capable of learning about learners over time.

---

## Negative Consequences

This approach introduces additional complexity:

* learner knowledge requires governance
* updates require domain rules
* historical understanding may need tracking
* more sophisticated data modelling will eventually be required

This complexity is accepted because learner understanding is the core value proposition of Homehelp.

---

# Future Evolution

The Learner Knowledge Evolution model may eventually include:

* learner knowledge history
* confidence levels
* evidence sources
* parent confirmations
* learner self-reflection
* educator observations
* knowledge versioning
* knowledge decay or reassessment

These capabilities will be introduced when required by product maturity.

---

# Relationship With Existing ADRs

This ADR extends:

* ADR-001: DDD Architecture
* ADR-002: Separate AI Service
* ADR-003: LearnerProfile Aggregate
* ADR-004: Discovery-Driven Learner Understanding
* ADR-005: Conversation Intelligence

Together these decisions establish Homehelp as a knowledge institution rather than a simple application.

---

# Summary

Homehelp treats learner understanding as a continuously evolving institutional asset.

The LearnerProfile is the trusted representation of that understanding.

Discovery discovers knowledge.

AI assists interpretation.

Insights contribute possibilities.

The domain governs what becomes lasting learner knowledge.
