# ADR-005: Conversation Intelligence as a Domain Capability

## Status

Accepted

## Date

2026-07-24

---

# 1. Context

Homehelp's primary goal is to understand learners deeply.

A significant amount of learner understanding will emerge through natural conversations with:

* parents
* learners
* educators
* mentors

Traditional systems often store conversations as unstructured messages.

Homehelp requires a way to transform conversations into meaningful educational knowledge.

A conversation should not only be stored.

It should contribute to understanding the learner.

---

# 2. Decision

Conversation Intelligence will be treated as a strategic domain capability.

The system will transform conversational interactions into structured educational insights while maintaining clear separation between:

* AI interpretation
* domain knowledge
* institutional decisions

---

# 3. Reasons for the Decision

## 3.1 Conversations Contain Valuable Knowledge

Parents naturally communicate important information about learners.

Examples:

> "My daughter loves solving puzzles but gets frustrated when tasks feel repetitive."

Possible insights:

```text
Strength:
- Problem solving ability

Preference:
- Challenging activities

Observation:
- May require variety in learning activities
```

The value is not only the conversation itself, but the knowledge extracted from it.

---

## 3.2 Structured Understanding Enables Personalisation

Personalised learning requires structured knowledge.

Conversation Intelligence helps identify:

* learner strengths
* challenges
* interests
* goals
* learning preferences
* observations

This knowledge contributes to the learner model.

---

# 4. Conversation Intelligence Model

Future domain concepts may include:

```text
Conversation

ConversationFact

FactType

LearnerInsight

LearningPattern

ParentObservation
```

---

# 5. Architectural Boundary

Conversation Intelligence follows this flow:

```text
Conversation

      |

      v

AI Processing

      |

      v

Structured Facts

      |

      v

Domain Validation

      |

      v

Learner Knowledge
```

AI identifies possible meaning.

The domain decides what becomes institutional knowledge.

---

# 6. Relationship With DiscoverySession

DiscoverySession uses Conversation Intelligence during learner discovery.

Relationship:

```text
Discovery Session

        |

        v

Conversation Intelligence

        |

        v

Learner Facts

        |

        v

Learner Profile
```

Discovery provides context.

Conversation Intelligence provides understanding.

---

# 7. Relationship With LearnerProfile

Conversation Intelligence does not directly modify LearnerProfile.

The application layer coordinates the process:

```text
Conversation Insight

        |

        v

Application Service

        |

        v

LearnerProfile Update
```

This protects domain integrity.

---

# 8. AI Responsibilities

AI is responsible for:

* understanding language
* identifying possible facts
* detecting patterns
* suggesting insights

AI is not responsible for:

* defining educational truth
* making final learner decisions
* replacing human judgement

---

# 9. Architectural Consequences

## Positive Consequences

### Richer Learner Understanding

The institution can learn continuously from interactions.

---

### Better Personalisation

Support becomes based on accumulated knowledge.

---

### Future Intelligence Capability

Creates a foundation for:

* adaptive learning
* predictive insights
* personalised recommendations

---

## Trade-offs

Conversation Intelligence introduces complexity:

* information extraction
* validation processes
* privacy considerations
* governance requirements

This complexity is accepted because learner understanding is the core institutional capability.

---

# 10. Responsible AI Considerations

Conversation Intelligence must follow:

## Privacy

Only meaningful information should be retained.

---

## Transparency

Families should understand how conversations contribute to learner insights.

---

## Human Oversight

Important interpretations should remain reviewable.

---

# 11. Future Evolution

Conversation Intelligence may evolve into:

* continuous learner understanding
* multilingual educational conversations
* voice-based interactions
* emotional learning support
* advanced learning analytics

---

# 12. Conclusion

Conversation Intelligence transforms Homehelp from a system that stores information into an institution that continuously learns about its learners.

Conversations become knowledge.

Knowledge becomes understanding.

Understanding enables better support.
