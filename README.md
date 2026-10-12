# my-skills

Curated collection of modular AI agent skills, rules, and workflows for Google Antigravity and compatible LLM coding assistants.

This repository serves as an umbrella catalog for specialized agent capabilities. As new skill suites are developed, they are added modularly under their respective collection directories.

---

## Collections

### 1. `socratic-mentor-skills`
A pedagogical skill suite designed to transform an AI coding assistant from a direct code generator into a rigorous, first-principles **Senior Technical Mentor**.

* **`socratic-pedagogy`**: 4-phase learning loop (Diagnostic -> Socratic Inquiries -> Progressive Scaffolding -> Consolidation).
* **`architecture-mentor`**: System design coaching, Non-Functional Requirements (NFR) analysis, CAP/ACID trade-offs, and Architecture Decision Record (ADR) writing.
* **`ml-first-principles`**: Deep learning mathematical foundations (gradients, self-attention, loss surfaces), tensor debugging, and RAG architectures.
* **`deliberate-practice-katas`**: Challenge generator ("Spot the Bug", Refactoring Katas, "Build from Scratch", and Incident Drills).
* **`code-critique-mentor`**: Pedagogical code review evaluating Big-O complexity, Clean Code, boundary conditions, and defensive programming without rewriting the code.
* **`AGENTS.md`**: Project-level rule contract enforcing the didactic mentor persona.

---

## Quickstart & Installation

To install these skills in your Antigravity workspace or compatible AI agent environment:

1. Clone this repository:
   ```bash
   git clone https://github.com/hamza-jpg/my-skills.git
   ```

2. Copy the desired skills into your project's `.agents/skills/` directory:
   ```bash
   mkdir -p .agents/skills
   cp -r my-skills/socratic-mentor-skills/* .agents/skills/
   ```

3. Copy the mentor rule contract to your project root:
   ```bash
   cp my-skills/socratic-mentor-skills/AGENTS.md ./AGENTS.md
   ```

---

## Design Principles & Behavioral Constraints

The skills in this repository follow strict pedagogical constraints:

1. **No Direct Code Generation:** The agent does not provide copy-paste solutions on the first pass. The learner writes the code; the agent guides with targeted questions.
2. **Zero Flattery:** Congratulatory filler and emotive praising ("Great job!", "Awesome!", "Tebrikler!") are prohibited. The interaction is objective, neutral, and technically demanding.
3. **No Unsolicited Analogies:** Metaphors and everyday analogies are forbidden unless explicitly requested. Concepts are explained using direct computer science and mathematical terminology.
4. **Zero Emojis:** Communication is strictly plain technical markdown text.

---

## References & Inspirations

This repository draws inspiration and patterns from the following open-source projects, academic literature, and engineering standards:

* **ClawForge Skills Repository:** [https://github.com/jackjin1997/ClawForge](https://github.com/jackjin1997/ClawForge) - Software craftsmanship and developer skill patterns.
* **Google Antigravity Customization Architecture:** YAML frontmatter specification with progressive disclosure.
* **Robert C. Martin ("Uncle Bob"):** *Clean Code: A Handbook of Agile Software Craftsmanship* - SOLID design principles and refactoring metrics.
* **Martin Kleppmann:** *Designing Data-Intensive Applications* (O'Reilly Media) - Distributed systems trade-offs.
* **Andrej Karpathy:** *Micrograd & Neural Networks: Zero to Hero* - First-principles machine learning pedagogy.
* **K. Anders Ericsson:** *The Role of Deliberate Practice in the Acquisition of Expert Performance* - Deliberate practice and targeted error analysis.
* **Michael Nygard:** *Documenting Architecture Decisions* - Standard Architecture Decision Record (ADR) format.

---

## License

This project is licensed under the [MIT License](LICENSE).
