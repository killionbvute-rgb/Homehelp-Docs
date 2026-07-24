# Homehelp RICEFW Catalogue

## 1. Introduction

The Homehelp RICEFW Catalogue provides an inventory of custom-developed capabilities within the platform.

The concept is adapted from enterprise software implementation practices and provides structured visibility of:

* custom functionality
* workflows
* interfaces
* reports
* future extensions

The purpose is traceability.

> Every capability should have a purpose, owner, and architectural home.

---

# 2. RICEFW Classification

Homehelp uses the following classification:

| Category | Meaning                              |
| -------- | ------------------------------------ |
| R        | Reports and Analytics                |
| I        | Interfaces and Integrations          |
| C        | Data Conversion                      |
| E        | Enhancements and Domain Capabilities |
| F        | Forms and Documents                  |
| W        | Workflows                            |

---

# 3. Current RICEFW Inventory

## Enhancements (E)

Current implemented capabilities:

| Object                     | Description                          | Location        |
| -------------------------- | ------------------------------------ | --------------- |
| LearnerProfile Aggregate   | Represents learner understanding     | packages/domain |
| DiscoverySession Aggregate | Manages learner discovery process    | packages/domain |
| LearnerName Value Object   | Validates learner identity data      | packages/domain |
| GradeLevel Value Object    | Represents learner grade information | packages/domain |

---

# 4. Workflow Objects (W)

Current workflows:

| Object                              | Description                         | Location             |
| ----------------------------------- | ----------------------------------- | -------------------- |
| CompleteDiscoverySession            | Completes learner discovery journey | packages/application |
| GenerateLearnerProfileFromDiscovery | Creates learner profile             | packages/application |

---

# 5. Interface Objects (I)

Current / Planned:

| Object                | Description                  | Status      |
| --------------------- | ---------------------------- | ----------- |
| Homehelp API          | External communication layer | Implemented |
| AI Service Interface  | AI capability boundary       | Planned     |
| Messaging Integration | Parent communication         | Planned     |

---

# 6. Reports (R)

Future reporting capabilities:

| Object                            | Purpose                             |
| --------------------------------- | ----------------------------------- |
| Learner Insight Report            | Present learner understanding       |
| Learning Progress Report          | Track learner development           |
| Parent Summary Report             | Communicate learner insights        |
| Institutional Analytics Dashboard | Provide organisational intelligence |

---

# 7. Data Conversion Objects (C)

Future data capabilities:

| Object              | Purpose                             |
| ------------------- | ----------------------------------- |
| Learner Data Import | Import existing learner information |
| Migration Tools     | Support institutional adoption      |

---

# 8. Forms (F)

Future documents:

| Object                   | Purpose                       |
| ------------------------ | ----------------------------- |
| Learner Profile Document | Share learner understanding   |
| Parent Report            | Communicate progress          |
| Learning Plan Document   | Capture personalised learning |

---

# 9. Object Naming Convention

Homehelp objects should follow:

```text
Capability + Purpose
```

Examples:

```text
GenerateLearnerProfile

CompleteDiscoverySession

LearnerInsightReport
```

---

# 10. Ownership

Each RICEFW object should have:

* business owner
* technical owner
* documentation reference
* test coverage

---

# 11. Lifecycle Management

Objects move through:

```text
Idea

 |

Design

 |

Development

 |

Testing

 |

Production

 |

Improvement
```

---

# 12. Conclusion

The RICEFW catalogue ensures that Homehelp capabilities remain visible, controlled, and maintainable.

The objective is not documentation for its own sake.

The objective is institutional knowledge preservation.

> What we build must be understood, governed, and improved.
