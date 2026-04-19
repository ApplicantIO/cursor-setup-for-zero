# Docs System Playbook (Senior-Grade)

This playbook captures why Drug Radar docs are strong and how to reproduce that quality in other projects.

## Why this docs system works

1. Clear separation of concerns:
   - `project-description/` = what and why
   - `architecture/` = how
   - `development/` = how to run
2. One source of truth per concern (no duplicated definitions).
3. Phase-driven roadmap linked to implementation and verification.
4. Strong cross-links between product, architecture, testing, and operations.
5. Explicit MVP vs out-of-scope boundaries to prevent scope drift.

## Mandatory docs design rules

1. Every critical statement must have an owner document.
2. Every phase must include:
   - Goal
   - Tasks
   - Verification criteria
   - References
3. Product docs must not contain implementation detail.
4. Architecture docs must include constraints, not just ideas.
5. Development docs must be executable by a new engineer in one pass.

## Recommended structure

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

## Cross-link contract

- `Project-Overview.md` must link to roadmap success criteria.
- `Roadmap.md` must link to setup, testing, security, deployment references.
- `Testing-Strategy.md` must link to acceptance criteria in roadmap.
- `Security.md` must link to phase checks and env handling.
- `Development-Setup.md` must link to environment examples and deploy docs.

## Quality gates for docs

Before setup is considered complete:

1. Navigation gate:
   - README files exist at `docs/`, `project-description/`, `architecture/`, `development/`
2. Coverage gate:
   - Product, architecture, development topics all present
3. Consistency gate:
   - Terminology is aligned (same terms in all files)
4. Verification gate:
   - Each roadmap phase has measurable outcome
5. Freshness gate:
   - No placeholder text in critical files

## Anti-patterns to avoid

- Single huge README for everything
- Product and implementation mixed in one file
- Roadmap without acceptance criteria
- Security/testing isolated from roadmap
- Docs that explain but cannot be executed
