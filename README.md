# Cursor Setup OS (v1-lite)

Portable setup pack for bootstrapping new projects in Cursor with a structured flow:

`Intake -> Select -> Adopt -> Cleanup -> Validate`

## Who this is for

- Teams and solo builders who want a repeatable Cursor project setup.
- Engineers who need project-fit rules/docs/memory-bank, not copy-all templates.
- Senior developers who prefer fast onboarding with explicit constraints.

## Who this is not for

- One-file throwaway experiments.
- Projects that do not need structured docs/rules/workflow.

## What it does

- Adapts setup to project stack and scope (not copy-all).
- Applies relevant rules, docs, and memory-bank structure.
- Cleans irrelevant modules.
- Reports missing capabilities and asks for external sources when needed.

## Requirements

> [!IMPORTANT]
> Best experience: **Cursor Pro (or higher)**.  
> Free tier may run out of credits before full setup/adoption completes on medium-large projects.

## Folder-name independence

This setup is folder-name independent for end users. They can clone this repository under any local directory name, open the repository root in Cursor, and run the same setup flow.

## Known limitations

- Free-tier credits may not be enough for full adoption on larger projects.
- Very large source packs can require limited-mode intake first, followed by iterative expansion.
- Some imported packs are broad community references and should be selectively applied via the matrix/checklist flow.

## 2-minute quick start

1. Open target project in Cursor.
2. Copy/paste `ADOPT_SETUP_PROMPT.md` into chat.
3. Answer intake questions (or provide a free-form expert brief).
4. Review include/exclude plan.
5. Let setup apply selected modules.
6. Confirm validation via `SETUP_EXECUTION_CHECKLIST.md`.

## Flexible intake (optional, not mandatory)

- You can answer structured intake questions from `PROJECT_INTAKE_TEMPLATE.md`.
- Or you can provide a short expert brief in your own style.
- Setup extracts required fields (stack, scope, security, UX, include/exclude intent) from either mode.
- If information is unclear, setup asks only critical follow-up questions.
- If some fields remain unknown, setup continues in limited mode and reports assumptions.
- If user cannot provide technical details, setup can trigger guarded auto-discovery via `AUTO_DISCOVERY_FALLBACK_POLICY.md`.

## 30-second demo flow

1. Open a new project in Cursor.
2. Paste `ADOPT_SETUP_PROMPT.md` into chat.
3. Answer intake in 3-6 short replies (stack, scope, constraints).
4. Cursor generates include/exclude plan and applies only relevant modules.
5. Cursor returns final status: `Applied`, `Missing`, `Pending user import`, `Deferred by user`.

## Core files

- `SETUP_MASTER.md` - orchestration
- `PROJECT_INTAKE_TEMPLATE.md` - intake questions
- `RULE_SKILL_MATRIX.yaml` - profile-based selection
- `MODULE_CATALOG.md` - source -> target mapping
- `SETUP_DEPENDENCY_MAP.md` - dependency integrity
- `MISSING_CAPABILITY_PROTOCOL.md` - gap fallback flow
- `AUTO_DISCOVERY_FALLBACK_POLICY.md` - safe research/plan fallback for incomplete intake
- `SETUP_EXECUTION_CHECKLIST.md` - done gates
- `DOCS_BLUEPRINT.md` / `DOCS_SYSTEM_PLAYBOOK.md` / `DOCS_REVIEW_CHECKLIST.md`
- `MEMORYBANK_BLUEPRINT.md`

## Missing capability behavior

If required modules are unavailable, setup must:

- continue partial adoption,
- generate Missing Capabilities Report,
- recommend external sources (GitHub/local/internal),
- re-run selection after import.

Final status must include:

- `Applied`
- `Missing (needs external source)`
- `Pending user import`
- `Deferred by user`

## Included source packs

- `cursor-memory-bank-main/`
- `cursor-security-rules-main/`
- `rules-design-bible/`
- `cursor-skills-main/`
- `awesome-cursorrules-main/`

## Sources and credits

This setup is built by adapting ideas, rules, and structures from community resources, including:

- [PatrickJS/awesome-cursorrules](https://github.com/PatrickJS/awesome-cursorrules)
- [vanzan01/cursor-memory-bank](https://github.com/vanzan01/cursor-memory-bank)
- [matank001/cursor-security-rules](https://github.com/matank001/cursor-security-rules)
- [araguaci/cursor-skills](https://github.com/araguaci/cursor-skills)
- [saralobo/rules-design-bible](https://github.com/saralobo/rules-design-bible)
- Other Cursor community rule/skills references ("and others")

### Attribution note

- This repository combines, adapts, and organizes external sources into a project-oriented setup workflow.
- Please review upstream licenses and attribution requirements before redistribution or commercial use.
