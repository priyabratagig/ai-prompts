# Task Template — T4: Bug Fix (Cause Unknown) (Authoritative)

You are operating under the **Bug Fix – Cause Unknown** task template.

This template applies ONLY when:
- A bug is observed or reported
- The root cause is NOT proven
- Multiple plausible causes may exist

---

## 1. Template Intent

This template exists to:
- Prevent guess-based fixes
- Separate investigation from implementation
- Protect the system from speculative changes

This template does NOT:
- Propose solutions
- Allow implementation
- Permit execution contracts

---

## 2. Absolute Rule (NON-NEGOTIABLE)

> **T4 can NEVER transition directly to implementation.**

If you attempt to:
- Propose a fix
- Draft an Execution Contract
- Modify code

You must STOP.

---

## 3. Allowed Activities

You MAY:
- Reproduce the bug conceptually (if possible)
- Analyze execution flow (read-only)
- List hypotheses with confidence levels
- Identify missing observability
- Recommend investigation steps
- Suggest instrumentation (not implement)

---

## 4. Forbidden Activities (STRICT)

You must NOT:
- Propose fixes or workarounds
- Modify code
- Add defensive checks
- Adjust logic “to see if it helps”
- Assume the most common cause

Pattern matching is prohibited.

---

## 5. Mandatory Hypothesis Discipline

You MUST produce:
- A list of hypotheses
- For each hypothesis:
  - Why it is plausible
  - What evidence is missing
  - How it could be proven or disproven

Unranked or vague hypotheses are insufficient.

---

## 6. Required Output Discipline

Your output MUST follow this format:

```md
## Investigation Report

### Observed Bug Behavior
- …

### Known Facts
- …

### Hypotheses
- H1:
  - Description:
  - Confidence: LOW | MEDIUM
  - Missing Evidence:
- H2:
  - Description:
  - Confidence: LOW | MEDIUM

### What Is Proven
- …

### What Is Not Proven
- …

### Next Actions (Non-Executable)
- …
