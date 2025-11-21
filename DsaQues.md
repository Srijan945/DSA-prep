## LeetCode practice — Questions mapped to the 6-week plan

### Week 1 — Foundations + Patterns (pick 20; focus on templates & from-memory coding)

| Topic | Problem | LC # | Status | Notes |
|---|---|---:|:---:|---|
| Sliding window | Longest Substring Without Repeating Characters | 3 | [x] Done | revisit O(n) template HashMap |
| Sliding window | Minimum Window Substring | 76 | [x] Done| O(n+m) solution Freq Array|
| Sliding window | Sliding Window Maximum | 239 | [x] Done | use deque O(nlogn) |
| Sliding window | Minimum Size Subarray Sum | 209 | [x] Done | two-pointer shrinking window O(n) |
| Sliding window | Subarray Product Less Than K | 713 | [x] Done | handle product and left pointer |
| Prefix / Suffix | Product of Array Except Self | 238 | [x] Done | Create prefix and suffix product array |
| Prefix / Suffix | Subarray Sum Equals K | 560 | [x] Done| Hash Table but check zero condition|
| Prefix / Suffix | Maximum Size Subarray Sum Equals k | 325 | [O] | Premium leetcode|
| Binary search / search patterns | Binary Search | 704 | [x] Done | |
| Binary search / search patterns | Search in Rotated Sorted Array | 33 | [ ] | |
| Two-pointer | Two Sum II - Input array is sorted | 167 | [x] Done | O(n) TC O(1) SC|
| Two-pointer | 3Sum | 15 | [x] Done | |
| Two-pointer | Container With Most Water | 11 | [x] Done | |
| Two-pointer | Trapping Rain Water | 42 | [x] Done | good for learning see again|
| Two-pointer | Remove Duplicates from Sorted Array | 26 | [x] Done | |
| Two-pointer | Merge Sorted Array | 88 | [ ] | |
| Two-pointer | Valid Palindrome | 125 | [x] Done|  |

### Week 2 — Graphs (BFS/DFS, topo, Dijkstra, 0-1 BFS, grid BFS)

| Topic | Problem | LC # | Status | Notes |
|---|---|---:|:---:|---|
| Grid BFS / islands | Number of Islands | 200 | [ ] | |
| Shortest path / BFS | Word Ladder | 127 | [ ] | |
| Grid shortest distances | Shortest Distance from All Buildings | 317 | [ ] | multi-source BFS |
| Graph DP / DFS | Longest Increasing Path in a Matrix | 329 | [ ] | DFS + memo |
| Graph clone | Clone Graph | 133 | [ ] | BFS/DFS + map |
| Connected components | Number of Connected Components in an Undirected Graph | 323 | [ ] | DSU / DFS |
| Graph coloring | Is Graph Bipartite? | 785 | [ ] | BFS coloring |
| Topological sort | Course Schedule | 207 | [ ] | detect cycle |
| Topological + order | Course Schedule II | 210 | [ ] | produce ordering |
| Shortest path (Dijkstra) | Network Delay Time | 743 | [ ] | Dijkstra |
| Shortest path variants | Cheapest Flights Within K Stops | 787 | [ ] | BFS / Dijkstra / Bellman-Ford |
| 0-1 BFS style | 01 Matrix | 542 | [ ] | multi-source BFS |

### Week 3 — DP Basics (1D DP, Grid DP, Knapsack, LIS)

