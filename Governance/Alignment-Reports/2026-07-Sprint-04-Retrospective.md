# Sprint 04 Retrospective

## Sprint

Sprint 04 — Learner Intelligence and Personalised Guidance

## Date

30 July 2026

## Status

Completed

---

# Sprint Objective

Sprint 04 transformed accumulated learner understanding into personalised educational guidance.

The sprint introduced the Learner Intelligence capability responsible for converting:

- Learner Profiles
- Learner Insights
- Knowledge Evolution history

into transparent and traceable educational guidance.

---

# What Went Well

## 1. Successful Extension of the Intelligence Pipeline

Sprint 04 successfully extended the Homehelp intelligence architecture:


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


The system now has a complete pathway from parent interaction to educational support.

---

## 2. Strong Domain Separation

The implementation maintained clear architectural boundaries.

Learner Intelligence introduced:

- GuidanceContext
- LearningRecommendation
- EducationalGuidance

without creating unnecessary coupling with:

- Conversation domain
- Discovery domain
- Learner Profile domain

This preserved the bounded context approach established in earlier sprints.

---

## 3. Responsible AI Boundary Established

Sprint 04 successfully maintained the principle that:

> AI generates suggestions; the domain preserves truth and history.

The AI capability was introduced through contracts:

- IGuidanceGenerator
- GuidanceGenerationResult

This allows future replacement of the current in-memory implementation with production AI services without changing the domain model.

---

## 4. Automated Verification Improved

Sprint 04 completion was supported by:

- Successful TypeScript builds
- 37 passing test files
- 52 passing tests

Testing covered:

- Learner Intelligence workflows
- Guidance generation
- Repository behaviour
- Integration scenarios

---

# Challenges Encountered

## 1. Rapid Domain Growth

As Homehelp evolved from learner profiles into intelligence capabilities, the number of domain concepts increased significantly.

New concepts introduced:

- Learner Insights
- Knowledge Evolution
- Learner Intelligence
- Educational Guidance

This reinforced the importance of maintaining strict domain organisation.

---

## 2. Repository Discipline

The project previously encountered issues caused by duplicated or competing domain structures.

Sprint 04 reinforced the importance of:

- Single source of truth
- Clear aggregate ownership
- Controlled domain evolution

Future development should continue verifying whether capabilities already exist before creating new structures.

---

## 3. AI Capability Design

Introducing AI required careful consideration of boundaries.

The key design decision was avoiding AI logic inside domain entities.

The resulting architecture keeps AI replaceable and preserves trust.

---

# Architectural Lessons Learned

## 1. Intelligence Must Be Built on Accumulated Understanding

Educational intelligence should not make isolated predictions.

It should reason from:

- Historical learner understanding
- Evidence
- Previous observations
- Recorded evolution

---

## 2. Domain Models Should Represent Meaning, Not Technology

The domain should express concepts such as:

- Recommendation
- Guidance
- Learner development

rather than:

- AI prompts
- Model outputs
- Vendor-specific implementations

---

## 3. AI Should Remain Replaceable

The current:


InMemoryGuidanceGenerator


is an implementation detail.

Future AI providers can be introduced behind:


IGuidanceGenerator


without architectural disruption.

---

# Technical Debt Identified

## AI Evaluation Framework

Future releases should introduce mechanisms to evaluate:

- Guidance quality
- Accuracy
- Parent usefulness
- Educational impact

---

## Persistent Intelligence Storage

Current repositories are in-memory.

Future implementation requires:

- Database-backed repositories
- Historical guidance storage
- Audit capabilities

---

## Human Feedback Loop

Future versions should capture:

- Parent feedback
- Guidance usefulness
- Learner outcomes

to improve future recommendations.

---

# Recommendations for Sprint 5

Sprint 5 should focus on transforming intelligence capabilities into a parent-facing experience.

Potential focus areas:

- Parent guidance presentation
- Explainability of recommendations
- Parent interaction workflows
- Trust-building mechanisms
- Feedback collection

The objective should move from:


Homehelp understands learners


towards:


Parents can understand and act on learner intelligence


---

# Final Reflection

Sprint 04 represents a major architectural milestone.

Homehelp has progressed from collecting learner information to creating meaningful educational intelligence.

The platform now has the foundation required for responsible AI-assisted learning support.

The next phase should focus on delivering this intelligence through trusted, accessible experiences for parents and learners.

After saving, run:

git status

Then:

git add Governance/Alignment-Reports/2026-07-Sprint-04-Retrospective.md

git commit -m "Document Sprint 4 retrospective and architectural lessons"

git push

Once this is committed, Sprint 4 will have the full governance lifecycle:

Blueprint
    ↓
Implementation
    ↓
Architecture Alignment
    ↓
Retrospective
    ↓
Sprint 5 Preparation