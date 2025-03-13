# LeetCode Patterns Strategy

A curated collection of algorithm patterns and essential LeetCode problems that cover approximately 80% of coding interview questions.

## Table of Contents
- [Core Algorithm Patterns](#core-algorithm-patterns)
- [Problem List by Pattern](#problem-list-by-pattern)
- [How to Use This Repository](#how-to-use-this-repository)
- [Contributing](#contributing)

## Core Algorithm Patterns

### 1. Two Pointers
This pattern uses two pointers to iterate through the data structure (often an array) in a single pass, saving time and space.

**When to use:** When dealing with sorted arrays or linked lists and looking for pairs or subarrays with certain properties.

**Implementation tips:**
- Usually involves moving pointers in opposite directions or at different speeds
- Often used to find pairs that sum to a target or to partition arrays

### 2. Sliding Window
This technique involves maintaining a "window" that slides through an array or string to process data in chunks.

**When to use:** For problems involving subarrays, substrings, or when you need to find a continuous sequence that meets certain criteria.

**Implementation tips:**
- Expand the window when adding elements
- Contract the window when removing elements
- Track a variable (sum, max, min) as the window changes

### 3. Binary Search
A divide-and-conquer algorithm that works on sorted data by repeatedly dividing the search space in half.

**When to use:** For sorted arrays or when the problem has a monotonic property.

**Implementation tips:**
- Check edge cases (empty array, single element)
- Be careful about integer overflow with mid calculation
- Use `left + (right - left) / 2` instead of `(left + right) / 2`

### 4. Depth-First Search (DFS)
Explores as far down a branch as possible before backtracking.

**When to use:** For tree/graph traversal, path finding, cycle detection, or exploring all possibilities.

**Implementation tips:**
- Can be implemented recursively or with a stack
- Mark nodes as visited to avoid cycles
- Consider space complexity due to recursion stack

### 5. Breadth-First Search (BFS)
Explores all neighbors at the current depth before moving deeper.

**When to use:** For finding shortest paths, level-order traversal, or when you need the closest solution.

**Implementation tips:**
- Implemented using a queue
- Good for finding shortest path in unweighted graphs
- More space-efficient than DFS for wide trees/graphs

### 6. Dynamic Programming
Breaks down complex problems into overlapping subproblems and stores their solutions.

**When to use:** When a problem has optimal substructure and overlapping subproblems.

**Implementation tips:**
- Define the state clearly
- Establish the recurrence relation
- Determine the base cases
- Consider using tabulation (bottom-up) vs. memoization (top-down)

### 7. Backtracking
A recursive approach that builds candidates and abandons them if they don't satisfy constraints.

**When to use:** For problems involving permutations, combinations, or when you need to explore all possible solutions.

**Implementation tips:**
- Define a clear recursive function with parameters that track state
- Implement a base case that indicates when to stop recursion
- Make a choice, explore recursively, then undo the choice (backtrack)

### 8. Greedy Algorithms
Makes locally optimal choices at each step with the hope of finding a global optimum.

**When to use:** When local optimal choices lead to a global optimal solution.

**Implementation tips:**
- Sort data first in many cases
- Consider edge cases carefully
- Prove that the greedy approach works

### 9. Union Find (Disjoint Set)
A data structure that keeps track of elements partitioned into disjoint sets.

**When to use:** For problems involving connected components, cycle detection in undirected graphs, or finding if two elements are in the same set.

**Implementation tips:**
- Implement path compression and union by rank for efficiency
- Find operation identifies the set an element belongs to
- Union operation merges two sets

### 10. Topological Sort
An ordering of vertices in a directed graph where for each directed edge (u, v), vertex u comes before v.

**When to use:** For scheduling problems, task ordering, or dependency resolution.

**Implementation tips:**
- Can be implemented using DFS or BFS (Kahn's algorithm)
- Only works on Directed Acyclic Graphs (DAGs)
- Track in-degrees or use recursion with visited states

## Problem List by Pattern

### Two Pointers
1. [Two Sum II - Input Array Is Sorted (167)](https://leetcode.com/problems/two-sum-ii-input-array-is-sorted/)
2. [Remove Duplicates from Sorted Array (26)](https://leetcode.com/problems/remove-duplicates-from-sorted-array/)
3. [Container With Most Water (11)](https://leetcode.com/problems/container-with-most-water/)
4. [3Sum (15)](https://leetcode.com/problems/3sum/)
5. [Move Zeroes (283)](https://leetcode.com/problems/move-zeroes/)
6. [Valid Palindrome (125)](https://leetcode.com/problems/valid-palindrome/)
7. [Trapping Rain Water (42)](https://leetcode.com/problems/trapping-rain-water/)

### Sliding Window
1. [Maximum Subarray (53)](https://leetcode.com/problems/maximum-subarray/)
2. [Minimum Size Subarray Sum (209)](https://leetcode.com/problems/minimum-size-subarray-sum/)
3. [Longest Substring Without Repeating Characters (3)](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
4. [Find All Anagrams in a String (438)](https://leetcode.com/problems/find-all-anagrams-in-a-string/)
5. [Sliding Window Maximum (239)](https://leetcode.com/problems/sliding-window-maximum/)
6. [Permutation in String (567)](https://leetcode.com/problems/permutation-in-string/)

### Binary Search
1. [Binary Search (704)](https://leetcode.com/problems/binary-search/)
2. [Find First and Last Position of Element in Sorted Array (34)](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
3. [Search in Rotated Sorted Array (33)](https://leetcode.com/problems/search-in-rotated-sorted-array/)
4. [Find Minimum in Rotated Sorted Array (153)](https://leetcode.com/problems/find-minimum-in-rotated-sorted-array/)
5. [Median of Two Sorted Arrays (4)](https://leetcode.com/problems/median-of-two-sorted-arrays/)
6. [Koko Eating Bananas (875)](https://leetcode.com/problems/koko-eating-bananas/)

### Depth-First Search
1. [Number of Islands (200)](https://leetcode.com/problems/number-of-islands/)
2. [Max Area of Island (695)](https://leetcode.com/problems/max-area-of-island/)
3. [Path Sum (112)](https://leetcode.com/problems/path-sum/)
4. [Course Schedule (207)](https://leetcode.com/problems/course-schedule/)
5. [Pacific Atlantic Water Flow (417)](https://leetcode.com/problems/pacific-atlantic-water-flow/)
6. [Word Search (79)](https://leetcode.com/problems/word-search/)

### Breadth-First Search
1. [Binary Tree Level Order Traversal (102)](https://leetcode.com/problems/binary-tree-level-order-traversal/)
2. [Minimum Depth of Binary Tree (111)](https://leetcode.com/problems/minimum-depth-of-binary-tree/)
3. [Word Ladder (127)](https://leetcode.com/problems/word-ladder/)
4. [Rotting Oranges (994)](https://leetcode.com/problems/rotting-oranges/)
5. [Shortest Path in Binary Matrix (1091)](https://leetcode.com/problems/shortest-path-in-binary-matrix/)
6. [Open the Lock (752)](https://leetcode.com/problems/open-the-lock/)

### Dynamic Programming
1. [Climbing Stairs (70)](https://leetcode.com/problems/climbing-stairs/)
2. [Coin Change (322)](https://leetcode.com/problems/coin-change/)
3. [Longest Increasing Subsequence (300)](https://leetcode.com/problems/longest-increasing-subsequence/)
4. [Longest Common Subsequence (1143)](https://leetcode.com/problems/longest-common-subsequence/)
5. [House Robber (198)](https://leetcode.com/problems/house-robber/)
6. [Maximum Product Subarray (152)](https://leetcode.com/problems/maximum-product-subarray/)
7. [Edit Distance (72)](https://leetcode.com/problems/edit-distance/)
8. [0/1 Knapsack](https://leetcode.com/tag/knapsack/) (Various problems)

### Backtracking
1. [Subsets (78)](https://leetcode.com/problems/subsets/)
2. [Permutations (46)](https://leetcode.com/problems/permutations/)
3. [Combination Sum (39)](https://leetcode.com/problems/combination-sum/)
4. [N-Queens (51)](https://leetcode.com/problems/n-queens/)
5. [Letter Combinations of a Phone Number (17)](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)
6. [Palindrome Partitioning (131)](https://leetcode.com/problems/palindrome-partitioning/)

### Greedy
1. [Jump Game (55)](https://leetcode.com/problems/jump-game/)
2. [Gas Station (134)](https://leetcode.com/problems/gas-station/)
3. [Task Scheduler (621)](https://leetcode.com/problems/task-scheduler/)
4. [Minimum Number of Arrows to Burst Balloons (452)](https://leetcode.com/problems/minimum-number-of-arrows-to-burst-balloons/)
5. [Partition Labels (763)](https://leetcode.com/problems/partition-labels/)

### Union Find
1. [Number of Connected Components in an Undirected Graph (323)](https://leetcode.com/problems/number-of-connected-components-in-an-undirected-graph/)
2. [Redundant Connection (684)](https://leetcode.com/problems/redundant-connection/)
3. [Graph Valid Tree (261)](https://leetcode.com/problems/graph-valid-tree/)
4. [Accounts Merge (721)](https://leetcode.com/problems/accounts-merge/)

### Topological Sort
1. [Course Schedule II (210)](https://leetcode.com/problems/course-schedule-ii/)
2. [Alien Dictionary (269)](https://leetcode.com/problems/alien-dictionary/)
3. [Minimum Height Trees (310)](https://leetcode.com/problems/minimum-height-trees/)

### Hash Table
1. [Two Sum (1)](https://leetcode.com/problems/two-sum/)
2. [Group Anagrams (49)](https://leetcode.com/problems/group-anagrams/)
3. [Valid Anagram (242)](https://leetcode.com/problems/valid-anagram/)
4. [LRU Cache (146)](https://leetcode.com/problems/lru-cache/)
5. [Longest Consecutive Sequence (128)](https://leetcode.com/problems/longest-consecutive-sequence/)

### Heap/Priority Queue
1. [Kth Largest Element in an Array (215)](https://leetcode.com/problems/kth-largest-element-in-an-array/)
2. [Merge K Sorted Lists (23)](https://leetcode.com/problems/merge-k-sorted-lists/)
3. [Find Median from Data Stream (295)](https://leetcode.com/problems/find-median-from-data-stream/)
4. [Top K Frequent Elements (347)](https://leetcode.com/problems/top-k-frequent-elements/)

### Linked List
1. [Reverse Linked List (206)](https://leetcode.com/problems/reverse-linked-list/)
2. [Linked List Cycle (141)](https://leetcode.com/problems/linked-list-cycle/)
3. [Merge Two Sorted Lists (21)](https://leetcode.com/problems/merge-two-sorted-lists/)
4. [Remove Nth Node From End of List (19)](https://leetcode.com/problems/remove-nth-node-from-end-of-list/)
5. [LRU Cache (146)](https://leetcode.com/problems/lru-cache/)

### Tree
1. [Maximum Depth of Binary Tree (104)](https://leetcode.com/problems/maximum-depth-of-binary-tree/)
2. [Validate Binary Search Tree (98)](https://leetcode.com/problems/validate-binary-search-tree/)
3. [Invert Binary Tree (226)](https://leetcode.com/problems/invert-binary-tree/)
4. [Lowest Common Ancestor of a Binary Tree (236)](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
5. [Binary Tree Maximum Path Sum (124)](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
6. [Serialize and Deserialize Binary Tree (297)](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/)

## How to Use This Repository

1. **Start with the patterns**: Understand each algorithm pattern before diving into the problems.
2. **Practice methodically**: Work through problems by pattern, not randomly.
3. **Review and revisit**: After solving a problem, review the solution and try to optimize it.
4. **Track your progress**: Mark problems as you complete them to maintain momentum.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request to:

- Add new problems that fit existing patterns
- Suggest new patterns with representative problems
- Improve explanations or implementation tips
- Add solution templates or code examples

## License

This repository is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Thanks to all the contributors who have helped curate this list
- Inspired by the countless software engineers studying for technical interviews
