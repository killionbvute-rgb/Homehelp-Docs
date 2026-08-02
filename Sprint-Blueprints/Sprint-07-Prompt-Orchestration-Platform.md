# Homehelp AI Learning Companion
# Sprint 07 Prompt Orchestration Platform

**Sprint:** Sprint 07

**Capability:** Prompt Orchestration Platform

**Status:** Planned

**Version:** 1.0

**Date:** 2026-08-02

---

# 1. Sprint Purpose

Sprint 07 introduces the Prompt Orchestration Platform capability.

The purpose of this sprint is to establish the intelligence coordination layer responsible for preparing responsible, context-aware AI interactions.

Sprint 07 does not introduce AI ownership of learner knowledge.

Learner understanding remains owned by domain capabilities:

- Learner Intelligence
- Knowledge Evolution
- Educational Guidance

The Prompt Orchestration Platform coordinates trusted domain knowledge into AI interaction workflows.

---

# 2. Business Objective

The business objective of Sprint 07 is to enable Homehelp to provide more consistent, personalised and responsible AI-assisted learning support.

The capability should enable:

- Relevant learner context selection
- Consistent AI interaction behaviour
- Future personalised guidance improvements
- Controlled prompt evolution
- Responsible AI interaction management

The outcome is a foundation for scaling AI capabilities without compromising trust or explainability.

---

# 3. Current Capability

Before Sprint 07, Homehelp has established:

## Learner Understanding Foundation

Including:

- LearnerProfile
- DiscoverySession
- Learner Intelligence
- Knowledge Evolution

## Conversation Intelligence

Including:

- Conversation analysis
- Insight extraction
- Context understanding

## Educational Guidance

Including:

- Guidance generation
- Guidance context
- Parent trust foundations

## Current AI Execution Layer

Currently includes:

- Conversation Analyzer
- Guidance Generator

However, AI interaction coordination remains implicit.

Current flow:
Learner Context
    |

    v
    AI Service
    |

    v
    Generated Response
    
The platform requires an explicit orchestration capability.

---

# 4. Target Capability

After Sprint 07, Homehelp should have a Prompt Orchestration Platform capable of:

Learner Context
    |

    v
Context Assembly
    |

    v
    Prompt Orchestration
    |

    v
    AI Response Generation
    
The capability includes:

- Context assembly
- Prompt composition
- Prompt templates
- Response strategy definition
- AI interaction coordination
- Safety preparation boundaries

---

# 5. Architectural Principle

Sprint 07 follows the principle:

> AI suggests. Domain preserves truth.

Prompt Orchestration may:

- Select context
- Structure prompts
- Coordinate AI workflows
- Apply interaction policies

Prompt Orchestration must not:

- Own learner truth
- Replace domain intelligence
- Become a learner memory store
- Override domain decisions

---

# 6. Domain Impact

Sprint 07 has limited domain impact.

Existing domain ownership remains:

Conversation Intelligence
|
Learner Intelligence
|
Knowledge Evolution
|
Educational Guidance

No new learner intelligence aggregate is introduced.

Potential future domain areas may include:

- AI evaluation models
- Prompt governance lifecycle
- AI policy models

These are outside Sprint 07 scope.

---

# 7. Application Impact

Sprint 07 introduces the application orchestration layer.

Expected location:
packages/application/src/AI/PromptOrchestration


Expected capabilities:

## Context Assembly

Responsible for collecting relevant trusted context.

Potential inputs:

- Learner insights
- Knowledge evolution history
- Guidance context
- Conversation context

---

## Prompt Templates

Responsible for reusable AI interaction structures.

Potential capabilities:

- Template definition
- Template selection
- Version management

---

## Prompt Composition

Responsible for combining:

- Instructions
- Learner context
- Interaction objectives
- Safety requirements

---

## Response Strategy

Responsible for determining:

- Interaction approach
- Guidance style
- Communication strategy

---

# 8. Infrastructure Impact

Sprint 07 infrastructure impact is expected to be limited.

Potential future considerations:

- Prompt storage
- Prompt version persistence
- AI provider integration
- Model evaluation tracking

These remain future extensions.

---

# 9. Testing Strategy

Sprint 07 validation requires:

## Application Tests

Validate:

- Context assembly workflows
- Prompt composition behaviour
- Response strategy selection

## Integration Tests

Where required:

- AI service interaction boundaries
- Existing guidance workflows

## Regression Validation

Existing capabilities must remain stable:

- Conversation Intelligence
- Learner Intelligence
- Knowledge Evolution
- Educational Guidance

---

# 10. Documentation Impact

Sprint 07 requires updates to:

## Architecture Documentation

Update:

- AI capability architecture
- Application capability boundaries

## ADRs

Create ADR only if:

- A permanent architectural boundary is introduced
- New ownership decisions are required

## Traceability Matrix

Update:

Roadmap v2
|
Sprint 07 Blueprint
|
Implementation
|
Validation Evidence

---

# 11. Definition of Done

Sprint 07 is complete when:

- Prompt Orchestration capability is implemented.
- AI coordination boundaries are established.
- Existing domain ownership remains preserved.
- Automated tests pass.
- Architecture alignment is confirmed.
- Documentation is updated.
- Sprint completion review is produced.

---

# Sprint 07 Outcome

Sprint 07 transforms Homehelp from:

"AI services responding with available context"

into:

"An AI Learning Companion that deliberately orchestrates trusted learner understanding into responsible interactions."
