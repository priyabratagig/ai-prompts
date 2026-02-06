# Task Template — T2: Modify Existing Feature (Authoritative)

You are operating under the **Modify Existing Feature** task template.

This template applies ONLY when:
- The feature already exists
- Behavior needs to be changed, extended, or corrected
- The change is intentional and scoped

---

## 1. Template Intent

This template exists to:
- Safely change existing behavior
- Prevent accidental rewrites
- Preserve existing architecture and assumptions

This template does NOT:
- Introduce new features
- Refactor unrelated code
- Improve architecture

---

## 2. Preconditions (MANDATORY)

Before proceeding, verify ALL:

- Existing feature is identified and understood
- Current behavior is documented
- Desired behavior is clearly stated
- Scope of change is bounded

If any condition fails:
- STOP
- Request clarification or recommend a different template

---

## 3. Allowed Activities

You MAY:
- Modify existing logic within approved scope
- Extend existing functions or components
- Adjust behavior where explicitly requested

You must:
- Minimize blast radius
- Preserve existing contracts unless approved

---

## 4. Forbidden Activities (STRICT)

You must NOT:
- Rewrite the feature wholesale
- Refactor code “for clarity”
- Rename functions or files unless approved
- Introduce new abstractions
- Change architecture

If existing design feels suboptimal:
- Report it
- Do NOT change it

---

## 5. Architecture Discipline

You must adapt to:
- Existing observed structure
- Declared project constraints

You must NOT:
- Apply patterns to “fix” perceived issues
- Introduce layers or helpers opportunistically

Missing architecture must be treated as UNKNOWN, not as a gap to fill.

---

## 6. Change Boundary Declaration (MANDATORY)

Planning must explicitly declare:
- Which behavior changes
- Which behavior remains untouched
- Which files/symbols are affected

Implicit behavior change is forbidden.

---

## 7. Regression Risk Handling

You must explicitly consider:
- Backward compatibility
- Side effects
- Dependent flows

Risks must be surfaced in planning.

---

## 8. Confidence Handling

Confidence rules apply strictly:

- CONFIRMED → may proceed to Execution Contract
- HYPOTHESIS → must clarify
- UNKNOWN → must stop

---

## 9. Required Output Discipline

You must comply with:
- Phase-specific output formats
- Global Execution Rules
- Domain execution rules

Deviation is a failure.

---

## Final Instruction

A modification is successful when:
- The requested change is achieved
- Everything else remains exactly the same

Change behavior, not structure.
