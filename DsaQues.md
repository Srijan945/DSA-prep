## LeetCode practice — Questions mapped to the 6-week plan

### Week 1 — Foundations + Patterns (pick 20; focus on templates & from-memory coding)

| Topic | Problem | LC # | Status | Notes |
|---|---|---:|:---:|---|
| Sliding window | Longest Substring Without Repeating Characters | 3 | [x] Done | revisit O(n) template HashMap |
| Sliding window | Minimum Window Substring | 76 | [ ] | |
| Sliding window | Sliding Window Maximum | 239 | [x] Done | use deque O(nlogn) |
| Sliding window | Minimum Size Subarray Sum | 209 | [x] Done | two-pointer shrinking window O(n) |
| Sliding window | Subarray Product Less Than K | 713 | [ ] | handle product and left pointer |
| Prefix / Suffix | Product of Array Except Self | 238 | [ ] | |
| Prefix / Suffix | Subarray Sum Equals K | 560 | [ ] | |
| Prefix / Suffix | Maximum Size Subarray Sum Equals k | 325 | [ ] | |
| Binary search / search patterns | Binary Search | 704 | [ ] | |
| Binary search / search patterns | Search in Rotated Sorted Array | 33 | [ ] | |
| Two-pointer | Two Sum II - Input array is sorted | 167 | [ ] | |
| Two-pointer | 3Sum | 15 | [ ] | |
| Two-pointer | Container With Most Water | 11 | [ ] | |
| Two-pointer | Trapping Rain Water | 42 | [ ] | |
| Two-pointer | Remove Duplicates from Sorted Array | 26 | [ ] | |
| Two-pointer | Merge Sorted Array | 88 | [ ] | |
| Two-pointer | Valid Palindrome | 125 | [ ] | |

Week 2 — Graphs (BFS/DFS, topo, Dijkstra, 0-1 BFS, grid BFS) — ~15–20 problems
- BFS / DFS fundamentals & grid: 200. Number of Islands, 127. Word Ladder, 317. Shortest Distance from All Buildings, 329. Longest Increasing Path in a Matrix
- Graph construction / cloning / traversal: 133. Clone Graph, 323. Number of Connected Components in an Undirected Graph, 785. Is Graph Bipartite?
- Topological sort & cycle detection: 207. Course Schedule, 210. Course Schedule II
- Shortest path variants: 743. Network Delay Time (Dijkstra), 787. Cheapest Flights Within K Stops (BFS / Bellman-Ford / Dijkstra)
- 01-matrix / 0-1 BFS style: 542. 01 Matrix

Week 3 — DP Basics (20 problems: 1D DP, grid DP, knapsack family, LIS)
- Simple / 1D: 70. Climbing Stairs, 509. Fibonacci Number, 53. Maximum Subarray, 198. House Robber, 213. House Robber II
- Grid DP: 62. Unique Paths, 63. Unique Paths II, 64. Minimum Path Sum, 221. Maximal Square
- Knapsack family / subset-sum: 416. Partition Equal Subset Sum, 322. Coin Change, 494. Target Sum
- LIS & variants: 300. Longest Increasing Subsequence, 354. Russian Doll Envelopes
- Other DP classics: 139. Word Break, 91. Decode Ways, 72. Edit Distance, 887. Super Egg Drop, 5. Longest Palindromic Substring

Week 4 — Advanced Data Structures (~15: segment tree / fenwick / DSU / heaps)
- Segment tree / BIT / range queries: 307. Range Sum Query - Mutable, 308. Range Sum Query 2D - Mutable, 327. Count of Range Sum
- Fenwick / order-statistics uses: 315. Count of Smaller Numbers After Self, 327. Count of Range Sum (alt approach)
- Disjoint Set Union: 721. Accounts Merge, 547. Number of Provinces, 684. Redundant Connection
- Priority queue / heap practice: 295. Find Median from Data Stream, 480. Sliding Window Median, 973. K Closest Points to Origin, 218. The Skyline Problem

Week 5 — Advanced Graphs (MST, bridges/articulation, Bellman-Ford and variants) — ~15
- MST / minimum connect: 1584. Min Cost to Connect All Points, 1168/1135-style problems (connectivity / min-cost variants)
- Bridges / critical connections / graph articulation: 1192. Critical Connections in a Network, 684. Redundant Connection (cycle detection / DSU)
- Shortest path variants including negative edges: 787. Cheapest Flights Within K Stops (Bellman-Ford style), 743. Network Delay Time
- Additional graph problems to practice advanced techniques: 310-ish / 400-ish medium-hard graph problems (focus on implementing Tarjan, Kosaraju, Kruskal, Prim)

Week 6 — Mixed + Revision (AtCoder DP subset, timed contests, review weaknesses)
- AtCoder DP subset ≈ translate to LeetCode: practice problems that map to AtCoder DP categories (knapsack, LIS, grid DP, digit DP if available)
- Mixed LeetCode picks for revision: re-solve previous weeks' hardest 10 problems from memory, plus:
  - Contest practice: attempt 2 LeetCode Weekly/Biweekly contests per week
  - Hard problems (choose 1/week): e.g., 214. Shortest Palindrome, 4. Median of Two Sorted Arrays, 297. Serialize and Deserialize Binary Tree (pick 1–2 sustained hard problems)

Notes & tips
- Target counts per week: Week1 ≥20, Week2 15–20, Week3 ≈20, Week4 ≈15, Week5 ≈15, Week6 mixed/contests.
- For each problem: write template + solve from memory at least once per weekend.
- Keep a Mistakes Log: record patterns, pitfalls, and one-line corrective notes.

Happy practicing — use this map as a checklist and adapt problem selection to your weak areas.