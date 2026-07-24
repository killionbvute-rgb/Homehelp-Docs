# ADR-002: Separate AI Service Architecture

## Status

Accepted

## Date

2026-07-24

---

# 1. Context

Homehelp is an AI-powered learning institution.

Artificial intelligence provides important capabilities including:

* conversation understanding
* learner insight extraction
* personalised support
* pattern recognition
* recommendation assistance

However, AI technology changes rapidly.

New models, providers, techniques, and capabilities will continue to emerge.

The core educational domain must remain stable regardless of AI technology changes.

---

# 2. Decision

AI capabilities will be implemented as a separate service boundary.

The AI layer will communicate with the application and domain layers through clearly defined interfaces.

The architecture follows:

```text
                Homehelp Application

                         |
                         |
                  AI Service Boundary

                         |
          --------------------------------
          |              |               |
       AI Models     AI Providers    AI Tools
```

---

# 3. Reasons for the Decision

## 3.1 Protect the Domain

Educational concepts must not depend on artificial intelligence implementation details.

The domain should understand:

* learner insights
* conversations
* discoveries
* recommendations

It should not understand:

* model versions
* prompts
* AI provider APIs
* inference mechanisms

---

## 3.2 Allow AI Evolution

AI technology changes faster than traditional software.

Separating AI allows Homehelp to:

* upgrade models
* change providers
* experiment safely
* introduce new capabilities

without redesigning the core system.

---

## 3.3 Improve Governance

AI requires additional governance.

A separate boundary allows better management of:

* AI decisions
* model behaviour
* safety controls
* monitoring
* evaluation

---

# 4. Architectural Consequences

## Positive Consequences

### Technology Flexibility

The institution can adopt improved AI technology over time.

---

### Better Security

AI interactions can be controlled and monitored.

---

### Clear Responsibilities

The system separates:

Educational Knowledge:

* Domain Layer

AI Processing:

* AI Service Layer

---

### Easier Testing

AI behaviour can be evaluated independently.

---

# 5. Trade-offs

Additional complexity is introduced.

The system requires:

* service interfaces
* communication boundaries
* AI integration management

This complexity is accepted because AI is a strategic capability that will continue evolving.

---

# 6. AI Responsibilities

The AI service is responsible for:

## Conversation Understanding

Processing natural conversations.

---

## Insight Extraction

Identifying meaningful learner information.

---

## Pattern Recognition

Finding useful learning-related patterns.

---

## Recommendation Support

Providing possible learning suggestions.

---

# 7. AI Does Not Own

The AI service does not own:

* learner identity
* learner profile lifecycle
* educational rules
* institutional policies

These remain in the domain.

---

# 8. Current Relationship With Domain

The relationship is:

```text
Conversation
      |
      v

AI Understanding

      |
      v

Structured Insight

      |
      v

Domain Model Update
```

The domain decides how knowledge is represented.

AI assists with understanding.

---

# 9. Future Evolution

The AI boundary allows future capabilities:

* specialised education models
* voice conversations
* multilingual learning support
* advanced learner analytics
* adaptive learning assistants

without disrupting the institutional core.

---

# 10. Conclusion

AI is a powerful capability, but it must remain aligned with institutional principles.

Separating AI from the core architecture ensures:

* flexibility
* safety
* governance
* long-term sustainability

The institution controls the intelligence layer rather than becoming dependent on it.
