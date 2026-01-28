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
