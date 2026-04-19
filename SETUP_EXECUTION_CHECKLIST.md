# Setup Execution Checklist

Use this to confirm setup is ready.

## Intake completed

- [ ] Intake captured (structured template or free-form expert brief)
- [ ] Setup mode selected: `minimal | standard | strict`
- [ ] Mandatory inclusions/exclusions confirmed with user
- [ ] Required fields extracted (stack, scope, security, UX, include/exclude intent)
- [ ] Assumptions documented for unknown fields (if any)
- [ ] Auto-discovery fallback used only under defined triggers (`AUTO_DISCOVERY_FALLBACK_POLICY.md`)
- [ ] Confidence labels recorded for auto-discovered fields (if fallback used)
- [ ] Critical gates confirmed or explicitly downgraded to limited baseline

## Rules and skills selected

- [ ] Relevant rule families selected via `RULE_SKILL_MATRIX.yaml`
- [ ] Source-target mapping checked via `MODULE_CATALOG.md`
- [ ] Irrelevant language rules removed
- [ ] Security baseline included
- [ ] Design rules included only if UI work exists
- [ ] Memory-bank workflow rules included if agent workflow is desired
- [ ] Missing capability scan completed via `MISSING_CAPABILITY_PROTOCOL.md`

## Project structure initialized

- [ ] `.cursor/rules/` contains only selected rules
- [ ] `memory-bank/` initialized
- [ ] `docs/` skeleton initialized
- [ ] Project master rule (single source of truth) exists

## Cleanup and quality

- [ ] No duplicate rules with conflicting guidance
- [ ] No stale template files unrelated to project
- [ ] Names and paths are consistent
- [ ] Team can understand where truth lives (`docs/`, `memory-bank/`, rules)
- [ ] Docs quality validated with `DOCS_REVIEW_CHECKLIST.md`
- [ ] Dependency integrity validated with `SETUP_DEPENDENCY_MAP.md`
- [ ] Missing Capabilities Report generated (if any gaps found)
- [ ] User decision recorded for each gap (import now / defer / continue limited)

## Done criteria

- [ ] Cursor can start first real feature task with no setup blockers
- [ ] Human teammate confirms setup clarity
- [ ] Final status includes: `Applied`, `Missing (needs external source)`, `Pending user import`, `Deferred by user`
- [ ] Final status includes `Assumptions` (or explicitly states no assumptions)
- [ ] If fallback used, final status includes `Discovery summary` and `Confidence`
