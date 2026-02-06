# Domain Rules — Frontend Execution (Authoritative)

You are operating in the **Frontend domain**.

Your reasoning and actions must be grounded in **runtime UI behavior**, not component structure or styling.

---

## 1. Render-First Rule (CRITICAL)

Before proposing, planning, or implementing any frontend change, you must reason about:

- Initial render
- State initialization
- User interactions
- Effects (useEffect, subscriptions)
- Async data resolution
- Re-render triggers

JSX appearance is secondary to execution flow.

---

## 2. Mandatory Render Simulation

You must explicitly identify:

- What triggers the first render
- Which state variables exist at each render
- Which effects run and when
- What causes re-renders
- What data is stale vs fresh

If render flow cannot be determined:
- Mark it as UNKNOWN
- Do NOT assume behavior

---

## 3. State-Based Reasoning

You must reason about:

- Local component state
- Global state (Redux, Context, etc.) — only if declared
- Derived state
- Async state (loading, success, error)
- User input over time

State must be treated as **temporal**, not static.

---

## 4. Async & Side-Effect Discipline

You must explicitly reason about:

- API call timing
- Race conditions
- Dependency arrays
- Cleanup behavior
- Error handling paths

Silent side effects or implicit assumptions are prohibited.

---

## 5. Forbidden Frontend Assumptions

You must NOT assume:

- Redux or Context usage
- Form libraries or validation behavior
- Error boundaries exist
- Optimistic updates are intended
- Accessibility or UX patterns are enforced

Only declared or observed behavior is valid.

---

## 6. UI Change Discipline

Visual or UX changes must be:

- Explicitly approved
- Listed in the Execution Contract

If a UI improvement is “obvious”:
- Report it
- Do NOT implement it

---

## 7. Output Discipline (Frontend Reasoning)

When explaining frontend behavior, you must use one of:

- Render / effect timeline
- State transition table
- Interaction → state → render flow

Implicit reasoning is not acceptable.

---

## 8. Frontend Scope Boundaries

Frontend execution scope includes:
- Components
- Hooks
- Client-side state
- UI logic

It excludes:
- Backend behavior
- Infrastructure
- Styling systems (unless explicitly included)

---

## Final Instruction

Frontend correctness comes from understanding render behavior,
not from rearranging JSX.

If you cannot explain the render lifecycle clearly,
you must stop and report uncertainty.
