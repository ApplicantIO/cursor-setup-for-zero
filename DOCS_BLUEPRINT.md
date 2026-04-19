# Docs Blueprint

Create this baseline docs structure in target project:

```text
docs/
  README.md
  project-description/
    README.md
    Project-Overview.md
    User-Scenarios.md
    Platform-Flow.md
    Roadmap.md
    Screens-List.md
    Data-Structure.md
    Glossary.md
    Data-Sharing-Export.md
  architecture/
    README.md
    System-Overview.md
    System-Architecture.md
    Tech-Stack.md
    API-Design.md
    Database-Schema.md
    Detection-Scoring.md
    Security.md
    Testing-Strategy.md
    Deployment.md
    Env-Examples.md
  development/
    README.md
    Development-Setup.md
```

## Minimum content contract

### `docs/README.md`
- Single source of truth statement
- Folder responsibilities
- "Read first" file order for AI and humans

### `docs/project-description/Project-Overview.md`
- Problem statement
- Target users
- Success metrics
- Scope boundaries

### `docs/project-description/User-Scenarios.md`
- 3-10 key user flows
- Inputs, outputs, failure states

### `docs/project-description/Platform-Flow.md`
- End-to-end sequence from login to core actions
- API/worker touchpoints at a high level
- Data and security notes

### `docs/project-description/Roadmap.md`
- Phase-by-phase plan (Phase 1..N)
- For each phase: goal, tasks, verification
- Cross-links to architecture/testing/deployment docs

### `docs/project-description/Screens-List.md`
- Screen inventory and purpose
- Inputs, actions, states (loading, empty, error)

### `docs/project-description/Data-Structure.md`
- Main entities and relationships in product language

### `docs/project-description/Data-Sharing-Export.md`
- How external organizations consume data
- Dashboard vs export/API access policy

### `docs/architecture/System-Overview.md`
- Components and responsibilities
- Data flow and integration map

### `docs/architecture/System-Architecture.md`
- Architecture diagram (text or mermaid)
- Component roles and boundaries

### `docs/architecture/Tech-Stack.md`
- Runtime, framework, DB, infra, tooling
- Rationale for each major choice

### `docs/architecture/API-Design.md`
- Endpoint groups
- Auth and error model
- Versioning approach
- Pagination and conventions

### `docs/architecture/Database-Schema.md`
- Core entities and relationships
- Constraints and indexing strategy

### `docs/architecture/Detection-Scoring.md`
- Signal components and formula
- Scoring bands and test expectations

### `docs/architecture/Security.md`
- Threats, controls, secrets handling
- Input validation and permission model
- Phase-based security verification checklist

### `docs/architecture/Testing-Strategy.md`
- Unit, integration, e2e scope
- Quality gates and CI expectations

### `docs/architecture/Deployment.md`
- Build, run, secrets, HTTPS, monitoring, backup
- Operations runbook basics

### `docs/architecture/Env-Examples.md`
- Environment variable examples by domain
- Development vs production separation

### `docs/development/Development-Setup.md`
- Local setup steps
- Run/test/lint commands
- Environment variable guide
- Common issues and E2E smoke path

## Cross-reference requirements

Every project must maintain these links:

1. `Project-Overview.md` <-> `Roadmap.md` (success and scope)
2. `Roadmap.md` <-> `Testing-Strategy.md` (verification)
3. `Roadmap.md` <-> `Security.md` (security checkpoints)
4. `Roadmap.md` <-> `Deployment.md` (operational phases)
5. `Development-Setup.md` <-> `Env-Examples.md` (runability)

## Authoring rule

Docs are living system artifacts; update them when architecture or scope changes.
