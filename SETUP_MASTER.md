# SETUP MASTER - Universal Cursor Project Bootstrap

Purpose: Convert this setup pack into a project-specific operating environment with minimal noise.

## Operating principles

1. Intake before action (never copy rules blindly).
2. Keep only relevant rules, skills, memorybank files, and docs.
3. Prefer smallest complete setup over maximal setup.
4. Security and architecture baselines are mandatory.
5. Output must be runnable by humans and AI agents.

## Execution phases

### Phase 0 - Detect project context

Collect:
- Project type (web app, API, mobile, CLI, data/ML, automation, mixed)
- Tech stack (frontend/backend/language/framework)
- Team constraints (security level, compliance, deadlines, team size)
- Product maturity (prototype, MVP, production)
- UX intensity (none/basic/high)
- Agent usage level (low/medium/high autonomy)

### Phase 1 - Build adoption plan

Using `RULE_SKILL_MATRIX.yaml`:
- Choose required modules
- Choose optional modules
- Reject irrelevant modules
- Record why each module was selected or skipped
- Validate source-target copy plan with `MODULE_CATALOG.md`

### Phase 2 - Apply project files

Create/update in target project:
- `.cursor/rules/` with selected `.mdc` files only
- `memory-bank/` from `MEMORYBANK_BLUEPRINT.md`
- `docs/` from `DOCS_BLUEPRINT.md` and `DOCS_SYSTEM_PLAYBOOK.md`
- project-level master rule (single source of truth style)

### Phase 3 - Cleanup and deduplicate

- Remove overlapping or conflicting rules
- Remove rule families unrelated to stack
- Ensure one canonical path for memory-bank and docs
- Keep naming consistent and predictable

### Phase 4 - Verification gate

Pass `SETUP_EXECUTION_CHECKLIST.md`:
- Rule coverage correct
- No obvious irrelevant modules
- Memory-bank initialized
- Docs skeleton initialized
- Docs quality checked via `DOCS_REVIEW_CHECKLIST.md`
- Dependency integrity checked via `SETUP_DEPENDENCY_MAP.md`
- Team can start implementation immediately

## Non-goals

- Do not over-engineer setup for tiny tasks.
- Do not force UI/UX heavy rules into backend-only repos.
- Do not force language-specific security rules for unused languages.

## Quality bar

A setup is "done" only when:
1. Cursor can reason with project context correctly
2. Human teammate can navigate docs and memory-bank quickly
3. First implementation task can begin without setup rework
