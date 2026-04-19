# Setup Dependency Map

This file defines required and optional dependencies between setup modules.

## Core dependency graph

1. `ADOPT_SETUP_PROMPT.md`
   - requires:
     - `SETUP_MASTER.md`
     - `PROJECT_INTAKE_TEMPLATE.md`
     - `RULE_SKILL_MATRIX.yaml`
     - `SETUP_EXECUTION_CHECKLIST.md`
   - conditionally requires:
     - `MEMORYBANK_BLUEPRINT.md` (if memory-bank workflow enabled)
     - `DOCS_BLUEPRINT.md` (if docs generation enabled)
     - `DOCS_SYSTEM_PLAYBOOK.md` (if docs generation enabled)
     - `DOCS_REVIEW_CHECKLIST.md` (if docs generation enabled)
     - `MODULE_CATALOG.md` (if source-to-target module copy is performed)

2. `SETUP_MASTER.md`
   - requires:
     - `RULE_SKILL_MATRIX.yaml`
     - `SETUP_EXECUTION_CHECKLIST.md`
   - conditionally requires:
     - `MEMORYBANK_BLUEPRINT.md`
     - `DOCS_BLUEPRINT.md`
     - `DOCS_SYSTEM_PLAYBOOK.md`
     - `DOCS_REVIEW_CHECKLIST.md`
     - `MODULE_CATALOG.md`

3. `SETUP_EXECUTION_CHECKLIST.md`
   - requires:
     - `PROJECT_INTAKE_TEMPLATE.md`
     - `RULE_SKILL_MATRIX.yaml`
   - should verify:
     - docs quality via `DOCS_REVIEW_CHECKLIST.md`
     - source-target mapping via `MODULE_CATALOG.md`

## Integrity rules

1. If `docs/` is created, both `DOCS_BLUEPRINT.md` and `DOCS_SYSTEM_PLAYBOOK.md` must be used.
2. If `memory-bank/` is created, `MEMORYBANK_BLUEPRINT.md` must be used.
3. If rule modules are copied, `RULE_SKILL_MATRIX.yaml` and `MODULE_CATALOG.md` must both be used.
4. Setup is incomplete if any required dependency above is skipped.
