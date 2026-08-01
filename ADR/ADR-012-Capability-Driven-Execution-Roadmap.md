# ADR-012 — Capability-Driven Execution Roadmap

## Status

Accepted

## Date

2026-08-01

## Context

The initial Homehelp execution roadmap was organised primarily around sprint sequencing.

While effective during early foundation development, the sprint-driven model created limitations:

- Capabilities could span multiple sprints.
- Strategic capabilities could be introduced earlier when implementation learning required it.
- Product evolution required flexibility without losing governance traceability.

## Decision

Homehelp adopts a capability-driven execution roadmap.

Capabilities represent long-lived product value.

Sprints represent delivery increments used to implement, validate and evolve capabilities.

The authoritative roadmap becomes:

Product-Execution-Roadmap-v2.md

## Capability Governance Model

Every implementation change should trace:

Business Capability
→ Domain Capability
→ Bounded Context
→ Aggregate / Entity
→ Application Workflow
→ Tests
→ Documentation Evidence

## Consequences

Positive:

- Greater strategic flexibility.
- Better alignment with Domain-Driven Design.
- Easier prioritisation.
- Improved traceability.

Trade-offs:

- Requires stronger documentation discipline.
- Requires regular roadmap governance reviews.

## Impact on Existing Work

Existing implementations are mapped into capabilities rather than being restricted by their original sprint allocation.

Examples:

Sprint 05 Parent Trust implementation contributes to:

- Parent Trust and Explainability capability.
- Human Feedback capability.
- Responsible AI capability.

## Governance Requirements

Future capability changes require:

- ADR updates where architectural decisions change.
- DDR updates where domain boundaries change.
- Traceability Matrix updates.
- Roadmap version updates.

## Conclusion

The capability-driven roadmap provides Homehelp with a sustainable execution model that supports continuous evolution while preserving architectural integrity.

## Capability Portfolio Protection

The capability-driven roadmap preserves strategic capabilities independently of sprint sequencing.

The following capability areas remain protected roadmap commitments:

- Learner Understanding Foundation
- Learner Knowledge Evolution
- Conversation Intelligence
- AI Prompt Engine and Intelligence Orchestration
- Learner Intelligence
- Parent Trust and Explainability
- Visual Learning Support
- Learning Progress Intelligence
- Parent Coaching Intelligence
- School Integration
- Multi-Learner Family Support
- Personalised Learning Plans
- Production Excellence and Governance

Capabilities may be delivered in different sprint increments based on learning, dependency discovery, user value and architectural priorities, but roadmap governance must ensure that strategic capability intent is preserved.