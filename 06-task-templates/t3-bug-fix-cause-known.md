# Task Template — T3: Bug Fix (Cause Known) (Authoritative)

You are operating under the **Bug Fix – Cause Known** task template.

This template applies ONLY when:
- A bug is reproducible
- The root cause is clearly identified
- The execution flow leading to the bug is understood

---

## 1. Template Intent

This template exists to:
- Correct a specific, proven defect
- Apply the smallest possible fix
- Avoid defensive or speculative changes

This template does NOT:
- Improve code quality
- Refactor structure
- Harden unrelated logic

---

## 2. Preconditions (MANDATORY)

Before proceeding, verify ALL:

- Bug behavior is explicitly described
- Reproduction steps are known or observed
- Root cause is stated and evidence-backed
- Why the bug occurs is explained in execution terms

If the cause is not PROVEN:
- STOP
- Recommend **T4: Bug Fix – Cause Unknown**

---

## 3. Mandatory Root Cause Declaration

You MUST explicitly state:

- Where the bug originates
- Why the incorrect behavior occurs
- Under what conditions it manifests

Example (conceptual, not content):
- “When X is null, branch Y executes, leading to Z”

If this cannot be stated clearly:
- The cause is NOT known

---

## 4. Allowed Activities

You MAY:
- Modify logic directly responsible for the bug
- Adjust validations related to the bug
- Correct incorrect conditions or state handling

You must:
- Keep changes minimal
- Target the exact failure point

---

## 5. Forbidden Activities (STRICT)

You must NOT:
- Add defensive checks “just in case”
- Refactor surrounding code
- Modify behavior not related to the root cause
- Introduce logging or monitoring unless approved
- Fix similar-but-unreported issues

If you notice similar issues:
- Report them
- Do NOT fix them

---

## 6. Regression & Counter-Example Requirement (MANDATORY)

Planning MUST include:
- At least one counter-example
- Explanation of why the fix does NOT break valid behavior

If this cannot be reasoned about:
- STOP
- Re-evaluate confidence

---

## 7. Confidence Handling

Confidence must be **CONFIRMED** to proceed.

- HYPOTHESIS → downgrade to T4
- UNKNOWN → investigation required

Bug fixing without certainty is prohibited.

---

## 8. Required Output Discipline

You must comply with:
- Phase-specific output formats
- Global Execution Rules
- Domain execution rules

Deviation is a failure.

---

## Final Instruction

A bug fix is successful when:
- The bug no longer occurs
- No other behavior changes

Fix the defect, not the codebase.

