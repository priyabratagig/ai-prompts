# Task Template — T5: Investigation Only (Authoritative)

You are operating under the **Investigation Only** task template.

This template applies when:
- System behavior is unclear
- Root cause cannot be proven
- Confidence is insufficient for planning or execution

---

## 1. Template Intent

This template exists to:
- Gather evidence
- Reduce uncertainty
- Avoid premature fixes
- Document what is known vs unknown

This template does NOT:
- Propose fixes
- Modify code
- Create execution contracts

---

## 2. Absolute Restrictions (NON-NEGOTIABLE)

While operating under this template, you must NOT:
- Propose solutions
- Draft implementation plans
- Suggest refactors or improvements
- Modify any code

Any attempt to do so is a failure.

---

## 3. Allowed Activities

You MAY:
- Trace execution flow (read-only)
- Analyze state transitions
- Examine logs, errors, stack traces (if provided)
- List hypotheses and rank confidence
- Identify missing observability
- Suggest instrumentation or logging (not implement)
- Recommend next investigative steps

---

## 4. Evidence Discipline (CRITICAL)

All statements must be classified as one of:
- Observed
- Proven
- Hypothesized
- Unknown

Mixing these is prohibited.

---

## 5. Required Output Format

Your output MUST strictly follow this format:

```md
## Investigation Report

### Observed Behavior
- …

### Proven Facts
- …

### Hypotheses
- H1:
  - Description:
  - Confidence: LOW | MEDIUM
  - Evidence Missing:
- H2:
  - Description:
  - Confidence: LOW | MEDIUM

### Unknowns
- …

### Suggested Next Steps (Non-Executable)
- …
