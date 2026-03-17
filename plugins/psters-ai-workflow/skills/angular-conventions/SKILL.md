---
name: angular-conventions
description: Frontend conventions for Angular projects: standalone components, features, error capture, styles. Use when implementing or reviewing code in Angular frontends.
---

# Angular Conventions

When working in `frontend/` (or Angular app root), follow these conventions:

- **Structure**: Feature-based; standalone components only. `core/`, `shared/`, `features/<feature>/` with components, services, models, `*-routes.ts`. Kebab-case files; PascalCase classes.
- **Error capture**: All errors must be captured: use centralized error capture in RxJS pipes, and wrap try/catch with error capture. See project rules for error-capture patterns.
- **User-facing text**: All in English.
- **Build**: Run `npm run build` after implementation.
- **Lazy loading**: Use loadComponent/loadChildren for feature routes.

Reference project rules and structure docs for full details.
