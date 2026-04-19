# Docs Review Checklist (Before Build Starts)

Use this checklist after docs generation and before implementation.

## A) Structure

- [ ] `docs/README.md` exists and explains source-of-truth ownership
- [ ] `project-description/`, `architecture/`, `development/` all exist
- [ ] Each folder has a local `README.md` with read-order guidance

## B) Product clarity

- [ ] MVP scope is explicit
- [ ] Out-of-scope is explicit
- [ ] Primary users are identified
- [ ] End-to-end flow is documented
- [ ] Roadmap phases have goals and outputs

## C) Engineering clarity

- [ ] Architecture layers are defined
- [ ] API conventions and error format are defined
- [ ] Schema and indexes are documented
- [ ] Security controls are documented
- [ ] Testing strategy maps to roadmap phases

## D) Operational readiness

- [ ] Development setup is reproducible for a new engineer
- [ ] Environment variables have examples
- [ ] Deployment runbook exists
- [ ] Monitoring and backup are documented

## E) Link integrity and consistency

- [ ] Core docs cross-link each other (overview/roadmap/testing/security/deploy)
- [ ] No broken internal links
- [ ] Terms are consistent across docs (glossary-aligned)

## F) Done bar

- [ ] A senior engineer can infer what to build and how to verify it
- [ ] A new engineer can run the project without external verbal guidance
