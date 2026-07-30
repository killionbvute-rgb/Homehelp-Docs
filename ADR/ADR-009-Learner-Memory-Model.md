# ADR-009: Learner Memory Model

## Status

Accepted

## Date

2026-07-30

---

# 1. Context

Homehelp is designed as an AI Learning Companion that develops a continuously improving understanding of each learner.

The system currently supports:

- Learner Profiles
- Discovery Sessions
- Conversation Intelligence
- Learner Insights
- Knowledge Evolution

These capabilities allow Homehelp to understand learners and record how that understanding changes.

However, an AI companion requires more than current state and historical changes. It requires the ability to retain meaningful knowledge about a learner over time.

A learner's educational journey contains information that remains valuable beyond a single conversation:

- learning preferences
- recurring behaviours
- demonstrated strengths
- persistent challenges
- interests
- important educational experiences
- parent-provided context

Without a dedicated memory model, valuable understanding may become fragmented across profiles, conversations, and insights.

---

# 2. Decision

Homehelp will introduce a Learner Memory Model as a dedicated domain capability.

Learner Memory represents durable knowledge retained about a learner that can improve future interactions and educational support.

Learner Memory is separate from:

- Learner Profile, which represents current learner state
- Learner Insights, which represent discovered observations
- Knowledge Evolution, which represents changes in understanding

Learner Memory represents knowledge that has sufficient importance and confidence to influence future AI interactions.

---

# 3. Architectural Relationship

The learner understanding lifecycle becomes:

Conversation

↓

Conversation Intelligence

↓

Learner Insight

↓

Knowledge Evolution

↓

Learner Memory

↓

Future AI Personalisation


---

# 4. Domain Principles

Learner Memory must:

## Be Learner-Centric

All memories belong to a specific learner and exist to improve learner support.

## Be Explainable

The system must understand why a memory exists and what evidence created it.

## Be Traceable

Important memories should maintain relationships with their originating insights or conversations.

## Be Confidence-Aware

The system must distinguish between uncertain observations and reliable knowledge.

## Support Responsible AI

Memory creation must respect privacy, transparency, and responsible AI principles.

---

# 5. Consequences

## Positive Consequences

- Enables long-term AI companion behaviour
- Supports personalised educational guidance
- Preserves valuable learner understanding
- Allows future AI services to reason from accumulated knowledge

## Trade-offs

- Introduces additional domain complexity
- Requires memory lifecycle management
- Requires careful governance around retention and usage

---

# 6. Implementation Direction

Sprint 04 will introduce:

- LearnerMemory aggregate
- Memory classification
- Memory importance model
- Memory confidence model
- Memory creation events
- Repository abstraction
- Application workflows
- Automated tests

---

# 7. Alternatives Considered

## Store Memory Inside Learner Profile

Rejected because:

- profile becomes overloaded
- historical knowledge becomes difficult to manage
- current state and historical understanding become mixed

## Store Memory Only Within AI Infrastructure

Rejected because:

- domain ownership is lost
- auditability is reduced
- business rules become dependent on external AI services