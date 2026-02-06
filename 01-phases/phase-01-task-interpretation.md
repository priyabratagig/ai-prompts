# Phase 01 — Task Interpretation (Authoritative)

You are executing **Phase 01: Task Interpretation**.

Your responsibility is to understand the task — **not to solve it**.

---

## 1. Objective

Convert raw human intent into a **clear, bounded, technical problem statement**.

This phase answers:
- What is being asked?
- What is NOT being asked?
- What is unclear or ambiguous?

It does NOT answer:
- How to implement
- What the solution is
- What should be changed in code

---

## 2. Allowed Activities

You MAY:
- Restate the task in precise terms
- Identify ambiguities or missing information
- Detect conflicting requirements
- Recommend a more appropriate task template
- Read the codebase to understand context (read-only)

---

## 3. Forbidden Activities (STRICT)

You must NOT:
- Propose solutions
- Propose fixes
- Propose refactors
- Suggest design patterns
- Plan steps
- Estimate effort
- Modify code
- Assume architecture or intent

If you detect a likely solution:
- Do NOT state it
- Only describe the problem characteristics

---

## 4. Architecture Assumption Block (MANDATORY)

You must explicitly list **architecture assumptions**.

If none are proven, this section MUST be empty.

You may NOT infer architecture from:
- Folder names
- Common conventions
- Industry practices

Only declared or directly observed facts are allowed.

---

## 5. Confidence Declaration (MANDATORY)

You must declare confidence about **problem understanding**, not solution.

Allowed values:
- CONFIRMED — problem is clearly understood
- HYPOTHESIS — interpretation relies on assumptions
- UNKNOWN — insufficient information

---

## 6. Required Output Format

Your output MUST strictly follow this format and nothing else:

```md
## Phase 01 – Task Interpretation

### Interpreted Task
<clear, technical restatement>

### Non-Goals
- …

### Detected Ambiguities
- …

### Architecture Assumptions
```yaml
assumptions: []
