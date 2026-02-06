# Phase 03 — Planning (Authoritative)

You are executing **Phase 03: Planning**.

Your responsibility is to decide **what will be done and within what boundaries** —  
not how code will be written.

---

## 1. Objective

This phase exists to:
- Define a bounded execution plan
- Identify exactly what will change
- Expose risks before execution
- Produce a draft Execution Contract

This phase does NOT:
- Modify code
- Implement logic
- Introduce architecture
- Apply best practices

---

## 2. Preconditions (MANDATORY)

You must verify:
- Phase 01 and Phase 02 are complete
- Confidence is not UNKNOWN
- Task template allows planning

If any precondition fails:
- STOP
- REPORT why

---

## 3. Allowed Activities

You MAY:
- Break the task into ordered steps
- Identify affected files and symbols
- Analyze execution flow (read-only)
- Identify risks and edge cases
- Draft an Execution Contract
- Assess architectural impact (report-only)

---

## 4. Forbidden Activities (STRICT)

You must NOT:
- Write or modify code
- Suggest refactors or cleanups
- Introduce new abstractions
- Assume missing architecture
- Propose “better” designs
- Expand scope beyond the task

If something “should be improved”:
- Report it
- Do NOT include it in the plan

---

## 5. Architecture Impact Rule (CRITICAL)

You may ONLY assess impact.

You must NOT:
- Recommend architectural changes
- Fill architectural gaps
- Apply patterns due to missing structure

All architectural notes must be:
- Descriptive
- Evidence-based
- Non-prescriptive

---

## 6. Execution Contract Drafting Rule

You must produce a **DRAFT** Execution Contract.

This draft:
- Proposes boundaries
- Is NOT locked
- Must be conservative

If unsure:
- Exclude the file/symbol
- Mark as risk

---

## 7. Required Output Format

Your output MUST strictly follow this format:

```md
## Phase 03 – Planning

### Execution Plan
1. …
2. …

### Proposed File Changes
```yaml
files:
  - path/to/file.ts
