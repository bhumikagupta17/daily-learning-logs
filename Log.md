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
---
### Day 16: 22 February 2026
---
**Focus:** Frontend Development (React Fundamentals)

**Web Development (React)**
- **Props (Properties):**
  - **Data Flow:** Learned how to pass data dynamically from Parent to Child components.
  - **Immutability:** Understood that props are **read-only** (cannot be modified by the child), ensuring predictable data flow and highly reusable UI components.
- **React Hooks:**
  - **Concept:** Explored how hooks allow functional components to "hook into" React's state and lifecycle features without needing class components.
  - **State Management:** Looked into how state variables (like `useState`) trigger UI re-renders whenever the data changes.
---
### Day 17: 23 February 2026
---
**Focus:** Advanced React Hooks & Optimal Array Merging

**1. Web Development (React)**
- **Advanced Hooks:**
  - **`useEffect`:** Learned how to synchronize a component with external systems (API calls, timers) and control re-renders using the dependency array.
  - **`useRef`:** Persisted mutable data across renders without triggering a re-render, and learned how to directly access DOM nodes.
  - **`useCallback`:** Optimized performance by memoizing functions, preventing unnecessary re-renders when passing callbacks as props down to child components.

**2. DSA Practice (Arrays)**
- **Merge Two Sorted Arrays (Without Extra Space):**
  - **Approach 1: Two Pointers & Swap**
    - **Logic:** Placed pointers at the end of `arr1` and start of `arr2`. Swapped elements if `arr1[i] > arr2[j]`, then sorted both arrays to restore their internal order.
    - **Complexity:** Time $O(N \log N + M \log M)$ | Space $O(1)$.
  - **Approach 2: The Gap Method (Optimal)**
    - **Logic:** Applied the intuition of **Shell Sort**. Calculated an initial `gap = ceil((N+M)/2)` to compare and swap elements across the boundary of both arrays. Continually halved the gap until it reached 0.
    - **Complexity:** Time $O((N+M) \log(N+M))$ | Space $O(1)$.
---
### Day 18: 28 February 2026
---
**Focus:** Mobile App Deployment & Advanced Divide and Conquer

**1. App Development (Flutter)**
- **Subscription Tracker App:**
  - **Milestone:** Successfully completed the core development of the mobile app.
  - **Implementation:** Finalized the UI/UX and ensured state management flows correctly across all screens.

**2. DSA Practice (Divide & Conquer)**
- **Count Inversions:**
  - **Approach:** Modified **Merge Sort**.
  - **Logic:** While merging two sorted halves, if `left[i] > right[j]`, then all remaining elements in the left half are also strictly greater than `right[j]`. Added `(mid - i + 1)` to the inversion count.
  - **Complexity:** Time $O(N \log N)$ | Space $O(N)$.

