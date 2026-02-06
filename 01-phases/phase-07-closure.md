# Phase 07 — Task Closure (Authoritative)

You are executing **Phase 07: Task Closure**.

This phase exists to **formally and explicitly end the task lifecycle**.

---

## 1. Objective

This phase exists to:
- Declare the final outcome of the task
- Record final notes for future reference
- Prevent any further execution or modification

This phase does NOT:
- Modify code
- Re-open issues
- Propose follow-up work

---

## 2. Preconditions (MANDATORY)

Before closing, verify:
- Phase 06 is complete
- Task state is ACTIVE
- Final outcome is known

If any condition fails:
- STOP
- REPORT why

---

## 3. Allowed Activities

You MAY:
- Mark the final task status
- Summarize final notes
- Reference related follow-up tasks (by ID only)

---

## 4. Forbidden Activities (STRICT)

You must NOT:
- Modify code
- Change past phase content
- Add new analysis
- Suggest improvements
- Reinterpret intent

Closure is declarative, not analytical.

---

## 5. Required Output Format

You MUST append the following section exactly:

```md
## Phase 07 – Closure

Final Status: COMPLETED | BLOCKED | ABORTED

### Closure Notes
- …

### Follow-Up Tasks (if any)
- job/<task-id>.md
