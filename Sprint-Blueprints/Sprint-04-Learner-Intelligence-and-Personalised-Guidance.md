# Sprint 04 — Learner Intelligence and Personalised Guidance

## Status

Completed — 30 July 2026

## Objective

Transform accumulated learner understanding into personalised educational guidance for parents and learners.

Sprint 3 established Homehelp's ability to continuously understand learners through:

- Learner Profiles
- Conversation Intelligence
- Learner Insights
- Knowledge Evolution

Sprint 4 introduces the intelligence capability that uses this understanding to provide meaningful educational support.

---

# Architectural Context

Sprint 4 extends the existing intelligence pipeline:

Parent Conversation

↓

Conversation Intelligence

↓

Learner Insights

↓

Knowledge Evolution

↓

Learner Intelligence

↓

Personalised Guidance

---

# Related Architecture Decisions

This sprint builds upon:

- ADR-002 — Separate AI Service Architecture
- ADR-005 — Conversation Intelligence
- ADR-007 — Learner Knowledge Evolution Model
- ADR-008 — Education Intelligence Platform

---

# Sprint Goals

## Goal 1 — Introduce Learner Intelligence Layer

Create the capability to combine:

- Learner Profile information
- Learner Insights
- Knowledge Evolution history
- Conversation context

into a structured intelligence context.

---

## Goal 2 — Generate Personalised Educational Guidance

Enable Homehelp to produce guidance such as:

- Recommended learning approaches
- Suggested parental support strategies
- Learning habit recommendations
- Areas requiring attention

---

## Goal 3 — Maintain Responsible AI Boundaries

AI-generated guidance must:

- Be based on available learner understanding
- Preserve transparency
- Avoid unsupported assumptions
- Maintain human oversight

---

# Proposed Domain Concepts

## LearningRecommendation

Represents a suggested educational action based on learner understanding.

Examples:

- Preferred learning approach
- Suggested study habit
- Learning support strategy

---

## EducationalGuidance

Represents a parent-facing recommendation generated from learner intelligence.

---

## GuidanceContext

Represents the information used when generating guidance.

Contains:

- Learner identity
- Learner profile
- Learner insights
- Knowledge evolution history

---

# Application Use Cases

Potential use cases:

- GenerateLearningRecommendation
- GenerateEducationalGuidance
- GetLearnerGuidanceHistory

---

# AI Integration Boundary

The AI capability remains outside the domain layer.

AI responsibilities:

- Pattern recognition
- Recommendation generation
- Natural language generation

Domain responsibilities:

- Learner concepts
- Guidance lifecycle
- Validation rules
- Historical records

---

# Testing Requirements

Sprint completion requires:

- Domain tests
- Application tests
- AI boundary tests
- Integration tests

---

# Completion Criteria

Sprint 04 is complete when:

- Learner Intelligence model exists
- Guidance generation workflow exists
- AI integration boundary is established
- Parent-facing guidance can be generated
- Tests pass successfully

---

# Implementation Evidence

## Repository

Homehelp-institution

## Completion Commit

99438b3908646af9625b846d7af3defaf80db65f

## Git Tag

sprint-4-complete

---

# Delivered Capabilities

Sprint 04 delivered:

## Learner Intelligence Layer

Implemented:

- GuidanceContext
- LearningRecommendation
- EducationalGuidance

The intelligence layer combines:

- Learner Profile
- Learner Insights
- Knowledge Evolution history

into a structured context for educational guidance generation.

---

## Personalised Guidance Workflow

Implemented application workflows:

- BuildGuidanceContext
- CreateLearningRecommendation
- GenerateEducationalGuidance
- GetLearnerGuidanceHistory
- GetLearnerRecommendations

---

## Responsible AI Boundary

Implemented:

- IGuidanceGenerator contract
- GuidanceGenerationResult
- InMemoryGuidanceGenerator

AI capabilities remain outside the domain layer.

The domain maintains:

- Guidance lifecycle
- Historical records
- Educational concepts
- Traceability

---

# Verification

Sprint 04 completion verified through:

- Successful TypeScript build
- 37 passing test files
- 52 passing tests

---

# Architectural Note

Conversation context is consumed indirectly through Learner Insights.

The system intentionally avoids coupling Learner Intelligence directly to Conversation entities.

Flow:

Parent Conversation

↓

Conversation Intelligence

↓

Learner Insights

↓

Learner Intelligence

↓

Personalised Guidance