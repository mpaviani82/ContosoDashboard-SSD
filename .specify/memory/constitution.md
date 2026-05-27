<!--
Sync Impact Report
Version change: none (initial creation) → 1.0.0
Modified principles: none (new constitution)
Added sections: Additional Constraints, Development Workflow
Removed sections: none
Templates requiring updates: ✅ .specify/templates/plan-template.md
Follow-up TODOs: none
-->

# ContosoDashboard Constitution

## Core Principles

### I. Training-First Clarity
Every design, implementation, and artifact MUST be understandable by learners and maintainers. Training features MUST avoid production-only complexity and MUST document known simplifications, intentional gaps, and educational assumptions.

### II. Spec-Driven Delivery
All work MUST begin from a concrete `spec.md` artifact before implementation. Every feature change MUST trace back to a defined user story, acceptance criteria, or requirement in the spec.

### III. Test-First Validation
Behavioral tests MUST be defined before implementation. Each change MUST include unit or integration coverage for new behavior, or a documented exception approved during review.

### IV. Observability & Traceability
Code and documentation MUST expose execution intent, success/failure conditions, and decision rationale. Logs, errors, telemetry, and architecture notes MUST support debugging and learning without hidden internal behavior.

### V. Incremental Simplicity
Deliver the smallest viable slice first. Features MUST be decomposed into independently testable, independently deployable increments; added complexity is only acceptable when it directly supports a validated user need.

## Additional Constraints
This project is a training-oriented application. Dependencies MUST be local-friendly, cloud integrations MUST be optional abstractions, and production-grade infrastructure may be deferred unless required for an explicit learning objective.

## Development Workflow
Work MUST follow the repository's spec-driven workflow:
- `spec.md` defines requirements, user stories, and acceptance criteria.
- `plan.md` captures design decisions, architecture, and principle alignment.
- `tasks.md` decomposes work into independently testable stories.
- Compliance with the constitution MUST be re-verified at each phase using `/speckit.plan` and `/speckit.analyze`.

## Governance
This constitution is authoritative for planning, specification, and task generation in this repository.
- Amendments require a documented change in `.specify/memory/constitution.md`.
- Any principle change MUST be paired with an update to affected templates or guidance docs.
- Versioning follows semantic versioning:
  - MAJOR for principle redefinition or removal,
  - MINOR for new principles or mandatory workflow changes,
  - PATCH for clarifications and editorial updates.
- Compliance reviews MUST occur before `/speckit.implement` and after `/speckit.plan` or `/speckit.tasks` changes.
**Version**: 1.0.0 | **Ratified**: 2026-05-26 | **Last Amended**: 2026-05-26
