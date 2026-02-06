# Task Template — T1: New Feature (Authoritative)

You are operating under the **New Feature** task template.

This template applies ONLY when the requested functionality
**does not currently exist in the system**.

---

## 1. Template Intent

This template exists to:
- Introduce new behavior deliberately
- Bound scope before any execution
- Prevent accidental refactors or redesigns

It does NOT:
- Modernize existing code
- Improve architecture
- Align patterns across the system

---

## 2. Preconditions

Before proceeding, you must verify:

- The feature does NOT already exist (even partially)
- The task intent is explicitly additive
- The domain (backend / frontend / full-stack) is declared

If similar behavior exists:
- STOP
- Recommend **T2 – Modify Existing Feature**

---

## 3. Allowed Scope

You MAY:
- Add new logic explicitly required by the feature
- Add new files **only if declared in planning**
- Extend existing flows only where approved

You must NOT:
- Refactor existing features
- Change unrelated behavior
- Apply architectural patterns “for consistency”

---

## 4. Architecture Discipline (CRITICAL)

New features must:
- Fit into **existing observed structure**
- Avoid introducing new architectural concepts
- Avoid “setting a pattern for the future”

If structure is missing or unclear:
- Treat it as UNKNOWN
- Report the risk
- Do NOT invent structure

---

## 5. Planning Implications

During planning:
- Scope must be minimal
- New files must be explicitly listed
- New symbols must be explicitly listed
- Risks must include future coupling concerns

Execution Contract must be:
- Conservative
- Explicit
- Human-approved

---

## 6. Confidence Rules

For this template:
- Planning confidence must reach **CONFIRMED**
- Execution may not begin under HYPOTHESIS

Speculative features are prohibited.

---

## 7. Output Discipline

This template does NOT define output format.

You must still follow:
- Phase rules
- Agent rules
- Domain rules
- Global execution rules

---

## 8. Failure Modes (Expected)

If:
- Feature boundaries cannot be defined
- Architecture cannot safely absorb the feature
- Requirements remain vague

Then:
- STOP
- Report
- Recommend clarification or investigation

---

## Final Instruction

A new feature is a commitment.

If it cannot be bounded clearly,
it must not be implemented.
