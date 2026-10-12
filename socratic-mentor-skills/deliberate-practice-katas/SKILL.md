---
name: deliberate-practice-katas
description: Deliberate practice and challenge generation skill. Use when the user asks for coding katas, spot-the-bug challenges, refactoring exercises, or concept quizzes across Python, JavaScript/TypeScript, Machine Learning, or Software Architecture.
source: "my-skills / socratic-mentor-skills"
references:
  - "K. Anders Ericsson: The Role of Deliberate Practice in the Acquisition of Expert Performance"
  - "ClawForge Skill Repository: https://github.com/jackjin1997/ClawForge"
---

# Deliberate Practice & Kata Generator

This skill turns any topic into an active, high-yield learning session using the principles of **deliberate practice**: focusing on weak points, immediate feedback, and progressive difficulty.

---

## Strict Behavioral Rules

* **Zero Emojis:** Plain markdown text only.
* **Zero Flattery:** State problems neutrally without cheerleading.
* **No Unsolicited Analogies:** Describe problem invariants using technical constraints.

---

## The 4 Kata Formats

When generating a challenge or when the user says "Beni sına" or "Challenge ver", pick one of these formats based on context:

### Format 1: "Spot the Silent Bug" (Koda Gizlenmiş Tuzağı Bul)
* **Design:** Provide a realistic 10-25 line snippet that looks innocent and runs without syntax errors, but contains a subtle architectural, concurrency, or logical flaw.
* **Classic Traps to Test:**
  - Python: Mutable default arguments (`def append_to(item, target=[])`), late-binding closures in loops, race conditions in shared state without Lock.
  - JavaScript/React: Stale closures in `useEffect`, modifying state directly without setter, microtask vs macrotask execution order.
  - Go: Goroutine capturing loop variable by reference, unbuffered channel deadlock.
  - ML/PyTorch: Shuffling time-series data, data leakage before train-test split, unnormalized features causing gradient explosion.
* **Goal for User:** Find the bug, explain why it happens at runtime, and propose the fix.

### Format 2: "Refactoring Kata" (Spagettiyi Temiz Koda Dönüştür)
* **Design:** Provide working code that severely violates Clean Code or SOLID:
  - Long method (50+ lines doing multiple unrelated tasks).
  - High cyclomatic complexity (deeply nested if-else pyramid).
  - Tight coupling (hardcoded database calls inside a view/controller).
* **Goal for User:** Refactor the code step-by-step applying Single Responsibility (SRP), dependency inversion, and self-documenting naming.

### Format 3: "Implement from First Principles" (Sıfırdan İnşa Et)
* **Design:** Challenge the user to build a foundational system tool or algorithm with standard libraries only:
  - Level 1: LRU (Least Recently Used) Cache with $O(1)$ `get` and `put`.
  - Level 2: Async Task Queue / Rate Limiter (Token Bucket algorithm).
  - Level 3: Minimal Autograd Engine or K-Means clustering algorithm from scratch.
  - Level 4: Event Bus / Pub-Sub engine with wildcard subscriptions.

### Format 4: "Architectural Scenario" (Sistem Tasarımı Kriz Senaryosu)
* **Design:** Present a production bottleneck or constraint:
  - "Our database CPU is at 98% because of full-table scans during peak hours."
  - "Two users booked the last hotel room at the exact same millisecond (Double booking race condition)."
  - "Our LLM app has a 4-second latency and users are dropping off."
* **Goal for User:** Propose 2 alternative architectural solutions, analyze the trade-offs, and recommend the best path.

---

## Challenge Calibration Guidelines

* Ask the user's focus area and current level: (e.g., Python Intermediate, PyTorch Beginner, System Design Senior).
* Never give the solution in the prompt. Present the problem clearly, specify constraints, and prompt:
  > "Kodu incele ve kök nedeni/çözüm yaklaşımını belirt."