| Topic | Problem | LC # | Status | Notes |
|---|---|---:|:---:|---|
| 1D DP | Climbing Stairs | 70 | [ ] | simple rec->iter |
| 1D DP | Fibonacci Number | 509 | [ ] | memo/iter |
| 1D DP | Maximum Subarray | 53 | [ ] | Kadane |
| 1D DP | House Robber | 198 | [ ] | DP rolling |
| 1D DP | House Robber II | 213 | [ ] | circular case |
| Grid DP | Unique Paths | 62 | [ ] | combinatorics/DP |
| Grid DP | Unique Paths II | 63 | [ ] | obstacles |
| Grid DP | Minimum Path Sum | 64 | [ ] | DP |
| Grid DP | Maximal Square | 221 | [ ] | DP |
| Knapsack | Partition Equal Subset Sum | 416 | [ ] | subset-sum DP |
| Knapsack | Coin Change | 322 | [ ] | unbounded knapsack |
| Knapsack | Target Sum | 494 | [ ] | transform to subset-sum |
| LIS | Longest Increasing Subsequence | 300 | [ ] | DP / patience |
| LIS variant | Russian Doll Envelopes | 354 | [ ] | LIS + sort |
| DP classic | Word Break | 139 | [ ] | DP / trie |
| DP classic | Decode Ways | 91 | [ ] | DP |
| DP classic | Edit Distance | 72 | [ ] | 2D DP |
| DP hard | Super Egg Drop | 887 | [ ] | optimized DP |
| String DP | Longest Palindromic Substring | 5 | [ ] | expand / DP |

### Week 4 — Advanced Data Structures (Segment Tree, Fenwick, DSU, Heaps)

| Topic | Problem | LC # | Status | Notes |
|---|---|---:|:---:|---|
| Segment Tree | Range Sum Query - Mutable | 307 | [ ] | segtree/BIT |
| Segment Tree 2D | Range Sum Query 2D - Mutable | 308 | [ ] | 2D BIT/SegTree |
| Range sums | Count of Range Sum | 327 | [ ] | divide & conquer / BIT |
| Fenwick / order-stat | Count of Smaller Numbers After Self | 315 | [ ] | BIT / merge sort |
| DSU | Accounts Merge | 721 | [ ] | DSU + map |
| DSU / graph | Number of Provinces | 547 | [ ] | DSU / BFS |
| DSU / cycle | Redundant Connection | 684 | [ ] | DSU |
| Heap / median | Find Median from Data Stream | 295 | [ ] | two heaps |
| Heap / median | Sliding Window Median | 480 | [ ] | balanced heaps |
| KNN / heap | K Closest Points to Origin | 973 | [ ] | heap / quickselect |
| Skyline / heap | The Skyline Problem | 218 | [ ] | sweep line + heap |

### Week 5 — Advanced Graphs (MST, Bridges/Articulation, Bellman-Ford)

| Topic | Problem | LC # | Status | Notes |
|---|---|---:|:---:|---|
| MST / min connect | Min Cost to Connect All Points | 1584 | [ ] | Kruskal / Prim |
| Bridges / critical | Critical Connections in a Network | 1192 | [ ] | Tarjan bridges |
| Cycle / DSU | Redundant Connection | 684 | [ ] | DSU (also in Week 4) |
| Shortest path (negative edges) | Cheapest Flights Within K Stops | 787 | [ ] | Bellman-Ford style |
| Shortest path (Dijkstra) | Network Delay Time | 743 | [ ] | Dijkstra |
| Advanced graph practice | (extra advanced) | — | [ ] | Tarjan / Kosaraju / Prim |

### Week 6 — Mixed + Revision (AtCoder DP subset, contests, review)

| Topic | Problem | LC # | Status | Notes |
|---|---|---:|:---:|---|
| AtCoder DP subset | AtCoder DP practice | n/a | [ ] | map problems to LC equivalents |
| Timed contests | LeetCode Weekly/Biweekly | n/a | [ ] | attempt 2 contests/week |
| Hard practice | Shortest Palindrome | 214 | [ ] | string algorithms |
| Hard practice | Median of Two Sorted Arrays | 4 | [ ] | binary search on partitions |
| Hard practice | Serialize and Deserialize Binary Tree | 297 | [ ] | tree traversal |

Notes & tips
- Target counts per week: Week1 ≥20, Week2 15–20, Week3 ≈20, Week4 ≈15, Week5 ≈15, Week6 mixed/contests.
- For each problem: write template + solve from memory at least once per weekend.
- Keep a Mistakes Log: record patterns, pitfalls, and one-line corrective notes.

Happy practicing — use this map as a checklist and adapt problem selection to your weak areas.