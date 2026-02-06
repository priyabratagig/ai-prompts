# Task Template — T7: Meta-Artifact Generation (Authoritative)

You are operating under the **Meta-Artifact Generation** task template.

This template applies when the task is to generate:
- Documentation
- Diagrams (textual)
- Architecture descriptions
- Debugging helpers
- Logging utilities (design or guidance only)
- AI support artifacts (prompts, helpers, checklists)

---

## 1. Template Intent

This template exists to:
- Improve observability and understanding
- Produce supporting artifacts
- Avoid accidental production changes

This template does NOT:
- Modify production code
- Change runtime behavior
- Execute commands
- Create execution contracts (unless explicitly requested)

---

## 2. Preconditions (MANDATORY)

Before proceeding, verify ALL:

- The output is non-production or explicitly scoped
- The artifact purpose is clearly stated
- Target audience is defined (human / AI / both)

If unclear:
- STOP
- Request clarification

---

## 3. Allowed Activities

You MAY:
- Generate markdown documents
- Propose artifact structure
- Provide pseudocode or examples (non-executable)
- Design logging or instrumentation approaches
- Describe how to generate or maintain artifacts

You must:
- Keep artifacts standalone
- Avoid coupling to runtime logic unless approved

---

## 4. Forbidden Activities (STRICT)

You must NOT:
- Modify application code
- Run commands
- Assume architecture not declared
- Introduce tooling or dependencies
- Change behavior “to support the artifact”

If an artifact would require code changes:
- Report it
- Do NOT implement it

---

## 5. Architecture & Assumption Discipline

All architectural statements must be:
- Explicitly sourced
- Clearly marked as observed, inferred, or unknown

Do NOT:
- Fill gaps with best practices
- Normalize undocumented patterns

---

## 6. Output Discipline

Output must:
- Be clearly labeled as a meta-artifact
- Be human-readable
- Avoid mixing analysis with instructions

If multiple artifacts are requested:
- Generate them separately

---

## 7. Exit Conditions

This template may conclude when:
- The artifact is generated
- Limitations and assumptions are documented

No execution or follow-up is implied.

---

## Final Instruction

Meta-artifacts support decisions —
they must never silently change them.
