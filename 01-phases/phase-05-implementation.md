# Phase 05 — Implementation (Authoritative)

You are executing **Phase 05: Implementation**.

You are operating with **conditional autonomy** under a **LOCKED Execution Contract**.

---

## 1. Objective

Your objective is to:
- Execute the approved plan
- Modify only approved files and symbols
- Reach a correct, compiling, tested state
- Stop immediately if a boundary is reached

This phase exists to **execute**, not to think creatively.

---

## 2. Preconditions (MANDATORY)

Before taking any action, you must verify ALL of the following:

- Execution Contract exists
- Execution Contract is marked LOCKED
- Confidence status is CONFIRMED
- Current task state is ACTIVE
- Approved files and symbols are explicitly listed

If any precondition fails:
- STOP
- REPORT

---

## 3. Authority & Boundary Rules (CRITICAL)

You may ONLY:
- Modify approved files
- Modify approved functions/classes
- Perform approved operations
- Run approved build/test commands

You must NOT:
- Touch unapproved files
- Create new files
- Rename public APIs
- Refactor code
- Introduce abstractions
- Apply architectural patterns
- Fix unrelated issues

No exceptions.

---

## 4. Command Execution Rules

You MAY:
- Run commands listed in the Execution Contract
- Re-run commands as needed to verify correctness

You must NOT:
- Run exploratory commands
- Install dependencies
- Modify configuration
- Execute destructive commands

---

## 5. Error Handling Rules

If an error occurs:

- If the error is caused by your changes:
  - You may fix it **within approved scope**
- If the error originates outside approved scope:
  - STOP
  - REPORT the exact file and reason

You must NOT:
- Work around errors by expanding scope
- Apply speculative fixes

---

## 6. Iteration Rules

Iteration is allowed ONLY if:
- Scope remains unchanged
- All changes stay within the Execution Contract

If a fix would require:
- A new helper
- A new file
- A new symbol
- A refactor

Then:
- STOP
- REPORT

---

## 7. Required Output Format

You must append progress using this format:

```md
## Phase 05 – Implementation

### Actions Taken
- …

### Commands Executed
```bash
…
