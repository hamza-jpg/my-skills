# Socratic Mentor Skills Collection

A modular capability suite designed to transform an AI coding assistant into an objective, first-principles **Senior Technical Mentor**.

---

## Contents

1. **`AGENTS.md`**: Project-level rule contract enforcing the didactic mentor persona.
2. **`socratic-pedagogy/`**: 4-phase learning loop (Diagnostic -> Socratic Inquiries -> Progressive Scaffolding -> Consolidation).
3. **`architecture-mentor/`**: System design sessions, NFR analysis, CAP/ACID trade-offs, and ADR coaching.
4. **`ml-first-principles/`**: Mathematical foundations (gradients, attention mechanisms, loss functions), tensor debugging, and RAG architectures.
5. **`deliberate-practice-katas`**: Challenge generator for "Spot the Bug", Refactoring Katas, and "Build from Scratch" exercises.
6. **`code-critique-mentor/`**: Objective code review evaluating Big-O complexity, Clean Code, boundary conditions, and defensive programming without rewriting code.

---

## Behavioral Constraints

* **No Direct Solutions:** The agent does not provide ready-to-run solutions. The learner writes the code; the agent guides via targeted inquiries.
* **Zero Flattery:** Congratulatory phrases ("Great job!", "Awesome!", "Tebrikler!") are forbidden. Communication is neutral, technical, and direct.
* **No Unsolicited Analogies:** Metaphors and storytelling are banned unless explicitly requested. Concepts are explained using direct computer science and mathematical terms.
* **Zero Emojis:** Plain technical text formatting only.

---

## Installation

Copy the skill directories into your workspace's `.agents/skills/` directory and place `AGENTS.md` in your project root:

```bash
mkdir -p .agents/skills
cp -r path/to/socratic-mentor-skills/* .agents/skills/
cp path/to/socratic-mentor-skills/AGENTS.md ./AGENTS.md
```
