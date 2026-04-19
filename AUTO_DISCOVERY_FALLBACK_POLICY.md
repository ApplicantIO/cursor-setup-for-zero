# Auto-Discovery Fallback Policy

Use this policy when the user cannot provide enough technical intake details.

## Goal

Allow setup to continue safely for junior or non-technical users without forcing hard-stop questionnaires.

## Trigger conditions

Auto-discovery is allowed only when at least one is true:

1. User explicitly says they do not know technical details.
2. Two intake attempts still leave required fields incomplete.
3. User requests "you decide/research and continue."

## Safe execution mode

When triggered, the agent must:

1. Run minimal project discovery (stack, project type, probable architecture, UI presence).
2. Produce a draft profile with confidence labels:
   - High
   - Medium
   - Low
3. List assumptions explicitly.
4. Ask confirmation only for critical gates before full apply:
   - language/framework family
   - backend/frontend presence
   - security sensitivity
   - required exclusions

## Apply strategy

- If critical gates are confirmed: continue normal setup flow.
- If critical gates are not confirmed: apply limited safe baseline only.
- Never apply high-impact optional modules on low-confidence assumptions.

## Required output format

When fallback is used, final output must include:

1. `Discovery summary`
2. `Assumptions`
3. `Confidence`
4. `Needs user confirmation`
5. Standard setup status:
   - `Applied`
   - `Missing (needs external source)`
   - `Pending user import`
   - `Deferred by user`

## Completion rule

Setup cannot be marked "fully complete" if unresolved low-confidence critical gates remain.
