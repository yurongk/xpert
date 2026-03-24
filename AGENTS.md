# AGENTS Guide for Xpert

This repository uses **NestJS + TypeORM** on the backend and **Angular 17+** (standalone components, signals, new control flow) on the frontend. Follow these guidelines when extending the codebase.

---

## General Guidelines

- **Search**: Prefer `rg` (ripgrep) for code search
- **Encoding**: Keep edits ASCII-compatible
- **Preservation**: Do not revert user changes without explicit instruction
- **UI Framework**: Avoid Angular Material (deprecated in this project). Use **Angular CDK + TailwindCSS v3** for UI components
  - ⚠️ Do not import `@angular/material` modules in new code
- **Angular Patterns**:
  - Use **standalone components** with signals
  - Use new control flow syntax: `@for`, `@if`, `@switch`
  - Use **reactive forms**
  - Keep templates **Tailwind-first**
- **Comments**: Keep them succinct; add only when clarifying non-obvious logic

---

## Backend (NestJS)

### Architecture Patterns

- **Entities**: Place in `packages/server-ai/src/**`
- **Services**: Extend `TenantOrganizationAwareCrudService` or appropriate base classes
- **Controllers**: Extend `CrudController` when possible
- **Modules**: Register in `packages/server-ai/src/index.ts` and wire into `app.module.ts` as needed

### Data Layer

- Keep **TypeORM entities** aligned with contract interfaces in `packages/contracts`
- Complex, independent logic can be implemented using **CQRS pattern**

---

## Frontend (Angular)

### Service Layer

- Services live in `apps/cloud/src/app/@core/services`
- Export services via the barrel file

### Feature Modules

- New settings pages belong under `apps/cloud/src/app/features/setting/**`
- Use **standalone components** and **lazy routing files** exporting `routes`

### State Management

- Use signals/models for state
- Prefer `getAllInOrg` patterns for organization-scoped data

### Styling

- **Tailwind utility classes** in templates
- **SCSS** only for minimal host-level tweaks
- Use translate for all user-facing text in HTML
- Support **light/dark modes** via Tailwind CSS classes

---

## API Endpoints

### Server Skill Repositories

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/skill-repository` | Register a skill repository |
| GET | `/skill-repository` | List all repositories |
| POST | `/skill-repository/indexes` | Index repositories |
| POST | `/skill-repository/sync/:repositoryId` | Sync a specific repository |

### Client Integration

- Match client services to these REST shapes
- Keep organization/tenant context via base services

---

## Testing & Validation

- Run **targeted tests** when possible; otherwise document when tests are not run
- Validate forms with Angular `Validators`
- Show errors via **Toastr** and `getErrorMessage` utility

---

## UX Guidelines

- Follow the **bold, terminal-inspired aesthetic** used in the skill repository page:
  - Gradient shells
  - Code-like cards
  - Clear CTAs
- Provide **loading/empty states** for all async operations
- Support **search/filter/sort** when dealing with lists
