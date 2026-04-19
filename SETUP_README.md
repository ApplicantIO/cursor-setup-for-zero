# Cursor Setup Pack (Portable)

This folder is your reusable Cursor setup pack, extracted from your best workflow in Drug Radar.

Use this pack when you start a new project and want Cursor to:

1. Ask project-specific intake questions first
2. Select only relevant rules/skills/docs/memorybank parts
3. Remove unrelated setup pieces
4. Finish with a ready-to-build project operating system

---

## Core files in this pack

- `SETUP_MASTER.md` - main orchestration protocol
- `PROJECT_INTAKE_TEMPLATE.md` - structured intake questions
- `RULE_SKILL_MATRIX.yaml` - selection logic for rules and skills
- `MODULE_CATALOG.md` - source-to-target mapping for copied modules
- `SETUP_DEPENDENCY_MAP.md` - dependency graph and integrity rules
- `MISSING_CAPABILITY_PROTOCOL.md` - fallback flow when required modules are unavailable
- `MEMORYBANK_BLUEPRINT.md` - memory-bank structure and templates
- `DOCS_BLUEPRINT.md` - docs skeleton and required sections
- `DOCS_SYSTEM_PLAYBOOK.md` - senior-grade docs architecture rules
- `DOCS_REVIEW_CHECKLIST.md` - docs quality gate before implementation
- `SETUP_EXECUTION_CHECKLIST.md` - done criteria
- `ADOPT_SETUP_PROMPT.md` - copy-paste prompt for Cursor in any new project

---

## Setup sources currently wired

- `cursor-memory-bank-main/` (workflow + memory-bank rules/commands)
- `cursor-security-rules-main/` (secure coding rules)
- `rules-design-bible/` (UI/UX and design quality rules)
- `cursor-skills-main/` (cross-domain Cursor best practices and templates)
- `awesome-cursorrules-main/` (extra optional rule references)

---

## Recommended usage in a new project

1. Copy this entire setup pack (or keep it as a shared reference folder).
2. Open the target project in Cursor.
3. Paste the contents of `ADOPT_SETUP_PROMPT.md` into chat.
4. Answer intake questions.
5. Let Cursor apply only relevant parts into target project `.cursor/`, `memory-bank/`, and `docs/`.
6. Run final checklist from `SETUP_EXECUTION_CHECKLIST.md`.

---

## Note

This pack is intentionally modular. It is not "copy everything"; it is "adapt by context".
