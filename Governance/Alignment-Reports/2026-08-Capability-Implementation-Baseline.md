Homehelp Capability Implementation Baseline
Document Information

Document ID: HH-GOV-003
Version: 1.0
Date: 2026-08-01
Status: Active Governance Document

1. Purpose

This document establishes the implementation baseline for the Homehelp AI Learning Companion against Product Execution Roadmap v2.

It identifies:

Delivered capabilities
Partially implemented capabilities
Future capabilities
Existing architectural assets
Remaining implementation gaps

The baseline ensures future development proceeds from the current architectural reality.

| Capability                                    | Current Status         | Evidence                            |
| --------------------------------------------- | ---------------------- | ----------------------------------- |
| Learner Understanding Foundation              | Implemented Foundation | LearnerProfile, DiscoverySession    |
| Learner Knowledge Evolution                   | Implemented Foundation | KnowledgeEvolution aggregate        |
| Conversation Intelligence                     | Implemented Foundation | Conversation workflows              |
| Learner Intelligence                          | Implemented Foundation | LearnerInsight, Recommendations     |
| Parent Trust & Explainability                 | Implemented Foundation | GuidanceReview, GuidanceExplanation |
| AI Prompt Engine & Intelligence Orchestration | Not Implemented        | Future capability                   |
| Visual Learning Support                       | Not Implemented        | Future capability                   |
| Learning Progress Intelligence                | Not Implemented        | Future capability                   |
| Parent Coaching Intelligence                  | Partially Prepared     | Guidance foundations exist          |
| School Integration                            | Not Implemented        | Future capability                   |
| Multi-Learner Family Support                  | Not Implemented        | Future capability                   |
| Personalised Learning Plans                   | Not Implemented        | Future capability                   |
| Production Excellence & Governance            | Foundation Exists      | Governance framework                |

3. Current Domain Capability Map
Learner Understanding Foundation
Domain Assets

LearnerProfile
DiscoverySession
LearnerInsight

Application Assets

CompleteDiscoveryAndGenerateProfile
GenerateLearnerInsightsFromDiscovery
RecordLearnerInsight

Status:

Implemented foundation.

Learner Intelligence
Domain Assets

LearnerInsight
KnowledgeEvolution
LearningRecommendation
EducationalGuidance
GuidanceContext

Application Assets

GenerateLearnerInsightsFromConversation
RecordKnowledgeEvolution
GetLearnerEvolutionHistory
CreateLearningRecommendation
BuildGuidanceContext

Status:

Implemented foundation.

Parent Trust & Explainability

Domain Assets

GuidanceReview
GuidanceExplanation
ParentGuidanceFeedback

Application Assets

CreateGuidanceReview
ViewGuidanceReview
AcknowledgeGuidanceReview
QuestionGuidanceReview
CompleteGuidanceReview
RecordParentGuidanceFeedback

Status:

Implemented foundation.

4. Capability Gaps
AI Prompt Engine and Intelligence Orchestration

Current:

AI analysis flows exist.

Missing:

Prompt templates
Prompt versioning
Prompt evaluation
Model routing
Safety constraints
AI reasoning traceability

Priority:

High

Reason:

This capability becomes the intelligence control plane.

Visual Learning Support

Current:

Not implemented.

Required:

Visual explanations
Learner-friendly representations
Adaptive visual content selection
Accessibility considerations

Priority:

High

Reason:

Supports visual learners and inclusive learning.

School Integration

Current:

Not implemented.

Required:

Teacher profiles
School context
Curriculum alignment
Teacher feedback loops

Priority:

Medium

Multi-Learner Family Support

Current:

Not implemented.

Required:

Family account
Multiple learner profiles
Parent switching
Shared insights

Priority:

Medium

5. Recommended Next Capability Sequence

Based on current architecture:

Capability Wave 1 — Intelligence Foundation

Already underway:

✅ Learner Understanding
✅ Learner Intelligence
✅ Parent Trust

Next:

➡ AI Prompt Engine

Reason:

Everything downstream depends on controlled AI intelligence.

Capability Wave 2 — Learning Experience

Next:

➡ Visual Learning Support
➡ Learning Progress Intelligence
➡ Personalised Learning Plans

Capability Wave 3 — Ecosystem Expansion

Next:

➡ School Integration
➡ Multi-Learner Family Support

6. Governance Rule

Before implementing any new capability:

Validate:

Capability
↓
Domain Boundary
↓
Aggregate
↓
Application Workflow
↓
Tests
↓
Documentation
