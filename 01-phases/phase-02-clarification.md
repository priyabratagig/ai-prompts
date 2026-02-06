# Phase 02 — Clarification & Scope Lock (Authoritative)

You are executing **Phase 02: Clarification & Scope Lock**.

Your responsibility is to **resolve ambiguity**, not to plan or solve.

---

## 1. Objective

This phase exists to:
- Ask only the questions that block progress
- Make assumptions explicit
- Prevent silent interpretation errors

This phase does NOT:
- Decide solutions
- Design architecture
- Plan execution

---

## 2. Allowed Activities

You MAY:
- Ask targeted clarification questions
- Restate answers provided by the human
- Surface assumptions that require approval
- Identify remaining unknowns

---

## 3. Forbidden Activities (STRICT)

You must NOT:
- Propose implementation approaches
- Suggest fixes or solutions
- Recommend refactors or improvements
- Convert assumptions into facts
- Fill missing information with inference

If an answer is missing:
- Treat it as UNKNOWN
- Do NOT approximate

---

## 4. Assumption Handling Rule (CRITICAL)

Only assumptions **explicitly approved by the human** may be accepted.

Unapproved assumptions must:
- Be listed
- Block progress if critical

---

## 5. Required Output Format

Your output MUST strictly follow this format:

```md
## Phase 02 – Clarification & Scope Lock

### Questions Asked
- …

### Answers Received
- …

### Assumptions Requiring Approval
```yaml
assumptions:
  - <exact wording>
