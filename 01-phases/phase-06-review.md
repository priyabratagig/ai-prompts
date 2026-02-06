# Phase 06 — Review & Reporting (Authoritative)

You are executing **Phase 06: Review & Reporting**.

Your responsibility is to verify, summarize, and report —  
**not to improve, refactor, or extend**.

---

## 1. Objective

This phase exists to:
- Confirm what was actually changed
- Verify behavior against intent
- Surface risks and limitations
- Produce an auditable record

This phase does NOT:
- Modify code
- Propose enhancements
- Fix issues
- Re-open execution

---

## 2. Preconditions (MANDATORY)

Before starting, verify:
- Phase 05 has completed
- Execution outcome is SUCCESS or BLOCKED
- Job state is ACTIVE

If these are not true:
- STOP
- REPORT why

---

## 3. Allowed Activities

You MAY:
- Review modified files and symbols
- Verify behavior against requirements
- Verify build/test results
- Cross-check against Execution Contract
- Report out-of-scope issues (report only)

---

## 4. Forbidden Activities (STRICT)

You must NOT:
- Modify any code
- Suggest refactors or cleanups
- Recommend architectural changes
- Propose optimizations
- Restart implementation

If issues are found:
- Report them
- Do NOT act on them

---

## 5. Verification Rules

Verification must be:
- Evidence-based
- Directly tied to the task intent
- Limited to approved scope

You must explicitly state:
- What is verified
- What is NOT verified

---

## 6. Required Output Format

Your output MUST strictly follow this format:

```md
## Phase 06 – Review & Reporting

### Summary of Changes
- …

### Verification Performed
- …

### Verified Behaviors
- …

### Unverified or Assumed Behaviors
- …

### Out-of-Scope Issues (Reported Only)
- …

### Known Limitations
- …
