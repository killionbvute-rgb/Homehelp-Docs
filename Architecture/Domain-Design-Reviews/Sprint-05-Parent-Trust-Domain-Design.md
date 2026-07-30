# Sprint 05 Domain Design Review

## Sprint

Sprint 05 — Parent Trust and Guidance Experience

## Date

30 July 2026

## Status

Draft for Review

---

# 1. Purpose

This Domain Design Review evaluates the domain changes required to transform Homehelp's personalised educational guidance capability into a trusted parent experience.

Sprint 04 established the Learner Intelligence capability responsible for transforming accumulated learner understanding into educational guidance.

Sprint 05 introduces the trust and interaction layer that enables parents to:

- Understand generated guidance
- Review recommendations
- Provide feedback
- Contribute additional learner context

---

# 2. Current Domain Capability

Before Sprint 05, Homehelp supports:


Learner Profile

    ↓

Conversation Intelligence

    ↓

Learner Insights

    ↓

Knowledge Evolution

    ↓

Learner Intelligence

    ↓

Educational Guidance


The system can generate educational guidance.

The current limitation:


Educational Guidance

    ↓

Parent Understanding

    ↓

Parent Feedback


The interaction and trust lifecycle does not yet exist.

---

# 3. Domain Design Objective

Sprint 05 should introduce the capability to represent:

- Parent interaction with guidance
- Guidance transparency
- Parent observations
- Trust-building feedback loops

The objective is:

> Enable parents to understand, evaluate, and contribute to learner intelligence.

---

# 4. Bounded Context Alignment

The proposed capabilities belong within the:

## Learner Intelligence Context

Reason:

The concepts relate to:

- educational recommendations
- guidance quality
- learner understanding evolution

They should not be placed inside:

## Parent Identity Context

because they do not represent:

- authentication
- registration
- identity management

They should not be placed inside:

## Conversation Intelligence Context

because they represent the outcome of intelligence, not the conversation itself.

---

# 5. Proposed Domain Concepts

## 5.1 GuidanceReview

### Purpose

Represents a parent's interaction with generated educational guidance.

A GuidanceReview records whether a parent:

- viewed guidance
- accepted guidance
- questioned guidance
- completed recommended actions

---

## Possible Lifecycle


Generated

↓

Viewed

↓

Acknowledged

↓

Questioned

↓

Completed


---

## Candidate Properties


reviewId

learnerId

guidanceId

parentId

status

createdAt

updatedAt


---

# 5.2 ParentGuidanceFeedback

## Purpose

Represents observations provided by parents about generated guidance.

Examples:

Positive feedback:

> "This matches what we observe at home."

Additional context:

> "The learner struggles more during evening study."

Review request:

> "This recommendation does not reflect current behaviour."

---

## Candidate Properties


feedbackId

learnerId

guidanceId

parentId

feedbackType

comment

createdAt


---

## Possible Feedback Types


Confirmed

AdditionalContext

Disagreed

NeedsReview


---

# 5.3 GuidanceExplanation

## Purpose

Provides transparency into why guidance was generated.

Example:

Guidance:

> Encourage daily reading practice.

Explanation:

> Recommendation generated because learner insights show strong curiosity while knowledge evolution indicates inconsistent study habits.

---

## Candidate Properties


explanationId

guidanceId

evidenceReferences

reasoningSummary

createdAt


---

# 6. Domain Relationship Model

Proposed relationship:


LearnerProfile

  ↓

LearnerInsights

  ↓

KnowledgeEvolution

  ↓

LearningRecommendation

  ↓

EducationalGuidance

  ↓

GuidanceReview

  ↓

ParentGuidanceFeedback


Supporting concept:


GuidanceExplanation


provides transparency across the guidance lifecycle.

---

# 7. Domain Events

Potential events:


GuidanceViewed

GuidanceAcknowledged

GuidanceQuestioned

ParentFeedbackRecorded

GuidanceExplanationGenerated


Events should preserve historical intelligence evolution.

---

# 8. Application Layer Impact

Potential use cases:


GetLearnerGuidanceForParent

ExplainGuidanceRecommendation

RecordGuidanceReview

RecordParentGuidanceFeedback

GetGuidanceInteractionHistory


---

# 9. AI Boundary Review

AI responsibilities:

- Generate explanation drafts
- Identify patterns
- Suggest possible interpretations

Domain responsibilities:

- Store guidance records
- Store parent feedback
- Manage lifecycle state
- Preserve historical truth

The principle remains:

> AI generates suggestions; the domain preserves truth and history.

---

# 10. Responsible AI Considerations

Sprint 05 must maintain:

## Transparency

Parents must understand why recommendations exist.

## Explainability

Guidance should be connected to available evidence.

## Human Oversight

Parents remain active participants.

## Feedback Loop

Parent observations should improve future learner understanding.

---

# 11. Testing Requirements

Required validation:

## Domain Tests

Validate:

- Review lifecycle
- Feedback rules
- Guidance relationships

## Application Tests

Validate:

- Parent guidance workflows
- Feedback recording
- Explanation retrieval

## Integration Tests

Validate:

- Guidance generation to parent interaction flow

---

# 12. Open Design Questions

Before implementation:

1. Should GuidanceReview become its own aggregate?

2. Should parent feedback directly modify learner understanding or create new knowledge evolution records?

3. Should GuidanceExplanation be stored permanently or generated on demand?

4. Should parent feedback require moderation before influencing learner intelligence?

---

# 13. Design Recommendation

Initial recommendation:

- GuidanceReview should be an aggregate.
- Parent feedback should create new intelligence evidence rather than directly modify learner data.
- Guidance explanations should be stored for auditability.
- Human review should remain possible before feedback affects learner evolution.

---

# Conclusion

Sprint 05 extends Homehelp from an intelligence generation platform into a trusted educational companion.

The system moves from:

"Homehelp understands learners"

towards:

"Homehelp helps parents understand and support learners."