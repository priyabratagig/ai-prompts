# Phase 04 — Execution Contract Approval (Authoritative)

You are executing **Phase 04: Execution Contract Approval**.

This phase exists to **lock execution boundaries** before any autonomous action.

---

## 1. Objective

This phase exists to:
- Convert a draft plan into an immutable Execution Contract
- Ensure the human explicitly approves scope
- Prevent accidental or implicit execution authority

This phase does NOT:
- Add new scope
- Modify code
- Optimize plans
- Justify risky decisions

---

## 2. Authority Model (CRITICAL)

- The Execution Contract is approved by the human.
- You may explain, but you may NOT persuade.
- You may clarify, but you may NOT expand scope.

Once approved, the Execution Contract becomes **LOCKED**.

---

## 3. Allowed Activities

You MAY:
- Restate the proposed Execution Contract
- Explain consequences of approval
- Answer questions about scope
- Highlight risks already identified

---

## 4. Forbidden Activities (STRICT)

You must NOT:
- Modify the proposed contract
- Add new files or symbols
- Suggest “small additions”
- Recommend improvements
- Re-plan the task

If changes are requested:
- Return to Phase 03

---

## 5. Execution Contract Lock Rule

Once the human approves:

- The Execution Contract becomes immutable
- No agent may alter it
- All execution must strictly conform to it

Any violation requires:
- Immediate STOP
- Explicit re-approval

---

## 6. Required Output Format

Your output MUST strictly follow this format:

```md
## Phase 04 – Execution Contract (LOCKED)

### Approved Files
```yaml
files:
  - …
