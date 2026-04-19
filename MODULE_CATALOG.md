# Module Catalog (Source -> Target)

This catalog defines where modules come from and where they should be copied in a target project.

## Rules modules

- Source: `cursor-memory-bank-main/.cursor/rules/isolation_rules/**`
  - Target: `.cursor/rules/isolation_rules/**`
  - Use when: agent workflow and structured phase execution are required

- Source: `cursor-security-rules-main/*.mdc`
  - Target: `.cursor/rules/security/*.mdc`
  - Use when: always (language-specific selection required)

- Source: `rules-design-bible/.cursor/rules/*.mdc`
  - Target: `.cursor/rules/design/*.mdc`
  - Use when: UI/UX work is in scope

- Source: project-specific rules (create new)
  - Target: `.cursor/rules/<project-name>.mdc`
  - Use when: defining single source of truth for docs, architecture, and workflow

## Commands modules

- Source: `cursor-memory-bank-main/.cursor/commands/*.md`
  - Target: `.cursor/commands/*.md`
  - Use when: you want `/van`, `/plan`, `/creative`, `/build`, `/reflect`, `/archive`

## Memory bank modules

- Source blueprint: `MEMORYBANK_BLUEPRINT.md`
  - Target: `memory-bank/*`
  - Use when: persistent context and task tracking are needed

## Documentation modules

- Source blueprint: `DOCS_BLUEPRINT.md`
  - Target: `docs/**`
  - Use when: project requires maintainable architecture/product documentation

## Optional knowledge modules

- Source: `cursor-skills-main/**`
  - Target: copy only relevant templates/scripts
  - Use when: specific stack guides or templates are needed

- Source: `awesome-cursorrules-main/rules/**`
  - Target: optional references only
  - Use when: you need extra domain-specific prompts/rules
