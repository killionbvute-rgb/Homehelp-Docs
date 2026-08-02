# Homehelp Architecture Traceability Matrix

Version: 2.1

Last Updated: Sprint 06 Learner Knowledge Evolution Intelligence Alignment

Status: Active Governance Document

---

# Capability Portfolio Traceability

The following capabilities represent the strategic commitments defined in Product Execution Roadmap v2.

| Capability | Current Status | Primary Bounded Context | Evidence |
|---|---|---|---|
| Learner Understanding Foundation | Implemented | Learner Profile / Discovery | ADR-003, ADR-004 |
| Learner Knowledge Evolution | Implemented | Learner Intelligence | ADR-007, ADR-013 |
| Conversation Intelligence | Implemented Foundation | Conversation | ADR-009 |
| AI Prompt Engine and Intelligence Orchestration | Planned | AI Intelligence | Pending |
| Learner Intelligence | Implemented | Learner Intelligence | ADR-007, ADR-010 |
| Parent Trust and Explainability | Implemented | Learner Intelligence | ADR-011 |
| Visual Learning Support | Planned | Learning Experience | Pending |
| Learning Progress Intelligence | Planned | Learner Intelligence | Pending |
| Parent Coaching Intelligence | Partially Implemented | Learner Intelligence | ADR-010 |
| School Integration | Planned | Collaboration | Pending |
| Multi-Learner Family Support | Planned | Family | Pending |
| Personalised Learning Plans | Planned | Learning Experience | Pending |
| Production Excellence and Governance | Ongoing | Platform Governance | ADR-012 |

---

# Purpose

This document provides traceability between:

- Business capabilities
- Architectural decisions
- Domain models
- Application workflows
- Domain events
- Implementation evidence

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
| Evolution of learner understanding | Learner Intelligence | KnowledgeEvolution, KnowledgeEvolution Confidence, Evidence References | RecordKnowledgeEvolution, GetLearnerEvolutionHistory, GetLearnerEvolutionHistoryWithContext | KnowledgeEvolutionRecorded | ADR-007, ADR-013 | Implemented |

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
| Infrastructure Layer | Successful TypeScript compilation |
| API Layer | Successful TypeScript compilation |
| Application Behaviour | Automated test suite passing |
| Current Validation Snapshot | Sprint 06 validation: 46 test files passing, 63 tests passing |

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

---

# Roadmap v2 Alignment

The traceability model follows capability-oriented governance.

Sprint references remain as implementation history.

Future delivery decisions shall trace:

Capability
|
v
Bounded Context
|
v
Domain Model
|
v
Application Workflow
|
v
Tests
|
v
Evidence


---

# Sprint 06 Alignment Summary

Sprint 06 extended Learner Knowledge Evolution from a historical record mechanism into an explainable intelligence model.

Traceability additions:

- ADR-013 Knowledge Evolution Intelligence Model
- Knowledge Evolution confidence tracking
- Evidence reference foundation
- Contextual learner evolution history retrieval

The capability now supports future:

- Trend detection
- Pattern recognition
- Evidence-backed AI reasoning
- Personalised guidance evolution
