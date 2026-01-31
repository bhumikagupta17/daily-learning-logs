# Daily Progress Log
---
### Day 1: 27 January 2026
---

 **Focus:** Version Control & DSA (LeetCode 75)

**1. Git & GitHub Fundamentals**
- Learned the core workflow: `git init`, `git add`, `git commit`, and `git push`.
- Understood the difference between the **Working Directory**, **Staging Area**, and **Local Repository**.
- *Action:* Initialized this tracking repository and pushed first commits.

**2. DSA Practice**
- **Problem:** Sort Colors (LeetCode #75)
- **Approach:** Counting Sort (Two-Pass).
   1. Counted frequency of 0s, 1s, and 2s in the first pass.
   2. Overwrote the original array based on counts in the second pass.
- **Complexity:** Time $O(N)$ (2N traversals) | Space $O(1)$

---
### Day 2: 28 January 2026
---
**Focus:** Deployment (GitHub Pages) & DSA (Kadane's Algorithm)

**1. Web Development & Deployment**
- **GitHub Pages:** Learned how to host static sites directly from a repo.
- **Project:** Deployed a landing page for my Game Hub (featuring Tic-Tac-Toe & Rock-Paper-Scissors).
- *Achievement:* My first project is now live on the web.

**2. DSA Practice**
- **Problem:** Maximum Subarray (LeetCode #53)
- **Algorithm:** **Kadane's Algorithm** (Dynamic Programming).
- **Logic:** Iterated through the array while maintaining a `prev_sum`. If adding the current number increases the sum vs starting fresh, extend the subarray; otherwise, reset.
- **Complexity:** Time $O(N)$ | Space $O(1)$

---
### Day 3: 29 January 2026
---
**Focus:** Linked Lists, System Internals & JS OOP

**1. DSA Practice**
- **Solved:**
  - **Max Ice Cream Bars (LC #1833):** Used Greedy approach with Sorting.
  - **Add Two Numbers (LC #2):** Used **Dummy Head** to handle edge cases.
  - **Add Two Numbers II (LC #445):** Solved by **Reversing Lists** to handle addition from LSB.

**2. Core Concepts**
- **OS & Systems:** Studied **API vs ABI**, **POSIX** standards, and **ELF** format.
- **Android:** Learned why Android uses **DVM/ART** (.dex files) instead of the standard JVM.

**3. Web Development**
- **JavaScript:** Learned ES6 **Classes**, **Objects**, and the `super` keyword for inheritance.

---
### Day 4: 30 January 2026
---
**Focus:** Two-Pointer Technique (Arrays & Linked Lists)
**DSA Practice**
#### **Solved 4 Problems:**
- **Remove Duplicates (LC #26) & Remove Element (LC #27):**
  - **Pattern:** Mastered in-place **Two Pointer** technique to modify arrays without extra space ($O(1)$).
- **Delete Middle Node (LC #2095):**
  - **Algorithm:** Used **Tortoise & Hare** (Slow/Fast pointers) to locate and remove the middle node in a single pass.
- **Remove Elements (LC #203):**
  - **Logic:** Filtered nodes using a **Dummy Head** to handle edge cases where the head itself needs removal.

---
### Day 5: 31 January 2026
---
**Focus:** Linked List Manipulation & Asynchronous JavaScript

**1. DSA Practice**
- **Insert GCD in Linked List (LC #2807):**
  - **Logic:** Used Euclidean Algorithm for GCD. Iterated through the list to insert new nodes between pairs.
  - **Complexity:** Time $O(N)$ | Space $O(N)$ (Current solution).
  - **Optimization Note:** Recognized that space can be improved to **$O(1)$** by inserting nodes directly into the existing list (In-Place) instead of creating a new dummy list.

**2. Web Development (JavaScript)**
- **Asynchronous Programming:**
 - **Callbacks:** Understood the base concept of passing functions as arguments.
 - **Callback Hell:** Learned why deeply nested callbacks are hard to read and debug.
 - **Promises:** Studied how to handle async operations more cleanly (`.then()`, `.catch()`).
 - **Async/Await:** Learned the modern syntactic sugar to write asynchronous code that looks synchronous.
