# AI Phase-Based + Lightweight Multi-Agent Workflow System

This repository contains a **deterministic, phase-gated, agent-driven AI software development workflow** designed specifically for **VS Code Copilot (Agent / Ask / Plan modes)**.

It is not a collection of prompts.
It is a **prompt architecture** — an AI SDLC control system that prioritizes:

* Human authority
* Explicit confidence over assumptions
* Zero architectural guessing
* Controlled autonomy
* Reproducible outcomes across models

---

## 1. Why This System Exists

Modern AI tools fail in software development because they:

* Rush to solutions before clarity
* Guess architecture when documentation is missing
* Apply best practices implicitly
* Expand scope silently
* Produce different solutions with different models

This system solves those failures by enforcing:

* Phase separation (think → decide → act)
* Confidence gates
* Execution contracts
* Strict role boundaries
* Explicit state tracking

> **Unknown is a valid outcome.**

---

## 2. Core Principles (Non‑Negotiable)

1. AI does **not** own scope
2. AI does **not** assume architecture
3. AI does **not** execute without confidence
4. AI does **not** refactor unless explicitly asked
5. Investigation is success, not failure
6. Every task has a single state container
7. Execution requires a locked Execution Contract

If any principle is violated, the system must **stop**.

---

## 3. High‑Level Architecture

```
ai-prompts/
├── 00-global/          # Absolute rules (always attached)
├── 01-phases/          # Phase-specific authority
├── 02-agents/          # Role-based behavior
├── 03-domains/         # Runtime reasoning rules
├── 05-project/         # Project-specific constraints
├── 06-task-templates/  # Situation framing
├── jobs/               # Task state containers
└── README.md
```

Each folder is **orthogonal**. No implicit dependencies.

---

## 4. What Is Reusable vs Project‑Specific

### Always Reused (Copy As‑Is)

* `00-global/`
* `01-phases/`
* `02-agents/`
* `03-domains/`
* `06-task-templates/`

### Project‑Specific

* `05-project/project-architecture-knowledge.md`
* `jobs/`

---

## 5. Phase Model (Authoritative)

| Phase    | Purpose                      |
| -------- | ---------------------------- |
| Phase 00 | Task initialization (manual) |
| Phase 01 | Task interpretation          |
| Phase 02 | Clarification & scope lock   |
| Phase 03 | Planning                     |
| Phase 04 | Execution Contract approval  |
| Phase 05 | Implementation               |
| Phase 06 | Review & reporting           |
| Phase 07 | Closure                      |

Rules:

* Phases cannot be skipped
* Phases cannot be mixed
* AI cannot advance phases

---

## 6. Confidence Gates

Every task must explicitly declare one of:

* `CONFIRMED` – proven by evidence
* `HYPOTHESIS` – plausible but unproven
* `UNKNOWN` – insufficient information

Rules:

* UNKNOWN → blocks planning & execution
* HYPOTHESIS → blocks execution
* Only CONFIRMED allows implementation

---

## 7. Execution Contract (Critical)

Before any code is modified, **a locked Execution Contract is required**.

It defines:

* Allowed files
* Allowed symbols
* Allowed operations
* Forbidden actions
* Build / test commands

Once locked:

* Immutable
* No silent expansion
* Boundary violation → STOP

---

## 8. Agent Model

Agents are logical roles, not separate models.

| Agent                  | Authority               |
| ---------------------- | ----------------------- |
| Task Interpreter       | Understand intent       |
| Clarifier              | Remove ambiguity        |
| Planner                | Define scope & steps    |
| Architect (Passive)    | Report impact only      |
| Implementer (BE/FE/FS) | Execute within contract |
| Reviewer               | Verify & report         |

Agents cannot exceed their authority.

---

## 9. Task Templates

Task templates prevent incorrect execution paths.

| ID | Template                 |
| -- | ------------------------ |
| T1 | New Feature              |
| T2 | Modify Existing Feature  |
| T3 | Bug Fix – Cause Known    |
| T4 | Bug Fix – Cause Unknown  |
| T5 | Investigation Only       |
| T6 | Refactor (Explicit Only) |
| T7 | Meta‑Artifact Generation |

> If unsure, choose the **more restrictive** template.

---

## 10. Job Files (State Containers)

Each task has **exactly one job file** under `jobs/`.

* Append‑only
* Single source of truth
* Past phases are immutable

Task lifecycle:

```
DRAFT → ACTIVE → BLOCKED | COMPLETED | ABORTED
```

---

## 11. Architecture Assumption Lock

Architecture must be:

* Explicitly declared
* Or explicitly observed

Anything else is **UNKNOWN**.

AI is forbidden from:

* Applying best practices
* Introducing patterns
* Normalizing structure

Absence of architecture ≠ permission to assume.

---

## 12. Copilot Usage Rules

This system is designed for **VS Code Copilot**.

| Mode  | Usage                                                   |
| ----- | ------------------------------------------------------- |
| Ask   | Clarification, review                                   |
| Agent | Interpretation, planning, investigation, implementation |
| Plan  | Optional (human-facing only)                            |

Rules:

* Never mix phases in one invocation
* Never attach unused prompt modules
* Agent mode is allowed for implementation **only after contract lock**

---

## 13. Daily Workflow (Practical)

1. Copy `jobs/_template.md` → `jobs/<task>.md`
2. Fill Phase 00
3. Run Phase 01 (Task Interpreter)
4. Run Phase 02 (Clarifier)
5. Run Phase 03 (Planner)
6. Approve Execution Contract
7. Run Phase 05 in Agent mode
8. Review
9. Close task

---

## 14. When AI Must Stop

AI must STOP if:

* Confidence ≠ CONFIRMED
* Execution Contract is missing
* Scope expansion is required
* Architecture is not declared
* A boundary is violated

Stopping is **correct behavior**.

---

## 15. Anti‑Patterns (Explicit)

❌ “While we are here, let’s clean this up”
❌ “This is best practice, so…”
❌ Guessing causes
❌ Implicit refactors
❌ Architecture inference
❌ Multi‑tasking in one job file

---

## 16. Extending the System Safely

You may add:

* New domain rules
* New task templates
* New tech modules

You must NOT:

* Change global rules
* Remove confidence gates
* Relax execution contracts

---

## 17. Philosophy

This system treats AI as:

* A **junior engineer with perfect recall**
* A **senior engineer without authority**

Authority always remains human.

---

## 18. Final Note

This repository is intentionally strict.

If AI feels less “helpful”, that means the system is working.

Correctness > Speed
Control > Convenience
Evidence > Guessing
