# ADR-014: AI Execution Boundary and Provider Architecture

## Status

Accepted

## Date

2026-08-03

---

# 1. Context

Homehelp AI Learning Companion has progressively introduced intelligence capabilities:

```
Conversation Intelligence

        |

        v

Learner Intelligence

        |

        v

Knowledge Evolution

        |

        v

Educational Guidance
```

Sprint 07 introduced Prompt Orchestration as an application capability responsible for preparing trusted AI interactions.

The next evolution requires Homehelp to execute AI interactions through external AI services.

This introduces an architectural question:

Where should AI execution responsibility exist, and how should AI providers be integrated without compromising domain ownership?

---

# 2. Decision

Homehelp will introduce an AI Execution Boundary.

AI execution will exist as an application capability supported by provider abstractions.

The architecture becomes:

```
DOMAIN OWNERSHIP

Learner Intelligence
Knowledge Evolution
Educational Guidance


        |

        v


APPLICATION INTELLIGENCE

Prompt Orchestration

        |

        v

AI Prompt Engine


        |

        v


AI PROVIDER CONTRACT


        |

        v


INFRASTRUCTURE

External AI Providers
```

---

# 3. AI Provider Abstraction

The application layer will depend on an abstraction:

```
IAIProvider
```

The application layer will not depend directly on:

* OpenAI
* Anthropic
* Google
* Other model providers

Provider implementations belong outside the application boundary.

---

# 4. Domain Protection Rules

AI execution must not:

* create learner truth
* update learner aggregates directly
* replace domain intelligence
* maintain independent learner memory

AI output must flow through controlled application/domain workflows.

The principle:

```
AI generates responses.

Domain determines meaning.
```

---

# 5. Responsibilities

## Prompt Orchestration

Responsible for:

* context assembly
* prompt preparation
* response strategy selection

---

## AI Prompt Engine

Responsible for:

* executing prepared prompts
* coordinating providers
* handling execution results

---

## AI Providers

Responsible for:

* communication with external models
* provider-specific concerns
* API interaction

---

# 6. Consequences

## Positive

* prevents vendor lock-in
* preserves domain ownership
* supports future AI providers
* enables responsible AI governance
* improves testability

---

## Negative

* introduces additional abstraction layers
* requires execution contracts
* requires future provider infrastructure

---

# 7. Testing Implications

The architecture enables:

* in-memory provider testing
* deterministic execution tests
* AI workflow validation
* safety boundary testing

---

# 8. Future Extensions

Future capabilities may include:

* AI quality evaluation
* prompt effectiveness measurement
* reasoning traceability
* model performance analytics
* production provider integrations

---

# 9. Traceability

```
Roadmap v2

        |

        v

Sprint 08 Blueprint

        |

        v

Sprint 08 Backlog

        |

        v

ADR-014

        |

        v

Implementation
```

---

# Decision Outcome

AI execution is established as an application-controlled capability.

The domain remains the owner of learner intelligence.

AI services consume trusted knowledge and assist interactions without becoming the source of learner truth.
