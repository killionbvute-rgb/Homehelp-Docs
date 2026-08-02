# Sprint 06 Domain Design Review

## Sprint

Sprint 06 — Learner Knowledge Evolution Intelligence

## Date

01 August 2026

## Status

Draft for Review

---

# 1. Purpose

This Domain Design Review evaluates the domain changes required to evolve Homehelp's Knowledge Evolution capability from a historical recording mechanism into an explainable learner intelligence model.

Previous sprints established:

Learner Profile

↓

Discovery

↓

Conversation Intelligence

↓

Learner Insights

↓

Knowledge Evolution

↓

Educational Guidance

Sprint 06 strengthens Knowledge Evolution by introducing:

- Confidence representation
- Evidence references
- Contextual historical understanding
- Improved explainability

The objective is:

> Enable Homehelp to understand how learner understanding changes over time while preserving evidence, confidence and auditability.

---

# 2. Current Domain Capability

Before Sprint 06, Homehelp supported:

Conversation Intelligence

    |

    v
    Learner Insights
    |

    v
Knowledge Evolution

Knowledge Evolution could record that a learner understanding changed.

The limitation:

Knowledge Evolution
    |

    v
    What changed?
    
but lacked:
Why did it change?

How confident is the system?

What evidence supports the change?

How does this relate to previous learner understanding?

---

# 3. Domain Design Objective

Sprint 06 introduces the capability to represent:

- Confidence of learner knowledge changes
- Evidence supporting evolution decisions
- Historical learner development context
- Explainable intelligence progression

The objective is:

> Transform Knowledge Evolution into an evidence-based learner intelligence foundation.

---

# 4. Bounded Context Alignment

The capability remains within:

## Learner Intelligence Context

Reason:

Knowledge Evolution represents understanding about the learner.

It depends on:

- Learner Insights
- Conversation Intelligence outcomes
- Evidence generated from interactions

It should not move into:

## Conversation Context

because conversations provide evidence but are not the intelligence model.

It should not move into:

## AI Intelligence Context

because AI may interpret intelligence but the domain remains the source of truth.

---

# 5. Existing Domain Concept

## KnowledgeEvolution

Purpose:

Represents a meaningful change in learner understanding.

Existing concepts:

- learnerId
- insightId
- evolutionType
- previousValue
- newValue
- reason
- timestamps

---

# 6. Sprint 06 Domain Enhancements

## 6.1 Knowledge Evolution Confidence

### Purpose

Represents how confident Homehelp is about an observed learner change.

Example:

Observation:

"Reading confidence improved."

Confidence:

High

Reason:

Multiple conversations and parent observations support the change.

---

### Proposed Property

confidence:
LearnerInsightConfidence

---

## 6.2 Evidence References

### Purpose

Links learner evolution to supporting evidence.

Evidence may originate from:

- conversations
- learner insights
- parent feedback
- future assessments

---

### Proposed Property

evidenceIds:
UniqueEntityID[]


---

## 6.3 Contextual Evolution History

### Purpose

Allow future intelligence capabilities to understand learner development over time.

Relationship:

Knowledge Evolution
    +
   Learner Insight Context
    +
   Confidence 
    +
    Evidence
    
---

# 7. Domain Relationship Model

Updated intelligence flow:

Conversation
    |

    v
    Conversation Evidence
    |

    v
Learner Insight
    |

    v
Knowledge Evolution
    |

    +--> Confidence

    +--> Evidence References

    +--> Historical Context

    |

    v
    Future Personalised Guidance
    
---

# 8. Domain Events

Existing event:

KnowledgeEvolutionRecorded


remains valid.

Future events may include:

KnowledgeEvolutionConfidenceUpdated

KnowledgeEvolutionEvidenceAdded

KnowledgeEvolutionPatternDetected


These are future considerations and are not required for Sprint 06.

---

# 9. Application Layer Impact

Sprint 06 affects:

## Existing Workflows

RecordKnowledgeEvolution


Updated to include:

- confidence
- evidence references


## New Workflow

GetLearnerEvolutionHistoryWithContext


Purpose:

Provide historical learner development context.

---

# 10. AI Boundary Review

AI responsibilities:

- Identify possible learner patterns
- Suggest confidence levels
- Assist interpretation

Domain responsibilities:

- Preserve recorded intelligence
- Maintain evidence references
- Store historical truth
- Support auditability

Principle:

> AI may suggest understanding; the domain preserves understanding history.

---

# 11. Responsible AI Considerations

Sprint 06 maintains:

## Explainability

Every learner evolution should answer:

"What changed and why?"

## Evidence-Based Intelligence

Changes should reference supporting observations.

## Confidence Awareness

The system should understand uncertainty.

## Auditability

Historical learner changes must remain reviewable.

---

# 12. Testing Requirements

Required validation:

## Domain Tests

Validate:

- Knowledge Evolution creation
- Confidence storage
- Evidence references

## Application Tests

Validate:

- Evolution recording workflow
- Contextual history retrieval

## Regression Tests

Validate:

- Existing learner intelligence flows remain stable

---

# 13. Design Recommendation

Sprint 06 recommendation:

- Keep KnowledgeEvolution as the owner of learner change history.
- Store confidence as part of evolution intelligence.
- Reference evidence rather than duplicating evidence data.
- Build contextual history retrieval as an application capability.
- Preserve AI as an assistant, not the source of truth.

---

# Conclusion

Sprint 06 evolves Homehelp from:

"Homehelp records learner changes"

towards:

"Homehelp understands how learner understanding evolves over time."

The domain now provides a foundation for:

- personalised guidance
- explainable AI
- learner development trends
- evidence-backed intelligence
