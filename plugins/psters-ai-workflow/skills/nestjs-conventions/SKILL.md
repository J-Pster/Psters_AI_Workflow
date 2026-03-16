---
name: nestjs-conventions
description: Backend conventions for NestJS projects: modular architecture, DTO validation, and migration safety.
---

# NestJS Conventions

**When to use:** Working in NestJS backend codebases.

**Workflow:** Apply these conventions consistently:
- **Architecture:** Feature-based modules with focused controllers and services.
- **DTOs:** Use DTOs with validation decorators for request/response contracts.
- **Separation of concerns:** Keep business rules in services, not controllers.
- **Configuration:** Use typed configuration; avoid hardcoded sensitive values.
- **Errors:** Keep exception handling consistent; user-facing text clear.
- **Migrations:** When TypeORM is in use, generate migrations via CLI; keep schema changes deterministic.

**Constraints:** Follow project rules for TypeORM, error handling, and commit format.
