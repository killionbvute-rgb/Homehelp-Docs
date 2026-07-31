# Homehelp Architecture Traceability Matrix

# Homehelp Architecture Traceability Matrix

Version: 2.0

Last Updated: Sprint 05 Completion

Status: Active Governance Document

## Purpose

This document provides traceability between business capabilities, architectural decisions, domain models, application workflows, domain events, and implementation evidence.

The matrix ensures that:

- Every capability has a clear architectural owner.
- Domain concepts map to application behaviour.
- AI-assisted functionality remains explainable and auditable.
- Implementation decisions remain traceable to ADRs.

---

# 1. Learner Identity Capability

| Capability | Bounded Context | Domain Concepts | Application Workflows | Domain Events | ADR | Status |
|---|---|---|---|---|---|---|
| Learner identity management | Learner Profile | LearnerProfile, LearnerName, GradeLevel | CreateLearnerProfile | LearnerProfileCreated | ADR-003 | Implemented |

---

# 2. Learner Discovery Capability

| Capability | Bounded Context | Domain Concepts | Application Workflows | Domain Events | ADR | Status |
|---|---|---|---|---|---|---|
| Learner information discovery | Discovery | DiscoverySession, DiscoveryResponse | CreateDiscoverySession, RecordDiscoveryResponse, CompleteDiscoverySession | DiscoveryStarted, DiscoveryCompleted | ADR-004 | Implemented |

---

# 3. Learner Intelligence Capability

## 3.1 Learner Insights

| Capability | Bounded Context | Domain Concepts | Application Workflows | Events | ADR | Status |
|---|---|---|---|---|---|---|
| Understanding learner patterns | Learner Intelligence | LearnerInsight | RecordLearnerInsight, GenerateLearnerInsights | LearnerInsightRecorded | ADR-007 | Implemented |

---

## 3.2 Knowledge Evolution

| Capability | Bounded Context | Domain Concepts | Application Workflows | Events | ADR | Status |
|---|---|---|---|---|---|---|
| Evolution of learner understanding | Learner Intelligence | KnowledgeEvolution | RecordKnowledgeEvolution, GetLearnerEvolutionHistory | KnowledgeEvolutionRecorded | ADR-007 | Implemented |

---

## 3.3 Learning Recommendations

| Capability | Bounded Context | Domain Concepts | Application Workflows | Events | ADR | Status |
|---|---|---|---|---|---|---|
| Generate actionable learning suggestions | Learner Intelligence | LearningRecommendation | CreateLearningRecommendation, GetLearnerRecommendations | LearningRecommendationCreated | ADR-010 | Implemented |

---

## 3.4 Educational Guidance

| Capability | Bounded Context | Domain Concepts | Application Workflows | Events | ADR | Status |
|---|---|---|---|---|---|---|
| Generate personalised educational guidance | Learner Intelligence | EducationalGuidance, GuidanceContext | GenerateEducationalGuidance, BuildGuidanceContext | EducationalGuidanceCreated | ADR-010 | Implemented |

---

# 4. Parent Trust Capability

| Capability | Bounded Context | Domain Concepts | Application Workflows | Domain Events | ADR | Status |
|---|---|---|---|---|---|---|
| Transparent parent interaction with AI guidance | Learner Intelligence | GuidanceReview, ParentGuidanceFeedback, GuidanceExplanation | CreateGuidanceReview, ViewGuidanceReview, AcknowledgeGuidanceReview, QuestionGuidanceReview, CompleteGuidanceReview, RecordParentGuidanceFeedback, CreateGuidanceExplanation | GuidanceReviewCreated, GuidanceReviewViewed, GuidanceReviewAcknowledged, GuidanceReviewQuestioned, GuidanceReviewCompleted, ParentGuidanceFeedbackRecorded | ADR-011 | Implemented |

---

# 5. Domain Event Traceability

| Aggregate | Events |
|---|---|
| LearnerProfile | LearnerProfileCreated |
| DiscoverySession | DiscoveryStarted, DiscoveryCompleted |
| LearnerInsight | LearnerInsightRecorded |
| KnowledgeEvolution | KnowledgeEvolutionRecorded |
| LearningRecommendation | LearningRecommendationCreated |
| EducationalGuidance | EducationalGuidanceCreated |
| GuidanceReview | GuidanceReviewCreated, GuidanceReviewViewed, GuidanceReviewAcknowledged, GuidanceReviewQuestioned, GuidanceReviewCompleted |
| ParentGuidanceFeedback | ParentGuidanceFeedbackRecorded |

---

# 6. Validation Evidence

| Capability | Evidence |
|---|---|
| Domain Layer | Successful TypeScript compilation |
| Application Layer | Successful TypeScript compilation |
| Application Behaviour | Automated test suite passing |
|| Current Validation Snapshot | Sprint 05 validation: 45 test files passing, 62 tests passing |

API / Interface Boundary

Pending API implementation

---

# 7. Change Impact Analysis

Before changing functionality, identify the affected:

- Business capability
- Bounded context
- Domain aggregates
- Value objects
- Application use cases
- Repository contracts
- Tests
- ADRs
- Documentation artifacts

Any architectural change must update the relevant traceability entries.

---

# 8. Governance Rules

New functionality requires:

- Documented business purpose
- Architectural consideration
- Domain impact analysis
- Implementation reference
- Testing evidence
- Traceability update

The Traceability Matrix must remain aligned with the implemented architecture.
