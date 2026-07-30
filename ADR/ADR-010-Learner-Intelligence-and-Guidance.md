# ADR-010: Learner Intelligence and Personalised Guidance

## Status

Accepted

## Date

2026-07-30

---

# Context

Homehelp has established the ability to understand learners through:

- Learner Profiles
- Conversation Intelligence
- Learner Insights
- Knowledge Evolution

However, understanding alone does not create educational value.

The system requires a capability that transforms accumulated learner understanding into personalised educational guidance.

---

# Decision

Homehelp will introduce a Learner Intelligence capability responsible for transforming learner knowledge into structured educational recommendations and guidance.

The capability will not replace human judgement.

It will provide supportive educational insights for parents and learners.

---

# Domain Boundary

The domain will model:

- Learning Recommendations
- Educational Guidance
- Recommendation lifecycle

AI services remain responsible for:

- Pattern recognition
- Natural language generation
- Recommendation generation assistance

---

# Consequences

Positive:

- Clear separation between intelligence and AI implementation
- Responsible AI boundary maintained
- Learner understanding can create actionable value

Negative:

- Additional domain concepts introduced
- Guidance quality depends on available learner knowledge

---

# Related ADRs

- ADR-002 Separate AI Service
- ADR-005 Conversation Intelligence
- ADR-007 Learner Knowledge Evolution
- ADR-008 Education Intelligence Platform