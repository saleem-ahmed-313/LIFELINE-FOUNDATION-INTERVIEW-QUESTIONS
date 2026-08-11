<style>
  :root {
    --neon-cyan: #00f0ff;
    --neon-magenta: #ff00aa;
    --bg-dark: #05050a;
    --text-light: #e0f7fa;
  }
  
  @keyframes neonGlow {
    0%, 100% { text-shadow: 0 0 5px var(--neon-cyan), 0 0 10px var(--neon-cyan); color: var(--text-light); }
    50% { text-shadow: 0 0 20px var(--neon-cyan), 0 0 30px var(--neon-magenta), 0 0 40px var(--neon-cyan); color: #ffffff; }
  }
  
  @keyframes scanline {
    0% { top: 0%; opacity: 0; }
    10% { opacity: 0.5; }
    90% { opacity: 0.5; }
    100% { top: 100%; opacity: 0; }
  }
  
  @keyframes pulseAlert {
    0%, 100% { opacity: 0.8; transform: scale(1); border-left-color: var(--neon-magenta); }
    50% { opacity: 1; transform: scale(1.01); border-left-color: #ff4d4d; }
  }
  
  @keyframes bootUp {
    0% { opacity: 0; transform: translateY(30px); filter: blur(5px); }
    100% { opacity: 1; transform: translateY(0); filter: blur(0); }
  }

  @keyframes terminalBlink {
    0%, 100% { opacity: 1; }
    50% { opacity: 0; }
  }

  body {
    background-color: var(--bg-dark);
    color: var(--text-light);
    font-family: 'Courier New', Courier, monospace;
    line-height: 1.6;
  }

  .scanline {
    position: fixed;
    left: 0;
    width: 100%;
    height: 15px;
    background: linear-gradient(to bottom, transparent, rgba(0, 240, 255, 0.2), transparent);
    animation: scanline 4s linear infinite;
    pointer-events: none;
    z-index: 9999;
  }

  .cyber-title {
    animation: neonGlow 4s infinite, bootUp 1s ease-out forwards;
    text-align: center;
    letter-spacing: 3px;
    border-bottom: 2px solid var(--neon-cyan);
    padding-bottom: 15px;
    margin-bottom: 30px;
  }

  .alert-box {
    animation: pulseAlert 2s infinite;
    border-left: 5px solid var(--neon-magenta);
    padding: 15px 20px;
    background: rgba(255, 0, 85, 0.08);
    margin: 25px 0;
    border-radius: 0 8px 8px 0;
    backdrop-filter: blur(4px);
  }

  .data-node {
    animation: bootUp 0.8s ease-out forwards;
    border: 1px solid rgba(0, 240, 255, 0.3);
    border-radius: 12px;
    padding: 25px;
    margin-bottom: 40px;
    background: linear-gradient(145deg, rgba(0, 240, 255, 0.03), rgba(0,0,0,0.5));
    box-shadow: 0 0 20px rgba(0, 240, 255, 0.05);
    transition: all 0.3s ease;
  }

  .data-node:hover {
    border-color: var(--neon-cyan);
    box-shadow: 0 0 30px rgba(0, 240, 255, 0.15);
  }

  table {
    width: 100%;
    border-collapse: separate;
    border-spacing: 0 8px;
    font-family: monospace;
  }

  th {
    background: rgba(0, 240, 255, 0.15);
    color: var(--neon-cyan);
    text-align: left;
    padding: 12px 15px;
    border: 1px solid var(--neon-cyan);
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  td {
    background: rgba(255, 255, 255, 0.02);
    border: 1px solid #2a2a35;
    padding: 12px 15px;
    transition: all 0.3s ease;
  }

  tr:hover td {
    background: rgba(255, 0, 170, 0.1);
    border-color: var(--neon-magenta);
    transform: translateX(5px);
  }

  .terminal-block {
    background: #0d0d14;
    border: 1px solid #333;
    border-radius: 8px;
    padding: 15px;
    margin: 20px 0;
    position: relative;
  }

  .terminal-block::before {
    content: "root@nexus:~# ";
    color: var(--neon-magenta);
    font-weight: bold;
  }

  .blink-cursor::after {
    content: "▊";
    animation: terminalBlink 1s step-end infinite;
    color: var(--neon-cyan);
    margin-left: 5px;
  }

  a {
    color: var(--neon-cyan);
    text-decoration: none;
    border-bottom: 1px dashed var(--neon-cyan);
    transition: all 0.2s;
  }

  a:hover {
    color: var(--neon-magenta);
    border-bottom: 1px solid var(--neon-magenta);
    text-shadow: 0 0 8px var(--neon-magenta);
  }
</style>

<div class="scanline"></div>

# <h1 class="cyber-title">▰▰▰ NEXUS MAINFRAME // INTERVIEW PROTOCOL v4.2 ▰▰▰</h1>

<div class="terminal-block">
  <span style="color: var(--neon-cyan);">SYSTEM STATUS:</span> 🟢 ONLINE | <span style="color: var(--neon-cyan);">UPLINK:</span> SECURE | <span style="color: var(--neon-cyan);">BUILD:</span> 2026.08.12 <span class="blink-cursor"></span>
</div>

---

## <h2 style="color: var(--neon-magenta); border-bottom: 1px solid #333; padding-bottom: 10px;">⚠️ [ DIRECTIVE 01 ] CORE OPERATIONAL RULES</h2>

<div class="alert-box">
  <strong>⚠️ IMPORTANT RULES</strong>
</div>

### 🧩 One Chance Only  
If you fail the interview, **no second attempt** will be given. Prepare well before attending.

### 🚫 No Mugging Up  
Don’t memorize code — you must **write and explain** the logic in your own words.  
We focus on **understanding**, not memorization.

### 💻 Language Flexibility  
You can **code in any language** — Python, C, C++, Java, or JavaScript.  
What matters most is your **approach**, **clarity**, and **problem-solving skill**.

### 🚨 Dynamic Mutation Protocol
Some questions **change every month**.  
Take a snapshot of your assigned question before coming to the interview.

---

## <h2 style="color: var(--neon-magenta); border-bottom: 1px solid #333; padding-bottom: 10px;">🏦 [ DIRECTIVE 02 ] RESOURCE ALLOCATION (BANK UPLINK)</h2>

<div class="alert-box">
  🎯 <strong>CRITICAL OVERRIDE:</strong><br>
  The <strong>scholarship amount will be transferred directly to the official college/institute bank account</strong>.<br>
  <code style="color: #ff4d4d; font-weight: bold;">ERROR 403:</code> No direct transfer will be made to the student’s personal account.
</div>

<table>
  <thead>
    <tr>
      <th>#</th>
      <th>Detail</th>
      <th>Information</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>🏛️ <strong>Account Name</strong></td>
      <td><code>[ REDACTED / AWAITING INPUT ]</code></td>
    </tr>
    <tr>
      <td>2</td>
      <td>🏦 <strong>Bank Name</strong></td>
      <td><code>[ REDACTED / AWAITING INPUT ]</code></td>
    </tr>
    <tr>
      <td>3</td>
      <td>🔢 <strong>Account Number</strong></td>
      <td><code>[ REDACTED / AWAITING INPUT ]</code></td>
    </tr>
    <tr>
      <td>4</td>
      <td>🏧 <strong>IFSC Code</strong></td>
      <td><code>[ REDACTED / AWAITING INPUT ]</code></td>
    </tr>
    <tr>
      <td>5</td>
      <td>📍 <strong>Branch Name</strong></td>
      <td><code>[ REDACTED / AWAITING INPUT ]</code></td>
    </tr>
  </tbody>
</table>

> 🏆 **REWARD TRIGGER:** If you **crack our interview**, you’ll receive a **scholarship**.

---

<div class="data-node">
  <h2 style="color: var(--neon-cyan); margin-top: 0;">🎓 [ DATA NODE ALPHA ] 2nd Year Engineering / BCA / BSc Students</h2>
  <p><strong>15 Easy-Level DSA Questions</strong> for <strong>2nd Year</strong> students (CSE, BCA, and BSc).</p>

  <h3 style="color: #fff; border-left: 4px solid var(--neon-cyan); padding-left: 10px;">🧠 Question List (Easy Level)</h3>

  | # | Question | Description | Practice Link |
  |---|-----------|--------------|----------------|
  | 1 | **Linear Search** | Search for an element in an unsorted array using linear traversal. | [GFG – Linear Search](https://www.geeksforgeeks.org/linear-search/) |
  | 2 | **Binary Search** | Search for an element in a sorted array using binary search technique. | [LeetCode – Binary Search](https://leetcode.com/problems/binary-search/) |
  | 3 | **Bubble Sort** | Sort an array in ascending order using bubble sort algorithm. | [GFG – Bubble Sort](https://www.geeksforgeeks.org/bubble-sort/) |
  | 4 | **Prime Number Check** | Determine whether a given number is prime. | [GFG – Check Prime](https://www.geeksforgeeks.org/c-program-to-check-prime-number/) |
  | 5 | **Factorial of a Number** | Compute factorial of a number using recursion or iteration. | [GFG – Factorial](https://www.geeksforgeeks.org/program-for-factorial-of-a-number/) |
  | 6 | **Fibonacci Number** | Print the first n Fibonacci numbers or find nth term. | [GFG – Fibonacci Series](https://www.geeksforgeeks.org/program-for-nth-fibonacci-number/) |
  | 7 | **Palindrome Number** | Check if a given integer reads the same backward and forward. | [LeetCode – Palindrome Number](https://leetcode.com/problems/palindrome-number/) |
  | 8 | **Palindrome String** | Check if a given string is a palindrome. | [GFG – Palindrome String](https://www.geeksforgeeks.org/problems/palindrome-string0817/1) |
  | 9 | **Reverse a String** | Reverse a given string without using built-in reverse functions. | [GFG – Reverse String](https://www.geeksforgeeks.org/reverse-a-string-in-c-cpp-different-methods/) |
  | 10 | **Find Duplicate Elements in Array** | Detect and print duplicate elements in an array. | [GFG – Find Duplicates](https://www.geeksforgeeks.org/find-duplicates-in-on-time-and-constant-extra-space/) |
  | 11 | **Find Max & Min in Array** | Find maximum and minimum elements in an array in one pass. | [GFG – Max & Min in Array](https://www.geeksforgeeks.org/maximum-and-minimum-in-an-array/) |
  | 12 | **Stack Implementation (Array)** | Implement push, pop, and display operations using an array. | [GFG – Stack Using Array](https://www.geeksforgeeks.org/stack-data-structure-introduction-program/) |
  | 13 | **Queue Implementation (Array)** | Implement enqueue and dequeue operations using an array. | [GFG – Queue Using Array](https://www.geeksforgeeks.org/queue-set-1introduction-and-array-implementation/) |
  | 14 | **Running Sum of 1D Array** | Return running sum of elements (prefix sum). | [LeetCode – Running Sum](https://leetcode.com/problems/running-sum-of-1d-array/) |
  | 15 | **Valid Palindrome (String)** | Check if a given sentence is palindrome ignoring case and punctuation. | [LeetCode – Valid Palindrome](https://leetcode.com/problems/valid-palindrome/) |
</div>

---

<div class="data-node">
  <h2 style="color: var(--neon-cyan); margin-top: 0;">🎓 [ DATA NODE BETA ] 3rd Year Engineering / BCA / BSc Students</h2>
  
  <div class="alert-box">
    ⚡ <strong>Important Note:</strong><br>
    All <strong>2nd Year Engineering questions</strong> are <strong>also included</strong> for 3rd Year students.<br>
    You are expected to be comfortable with all <strong>15 questions from the 2nd Year list</strong>, plus the <strong>10 new questions</strong> listed below.
  </div>

  <h3 style="color: #fff; border-left: 4px solid var(--neon-cyan); padding-left: 10px;">🧠 Additional 10 Questions (Medium Level)</h3>

  | # | Question | Description | Practice Link |
  |---|-----------|--------------|----------------|
  | 1 | **Find Missing Number in Array** | Given `n` numbers in range `1...n+1`, find the missing one. | [LeetCode – Missing Number](https://leetcode.com/problems/missing-number/) |
  | 2 | **Move Zeroes to End** | Move all zeros in an array to the end while maintaining relative order. | [LeetCode – Move Zeroes](https://leetcode.com/problems/move-zeroes/) |
  | 3 | **Merge Two Sorted Arrays** | Merge two sorted arrays into one sorted array without using extra sort. | [LeetCode – Merge Sorted Array](https://leetcode.com/problems/merge-sorted-array/) |
  | 4 | **Count Frequency of Elements** | Count how many times each element appears in an array. | [GFG – Count Frequencies](https://www.geeksforgeeks.org/count-frequencies-of-array-elements-in-range-1-to-n/) |
  | 5 | **Reverse a Linked List** | Reverse a singly linked list iteratively or recursively. | [LeetCode – Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/) |
  | 6 | **Find Middle Element of Linked List** | Return the middle node of a linked list. | [LeetCode – Middle of the Linked List](https://leetcode.com/problems/middle-of-the-linked-list/) |
  | 7 | **Valid Parentheses** | Check if parentheses in a string are balanced using a stack. | [LeetCode – Valid Parentheses](https://leetcode.com/problems/valid-parentheses/) |
  | 8 | **Maximum Subarray Sum (Kadane’s Algorithm)** | Find contiguous subarray with the maximum sum. | [LeetCode – Maximum Subarray](https://leetcode.com/problems/maximum-subarray/) |
  | 9 | **Remove Duplicates from Sorted Array** | Remove duplicates in-place from a sorted array. | [LeetCode – Remove Duplicates](https://leetcode.com/problems/remove-duplicates-from-sorted-array/) |
  | 10 | **Find Intersection of Two Arrays** | Return the intersection of two integer arrays. | [LeetCode – Intersection of Two Arrays](https://leetcode.com/problems/intersection-of-two-arrays/) |
</div>

---

<div class="data-node">
  <h2 style="color: var(--neon-cyan); margin-top: 0;">🎓 [ DATA NODE GAMMA ] 4th Year Engineering / BCA / MCA / MSC / BSc Students</h2>
  
  <div class="alert-box">
    ⚡ <strong>Important Note:</strong><br>
    - All <strong>2nd Year questions (15)</strong> and <strong>3rd Year questions (10)</strong> are <strong>also included</strong>.<br>
    - You must be thorough with all previous questions before attempting this set.<br>
    - The questions below are <strong>advanced-level</strong> and test recursion, graph traversal, and hashing concepts.
  </div>

  <h3 style="color: #fff; border-left: 4px solid var(--neon-cyan); padding-left: 10px;">🧠 Additional 10 Questions (Medium–Hard Level)</h3>

  | # | Question | Description | Practice Link |
  |---|-----------|--------------|----------------|
  | 1 | **Two Sum** | Find two numbers in an array that add up to a target value using HashMap. | [LeetCode – Two Sum](https://leetcode.com/problems/two-sum/) |
  | 2 | **Valid Anagram** | Check if two strings are anagrams of each other using HashMap. | [LeetCode – Valid Anagram](https://leetcode.com/problems/valid-anagram/) |
  | 3 | **DFS Traversal (Graph)** | Implement Depth First Search (DFS) on a graph using recursion. | [GFG – DFS Traversal](https://www.geeksforgeeks.org/depth-first-search-or-dfs-for-a-graph/) |
  | 4 | **BFS Traversal (Graph)** | Implement Breadth First Search (BFS) on a graph using a queue. | [GFG – BFS Traversal](https://www.geeksforgeeks.org/breadth-first-search-or-bfs-for-a-graph/) |
  | 5 | **Climbing Stairs (Recursion + DP)** | Find number of distinct ways to climb `n` stairs (Fibonacci pattern). | [LeetCode – Climbing Stairs](https://leetcode.com/problems/climbing-stairs/) |
  | 6 | **Merge Two Linked Lists** | Merge two sorted linked lists into one sorted list. | [LeetCode – Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/) |
  | 7 | **Longest Substring Without Repeating Characters** | Find the length of the longest substring without repeating characters. | [LeetCode – Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/) |
  | 8 | **Maximum Depth of Binary Tree (Recursion)** | Compute the maximum depth of a binary tree recursively. | [LeetCode – Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/) |
  | 9 | **Detect Cycle in Linked List** | Determine if a linked list contains a cycle using fast & slow pointers. | [LeetCode – Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/) |
  | 10 | **Number of Islands (DFS/BFS)** | Count the number of islands in a 2D grid using DFS or BFS traversal. | [LeetCode – Number of Islands](https://leetcode.com/problems/number-of-islands/) |
</div>

<div class="terminal-block">
  <span style="color: var(--neon-cyan);">[ END OF TRANSMISSION ]</span> &gt; May your logic be flawless and your syntax pure.<span class="blink-cursor"></span>
</div>
