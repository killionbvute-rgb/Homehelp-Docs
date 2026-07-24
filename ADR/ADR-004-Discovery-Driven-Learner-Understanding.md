# ADR-004: Discovery-Driven Learner Understanding

## Status

Accepted

## Date

2026-07-24

---

# 1. Context

Traditional educational systems often begin by assigning learning content, assessments, or recommendations before deeply understanding the learner.

Homehelp takes a different approach.

The institution believes that effective support requires understanding the learner first.

Before recommending learning paths, interventions, or support strategies, the system must discover:

* who the learner is
* how the learner thinks
* what motivates the learner
* what challenges exist
* what goals the learner and family have

Discovery is therefore a foundational institutional capability.

---

# 2. Decision

Homehelp will adopt a discovery-first approach.

Every personalised learning journey begins with a structured Discovery Session.

The Discovery Session becomes the primary mechanism for gathering meaningful learner understanding before creating recommendations or interventions.

---

# 3. Reasons for the Decision

## 3.1 Understanding Before Action

Recommendations without context can be inaccurate.

Two learners may experience the same challenge but require different support.

Example:

A learner struggling with mathematics may need:

* additional practice
* a different explanation style
* confidence building
* a different learning approach

Understanding must come before action.

---

## 3.2 Learners Are Complex

A learner cannot be represented by:

* age
* grade
* marks
* test results alone

A complete understanding includes:

* interests
* personality
* learning preferences
* environment
* aspirations
* challenges

---

## 3.3 Builds Trust With Families

The discovery process creates a relationship with parents.

Parents experience that Homehelp is interested in understanding their child rather than immediately prescribing solutions.

---

# 4. DiscoverySession Aggregate

The Discovery Session is modelled as a domain aggregate.

Its responsibility is to manage the discovery journey.

Lifecycle:

```text
Draft

  |

In Progress

  |

Completed
```

---

# 5. Discovery Responsibilities

The Discovery Session manages:

## Conversation Flow

Guiding meaningful interactions.

---

## Information Capture

Collecting relevant learner information.

---

## Completion State

Determining when sufficient discovery has occurred.

---

## Domain Events

Communicating important milestones.

Examples:

```text
DiscoveryStarted

DiscoveryCompleted
```

---

# 6. Relationship With LearnerProfile

Discovery and LearnerProfile have separate responsibilities.

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

Discovery discovers knowledge.

LearnerProfile preserves knowledge.

---

# 7. Relationship With AI

AI assists the discovery process but does not replace the domain.

The flow:

```text
Parent Conversation

        |

        v

AI Conversation Understanding

        |

        v

Structured Discovery Information

        |

        v

Learner Profile Generation
```

The AI helps interpret conversations.

The institution owns the resulting learner understanding.

---

# 8. Architectural Consequences

## Positive Consequences

### Higher Quality Personalisation

Support is based on understanding rather than assumptions.

---

### Stronger Parent Relationships

Families participate in the learner journey.

---

### Better AI Context

AI systems receive meaningful context before generating insights.

---

## Trade-offs

Discovery requires:

* thoughtful conversations
* additional processing
* patience before recommendations

This is accepted because quality understanding creates better long-term outcomes.

---

# 9. Future Evolution

Discovery may expand to include:

* learner self-reflection
* educator observations
* assessment insights
* behavioural patterns
* ongoing conversations

Discovery becomes a continuous institutional capability.

---

# 10. Conclusion

Homehelp believes that the future of education begins with understanding.

The Discovery-First approach ensures that every learner receives support based on who they are, not assumptions about who they should be.

> Understand first. Support better.
