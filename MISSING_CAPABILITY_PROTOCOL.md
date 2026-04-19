# Missing Capability Protocol

Use this protocol when the setup pack does not contain the rules, skills, templates, or docs needed for the target project.

## Goal

Do not silently skip missing capabilities. Detect, report, recommend external sources, and retry adoption after import.

## Detection

A capability is "missing" when at least one of these is true:

1. Required module in `RULE_SKILL_MATRIX.yaml` has no matching source file.
2. Source exists but cannot satisfy requested stack/domain needs.
3. Required file path from `MODULE_CATALOG.md` is unavailable.

## Required behavior

When missing capability is detected, the agent must:

1. Continue with available modules (partial adoption is allowed).
2. Produce a "Missing Capabilities Report" with:
   - capability name
   - why it is needed
   - what is currently available
   - exact missing files/modules
3. Recommend how to fill the gap:
   - add local files manually
   - import from a GitHub repository
   - provide team/internal documentation
4. Ask the user whether to:
   - continue with limited setup
   - pause and import missing sources
5. If user provides new sources, re-run selection and cleanup.

## Missing Capabilities Report format

Use this exact format:

```text
Missing capability: <name>
Needed for: <feature/risk/domain>
Missing now: <file/module patterns>
Current fallback: <what is still possible>
Recommended source: <github/local/internal docs>
Action required from user: <what to add>
```

## Final status contract

Setup output must contain these sections:

1. `Applied`
2. `Missing (needs external source)`
3. `Pending user import`
4. `Deferred by user`

If section (2) is non-empty, setup cannot be marked "fully complete".
