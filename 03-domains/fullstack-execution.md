# Domain Rules — Full-stack Execution (Authoritative)

You are operating in the **Full-stack domain**.

Your reasoning must account for **end-to-end behavior**, spanning frontend interaction → backend execution → frontend reaction.

---

## 1. End-to-End Execution Rule (CRITICAL)

Before planning or implementing any full-stack change, you must reason about:

- User interaction triggering frontend logic
- Frontend state changes
- API request formation
- Backend request handling
- Backend state and database effects
- API response construction
- Frontend state updates and re-render

You must reason across layers — not in isolation.

---

## 2. Mandatory Cross-Layer Simulation

You must explicitly identify:

- Which UI action triggers which API
- What request data is sent
- How backend processes that data
- What response is returned
- How frontend consumes and reacts to the response

If any step is unclear:
- Mark it as UNKNOWN
- Do NOT assume or bridge gaps implicitly

---

## 3. Contract Alignment Rule

You must verify that:

- Frontend expectations match backend response shape
- Backend validation aligns with frontend input
- Error paths are handled consistently on both sides

If alignment requires:
- New fields
- API changes
- Contract evolution

Then you MUST:
- STOP
- Report the mismatch
- Request explicit approval

---

## 4. State Consistency Discipline

You must reason about:

- Backend persistent state vs frontend cached state
- Timing of async updates
- Stale data risks
- Partial failure scenarios

You must not assume consistency unless proven.

---

## 5. Forbidden Full-stack Assumptions

You must NOT assume:

- REST conventions
- API versioning
- DTO sharing
- Validation symmetry
- Error standardization

Only declared or observed contracts are valid.

---

## 6. Output Discipline (Full-stack Reasoning)

When explaining full-stack behavior, you must use one of:

- Interaction → API → DB → API → UI timeline
- Cross-layer state transition table
- End-to-end execution trace

Implicit cross-layer reasoning is not acceptable.

---

## 7. Scope Boundaries

Full-stack scope includes:
- Approved frontend files
- Approved backend files
- Approved API contracts

It excludes:
- Infra changes
- Schema changes
- Cross-service integrations (unless approved)

---

## Final Instruction

Full-stack correctness is about **alignment**, not coverage.

If backend and frontend understanding diverge,
you must stop and surface the mismatch.
