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

---
### Day 6: 01 February 2026
---

**Focus:** Fetch API, Hashing & Array Logic

**1. Web Development (JavaScript)**
- **Network Requests:**
  - **Fetch API:** Learned how to make HTTP requests to servers (`fetch(url)`).
  - **Request & Response:** Understood how to handle incoming data (JSON parsing) and HTTP status codes.

**2. DSA Practice**
- **Concepts:**
  - **Hashing & Maps:** Studied Key-Value pairs for efficient $O(1)$ lookups and frequency counting.

- **Find Smallest Letter (LC #744):**
  - **Approach:** Linear Scan.
  - **Logic:** Iterated through the sorted array to find the first character strictly greater than the target.
  - **Optimization Note:** Since the array is **sorted**, this can be optimized to **Binary Search** ($O(\log N)$) using `std::upper_bound` in C++.
  - **Complexity:** Time $O(N)$ (Current) vs $O(\log N)$ (Optimal).

- **Divide Array for Min Cost (LC #3010):**
  - **Approach:** **Greedy Strategy**.
  - **Logic:** Since the first element `nums[0]` is mandatory, I simply found the **two smallest** integers in the remaining array to minimize the total sum.
  - **Complexity:** Time $O(N)$ (Single pass to find mins) | Space $O(1)$.

---
### Day 7: 02 February 2026
---
**Focus:** Operating System Fundamentals (Theory)

**CS Fundamentals (OS)**
- **Introduction:** Understood the Operating System as a **Resource Manager** and the interface between User/Software and Hardware.
- **Key Concepts:**
  - **Kernel vs. Shell:** Learned that the **Kernel** is the core program managing hardware, while the **Shell** is the interface for users to command the OS.
  - **Modes of Operation:** Studied the difference between **User Mode** (restricted access) and **Kernel Mode** (privileged access).
  - **System Calls:** Learned how programs request services from the Kernel (e.g., reading a file or creating a process).
 
---
### Day 8: Feb 03, 2026
---
  
**Focus:** OS Fundamentals & Array Algorithms

**1. Operating Systems (Theory)**
- **Core Concepts:** Studied **Degree of Multiprogramming** (maximizing CPU utility) and **OS Classes** (Batch, Time-Sharing, Real-Time).
- **Booting:** Learned the **Boot Sequence** flow: BIOS/UEFI $\rightarrow$ MBR $\rightarrow$ Bootloader $\rightarrow$ Kernel.
- **History:** Traced the evolution from serial processing to modern mobile architectures.

**2. DSA Practice (Arrays)**
- **Minimum Size Subarray Sum (LC #209):**
  - **Pattern:** **Variable Sliding Window**.
  - **Logic:** Dynamically adjusted window size to find the minimal length matching the target sum ($O(N)$).

- **Next Permutation (LC #31):**
  - **Algorithm:** **Lexicographical Generation**.
  - **Optimization Note:** Currently using `sort()` for the suffix ($O(N \log N)$). Noted that `reverse()` can be used instead to achieve strict **$O(N)$** time since the suffix is already descending.

- **Rearrange Array by Sign (LC #2149):**
  - **Approach:** **Two Pointers (Constructive)**.
  - **Performance Gains:**
    - **Runtime:** Reduced from **13ms** to **3ms** (significant speedup).
    - **Memory:** Achieved a significant reduction in **Space Complexity** through better memory access patterns.

- **Leaders in an Array:**
  - **Approach:** **Suffix Max**.
  - **Logic:** Iterated **Right-to-Left** keeping track of the `max_so_far`. If current $>$ max, it is a leader.
---
### Day 9: 4 February 2026
---
**Focus:** Sequence Algorithms

**DSA Practice**
- **Longest Consecutive Sequence (LC #128):**
  - **Approach:** Sorting & Linear Scan.
  - **Logic:** Sorted the array and tracked sequences by comparing adjacent elements, handling duplicates with a `continue` check.
  - **Complexity:** Time $O(N \log N)$ | Space $O(1)$.
  - **Optimization:** Identified an **$O(N)$** approach using `std::unordered_set` to replace sorting with hash-based lookups.
---
### Day 10: 5 February 2026
---
**Focus:** Matrix Algorithms & Space Optimization

**DSA Practice**
- **Set Matrix Zeroes (LC #73):**
  - **Approach:** **Optimal In-Place** ($O(1)$ Space).
  - **Logic:** Used the **first row** and **first column** as flag arrays to mark rows/cols that need to be zeroed.
  - **Edge Case:** Maintained a separate variable `col0` to handle the overlap at `matrix[0][0]`, preventing the first row's status from corrupting the first column's status.
  - **Complexity:** Time $O(N \times M)$ | Space $O(1)$.
---
### Day 11: 6 February 2026
---
**Focus:** Arrays & Hashing (Prefix Sum)

**DSA Practice**
- **Subarray Sum Equals K (LC #560):**
  - **Approach:** **Prefix Sum + HashMap**.
  - **Logic:** Used the formula `CurrentPrefixSum - k = PreviousPrefixSum` to find valid subarrays.
  - **Technique:** Used a Hash Map to store the frequency of past prefix sums for $O(1)$ lookups.
  - **Edge Case:** Initialized `map[0] = 1` to handle subarrays starting from index 0.
  - **Complexity:** Time $O(N)$ | Space $O(N)$.
---
### Day 12: 9 February 2026
---
**Focus:** Frontend Development (CSS Frameworks)

**Web Development**
- **Tailwind CSS:**
  - **Core Concepts:** Learned the **Utility-First** workflow to style components directly in HTML.
  - **Layouts:** Mastered Flexbox (`flex`, `justify-`, `items-`) and Grid (`grid`, `gap-`) utilities.
  - **Responsiveness:** Understood mobile-first breakpoints (`sm`, `md`, `lg`) and state variants (`hover:`, `focus:`).
  - **Customization:** Learned how to configure `tailwind.config.js` for custom themes.

---
### Day 13: 10 February 2026
---
**Focus:** CS Fundamentals (OS & Networks)

**1. Computer Networks (CN)**
- **Architecture:**
  - **OSI Model:** Deep dive into the 7 layers (Physical to Application) and their specific functions.
  - **Topologies:** Star, Mesh, Bus, and Ring architectures.
  - **Transmission:** Simplex, Half-Duplex, and Full-Duplex modes.
- **Data Communication:**
  - **Signal Metrics:** Studied **Signal-to-Noise Ratio (SNR)** and its impact on data capacity.
  - **Line Coding (Digital-to-Digital):**
    - **Unipolar:** Simple NRZ.
    - **Polar:** NRZ-L, NRZ-I, and RZ (Return to Zero).
    - **Biphase:** Manchester and Differential Manchester.
    - **Bipolar:** AMI (Alternate Mark Inversion).

**2. Operating Systems (OS)**
- **System Structure:**
  - **System Calls:** The interface between User Mode and Kernel Mode.
  - **OS Structures:** Monolithic vs. Microkernel architectures.
- **Process Management:**
  - **Process Life Cycle:** New $\rightarrow$ Ready $\rightarrow$ Running $\rightarrow$ Waiting $\rightarrow$ Terminated.
  - **PCB:** Understood the **Process Control Block** (PID, Program Counter, Registers).
  - **Scheduling:** Basics of how the OS selects processes for the CPU (Context Switching).
---
### Day 14: 11 February 2026
---
**Focus:** Advanced Voting Algorithms & OS Process Management

**1. DSA Practice**
- **Majority Element II (LC #229):**
  - **Approach:** **Extended Boyer-Moore Voting Algorithm**.
  - **Logic:** Maintained **two candidates** and **two counters** since there can be at most two elements appearing more than $\lfloor N/3 \rfloor$ times.
  - **Complexity:** Time $O(N)$ (Two passes: one to find candidates, one to verify) | Space $O(1)$.

**2. Operating Systems (Process Control)**
- **Scheduling & Execution:**
  - **Schedulers:** Studied the roles of Long-term (Job), Short-term (CPU), and Medium-term (Swapping) schedulers.
  - **Context Switch:** Learned how the OS saves the **PCB** (Process Control Block) of the running process and loads the PCB of the next process.
  - **System Calls:** Understood `fork()` to create child processes (where the child gets a copy of the parent's address space).
- **Inter-Process Communication (IPC):**
  - **Shared Memory:** Processes communicate by reading/writing to a common memory block (Faster, but requires synchronization).
  - **Message Passing:** Processes communicate by sending packets via the kernel (Easier to implement, but slower due to system calls).
---
### Day 15: 12 February 2026
---
**Focus:** Interval Manipulation & Bitwise Algorithms

**DSA Practice**
- **Merge Intervals (LC #56):**
  - **Pattern:** **Sorting + Linear Scan**.
  - **Logic:** Sorted intervals by start time. Iterated through the list, merging overlapping intervals whenever `current.start <= last_merged.end`.
  - **Complexity:** Time $O(N \log N)$ (Dominated by sorting) | Space $O(N)$ (Result storage).

- **Count Subarrays with XOR K:**
  - **Pattern:** **Prefix XOR + HashMap**.
  - **Logic:** relied on the property that if `PrefixXOR[i] ^ PrefixXOR[j] = K`, then `PrefixXOR[i] ^ K = PrefixXOR[j]`.
  - **Algorithm:** Maintained a running `xr` (prefix XOR). For every element, checked if `xr ^ k` existed in the map. If yes, added its frequency to the count.
  - **Edge Case:** Initialized `map[0] = 1` to handle subarrays starting from index 0.
  - **Complexity:** Time $O(N)$ | Space $O(N)$.
