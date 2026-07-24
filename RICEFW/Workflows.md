# Homehelp Workflow Catalogue

## 1. Introduction

Workflows represent institutional processes that transform user interactions into meaningful outcomes.

In Homehelp, workflows connect:

* parents
* learners
* application services
* domain capabilities
* future AI intelligence

The guiding principle:

> A workflow transforms intention into value.

---

# 2. Workflow Register

| ID    | Workflow                     | Status      |
| ----- | ---------------------------- | ----------- |
| W-001 | Learner Discovery Journey    | Implemented |
| W-002 | Complete Discovery Session   | Implemented |
| W-003 | Generate Learner Profile     | Implemented |
| W-004 | AI Conversation Intelligence | Planned     |

---

# 3. W-001 Learner Discovery Journey

## Purpose

Understand the learner through structured discovery.

## Trigger

Parent begins learner discovery.

## Process

```text id="v8m2q5"
Parent Starts Discovery

        |

        v

Discovery Session Created

        |

        v

Conversation Information Captured

        |

        v

Discovery Completed

        |

        v

Learner Profile Generated
```

## Outcome

A structured learner understanding record.

---

# 4. W-002 Complete Discovery Session

## Purpose

Move a discovery session from active participation to completion.

## Implementation

```text id="x4n7m9"
packages/application

CompleteDiscoverySession
```

---

## Process

```text id="s6q3p8"
Receive Session Request

        |

        v

Retrieve Session

        |

        v

Validate State

        |

        v

Complete Session

        |

        v

Publish Domain Event
```

---

## Business Value

Ensures learner discovery follows a controlled lifecycle.

---

# 5. W-003 Generate Learner Profile

## Purpose

Transform completed discovery information into learner understanding.

## Implementation

```text id="m9k4v2"
packages/application

GenerateLearnerProfileFromDiscovery
```

---

## Process

```text id="n5x8q3"
Completed Discovery

        |

        v

Extract Learner Information

        |

        v

Create LearnerProfile

        |

        v

Persist Understanding
```

---

## Business Value

Creates the foundation for personalised learning.

---

# 6. W-004 AI Conversation Intelligence

## Status

Planned

## Purpose

Transform natural conversations into structured learner insights.

Future process:

```text id="q7m3x9"
Conversation

       |

       v

AI Processing

       |

       v

Facts Extracted

       |

       v

Domain Validation

       |

       v

Learner Insight
```

---

# 7. Workflow Ownership

Each workflow requires:

* business owner
* technical owner
* process documentation
* test coverage

---

# 8. Workflow Testing

Workflows should verify:

## Correct sequence

Steps happen in the correct order.

---

## Business rules

Invalid actions are prevented.

---

## Recovery

Failures can be handled safely.

---

# 9. Future Workflow Expansion

Potential workflows:

| ID    | Workflow                         |
| ----- | -------------------------------- |
| W-005 | Parent Engagement Journey        |
| W-006 | Learning Recommendation Workflow |
| W-007 | Progress Review Workflow         |
| W-008 | Educator Collaboration Workflow  |

---

# 10. Conclusion

Workflows represent the operational heartbeat of Homehelp.

They transform technical capabilities into meaningful learner experiences.

> Great systems are built around great journeys.
