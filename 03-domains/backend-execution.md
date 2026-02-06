# Domain Rules — Backend Execution (Authoritative)

You are operating in the **Backend domain**.

Your reasoning and actions must be grounded in **runtime execution**, not static code structure.

---

## 1. Execution-First Rule (CRITICAL)

Before proposing, planning, or implementing any backend change, you must reason about:

- Request entry point
- Controller execution
- Service execution
- Database interactions
- Side effects
- Response construction

You must reason in terms of:
- State before execution
- State during execution
- State after execution

Line-by-line code reading is insufficient.

---

## 2. Mandatory Execution Simulation

You must explicitly identify:

- Which code paths execute
- Which branches are skipped
- Which validations run
- Which database queries execute
- Which transactions open/commit/rollback

If execution flow cannot be determined:
- Mark it as UNKNOWN
- Do NOT assume behavior

---

## 3. State-Based Reasoning

You must reason about:

- Request data (params, body, query)
- Persisted database state
- In-memory state changes
- Side effects (writes, events, logs)

Variables must be treated as **values changing over time**, not static declarations.

---

## 4. Database Discipline

You must NOT:
- Assume schema shape
- Assume constraints
- Assume transaction boundaries

All DB-related statements must be based on:
- Observed entities
- Declared migrations
- Explicit queries

If database behavior is unclear:
- Say so
- Block execution if critical

---

## 5. Error Handling & Edge Cases

You must explicitly reason about:

- Validation failures
- Empty results
- Null/undefined values
- Transaction failures
- Partial updates

Silent failure paths must be surfaced.

---

## 6. Forbidden Backend Assumptions

You must NOT assume:

- Controllers are thin
- Services own business logic
- Repositories are pure data access
- Global error handling exists
- Idempotency is guaranteed

Only what is declared or observed is valid.

---

## 7. Output Discipline (Backend Reasoning)

When explaining backend behavior, you must use one of:

- Step-by-step execution trace
- State transition table
- Request → Response timeline

Implicit reasoning is not acceptable.

---

## 8. Backend Scope Boundaries

Backend execution scope includes:
- API handlers
- Services
- Database interactions

It excludes:
- UI concerns
- Network infrastructure
- External systems (unless explicitly included)

---

## Final Instruction

Backend correctness comes from understanding execution flow,
not from following patterns.

If you cannot simulate the runtime accurately,
you must stop and report uncertainty.
