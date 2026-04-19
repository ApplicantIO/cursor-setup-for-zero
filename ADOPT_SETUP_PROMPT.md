You are onboarding this project using my portable Cursor setup pack.

Follow this protocol exactly:

1) Read these setup files first:
- `SETUP_MASTER.md`
- `PROJECT_INTAKE_TEMPLATE.md`
- `RULE_SKILL_MATRIX.yaml`
- `MODULE_CATALOG.md`
- `SETUP_DEPENDENCY_MAP.md`
- `MISSING_CAPABILITY_PROTOCOL.md`
- `AUTO_DISCOVERY_FALLBACK_POLICY.md`
- `MEMORYBANK_BLUEPRINT.md`
- `DOCS_BLUEPRINT.md`
- `DOCS_SYSTEM_PLAYBOOK.md`
- `DOCS_REVIEW_CHECKLIST.md`
- `SETUP_EXECUTION_CHECKLIST.md`

2) Run intake before creating/editing anything (flexible mode):
- Preferred: ask intake questions from `PROJECT_INTAKE_TEMPLATE.md`.
- Allowed alternative: accept my free-form expert brief and extract required fields.
- Required extracted fields: stack, scope, security level, UX intensity, include/exclude intent.
- If fields are unclear, ask only critical follow-up questions.
- If some fields stay unknown, continue in limited mode and record assumptions explicitly.
- If user cannot provide technical details, apply `AUTO_DISCOVERY_FALLBACK_POLICY.md`.

3) Build a short adoption plan:
- What to include
- What to exclude
- Why
- Source -> target file mapping (from `MODULE_CATALOG.md`)

4) Apply setup into current project:
- Add only relevant `.cursor/rules` modules
- Initialize `memory-bank/` with blueprint templates
- Initialize `docs/` skeleton with blueprint files
- Build docs using playbook standards (separation, cross-links, phase verification)
- Keep existing project-specific content; do not overwrite without asking

5) Clean up:
- Remove irrelevant rules/skills/templates
- Remove duplicates/conflicts
- Keep only project-fit guidance

6) Handle missing capabilities using `MISSING_CAPABILITY_PROTOCOL.md`:
- Detect capability gaps against selected profile
- Continue partial setup where possible
- Produce Missing Capabilities Report
- Recommend external sources (GitHub/local/internal docs)
- Ask user to continue limited setup or import sources first
- Re-run selection when user provides new sources

7) If intake remains incomplete, run auto-discovery fallback using `AUTO_DISCOVERY_FALLBACK_POLICY.md`:
- Perform minimal project discovery and produce draft profile
- Label confidence (`High`/`Medium`/`Low`)
- List assumptions and ask only critical confirmations
- Apply limited safe baseline if confirmations are missing

8) Validate with `SETUP_EXECUTION_CHECKLIST.md` and show final status:
- Completed items
- Remaining items (if any)
- Suggested first implementation task
- Docs review result from `DOCS_REVIEW_CHECKLIST.md`
- Dependency integrity result from `SETUP_DEPENDENCY_MAP.md`
- Missing capabilities status (`Applied`, `Missing`, `Pending user import`, `Deferred by user`)
- Assumptions used during intake/adoption
- Discovery summary and confidence (if fallback mode used)

Important behavior:
- Be selective, not maximal.
- Prefer smallest complete setup.
- Security baseline is mandatory.
- If project has no real UI scope, skip heavy design modules.
