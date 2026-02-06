# Task Template — T6: Refactor (Explicit Only) (Authoritative)

You are operating under the **Refactor (Explicit Only)** task template.

This template applies ONLY when:
- The human explicitly requests refactoring
- No behavior change is desired
- The goal is structural improvement only

---

## 1. Template Intent

This template exists to:
- Improve internal structure intentionally
- Reduce technical debt with approval
- Prevent accidental behavior changes

This template does NOT:
- Add features
- Fix bugs
- Change runtime behavior

---

## 2. Preconditions (MANDATORY)

Before proceeding, verify ALL:

- Refactoring is explicitly requested
- Refactoring goals are stated
- Success criteria are defined
- Behavior to preserve is documented

If any condition fails:
- STOP
- Request clarification

---

## 3. Allowed Activities

You MAY:
- Rename variables or functions (if approved)
- Reorganize code structure (if approved)
- Improve readability or maintainability
- Extract or inline logic as approved

All changes must:
- Preserve observable behavior
- Stay within approved scope

---

## 4. Forbidden Activities (STRICT)

You must NOT:
- Change logic or outcomes
- Fix bugs “along the way”
- Add features
- Introduce new architecture
- Apply best practices beyond scope

If a bug is discovered:
- Report it
- Do NOT fix it

---

## 5. Behavior Preservation Rule (CRITICAL)

You must explicitly reason about:
- What behavior remains unchanged
- How equivalence is ensured

If equivalence cannot be proven:
- STOP
- Do not proceed

---

## 6. Scope Declaration (MANDATORY)

Planning must declare:
- Files to be refactored
- Symbols affected
- Refactoring techniques used

Implicit refactors are forbidden.

---

## 7. Confidence Handling

Confidence must be **CONFIRMED** to proceed.

- HYPOTHESIS → clarify
- UNKNOWN → stop

---

## 8. Required Output Discipline

You must comply with:
- Phase-specific output formats
- Global Execution Rules
- Domain execution rules

Deviation is a failure.

---

## Final Instruction

Refactoring without permission is vandalism.

Change structure only when asked — and nothing else.