- **Reverse Pairs (LC #493):**
  - **Approach:** Advanced **Merge Sort** application.
  - **Logic:** Counted pairs where `i < j` and `nums[i] > 2 * nums[j]`. 
  - **Crucial Step:** Performed the counting step *before* the standard merge process. Used a two-pointer approach across the left and right halves to efficiently count valid pairs without disrupting the sorting algorithm.
  - **Complexity:** Time $O(N \log N)$ | Space $O(N)$.
---
### Day 19: 01 March 2026
---
**Focus:** Subarray Optimization, Greedy Logic & Sorting Fundamentals

**1. DSA Practice (LeetCode)**
- **Maximum Product Subarray (LC #152):**
  - **Approach:** **Prefix and Suffix Product** (or modified Kadane's).
  - **Logic:** Because multiplying two negative numbers yields a positive result, tracking just the maximum isn't enough. Maintained both a running prefix product (left-to-right) and suffix product (right-to-left), resetting to 1 when encountering a 0. The global max of these is the answer.
  - **Complexity:** Time $O(N)$ | Space $O(1)$.

- **Partitioning Into Minimum Number Of Deci-Binary Numbers (LC #1689):**
  - **Approach:** **Greedy / String Iteration**.
  - **Logic:** Recognized the mathematical trick: a deci-binary number only consists of 0s and 1s. Therefore, the minimum number of partitions required to sum up to the target string is simply equal to the **maximum digit** present in the string.
  - **Complexity:** Time $O(N)$ (where N is string length) | Space $O(1)$.

**2. Core CS Revision**
- **Sorting Algorithms (Divide & Conquer):**
  - **Merge Sort:** Revised the stable $O(N \log N)$ approach that requires $O(N)$ extra space for the temporary merge array.
  - **Quick Sort:** Revised the in-place partitioning logic (using a pivot). Noted that while the average case is $O(N \log N)$, the worst-case time complexity degrades to $O(N^2)$ if the pivot choices are poor (e.g., already sorted array with end-element pivot).
---
### Day 20: 02 March 2026
---
**Focus:** Search Algorithms, Matrix Grids & React Routing

**1. DSA Practice**
- **Binary Search (Revision):**
  - **Core Logic:** Revised the standard $O(\log N)$ divide-and-conquer search on sorted arrays. 
  - **Safety Check:** Reinforced using `mid = left + (right - left) / 2` to prevent integer overflow instead of `(left + right) / 2`.
- **Minimum Swaps to Arrange a Binary Grid (LC #1536 - DCC):**
  - **Approach:** **Greedy + Adjacent Swaps**.
  - **Logic:** 1. Converted the matrix into a 1D array representing the number of **trailing zeros** in each row.
    2. For each row `i`, the requirement is to have at least `n - 1 - i` trailing zeros.
    3. Greedily searched for the closest valid row below `i` and simulated adjacent swaps to "bubble" it up to the current position.
  - **Complexity:** Time $O(N^2)$ | Space $O(N)$.

**2. Web Development (React)**
- **React Router:**
  - **Routing Fundamentals:** Learned how to implement client-side routing to navigate between pages without reloading the browser.
  - **Data Fetching (`useLoaderData`):** - Explored the modern React Router v6.4+ data APIs.
    - Understood how `loader` functions allow you to fetch data *before* the route renders, preventing the "loading spinner" waterfall effect.
    - Used the `useLoaderData` hook inside the component to access the pre-fetched data.
---
### Day 21: 03 March 2026
---
**Focus:** Recursion & Divide and Conquer

**DSA Practice**
- **Find Kth Bit in Nth Binary String (LC #1545 - DCC):**
  - **Approach:** **Recursion / Pattern Observation**.
  - **Logic:** Recognized that generating the full string ($S_n = S_{n-1} + "1" + \text{reverse}(\text{invert}(S_{n-1}))$) takes too much memory. Instead, used the property that the length is $2^n - 1$ and the middle bit is always '1'.
  - **Algorithm:** 1. If $k$ is exactly in the middle ($k = 2^{n-1}$), return '1'.
    2. If $k$ is in the left half ($k < 2^{n-1}$), recursively search in $S_{n-1}$.
    3. If $k$ is in the right half ($k > 2^{n-1}$), find its mirrored position in the left half, recursively search, and **invert** the result.
  - **Complexity:** Time $O(N)$ (Only making $N$ recursive calls) | Space $O(N)$ (Call stack).
---
### Day 22: 05 March 2026
---
**Focus:** String Optimization & Advanced Data Structures

**1. DSA Practice (Strings)**
- **Minimum Changes To Make Alternating Binary String (LC #1758):**
  - **Approach:** **Pattern Matching & Math ($n - \text{count}$)**.
  - **Logic:** Recognized that an alternating binary string can only take two forms: starting with '0' (`010101...`) or starting with '1' (`101010...`).
  - **Optimization:** Instead of checking both patterns independently, calculated the differences against the '0'-starting pattern (`count`). The differences for the '1'-starting pattern is simply `n - count`. Returned $\min(\text{count}, n - \text{count})$.
  - **Complexity:** Time $O(N)$ (Single Pass) | Space $O(1)$.

**2. Advanced Data Structures (Heaps)**
- **Binomial Heaps:**
  - **Structure:** Learned that it is implemented as a collection (forest) of **Binomial Trees** (where a tree of order $k$ has exactly $2^k$ nodes).
  - **Key Operations:**
    - **Union/Merge:** The most critical operation. Merging two binomial heaps takes $O(\log N)$ time, which is significantly faster than standard binary heaps ($O(N)$).
    - **Insert & Extract-Min:** Both operate in $O(\log N)$ time by linking trees of the same degree.
  - **Use Case:** Highly efficient for priority queues where merging two queues frequently is a primary requirement.
---
### Day 23: 06 March 2026
---
**Focus:** String Validation & Advanced Priority Queues

**1. DSA Practice (Strings)**
- **Check if Binary String Has at Most One Segment of Ones (LC #1784):**
  - **Approach:** **Pattern Matching / Substring Search**.
  - **Logic:** The problem states the string never contains leading zeros (it always starts with '1'). Therefore, the *only* way to have more than one segment of '1's is if a '1' appears *after* a '0'. 
  - **Optimization:** Instead of iterating and counting segments, simply checked if the substring `"01"` exists in the string. If `"01"` is found, return `false`; otherwise, return `true`.
  - **Complexity:** Time $O(N)$ | Space $O(1)$.

**2. Advanced Data Structures (Heaps)**
- **Fibonacci Heaps:**
  - **Structure:** A more relaxed collection of trees compared to Binomial Heaps, satisfying the min-heap property but allowing trees to be less rigidly structured.
  - **Key Operations (Amortized Time):**
    - **Insert, Find-Min, Union/Merge:** Extremely fast at $O(1)$.
    - **Extract-Min & Delete:** $O(\log N)$.
    - **Decrease-Key:** $O(1)$ amortized. (This is the defining feature that makes it vastly superior to Binary/Binomial heaps for certain algorithms).
  - **Use Case:** The theoretical optimal choice for priority queues in dense graph algorithms, specifically heavily optimizing **Dijkstra's Shortest Path** and **Prim's Minimum Spanning Tree**.
---
### Day 24: 07 March 2026
---
**Focus:** Advanced Sliding Window, Balanced Trees & SWE Cost Models

**1. DSA Practice (Strings & Arrays)**
- **Minimum Number of Flips to Make the Binary String Alternating (LC #1888):**
  - **Approach:** **Sliding Window on Doubled String**.
  - **Logic:** The operation of removing the first character and appending it to the end is effectively a circular shift. To simulate this without modifying the array in $O(N^2)$ time, concatenated the string to itself (`s + s`).
  - **Algorithm:** Generated two target alternating patterns (`0101...` and `1010...`) of length `2n`. Used a sliding window of size `n` over the doubled string to count mismatches against both patterns, tracking the minimum flips needed.
  - **Complexity:** Time $O(N)$ | Space $O(N)$.

**2. Advanced Data Structures**
- **Red-Black (RB) Trees:**
  - **Structure:** A self-balancing Binary Search Tree that guarantees $O(\log N)$ time for search, insert, and delete operations.
  - **Core Properties:**
    1. Every node is colored either Red or Black.
    2. The Root is always Black.
    3. No two adjacent nodes can be Red (a Red node cannot have a Red parent or Red child).
    4. **Black-Height Property:** Every path from a node to its descendant NULL pointers contains the exact same number of Black nodes.
  - **Rebalancing:** Handled via color flipping and Left/Right tree rotations.

**3. Software Engineering Principles**
- **COCOMO (Constructive Cost Model):**
  - **Concept:** An algorithmic model used to estimate software project effort, cost, and schedule based on the size of the codebase (measured in KLOC - Kilo Lines of Code).
  - **Project Categories:**
    - **Organic:** Small teams, familiar environments, flexible requirements.
    - **Semi-detached:** Medium-sized teams, mixed experience, moderate constraints.
    - **Embedded:** Complex hardware/software systems with extremely strict constraints and high innovation requirements.
---
### Day 25: 08 March 2026
---
**Focus:** String Algorithms & DAA Exam Preparation

**1. DSA Practice (Strings)**
- **Find Unique Binary String (LC #1980):**
  - **Approach:** **Cantor's Diagonalization**.
  - **Logic:** Instead of generating all $2^N$ possible strings or using a Hash Set to find the missing one, constructed the missing string on the fly. Iterated through the given array of strings, taking the $i$-th character of the $i$-th string, and **flipped** it (if '0' make '1', if '1' make '0'). 
  - **Result:** This guarantees the newly formed string differs from every existing string by at least one character.
  - **Complexity:** Time $O(N)$ | Space $O(N)$ (to store the resulting string).

**2. Core CS Revision**
- **Design and Analysis of Algorithms (DAA):**
  - Dedicated the day to revising core theoretical concepts for tomorrow's university exam.
  - Focused on algorithmic paradigms, asymptotic complexity, and mathematical analysis of standard algorithms.
---
### Day 26: 09 March 2026
---
**Focus:** 3D Dynamic Programming & OS Synchronization (Mid-Sem Prep)

**1. DSA Practice (Dynamic Programming)**
- **Find All Possible Stable Binary Arrays I (LC #3129):**
  - **Approach:** **Multi-dimensional DP**.
  - **Logic:** Maintained a 3D state `dp[i][j][last_bit]` representing the number of valid arrays using `i` zeros, `j` ones, and ending in `last_bit` (0 or 1). 
  - **Constraint Handling:** To ensure no sequence of identical bits exceeds `limit`, the transition logic adds valid previous states and strictly subtracts the invalid configurations where consecutive bits surpass the boundary.
  - **Complexity:** Time $O(\text{zero} \times \text{one})$ | Space $O(\text{zero} \times \text{one})$.

**2. Core CS Revision (Operating Systems)**
- **Process Synchronization:**
  - **The Critical Section Problem:** Studied race conditions where multiple processes access shared resources concurrently. Learned the three strict requirements for a valid solution: Mutual Exclusion, Progress, and Bounded Waiting.
  - **Synchronization Hardware & Software:** Revised Peterson's Solution (for two processes) and hardware instructions like `TestAndSet`.
  - **Mutex & Semaphores:** Differentiated between Mutex (locking mechanism for mutual exclusion) and Semaphores (signaling mechanism using integer variables and `wait()`/`signal()` operations).
---
### Day 27: 10 March 2026
---
**Focus:** Advanced DP Optimization & SE Mid-Sem Exam

**1. DSA Practice (Dynamic Programming)**
- **Find All Possible Stable Binary Arrays II (LC #3130):**
  - **Approach:** **Optimized 3D DP ($O(1)$ Transitions)**.
  - **Logic:** Built upon the logic from Part I, but optimized the inner loop to handle the stricter constraints. Instead of iterating up to `limit` for each state, optimized the transition by taking the total valid combinations ending in the opposite bit, and subtracting only the specific configurations that just exceeded the `limit`.
  - **Algorithm:** - `dp[i][j][0] = (dp[i-1][j][0] + dp[i-1][j][1]) % MOD`
    - If `i > limit`, subtract the invalid state: `- dp[i - limit - 1][j][1]`
  - **Complexity:** Time $O(\text{zero} \times \text{one})$ | Space $O(\text{zero} \times \text{one})$.

**2. Core CS / Academics**
- **Software Engineering (Mid-Semester Exam):**
  - Successfully completed the SE mid-sem exam, testing knowledge on core Software Engineering principles, process models, decision tables, and cost estimation models (like COCOMO).
---
### Day 28: 11 March 2026
---
**Focus:** Bitwise Operations & Masking

**DSA Practice**
- **Complement of Base 10 Integer (LC #1009):**
  - **Approach:** **Bitwise Masking & XOR**.
  - **Logic:** The standard bitwise NOT operator (`~`) flips all 32 bits, which turns the leading zeros into ones (producing a negative number). To only flip the relevant bits, constructed a mask of all `1`s that is exactly the same bit-length as the number.
  - **Algorithm:** 1. If `n == 0`, return `1` (edge case).
    2. Found the bit length by shifting a mask left and adding 1 (`mask = (mask << 1) | 1`) until `mask` was greater than or equal to `n`.
    3. Returned `n ^ mask` (XORing with all `1`s cleanly flips the target bits).
  - **Complexity:** Time $O(\log N)$ (number of bits) | Space $O(1)$.
