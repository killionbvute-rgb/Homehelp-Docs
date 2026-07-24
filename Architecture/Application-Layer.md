# Homehelp Application Layer Architecture

## 1. Introduction

The Application Layer coordinates the workflows of the Homehelp institution.

It connects external interactions with domain capabilities.

The Application Layer does not contain core educational knowledge.

Instead, it orchestrates activities by using domain models.

The guiding principle:

> The application layer coordinates. The domain layer understands.

---

# 2. Architectural Role

The Application Layer sits between the API and Domain layers.

```text id="s9f5v2"
API Layer

      |

      v

Application Layer

      |

      v

Domain Layer
```

---

# 3. Responsibilities

The Application Layer is responsible for:

## Use Case Execution

Executing institutional workflows.

Examples:

* Start Discovery Session
* Complete Discovery Session
* Generate Learner Profile

---

## Workflow Coordination

Managing the sequence of actions required to complete a business process.

Example:

```text id="sv2j89"
Complete Discovery

        |

Validate Session

        |

Complete Discovery Aggregate

        |

Generate Learner Profile

        |

Return Result
```

---

## Dependency Management

The Application Layer coordinates:

* repositories
* domain objects
* external services

---

# 4. What Does Not Belong Here

The Application Layer should not contain:

* learner rules
* educational decisions
* domain policies
* database logic

Those belong elsewhere.

---

# 5. Relationship With Domain Layer

The Application Layer uses domain capabilities.

Example:

```text id="x9v3r0"
CompleteDiscoverySession Use Case

              |

              v

DiscoverySession Aggregate

              |

              v

Domain Event
```

The domain remains responsible for correctness.

---

# 6. Relationship With API Layer

The API invokes application use cases.

Example:

```text id="0d7v9m"
HTTP Request

      |

      v

Controller

      |

      v

Use Case

      |

      v

Response
```

The API does not know domain details.

---

# 7. Current Use Cases

## Complete Discovery Session

Purpose:

Finalize a learner discovery journey.

Responsibilities:

* validate discovery session
* complete discovery
* trigger next steps

---

## Generate Learner Profile From Discovery

Purpose:

Create learner understanding from completed discovery.

Responsibilities:

* transform discovery information
* create LearnerProfile
* persist learner knowledge

---

# 8. Application Contracts

The Application Layer defines contracts for infrastructure.

Examples:

```text id="6p2x9v"
Repository Interfaces

Use Case Interfaces

Service Contracts
```

This prevents dependency on technical implementations.

---

# 9. Error Handling

Application workflows should return meaningful results.

Current approach supports:

* Result pattern
* Either pattern
* explicit failures

This avoids uncontrolled exceptions.

---

# 10. Future Application Services

Future capabilities may include:

## Learning Journey Service

Managing personalised learning plans.

---

## Insight Generation Service

Coordinating AI-generated insights.

---

## Parent Communication Service

Managing family interactions.

---

## Progress Intelligence Service

Supporting learner growth tracking.

---

# 11. Architectural Benefits

The Application Layer provides:

## Clear Workflows

Business processes are explicit.

---

## Testability

Use cases can be tested independently.

---

## Flexibility

Interfaces allow infrastructure changes.

---

# 12. Conclusion

The Application Layer represents the operational processes of Homehelp.

It transforms institutional intentions into executable workflows while keeping educational intelligence protected inside the Domain Layer.

> Application coordinates. Domain governs.
