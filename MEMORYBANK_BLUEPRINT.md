# Memory Bank Blueprint

Initialize this structure in target project root:

```text
memory-bank/
  tasks.md
  activeContext.md
  progress.md
  archive/
  creative/
```

## File intent

- `tasks.md`: active and queued work items
- `activeContext.md`: current objective, assumptions, blockers
- `progress.md`: changelog-style progress notes
- `creative/`: design/architecture explorations
- `archive/`: completed task records and lessons learned

## Starter template - tasks.md

```markdown
# Tasks

## Current
- [ ] TASK-001: <short title>

## Next
- [ ] TASK-002: <short title>

## Done
- [x] TASK-000: Setup initialized
```

## Starter template - activeContext.md

```markdown
# Active Context

- Current objective:
- Why now:
- In scope:
- Out of scope:
- Constraints:
- Current branch:
- Next action:
```

## Starter template - progress.md

```markdown
# Progress Log

## YYYY-MM-DD
- Initialized project setup
- Applied selected rules and docs skeleton
- Open items: <list>
```

## Rules for maintenance

1. Keep entries concise and current.
2. Archive completed tasks instead of deleting history.
3. Update `activeContext.md` when objective changes.
4. Use same task IDs across docs and PR notes.
