# Homehelp Source Code Map

## 1. Introduction

This document provides a map between Homehelp architectural capabilities and their physical implementation within the source repository.

Repository:

```text
homehelp-institution
```

The purpose is to maintain visibility between design decisions and actual code.

The guiding principle:

> Every important capability should have a known place in the codebase.

---

# 2. Repository Overview

```text
homehelp-institution

├── apps
│
│   └── api
│
└── packages
    │
    ├── domain
    │
    ├── application
    │
    ├── infrastructure
    │
    ├── ai
    │
    └── shared
```

---

# 3. Domain Package

Location:

```text
packages/domain
```

Purpose:

Contains enterprise business concepts.

Responsibilities:

* aggregates
* entities
* value objects
* domain events
* business rules

---

## Current Domain Capabilities

### Learner Profile

Concept:

```text
LearnerProfile
```

Purpose:

Represent understanding of an individual learner.

Related documentation:

```text
Domain/Domain-Overview.md
Implementation/Domain-Implementation.md
ADR/ADR-003-LearnerProfile-Aggregate.md
```

---

### Discovery Session

Concept:

```text
DiscoverySession
```

Purpose:

Represent the learner discovery journey.

Related documentation:

```text
ADR/ADR-004-Discovery-Driven-Learner-Understanding.md
```

---

### Domain Events

Current events:

```text
DiscoveryStarted

DiscoveryCompleted
```

Purpose:

Allow business events to be communicated without coupling components.

---

# 4. Application Package

Location:

```text
packages/application
```

Purpose:

Coordinates business workflows.

Responsibilities:

* execute use cases
* coordinate repositories
* manage application processes

---

## Current Use Cases

### Complete Discovery Session

Implementation:

```text
CompleteDiscoverySession
```

Purpose:

Move discovery journey to completion.

---

### Generate Learner Profile

Implementation:

```text
GenerateLearnerProfileFromDiscovery
```

Purpose:

Create learner understanding from discovery information.

---

# 5. API Application

Location:

```text
apps/api
```

Purpose:

External system entry point.

Responsibilities:

* HTTP communication
* request handling
* authentication
* application invocation

---

# 6. Infrastructure Package

Location:

```text
packages/infrastructure
```

Purpose:

Technical implementations.

Potential responsibilities:

* database persistence
* external services
* messaging
* integrations

---

# 7. AI Package

Location:

```text
packages/ai
```

Purpose:

Future intelligence capabilities.

Planned components:

```text
Conversation Intelligence

Insight Extraction

Recommendation Engine
```

Related documentation:

```text
AI/AI-Learning-Companion-Design.md

ADR/ADR-005-Conversation-Intelligence.md
```

---

# 8. Shared Package

Location:

```text
packages/shared
```

Purpose:

Common technical capabilities.

Potential contents:

* shared utilities
* common types
* cross-cutting helpers

---

# 9. Capability Mapping

| Capability         | Layer          | Location                |
| ------------------ | -------------- | ----------------------- |
| Learner Profile    | Domain         | packages/domain         |
| Discovery Workflow | Application    | packages/application    |
| API Access         | API            | apps/api                |
| Persistence        | Infrastructure | packages/infrastructure |
| AI Intelligence    | AI             | packages/ai             |

---

# 10. Dependency Direction

Homehelp follows:

```text
API

 |

v

Application

 |

v

Domain


Infrastructure implements interfaces
```

The domain remains independent.

---

# 11. Future Expansion

Future mappings will include:

* LearnerInsight aggregate
* LearningPlan aggregate
* Parent Engagement capability
* AI conversation pipelines
* Analytics services

---

# 12. Conclusion

The Source Code Map ensures that Homehelp remains understandable as the codebase grows.

It creates a permanent link between:

* institutional goals
* architecture decisions
* domain concepts
* implementation reality

> A system that can explain its structure can evolve safely.
